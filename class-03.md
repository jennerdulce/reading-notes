## Mustache Templating
- Separation of concerns
- Templating helps to separate HTML from Javascript
  - The person working frontend (HTML) can create their own template which asks for values that will be replaced within the code.
```
  <script id="image-template" type="x-tmpl-mustache">
    <section class="{{ class }}">
      <h2>{{ title }}</h2>
      <img src="{{ image }}" alt="{{ description }}" title="{{ title }}" >
      <p>{{ description }}</p>
    </section>
  </script>

```
- The person working backend (Javascript) will then follow a series of steps:
1. Make variable and target the template (which is a script/template)
2. Make a variable and run the `Mustache.render(insert template, { add keys and values for template }`
  - This inserts the template. Using the same KEYWORDS, will replace the {{ keywords }} within the HTML file.
3. Append to where you want the script to be displayed
```
function renderImages(arr, page) {
  arr.forEach(function (value) {

    // MUSTACHE -----
    let $imageTemplate = $('#image-template').html();
    let $rendered = Mustache.render($imageTemplate, {
      class: `${value.keyword} horns${value.horns} ${page}`,
      title: value.title,
      image: value.url,
      description: value.description
    });
    $('#container').append($rendered);
  });
}
```

## Flexbox
- Flexbox is exremely useful to make the Webpage dynamic
- is especially helpful for evenly spacing out elements/contents

- container needs `display: flex` in order for commands to work.
- `flex-direction: row/row-reverse/column/column-reverse`
- `flex-wrap: wrap`
- `justify-content` aligns on main (horizontal axis)
- `align-items` aligns on cross (vertical axis)
- `order` can place elements in a specific order. the lower the number the more forward it will be
- `flex-grow` all items start with a value of 1. Changing this value would mean that the item takes a multiple of the other spaces
