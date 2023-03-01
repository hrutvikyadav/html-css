# Emmet

## Abbreviations

These are shorthand expressions that are transformed into code blocks after execution\
Syntax looks like `css` with some changes to generate code as needed

```emmet
#page>div.logo+ul#navigation>li*5>a{Item $}
```

This will generate html as follows:

```html
<div id="page">
    <div class="logo"></div>
    <ul id="navigation">
        <li><a href="">Item 1</a></li>
        <li><a href="">Item 2</a></li>
        <li><a href="">Item 3</a></li>
        <li><a href="">Item 4</a></li>
        <li><a href="">Item 5</a></li>
    </ul>
</div>
```

See [syntax documentation](https://docs.emmet.io/abbreviations/syntax/) for more abbreviations

See [cheatsheet](https://docs.emmet.io/cheat-sheet/) for common useful shortcuts

## Shortcuts

1. Ctrl + shift + A

    Wrap in `Abbreviation`\
    This will _generate code from abbreviation_, and place _selected elements_ in __last element generated__

    Control placement of selected text by using `$#` placeholder in the abbreviation like\
    `ul>li[title=$#]*>{$#}+img[alt=$#]`

2. Ctrl + k

    Remove a tag(opening and closing)\
    Place cursor on a tag, then remove it

___
