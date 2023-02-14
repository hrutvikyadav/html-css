# HTML

All html pages start with the declaration `<!DOCTYPE html>`\
All page elements is are nested inside one `<html></html>` tag

HTML elements have `opening` and `closing tags`- `<h1>Heading here</h1>`\
Some elements have a self closing tag- `<img/>`\
HTML attributes are special keywords used inside opening tags to control the element's behaviour
`id` attributes are used to uniquely identify elements

__Inline elements__ appear _side by side_ and not on separate lines\
__Block level__ elements appear on _new lines_

Page content, meant to be rendered on the screen is enclosed in `<body></body>` tags\
Other important information is enclosed in `<head></head>` tags

Adding `name` + `value` attribute to any radio or checkbox items is best practice
___

## Meta

`<title></title>` tags hold the title to display in browser tab\
`lang` attribute of `html` tag denotes language of the page\
ex: `<html lang="en"> </html>`

Determine browser behaviour by adding _self closing_ `<meta>` tags in `<head></head>`\
ex: Tell browser to parse markup in multiple languages with `<meta charset="UTF-8">`

## Headings

`<h1></h1>` to `<h6>` tags are available with lower number signifying more importance
Using a lower rank heading implies start of a subsection

## Paragraphs

`<p></p>` tags are used for paragraphs of text

## Special elements that help with `SEO`, accessibility

These make the _HTML easier to read_

- `<main>` used to identify main section of this page
- `<footer>` used for footer section at the end of page

## Images

`<img/>` is used for image elements
__This is a self closing tag__

Use the `src` attribute to provide link for the image
Also use the `alt` attribute to provide _alternate text to display_ for the __screen reader__, incase _image does not load_

## Link to other pages

Use `a` tag with `href` attribute to link to another page,\
along with link text between the two tags

Use `target` attribute set to "_blank" to __open link in new tab__

```html
<a href="https://freecatphotoapp.com"> Link text here </a>
```

Other types of content can also be converted to link, by enclosing something between anchor tags
example: `<a> <img/> </a>`

## Sections

Use `<section></section>` tags to _separate the HTML elements into sections_

## Lists

Use `ul` for unordered lists, `ol` for ordered lists\
along with nested `<li></li>` to represent list items

## Figure

Use `figure` element to describe self contained content\
Useful to _associate things together_ like images and captions

Nest an image inside `figure` and add `<figcaption>Caption here</figcaption>` element

## Emphasise

`<em></em>` element emphasises text

## Strong/Important text

`<strong></strong>` is used to indicate text that is important

## Forms

Use `<form></form>` element to start a form\
add `action` attribute to indicate URL where _form data is sent_

`<input/>` elements are nested inside form elements to get _different __types__ of data from user_\
Input elements are self closing\
`type` attribute is used to create different input types\

- `type="radio"` i.e. radio buttons are used for multiple options and single answer

    ```html
    <input type="radio"> First Choice
    ```

    > If multiple radio inputs are present, __all must have same name attribute__, so that _selecting one will deselect others_

    When form is submitted, information for radio inputs is based on `name` and `value` attributes\
    If __`value` is absent__, submitted data is _not very useful_\
    used `checked` attribute to _select a radio or checkbox_ by __default__

- `type="checkbox"` is used when multiple answers are correct

`name` attribute is used to _refer to the input data_ when form is submitted to action URL\
`placeholder` attribute gives user a hint regarding expected input\
`required` attribute can be used to prevent form submission, when input is empty\
_By default_, a `<button></button>` element(with no attributes) nested in a form will submit form data to action URL upon click
> Button without attributes will work correctly in forms, but `type="submit"` attribute is still added for clarification

`<label>` is used to _associate an input with a label_, useful for __screen readers__.
ex.

1. Wrap the `input` element and text with label: `<label><input type="radio"> cat</label>`
   > note: this will also cause _clicking_ on the _label text_ to _select the  associated option_
2. Wrap the label text with label tags, and give a `for` attribute that matches the input `id` attribute:\
   `<input id="loving" type="checkbox"> <label for="loving">Loving</label>`

`<fieldset></fieldset>` element is used to group together related `inputs` and `labels` in _forms_\
this is a block level element\
`<legend></legend>` serves as caption for elements in `fieldset`
___
