# charAt()
JavaScript method.

Returns a character from a string.

## Syntax
```
 string.charAt(index)
```

## Parameters
`index`: an integer greater or equal to 0.

## Return value
Returns a string which is the character at the specified index. If the passed index is out of bounds, i.e, is a number greater than the length of the string, then an empty string is returned.

## Example 1
```
var char = "hello".charAt(1);
console.log(char) /* Prints 'e' */
```

## Example 2
```
var str = "ThisIsAString";
console.log(str.charAt(6));  /* Prints 'A' */
console.log(str.charAt(256)) /* Prints '' (empty string) */
```
The `charAt()` function is supported by all the main Browsers.
