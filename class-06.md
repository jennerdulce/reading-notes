## Node
- Node is an event-based non-block asynchronous I/O runtime that uses googles V8 JS engine and libuv library
- Node is suited to build application that require some form of real time interaction/collaboration
  - streaming sites
  - chat apps
  - blogs
- Speaks JSON which allows data to flow neatly between layers without needing to be reformatted
- Events trigger callback when an event is detected which happens asynchronously
- Node is able to support tens of thousands of connection which are held in an event loop
- Traditional older models would have to wait for tasks to finish one at a time before moving on to the next (synchronous).
  - have multithreads which continue to create threads until it has reached memory capacity which then has a chance of crashing the program
`node` actives runtime in terminal where you can type JS like how you do in the console in a browser
- `node filename` allows you to run a document in the runtime environment    
- If you `node filename` with a server, it will create a server and it will continue to be open until you close it by pressing 'command C'
```
const http = require('http')

  http.createServer((request, response) => {
  response.writeHead(200);
  response.end('Hello World')
});.listen(3000)

console.log('listening on http://localhost:3000')
```
### in the example above:
- start by requiring nodes native 'HTTP' module `require('http')`
- use the `createServer()` method to create a new web server object.
  - in this, we pass an anonymous function
  - this function will be invoked everytime a new connection to the server has been made
- the anonymous function is called with TWO arguments
  1. request
  2. response
  - these contain the request from the user AND the response
  - we use to send back a '200 HTTP status code' along with a 'hello world' message
- finally we tell the server to listen for incoming requests on port 3000

## Express
- express is one of node's most popular packages.
- express is a web development framework
- is a server side backend framework
- often used in conjunction with clientside framework (REACT)
- makes building apps with node easier
- full control of request and response


## API (application programmable interface)
- helps multiple programs work together
1. Access to data
  - i.e. weather app; apple uses 3rd party api from the weather channel to exchange data and display the weather.
  - APPLE the company itself does not have their own set of weather data.
  - APIs allow different apps and services to exchange information
  
2. Hide complexity/perform tasks
  - Operating system gives developers a bunch of APIs to simplify complexities of how apps work
  - allows users to just use rather than build the whole thing on their own
  
3. extend functionality
  - siri, alexa, google home
  - phone asking permission: for gps, access photos
  
4. Security
  - gives users permission to allow/deny program access to personal data: photos, location, contact information
  
