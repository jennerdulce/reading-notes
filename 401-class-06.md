# Authentication

## Review, Research, and Discussion

1. Explain what a “Singleton” is (in Computer Science terms)

- Simple design pattern that restricts single instantiation of a class to the object

2. Explain how the Singleton pattern can be used with Node modules, specifically with classes

- After we instantiate once, every time we call to instantiate again, it will not create another instance.. instead it will refer to only one instantiation (the first one).

3. If you were tasked with building a middleware system like Express uses, what approach might you take to construct/operate it?

- Singleton seems correct to implement using a schema. in this case when we instantiate a new Object from the model schema, it would actually just create a new entry for the collection

## Terminology
- Router Middleware:
  - router level middleware the executes when a request is sent to the specific routes that have a middleware
  - modifies the request

- Dynamic Module Loading:
  - function-like form of import that returns a promise of the requested module

- Singleton Pattern:
  - A design pattern that restricts instantion of a class to a single object

- CRUD / REST MATCHES:
  - Create -> Post
  - Read -> Get
  - Update -> Put/Patch
  - Delete -> Delete

- Mock Testing:
  - form of unit testing by utilizing assertions and test data on modules
  - API mocks are used to simulate external dependencies that otherwise retrieve data
  - mock objects are simulated to create real ones

## Preview

1. Which 3 things had you heard about previously and now have better clarity on?

- Mock Testing, Singleton Pattern, CRUD

2. Which 3 things are you hoping to learn more about in the upcoming lecture/demo?

- Username Passwords and authentication, how user specific data is retrieved and rendered, creating a CRUD app utilizing username and password

3. What are you most excited about trying to implement or see how it works?

- Username Passwords and Authentication

## References:
- https://medium.com/@bretcameron/singletons-in-javascript-59655927b7d7
- https://devopedia.org/mock-testing
- https://v8.dev/features/dynamic-import
