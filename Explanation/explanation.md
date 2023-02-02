# Controllers:
- Controllers are charged with receiving requests from clients and giving responses depending on what was programmed. They are used for routing, defining endpoints with resources, defining routes with parameters, redirecting, defining status code for different endpoints, and so on. To use the controller in typescript, you need to use the nest controller decorator @Controller() followed by its associated class, you can also add an optional route path to a controller, for example@Controller(‘users’). A controller can have as many endpoints or resources as possible. For instance, we can use the Get decorator attached to a method to fetch all customers in a database, and a post decorator with the endpoint create to create a new user.

# Providers:
- Providers are most of the time classes, that can be injected as a dependency to other classes such as the controller class. They are used as services for controller resources, it used to deal with database (business layer).
