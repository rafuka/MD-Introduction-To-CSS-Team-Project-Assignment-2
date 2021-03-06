# :only-of-type

CSS pseudo-class selector.

Used to select elements that have no siblings of the given type.

## Syntax
```
<element>:only-of-type {
  ...
}
```
Where `<element>` is an optional CSS selector. If no `<element>` tag is provided, it will match any tag, i.e, any tag that does'nt have a sibling of it's same type will be selected. If `<element>` is specified as an *id* or *class* selector, it will match the type of tag that matches the *is* or *class*.

## Example 1
Consider the following CSS rule:
```
:only-of-type {
  color: green;
}
```
And the following HTML snippet:
```
<body>
  <p>I'm a lonely paragraph, I have siblings but none of them are my type</p>
  <a>I have an anchor sibling!</a>
  <a>I have an anchor sibling too!</a>
</body>
```
The result would look like this:
![Example 1 Image](http://i.imgur.com/Y0tBRbn.png)

As you can see, all the elements had the `color: green` rule applied to them. However, not every element got selected by the `:only-of-type` pseudo class selector. The only elements that got selected where the `body` and the `p` elements. The reason for which the two `a` elements got the rule applied is that they inherited it from the body tag. Remember, there is only one `body` element in any HTML document, so any time you use `:only-of-type` without a preceding selector, the `body` element will be matched.

## Example 2
Consider the following CSS rules:
```
a:only-of-type {
  color: red;
}

p:only-of-type {
  color: green;
}

div {
  border: 1px solid yellow;
}
```
And the following HTML snippet:
```
<div>
  <p>I'm a lonely paragraph, I have siblings but none of them are my type</p>
  <a>I have an anchor sibling!</a>
  <a>I have an anchor sibling too!</a>
</div>
<div>
  <a>I'm a lonely anchor element</a>
  <p>I'm a paragraph with a sibling of my type</p>
  <p>I'm the sibling paragraph!</p>
</div>
```

The result would look like this:
![Example 2 Image](http://i.imgur.com/Nnr8PtG.png)

Only the elements of type `p` and `a` that were "alone", i.e, without any siblings of their same type within their parent containers, got selected.

## Example 3
Consider the following CSS rules:
```
.myclass:only-of-type {
	color: green;
}

#myid:only-of-type {
	color: red;
}

div {
  border: 1px solid yellow;
}
```
And the following HTML snippet:
```
<div>
  <p class="myclass">I'm a lonely paragraph, I have siblings but none of them are my type</p>
  <a class="myclass">I have an anchor sibling!</a>
  <a>I have an anchor sibling too!</a>
</div>
<div>
	<a class="myclass">I'm a lonely anchor element</a>
  <p id="myid">I'm a paragraph with a sibling of my type</p>
  <p>I'm the sibling paragraph!</p>
</div>

```
The result would look like this:
![Example 3 Image](http://i.imgur.com/0Uhlvos.png)

The `p` element with the `id="myid` didn't match the rule because it has another `p` element as a sibling.
The `p` and `a` elements with `class="myclass"` got selected because they do not have sibling elements of the same type.

## Browser compatibility
Chrome (1.0), Firefox/Gecko (3.5/1.9.1), Internet Explorer (9.0), Opera (9.5), Safari (3.2).
