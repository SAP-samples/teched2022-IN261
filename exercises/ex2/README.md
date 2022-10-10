# Exercise 2 - Play around with SAP Event Mesh in a pre-configured scenario


Now we will explore an event-driven end-to-end architecture in a pre-configured scenario. First, we will log into SAP Event Mesh and look at our queue and the respective queue subscription. In a next step we will create a test queue and another queue subscription for this queue. Then, we will open our shared extension application. 

![Pre-configured scenario](/./images/IN261-ex2-1.png)

In SAP S/4HANA we will update our business partner and as a result trigger an event. We can now see how this event is added to our queue and then almost immediately disappears from our queue. Since the extension application does not consume from our test queue, we can consume the event and look at it. Next, we can see that the customer/business partner has been added to the extension application and that additional data has been collected using an API call to the backend.

## Exercise 2.1 - Log into SAP Event Mesh and make yourself familiar with it

Now we will have log into SAP Event Mesh and explored its main features.

1. Click on the link and enter your user and password:

Link: https://georel.enterprise-messaging.cfapps.eu10.hana.ondemand.com/cockpit/#/home/message-clients

User: TechEd-IN261-** where you replace ** with your user number
Password: <PASSWORD>

2. You will see the Message Clients. Click on EMGeo.

3. Select Queues. You will now see the list of already created queues.

- You should see at least one queue here already that is the pre-created one for connecting the extension application.

- Potentially there are already more that some people have already created. 

## Exercise 2.2 - Create a queue and a queue subscription in SAP Event Mesh

After completing these steps you will have looked at the queue of your extension application and will have created a queue and a topic subscription.

1. Click on Create Queue. The Create a New Queue pop up becomes visible.

2. Enter aemconnect** into Queue Name (replace ** with your number)

3. Click Create

4. Find the queue you just created in the list.

5. In the overview table, behind your queue, click Actions

6. In the drop down select Queue Subscriptions. This opens up the Queue Subsciptions menu.

7. Copy the following into Topic: sap/S4HANAOD/1406/ce/sap/s4/beh/businesspartner/v1/BusinessPartner/Changed/v1	

HINT: make sure you copied this exactly and there are no spaces etc 

8. Click Add

9. You should see the topic added under Subscribed Topic Name

10. Copy the following itno Topic: sap/S4HANAOD/1406/ce/sap/s4/beh/businesspartner/v1/BusinessPartner/Created/v1	

11. Click Add

Now you should see both topics under Subscribed Topic Name.

12. Click Close

## Exercise 2.3 - Explore the Extension Application

After completing these steps you will have gained a quick impression of an extension application on the SAP BTP.

1. Now let's open the extension application. Click on: https://geo.cfapps.eu10.hana.ondemand.com/georelApplication.html#Shell-home 

This will open the Home screen of our extension application.

2. Click on the tile GeoRelations

This opens the FioriElements app.

3. Click on Go to see what customers are already in the app.

If you want to you can click around some. Click for example on a customer and see what features are available.

4. Go back to the customer processes page and keep it open.

This is where you will see additional customers added in real time after clicking the Go button later on.

## Exercise 2.4 - Trigger an event and follow the flow all the way from SAP S/4HANA to the extension application

After completing these steps you will have triggered an event in SAP S/$HANA by updating a business partner, have explored the event from the test queue and have seen how the business partner has been distributed to the extension application in near real time

1. Log into the SAP S/4HANA system and go directly to the Manage Business Partner transaction:

Link: https://my304263.s4hana.ondemand.com/ui#BusinessPartner-manage&/C_BusinessPartner(BusinessPartner='1000746',DraftUUID=guid'00000000-0000-0000-0000-000000000000',IsActiveEntity=true)/?sap-iapp-state--history=TASFB1VS4H9SGATPI3LCD98WALG3XL069FF6NMDG1

User: TechEd-IN261-** where you replace ** with your user number
Password: <PASSWORD>

2. Click on Copy

3. Update the Last name with your TechEd user (TechEd-IN261-** where you replace ** with your user number)

4. Click Create

Wait for the creation to finish and keep the page open / bookmark this page for later use

You should have raised a BusinessPartner Create Event. Go to Event Mesh and check on your queue and then check that the Business Partner got added to the Extension Application.

5. Go to SAP Event Mesh

6. In case you are still in Event Mesh, click Refresh. If not, go to the Queues list.


## Summary

You have now:

- triggered a business partner event from SAP S/4HANA Cloud
- created a queue and a topic subscription in SAP Event Mesh
- have explored the BusinessPartner.changed event in your test queue
- have seen the updated customer added to the extension application

Continue to - [Exercise 3 - Connect SAP Event Mesh to Advanced Event Mesh](../ex3/README.md)
