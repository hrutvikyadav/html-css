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

## CSS comments

comments in css are written as `/* this is a comment */`
___

## Units

- `px` : describe values in pixels on the screen
- `%` : values as percentage of parent elements

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
