# Controllers:
- Controllers are charged with receiving requests from clients and giving responses depending on what was programmed. They are used for routing, defining endpoints with resources, defining routes with parameters, redirecting, defining status code for different endpoints, and so on. To use the controller in typescript, you need to use the nest controller decorator @Controller() followed by its associated class, you can also add an optional route path to a controller, for example@Controller(‘users’). A controller can have as many endpoints or resources as possible. For instance, we can use the Get decorator attached to a method to fetch all customers in a database, and a post decorator with the endpoint create to create a new user.

# Providers:
- Providers are a fundamental concept in Nest. Many of the basic Nest classes may be treated as a provider – services, repositories, factories, helpers, and so on. The main idea of a provider is that it can be injected as a dependency; this means objects can create various relationships with each other, and the function of "wiring up" instances of objects can largely be delegated to the Nest runtime system.

# DTOs:
 ## What is DTO?
 - DTO is the short name of Data Transfer Object. DTO is used in order to validate incoming requests. 
The DTO on its own is more of a guideline for the developer and those who consume the API to know what kind of shape the request body expects to be, it doesn’t actually run any validations on its own!!!.
