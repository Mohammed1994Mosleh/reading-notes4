# class 32 Reading Notes:Serverless and AmplifyEspresso Test

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



