## JavaScript and jQuery book by Jon Duckett pages 293-301, 306-331 and 354-357
- jQuery is JD that you include in webpages
- find elements using CSS-Style selector
- Then do somethingwith it
```
$('selector')
$('#id')
$('.class')
$('div p')
```
- syntax is much simplier than vanilla JS.
- you can store jQuery object/elemnt reference in a variable
- use jQuery methods and properties to manupliate values and DOM nodes
- do something with the elements using jQuery methods

`$('li.hot').addClass('complete')`
- each method has parameters that provide details about how the element is updated
- jQuery does not need fallback code
- easier to target elements
- event handling made simplier
- chaining methods

```
var content = $('li').text() // gets data
$('li').text("change text") // sets data
```

- Implicit iteration: methods affect all elements without having to loop
` $('element').hide().delay(500).fadeIn(400)`

- methods are used to update the jQUery selection.
- if one method of the chain is wrong, they chain does not work

```
$(function() {
  // code block
}
```
- creates function level scope
-prevents naming collisions
- checks to see if page is ready to work with

`$('li:contains('word')')`
- targets the li that has word in the text content

## Get/Set CSS properties
- `.css()` method lets you get or set the values of CSS properties
- `var color = $('li').css('color')` // gets
- `$('li').css('color', 'blue')` // sets
- It is better to trigger change in CSS by adding or removing a class rather than chainging CSS directly in jQuery/JavaScript


#### Getting Setting Methods
- `.html()`
- `.text()`
- `.attr()` // creates attr if does not currently exist
- `.removeAttr()`
- `.addClass()` // can add more than 1 class by adding spaces in between
- `.removeClass()`

#### Inserting/Creating Methods
- `.append()` // within the element
- `.prepend()`
- `.before()` // outside of the element
- `.after()` // outside of the element

## 6 Reasons Why for Pair Programming
