# Exercise 5 - Explore an event mesh spanning two continents in Advanced Event Mesh

In this exercise, we will explore an already existing event mesh of three brokers: one in Europe, one the United States and another one in Asia. 

## Exercise 5.1 Create a Queue in your second broker

After completing these steps you will have created a queue on your second broker.

1. Click on Cluster Manager on the left

![Pic 1](/./images/IN261-ex5-1.png)
  
2. In the All Services screen click on the TechEd Las Vegas Tile (US)
  
3. Click in Manage
  
![Pic 2](/./images/IN261-ex5-2.png)  
  
4. Under Broker Manager Quick Setting click the Queues tile. A new window opens up.
  
![Pic 3](/./images/IN261-ex5-3.png)    
  
5. Click the +Queue button on the top right
  
![Pic 4](/./images/IN261-ex5-4.png)      
  
6. In the pop up enter the queue name: IN261_aemconnect_*** (replace ** with your number)
    
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

13. Enter the topic you had created in SAP Event Mesh when creating the webhook. This is most likely: IN261_aemconnect_***_topic (replace *** with your number)

![Pic 10](/./images/IN261-ex5-10.png)   

14. Click Create

![Pic 11](/./images/IN261-ex5-11.png)   

## Exercise 5.2 Consume and explore events in Queue Consumer 

After completing these steps you will have consumed events using the Queue Consumer from the second broker in the Event Mesh, meaning that the events got forwarded in your Mesh and have ended up in your queue based on the queue subscription.

1. Go to your Queue Consumer if it is still open and click on Disconnect - in case that it is not open any more, restart it

2. Make sure that it listens to the same queue you have just created in the previous step: IN261_aemconnect_*** (replace ** with your number) 

![Pic 12](/./images/IN261-ex5-12.png)   

If this is not the case, you have to adjust it in your QueueConsumer.html

![Pic 13](/./images/IN261-ex5-13.png)   

3. Go to Advanced Event Mesh

4. Click on Cluster Manager

![Pic 14](/./images/IN261-ex5-14.png)   

5. Click on the tile for TechEd Las Vegas (US) - ensure this is the second broker, not the one that you just disconnected from

![Pic 15](/./images/IN261-ex5-15.png)   

6. Click on Connect

![Pic 16](/./images/IN261-ex5-16.png)   

7. Expand Solace Web Messaging (ensure this - REST as before will not work)

![Pic 17](/./images/IN261-ex5-17.png)   

8. Copy Username, Password, Message VPN and Secured Web Messaging Host into the respective fields of your Queue Consumer

![Pic 18](/./images/IN261-ex5-18.png)   

9. In the Queue Consumer, click Connect. You should get a success message indicating that the connection has worked.

![Pic 19](/./images/IN261-ex5-19.png)   

10. In order to consume messages from your queue, click on *Consume Messages*. If you would like to stop consuming later on, click *Stop Consuming*.

11. Go back to the SAP S/4HANA system and update your BusinessPartner. 

12. If everything works, you should now receive the BusinessPartner.changed event in your Queue consumer on the second broker.

![Pic 20](/./images/IN261-ex5-20.png)   

## Exercise 5.3 Consume events via a topic

After completing these steps you will have consumed events via a topic from the third broker in the Event Mesh. You will use the Try Me ! feature of Advanced Event Mesh for this.

1. Go to the cluster manager and select the third broker.

![Pic 21](/./images/IN261-ex5-21.png)   

2. Click Try Me !

![Pic 22](/./images/IN261-ex5-22.png)   

3. In the Subscriber section, click on show advanced settings

![Pic 23](/./images/IN261-ex5-23.png)   

4. Fill the data in the Establish connection section. You can get this data in the connect part like before. Go to Connect and the Solace Web Messaging section. 

![Pic 24](/./images/IN261-ex5-24.png)   

5. Copy the Connection Details and fill them into the fields in Try Me !

![Pic 25](/./images/IN261-ex5-25.png)   

6. Click on Connect

![Pic 26](/./images/IN261-ex5-26.png)   

7. Fill your topic into Subscribe Add Topic

Your topic should be IN261_aemconnect_***_topic where you replace *** with your number

![Pic 27](/./images/IN261-ex5-27.png)   

8. Click on Subscribe

You should see your topic in Subscribed Topics

9. Go back to the S/4HANA system and trigger an event by changing the Business Partner

10. You should see your event in the messages section

![Pic 28](/./images/IN261-ex5-28.png)   

## Summary

You've now seen what a mesh looks like in Advanced Event Mesh. You consumed the events from a queue on the second broker in the mesh - the one on the US West Coast. The forwarding of events has happened automatically based on the topic that the queue is subscribed to.

You can easily extend this to the third broker by following the same procedure described above ...

Continue to - [Exercise 6 - Play Around with Advanced Event Mesh (optional)](../ex6/README.md)


