---
created: 2024-02-08T16:48:21 (UTC +01:00)
tags: []
source: https://learn.microsoft.com/en-us/training/modules/describe-azure-compute-networking-services/6-functions
author: wwlpublish
---

# Describe Azure functions - Training | Microsoft Learn

> ## Excerpt
> Describe Azure functions

---
-   4 minutes

Azure Functions is an event-driven, serverless compute option that doesn’t require maintaining virtual machines or containers. If you build an app using VMs or containers, those resources have to be “running” in order for your app to function. With Azure Functions, an event wakes the function, alleviating the need to keep resources provisioned when there are no events.

## Serverless computing in Azure

![[video002.mp4]]
transcript
In this video we'll discuss what we mean by serverless computing, let's begin.
As a software developer you want to spend time doing what matters, building your application.
You don't want to spend your time executing tedious, time-consuming tasks
like installing an operating system or downloading system updates.
The goal of serverless computing is to help you with this by taking care of those tiresome types of server management tasks,
so that you can focus your effort on getting you application to your customers.
Serverless computing is a bit of a misleading name, because there are in fact servers being used.
But what it really means is that the responsibility of managing servers is already handled for you.
In other words, it's an abstraction of servers so that you can take your mind
off of infrastructure concerns and focus them on developer concerns.
There are 3 big benefits of using serverless approach.
First, there's no infrastructure management.
And as a business you don't have to focus on administrative tasks
like installing an operating system, instead, you simply deploy your code and it automatically runs with high availability.
The second benefit is scalability and as your application grows in popularity,

your application will continue working under any workload.
Serverless computers can scale from nothing to tens of thousands of requests without any configuration.
Finally, the third benefit is that you only pay for what you use.
Serverless computing is event driven, resources are only allocated from a direct action.
You are only charged for the time that takes to run your code instead of paying for the resources if they're not being used.

Time is money in the business world, you want to be focusing your time on what matters.
Using Azure to support serverless computing through products like Azure functions,
your main job will simply be to upload your code and you automatically get the benefits of infrastructure management and scalability

plus a payment model that will only charge you for what you use.

## Benefits of Azure Functions

Using Azure Functions is ideal when you're only concerned about the code running your service and not about the underlying platform or infrastructure. Functions are commonly used when you need to perform work in response to an event (often via a REST request), timer, or message from another Azure service, and when that work can be completed quickly, within seconds or less.

Functions scale automatically based on demand, so they may be a good choice when demand is variable.

Azure Functions runs your code when it's triggered and automatically deallocates resources when the function is finished. In this model, you're only charged for the CPU time used while your function runs.

Functions can be either stateless or stateful. When they're stateless (the default), they behave as if they're restarted every time they respond to an event. When they're stateful (called Durable Functions), a context is passed through the function to track prior activity.

Functions are a key component of serverless computing. They're also a general compute platform for running any type of code. If the needs of the developer's app change, you can deploy the project in an environment that isn't serverless. This flexibility allows you to manage scaling, run on virtual networks, and even completely isolate the functions.

___

## Next unit: Describe application hosting options

[Continue](https://learn.microsoft.com/en-us/training/modules/describe-azure-compute-networking-services/7-describe-application-hosting-options/)

Having an issue? We can help!

-   For issues related to this module, explore existing questions using the [#azure training](https://aka.ms/azure-fundamentals-qna) tag or [Ask a question](https://aka.ms/qnaaztraining) on Microsoft Q&A .
-   For issues related to Certifications and Exams, post on [Credentials Support Forum](https://aka.ms/pilot-certifications-forums) or visit our [Credentials Help](https://aka.ms/pilot-cert-help).
