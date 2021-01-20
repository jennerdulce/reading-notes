# EJS
# references:
- https://www.youtube.com/playlist?list=PL7sCSgsRZ-slYARh3YJIqPGZqtGVqZRGt
- https://www.digitalocean.com/community/tutorials/how-to-use-ejs-to-template-your-node-application

## How to implement EJS:
1. `app.use(express.static('./public'))
2. `app.set('view engine', 'ejs);
  - searches for EJS files in the 'views' directory by default
3. create 'views' directory
  - touch views
4. YOU DO NOT HAVE TO BRING IN DEPENDENCY
5. install ejs

- when using POST:
  - using post makes URL queries private
  1. `app.use(express.urlencoded({ extended: true }))`
    - decodes encoded content (post content is encoded)
  2. `app.post()` instead of `app.get()` when creating routes
  3. in a form `method="POST"`

- when using GET:
  1. `app.get()`
  2. in a form `method="GET"`
  
## General Notes
- in EJS. what were doing is rendering webpages through the back end
- instead of responding with only an object.. the back end responds with EJS files that are similar to HTML files
  - EJS files contain HTML mark up.
  - along with this, you are able to pass in data though javascript using proper EJS syntax

- `.render()` actually takes 3 parameters:
  1. str of the filename
  2. object/local variables that you want to pass into the file
  3. callback function
  - ex. `res.render('ejsfilename', {data: someArrayW/Objects})`
  - ex. `res.render('ejsfile.ejs')
  
- you can loop through data:
  - given that data has been passed in the form of `res.render('ejsfilename', {data: someArray})`
  - inside the ejs file:
```
<% data.forEach(value => { %>
  <p><%= value%></p>
  <%}%>
```
- notice the name of the object
- the syntax is different when implementing ejs (on the first line) compared to when you want to EVALUATE a value (secondline)

## If/else
- an example of using an if else statement within a EJS file
```
<% data.forEach(value => { %>
  <% if(value === 1) { %>
  <p>display this line</p>
  <% } else { %>
  <p> display this other line </p>
  <% } %>
```

## Layouts
- ref: https://www.youtube.com/watch?v=3nl3LFgKZ2o&list=PL7sCSgsRZ-slYARh3YJIqPGZqtGVqZRGt&index=7&ab_channel=WalkThroughCode

- How to implement layouts
1. `npm install --save express-ejs-layouts`
2. `var expressLayouts = require('express-ejs-layouts')`
3. `app.use(expressLayouts);`

- in a layout.ejs file
```
<h1> this is in the layouts ejs file </h1>
<%- body %>
```
