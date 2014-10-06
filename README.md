css-positions
=============

In a previous [article](https://github.com/owietrich/css-flow), I was saying how CSS normal flow is important and too often misunderstood. Obviously CSS positionning is also really important to know and is the key to mastering layouts.

A *positioned element* is an element whose computed `position` property is `relative, absolute, fixed or sticky`. 

## static

The `static` position is the default position of an element in the [normal flow](https://github.com/owietrich/css-flow). The `top, right, bottom, left and z-index` properties do not apply.

An element which is not positionned is static.

## relative

The position property `relative` allows you to adjust an element's position in the normal flow from its [static](#static) position.

```css
.two {
	position:relative;
	top:30px; left:10px;
}
```

![relative](/assets/relatives.png)


As seen above, you can change the position of a relative element with optional offset properties such as `top, right, bottom, left`. The other elements in the normal flow are displayed as if the relative element were in its normal/static position.

You also can change the `z-index` of a relatively positioned element.

## absolute

An absolutely positioned element is positioned relatively to its closest positioned ancestor (or the document body if any). 


```css
.two {
  position: absolute;
  top: 70px;
  left: 30px;
}
```

![absolute](/assets/absolute.png)

An absolutely positioned element is taking out the normal flow and the other elements are displayed as it wasn't there.


## fixed

An element that has `fixed` as position's value i basically like an element absolutely positionned  to the screen's viewport. It won't move when scrolled or resized. 


## float

## sticky