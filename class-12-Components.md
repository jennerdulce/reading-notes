# Components and EJS partials
references: 
https://medium.com/@henslejoseph/ejs-partials-f6f102cb7433
https://www.youtube.com/watch?v=3_xEEH4fTEk&t=0s&index=7&list=PL7sCSgsRZ-slYARh3YJIqPGZqtGVqZRGt&ab_channel=WalkThroughCode

- use case
  - nav bar, footer, or any reusable static code that you want across multiple pages
  - partials are handy when you want to reuse the same HTML across multiple views
- partials are similar to functions such that you can change content in multiple pages by altering 1 area of your code.

- How to use components/EJS partials:
1. create folder called partials
2. create an ejs file that has markup that you want to embed into pages.
  - you may want to make an ejs folder name `footer.ejs` or `navbar.ejs` that contain the correspoinding layouts
  - this file should not contain other markup.. html, head, body, doctype etc
3. withing the ejs file that you want to display this markup in
  - `<%- include('FILEPATH')%>`
  - place `<%- include('partials/ejsfile')%>` anywhere you want
  - ** The command starts the filepath within the "views" directory by default. **
  - you typically want to insert these statements into the same areas across your EJS files.
