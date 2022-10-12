# IN261 - Experience Event-Driven Integrations Hands-On with SAP Integration Suite

![Pic 1](/./images/IN261-1.png)

## Description

Build an end-to-end integration scenario and gain hands-on experience with SAP's event brokers, namely the SAP Event Mesh capability and SAP Integration Suite, advanced event mesh.

Learn how you can improve your situational awareness by having your SAP backends, namely SAP S/4HANA and SAP ECC, act as a real-time teamplayer.

## Overview

This session allows you to get an end-to-end impression of event-driven architecture hands-on. Starting from the event source, you will follow the flow of outbound events via the event broker to the event consumer.

As an event source we will use SAP S/4HANA Cloud. SAP Event Mesh and SAP Integration Suite, advanced event mesh will be our event brokers, and events are consumed by a BTP based SAP Fiori Elements extension application and an HTML/JS based event consumer. 

The session will be broad rather than deep, with the goal to provide a highspeed end-to-end experience, with a specific focus on our new event broker SAP Integration Suite, advanced event mesh. You will be able to experience basic and advanced features of SAP Event Mesh and specifically SAP Integration Suite, advanced event mesh.

During the free flow part towards the end you can use the HTML/JS based event consumer and an HTML/JS based event producer to try out different features of SAP Integration Suite, advanced event mesh.

Features touched, some just shortly, some in more detail, include:

- SAP S/4HANA Cloud standard notification events
- SAP Event Mesh queues 
- SAP Event Mesh queue subscriptions
- SAP Event Mesh webhooks
- SAP Event Mesh test tool
- SAP Integration Suite, advanced event mesh queues
- SAP Integration Suite, advanced event mesh Cluster Manager 
- SAP Integration Suite, advanced event mesh Mesh Manager 
- SAP Integration Suite, advanced event mesh Event Insights 
- SAP Integration Suite, advanced event mesh Eventand Event Management

## Scenario Setup

As a call center employee your job is to follow up on newly created customers and customers for which information has been updated. You would like to do this for all customers in selected focus regions - like the United States for example. As a call center employee, you have no access to the SAP S/4HANA system in which the business partners are maintained, would still need to be able to work on real time data. The solution to this is a Fiori Elements based extension application on the SAP Business Technology Platform, that is, based on SAP S/4HANA business events, informed on business partner events and updated in real time.

![Pic 2](/./images/IN261-2.png)

The scenario sounds familiar? This is a popular SAP Discovery Center mission that we will use as a basis to look into SAP Event Mesh and SAP S/4HANA notification events. The original mission can be found in the [Discovery Center](https://discovery-center.cloud.sap/missiondetail/3156/3192/) . It holds a lot more detail and steps include development and deployment.

The mission has been very successful, so has been the business case. Therefore the call center has decided to expand on a global level and open a second call center in a different part of the world - to work on customers in specific focus regions. Instead of a single event broker, in order to handle the global setup and the higher load, we would use a mesh of event brokers - an event mesh - and dynamic message routing and filtering. 

![Pic 3](/./images/IN261-3.png)

For this more demanding scenario we will use SAP Integration Suite, advanced event mesh and we will build a mesh of two event brokers. As an event consumer we will use a simple HTML/JS based event consumer that will allow for further exploration.

## Requirements

- Understanding the basics of event-driven architectures, namely events, queues, topics, event subscriptions ...
- You would be able to execute most of the excercises without prior experience by just following the descriptions. For taking value out of the chance to explore the brokers, specifically Advanced Event Mesh, some experience with event-driven architectures is recommended.

## Exercises

In the following, the complete list of exercise steps are listed. Run through them in the given order. You can use this section as an index or table of contents. Use the breadcrumb navigation on top of the pages to go back to the Table of Contents. Exercises marked as (optional) can be skipped if wanted.

- [Getting Started](exercises/ex0/)

SAP S/4HANA (optional)

- [Exercise 1 - Explore Standard Events in SAP S/4HANA Cloud (optional)](exercises/ex1/)

    - [Exercise 1.1 - Look up BusinessPartner events in SAP API Business Hub (optional)](exercises/ex1#exercise-11-sub-exercise-1-description)
    - [Exercise 1.2 - Explore events in SAP S/4HANA (optional)](exercises/ex1#exercise-11-sub-exercise-1-description)
   
SAP Event Mesh   
   
- [Exercise 2 - Use SAP Event Mesh in pre-configured scenario](exercises/ex2/)

    - [Exercise 2.1 - Log into SAP Event Mesh and explore](exercises/ex1#exercise-21-sub-exercise-1-description)
    - [Exercise 2.2 - Create a queue and a topic subscription in SAP Event Mesh](exercises/ex1#exercise-22-sub-exercise-1-description)
    - [Exercise 2.3 - Explore the Extension Application](exercises/ex1#exercise-23-sub-exercise-1-description)
    - [Exercise 2.4 - Trigger an event and follow the flow all the way from SAP S/4HANA to the extension application](exercises/ex1#exercise-24-sub-exercise-1-description)
    
SAP Event Mesh and SAP Integration Suite, advanced event mesh 
    
- [Exercise 3 - Connect SAP Event Mesh to Advanced Event Mesh](exercises/ex3/)

    - [Exercise 3.1 - Create a queue and a topic subscription](exercises/ex3#exercise-31-sub-exercise-1-description)
    - [Exercise 3.2 - Log into Advanced Event Mesh and explore it](exercises/ex3#exercise-32-sub-exercise-1-description)
    - [Exercise 3.3 - Create a queue in Advanced Event Mesh](exercises/ex3#exercise-33-sub-exercise-1-description)
    - [Exercise 3.4 - Create a webhook to send events to Advanced Event Mesh](exercises/ex1#exercise-34-sub-exercise-1-description)
    
SAP Integration Suite, advanced event mesh    
    
- [Exercise 4 - Consume Event in Advanced Event Mesh](exercises/ex4/)

    - [Exercise 4.1 - Start your Queue Consumer Application and connect to Advanced Event Mesh](exercises/ex4#exercise-41-sub-exercise-1-description)
    - [Exercise 4.2 - Consume and explore events in Queue Consumer](exercises/ex4#exercise-42-sub-exercise-1-description)
    
- [Exercise 5 - Explore an event mesh spanning two continents in Advanced Event Mesh](exercises/ex5/)

    - [Exercise 5.1 - Create a Queue in your second broker](exercises/ex5#exercise-41-sub-exercise-1-description)
    - [Exercise 5.2 - Consume and explore events in Queue Consumer](exercises/ex5#exercise-42-sub-exercise-1-description)
    
- [Exercise 6 - Start HTML Queue Consumer and consume filtered events](exercises/ex6/)  

    - [Exercise 6.1 - Start a second Queue Consumer and connect against US West broker](exercises/ex6#exercise-61-sub-exercise-1-description)
    - [Exercise 6.2 - Set up Filtering and Consume Filtered Events](exercises/ex6#exercise-62-sub-exercise-1-description) 
   
SAP Integration Suite, advanced event mesh (optional)       
   
- [Exercise 7 - Play around with Advanced Event Mesh (Optional)](exercises/ex7/)  

    - [Exercise 7.1 - Explore Insights](exercises/ex7#exercise-71-sub-exercise-1-description)
    - [Exercise 7.2 - Event Management](exercises/ex6#exercise-72-sub-exercise-1-description) 

## License
Copyright (c) 2022 SAP SE or an SAP affiliate company. All rights reserved. This project is licensed under the Apache Software License, version 2.0 except as noted otherwise in the [LICENSE](LICENSES/Apache-2.0.txt) file.
