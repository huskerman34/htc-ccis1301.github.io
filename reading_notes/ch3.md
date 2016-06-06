---
title:  "Chapter 3: Web Design Basics"
layout: notes
---

# Web Design Basics
These notes include some highlights from Chapter 3.  Please read through Chapter 3, then come back and review the key information highlighted in these notes as well.

## Design Principles
This is a high-level overview of the key principles that I expect you will recognize and understand from Chapter 3 of your textbook.  

### Target Audience
What works for one site, may not work for another.  The reason behind that is often that the target audience and/or purpose of the site are different.  A site geared towards children is likely to be more colorful and bright, while one focused on adults is likely to be a bit more monochrome and subdued. An information heavy site like wikipedia will focus more on text, while a site advertising a movie is going to focus more on media, graphics and sound.

Understanding the target audience and purpose also leads to some technical considerations.  If you compare your average computer across age groups and demographics, the device they use (home computer, tablet, phone), the size of their display, web browser, and the version of that browser will vary.  I am fairly certain that they have never looked at a website on their phone. For that matter, I'm not even sure they have a phone that views websites...  My 3 and 5 year old nieces on the other hand are already quite adept at using their parents mobile phone apps.  As an IT professional, I wonder how I'd function without two big widescreen displays, while my father-in-law is more than content with his old square 15 inch monitor.

Keep in mind that a discussion on target audience can have wide-ranging implications.

### Organization & Presentation
Web site maps generally fall into two groups, hierarchical and linear.  Larger websites - like an online storefront - may incorporate both.  (Products are hierarchical, while checkout is linear.)  Rare sites are set up more randomly, but these are generally not commercial sites and may be more focused on exploration and discovery - perhaps through a social network, game or story telling.

A web site's organization has a huge affect on usability.  There is a generally accepted *3-click* rule that says you shouldn't have to click more than 3 times to get to what you want. Likewise, they say that your average person can only keep about 3 or 4 items or chunks of information in memory at a time.  Keep in mind the 4 principles of visual design - proximity, contrast, repetition, and alignment.  

