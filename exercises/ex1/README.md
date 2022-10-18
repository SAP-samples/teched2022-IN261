# Exercise 1 - Explore Standard Events in SAP S/4HANA Cloud (optional)

THIS IS AN OPTIONAL EXERCISE TO PROVIDE YOU WITH A REAL END-TO-END VIEW. IT PROVIDES YOU WITH A BACKGROUND ON SAP S/4HANA EVENTS.

We will look for and at Business Partner events on the SAP API Business Hub and will see how to enable these events in SAP S/4HANA Cloud. 

![Pic 1](/./images/IN261-ex1-1.png)

## Exercise 1.1 - Look up the BusinessPartner events in SAP API Business Hub (optional)

You will see how easy it is to look up available events in the SAP API Business Hub. Overall, SAP API Business Hub provides you with information on standard APIs and events available for selected SAP backends.

1. In order to explore available events, go to the SAP Api Business Hub: http://api.sap.com
2. Now you can take different tracks - we will take the SAP S/4HANA Cloud path. Under Choose products to explore, click on S/4HANA

![Pic 2](/./images/IN261-ex1-2.png)

4. On the next screen, click on Events

![Pic 3](/./images/IN261-ex1-3.png)

6. Now you can just scroll down to the Business Partner Events tile.

![Pic 4](/./images/IN261-ex1-4.png)

8. Click on the tile. This will take you to the Event Overview page.

![Pic 4](/./images/IN261-ex1-5.png)

10. Click on Event References
11. Now you can select your event on the left (Changed, Created) or click into the green box to expand the event description. You will see the Request body with example values.

![Pic 4](/./images/IN261-ex1-6.png)

8. Click on Schema to see the Schema

## Exercise 1.2 - Explore switching events on in SAP S/4HANA (optional)

Now we will look at how to switch events on in SAP S/4HANA.

HINT: the environment is pre-configured to expose events. We will use a shared channel to explore this feature.

1. Log into SAP S/4HANA Cloud using the below link and your user an password.
2. Click on the Enterprise Event Enablement Tile (under Enterprise Event Enablement)

![Enterprise Event Enablement](/./images/IN261-ex1-7.png)

3. Click Go

![Go](/./images/IN261-ex1-8.png)

5. Select our example channel SAP_CP_XF_EXAMPLE by clicking on the arrow behind the name

![Pic 9](/./images/IN261-ex1-9.png)

7. You should see the Business Partner events enabled in the Outbound Topics section

![Pic 10](/./images/IN261-ex1-10.png)

9. Click on Create

![Pic 11](/./images/IN261-ex1-11.png)

11. On the Outbound Topics page, expand the selection box for topic and check on the available events in the system by simply scrolling down

![Pic 12](/./images/IN261-ex1-12.png)

13. Select an Outbound Topic

![Pic 13](/./images/IN261-ex1-13.png)

15. Click Create

![Pic 14](/./images/IN261-ex1-14.png)

17. Click the Back Arrow

![Pic 15](/./images/IN261-ex1-15.png)

19. You will see the topic assigned
20. Mark the topic you have added using the checkbox and click Delete

![Pic 16](/./images/IN261-ex1-16.png)

22. Confirm the deletion by clicking Delete

![Pic 17](/./images/IN261-ex1-17.png)

24. Go back to Home

## Summary

You have now:

- explored a SAP S/4HANA standard notification event in SAP API Business Hub
- you have assigned an event to a channel
- you have deleted this event

Continue to -> [Exercise 2 - Use SAP Event Mesh in a pre-configured scenario](../ex2/README.md)

