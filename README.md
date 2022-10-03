# IN261 - Experience Event-Driven Integrations Hands-On with SAP Integration Suite

## Description

Build an end-to-end integration scenario and gain hands-on experience with SAP's event brokers, namely the SAP Event Mesh capability and SAP Integration Suite, advanced event mesh.


![I want my ERP to be a Team Player](./images/TechEd IN261 1.png)

## Overview

This session allows you to get an end-to-end impression of event-driven architecture hands-on. Starting from the event source, you will follow the flow of outbound events via the event broker to the event consumer.

As an event source we will use SAP S/4HANA Cloud. SAP Event Mesh and SAP Integration Suite, advanced event mesh will be our event brokers, and events are consumed by a BTP based SAP Fiori Elements extension application and an HTML/JS based event consumer. 

The session will be broad rather than deep, with the goal to provide a highspeed end-to-end experience, with a specific focus on our new event broker SAP Integration Suite, advanced event mesh. You will be able to experience basic and advanced features of SAP Event Mesh and specifically SAP Integration Suite, advanced event mesh.

Features touched, some just shortly, some in more detail, include:

- SAP S/4HANA Cloud standard notification events
- SAP S/4HANA Cloud RAP based events
- SAP Event Mesh queues 
- SAP Event Mesh queue subscriptions
- SAP Event Mesh webhooks
- SAP Event Mesh test tool
- SAP Integration Suite, advanced event mesh queues
- SAP Integration Suite, advanced event mesh Cluster Manager 
- SAP Integration Suite, advanced event mesh Mesh Manager 
- SAP Integration Suite, advanced event mesh Event Insights and Event Management

## Scenario Setup

As a call center employee your job is to follow up on newly created customers and customers for which information has been updated. You would like to do this for all customers in selected focus regions. You have no access the the SAP S/4HANA system in which the business partners are maintained, would still need to be able to work on real time data. The solution to this is a Fiori Elements based extension application on the SAP Business Technology Platform, that is, based on SAP S/4HANA business events, informed on business partner events and updated in real time.

This scenario sounds familiar? This is a popular SAP Discovery Center mission that we will use as a basis to look into SAP Event Mesh and SAP S/4HANA notification events. 

The mission has been very successful, so has been the business case. Therefore the call center has decided to expand on a global level and open a second call center to work on customers in specific focus regions. Instead of a single event broker, in order to handle the global setup and the higher load we would use a mesh of event brokers - an event mesh - and dynamic message routing and filtering. 

For this more demanding scenario we will use SAP Integration Suite, advanced event mesh and we will build a mesh of two event brokers. As an event consumer we will use a simple HTML/JS based event consumer that will allow for further exploration.

## Requirements

- Understanding the basics of event-driven architectures, namely events, queues, topics, event subscriptions
- You would be able to execute most of the excercises without prior experience, for taking value out of the chance to explore the brokers some experience with event-driven architectures is recommended

## Exercises

In the following, the complete list of exercise steps are listed. Run through them in the given order. You can use this section as an index or table of contents. Use the breadcrumb navigation on top of the pages to go back to the Table of Contents.

- [Getting Started](exercises/ex0/)
- [Exercise 1 - First Exercise Description](exercises/ex1/)
    - [Exercise 1.1 - Exercise 1 Sub Exercise 1 Description](exercises/ex1#exercise-11-sub-exercise-1-description)
    - [Exercise 1.2 - Exercise 1 Sub Exercise 2 Description](exercises/ex1#exercise-12-sub-exercise-2-description)
- [Exercise 2 - Second Exercise Description](exercises/ex2/)
    - [Exercise 2.1 - Exercise 2 Sub Exercise 1 Description](exercises/ex2#exercise-21-sub-exercise-1-description)
    - [Exercise 2.2 - Exercise 2 Sub Exercise 2 Description](exercises/ex2#exercise-22-sub-exercise-2-description)


## How to obtain support

Support for the content in this repository is available during the actual time of the online session for which this content has been designed. Otherwise, you may request support via the [Issues](../../issues) tab.

## License
Copyright (c) 2022 SAP SE or an SAP affiliate company. All rights reserved. This project is licensed under the Apache Software License, version 2.0 except as noted otherwise in the [LICENSE](LICENSES/Apache-2.0.txt) file.
