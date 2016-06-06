---
title:  "Chapter 2: HTML Basics"
layout: notes
---

## Overview
This section covers highlights from the first part of Chapter 2 of your textbook.  These are only highlights, and it is expected that you will fill in the details by reading the material presented in the textbook. Don't skip things just because I don't point them out here.  However, if you are short on time, those are good things to skim.  

I expect that you will work through the hands on practice exercises provided in the textbook. While these are not graded, they will give you practice with the techniques that you will use for the larger case study assignments that are graded.  It is suggested that you make a [GitHub](http://github.com/) repository for these practice exercises, as that will give you practice working both with HTML/CSS and managing your files using Git.

<div class="well well-sm">
:memo: Remember that all of the tags for visible content are placed inside the HTML body.  Tags in the head section are not shown (though the title is used for the name of the browser window or tab) and only provide information *about* the document.
</div>

## HTML Tags

### Headings and Paragraphs
Headings and paragraphs provide structure for the main content of your pages.  The headings provide an outline, and paragraphs provide the details underneath.  The `<h1>` tag is used for the most general heading, followed by the `<h2>`, `<h3>`, etc.  The proper use of headings to outline the structure of your pages supports a good user experience as well as accessibility tools.

It is a common mistake for beginners to choose a heading tag based on it's appearance (size) in the web browser.  *Do not do this!*  Even if you think the `<h1>` tag is too big or don't like the way it looks, use it for your main or top level heading(s).  It is the structure that is important right now, not the appearance.  We will soon learn how to modify the default way that tags are displayed in the browser using CSS.  

When designing web sites, it is often helpful to get some dummy text to put on your page to work on your layout.  Traditionally, *fake* Latin text called lorem ipsum is used for this. The [Lorem ipsum](http://www.lipsum.com/) website will generate various amounts of this text for you to use on your page while you work on the layout.  You can then come back later and replace it with the actual content text.


### Phrase Elements
These tags are used to call attention to special words or phrases. They change the appearance of the text in browser specific ways, but again, that is easy to change and control with CSS.  When using these tags, focus on the meaning or structure over the appearance.  

Another common beginner mistake is to use `<b>` or `<i>` tags with other tags to change the way they are displayed.  For example, perhaps you want your headings to be italicized.  You might do this:

{% highlight html %}
<h2><i>My Heading</i></h2>
{% endhighlight %}

A better choice would be to use CSS to italicize the heading text.  By using CSS, all `<h2>` tags would be italicized the same way, providing a more consistent experience for the visitors to your website.

So when *would* you use the `<i>` tag and *not* CSS?  Exactly in an instance like the previous sentence.  When you want to call attention to specific words or text.
{% highlight html %}
<p>
   So when <i>would</i> you use the &lt;i&gt; tag and <i>not</i> CSS?  
   Exactly in an instance like the previous sentence.  
   When you want to call attention to specific words or text.
</p>
{% endhighlight %}

Notice that in the example above, when I am talking about the `<i>` tag but not wanting to italicize the text I used `&lt;` and `&gt;` around the i instead of the < and >.  These are special entity characters.  We will learn more about them soon.

<div class="well well-sm">
:memo: Technically, for HTML5 with its focus on semantic markup, the &lt;em&gt; or &lt;strong&gt; tag would be a better choice over &lt;i&gt; and &lt;b&gt;.
</div>


### Lists
Lists - both ordered and unordered - are very common on websites.  They are used both for structure and display.  Most web sites have a set of links that serves as the website's main navigation.  This is often not displayed as a bullet-point list, but structurally it *is* a list.  Again, remember that CSS allows us to change the display of HTML tags.  Even if you do not want to see something as a bullet-point or numbered list, if is is structurally a list then you should mark it up using HTML list tags.

A common beginner mistake is to mark up the list items using `<li>` tags, but to forget to put the `<ul>` or `<ol>` tags around them.  It is also easy to forget the closing `</ul>` or `</ol>` tag at the end of the list.  A good practice is to write both the open and close list tags first, then move the cursor back in between them to start writing the list item `<li>` tags.

Description lists are less commonly used on websites, mainly because structurally they are just less common for the content most commonly seen.  While the layout might *look* nice, again remember that your HTML tags should reflect the structure of the content, not how you want it to appear.  If your content is not text and a description or definition, do not use a definition list to mark it up.

### Special entity characters
These special codes are used to insert symbols into your web page.  These are often things that you cannot type (like a &copy; copyright symbol), or a character that you could type but that has a special meaning in HTML markup (like the < character).  

I will expect you to know and use the following in your web pages:

- `&copy`
- `&lt;`
- `&gt;`
- `&amp;`
- `&nbsp;`

Be careful that if you want to use the & character on your page that you remember to use the `&amp;` entity.  It is easy to forget this.

## HTML Validation
As you learned earlier, HTML5 is a W3C standard.  As we write HTML pages, it is important to ensure that they conform to that standard.  Pages that validate against this standard are more likely to display correctly and consistently in different web browsers, providing a better user experience.

<div class="alert alert-danger" role="alert">
:exclamation: This is a skill that you are expected to learn in this class. Significant points will be deducted for validation errors in your assignments.
</div>

To determine if a web page is valid HTML5, we can run it through the online [HTML validator](https://validator.w3.org/) provided by the W3C. Here is an example that shows a validation error.
<img src="{{ "/assets/images/s1/html-validation-error-top.png" | prepend:site.baseurl }}"
    alt="Image showing the W3C HTML Validation page with an error.">

When you have an error, you'll see that at the top of the page, but you must scroll down to see details on what has caused the error.

<img src="{{ "/assets/images/s1/html-validation-error-msg.png" | prepend:site.baseurl }}"
    alt="Image showing the W3C HTML Validation page with an error.">

The error message clearly shows you:

- the line number where the problem was identified
- the error message
- the HTML that it is detecting as wrong

Usually these things will point you to the error, but it is up to you to determine how to fix it.  Here the error is saying we can't have a "Bad value for attribute href on element link: Must be non-empty." If you look at the HTML show below, the tag does include href="".  There is no value for the href attribute.  That seems to be the problem.  Now how do we fix it?

On most web pages we create, we will have stylesheets.  That is why I included it in the template code.  However, right now, we haven't learned about them yet and so for this project we don't have one.  Since we don't need the tag, let's just take it out.  (Leave it in your template, but take it out of the index.html file.)

Once you have made the change and saved the index.html file validate it again. This time, you should see no errors and the page should display green instead of red.

<img src="{{ "/assets/images/s1/html-validation-no-errors.png" | prepend:site.baseurl }}"
    alt="Image showing the W3C HTML Validation page no errors.">

If you made changes to your files, be sure to commit and push those changes to GitHub.

### Validation Tips

- Make sure that it says it is validating as HTML 5. A missing or incorrect doctype will cause it to make incorrect assumptions.
- Correct errors one at a time. Fixing one error often resolves many. Make one change and then save and validate again.
- Let Brackets help you. It will often highlight tag closure errors along the left margin.
- Watch for double tags or partial double tags, where you typed the tag but Brackets also auto-completed it for you.

If you get stuck with a validation error, try asking one of your peers before you ask me for help.  But *DO* ask for help if you are stuck. These errors are very important to fix, even if you think your page looks fine.

Remember that the [Gitter online chat room](https://gitter.im/htc-ccis1301) is a good place to find me when I am available outside of class, and you can post questions even no one is there. Perhaps another student will be able to help out before I can. Also note that if you call out someone specifically, they can be notified of your message and respond when they are available.


## HTML5 and Web Browsers
For this class it is important that you are working with a browser that has good support of HTML5.  I strongly encourage you to work with the latest version of the [Google Chrome](http://www.google.com/chrome/) browser.  It has very high support of new HTML5 features and also has excellent developer tools.  Firefox is a decent fallback, but do not use Internet Explorer or Safari as your main browser for this course. (Feel free to use them as a comparison, but for now do not be overly concerned by differences or problems with their display.)

How can you tell if a browser will support the HTML tags that you want to use?  There are many sites on the internet, such as  [CanIUse?](http://caniuse.com/) that are dedicated to providing this information, as it is a common problem that all web developers face.

 Alongside the information on browser support of these features, it is important to know what browsers and versions are most used.  This information can be quite dynamic, as it also includes browsers used on mobile devices. One site that provides such information is [NetMarketShare](https://www.netmarketshare.com/browser-market-share.aspx?qprid=2&qpcustomd=0)

As you can see this is not a simple issue.  Fortunately there are many tools, libraries, and frameworks available to help us deal with the problems caused by the different levels of support found in various browsers. As we start to learn CSS, we'll address some simple issues, and will follow up on this at the end of the class as we discuss some web frameworks and libraries.  However it is a large issue, and a comprehensive discussion is beyond the scope of this course.


## More HTML Tags
### HTML5 Structural Elements
These tags are used to call attention to special words or phrases. In the previous section we learned to structure the content of our site.  Now we are going to look at the HTML tags to structure the web page itself.  

The HTML5 structural elements `<header>`, `<nav>`, and `<footer>` support a structure that was common across most websites before these tags were created.  At that time, it was common to see `<div>` tags used instead with ids to indicate they represented the page header, navigation, and footer.

We will use these structural tags for the websites that we develop in this course, so having a template or [Gist](https://gist.github.com/) for this code will be helpful.
<code class="gist" data-gist="5785c6e9534e956b79d7" data-gist-file="structuredHTML5.html">
</code>

Note that I've also used comments to highlight each structural area.  You can remove these if you like, but I find that the comments often help these tags to stand out more once you have all of their inner html filled in.  Comments are often shown in editors in a different color from other tags.

<div class="alert alert-warning" role="alert">
:warning: The hands on practice for this section (and likely others too) has you use &lt;b&gt; and &lt;i&gt; tags in ways I've told you not to - strictly for appearance. Keep in mind that it is <em>not</em> the proper way to alter the appearance of these things; it is just the only way that you know right now. Don't make a habit of it.
</div>

### Div Tags
The `<div>` tag is not new to HTML5. It's been around and is used all over the place.  You will commonly see `<div>` tags inside of `<div>` tags inside of `<div>` tags.  Get used to the idea that you can put them pretty much anywhere and use them to group just about anything you want.  

They are often used to apply a particular look (or style) to a set of HTML tags. This is done by adding `id` or `class` attributes onto the div.  We'll talk more about this after we have learned some basic CSS.


### Links
Web pages would probably not be as popular as they are if there wasn't a way to link from page to page and site to site. In fact links or *hyperlinks* are so important they are the *H* in HTML.  

You make a link with the `<a>` or anchor tag.  It is very common for beginners to confuse this with the actual `<link>` tag which has a very different purpose - to *link* the page to a stylesheet or CSS file.  Keep this in mind from the beginning and you'll *anchor* this in your mind forever.

The most important concept around links is getting the path for the `href` attribute correct. If this is not correct, your link won't work and you'll get an error saying the page could not be found.  This is mainly a concern for relative links within your site, though it can apply to external links too.  However you'll usually be able to copy external links, but you have to figure out the path yourself for files in your own site.

Remember that relative links *do not* include http and *do not* start with a / character.  They must contain the full path from the current document to the one that you want to get to.  For small websites that do not use folders, this is simple, just use the file name.  If the other file is in a folder, you must include the folder name as well.  

<div class="alert alert-danger" role="alert">
:exclamation: Pay attention to the text that you use for the actual link - the text inside the open and close &lt;a&gt; tags.  You should not use text like "click here" or "see this". You should use specific descriptive text for what you are linking to or the name of the other page or site.  This supports accessibility and offers a better user experience for everyone.
</div>

Links can also be used to create an email. Trends around this have varied over the years as people have tried many different things to avoid having their email addresses picked up off websites by bots and used for spam.  Unfortunately as quickly as people come up with ways to try and get around this, the spammers find ways to circumvent their efforts, but this is why you will often see things like "Contact me at: mary dot mosman at hennepintech.edu" with no mailto link instead of "Contact me at: <a href="mailto:mary.mosman@hennepintech.edu">mary.mosman@hennepintech.edu</a>".

## HTML Attributes
An attribute is a name/value pair that is placed inside the HTML tag after the tag name.  Common attributes are `id` and `class`, as they can be used on any HTML tag.

{% highlight html %}  
<div id="myId" class="specialStyle">
   Some stuff in the div.  A div can contain text and/or other tags.
</div>
{% endhighlight %}

Notice that the attribute name is followed by an = and the value is in quotes.  It is not required that an attribute has a value, but most of them do.  If you put an id on your tag, it is required for the value to be unique on that particular web page.  (It is OK to reuse it on a different page, but it can only be used once per page.)

There are other attributes that are only used on certain tags, and some HTML tags require certain attributes in order to be valid.  (We'll see an example of this for links in the next section.)  
