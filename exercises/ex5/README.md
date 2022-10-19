# Exercise 5 - Explore an event mesh spanning two continents in Advanced Event Mesh

In this exercise, we will explore an already existing event mesh of three brokers: one in Europe, one on the West coast of the United States and another one in South Asia. 

## Exercise 5.1 Create a Queue in your second broker

After completing these steps you will have created a queue on your second broker.

1. Click on Cluster Manager on the left

![Pic 1](/./images/IN261-ex5-1.png)
  
2. In the All Services screen click on the TechEd Las Vegas Tile (US West)
  
3. Click in Manage
  
![Pic 2](/./images/IN261-ex5-2.png)  
  
4. Under Broker Manager Quick Setting click the Queues tile. A new window opens up.
  
![Pic 3](/./images/IN261-ex5-3.png)    
  
5. Click the +Queue button on the top right
  
![Pic 4](/./images/IN261-ex5-4.png)      
  
6. In the pop up enter the queue name: IN261-aemconnect-** (replace ** with your number)

HINT: you might pick a slightly different name indicating that you are on a different broker, like IN261-aemconnect-**-US. This would require you to adjust your queue consumer though. So if you want to keep it simple, stick to the name you used in the other broker.
    
7. Click Create
  
![Pic 5](/./images/IN261-ex5-5.png)   

8. On the next screen click Apply
  
![Pic 6](/./images/IN261-ex5-6.png)     
  
9. Check whether you can see your queue in the list  

![Pic 7](/./images/IN261-ex5-7.png)     

10. Click on your queue in the list

11. Click on Subscriptions

![Pic 8](/./images/IN261-ex5-8.png)     

12. Click on the button +Subscription

![Pic 9](/./images/IN261-ex5-9.png)   

13. Enter the topic you had created in SAP Event Mesh when creating the webhook. This is most likely: IN261-aemconnect-topic-** (replace ** with your number)

![Pic 10](/./images/IN261-ex5-10.png)   

14. Click Create

![Pic 11](/./images/IN261-ex5-11.png)   

## Exercise 5.2 Consume and explore events in Queue Consumer 

After completing these steps you will have consumed events using the Queue Consumer from the second broker in the Event Mesh, meaning that the events got forwarded in your Mesh

1. Go to your Queue Consumer

2. Click Disconnect

3. Go to Advanced Event Mesh

4. Click on Cluster Manager

5. Click on the tile for TechEd Las Vegas (West US) - ensure this is the second broker, not the one that you just disconnected from

6. Click on Connect

7. Expand Solace Web Messaging (ensure this - REST as before will not work)

8. Copy Username, Password, Message VPN and Secured Web Messaging Host into the respective fields of your Queue Consumer

9. In the Queue Consumer, click Connect. You should get a success message indicating that the connection has worked.

1. In order to consume messages from your queue, click on *Consume Messages*. If you would like to stop consuming later on, click *Stop Consuming*.

2. Go back to the SAP S/4HANA system and update your BusinessPartner. If everything works, you should now receive the BusinessPartner.changed event in your Queue consumer on the second broker.

## Summary

You've now seen what a mesh looks like in Advanced Event Mesh. You consumed the events from a queue on the second broker in the mesh - the one on the US West Coast. The forwarding of events has happened automatically.

Continue to - [Exercise 6 - Start HTML Queue Consumer and consume filtered events](../ex6/README.md)


