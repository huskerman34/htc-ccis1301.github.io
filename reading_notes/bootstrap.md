---
title: Bootstrap Introduction
---

## Introduction
[Bootstrap](http://getbootstrap.com/) (a.k.a. Twitter Bootstrap) is currently one of the most popular front end web framework libraries. It is a collection of commonly used, responsive CSS and JavaScript components that can be easily incorporated into any website.  This allows you to create a stylish new website quickly and easily.

The main resource for learning to work with Bootstrap is their website documentation.  You should read through the [Getting Started](http://getbootstrap.com/getting-started/) page and look at the [Example Pages](http://getbootstrap.com/getting-started/#examples).

We will use the Bootstrap [CSS](http://getbootstrap.com/css/), [Standard Components](http://getbootstrap.com/components/), and [JavaScript Components](http://getbootstrap.com/javascript/) for our projects.  A brief intro to some of them follows, but you will need to use the website as your main reference.  This will give you practical experience learning to work with a new web framework, an important job skill.


## Get Bootstrap
To get started, you need to get the Bootstrap files into your website.  The [Bootstrap Getting Started](http://getbootstrap.com/getting-started/) page provides several options on how to do this.  One of the easiest options is to use a CDN.  For our projects, we'll use these CDN links. This is a great option if you are not doing a lot of customization to the standard configuration.  By using a CDN, the files needed may already be cached in the users browser from a previous site, which means they don't need to download the files again to view your site.

## Basic Template & Examples
Scroll down the getting started page and note the basic template that is provided.  This might make a great Gist for your collection on GitHub.  (For mine, I've filled in the CDN information into the `<link>` and `<script>` tags.) This is a great starting point for a new website.

Looking at the template, you might note that it is an HTML5 document, and that it includes some basic setup for you.

- meta tags for the charset and viewport
- [HTML5 Shim](https://github.com/afarkas/html5shiv) & [Respond.js](https://github.com/scottjehl/Respond)
- [jQuery](https://jquery.com/) which is needed for the Bootstrap JavaScript components
- setup for the [minified](https://en.wikipedia.org/wiki/Minification_(programming)) Bootstrap CSS and JavaScript files

If you continue past the template, there are several basic example pages using Bootstrap for layout.  Take a look at some of these by clicking on the images/links to open the page in the browser and then viewing the page source and/or using the developer tools to inspect elements.  With the example page open, resize the browser window to the see how the responsive layout is adjusted.

We'll be looking at this in more detail through the rest of this session, so you don't need to try and figure everything out.  Just explore a bit just to see what the framework can do.

## Bootstrap CSS
Most of what Bootstrap provides is a responsive, mobile first CSS framework to use when building your site.  The [Bootstrap CSS](http://getbootstrap.com/css/) page introduces this CSS infrastructure and its dependencies. Read through the Overview section for an introduction.  (We'll get into the Grid more after we setup our new site.)

For most of Bootstrap to work properly, you need to first have a Container.  They offer two choices, a responsive, fixed width `container`  or a fluid - full display width `container-fluid`.  Both are *responsive*, but they respond in different ways.  The fixed width container is not required to fill the entire display, it can get a width (like what we did with the content div in the previous case study) and can then be centered.  The fluid container will always fill the entire display.

Regardless of the option you choose, the container is generally setup as a div with the appropriate style class: `<div class="container">` or `<div class="container-fluid">`.  However, you should note that it is not required that you use a div element.  You could use a section, or any other appropriate HTML element, as a container.

<div class="alert alert-warning" role="alert">
:warning: You can have more than one container on a page, but it is suggested that you should not nest one inside of another.
</div>
