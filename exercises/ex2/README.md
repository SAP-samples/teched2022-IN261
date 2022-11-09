# Exercise 2 - Play around with SAP Event Mesh in a pre-configured scenario


Now we will explore an event-driven end-to-end architecture in a pre-configured scenario. First, we will log into SAP Event Mesh and make ourselves familar with it. In a next step we will create a queue and another queue subscription for this queue. Then, we will open our shared extension application. 

![Pre-configured scenario](/./images/IN261-ex2-1.png)

In SAP S/4HANA we will update our business partner and as a result trigger an event. 

We can now see how this event is added to our queue. 

Since the extension application does not consume from our test queue, we can consume the event and look at it. Next, we can see that the customer/business partner has been added to the extension application and that additional data has been collected using an API call to the backend.

## Exercise 2.1 - Log into SAP Event Mesh and make yourself familiar with it

Now we will log into SAP Event Mesh and explored its main features.

1. Click on the link and enter your user and password:

Link: https://in261-8hv3x7zb.authentication.eu10.hana.ondemand.com/login

User: IN261_*** where you replace *** with your user number

Password:

2. You will see the Message Clients. Click on IN261_Consumer.

![Pic 2](/./images/IN261-ex2-2.png)

3. Select Queues. 

![Pic 3](/./images/IN261-ex2-3.png)

You will now see the list of already created queues.

![Pic 4](/./images/IN261-ex2-4.png)

- You should see at least one queue here already that is the pre-created one for connecting the extension application.

- Potentially there are already more that some people have already created. 

## Exercise 2.2 - Create a queue and a queue subscription in SAP Event Mesh

After completing these steps you will have looked at the queue of your extension application and will have created a queue and a topic subscription.

1. Click on Create Queue. The Create a New Queue pop up becomes visible.

![Pic 5](/./images/IN261-ex2-5.png)  
  
2. Enter IN261_test_*** into Queue Name (replace *** with your number)

![Pic 6](/./images/IN261-ex2-6.png)    
  
3. Click Create

4. Find the queue you just created in the list.

5. In the overview table, behind your queue, click Actions

![Pic 7](/./images/IN261-ex2-7.png)      
  
6. In the drop down select Queue Subscriptions. This opens up the Queue Subsciptions menu.

![Pic 8](/./images/IN261-ex2-8.png)       
  
7. Copy the following into Topic: sap/S4HANAOD/S4HC/ce/sap/s4/beh/businesspartner/v1/BusinessPartner/Created/v1

HINT: make sure you copied this exactly and there are no spaces etc 

![Pic 9](/./images/IN261-ex2-9.png)      
  
8. Click Add

9. You should see the topic added under Subscribed Topic Name

10. Copy the following into Topic: sap/S4HANAOD/S4HC/ce/sap/s4/beh/businesspartner/v1/BusinessPartner/Changed/v1	

11. Click Add

Now you should see both topics under Subscribed Topic Name.

![Pic 10](/./images/IN261-ex2-10.png)      
  
12. Click Close

![Pic 11](/./images/IN261-ex2-11.png)        
  
You have now created two queue subscriptions for BusinessPartner.Changed and BusinessPartner.Created events.  
   
## Exercise 2.3 - Explore the Extension Application

After completing these steps you will have gained a quick impression of an extension application on the SAP BTP.

1. Now let's open the extension application. 

Click on: https://geo-kind-turtle-ix.cfapps.eu10-004.hana.ondemand.com/georelApplication.html#Shell-home  

This will open the Home screen of our extension application.

2. Click on the tile GeoRelations

This opens the FioriElements app.

![Pic 12](/./images/IN261-ex2-12.png)    

3. Click on Go to see what customers are already in the app.

![Pic 13](/./images/IN261-ex2-13.png)   

If you want to you can click around some. Click for example on a customer and see what features are available.

![Pic 14](/./images/IN261-ex2-14.png)   

4. Go back to the Customer Processes page of the extension application and keep it open for later use.

This is where you will see additional customers added in real time after clicking the Go button later on.

## Exercise 2.4 - Trigger an event and follow the flow all the way from SAP S/4HANA to the extension application

After completing these steps you will have triggered an event in SAP S/4HANA by updating a business partner, have explored the event from the test queue and have seen how the business partner has been distributed to the extension application in near real time

1. Log into the SAP S/4HANA system 

Link: https://my401666.s4hana.cloud.sap/ui#Shell-home

Log in with the data below:  
  
User: IN261_*** where you replace *** with your user number

Password:

2. Go to the Business Partner Transaction 

![Pic 15](/./images/IN261-ex2-14-2.png) 

- Type Manage Business Partner Master Data into the Apps search field 

- Select Manage Business Partner Master Data in the Drop Down

3. In the Manage Business Partner Transaction type IN261 into the search field

![Pic 15](/./images/IN261-ex2-14-3.png)   

4. Click Go

5. Select the Business Partner below

![Pic 15](/./images/IN261-ex2-14-4.png)   

Note: It is important for the Extension Application that the BusinessPartner has the Customer (FLCU01) role.

6. Click on Copy

![Pic 15](/./images/IN261-ex2-15.png)   

7. Update the first name with your TechEd user (IN261_*** where you replace *** with your user number)

![Pic 16](/./images/IN261-ex2-16.png)   


8. Click Create

Wait for the creation to finish and keep the page open / bookmark this page for later use

You should have raised a BusinessPartner.Created Event. 
  
In the following steps, you will go to SAP Event Mesh and check on your queue and then check that the Business Partner got added to the Extension Application.
  
Note down / remember your BusinessPartnerId  

![Pic 17](/./images/IN261-ex2-17.png)   

9. Go to SAP Event Mesh

10. In case you are still in Event Mesh, click Refresh. If not, go to the Queues list.
  
11. Find your queue. You should now see a number of messages in the queue. This is because everybody has probably already updated their Business Partner and the queue is listening to all Business Partner changes.
  
![Pic 18](/./images/IN261-ex2-18.png)     
  
12. Click on Test
  
![Pic 19](/./images/IN261-ex2-19.png)     
  
13. In the Consume Messages section on the right, select your queue (IN261_test_***) from the pull down menu.
  
![Pic 20](/./images/IN261-ex2-20.png)     
  
14. Click on Consume Message
  
![Pic 21](/./images/IN261-ex2-21.png)       
  
15. Consume the messages until you find your Business Partner Id in the data section   

![Pic 22](/./images/IN261-ex2-22.png)       

16. Go to the Extension Application
  
17. Click Go
  
![Pic 23](/./images/IN261-ex2-23.png)     
  
18. Find your Business Partner under Customer Name and confirm it has been added to the Extension Application. If you want to, you can play around with it some by changing the status etc.  
  
![Pic 24](/./images/IN261-ex2-24.png)     
  
## Summary

You have now:

- triggered a business partner event from SAP S/4HANA Cloud
- created a queue and a topic subscription in SAP Event Mesh
- have explored the BusinessPartner.created event in your queue
- have seen the copied customer added to the extension application

Continue to - [Exercise 3 - Connect SAP Event Mesh to Advanced Event Mesh](../ex3/README.md)
