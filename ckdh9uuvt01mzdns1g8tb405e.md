## Introduction to Element Positioning: (Positions)

A popular myth we might have stumbled upon is that positioning items is a **Nightmare**. However, while this might be true, the idea that it is a nightmare has been reduced drastically over time.

Bootstrap was one technology that helped to position items on a webpage with ease, alongside Flexbox, Grid, and Positions. In this article, we're going to be focusing on Positions, we're going to learn how to place elements where ever we want on a webpage using different position property values.

By the end of this article, you would be able to position items on a webpage using five different position values. No more nightmares, yeah?

## What is Position
The **Position** property is a CSS property that sets how an element is positioned in a document.
```
position:[static] [relative] [absolute] [fixed] [sticky]
```
## Position Values
The Position property can have some values, namely:
* Static
* Relative
* Fixed
* Absolute
* Sticky

After defining the position property, Elements are positioned on the webpage using the **Top**, **Down**, **Left**, and **Right** properties, except, the **static** position is specified first. I know this might be a little confusing at first however, a few examples would make this a lot understandable. Great, let's carry on.
## Position : Static;
Giving an element a position value of **static** changes nothing because the static value takes the normal flow of a webpage, that is to say, Static is the default property value for elements on a webpage.
> Note: The top, bottom, left, and right properties don't apply when the **static** position is defined.  

```
div{
  position: static;
  border: 2px solid green;
  height:150px;
  width: 200px;
}
```
%[https://codepen.io/thesultan00/pen/MWKROwy]

## Position : Relative;
The relative position value is the same as the static position value because it still maintains the normal flow of the webpage. However, relative position lets you set an element's top, right, bottom, and left property relative to its original position without other elements adjusting to fit the space left by the element. Let's look at an example;
```
.learning{
    height:150px;
    width:200px;
    border: 2px solid blue;
    position: relative;
    top: 250px;
    left:450px;
}
.learning1{
    height:150px;
    width:200px;
    border: 2px solid green;
    
}

```
%[https://codepen.io/thesultan00/pen/WNrWXOv]

The element with the relative position value, adjusts according to the **Top** and **Left** properties we defined, and the element without relative position value doesn't adjust to fit the gap left by the former, thereby maintaining the normal page flow.

## Position : Fixed;

An element with a fixed position value maintains a fixed position relative to the viewport. What this means is that it maintains its position even if the page is scrolled. Fixed position can also take the top, right, bottom and left properties to elements on the webpage.
```
div{
  height: 70px;
  width:60px;
  border: 2px solid purple;
  border-radius:15px;
  position: fixed;
  top:250px;
 }
```
%[https://codepen.io/thesultan00/pen/oNbOpbO]

## Position : Absolute;

An Element with `Absolute` position value would be positioned relative to the nearest ancestor that has an absolute or relative position value assigned to it. When there isn't an element with these position values, the element would be positioned relative to the HTML element i.e it would be placed relative to the page itself. 

One thing to note about elements with `Absolute` position is that these elements are **removed from the page flow**. This means is that elements with this type of positioning are not affected by other elements on the webpage neither does it affect other elements on the webpage.
```
.parent{
    height:150px;
    width:200px;
    border: 2px solid red;
    position: relative;
}
.child{
    height:50px;
    width:100px;
    border: 2px solid blue;
    position:absolute;
    top:50px;
    right:0;
}
```
%[https://codepen.io/thesultan00/pen/wvMZbPX]

## Position: Sticky;

The Sticky position value is very unique because it takes two-position values relative and fixed. An element with position sticky will maintain where it is positioned using the Top, Right, Left, and Bottom properties since it is relative but as soon as the page is scrolled to the top, the element becomes fixed and sticks to the top of the webpage.

See [ W3schools](https://www.w3schools.com/css/tryit.asp?filename=trycss_position_sticky) for example.

%[https://www.w3schools.com/css/tryit.asp?filename=trycss_position_sticky]

## Conclusion

Great you made it to the end, I hope you got a grasp of what `positions` are and how to use them.

In this part of the series, we looked at how to place elements where ever we want on a webpage, by specifying the position property and giving it specific position values. In the coming parts of the series, we're going to be looking at other ways we could position elements on a webpage.   
## Attributions
* [W3schools](https://www.w3schools.com/css/css_positioning.asp)
* [CSS-tricks](https://css-tricks.com/absolute-relative-fixed-positioining-how-do-they-differ/)