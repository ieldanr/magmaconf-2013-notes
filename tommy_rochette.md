Angular JS: Advanced Design Patterns and Best Practices
by Tommy Rochette

github.com/trochette

1. Keep your code organized
  As it grows, it gets harder to find what you are looking for.
  Analogy with clothes. It will take a while to find the black tshirt from a pile.
  

2. Keep controllers simple
  Controllers are meant to define your scope variables and encapsulate view related logic. 
  Please don't use controllers for DOM interactions or data manipulation.

Opiniated: Angular is missing two critical things. Structured class approach and class inheritance.

3. Business logic belongs to models.
  Data processing should always be kept in models, that way they can easily be shared between controllers and other services. 
  Plus it's easier to write unit test for them.

4. Create facade to interact with servers
  Keep it single, separate server interaction and error handling from the model.
  That way model only handle data processing and code is easier to maintain.

5. Leverage provider configuration
  Angular gives developers the ability to configure providers before they are injected inside other objects in our application. 
  Use that to your advantage and handle global events like service errors from that level.

6. Share a notification service
  While it's a good solution to bridge gaps between directives, controllers and models we encourage you to use $scope.$emit() and $scope.$broadcast when possible.
  Don't overuse it.

7. Automate your workflow
  AngularJS ecosystem is growing fast. Each month new tools are released.
  Use them to build your own boilerplate and use that for your projects

