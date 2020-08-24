## Introduction to Element Positioning:(CSS Grid)

The introduction of CSS grid was a breakthrough for webpage layout, it was a new and easy way to place elements on a webpage where ever you'd want. 

CSS Grid is a powerful property because sides letting us easily layout a webpage, it also helps with responsive web design, allowing our webpage look good on various screen sizes.

By the end of this article, you would be able to layout a webpage with CSS Grid effectively, using different Grid properties.

## What is CSS Grid?

CSS Grid is a two-dimensional layout system, which means it works with rows and columns that is used to position elements on a webpage.

CSS Grid is activated by setting the display property of a parent element to **grid**, **inline-grid**, or **subgrid**.

```
.container{
    display:grid inline-grid subgrid;
}
```

## Grid Properties

We're going to be looking at two property groups, namely: 
**Properties for the Parent Elements(Grid Container) and Properties for the Children Elements(Grid Items).**

In this article, we're going to be focusing on some properties from each property group, that's going to help you create beautiful and responsive page layouts.

##  Parent Elements(Grid Container) Properties

* Display
* Grid-template-columns (repeat, auto-fill and minmax)
* Grid-template-rows
* Gap

## Display 
By setting a parent element's display property to **grid**, you have activated the CSS Grid system. let's look at the example below ;
```
.container{
    display:grid;
}
```

## Grid-template-columns

This grid property is used to define the columns of a grid system, think of this as the width of the element. The values can be lengths, percentages, or fractions. In this article, we're going to be using fractions.

```
.container{
  display:grid;
  grid-template-columns: 1fr 1fr 1fr;
}
```

%[https://codepen.io/thesultan00/pen/jOqqawO]

Let's analyze our code. We set the display property of the container to **Grid** which activates the CSS grid layout system and the **grid-template-columns** to **1fr**.

Notice how we put in **1fr** thrice? Well, that simply means, take a third of the container 3 times, so 1/3. Let's look at the code below;

```
.container{
    display:grid;
    grid-template-columns: 1fr 1fr 2fr;
}
```

In the example above, **2fr** is going to take twice the size of **1fr** whilst **1fr** reduces in size so that when the new size of **1fr** is added it gives the exact amount of the size left by **2fr** and they can all fit into the container. 

Another way to set the values for the **grid-template-columns** is to use the **repeat()** value. Let's look at how this works below;

```
.container{
    display:grid;
    grid-template-columns: repeat(3, 1fr);
}
```

The above code would produce the same result, it's just a faster way to set the values. The first value specifies how many times you want to repeat and the second set the value you want to repeat.

> **NOTE:** The fraction unit is more advisable to use when working with the grid system because it takes into account other factors like the gap between the elements in the container and then adjusts so that it can fit in properly; we'll get a better understanding of this when we get to the gap property. 

## Grid-template-rows

The **grid-template-rows** property is used to define the rows of a grid system, think of this as the height of the element. The values can be lengths, percentages, or fractions.

```
.container{
  display:grid;
  grid-template-columns: repeat(3, 1fr);
  grid-template-rows: 1fr 2fr;
}
```

%[https://codepen.io/thesultan00/pen/NWNroQB]

## Gap

The **gap** property is used to set the space between items on a grid system, think of this as setting the margin-top, left, bottom, and right property of the item.

```
.container{
  display:grid;
  grid-template-columns: repeat(3, 1fr);
  grid-template-rows: 1fr 2fr;
  gap: 10px;
}
```
%[https://codepen.io/thesultan00/pen/xxVOBEO]

## Bonus

Let's look at a common code pattern that is going to help our grid system be a lot more responsive.

```
.container{
  display:grid;
  grid-template-columns: repeat(auto-fill, minmax(200px, 1fr));
  grid-template-rows: 1fr 2fr;
  gap: 10px;
}
```
%[https://codepen.io/thesultan00/pen/yLOJrLO]

In the code above, we set the **auto-fill** value and this means the grid items would auto-fill according to the size of the viewport to fill up whatever space is left. Then we set the **minmax** value which specifies the minimum size of the column which is **200px** and the maximum to be **1fr**

## Children Elements(Grid Items) Properties
* grid-column
* grid-row

## Grid-column

**Grid-column** is a grid item property that specifies the position of an item in a grid system on the column axis. **Grid-column** is a short-hand property used for specifying the **grid-column-start** and **grid-column-end** property of an item.

```
.item {
<!-- ...shorthand property... -->

    grid-column: 1 / 4 ;

<!-- ...longhand property... -->
    
   grid-column-start: 1;
   grid-column-end: 3;   
}
```

%[https://codepen.io/thesultan00/pen/poyEPOZ]

Now let's do a quick analysis of what is going on in this example so that we can have a better understanding.

![](https://i.imgur.com/C6E2DI6.png)


When we create a grid system, there are invisible grid lines that are created that we don't see, well technically they are not invisible when you use the chrome developer tools.

In our example,  we set the **grid-column-start** of the items with the **.green** class to **1**. Now notice the green class in the image, it starts at **1** where the first column begins continues to **2** where the second column begins and then **ends** at **3**


## Grid-row

**Grid-row** is a grid item property that determines how an item in a grid system is positioned on the row axis. **Grid-row** is a short-hand property used for specifying the **grid-row-start** and **grid-row-end** property of an item.

```
.item {
<!-- ...shorthand property... -->

    grid-row: 1 / 4 ;

<!-- ...longhand property... -->
    
   grid-row-start: 1;
   grid-row-end: 3;   
}
```

%[https://codepen.io/thesultan00/pen/XWdjaxV]

![](https://i.imgur.com/hRZyBIJ.png)



The above example follows the same principle as the **grid-column**, but this only affects the row axis.


## Conclusion

> "On October 17th, Microsoft’s Edge browser shipped its implementation of CSS Grid. This is a milestone for several reasons. First, it means that all major browsers now support this incredible layout tool. Second, it means that all major browsers rolled out their implementations in a single year(!), a terrific example of standards success and cross-browser collaboration. But third, and perhaps most interestingly, it closes the loop on a process that has been more than 20 years in the making. ~[A LIST APART](https://alistapart.com/article/the-story-of-css-grid-from-its-creators/)"

CSS Grid makes a great, easy, and responsive way to layout a webpage, by specifying simple properties we can make our webpage look beautiful and organized.


This brings me to the end of this article. In this part of the series, we looked at how to layout a webpage, by using the CSS Grid system. In the coming parts of the series, we're going to be looking at other ways we could layout and position elements on a webpage.

## Attributions

* Zero to Mastery Academy