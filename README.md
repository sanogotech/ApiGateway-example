# ApiGateway-example
Example of API Gateway based on .NET Core, Ocelot, Consul

- https://www.linkedin.com/pulse/api-gateway-usingnet-core-ocelot-andconsul-paulius-juozelskis/


## API  Gateway  Process

![API  Gateway  Process](https://github.com/sanogotech/ApiGateway-example/blob/master/images/ApiGatewayProcess.jpg)


Step 1 - The client sends an HTTP request to the API gateway.


Step 2 - The API gateway parses and validates the attributes in the HTTP request.


Step 3 - The API gateway performs allow-list/deny-list checks.


Step 4 - The API gateway talks to an identity provider for authentication and authorization.


Step 5 - The rate limiting rules are applied to the request. If it is over the limit, the request is rejected.


Steps 6 and 7 - Now that the request has passed basic checks, the API gateway finds the relevant service to route to by path matching.


Step 8 - The API gateway transforms the request into the appropriate protocol and sends it to backend microservices.


Steps 9-12: The API gateway can handle errors properly, and deals with faults if the error takes a longer time to recover (circuit break). It can also leverage ELK (Elastic-Logstash-Kibana) stack for logging and monitoring. We sometimes cache data in the API gateway.



##  Monolithic vs Microservices

![ Monolithic vs Microservices  ](https://github.com/sanogotech/ApiGateway-example/blob/master/images/monolithicvsmicroservice.jpg)


##  Granularité des Microservices

![ Domaine microservice ](https://github.com/sanogotech/ApiGateway-example/blob/master/images/MicroServiceArchiDomaineDB.jpg)

## Architecture  Sample

![  Api Gateway](https://github.com/sanogotech/ApiGateway-example/blob/master/images/apigatewaysample.jpg)



## API Gateway between a client and our services/functions

By placing API Gateway between a client and our services/functions we can have a centralized component that will be responsible for API management, logging, authentication/authorization, rate limiting and load balancing and distributed tracing. However, we will introduce a component that can become a single point of failure to our system, so we need to deploy at least two replicas of it to have high availability and scale up depending on load.

##  API  Gateway vs Loadbalancing

![ API Gateway vs Loadbalancing](https://github.com/sanogotech/ApiGateway-example/blob/master/images/apigatewayvsloadbalancer.jpg)
