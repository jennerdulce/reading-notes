## Heroku
- Heroku is a webapp to allow users to upload their projects on github and create a live server through heroku that enables people to use the app via internet!
- However, the file that is being deployed has to have a JS server built into the file.
- Here are some steps to uploading the document:
1. create the document
2. use correct modules and build a simple server
3. upload docs to the existing repo on github
4. log into heroku and search for repo with your linked github account.
5. deploy

## Node
- Node is an event-based non-block asynchronous I/O runtime that uses googles V8 JS engine and libuv library
- Node is suited to build application that require some form of real time interaction/collaboration
- Speaks JSON which allows data to flow neatly between layers without needing to be reformatted
- Events trigger callback when an event is detected which happens asynchronously
- Traditional older models would have to wait for tasks to finish one at a time before moving on to the next (synchronous).
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
