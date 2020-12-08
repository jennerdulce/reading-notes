## Responsive Web Design
- Practice of building a website suitable to work on every davice/screen size
- Responsive: React quickly and positively to change
- Adaptive: Easily modified for new purpose/situation
- Mobile: Build website new domain solely for mobile users.
- Favor design that dynamically adapts to different browser and device viewports

### Flexible Layouts
- Build with a flexible grid capable of dynamically resizing to any width
- use units '$' or 'em'
- vew,vh, vmin, vmax
- When adjusting margin: 10px / total width = result
  - `margin: result`
  
### Media Queries
- Media queries provide the ability to specify different tyles for indivdual browser and device circumstances
@import 'styles.css'
@media (min-width: #)
- When media feature and value allocate to true, styles wiill be applied. False, will be ignored

### Logical Operators in Media Queries
- 'and' 'not' 'only'
- Media Features: Identify what attributes of properties will be targeted within media query expression
- height and width are based off vierport rendering area

### Orientation
- `@media (orientation: landscape)`

### Aspect Ratio
- `@media (min-device-aspect-ration: 16/5)`
- Use media queries to add/remove floats and change their widths

### Identifying Breakpoints
- Should adjust to an array of different viewpoer sizes
- Breakpoints should only be introduced when a website starts to break

### Mobile First
- Target sall viewports as default styles for the website
- Then use media queries as the viewport grows
- Use media queries to remove excess animation/css
  - Animation, shadows transforms, will be slower and drain battery life on mobile devices
- `IMPORTANT: <meta name="viewport" content = "width=device-width, initial-scale=1.0">`
- 
 @viewport {
 width: device-width;
 zoom:1 ;

- `content="user-scalable=yes"`

### Flexible Media
- Media doesn't always follow suit
  - images, videos and others tend to be scalable
   ` img, video, canvas {max-wdith: 100%}`
- Embedded media needs to be `position: absolute` to a parent container with a width of 100% and height of 0
  - `padding-bottom` should be added as well. Based on aspect ratio
```
figure {
height: 0;
width: 100%;
padding-bottom: 56.25%;
position: relative
}

iframe {
position: absolute;
height: 100%;
width: 100%;
top: 0;
left: 0
}
```

## All About Floats
### What are Floats used for?
- Can configure entire web layouts. However there are stronger tools for creating layout on web pages such as FLEXBOX or GRID
- Floats are especially helpful for smaller layouts.
  - Compared to using positoning. Elements stacked next to floats auto adjust.

### Clearing the Float
- `clear: both` is floats sister property. clear also has values of, left, right, or none

### The Great Collapse
- If a parent element (container) only contains float elements. the container will crash.
- be sure to clear the float after the floated elements in the container, but before the close of the container

#### Techniques for Clearing Floats
1. Create an empty div and `clear: both`
2. CSS for the parent element. set `overflow: auto/hidden`

```
.clearfix:after { 
   content: "."; 
   visibility: hidden; 
   display: block; 
   height: 0; 
   clear: both;
}
```

### Problem with Floats
- Sometimes images will break out of containers
- Items will be pushed down
- Double Margins
- 3px Jog

Resources:
- https://learn.shayhowe.com/advanced-html-css/responsive-web-design/
- https://css-tricks.com/all-about-floats/
