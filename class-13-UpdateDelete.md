# UPDATE/DELETE
ref:
- https://developer.mozilla.org/en-US/docs/Learn/Forms/Sending_and_retrieving_form_data
- https://htmlreference.io/forms/
- https://www.youtube.com/playlist?list=PL4cUxeGkcC9g5_p_BVUGWykHfqx6bb7qK

## General
- The web uses client/server architecture
- client (web browser) sends request to a server using the HTTP protocol
  - the server answers the request using the same protocol
  - HTML convenient-user-friendly way to configure on HTTP request to send data to a server

## FORM
- the form element defines how the data will be sent
- when button/submit is pressed, passes information through
- `action=""` is very important
- `method=""` is very important

### action=""
- action attribute defines where the data gets sent
- `<input action="" method="" name="" value="">`
- the action VALUE should be a file on the server that can handle incoming data. This should also include server-side validation
- server should respond with a new page (html or EJS file)
  - the data that is sent to the server should be used toward the content that is generated on the new page

### method=""
- defines how data is sent
  - GET
  - POST
  
#### GET
- method is used by. browser to ask the server to send back data given resources
- using GET appends data to the end of the url 
- `request.query`
- using a form
  - attributes:
  - name = name of property/key
  - values = value of property/key
- data is appended to URL as a pair of key:value pairs
- after URL is ended ? and & are followed
  - `https://somewebsite.com/?&id=12901931&name=jenner`
  
#### POST
- takes into account data provided in the BODY
  - `request.body`
- if a form is ent using this method, the data is appended to the body
- sending with the method value of POST, the information does not get appended to the URL
- instead of data being in the URL query, data will be found in the body
- POST is very useful:
  1. if you send important content such as a password or ID
  2. send large amounts of data
    - some browswers have a size limit on URL
- each time you send to a server, you need to consider security
- HTML forms are most common server attack vectors and using POST can add an extra layer of security