### Colors
A colorful site might jump out at you, but imagine if [Wikipedia](https://en.wikipedia.org/) were as colorful as [Nickelodeon](http://www.nick.com/).  Again, color should tie to purpose and your target audience, but there are technical aspects to color as well.

Computers generate color as a combination of red, green, and blue in various intensities.  There are a few different ways to express this, but most commonly you will see hexadecimal, or "hex", color specification. (We'll look at more options for specifying colors in Chapter 6.)  These hex color codes begin with a # and consist of 3 pairs of values from 00 to FF.  They only contain digits and the letters A-F.  

Choosing colors with sufficient contrast is important for usability.  Your should also ensure that your site information can be clearly conveyed to those who cannot see the colors clearly or cannot see them at all.  Pay particular attention to this with things like alert boxes or panels where you may easily assume the color of the panel - green is OK, yellow is caution, red is warning - conveys a special meaning.

Finally, colors can be used artistically to set the tone and mood of your site, but some color combinations work better together than others.  A full study of color and design is outside the scope of this course, but you can learn more about it through sites like [Colors on the Web](http://www.colorsontheweb.com/), and see some color design principles applied through websites like [Paletton - the Color Scheme Designer](http://paletton.com/).

### Text and Multimedia
Keep text on the web to the minimum needed to communicate the idea, concept or information needed by the site.  When using larger amounts of text, use an easy to read, sans-serif, font such as Arial and keep the line length to around 50-80 characters per line.  Left-align paragraphs of text.  Center-alignment can make image captions, headings or small bits of text (1-3 lines) stand out, but it is hard to read large amounts of text formatted this way.  

Use multimedia - images, sound, and video - judiciously.  Don't add things just because you can.  Ensure they are relevant, important, and add benefit to your site.  Ensure that any meaning is communicated in other ways - a text script for a video, alternate text for images and sound files.  Even for those who are not prevented from seeing or hearing these things due to disabilities, providing alternatives is friendly to those on mobile devices as well as those in a quiet setting.

And __*please*__ don't have any website you make just randomly start blaring music or videos.  This is one area that it is safer to "opt-in" versus having to figure out how to stop the sound when you don't want it. This is particularly true for business or informational sites.  The quickest way to not have me come to buy your product or visit your restaurant is to have it start playing music when I sneak a peek at work!

We will talk more about images and multimedia in later chapters as well.


### Above the Fold
The term *above the fold* comes from newspapers, where what you see "above the fold" is what will sell the paper, or catch your eye as you look at a stack of papers.  The concept though is just as applicable to the web.  If you have a lot of content, what the visitor sees when they first land on your page is important.  It *sells* them on staying on your site.  You should ensure that a site's key information is visible on the page without the need to scroll down to find it.  

A common site design today uses scrolling to have different *pages* all on one page.  A welcome with key information is visible when you land on the site, and as you scroll down the page, you are presented with screen size *chunks* of information.  In some cases this is done with the scrollbar visible, and you just see nicely framed content that matches your page size.  In other examples, the content of the page itself changes with scrolling (this requires JavaScript), and the content appears to flip, just like turning a page in a book.


#### Example 1 - The home page for [Heroku](https://www.heroku.com/)

This site has typical navigation along the top, but the layout of the homepage frames each section to be visually separate as you scroll down the page.

  <img src="{{ "/assets/images/ch3/design-heroku1.png" | prepend: site.baseurl }}" alt="Screen capture of the Tumblr welcome page." />

Scrolling down makes me think of *streaming* content.  It flows from one section to the next, often aided with small animations.

  <img src="{{ "/assets/images/ch3/design-heroku3.png" | prepend: site.baseurl }}" alt="Screen capture of the third section of the Heroku page, obtained by scrolling further down." />



#### Example 2 - The welcome page for [Tumblr](https://www.tumblr.com/)

Notice the typical banner and navigation are missing from the top of the page.

  <img src="{{ "/assets/images/ch3/design-tumblr1.png" | prepend: site.baseurl }}" alt="Screen capture of the Tumblr welcome page." />

Scrolling down is like flipping a page.  Notice the dots down the left side that indicate where you are, and can be clicked to move forward and back.  

  <img src="{{ "/assets/images/ch3/design-tumblr2.png" | prepend: site.baseurl }}" alt="Screen capture of the next Tumblr page, obtained by scrolling down." />


### Mobile & Responsive Design
There are a few different approaches to addressing mobile design.  Initially, sites provided a separate mobile site that was hosted at a different URL. Those accessing the site on a mobile device were redirected to the mobile site. While this approach allows a very tailored mobile view, it also involves a lot of overhead to create and maintain two separate versions of your web site.

Today a website that is *responsive* to your display is a much more common trend.  It allows you to main a single version of your site while at the same time allowing you to provide a tailored experience for the viewer.  Creating a site like this requires a different design and implementation approach, and perhaps even more work up front, but is easier to maintain and support going forward.  

Key considerations for mobile include:

- bandwidth and load time
- page layout due to the smaller view area
- touch controls and click area
- color, text, and contrast may vary significantly by device

Mobile designs tend to feature a single column layout, and limit or hide non-essential information, graphics, and media.  

It is also important to remember that responsive design addresses more than just mobile phones.  It also addresses tablet which come in various sizes and may be rotated for portrait or landscape view, as well as older square monitors and super big widescreen displays.  A responsive website will look different - but good - on all of these devices.


## Design Best Practices
There is a web design best practices checklist in your textbook.  In the 2nd edition, it is pages 94-95, and in the 3rd edition, it is pages 102-103.  This is a handy checklist to review as you are working on a site's design.  It is also nice to use to evaluate your site are working on it.  

## Web Resources
There are also many resources on the web that are very handy.  I've included many of them in the class web site side bar.

- [Lorem ipsum](http://www.lipsum.com/)
- [Paletton Color Designer](http://paletton.com/)
- [Font Awesome Icons](http://fortawesome.github.io/Font-Awesome/icons/)
- [CSS Font Stack](http://www.cssfontstack.com/)
- [Icomoon](https://icomoon.io/)
- [Brackets Editor](http://brackets.io/)
