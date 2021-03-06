css-positions
=============

In a previous [article](https://github.com/owietrich/css-flow), I was saying how CSS normal flow is important and too often misunderstood. Obviously CSS positionning is also really important to know and is the key to mastering layouts.

A *positioned element* is an element whose computed `position` property is `relative, absolute, fixed or sticky`.

> we won't talk about sticky positionning since it's not widely supported 

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

![relative](/assets/relative.png)


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


 > animations are faster on elements taken out the flow because they won't trigger repaint, relayout or reflow on sibling elements.

## fixed

An element that has `fixed` as position's value i basically like an element absolutely positionned to the screen's viewport. It won't move when scrolled.

It is useful to create a floating element that stays in the same position.

## float

`float` is a CSS positionning property that takes an element out the normal flow and shifted it to the `right` or `left` to its ancestor element.

```css
.floating {
  float: left;
}
```

![float](/assets/float.png)

Its sibling elements in the normal flow will fill the empty space left. This is why floating elements are commonly used to do text wrap.

![wrap](/assets/wrap.png)

I don't like using `float` to layout interfaces because it forces you to clearfix (using the `clear` property ) a sibling element in order to move it down past the float or to prevent the parent to collapse.

  > If you just need to display one element next to an other, you would prefer using [inline-blocks](https://github.com/owietrich/css-flow/#inline-block). It has the advantage to do exactly what you need and to keep your element in the normal flow.



If you have any questions or comments, please feel free to post an [issue](https://github.com/owietrich/css-positions/issues).

## License

The MIT License (MIT)

Copyright (c) 2014 Olivier Wietrich <olivier.wietrich@gmail.com>

Permission is hereby granted, free of charge, to any person obtaining a copy of this software and associated documentation files (the "Software"), to deal in the Software without restriction, including without limitation the rights to use, copy, modify, merge, publish, distribute, sublicense, and/or sell copies of the Software, and to permit persons to whom the Software is furnished to do so, subject to the following conditions:

The above copyright notice and this permission notice shall be included in all copies or substantial portions of the Software.

THE SOFTWARE IS PROVIDED "AS IS", WITHOUT WARRANTY OF ANY KIND, EXPRESS OR IMPLIED, INCLUDING BUT NOT LIMITED TO THE WARRANTIES OF MERCHANTABILITY, FITNESS FOR A PARTICULAR PURPOSE AND NONINFRINGEMENT. IN NO EVENT SHALL THE AUTHORS OR COPYRIGHT HOLDERS BE LIABLE FOR ANY CLAIM, DAMAGES OR OTHER LIABILITY, WHETHER IN AN ACTION OF CONTRACT, TORT OR OTHERWISE, ARISING FROM, OUT OF OR IN CONNECTION WITH THE SOFTWARE OR THE USE OR OTHER DEALINGS IN THE SOFTWARE.
