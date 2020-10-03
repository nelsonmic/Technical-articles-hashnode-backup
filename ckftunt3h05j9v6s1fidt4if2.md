## CSSOM - CSS Object Model (A brief overview)

Ever so often, we see the abbreviation **DOM (Document object model)** almost everywhere on the internet, and I'm pretty sure I have a 60% chance of winning this bet that this is the first time you're seeing the abbreviation **CSSOM**, or I might be woefully wrong. 

while the **DOM** focuses primarily on HTML elements, the **CSSOM** focuses on the stylesheet. It creates a map of all CSS selectors and their relevant properties. The **CSSOM** is also a tree-like structure.

In this article we're not going to be talking about manipulation in CSSOM, instead, we would be looking at a basic overview of CSSOM, what it is and how it works.

And by the end of this article, you would understand what CSSOM is, how it works, and how it helps in the page rendering process. Great, let's get started.

![](https://media.giphy.com/media/Ln2dAW9oycjgmTpjX9/giphy.gif)

## What is CSSOM 

"The CSS Object Model is a set of APIs allowing the manipulation of CSS from JavaScript. It is much like the DOM, but for the CSS rather than the HTML. It allows users to read and modify the CSS style dynamically."

> [MDN Docs.](https://developer.mozilla.org/en-US/docs/Web/API/CSS_Object_Model)

**CSSOM** and **DOM** are a part of the [critical rendering path](https://varvy.com/pagespeed/critical-render-path.html) which is a series of steps that happens before a website is properly rendered.

## How does CSSOM works?

I assume you already have an understanding of the document object model, if you do not please check this [out](https://developer.mozilla.org/en-US/docs/Web/API/Document_Object_Model/Introduction).

![DOM TREE](https://i.imgur.com/sbYSiTQ.png)

> DOM TREE — image source: [google](https://www.google.com/search?q=what+is+a+dom+node&rlz=1C1CHBD_enNG918NG919&sxsrf=ALeKk00jEhawOXweaUiEcxqlTT9N7WvW7Q:1601651803448&source=lnms&tbm=isch&sa=X&ved=2ahUKEwiPh7H2mZbsAhVxo4sKHTgUA1IQ_AUoAXoECBEQAw&biw=1600&bih=827#imgrc=nGwN3SOwq7YYtM)

The CSSOM creates a map of all the selectors and their relevant style properties, in a tree-like structure as seen below.

![CSSOM MAP](https://i.imgur.com/uWIv1Ai.png)

> Tree Structure of CSSOM — image source: [google](https://www.google.com/search?q=cssom&tbm=isch&ved=2ahUKEwi37N_S5ZbsAhXJt6QKHRtZBE8Q2-cCegQIABAA&oq=cssom&gs_lcp=CgNpbWcQAzIECCMQJzIECCMQJzIECAAQQzIECAAQQzIECAAQQzIECAAQQzICCAAyAggAMgIIADICCAA6CAgAELEDEIMBOgUIABCxA1CCv1ZY89FWYOPVVmgBcAB4AIABpAOIAcwIkgEFMy0yLjGYAQCgAQGqAQtnd3Mtd2l6LWltZ8ABAQ&sclient=img&ei=wZN3X_eHMcnvkgWbspH4BA&bih=827&biw=1600&rlz=1C1CHBD_enNG918NG919#imgrc=tfV92raWe8oEcM)

Then with the appropriate selectors, the CSSOM applies the style rules to the HTML elements.

let me walk you through a series of steps to properly explain this process

1. The browser downloads the HTML for the requested webpage.
2. While processing the HTML, the parser notices a link referencing a stylesheet.
3. The CSS stylesheet is then parsed into a map
4. The mapped results are applied to the HTML elements in the DOM

> **NOTE:**  The CSSOM must be fully loaded before the web page will be displayed.

## Conclusion

CSSOM is a very viable topic for web developers to understand, perhaps it is not so crucial but it is worth paying attention to, it is important for developers to understand what happens behind the scenes sometimes.

I hope this article was really helpful, here we focused on just an overview of the CSS object model, I wrote a list of resources below to help give you a deep dive into the topic, you could check those out. Have a good one :-)

## Resources
This article covers just a brief overview of the CSS object model, here are some other resources to aims to teach you how to manipulate the CSSOM.

* [An Introduction and Guide to the CSS Object Model (CSSOM)](https://css-tricks.com/an-introduction-and-guide-to-the-css-object-model-cssom/)
* [CSS Object Model (CSSOM)](https://developer.mozilla.org/en-US/docs/Web/API/CSS_Object_Model)

Like this article? Follow [@D_kingnelson](https://twitter.com/D_kingnelson) on Twitter.


