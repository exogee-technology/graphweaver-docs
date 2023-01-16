# Backend

The primary backend entry point for a GraphWeaver project is an AWS Lambda function handler. This handler is built together with your code, then can be deployed to AWS using any mechanism you prefer.

You can run the backend locally with the GraphWeaver CLI, or with a tool such as AWS SAM or Serverless Offline.

Your code needs to contribute:

* An adapter for each backend that you want to connect to that the Base Resolver inside of GraphWeaver can use to interface with your data.
* Knowledge about Authentication / Authorisation and roles, which GraphWeaver will use to secure the service.
* A definition of the Schema of the entities used in your solution.
* Any custom queries / mutations that you want added to GraphWeaver's default operations generated for each entity.
* Any additional non-GraphWeaver services which make up your application.
