## Introduction to Element Positioning:(FlexBox)

Hey there, welcome back. If you have been following my ongoing series **Introduction to Elements Positioning**, well you've made it to the third part of the series and here we're are going to be focusing on **FlexBox**.

At the end of this article, you would be able to use the flexbox module and it's properties to layout a webpage beautifully. Alright, let's carry on.

## What is Flexbox?

Flexbox is a CSS module, designed as a one-dimensional layout model which means it deals with one dimension at a time either rows or columns in contrast to the CSS grid which is a two-dimensional model and can take rows and columns together. 
Just like the CSS grid, it is a module because it has a whole lot of properties that help the flexbox model come to life.

Flexbox is activated by setting the display property of a parent element to Flex or inline-flex.

```
.container{
    display: flex || inline-flex;
}
```

## Flexbox Properties

In this article, We're only going to be focusing on  Properties for the Parent Elements(Flex Container).

We're going to be looking at properties from the parent elements property group, that will help you create beautiful and responsive page layouts.

## Parent Elements(Flex Container) Properties

* Display
* Flex-direction (row, row-reverse, column, column-reverse)
* Flex-wrap (wrap, nowrap, wrap-reverse)
* Flex-flow 
* Justify-content (center, flex-start, flex-end, space-around, space-between)
* align-items (center, flex-start, flex-end, stretch)

## Display 

By setting a parent element's display property to Flex or Inline-flex, you have activated Flexbox. let's look at the example below ;

```
.container{
    display: flex;
}
```

## Flex-direction

The flex-direction property defines what direction the flex-items would be arranged in, this could be in rows or columns i.e horizontally or vertically. 

let's look at some examples to show us the various flex-direction values; 

```
.container {
    display:flex;
    flex-direction : row;
}
```
%[https://codepen.io/thesultan00/pen/xxVWMOY]

The row value sets the horizontal direction of the flex-items, from left to right.

```
.container{
    display: flex;
    flex-direction:row-reverse;
}
```

%[https://codepen.io/thesultan00/pen/qBZogRK]

The row-reverse value sets the horizontal direction of the flex-items, but this time from right to left.

```
.container{
    display: flex;
    flex-direction:column;
}
```
%[https://codepen.io/thesultan00/pen/VwaXgbq]

The column value sets the vertical direction of the flex-items, from top to bottom.


```
.container{
    display: flex;
    flex-direction:column-reverse;
}
```

%[https://codepen.io/thesultan00/pen/VwaXgWq]

The column-reverse value sets the vertical direction of the flex-items, but this time from bottom to top.

## Flex-wrap

The flex-wrap specifies whether or not flex-items should continue on their specified direction which may cause some scrolling or wrap. let's look at some examples that explain better; 

```
.container{
  display:flex;
  flex-direction : row;
  flex-wrap : wrap;
}
```

%[https://codepen.io/thesultan00/pen/vYGRPKN]

Notice how the flex-items wraps? So that now there is no more scrolling 

```
.container{
  display:flex;
  flex-direction : row;
  flex-wrap : nowrap;
}
```
%[https://codepen.io/thesultan00/pen/abNYMBx]

The `nowrap` value is the default value for flex-items, which means there still is going to be some scrolling.

```
.container{
  display:flex;
  flex-direction : row;
  flex-wrap : wrap-reverse;
}
```

%[https://codepen.io/thesultan00/pen/XWdEGpo]

The wrap-reverse value wraps the flex-items in reverse.

## Flex-flow

The flex-flow flexbox property is a shorthand property for setting the `flex-direction` and `flex-wrap` of a flex-box container.

```
.container{
  display:flex;
  flex-flow : row wrap-reverse;
}
```

%[https://codepen.io/thesultan00/pen/BaKrbwd]

## Justify-content

Justify-content property is used for aligning items in a flex container.

```
.container{
  display:flex;
  flex-flow: row wrap-reverse;
  justify-content: center;
}
```
%[https://codepen.io/thesultan00/pen/ZEWxNgx]

the center value aligns items to the center of the flexbox container.

```
.container{
  display:flex;
  flex-flow: row wrap-reverse;
  justify-content: flex-start;
}
```
%[https://codepen.io/thesultan00/pen/ExKEBxO]

flex-start value aligns items to the start of the flexbox container.


```
.container{
  display:flex;
  flex-flow: row wrap-reverse;
  justify-content: flex-end;
}
```

%[https://codepen.io/thesultan00/pen/zYqWVOm]

flex-end value aligns items to the end of the flexbox container.



```
.container{
  display:flex;
  justify-content: space-around;
  background-color : black;
}
```

%[https://codepen.io/thesultan00/pen/bGpvyrV]

the space-around value specifies space before, between, and after a flex-item in a  flexbox container.


```
.container{
  display:flex;
  justify-content: space-between;
  background-color : beige;
}
```

%[https://codepen.io/thesultan00/pen/RwaMmJX]

the space-between value specifies space between a flex-item in a  flexbox container.

## Align-items

While the `justify-content` property aligns items on the horizontal axis, the `align-items` property aligns items on the vertical axis.

let's look at the values for the `align-items` property;

```
.container{
  background-color:yellow;
  height: 600px;
  display:flex;
  align-items:center;
}

```

%[https://codepen.io/thesultan00/pen/bGpMpEb]

`align-items: center` aligns the flex-items to the center of the flex-container on a vertical axis.

```
.container{
  background-color:yellow;
  height: 600px;
  display:flex;
  align-items:flex-start;
}

```
%[https://codepen.io/thesultan00/pen/qBZYZwL]

`align-items: flex-start` aligns the flex-items to the start of the flex-container on a vertical axis.



```
.container{
  background-color:yellow;
  height: 600px;
  display:flex;
  align-items:flex-end;
}

```
%[https://codepen.io/thesultan00/pen/rNeveEv]

`align-items: flex-end` aligns the flex-items to the end of the flex-container on a vertical axis.



```
.container{
  background-color:yellow;
  height: 400px;
  display:flex;
  align-items:stretch;
}

```
%[https://codepen.io/thesultan00/pen/KKzRMPv]

`align-items: stretch` stretches flex-items to fill the flex-container on a vertical axis.

## Conclusion 

The `flexbox` module has eased front-end web development and brought a new way to position items with ease. It's comes packed with simple to read properties that make it have an even better learning experience.

This brings me to the end of this article. In this part of the series, we looked at how to layout a webpage,  using the Flexbox module. I hope you had a wonderful time, cheers ;-)


