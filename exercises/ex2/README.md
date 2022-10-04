# Exercise 2 - Play around with SAP Event Mesh in a pre-configured scenario


In this exercise, we will explore an event-driven end-to-end architecture in a pre-configured scenario. We will log into SAP Event Mesh and look at our queue and the respective queue subscription. In a next step we will create a test queue and a queue subscription. We will then open our shared extension application. Next, we will update our business partner in SAP S/4HANA and as a result trigger an event. We can now see how this event immediately disappears from our queue, and can look at it in detail in our test queue. Next, we can see that the customer/business partner has been added to the extension application.

## Exercise 2.1 - Log into SAP Event Mesh and make yourself familira with it

After completing these steps you will have logged into SAP Event Mesh and will have explored it.

## Exercise 2.2 - Create a queue and a topic subscription in SAP Event Mesh

After completing these steps you wwill have looked at the queue of your extension application and will have created a queue and a topic subscription.

## Exercise 2.3 - Explore the Extension Application

After completing these steps you will have gained a quick impression of an extension application on the SAP BTP.

## Exercise 2.4 - Trigger an event and follow the flow all the way from SAP S/4HANA to the extension application

After completing these steps you will have triggered an event in SAP S/$HANA by updating a business partner, have explored the event from the test queue and have seen how the business partner has been distributed to the extension application in near real time

## Summary

You have now:

- triggered a business partner event from SAP S/4HANA Cloud
- created a queue and a topic subscription in SAP Event Mesh
- have explored the BusinessPartner.changed event in your test queue
- have seen the updated customer added to the extension application

Continue to - [Exercise 3 - Connect SAP Event Mesh to Advanced Event Mesh](../ex3/README.md)
