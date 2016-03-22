# aws-lambda-api
### This Lambda function is used to get item values from Dynamodb table which is integrated with Amazon API Gateway. By invoking API url the lambda functions gets the item value.


1) Create a Lambda Function for item values from DynamoDB table. Use the below code.

https://github.com/adildhar/aws-lambda-api/blob/master/index.handler


2). Assign the IAM role for the function with following 
````
Action": [
        "dynamodb:DeleteItem",
        "dynamodb:GetItem",
        "dynamodb:PutItem",
        "dynamodb:Query",
        "dynamodb:Scan",
        "dynamodb:UpdateItem"
      ],
  "Action": [
        "logs:CreateLogGroup",
        "logs:CreateLogStream",
        "logs:PutLogEvents"
      ]
````
3). Create api using Amazon API gateway.
`````
Method: Post
Integration Type: Lambda Function
Lambda Region: <yourregion>
Lambda Function: <yourlambdafunctionname>
``````
4).  Deploy API
`````
Deployment Stage: New stage
stage Name: prod
````
You get the invoke URL after deploy API.

5). Using Postman plugin in Chrome, you can test the functionality





