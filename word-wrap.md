# word-wrap

CSS property.

Used to specify how words within text should be treated when reaching the limits of its container.

## Syntax
```
word-wrap: <value>;
```

## Values
### normal
The default value. When the `word-wrap` property is set to `normal`, any word that is longer than the width of the container
will overflow.

### word-break
The `word-break` value allows the browser to break words longer than the width of the container, preventing overflow.

## Example 1
Consider a paragraph with the following CSS rules.
```
p { 
  word-wrap: normal;
  background-color: salmon;
  width: 100px;
}
```
![Example 1 Image](http://i.imgur.com/JrnOlaC.png)

## Example 2
Now lets look at the same paragraph with the `break-word` value set to the `word-wrap` property.
```
p { 
  word-wrap: break-word;
  background-color: salmon;
  width: 100px;
}
```
![Example 2 Image](http://i.imgur.com/nD0jYmO.png)

## Notes 
The `word-wrap` property has been renamed to `overflow-wrap` in the current CSS3 Text specification. This two properties have
the exact same functionality.
