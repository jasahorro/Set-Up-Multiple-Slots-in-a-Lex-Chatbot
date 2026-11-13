<picture><source media="(prefers-color-scheme: dark)" srcset="https://nextwork.ai/static/nextwork-logo-paper.svg" /><img src="https://nextwork.ai/static/nextwork-logo-leather.svg" alt="NextWork" width="300" /></picture>

# Set Up Multiple Slots in a Lex Chatbot

**Project Link:** [View Project](https://nextwork.ai/projects/13cfd692-9802-5c98-ada7-92fde8b30a99)

**Author:** Maria Jasmin Ahorro

---

## Introducing Today's Project!

### ✍️ What are we here to do today?

In this project, I will demonstrate how to configure multiple slots with a shared slot type, implement confirmation prompts, use conversation flow and visual builder tools, and automate AWS resource deployments with CloudFormation. I'm doing this project to learn how to build more advanced, multi-turn conversational agents with Amazon Lex and streamline infrastructure setup using infrastructure-as-code principles!

### ✍️ What are we doing in this step?

In this step, I will review the FollowupCheckBalance intent configuration in the Amazon Lex console because we need to verify its input and output contexts (contextCheckBalance), sample utterances, and slots (accountType and dateOfBirth) to ensure seamless conversational state carryover.

### ✍️ What are we doing in this step?

In this step, I will review the FollowupCheckBalance intent configuration in the Amazon Lex console because we need to verify its input and output contexts (contextCheckBalance), sample utterances, and slots (accountType and dateOfBirth) to ensure seamless conversational state carryover.

### What is Amazon Lex?

Amazon Lex is a fully managed artificial intelligence service with advanced natural language models designed for building conversational interfaces into any application and it is useful because it enables developers to quickly build, test, and deploy highly engaging chatbots and virtual assistants with natural, multi-turn conversational capabilities across multiple messaging platforms without needing to manage complex underlying infrastructure.

### How I used Amazon Lex in this project

In today's project, I used Amazon Lex to build an advanced TransferFunds intent with multiple slots sharing the same custom accountType slot type, configure interactive confirmation prompts and closing responses, explore built-in conversation flow and visual builder tools, and automate the deployment of my entire BankerBot stack using AWS CloudFormation!

### One thing I didn't expect in this project was...

One thing I didn't expect in this project was how smooth and fast it is to automate an entire cloud infrastructure stack—including Amazon Lex bots, custom intents, and AWS Lambda functions—using an AWS CloudFormation template, rather than manually setting everything up step-by-step through the console!

### This project took me...

This project took me 1 hour to complete, allowing me to successfully build an advanced multi-turn chatbot with multiple slots, configure confirmation prompts, explore visual conversation flows, and automate the entire infrastructure deployment using AWS CloudFormation!

### ❤️ Thanks for doing this project!

I chose to do this project today because I wanted to master building advanced multi-turn conversational agents with multiple slots sharing the same custom slot type, learn how confirmation prompts enhance transaction safety, and explore how to automate entire cloud infrastructure deployments using Infrastructure as Code (IaC) with AWS CloudFormation! Something that would make learning with NextWork even better is having even more hands-on cloud automation projects and real-world DevOps scenarios to practice building scalable, production-ready architectures from scratch!

## TransferFunds

An intent I created for my chatbot was TransferFunds, which handles moving money between different bank accounts using multiple slots (sourceAccountType, targetAccountType, and transferAmount), confirmation prompts, and closing responses to streamline financial transactions in BankerBot.

![TransferFunds](https://nextwork.ai/overjoyed_magenta_proud_yak/uploads/13cfd692-9802-5c98-ada7-92fde8b30a99_67890123)

## Using multiple slots

For this intent, I had to use the same slot type twice. This is because the TransferFunds intent requires two distinct account references (sourceAccountType and targetAccountType) to successfully process money movement between accounts, and utilizing our custom accountType slot type for both slots allows us to correctly capture and validate both the origin and destination account types.

### ✍️ What are we doing in this step?

In this step, I will explore Amazon Lex's built-in conversation flow and visual builder features in the AWS console because I want to analyze the chronological sequence of my TransferFunds intent, visualize how slot prompts interact, and learn how visual flowcharts can streamline building and editing complex conversational agents.

I also learnt how to create confirmation prompts, which are built-in safety mechanisms in Amazon Lex that repeat transaction details (such as transferring money) back to the user for explicit verification before executing the intent fulfillment, allowing users to either confirm or cancel the action.

![Using multiple slots](https://nextwork.ai/overjoyed_magenta_proud_yak/uploads/13cfd692-9802-5c98-ada7-92fde8b30a99_97dc2351)

## Exploring Lex features

Lex also has a special conversation flow feature that displays every step of an intent's conversation in a logical, chronological order, complete with clickable "ghost-like" response recommendations that let you easily add new conversational paths or jump straight to editing specific prompt messages!

You could also set up your intent using a visual builder! A visual builder transforms the standard text-based setup page into an interactive flowchart, allowing you to easily visualize, design, and manage your bot's conversational paths and slot prompts visually!

### ✍️ What are we doing in this step?

In this step, I will use AWS CloudFormation to deploy the BankerBot stack from the provided nextwork-banker-bot.yaml template because automating our infrastructure setup with Infrastructure as Code (IaC) saves time and ensures all Lex bots, intents, and Lambda resources are consistently and correctly configured in seconds!

![Exploring Lex features](https://nextwork.ai/overjoyed_magenta_proud_yak/uploads/13cfd692-9802-5c98-ada7-92fde8b30a99_12345678)

## AWS CloudFormation

AWS CloudFormation is a service that gives you an easy way to create and manage a collection of related AWS resources, provisioning and updating them in an orderly and predictable fashion through infrastructure as code templates.

I used CloudFormation to automatically deploy the complete BankerBot stack using the nextwork-banker-bot.yaml template, creating all necessary Amazon Lex bots, intents, and Lambda resources in seconds and streamlining infrastructure setup with Infrastructure as Code (IaC)!

![AWS CloudFormation](https://nextwork.ai/overjoyed_magenta_proud_yak/uploads/13cfd692-9802-5c98-ada7-92fde8b30a99_c4fc89af)

## The final result!

Re-building my bot with CloudFormation took me 5 minutes, allowing me to fully automate the deployment of my BankerBot stack using the nextwork-banker-bot.yaml template!

There was an error after I deployed my bot! The error was an access denied error when testing the CheckBalance intent because the CloudFormation-deployed Lambda function lacked the proper resource-based permissions required for Amazon Lex to invoke it. I fixed this by creating a new Lambda function (BankingBotEnglish) with the correct Python code and adding a resource-based policy statement (my-custom-permission-amazonlexchatbot) granting lexv2.amazonaws.com permission to invoke the function via the bot alias ARN!

![The final result!](https://nextwork.ai/overjoyed_magenta_proud_yak/uploads/13cfd692-9802-5c98-ada7-92fde8b30a99_505be5b8)
