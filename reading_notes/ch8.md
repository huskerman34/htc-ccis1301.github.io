---
title:  "Chapter 8: More on Links, Layout & Mobile"
layout: notes
---

## More Links
Chapter 8 begins with more information on hyperlinks.  It's important to understand how relative paths work, as they are very common. With bigger web sites, the files are usually grouped into folders for organization, so when you reference one of those files, you need to include both the folder and file name.  Any link that does not begin with a / or a protocol (like http or ftp) is a relative link.

A common mistake is to forget that the path that you specify is relative to the location of the file that the link is in.  So sometimes you need to go up a folder level to get to the folder you want.  You can use a `..` in the path to indicate that you need to go up a level.  A single dot `.` can be used to indicate the current level, but usually this is just left off.

The following are equivalent:

&nbsp;&nbsp;&nbsp;&nbsp;   ./index.html

AND

&nbsp;&nbsp;&nbsp;&nbsp;   index.html

The next section on Fragment Identifiers shows you how to link to content further down your page.  This is great for information heavy sites like Wikipedia.  Check out the article on [HTML5](https://en.wikipedia.org/wiki/HTML5).  There's a lot of information there, but you can use the links in the Contents block near the top to skip down to the section you are interested in without scrolling.  

Pay attention to the FAQ note at the end of this section. "Why don't some of my hyperlinks to fragment identifiers work?"  The browser will try to position the content you link to at the top of the page, but if there is not enough content below it, then it may be visible on the page, but not at the top.

## Figure and Captions
Check out the examples of adding captions to images, and the example of the image that is framed to look like a [Polaroid](https://en.wikipedia.org/wiki/Instant_film).  This can make a neat effect for images on a website, particularly if it is intended to look like a paper photo album.

## More HTML5 Elements
The additional HTML5 elements for section, article, and aside should be used where they make sense to markup the content in an HTML5 site. Again, Wikipedia is a great example of where articles and sections make sense.  An online book is another great example, but it doesn't have to be that literal.  We looked at some single page sites, where each *page* was something you scrolled to.  It might make sense for each of those *pages* to be a section.  

The aside is commonly used to for *extra* content.  Things that are might be moved or hidden in certain contexts, perhaps a sidebar or part of a sidebar. Something that is related to the main content, but not integral to it.  

There aren't hard rules around the use of these additional elements, but you should try to use them in a way that is intuitive and makes sense for the content they contain.

## Browser Compatibility
One could easily spend an entire course discussing issues around browser compatibility.  The book only touches on some basics, and while I'll point you to a few other resources, we'll leave a lot of ground here untouched.  It's a tricky topic for a class, as each browser has different issues and each version of the browser changes the features it supports.

### CSS Block Display & HTML5 Shim
The two browser compatibility fixes introduced in the textbook are simple snippets you can just add as part of a basic site template.  One snippet goes in your CSS file, the other on each HTML page.

Configure Block CSS:
{% highlight css %}
header, main, nav, footer, figure, figcaption, aside, section, article {
  display: block;
}
{% endhighlight %}

Configure HTML5 Shim:
{% highlight html %}
  <!--[if lt IE 9]>
  <script src="http://html5shim.googlecode.com/svn/trunk/html5.js"> </script>
  <![endif]-->
{% endhighlight %}

### Additional Information
Here are my favorite resources for determining what features are supported in various browsers:

- [Can I Use?](http://caniuse.com/)
- [Quirksmode](http://www.quirksmode.org/compatibility.html)


[Modernizr](http://modernizr.com/) is a JavaScript library that can do feature detection and assist with providing a consistent look across different browsers and versions.

This article on Mashable [Browser Testing Tools](http://mashable.com/2014/02/26/browser-testing-tools/), lists several tools and services for assisting with compatibility testing. It's dated, but is a good starting place to see what options are out there.

## Print CSS
It's great to have a spiffy and eye-catching layout for your web page, but what happens if someone wants to print that information?  There's nothing more frustrating than finding the information you need, like that perfect brownie recipe, and then not being able to print it to take it with you.

If you have information someone may want to print, providing CSS for printing is both thoughtful and environmentally friendly.  By removing unnecessary content and streamlining your layout, you can ensure that the content prints neatly and with as little paper (and ink) wasted as possible.

This probably isn't something that you need to do on every site you make, but if you know that you've got information many people will want on paper, then make those people happy and provide a layout just for printing.

## Mobile Web
The use of media query to choose a specific stylesheet for mobile is one option to have a special site layout for mobile:

{% highlight html %}
<link href="mobile.css" rel="stylesheet" type="text/css" media="only screen and (max-device-width: 480px)" />
{% endhighlight %}

However, the general trend leans more toward using one CSS file that uses media queries (and/or 3rd party libraries like Bootstrap) to customize the experience based on the available display size.  This is the approach we will be taking for the projects created for this course.  

### Mobile First
Since we already have a desktop site for our case study, we will use media queries to alter that view to have it display nicely on a smaller display. This not uncommon in practice as historically most websites were accessed on a computer.

However, with the growing popularity of mobile devices this is increasingly untrue. In fact in many places throughout the world the only way for many people to access the web is by using a mobile device.  Thus, a growing trend in web design is to design for smaller devices first, then later enhancing the layout and design for those who do use larger displays. We will take this approach when designing our portfolio project. 

### CSS Media Queries
We will be using media queries extensively throughout the remainder of the course.  It is very important that you understand both how add them into your CSS and the mechanics of how they work. Their intent is to alter the CSS applied to an element by overriding what was applied before.

Let's look at a simple example that just shows or hides an element based on the display size.  What would happen if the `mobile-only` class were applied to a `div`?

{% highlight css %}
.mobile-only {
    display: none;
}

@media only screen and (max-width: 480px) {

    .mobile-only {
        display: block;
    }
}
{% endhighlight %}

If we apply the `mobile-only` class to a `div` element on our page, that `div` would be hidden when the display width was larger than 480px.  On a display with a width smaller than 480px, that `div` would be visible.  

If you looked at the `div` using the developer tools, on a wide display, you would only see that the `mobile-only` class was hiding the display. If you look at it on a mobile sized display, then you would see that the media query css was altering the behavior of the `mobile-only` class by overriding the display and changing it from none to block.  

Try it out and make sure that you understand how this works.

