## Basic example

```
@import oobleck
#container
  container()
  #mainfocus
    row()
    #gianttagline
      span 12
  #detailedinfo
    row()
    #sec1
      span 4
    #sec2
      span 4
    #sec3
      span 4 true
```

You probably thought, "WTF was that?" Let me break it down for you.

## The breakdown
`@import oobleck` loads Oobleck into your .styl file.

`container()` turns the div into a container. This will make the div the full page width (the width of the browser with 20px of padding inside on the left and right). You can use one big container, or use multiple to break the page horizontally.

`row()` turns the div into a row of columns. It centers them and defines the 1280px max-width of the content.

`span(#,["true"])` defines the width of the column. If you add `true` to the end of the mixin, it will remove the gutter of the column. You can nest columns up to one extra level.

Now that you have the basics, read on for the full syntax.

## The syntax
### Import
Loads Oobleck into your .styl file.

    @import oobleck

### Containers
Turns the div into a container. This will make the div the full page width (the width of the browser with 20px of padding inside on the left and right). You can use one big container, or use multiple to break the page horizontally.

    container()

### Rows
Turns the div into a row of columns. It centers them and defines the 1280px max-width of the content.

    row()

### Columns
#### Width
Defines the width of the column. If you add `true` to the end of the mixin, it will remove the gutter of the column. You can nest columns up to one extra level.

```
span 4  // Regular column

span 6 last // Removes gutter

span 12  // Automatically sets as last column based on max number of columns
```

#### Prepend
Adds space before the column

    prepend 2

#### Append
Adds space after the column

    append 2

### Mobile
#### Hide from mobile browser
Only display this content in wider browsers (not mobile browsers)

    d-only()

#### Only show in mobile browser
Only display this content in mobile browsers (smaller window)

    m-only()