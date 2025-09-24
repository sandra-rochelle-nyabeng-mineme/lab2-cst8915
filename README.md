# Lab 2 - CST8915 Full-stack Cloud-native Development
### Name : Sandra Rochelle Nyabeng Mineme
### Student ID :041268641

Youtube video link :https://youtu.be/qiXvqiU-6b8
Order service repository:https://github.com/sandra-rochelle-nyabeng-mineme/order-service-lab2
Product service repository:https://github.com/sandra-rochelle-nyabeng-mineme/product-service-lab2
Store Front service repository:https://github.com/sandra-rochelle-nyabeng-mineme/storefront-lab2
RabbitMQ repository:https://github.com/sandra-rochelle-nyabeng-mineme/RabbitMQ

## Reflection Questions/Answers

### What changes did you make to the order-service and product-service to comply with the Configurations and Backing Services factors of the 12-Factor App methodology?
I removed any hardcoded values like URLs and i used environment variables. I create an .env files and add ports, the RabbitMQ connection string. It ensured the services can connect to RabbitMQ or a database via URLs defined in environment variables. I ensured all dependencies are declared in a dependency management file and installed dependencies. Treated dependencies like RabbitMQ as attached resources, not tighly coupled.


### Why is it important to use environment variables instead of hard-coding configurations in your application?
The same codebase can run in differents environments. the password or any secrets are not exposed in source code or git repositories. Changes are easy to make without redeploying code.

### Why is it important to have separate repositories for each microservice? How does this help maintain independence and scalability of each service?
- Independence: Each microservice can be developed, deployed and scaled independtly of the other.
- Autonomy: Teams can work on different services without stepping on each other's code.
- Scalalbility:  you can scale only the services that need more resources
- Versioning: Each service has its own release cycle, bug fixes, and upgrade path.