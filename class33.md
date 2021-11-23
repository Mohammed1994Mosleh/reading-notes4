# class 33 Reading Notes:Serverless and AmplifyEspresso Test and API (GRAPHQL)

## what is serverless architecture?
![](https://cdn2.hubspot.net/hubfs/5129222/Imported_Blog_Media/serverless-architecture-590x474-1.png)


- Serverless is a cloud computing execution model where the cloud provider dynamically manages the allocation and  provisioning of servers.

- A serverless application runs in stateless compute containers that are event-triggered, ephemeral (may last for one invocation), and fully managed by the cloud provider.

- Pricing is based on the number of executions rather than pre-purchased compute capacity, isn’t it the ideal framework for that project you have been planning since a long time? Well, go ahead do it.

- Traditional vs. Serverless Architecture:
   - Traditional: applications have run on servers which you had to patch, update, and continuously look after      your application late  nights and early mornings due to all the unimaginable errors that broke your production.

- Serveless users are no longer need to worry about the underlying servers.beacuse they are not managed by users  anymore and with management out of the picture the responsibility falls on the Cloud vendors.


- [Pricing]

    One of the major advantages of using Serverless is reduced cost. The cost model of Serverless is execution-based: you’re charged for the number of executions.

- [Networking]

   The downside is that Serverless functions are accessed only as private APIs. To access these you must set up an API Gateway.

- [3rd Party Dependencies]

   Most, if not all of your projects have external dependencies, they rely on libraries that are not built into the language or framework you use.

- [Environments]

   Given that it’s pay per execution, this is a large improvement over traditional servers, you no longer need to set up dev, staging, and production machines.

- [Timeout]

   With Serverless computing, there’s a hard 300-second timeout limit. Too complex or long-running functions aren’t good for Serverless, but having a hard timeout makes it impossible to perform certain tasks.

- [Scale]

   Scaling process for Serverless is automatic and seamless, but there is a lack of control or entire absence of control.


## AWS: 
![AWS Amplify](https://res.cloudinary.com/practicaldev/image/fetch/s--zQ-O5dca--/c_imagga_scale,f_auto,fl_progressive,h_900,q_auto,w_1600/https://dev-to-uploads.s3.amazonaws.com/i/tldx6slnss1r9o241718.png)

- AWS Amplify is a set of tools and services that can be used together or on their own, to help front-end web and   mobile developers build scalable full stack applications, powered by AWS.

- [Benefits]

  1. Configure backends fast.
  2. Seamlessly connect frontends.
  3. Deploy in a few clicks.
  4. Easily manage content.

## The GraphQL

![GraphQL](https://cdn.netlify.com/f77989acee58aa60fe4f29f0cf0e751e3996d9c0/0f5ec/img/blog/graphql2.png)

   - The GraphQL Transform provides a simple to use abstraction that helps you quickly create backends for your web and mobile applications on AWS. 


### Create a GraphQL API

  1. Navigate into the root of a JavaScript, iOS, or Android project and run amplify init.

  2. Test the API

     Once the API is finished deploying, go to the AWS AppSync console or run amplify mock api to try some of these queries in your new API's query page.

  3. Update schema

If you want to update your API, open your project's backend/api/apiname/schema.graphql file and apply this
 
                                "amplify api gql-compile"


  4. API Category Project Structure
    At a high level, the transform libraries take a schema defined in the GraphQL Schema Definition Language (SDL) and converts it into a set of AWS CloudFormation templates and other assets that are deployed as part of amplify push. 

### API (GRAPHQL) Directives: 

![](https://devopedia.org/images/article/147/8496.1558526064.jpg)

  - The Amplify CLI provides GraphQL directives to enhance your schema with additional capabilities such as custom indexes, authorization rules, function triggers, and more.

#### Amplify-provided directives:

1. @model: Defines top level object types in your API that are backed by Amazon DynamoDB
2. @key: Configures custom index structures for @model types
3. @auth: Defines authorization rules for your @model types and fields
4. @connection: Defines 1:1, 1:M, and N:M relationships between @model types
5. @function: Configures a Lambda function resolvers for a field
6. @http: Configures an HTTP resolver for a field
7. @predictions: Queries an orchestration of AI/ML services such as Amazon Rekognition, Amazon Translate, and/or    Amazon Polly
9. @searchable: Makes your data searchable by streaming it to Amazon OpenSearch
10. @versioned: Defines the versioning and conflict resolution strategy for an @model type.


#### AWS AppSync-provided directives:

1. @aws_api_key
2. @aws_iam
3. @aws_oidc
4. @aws_cognito_user_pools
5. @aws_auth
6. @aws_subscribe

#### 3rd party directives:

1. @algolia: Add serverless search to your Amplify API with Algolia.
2. @ttl: Enable DynamoDB's time-to-live feature to auto-delete old entries in your AWS Amplify API
3. @firehose: Add a simple interceptor to all of your Amplify API mutations and queries
4. @retain: Enable the "Retain" deletion policy for your Amplify-generated DynamoDB tables