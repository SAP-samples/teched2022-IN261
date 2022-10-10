# Exercise 3 - Connect SAP Event Mesh to Advanced Event Mesh

In this exercise, we will setup a connection from SAP Event Mesh to SAP Integration Suite, advanced event mesh

## Exercise 3.1 - Create a queue and a topic subscription

After completing these steps you will have created a queue and a topic subscription to use as a basis for the connectivity to Advanced Event Mesh.

In the end, these are the same steps you have performed before, just not for a test queue but for a queue used for Advanced Event Mesh connectivity.

After completing these steps you will have looked at the queue of your extension application and will have created a queue and a topic subscription.

1. Click on Create Queue. The Create a New Queue pop up becomes visible.

2. Enter IN261-aemconnect** into Queue Name (replace ** with your number)

3. Click Create

4. Find the queue you just created in the list.

5. In the overview table, behind your queue, click Actions

6. In the drop down select Queue Subscriptions. This opens up the Queue Subsciptions menu.

7. Copy the following into Topic: sap/S4HANAOD/1406/ce/sap/s4/beh/businesspartner/v1/BusinessPartner/Changed/v1	

HINT: make sure you copied this exactly and there are no spaces etc 

8. Click Add

9. You should see the topic added under Subscribed Topic Name

10. Copy the following into Topic: sap/S4HANAOD/1406/ce/sap/s4/beh/businesspartner/v1/BusinessPartner/Created/v1	

11. Click Add

Now you should see both topics under Subscribed Topic Name.

12. Click Close

You have no created a queue and a queue subscription that we will use for Advanced Event Mesh connectivity.

## Exercise 3.2 - Log into Advanced Event Mesh and explore it

After completing these steps you will familiarized yourself with AEM.

## Exercise 3.3 - Create a queue in Advanced Event Mesh

After completing these steps you will have created a queue in Advanced Event Mesh and will have collected the required data to create a webhook in SAP Event Mesh.

## Exercise 3.4 - Create a webhook to send events to Advanced Event Mesh

After completing these steps you will have created a webhook to send events from SAP Event Mesh to Advanced Event Mesh.

## Summary

You have now setup the one-directional connectivity between SAP Event Mesh and SAP Advanced Event Mesh 

Continue to - [Exercise 4 - Consume Event in Advanced Event Mesh](../ex4/README.md)


