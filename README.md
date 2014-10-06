css-positions
=============

In a previous [article](https://github.com/owietrich/css-flow), I was saying how CSS normal flow is important and too often misunderstood. Obviously CSS positionning is also really important to know and is the key to mastering layouts.


Whatever you are a JavaScript developer or a designer it is really important to 


  > as a JavaScript developer I think it is really important to know really well HTML and CSS


A positioned element is an element whose computed `position` property is `relative, absolute, fixed or sticky`. 

## static

The `static` position is the default position of an element in the [normal flow](https://github.com/owietrich/css-flow). The `top, right, bottom, left and z-index` properties do not apply.

An element which is not positionned is static.

## relative

The position property `relative` allows you to adjust an element's position in the normal flow. 







For starters, we can adjust a relatively positioned element with offset properties: top, right, bottom, and left. Using the markup from our previous example, let’s add an offset position to #box_2:



This keyword lays out all elements as though the element were not positioned, and then adjust the element's position, without changing layout (and thus leaving a gap for the element where it would have been had it not been positioned). The effect of position:relative on table-*-group, table-row, table-column, table-cell, and table-caption elements is undefined.


## absolute

## fixed

## float

## sticky