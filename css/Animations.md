# Animations

## transform-origin

This is used to set a reference point of origin of css transformations

set value to `0% 0%` to set origin to offset 0% from top and 0% form left\
i.e. top left corner of element

## transform

used to apply a transform to element

set to `rotate(60deg)` to rotate element 60 degrees from _origin point_

## @keyframes

this is used to define animation flow. It is possible to create selectors to target points in animation sequence like 0%, 25%\
`from` and `to` can also be used to define sequence start and end

requires __name__ to be assigned to @keyframe rule
`@keyframes wheel {}` rule is associated with _name 'wheel'_
> use this `animation name` to link a @keyframes rule to desired css selector

link a css selector to the @keyframes rule using `animation-name` property\
then use `animation-duration` property to set time(`s` or `ms`) which the animation takes to complete

## animation-timing-function

used to define how animation plays out as time progresses

## animation-iteration-count

used to define how many times animation will repeat
___
