---
title:  "Chapter 1: Internet & Web Basics"
layout: notes
---

## Background Information
We're not going to spend a lot of time on background, but there are a few things that you should be aware of as you begin your journey into web development.  Highlights can be found here.  You will find more details in Chapter 1 of your textbook.

### What is the W3C?
The [World Wide Web Consortium (W3C)](http://www.w3c.org) is a group that prototypes technology and recommends standards for the Web. They address topics such as web architecture, specifications for HTML and CSS, and guidelines for design and accessibility.  It is important to keep in mind however that these are recommendations and may or may not be followed by everyone in the same way.  

The biggest area where that this affects us is in regards to HTML and CSS support in web browsers.  The HTML5 specification has been available as a public draft since 2008, and was made an official recommendation in October of 2014.  However support for it in web browsers varies widely. ([Can I Use? HTML5](http://caniuse.com/#cats=HTML5)) It is easy to think "This is the standard, so I should use it!", but with web development we want to aim for the standard while still providing a good experience for our customers who may have old browsers.

### How does the web work?
<iframe width="560" height="315" src="https://www.youtube.com/embed/i8TTdaEkBiw" frameborder="0" allowfullscreen></iframe>

### Protocols
There are several key protocols (or communication rules) that support how the internet works.  You should be aware of these and know how they are relevant to the internet and web.

- TCP/IP (Transmissing Control Protocol / Internet Protocol) - the official communication protocol of the internet
- HTTP (Hypertext Transfer Protocol) - used by web browsers, supports requesting and sending files over the web
- FTP (File Transfer Protocol) - moving files from one place to another; often used for downloads
- SMTP (Simple Mail transfer Protocol) - sending email
- POP (Post Office Protocol) and IMAP (Internet Mail Access Protocol) - receiving email

### Web Addresses
One way to get to a web site is to enter its URL (Uniform Resource Locator) into the address bar on your web browser.  A URL is made up of several parts.

- The protocol - generally this will be HTTP or HTTPS
- The domain name or IP
- The path to the requested file on that server
- The file name requested

<img src="{{ "/assets/images/s1/web-standards-url.png" | prepend:site.baseurl }}"
    alt="Image illustrating the parts of a URL for this site
         (http://htc-ccis1301.github.io/htc-html/sessions/session1-class-v1.html.  
         The protocol is http; the domain name is htc-ccis1301.github.io;
         the path is /htc-html/sessions/; the file requested is session1-class-v1.html">

As we build links to tie our web pages to other pages on our own site and other sites, it is important to understand what a URL is referring to.

### Request / Response
It's important to remember that your web browser is a *client* getting resources from a remote web *server*.  They communicate through a request/response cycle.  The browser makes a request for a web page or resource, and the server responds with that content.  This request/response cycle (and the number of times that it needs to occur to load your page) has performance implications for web pages that you build.


## Accessibility
As we learn to build web sites, we will call attention to accessibility guidelines and best practices.  In 1996 the Department of Justice ruled that the ADA (Americans with Disabilities Act) also applies to the web, and this was followed up in 1998 with an amendment to Section 508 of the Federal Rehabilitation Act which requires the government to give those with disabilities access to electronic information that is comparable to the access available to others. Not surprisingly, the W3C is also very involved with accessibility on the web. Their Web Accessibility Initiative (WAI) provides guidelines for both web content developers and web browser developers to facilitate access to web resources for those with disabilities.  

## HTML Introduction
We often talk about HTML as code, but writing HTML and CSS is different from *programming*. HTML is a markup language, meaning that it *marks up* or adds structure to text content. CSS tells a web browser how it should display that marked up content, but neither involve any programming logic.  While many web developers are programmers and also write JavaScript for their websites (JavaScript is a programming language), there are some who do not and focus more on web design, marketing, and user experience.

This course will teach you HTML5 and CSS3.  As you work through this material, it is important to keep in mind that different browsers and different operating systems may display the same web page differently.  Both the web browser itself and the version that is installed make a difference.  On top of that, even in the same version of the same browser, the page may look different due to the operating system.  While we will only skim the surface of handling these issues, it is very important to remember this while you develop web pages.  

It is also important to keep in mind that we are learning the latest version of HTML and CSS.  While support for this is currently good in the *latest* version of Chrome and Firefox, Internet Explorer lags a bit behind.  For earlier versions of all browsers, support might not be as strong or it may not be there at all.

### HTML5 Template
The core structure of an HTML page is always the same.  You will always begin with the `<!DOCTYPE>` tag. The content of this tag is different based on the version of HTML that you are writing.  This will always be followed by the `<html>` tag.  All of your page's HTML is included between the opening `<html>` and closing `<\html>` tags.  Notice that the closing tag has a \ before the tag name.

Inside the `<html>` tags, you will always have a `<head>` and `<body>` tag.  The content of the `<head>` tag is not shown in the browser display area.  It contains information *about* the page - things like the title, the stylesheet or CSS to apply, and `meta` information.  The contents of the `<body>` tag are what is shown in web browser display area.

<code class="gist" data-gist="5785c6e9534e956b79d7" data-gist-file="basicHTML5.html">
</code>

<div class="well well-sm">
:memo: Note that you can view and bookmark the above template on GitHub by clicking the link at the bottom of the <em>Gist</em>.  (I suggest that if you do that you open it in a new tab or window.)  When looking at it while logged into GitHub, <em>star</em> the gist to bookmark it or <em>fork</em> the gist if you want to be able to alter it.  Gists are snippets of code you want to keep handy.  You can create you own from the + button next to your profile in the upper right.
</div>

### Nesting of Tags
It is important to understand the structure of HTML is a tree or branching hierarchy - much like a folder structure.  The `<html>` tag is the root of this structure.  Looking at our template it has two children - `<head>` and `<body>`.  These children are between (or inside) the opening and closing tags. You could also say they are *wrapped* (or surrounded) by the `<html>` tag.

Using the Chrome Browser Developer tools, we can view the structure of the HTML similar the the way you might see a file tree shown on your computer.  
<img src="{{ "/assets/images/s1/basic-html-tree1.png" | prepend:site.baseurl }}"
    alt="Image illustrating the tree structure of the template above. The html tag contains the head and body.">

By clicking the arrow next to a tag name, you can see what is inside of it.
<img src="{{ "/assets/images/s1/basic-html-tree2.png" | prepend:site.baseurl }}"
    alt="Image illustrating the tree structure of the template above. The html tag contains the head and body.">
