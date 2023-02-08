# Controllers:
- Controllers are charged with receiving requests from clients and giving responses depending on what was programmed. They are used for routing, defining endpoints with resources, defining routes with parameters, redirecting, defining status code for different endpoints, and so on. To use the controller in typescript, you need to use the nest controller decorator @Controller() followed by its associated class, you can also add an optional route path to a controller, for example@Controller(‘users’). A controller can have as many endpoints or resources as possible. For instance, we can use the Get decorator attached to a method to fetch all customers in a database, and a post decorator with the endpoint create to create a new user.

# Providers:
- Providers are a fundamental concept in Nest. Many of the basic Nest classes may be treated as a provider – services, repositories, factories, helpers, and so on. The main idea of a provider is that it can be injected as a dependency; this means objects can create various relationships with each other, and the function of "wiring up" instances of objects can largely be delegated to the Nest runtime system.
- Providers such as services, repository .

# Service:
- In enterprise applications, we follow the SOLID principle, where S stands for Single Responsibility.
- The controllers are responsible for accepting HTTP requests from the client and providing a response. For providing the response, you may need to connect to some external source for data.
- If we add the code to connect to the external source inside, we are not following the single responsibility principle.
- To avoid this issue, you use services, which will be responsible for providing some data, which can be reused across the application. It can also hold some validation logic or logic to validate users.
- it will added @injectable decoratore that mean every class has injectable decoratore that mean this class can be injected inside other classes like service can be injected inside controller.

# DTOs:
 ## What is DTO?
 - DTO is the short name of Data Transfer Object. DTO is used in order to validate incoming requests. 
The DTO on its own is more of a guideline for the developer and those who consume the API to know what kind of shape the request body expects to be, it doesn’t actually run any validations on its own!!!.
- and we should this decoratore before route in controller to allow us to use dto @UsePipes(ValidationPipe).
- this link for more decoratores of **DTOs:** https://github.com/hippo-oss/nest-dto

## Why we should use DTO?
- There are a few other important concepts in Nest. js: DTO: Data transfer object is an object that defines how data will be sent over the network. Interfaces: TypeScript interfaces are used for type-checking and defining the types of data that can be passed to a controller or a Nest service.

# Modules
- Both the controllers are provider classes are defined in the module. You can decide to create a different module for different functions, for example, the users’ module for all users’ functions. These sub-modules would be imported to the app module which is the main app module for our project. Other needed modules are also imported in the module.ts file, such as the typeorm module, configuration module, and so on.


