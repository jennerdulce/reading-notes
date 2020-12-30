## API NOTES (Application Program Interface)
### An API is like a messenger
- Contract from 1 piece of software to another piece of software
- structured request and response
- API is a messenger/waiter between running software
- formatted style JSON and other styles

### REST (Representational State Transfer)
- Architecture style for desigining networked application
- Reliies on stateless, client-server protocol
- *HTTP*: foundation of web communication 
  - Is the first thing you type into a browser to access a specific site or location (protocol)
    - Protocols describe the location from something from anywhere around the world Like GPS coordinates
  - HTTP is a server somewhere
  - treats server objects as resources that can be created/destroyed (posted and deleted)
- Can be virturally used by any programming langugage
- *REST* lets us use HTTP requests to format API messages
  - Whole web is designed based on REST
- *RESTFUL* means conforming to *REST* constraints
- webpages are representations of resources

### HTTP Methods
- *GET*: retrieve data from specified resource  
- *POST*: submit data. typically on webforms
- *PUT*: updates specified resource
- *DELETE*: delete specified resource

### Endpoints
- URI/URL where api/service can be accessed by a client application
- HTTP requests are sent to

#### Examples
`GET mysite.com/api/users`
- api folder
- endpoint for GET reuest
- will return a list of users

`GET mysite.com/api/users/details/1`
- will retrieve a specific user

`POST mysite.com/api/users`
- will ADD a user to server/database
- have to send data with this request

`PUT mysite.com/api/users/update/1`
- will UPDATE specific user
- have to send data along with this request

`DELETE mysite.com/api/users/details/1`
- deletes the user specified
- will ADD a user to server/database
