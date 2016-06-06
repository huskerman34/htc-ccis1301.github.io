---
title: Personal Portfolio - Part 1
name:  portfolio-pt1-v1
---

## Grading
This assignment is worth 50 points and will be graded as follows:

<div class="alert-danger">
Prerequiste: The Hand-drawn or [Moqups](https://moqups.com) wireframe are required to receive _*any*_ credit for any part of this project. No credit will be given until the wireframes have been submitted to the dropbox and any required corrections or updates made.
</div>

- All HTML and CSS files are valid - 10 points (all or nothing)
- Good mobile presentation - 10 points
- HTML5 sections used to for "pages" - 10 points
- Bootstrap Navbar and ScrollSpy used for navigation - 10 points
- Site matches expectations set by wireframes - 10 points

## Introduction
For our last project, we are going to work on a personal portfolio site.  Think of it as your online resume.  You are free to customize the look of the site to suit your own tastes and style, as it is meant to showcase your style and personality.  However, you must include the information required below.  The wireframes you submitted are our _contract_ for this assignment. Any major changes to them should be approved by the instructor, otherwise points may be reduced for deviations.

## Outline the site
For the first part of the assignment, you'll need to outline the main page of the site focusing mainly HTML and using default Bootstrap CSS.  Consider what we did with Ms. B's website.  It looked pretty ho-hum and standard, right up until that last few minutes as we started tweaking the CSS.  Get the HTML foundation in place, use default Bootstrap components, and later work on making the style unique.

Remember not to get caught up in the content itself.  Use [Lorem ipsum](http://www.lipsum.com/) text to avoid getting caught up writing. Use placeholder images, or just a `<div>` with a size, fill and "Image TBD" text is enough for now.  The details can come later.

Fill in and polish the personal details as you have time, and finish that up after the class ends if needed.  You've got a life-time to polish the resume/portfolio, but only a few weeks to complete this final project. I'm grading on page structure and style, the HTML/CSS and use of Bootstrap, not the personal site content.  

## Focus on Mobile
Keep in mind that a goal of this project is to practice Mobile First Design.  When designing and testing your site, start with a small browser display that mimics a phone.  How does your site look?  Is the key information shown?  Can you better tailor that content for the display size?  Keep a minimalist mindset.  You don't want to swipe 20 times to get to the next section.

Once you are satisfied with the mobile view, then you can explore how to enhance that experience for larger display sizes.  Take advantage of the [Bootstrap Grid](http://getbootstrap.com/css/#grid) system for layout and take a look at the default classes Bootstrap provides to [show and hide content](http://getbootstrap.com/css/#helper-classes-show-hide).  

## Landing Page
We've discussed a sectioned scrolling main page for the site, that may link out to other bits of more detailed information. Focus should be on that main landing page, additional pages can be added later. For now, stay focused on the first impression.

### Design
Look on the web for some pages that use this design, paying particular attention to how they communicate their message. Point out your favorite examples in chat to share and discuss with your classmates.  Don't just add links, mention what you like or don't like, and what you learned from the site.  

We've looked at some examples in the past - [Heroku](https://www.heroku.com/) & [Tumblr](https://www.tumblr.com/).  I'll recommend one other site for you to check out as well. [Start Bootstrap](http://startbootstrap.com/), provides Bootstrap based themes and templates, and they are simple enough to explore and learn from.

<div class="alert alert-danger" role="alert">
  :exclamation: As this is an HTML/CSS class, I expect that you will hand craft all the HTML/CSS details for your site.  You must be able to explain on demand how any particular piece of your site functions and is implemented.   <strong>Do not just download and use someone else's theme!</strong>
</div>

### Structure
As you begin working on the HTML, you'll want to use HTML5 `<section>` tags to mark off each "page" of scrolling content.  You might also use the `<header>` tag to specifically markup the first or main section.  Add links to these sections in the Bootstrap [Navbar](http://getbootstrap.com/components/#navbar) at the top, and use the [ScrollSpy](http://getbootstrap.com/javascript/#scrollspy) component to sync the Navbar active link and page scrolling together.


## Test & Validate
Check your page by viewing it in the browser, paying particular attention to the mobile and tablet presentation.  At this point, it should have the overall layout shown by our in-class design mockup.  I expect that you will have outlined all of the sections of the main page.  Adding additional pages is not required for this part of the assignment.

Be sure to test the navigation and scrolling.  If you scroll to a section it should highlight in the Navbar.  Ensure that the navigation - both click and scroll - is just as easy to use on a small device as a large one.

When you are satisfied, make sure to save and validate all of your files.  You should also test your site with other browsers.  Since the intent is for you to use this as a resume/portfolio, we really should address any issues.  


## Submit the Assignment
Before you turn your project in:

1. Double check that you have saved all your files and close your editor.

2. Find your project folder in the file system, and open the index.html page in the Chrome browser. Verify that it looks as expected.

3. Verify your navigation links.  You should be able to use the links or scrolling to access different sections on the main page.

4. Next open the web page in a different browser such as Firefox, Internet Explorer, or Safari. Note any issues you encountered in your dropbox comments, along with resolutions if you fixed the issue.

5. Use the W3C Validator to re-validate the HTML and CSS files.

When everything looks good, commit and push your files up to GitHub and submit a pull request to have your work graded.  
