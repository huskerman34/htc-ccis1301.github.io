---
title:  "Chapter 4: Cascading Style Sheet Basics"
layout: notes
---

## Overview
To wrap up this session, we're going to learn some basics about CSS.  This section corresponds to Chapter 4 of your textbook.  (We'll return to Chapter 3 later.)  For now, we will learn what CSS does, how it does it, and how to apply and use it to change the text and background color of a web page.  

<div class="alert alert-info" role="alert">
This is a very, <em>very</em>, important chapter.  Don't skim or just glance over any of it.  Pay close attention to how the CSS is used and applied.  
</div>

Just like with HTML5, it is also important to keep in mind that we are learning the latest version of CSS - CSS 3.  While support for this is less of an issue with the *latest* browser versions, it can still cause problems.  You can view support for various CSS 3 features on many websites, including [CanIUse?](http://caniuse.com/#search=CSS3).


## What is CSS
CSS allows us to apply different fonts and font styles, colors, and layout to our web pages. This can cause the exact same HTML markup to be rendered (or displayed) in the browser in many different ways.  This is a very powerful feature!

To see how powerful, let's look at some examples from the [CSS Zen Garden](http://www.csszengarden.com/) website.  All four images below represent the exact same HTML, just with different CSS applied.

<div class="row" style="margin: 15px;">
<div class="col-md-6" style="padding: 5px;">
    <a href="http://www.csszengarden.com/">
    <img src="{{ "/assets/images/s1/basic-css-zengarden-main.png" | prepend:site.baseurl }}"
        alt="A light green watercolor view of the CSS Zen Garden website.">  
    </a>
</div>
<div class="col-md-6" style="padding: 5px;">
<a href="http://www.csszengarden.com/216/">
<img src="{{ "/assets/images/s1/basic-css-zengarden-fk.png" | prepend:site.baseurl }}"
    alt="A light green watercolor view of the CSS Zen Garden website.">  
</a>
</div>
<div class="col-md-6" style="padding: 5px;">
<a href="http://www.csszengarden.com/221/">
<img src="{{ "/assets/images/s1/basic-css-zengarden-midcent.png" | prepend:site.baseurl }}"
    alt="A light green watercolor view of the CSS Zen Garden website.">  
</a>
</div>
<div class="col-md-6" style="padding: 5px;">
<a href="http://www.csszengarden.com/215/">
<img src="{{ "/assets/images/s1/basic-css-zengarden-robot.png" | prepend:site.baseurl }}"
    alt="A light green watercolor view of the CSS Zen Garden website.">  
</a>
</div>
</div>

This illustrates some very dramatic formatting and layout changes that can be applied through the use of CSS.  It is almost unbelievable to think that all of this pages use the exact same HTML! In addition to formatting and layout, CSS also supports gradients, transparencies, animations and transitions.  

You'll get the hang of HTML in no time, but becoming a true master of CSS will take much longer.  There is a lot to learn; so don't let that discourage you.

## The CSS Cascade
The *C* in CSS stands for *Cascading* and that refers to the way that CSS handles multiple styles being applied to the same element. We will experiment with this a bit in our next exercise, but for now, just aim to remember there are rules behind what style or styles are applied to a given HTML element.

The simplest of these rules is based on where the style rules is defined.  There are browser defaults for how everything is displayed.  These rules trickle down the chain, but can be overridden by any or all of the layers that follow. Rules from external stylesheets come next.  They may add to and/or change the default rules, then those also trickle on to the next layer. The same applies to the embedded styles, then the inline styles.

<img src="{{ "/assets/images/s1/basic-css-cascade.png" | prepend:site.baseurl }}"
    alt="Illustration of the CSS Cascade: Browser Defaults, Overridden by External Style Sheet, Overridden by Embedded Styles, Overridden by Inline Styles.">

The rules from each layer add on to what was there from before, but when there are conflicts, then it is important to remember that the last one in wins.  

<div class="well well-sm">
:memo: Understanding this cascading behavior is key to understanding how CSS works.  It will take a lot of practice to get used to.  
</div>

## Style Declaration
A stylesheet is made up of one or more rules, and each rule has two parts - a selector and declaration.  The selector is placed before the curly braces { }, and the declaration is placed inside.  The declaration is make up of one or more property/value pairs.

Some examples:
{% highlight css %}
body {
    background-color: blue;
    color: white;
}

h1 { color: lime; }

div { background-color: lightYellow;  color: red; }
{% endhighlight %}

In the examples above, all of the selectors should be recognizable as HTML tag names.  Selectors can also be class or id selectors.  You can also combine one or more to make a descendant selector.


|  `#content`  |  an ID selector  |  selects the item with the `id="content"`
|  `.myClass`  |  a class selector | selects all elements that have `class="myClass"`
| `#content p` |  a descendant selector | selects all p elements *inside* the element with `id="content"`


## The Span Element
Just like `<div>` tags are used all over the place to identify and style *blocks* of content,  `<span>` tags are used to identify and style *inline* content.

In the simplest terms, a block of content is content that uses the entire width of the browser display with a space or break before and after it. Inline content *flows* in a line, usually a line of text, but it may be a line of images, or buttons, or anything.  

There will only be one block in a row of content, there may be many pieces of inline content in a row and as they overflow one row, they will wrap to the next.


## Validation
The W3C provides an online validation service for CSS similar to the one that it provides for HTML - [W3C CSS Validator](http://jigsaw.w3.org/css-validator/).  Links to both validation sites are included in the Links and Resources in the sidebar.

They work basically the same way, however they are both specific in regards to the type of files that they validate.  The CSS Validator will not validate HTML and likewise the HTML validator will not validate CSS.  This may seem obvious now, but things can get blurry at the end of a long day.  I have reminded people of this numerous times.

Validation errors in your CSS file will also result in points being deducted from your assignment grades.  However, they also tend to result more frequently in the page not appearing correctly, and thus are more often caught before being submitted.  If you are not getting the results that you expect from your CSS, run in through the validator.  It just might save you a lot of trial and error in trying to resolve the problem.
