🌩️ Fun-Facts — Cloud Fun Facts Generator

A cloud-based, serverless, AI-powered application that generates witty cloud fun facts using AWS Lambda, API Gateway, DynamoDB, Bedrock, and Amplify.

🚀 Features

✔ Fully serverless architecture

✔ AI-powered fact generation using Amazon Bedrock (Claude)

✔ Uses AWS best practices (IAM Roles, least privilege)

✔ Auto-deployed frontend using AWS Amplify

✔ Fast, scalable, and extremely cost-efficient

👩‍💻 Steps To Be Performed
1️⃣ Backend Deployment (Lambda + API Gateway)

Create a Lambda function (Node.js/Python)

Write code to return a random cloud fact

Expose the Lambda using Amazon API Gateway

Test the API using Postman or browser

2️⃣ Add DynamoDB Integration

Create a DynamoDB table → CloudFunFacts

Insert 10–20 cloud facts

Update Lambda to:

Query a random item

Return JSON response to frontend

3️⃣ Add Amazon Bedrock (GenAI Enhancement)

Use Claude 3 Sonnet / Haiku

Rewrite each cloud fact in a fun, witty tone

Update Lambda to integrate Bedrock + DynamoDB

Return enhanced version to API Gateway

4️⃣ Frontend Deployment with AWS Amplify

Build a simple HTML/JS or React frontend

Add button → calls API endpoint

Display the generated fun fact

Push project to GitHub

Connect repo to AWS Amplify Hosting

Deploy with one click

🛠️ Services Used

Service	                 Purpose
AWS Lambda	             Backend logic
Amazon API Gateway	     REST API
Amazon DynamoDB	         Fact storage
Amazon Bedrock           AI enhancement
(Claude)
AWS Amplify            	 Frontend hosting
AWS IAM	                 Secure permissions

⚙️ Estimated Time & Cost
Item	           Value
Total Time     	 90–120 minutes
Total Cost	    ~ $0.03 (almost free on AWS Free Tier)

🏗️ Cloud Fun Facts Generator – Text-Based Architecture Diagram

                         ┌────────────────────────┐
                         │        USER            │
                         │  Clicks "Fun Fact"     │
                         └────────────┬───────────┘
                                      │
                                      ▼
                         ┌────────────────────────┐
                         │      AWS AMPLIFY       │
                         │  (Frontend Hosting)    │
                         └────────────┬───────────┘
                                      │ 1. Calls API
                                      ▼
                         ┌────────────────────────┐
                         │    API GATEWAY         │
                         │ Exposes REST Endpoint  │
                         └────────────┬───────────┘
                                      │ 2. Triggers Lambda
                                      ▼
                         ┌────────────────────────┐
                         │        LAMBDA          │
                         │ Backend Logic          │
                         │ - Fetch random fact    │
                         │ - Enhance using AI     │
                         └───────┬────────┬──────┘
                                 │        │
       3. Query random fact      │        │ 4. Send fact for AI enhancement
                                 │        ▼
                                 ▼   ┌────────────────────────┐
                         ┌────────────────────────┐           │
                         │       DYNAMODB         │           │
                         │ Stores cloud facts     │           │
                         └────────────────────────┘           │
                                                             ▼
                                             ┌────────────────────────┐
                                             │       BEDROCK          │
                                             │ Claude AI Enhances Fact│
                                             └────────────┬───────────┘
                                                          │ 5. Return witty fact
                                                          ▼
                         ┌────────────────────────┐
                         │  AWS AMPLIFY FRONTEND  │
                         │ Displays final fact     │
                         └────────────────────────┘

🤝 Contribution

Pull requests are welcome!
If you want to add more cloud facts or UI improvements, feel free to contribute.

⭐ Support

If you like this project, please ⭐ star the repository!
