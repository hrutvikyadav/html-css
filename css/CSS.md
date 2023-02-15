# CSS

Use `type selectors` to select HTML elements and style them with `property` and `value`

```css
h1 {
    text-align: center;
    ^^^         ^^^
    property    value
}
h2 {
    text-align: center;
}
^^^
css rule
```

One problem with this is repitition of same styles

We can select multiple elements and apply common styles in the same place

```css
h1, h2 {
    text-align: center;
}
```

As stylesheets can grow big, it is best to include styles in a separate file with `.css` extension\
then link this file in the html document

___

## Default styles

When a stylesheet is loaded in browser, browser applies some default styles to some common elements\
To make sure your styles work correctly, target these elements and override default browser styles
> Also see fallback values

## CSS comments

comments in css are written as `/* this is a comment */`
___

## Units

- `px` : describe values in pixels on the screen
- `%` : values as percentage of parent elements
- `vh` : value as % of _viewport height_
- `rem` : _root em_ holds values relative to html element font size

___

## Selectors

### Class selectors

Used to target elements by class name, preceeded by a `.`

```css
.some-class {
    /* ...styles */
}
```

> Only works if an element with _given class name exists_ in `html`

### Child selectors

Select a nested element by specifying parents

```css
.item p {
    /* selects p element inside el with class of "item" */
}
```

### Pseudo selectors

Used to select `pseudo` elements, meaning focused, hovered, visiten link elements among others

```css
a:visited {
  color: grey;
}
```

### Attribute selectors

These will select elements based on provided attributes

```css
div[class="container1"] { }
/* selects div with class attr of container1*/
```

## Shorthand properties

for properties like `margin-top`, `margin-bottom` etc, we can use shorthand `margin` property to style all of them at once

```css
div {
    margin: 5px, 10px;
            ^^^  ^^^
    [top,bottom] [left,right]

    /* or provide a single value to set all */
    padding: 2px;
}
```

## Colors

One way to write _color values_ is by _color name_

There are 2 color models:

1. additive RGB used in electronic devices
2. subtractive CMYK (cyan, magenta, yellow, black) used in printing

`rgb(red, green, blue)` _css function_ uses _RGB model_, i.e colors start as black and change as R, G, B shades are added\
It takes rgb color values from _0(0% color) to 255(100% color)_ and produces a final color

> rgb are primary colors, which gives white when combined\
secondary colors are obtained by mixing primary colors\
tertiary colors are obtained by combining a primary and nearby secondary color\
In a color wheel, _similar colors(hues)_ are _close together_, and different colors are _far apart_\
Colors opposite to each other on color wheel are complimentary, which produce gray when combined, and strong contrast when placed side by side
>> Note that text can be hard to read if placed on complimentary background\
It is best to choose one color as the dominant color, and use its complementary color as an accent to bring attention[^example]

- yellow> red + green
- cyan> green + blue
- magenta> red + blue

___

- orange> red + green(127)
- spring green> green + blue(127)
- violet> red(127) + blue
- chartreuse green> green + red(127)
- azure> blue + green(127)
- rose> red + blue(127)

`Hex values` can also be used for colors\
These start with `#` and have a six character value (0-9, A-F)
> _1st two chars_ represent __red__, _next two_ represent __green__, and _last two_ represent __blue__
>
> ```css
> div {
>   background-color: #FF007F
>                      ^ ^ ^
>                      r g b
> }
> ```

`hsl(hue, saturation, lightness)` or hue-saturation-lightness can also be used for colors\
hue ranges from 0-360, representing angle of hue on color wheel\
where r -> 0, g -> 120, b -> 240 degrees

saturation(intensity) and lightness(brightness) are expressed from 0%-100%\
for saturation 0% is gray and 100% is pure color\
for lightness, 0% is black, 100% is white, 50% neutral

___

### Gradient

Color transitions or gradient can be obtained with `linear-gradient(direction, color1, color2, ...)`[^g-dir] function\
If no gradient-direction arg is provided, default `180deg` is assumed
It can be used to control _direction of transition_ and which _colors to use_(min 2 colors)
> `linear-gradient` _creates an image_ and is used along with _`background` property_ that can accept _image `value`_

```css
.red {
  background: linear-gradient( 90deg, rgb(255, 0, 0), rgb(0, 255, 0) );
}
```

Color stops are used to determine color placement along gradient line\
i.e. _space taken by a color_ on the _gradient line_ is decided by _color stop value_\
They are length units(px, % etc) that follow a color
> Color stops of 0%, 50%, 100% is applied by default for 3 colors, i.e. the _function automatically spreads out all colors evenly_

```css
...
background: linear-gradient(180deg, rgb(255, 0, 0) 0%, rgb(0, 255, 0) 50%, rgb(0, 0, 255) 100%);
...
```

### Opacity

__Colors can be combined__ with `opacity` or `alpha channel` to change it's transparency\
`opacity` property takes values from 0 to 1.0(opaque)\
`alpha channel` can be used to _set color and opacity in one go_, with the `rgba()` function, it works the same as `rgb()`, just takes _extra parameter for alpha channel_
___

## Box model

Css box model treats all html elements as a box having 4 areas

1. Content - this is the item inside elements, has a height and width
2. Padding - space surrounding the content
3. Border - encloses padding and content, i.e. the element
4. Margin - the area outside element/border, used to control spacing between elements

___

[^example]: youtube's red buttons on black background

[^g-dir]: 90deg-or-180deg-most-common
