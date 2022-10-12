# Exercise 5 - Explore an event mesh spanning two continents in Advanced Event Mesh

In this exercise, we will explore an already existing event mesh of two brokers: one in Europe, one on the West coast of the United States. 

## Exercise 5.1 Explore an Event Mesh of two brokers

After completing these steps you will have seen what an event mesh looks like in Advanced Event Mesh.

1. Go to your Queue Consumer

2. Click Disconnect

3. Go to Advanced Event Mesh

4. Click on Cluster Manager

5. Click on the tile for TechEd Las Vegas (West US) - ensure this is the second broker, not the one that you just disconnected from

6. Click on Connect

7. Expand Solace Web Messaging (ensure this - REST as before will not work)

8. Copy Username, Password, Message VPN and Secured Web Messaging Host into the respective fields of your Queue Consumer

9. In the Queue Consumer, click Connect. You should get a success message indicating that the connection has worked.

## Exercise 5.2 Consume and explore events in Queue Consumer 

After completing these steps you will have consumed events using the Queue Consumer from the second broker in the Event Mesh, meaning that the events got forwarded in your Mesh

1. In order to consume messages from your queue, click on *Consume Messages*. If you would like to stop consuming later on, click *Stop Consuming*.

2. Go back to the SAP S/4HANA system and update your BusinessPartner. If everything works, you should now receive the BusinessPartner.changed event in your Queue consumer on the second broker.

## Summary

You've now seen what a mesh looks like in Advanced Event Mesh. You consumed the events from the second broker in the mesh.

Continue to - [Exercise 6 - Start HTML Queue Consumer and consume filtered events](../ex6/README.md)


