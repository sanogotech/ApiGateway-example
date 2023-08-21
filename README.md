# ApiGateway-example
Example of API Gateway based on .NET Core, Ocelot, Consul

- https://www.linkedin.com/pulse/api-gateway-usingnet-core-ocelot-andconsul-paulius-juozelskis/

##  Monolithic vs Microservices

![ Monolithic vs Microservices  ](https://github.com/sanogotech/ApiGateway-example/blob/master/images/monolithicvsmicroservice.jpg)

## Architecture  Sample

![  Api Gateway](https://github.com/sanogotech/ApiGateway-example/blob/master/images/apigatewaysample.jpg)



## API Gateway between a client and our services/functions

By placing API Gateway between a client and our services/functions we can have a centralized component that will be responsible for API management, logging, authentication/authorization, rate limiting and load balancing and distributed tracing. However, we will introduce a component that can become a single point of failure to our system, so we need to deploy at least two replicas of it to have high availability and scale up depending on load.

##  API  Gateway vs Loadbalancing

![ API Gateway vs Loadbalancing](https://github.com/sanogotech/ApiGateway-example/blob/master/images/apigatewayvsloadbalancer.jpg)
