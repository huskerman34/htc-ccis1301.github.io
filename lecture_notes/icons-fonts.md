---
title:  Custom Fonts & Icons
layout: notes
---

# Font Support
In the work we've done so far, we've been limited to the fonts that are already on the users computer or the common web fonts.  You are also able to use custom fonts in your CSS, but you need to also provide the font files for download.  

See this article on CSS-tricks.com for additional information:  [Using @font-face](https://css-tricks.com/snippets/css/using-font-face/)


## Font Awesome
Font Awesome is a set of common icons that you can use on your web page by including their stylesheet.  They provide general application icons as well as icons for various web and social media brands.

To begin working with Font Awesome, check out how to include their files from the [Getting Started ](https://fortawesome.github.io/Font-Awesome/get-started/) page. It is strongly recommended that you reference their files from a CDN.  [Why use a CDN?  Check here.](https://gtmetrix.com/why-use-a-cdn.html)  Since these files are not "yours" and the CDN already exists, you really have no reason not to. It should result in a faster load of your web site.

Then take a look at the [Examples](https://fortawesome.github.io/Font-Awesome/examples/) page to see how to include the icons on your page.  They are added by placing a particular style class on an empty tag, usually and `<i>` or `<span>` tag.

Because these icons are set up as a font, in addition to using their pre-set styles, you can easily alter their size and color the same way you would any other text using the font-size and color properties.  


## Bootstrap Glyphicons
Bootstrap, which is a library we will be looking at more closely next week, also includes some icons which they call [glyphicons](http://getbootstrap.com/components/#glyphicons) that can be used on your website in a similar fashion to those from Font Awesome.  To use these, you will need to include Bootstrap on your page.  See their [Getting Started](http://getbootstrap.com/getting-started/) page for more information.
