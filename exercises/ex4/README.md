# Exercise 4 - Consume Event in Advanced Event Mesh

In this exercise, we will consume an event from our queue in SAP Integration Suite, advanced event mesh. For that we will use the Queue Consumer HTML/JS application and you will connect against the AEM broker your have connected to SAP Event Mesh

## Exercise 4.1 Start your Queue Consumer Application and connect to Advanced Event Mesh

After completing these steps you will have connected your Queue Consumer application to Advanced Event Mesh

1. As part of the Getting Started you have downloaded or cloned the basic samples from GitHub. Go to the folder that you have downloaded or cloned to.

2. Go to teched2022-IN261-main

3. Go to the directory tools/AEM Samples/src/basci-samples/QueueConsumer

4. Open up the QueueConsumer.html file with an editor

5. Go to the line

        // create the consumer, specifying name of the queue
        subscriber = new QueueConsumer('AEMCONNECT1');
        
and replace AEMCONNECT1 with the name of your queue in Advanced Event Mesh, which should be AEMCONNECT** where ** is your individual number.

6. Save the file after you have made the changes.

7. Double click on QueueConsumer.html. The Queue Consumer app opens up.

8. Go to Advanced Event Mesh

9. Click on Cluster Manager

10. Click on the tile for TecEd Las Vegas (Frankfurt)

11. Click on Connect

12. Expand Solace Web Messaging (ensure this - REST as before will not work)

13. Copy Username, Password, Message VPN and Secured Web Messaging Host into the respective fields of your Queue Consumer

14. In the Queue Consumer, click Connect. You should get a success message indicating that the connection has worked.

## Exercise 4.2 Consume and explore events in Queue Consumer 

After completing these steps you will have consumed events using the Queue Consumer

1. In order to consumer messages from your queue, click on *Consume Messages*. If you would like to stop consuming later on, click *Stop Consuming*.

2. In case there were events in your queue, they automatically get consumed.

2. Go back to the SAP S/4HANA system and update your BusinessPartner. If everytging works, you should now receive the BusinessPartner.changed event in your Queue consumer.

## Summary

You have now connected your queue consumer to your queue in Advanced Event Mesh and have consumed your first events

Continue to - [Exercise 5 - Set up an event mesh and filtering in AEM](../ex5/README.md)


