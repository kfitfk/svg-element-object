Convert an SVG node to a JavaScript object, say

```js
var ElementObject = require('svg-element-object');

/* provided element
<linearGradient
  id="c_11_"
  gradientUnits="userSpaceOnUse"
  x1="333" y1="21.5" x2="333" y2="90.5">
*/

var elObj = ElementObject(element);

/*
{
  type: 'linearGradient',
  x1: 333,
  y1: 21.5,
  x2: 333,
  y2: 90.5
}
*/
```

The default properties only contains those useful to my use cases. So provide an attribute list to fetch other attributes.

```js
var elObj = ElementObject(element, ['gradientTransform']);
```