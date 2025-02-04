---
sidebar_position: 1
title: "🛌 Integrate with Amazon Bedrock"
---

:::warning
This tutorial is a community contribution and is not supported by the Open WebUI team. It serves only as a demonstration on how to customize Open WebUI for your specific use case. Want to contribute? Check out the contributing tutorial.
:::

---

# Integrating Open-WebUI with Amazon Bedrock

In this tutorial, we'll explore one of the most common and popular approaches to integrate Open-WebUI with Amazon Bedrock.

## Prerequisites


In order to follow this tutorial, you must have the following:

- An active AWS account
- An active AWS Access Key and Secret Key
- IAM permissions in AWS to enable Bedrock models
- Docker installed on your system


## What is Amazon Bedrock

Direct from AWS' website:

"Amazon Bedrock is a fully managed service that offers a choice of high-performing foundation models (FMs) from leading AI companies like AI21 Labs, Anthropic, Cohere, Luma, Meta, Mistral AI, poolside (coming soon), Stability AI, and Amazon through a single API, along with a broad set of capabilities you need to build generative AI applications with security, privacy, and responsible AI. Using Amazon Bedrock, you can easily experiment with and evaluate top FMs for your use case, privately customize them with your data using techniques such as fine-tuning and Retrieval Augmented Generation (RAG), and build agents that execute tasks using your enterprise systems and data sources. Since Amazon Bedrock is serverless, you don't have to manage any infrastructure, and you can securely integrate and deploy generative AI capabilities into your applications using the AWS services you are already familiar with."

To learn more about Bedrock visit: [Amazon Bedrock's Official Page](https://aws.amazon.com/bedrock/)

# Integration Steps

## Step 1: Verify access to Amazon Bedrock Base Models

Before we can integrate with Bedrock, you first have to verify that you have access to at least 1, but preferably many, of the Base Models. You can see in the screenshot below that I have access to mulitple models. You'll know if you have access to a model if it says "✅ Access Granted" next to the model. If you don't have access to any models, you will get an error on the next step.


AWS provides good documentation for request accessing / enabling these models here: [Amazon Bedrock's Model Access](https://docs.aws.amazon.com/bedrock/latest/userguide/model-access-modify.html)

![Amazon Bedrock Base Models](/images/tutorials/amazon-bedrock/amazon-bedrock-base-models.png)


## Step 2: Configure the Bedrock Access Gateway

Now that we have access to at least one Bedrock base model, we need to configure the Bedrock Access Gateway.

- Describe why we need the BAG
- Link to BAG repo
- Include docker commands
- Include error message you might see if you don't have any bedrock models enabled
- Include info about changing the defeault password
- Explain why these 4 endpoints and how they match OpenAI schema (link to schema)

https://github.com/aws-samples/bedrock-access-gateway

![Bedrock Access Gateway API](/images/tutorials/amazon-bedrock/amazon-bedrock-proxy-api.png)

## Step 3: Add Connection in Open-WebUI

- add basic instricutions for adding a new connection
- add URL and PW


![Add New Connection](/images/tutorials/amazon-bedrock/amazon-bedrock-proxy-connection.png)


## Step 4: Start using Bedrock Base Models

- add simple text for seeing the models

![Use Bedrock Models](/images/tutorials/amazon-bedrock/amazon-bedrock-models-in-oiu.png)



## Other Helpful Tutorials

While I'd take all the credit for this tutorial, I relied on several other contributors tutorials and examples. Credit to:

- https://gauravve.medium.com/connecting-open-webui-to-aws-bedrock-a1f0082c8cb2
- https://jrpospos.blog/posts/2024/08/using-amazon-bedrock-with-openwebui-when-working-with-sensitive-data/
