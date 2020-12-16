## Grid
- Easily style HTML in 2 Dimensions
- `display: grid` on the container
- `grid-template-columns:` 1fr 1fr 1fr // 70% 30%
  - `grid-template-columns: repeat(3, 1fr)`
- `column-gap row-gap: 1em` is really useful and a perfect amount of spacing
- `grid-auto-rows:#` sets the height of the rows
- `grid-auto-rows: minmax(100p, auto)`
- `justify-items:` aligns horizontally
- `align-items:` aligns vertically within their container
  - `place-items: (align) (justify)`
- `align-self:` individually aligns

### Taking up more space
- `grid-column: 1/3` takes up spaces (columns/width) from line 1 to 4
- `grid-row: 2/4` takes up spaces (rows/height) from line 2 to 4
- `gap: (#row) (#col)`

### Creating Grid Tempalates
```
.box1 {
  grid-area: header
}
.box2 {
  grid-area: main
}
.box3 {
  grid-area: sidebar
}
.box4 {
  grid-area: footer
}

grid-template-area:
  "header header header header"
  "main main . sidebar"
  "footer footer footer footer"
```
- You create a templatae
### Nested/Subgrids
- Set one of the contents in the current grid as `display: grid` and create more divs in the div

### RegEx (Regular Expressions)
- Useful for extracting information from any text by searching for one or more matches of a specfici search pattern
- once you've learned syntax, can be used in all programming languages with slight syntax variations

### Basic Topics
#### Anchors '^' and '$'
- `^The`  beginning of text
- `end$` end of text
- `^The end$` starts with 'the' ends with 'end'
- roar finds roar

#### Quantifiers '*''+''?' and '{}'
- `abc*` finds 0 or more c
- `abc+` finds 1 or more c
- `abc?` finds 0 or ONE c
- `abc{2}` finds 2 c
- `abc{2, }` finds 2 or more c
- `abc{2, 5}` finds 2 up to 5 c
- `a(bc)*` finds 0 or more copies of bc

#### Character Classes '\d''\w''\s' and '.'
- `\d` identifies digits
- `\D` identifies NON-digits
- `\s` identifies whitespace
- `\$\d` identifies money sign followed by a digit


#### Bracket Expressions
- `[abc]` matches any of these letter
- `[a-z]` identifies a range
- `[a-z0-9]` 
- `[^a-zA-z]` ^ in a bracket represents NOT; is not a letter from these ranges 
- `` 

#### General

#### Flags
- `/ word /i` ignores case sensitivity
- `/ word /i` finds all cases
