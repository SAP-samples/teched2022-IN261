# Exercise 3 - Connect SAP Event Mesh to Advanced Event Mesh

In this exercise, we will setup a connection from SAP Event Mesh to SAP Integration Suite, advanced event mesh

## Exercise 3.1 - Create a queue and a topic subscription

After completing these steps you will have created a queue and a topic subscription to use as a basis for the connectivity to Advanced Event Mesh.

In the end, these are the same steps you have performed before, just not for a test queue but for a queue used for Advanced Event Mesh connectivity from SAP Event Mesh.

1. Go to your Message Client (IN261_Consumer) and select Queues

![Pic 1](/./images/IN261-ex3-1.png)

2. Click on Create Queue. The Create a New Queue pop up becomes visible.

3. Enter IN261_aemconnect_*** into Queue Name (replace *** with your number)

![Pic 2](/./images/IN261-ex3-2.png)

4. Click Create

5. Find the queue you just created in the list.

6. In the overview table, behind your queue, click Actions

![Pic 3](/./images/IN261-ex3-3.png)

7. In the drop down select Queue Subscriptions. This opens up the Queue Subsciptions menu.

8. Copy the following into Topic: sap/S4HANAOD/S4HC/ce/sap/s4/beh/businesspartner/v1/BusinessPartner/Changed/v1	

HINT: make sure you copied this exactly and there are no spaces etc 

9. Click Add

![Pic 4](/./images/IN261-ex3-4.png)

10. You should see the topic added under Subscribed Topic Name

11. Copy the following into Topic: sap/S4HANAOD/S4HC/ce/sap/s4/beh/businesspartner/v1/BusinessPartner/Created/v1

![Pic 5](/./images/IN261-ex3-5.png)

12. Click Add

Now you should see both topics under Subscribed Topic Name.

![Pic 6](/./images/IN261-ex3-6.png)

13. Click Close

![Pic 7](/./images/IN261-ex3-7.png)

You have no created a queue and a queue subscription that we will use for Advanced Event Mesh connectivity.

## Exercise 3.2 - Log into Advanced Event Mesh and explore it

After completing these steps you will familiarized yourself with AEM.

1. Log into Advanced Event Mesh

Link: https://eu10.console.pubsub.em.services.cloud.sap/login?zone-id=908a280d-c2f1-4d2b-b003-de94ffc5a4ee

User: in261-***@education.cloud.sap (replace *** with your user number)

Password: see whiteboard
  
2. Explore Advanced Event Mesh  

![Pic 8](/./images/IN261-ex3-8.png)

- check out the different areas in the Advanced Event Mesh cockpit like Mission Control, Event Portal and Event Insights
- just have a quick glimpse here and there to understand the three different areas offered: Event Streaming, Event Management and Event Insights

## Exercise 3.3 - Create a queue in Advanced Event Mesh

After completing these steps you will have created a queue in Advanced Event Mesh and will have collected the required data to create a webhook in SAP Event Mesh.
  
1. Click on Cluster Manager on the left
  
![Pic 9](/./images/IN261-ex3-9.png)  
  
2. In the All Services screen click on the TechEd Las Vegas: Europe Tile (Frankfurt)
  
![Pic 10](/./images/IN261-ex3-10.png)    
  
HINT: If you cannot see the tiles, uncheck the Only show my services box
  
3. Click in Manage
  
![Pic 11](/./images/IN261-ex3-11.png)     
  
4. Under Broker Manager Quick Setting click the Queues tile. A new window opens up.
  
![Pic 12](/./images/IN261-ex3-12.png)      
  
5. Click the +Queue button on the top right
  
![Pic 13](/./images/IN261-ex3-13.png)        
  
6. In the pop up enter the queue name: IN261_aemconnect_*** (replace *** with your number)
  
7. Click Create
  
![Pic 14](/./images/IN261-ex3-14.png)      
  
8. On the next screen click Apply
  
![Pic 15](/./images/IN261-ex3-15.png)      
  
9. Check whether you can find your queue in the list  

![Pic 16](/./images/IN261-ex3-16.png)   

10. Click on your queue

11. Click on Subscriptions

![Pic 17](/./images/IN261-ex3-17.png)  

12. Click on +Subscription

13. Enter your topic into the field. Use IN261_aemconnect_***_topic (replace *** with your number)

![Pic 18](/./images/IN261-ex3-18.png)  

14. Click on Create

15. Check on whether your queue subscription got created

![Pic 19](/./images/IN261-ex3-19.png)  

## Exercise 3.4 - Create a webhook to send events to Advanced Event Mesh

Now you will create a webhook to send events from SAP Event Mesh to Advanced Event Mesh.

1. In Advanced Event Mesh, go to the overview window again (HINT: remember that a second browser window got opened; go to the parent window)
  
2. Click on Connect
  
![Pic 20](/./images/IN261-ex3-20.png)     
  
3. Click on REST and expand the details
  
![Pic 21](/./images/IN261-ex3-21.png)      
  
4. Keep this browser window open. You will have to copy data over into SAP Event Mesh.
  
5. Go to SAP Event Mesh
  
6. Click on Webhooks
  
![Pic 22](/./images/IN261-ex3-22.png)       
  
7. Click on Create Webhook. This opens a popoup.
  
![Pic 23](/./images/IN261-ex3-23.png)     
  
8. Into the Subscription Name field enter: IN261_aemconnect_*** (replace *** with your number)
  
![Pic 24](/./images/IN261-ex3-24.png)      
  
9. Select your queue from the drop down in Queue Name
  
10. Exempt Handshake: set to YES by clicking on the button
  
11. Go to Advanced Event Mesh and copy the Webhook URL. You can click on the copy icon behind Secured Web Messaging Host / Public Internet.
  
12. Paste this into SAP Event Mesh - Webhook URL
  
13. Change Authentication to Basic Authentication
  
14. Go to Advanced Event Mesh 
  
15. Copy User Name by clicking on the copy icon
  
16. Go to Event Mesh and paste the user name into user  
  
17. Go to Advanced Event Mesh 
  
18. Copy Password by clicking on the copy icon
  
19. Go to Event Mesh and paste the password into Password

20. Now go back to the Webhook URL field

21. Add /Topic/IN261_aemconnect_***_topic (replace *** with your number) behind the Webhook URL you had pasted there

This will post the event to the topic IN261_aemconnect_***_topic . Make sure this matches the topic you have entered into the queue subscription in Advanced Event Mesh. 
  
![Pic 25](/./images/IN261-ex3-25.png)      
  
20. Click on create 

![Pic 26](/./images/IN261-ex3-26.png)    
  
21. Check that your webhook got created by finding it in the list. Make sure the webhook is active and the handshake exempted.  
  
## Summary

You have now setup the one-directional connectivity between SAP Event Mesh and SAP Advanced Event Mesh 

Continue to - [Exercise 4 - Consume Event in Advanced Event Mesh](../ex4/README.md)


