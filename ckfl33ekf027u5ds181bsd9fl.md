## The Right Pick (CSS Selectors)

When I started learning how to write CSS(cascading style sheet), one of the problems I faced was declaring style rules that just won't apply for some reason, well that was because I was either using the wrong selectors or I didn't know how to properly select an element when it was nested.

Selectors in CSS are rules that specify what styles would be applied to specific HTML elements. It is a way to select particular elements to receive a particular set of styling rules.

At the end of this article, you would be able to understand the full concept of CSS selectors and how to use them to apply styling rules to HTML elements.

## Types of Selectors 
* Element Selectors 
* Class Selectors
* ID Selectors
* Universal Selector 
* Attribute Selectors
* Grouping Selectors (Selector list)
* Combinator Selectors
* Pseudo Selectors

Now let us go over each type of selector and see their use cases.

## Element Selectors

The Element selector is used to select specific elements by calling their tag name.

> tagname {style properties}

```
p{
    color:red;
}
```
in the example above we are styling the p tag, using the element selector.

## Class Selectors

The class selector is used for applying the same style rule to multiple elements with the same class attribute.

> .classname {style properties}

```
.wide-cover{
    color:red;
    font-weight:bold;
}
```

## ID Selectors

ID selectors are used for selecting a specific element to be styled, the same ID can not be given to two or more elements.

> #id_value {style properties}

```
#pacer{
    border : 2px solid green;
}
```

## Universal Selector

The universal selector **(*)** Asterisk can is used for styling elements of any type on a webpage.

>  *{style properties}

```
*{
    text-align : right;
}
```

## Grouping Selectors (Selector list)

The selector list can be used to group different elements to apply specific style rules to them.

> element, element, element {style properties}

> .classname, .classname, .classname {style properties}

> #id_value, #id_value, #id_value {style properties}

> element, .class_name, #id_value {style properties}

```
p, #pacer, .content{
    text-align : right; 
}
```

## Combinator Selectors

* Adjacent sibling selectors
* Child selectors
* Descendant selectors 

### Adjacent sibling selectors 

The adjacent sibling selector applies style rules to elements that come after a particular element only if they are both children of the same parent element 

> h2 + p {style properties}

```
<div>
    <h2>Hello there</h2>
    <p>It's a great time to be alive</p>
</div>
```
```
h2 + p {
    color : red;
    text-align : right;
}
```

### Child selectors 

The child selectors apply style rules to elements that are direct children of the parent element.

> h2 > p {style properties}

```
h2 > p {
    color : red;
    text-align : right;
}
```

### Descendant Selectors 

The descendant selectors apply style rules to the elements that are descendants of an ancestor element (parent, parent's parent, parent's parent's parent, etc).

> h2 p {style properties}

```
h2 p{
    color : #ffffff;
    cursor :pointer;
}
```

## Pseudo Selectors

Pseudo selectors are special keywords that are added to a selector that specifies a state for when the style rules are to be applied.

> h2 :hover {style properties}

```
h2:hover{
    color : blue ;
}
```

in the example above, the style properties would only be applied when the cursor hovers on the h2 element. 

find the index of more standard pseudo-classes [here](https://developer.mozilla.org/en-US/docs/Web/CSS/Pseudo-classes).

## Conclusions

CSS Selectors are a very important part of CSS even as important as CSS itself, understanding how it works properly is very critical. it helps us pick and choose what particular element to receive a set of styling rules.

Congratulations, you have made it to the end of this article :satisfied: .
hit me up or follow me on twitter [@D_Kingnelson](https://twitter.com/D_kingnelson)