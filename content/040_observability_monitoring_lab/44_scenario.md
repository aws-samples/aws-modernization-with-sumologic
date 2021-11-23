---
title: "Lab 2 Scenario"
chapter: true
weight: 10
---

## Lab 2: Tracing in Sumo Coffee App

With more and more modern apps using microservices architecture, it’s difficult to fully understand the actual cause of an outage due to the dynamic nature of the architecture. In this lab, you'll learn how to trace a transaction in Sumo Logic in case of a failure to find out the root cause of the unsuccessful transaction.

Here’s the scenario you are trying to troubleshoot and isolate the root cause. 

Welcome to the Sumo Logic Coffee app that delivers a hot and fast cup of coffee globally in thousands of locations. The app uses Kubernetes platform and the distributed architecture. It uses several microservices like user login, order registration, water service, coffee bean service, and payment service.

1. Typically, a customer orders coffee from the Sumo Logic Coffee app. 
1. Barista turns on the coffee machine. The machine service, in action, connects with water service to check whether the adequate water level is available. 
1. Coffee service is then initiated for preparing the coffee. At the same time, a payment request is sent to the Payment System. 
1. The SQL commands are executed and a bill is generated post the bill amount calculation for the coffee service.

The duration in milli or microseconds is captured while each span of the transaction is completed. With the Span ID and Trace ID, you can track a transaction across multiple microservices the app uses.

#### The Problem to Solve:

Abel, the Coffee Lover orders coffee at 8:45 am using the Coffee App, However, his transaction is unsuccessful. You need to trace the transaction and troubleshoot and address the issue ASAP.
