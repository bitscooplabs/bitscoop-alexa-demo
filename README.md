# BitScoop Alexa Demo

You can build with any API on the BitScoop platform which makes being a software developer more interesting than ever. In our “Built with BitScoop” series, we show very specific use cases for the BitScoop platform to give you ideas and foundations for new projects.

Today we demonstrate how to build an Alexa “skill” to make Alexa devices part of the DevOps team. We’ll call this Alexa demo app “Ops Buddy,” which enables Alexa to tell me in real-time how my stack is doing.

*Alexa, ask “Ops Buddy” “How is the stack doing?”*

**(From Google Analytics)**

*There were 523 visitors to the site today. 201 were new
visitors.*

**(From StatusCake)**

*There have been [no, X] outage alerts since yesterday.*

**(From Postman)**

*The API status check has [passed/failed].*

**(From GitHub)**

*There are [no, X] pending pull requests for API maps.*

*The top trending APIs on GitHub are currently…*

*Built with BitScoop*

It’s all built with BitScoop as the unified interface for the requisite APIs. Specifically, we use Google Analytics, StatusCake, Postman and GitHub; but you can easily add other services.

Any other service with an API can be brought into your project, like Pagerduty, Kubernetes, Chef, Docker, or AlertLogic. This demo project is open source and the related GitHub project is listed below. Feel free to use it as the foundation of your next great project.

[Alexa](https://en.wikipedia.org/wiki/Amazon_Alexa) is the world’s most popular personal assistant and chatbot platform. An Alexa “skill” is a capability you can add to make Alexa more personalized. Alexa skills are comprised of an “Invocation Name,” which you can think of as your app name; a set of “Intents”; the phrases that map to each intent; and the software that can detect the intent and return the appropriate results. (BTW you don’t actually need an Amazon Echo or Echo Dot to use or test Alexa. You can use https://echosim.io or even [build your own device like we did](https://www.facebook.com/bitscooplabs/photos/a.1799207820329206.1073741829.1616937155222941/1855601798023141/?type=3&theater).)

We set out to quickly get a verbal snapshot of our stack with a very short question to Alexa. Building this BitScoop powered Alexa skill is comprised of four steps.

## Tutorial

1. [Create accounts, add API maps to BitScoop, and set up authorization](https://github.com/bitscooplabs/bitscoop-alexa-demo/blob/master/tutorial/step-1.md)

2. [Download the “Ops Buddy” project from GitHub](https://github.com/bitscooplabs/bitscoop-alexa-demo/blob/master/tutorial/step-2.md)

3. [Deploy the code into Amazon Lambda](https://github.com/bitscooplabs/bitscoop-alexa-demo/blob/master/tutorial/step-3.md)

4. [Set up the skill in the Amazon Alexa Skills Developer Portal](https://github.com/bitscooplabs/bitscoop-alexa-demo/blob/master/tutorial/step-4.md)
