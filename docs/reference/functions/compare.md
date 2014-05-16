# Function compare

Compare two values. Returns 1 when x > y, -1 when x < y, and 0 when x == y.

x and y are considered equal when the relative difference between x and y is smaller than the configured epsilon. The function cannot be used to compare values smaller than approximately 2.22e-16.

For matrices, the function is evaluated element wise.


## Syntax

```js
math.compare(x, y)
```

### Parameters

Parameter | Type | Description
--------- | ---- | -----------
`x` | Number &#124; BigNumber &#124; Boolean &#124; Unit &#124; String &#124; Array &#124; Matrix | First value to compare
`y` | Number &#124; BigNumber &#124; Boolean &#124; Unit &#124; String &#124; Array &#124; Matrix | Second value to compare

### Returns

Type | Description
---- | -----------
Number &#124; BigNumber &#124; Array &#124; Matrix | Returns the result of the comparison: 1, 0 or -1.


## Examples

```js
var math = mathjs();

math.compare(6, 1);           // returns 1
math.compare(2, 3);           // returns -1
math.compare(7, 7);           // returns 0

var a = math.unit('5 cm');
var b = math.unit('40 mm');
math.compare(a, b);           // returns 1

math.compare(2, [1, 2, 3]);   // returns [1, 0, -1]
```


## See also

[equal](equal.md),
[unequal](unequal.md),
[smaller](smaller.md),
[smallereq](smallereq.md),
[larger](larger.md),
[largereq](largereq.md)


<!-- Note: This file is automatically generated from source code comments. Changes made in this file will be overridden. -->