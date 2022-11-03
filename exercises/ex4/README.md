# Exercise 4 - Consume Event in Advanced Event Mesh

In this exercise, we will consume an event from our queue in SAP Integration Suite, advanced event mesh. For that we will use the Queue Consumer HTML/JS application and you will connect against the AEM broker your have connected to SAP Event Mesh

## Exercise 4.1 Start your Queue Consumer Application and connect to Advanced Event Mesh

After completing these steps you will have connected your Queue Consumer application to Advanced Event Mesh

1. As part of the Getting Started you have downloaded or cloned the basic samples from GitHub. Go to the folder that you have downloaded or cloned to.

2. Go to teched2022-IN261-main

3. Go to the directory tools/AEM Samples/src/basic-samples/QueueConsumer


![Pic 1](/./images/IN261-ex4-1.png)

4. Open up the QueueConsumer.html file with an editor

5. Go to the line

        // create the consumer, specifying name of the queue
        subscriber = new QueueConsumer('AEMCONNECT1');
        
and replace AEMCONNECT001 with the name of your queue in Advanced Event Mesh, which should be AEMCONNECT*** where ** is your individual number.

![Pic 2](/./images/IN261-ex4-2.png)

6. Save the file after you have made the changes.

7. Double click on QueueConsumer.html. The Queue Consumer app opens up.

![Pic 3](/./images/IN261-ex4-3.png)

8. Go to Advanced Event Mesh

9. Click on Cluster Manager

![Pic 4](/./images/IN261-ex4-4.png)

10. Click on the tile for TechEd Las Vegas (Frankfurt)

![Pic 5](/./images/IN261-ex4-5.png)

11. Click on Connect

![Pic 6](/./images/IN261-ex4-6.png)

12. Expand Solace Web Messaging (ensure this - REST as before will not work)

![Pic 7](/./images/IN261-ex4-7.png)

13. Copy Username, Password, Message VPN and Secured Web Messaging Host into the respective fields of your Queue Consumer

14. In the Queue Consumer, click Connect. 

![Pic 8](/./images/IN261-ex4-8.png)

You should get a success message indicating that the connection has worked.

![Pic 9](/./images/IN261-ex4-9.png)

## Exercise 4.2 Consume and explore events in Queue Consumer 

After completing these steps you will have consumed events using the Queue Consumer

1. In order to consumer messages from your queue, click on *Consume Messages*. If you would like to stop consuming later on, click *Stop Consuming*.

![Pic 10](/./images/IN261-ex4-10.png)

2. In case there were events in your queue, they automatically get consumed.

3. Go back to the SAP S/4HANA system and update your BusinessPartner. If everything works, you should now receive the BusinessPartner.changed event in your Queue consumer.

![Pic 11](/./images/IN261-ex4-11.png)

## Summary

You have now connected your queue consumer to your queue in Advanced Event Mesh and have consumed your first events

Continue to - [Exercise 5 - Explore a mesh spanning three continents in AEM](../ex5/README.md)


