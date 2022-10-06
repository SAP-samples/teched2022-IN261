# Exercise 1 - Explore Standard Events in SAP S/4HANA Cloud (optional)

THIS IS AN OPTIONAL EXERCISE TO PROVIDE YOU WITH A REAL END-TO-END VIEW. IT PROVIDES YOU WITH A BACKGROUND ON SAP S/4HANA EVENTS.

We will look for and at Business Partner events on the SAP API Business Hub and will see how to enable these events in SAP S/4HANA. 

## Exercise 1.1 - Look up the BusinessPartner events in SAP API Business Hub (optional)

You will see how easy it is to look up available events in the SAP API Business Hub. Overall, SAP API Business Hub provides you with information on standard APIs and events available for selected SAP backends.

1. In order to explore available events, go to the SAP Api Business Hub: http://api.sap.com
2. Now you can take different tracks - we will take the SAP S/4HANA Cloud path. Under Choose products to explore, click on S/4HANA
3. On the next screen, click on Events
4. Now you can just scroll down to the Business Partner Events tile.
5. Click on the tile. This will take you to the Event Overview page.
6. Click on Event References
7. Now you can select your event on the left (Changed, Created) or click into the green box to expand the event description. You will see the Request body with example values.

![API Business Hub](/./images/IN261-ex1-1.png)

8. Click on Schema to see the Schema

## Exercise 1.2 - Explore switching events on in SAP S/4HANA (optional)

Now we will look at how to switch events on in SAP S/4HANA.

HINT: the environment is pre-configured to expose events. We will use a shared channel to explore this feature.

1. Log into SAP S/4HANA Cloud using the below link and your user an password.
2. Click on the Enterprise Event Enablement Tile (under Enterprise Event Enablement)

![Enterprise Event Enablement](/./images/IN261-ex1-2.png)

3. Click Go
4. Select our example channel SAP_CP_XF_EXAMPLE by clicking on the arrow behind the name
5. You should see the Business Partner events enabled in the Outbound Topics section
6. Click on Create
7. On the Outbound Topics page, expand the selection box for topic and check on the available events in the system by simply scrolling down
8. Select an Outbound Topic
9. Click Create
10. You will see the topic assigned
11. Mark the topic you have added using the checkbox and click Delete
12. Confirm the deletion by clicking Delete
13. Go back to Home

## Summary

You have now:

- explored a SAP S/4HANA standard notification event in SAP API Business Hub
- you have assigned an event to a channel
- you have deleted this event again

Continue to - [Exercise 2 - Play around with SAP Event Mesh in a pre-configured scenario](../ex2/README.md)

