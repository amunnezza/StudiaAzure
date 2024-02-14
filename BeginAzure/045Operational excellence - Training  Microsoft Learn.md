---
created: 2024-02-14T09:28:32 (UTC +01:00)
tags: []
source: https://learn.microsoft.com/en-us/training/modules/azure-well-architected-introduction/4-operational-excellence
author: martinekuan
---

# Operational excellence - Training | Microsoft Learn

> ## Excerpt
> Operational excellence

---
-   10 minutes

Moving just your resources to the cloud is taking advantage of only a small portion of what the cloud can bring to your organization. Along with the technical capabilities that the cloud delivers, you can improve your operational capabilities as well. From improving developer agility to improving your visibility into the health and performance of your application, you can use the cloud to improve the operational capabilities of your organization.

In this unit, we look at the pillar of operational excellence.

## What is operational excellence?

Operational excellence is about ensuring that you have full visibility into how your application is running, and ensuring the best experience for your users. Operational excellence includes making your development and release practices more agile, which allows your business to quickly adjust to changes. By improving operational capabilities, you can have faster development and release cycles, and a better experience for your application's users.

You can use several principles when driving operational excellence through your architecture.

### Design, build, and orchestrate with modern practices

Modern architectures should be designed with DevOps and continuous integration in mind. A modern architecture allows you to automate deployments by using infrastructure as code, automate application testing, and build new environments as needed. DevOps is as much cultural as it's technical, but can bring many benefits to organizations that embrace it.

Regardless of the type of project you're managing, you can bring DevOps practices into your organization. Whether your project is an application that uses full continuous integration and continuous deployment (CI/CD) and containers, or a legacy application that you're continuing to service.

Breaking down silos within an organization is a common thread throughout DevOps. So is working collaboratively across every stage in a project, including change management. By creating a culture of sharing, collaboration, and transparency, you can bring operational excellence to your organization.

### Use monitoring and analytics to gain operational insights

Throughout your architecture, you want to have a thorough monitoring, logging, and instrumentation system. By creating an effective system for monitoring what's going on in your architecture, you can ensure that you know when something isn't right before your users are affected. With a comprehensive approach to monitoring, you can identify performance issues and cost inefficiencies, correlate events, and gain a greater ability to troubleshoot issues.

Operationally, it's important to have a robust monitoring strategy. Monitoring helps you identify areas of waste, troubleshoot issues, and optimize the performance of your application. A multilayered approach is essential. Gathering data points from components at every layer will help alert you when values are outside acceptable ranges and help you track spending over time.

### Use automation to reduce effort and error

You should automate as much of your architecture as possible. The human element is costly, injecting time and error into operational activities. This increased time and error results in increased operational costs. You can use automation to build, deploy, and administer resources. By automating common activities, you can eliminate the delay in waiting for a human to intervene.

### Test

You should include testing in your application deployment and your ongoing operations. A good testing strategy helps you identify issues in your application before it's deployed, and ensure that dependent services can properly communicate with your application.

A good testing strategy can also help identify performance issues and potential security vulnerabilities in both preproduction and production deployments. A robust testing plan can uncover issues with infrastructure deployments that can affect the user experience, and testing can help you provide a great experience for your users.

## Check your knowledge

**1.** 

Which of the following is a good example of using testing in your environment?

 

Waiting for users to reach out to you with reports of errors in your application.

Performing functionality tests in the development environment that are different from functionality tests in the production environment.

Omitting infrastructure deployment from test plans.

**Performing regular security tests of your application code in development and production environments.**

_Regular security tests are a key element of security for your application and can help identify security defects and issues._


**2.**

Which of the following examples uses automation to improve operational excellence?

 

Manually provisioning development environments every day for your development teams.

Logging on Linux VMs after deployment and installing the software packages that are required for the application.

**Using a configuration template to deploy infrastructure in each environment.**

_By using a configuration template to deploy infrastructure, you can be sure to have consistent, repeatable environments._

Manually copying application binaries from your build system to your deployment infrastructure.