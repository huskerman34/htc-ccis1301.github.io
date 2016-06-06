---
title: Pacific Trails - Part 1
---

<div class="alert alert-danger" role="alert">
  :exclamation: Overall the Pacific Trails Case Study will follow the case study from the textbook, but how we get from beginning to end will be a little different. Please use this assignment sheet to direct your work. The instructions from the end of chapter case studies in the book do not match my assignments.
</div>

## Grading
This assignment is worth 50 points and will be graded as follows:

- All HTML and CSS files are valid - 10 pts (all or nothing)
- Page display/functionality in browser matches wireframes - 5pts each, 10 points total
- Correct HTML5 template elements (html, body, head, meta, title) - 5 pts each, 10 points total
- Correct HTML5 structure elements(header, nav, content div, footer) - 5 pts each, 10 points total
- External Stylesheet is correct - 10 points

## Introduction
We will be working on a business site for the owner of the Pacific Trails Resort located on the coast of Northern California. The owner, would like a website that emphasizes the uniqueness of the location and accommodations. Currently the discussions on website content are in the preliminary stage, but following [agile project principles](http://agilemanifesto.org), we will get to work right away and revise our design and website code iteratively as the project requirements evolve.

We have been given some initial content and style information for the the website, but the requirements team is continuing to work with our client on layout details.  Over the next few sessions, these wireframes will be updated as more design specifics are worked out with our client.

##Site Map and Wireframes
The planned site map:
<img src="{{ "/assets/assignments/cs-pt/sitemap.png" | prepend:site.baseurl }}" title="Pacific Trails site map"
      alt="The site map - a Home Page with sub pages for Yurts, Activities, and Reservations." />

We will begin with the Home page and the Yurts page. The requirements team has been working with the client to create wireframe mock-ups of the proposed site. They are using an online tool called [Moqups](https://moqups.com/) - a tool used to create and share wireframes on the web.

The wireframes will show you the expected content and structure of the web pages. They will be updated for each case study project.  

Current wireframes:
<a target="_blank" href="{{ "/assets/assignments/wireframes/PacificTrailsP1-Wireframes.pdf" | prepend:site.baseurl }}">PacificTrailsP1-Wireframes.pdf</a>

<div class="alert alert-info" role="alert">
You can also copy and paste the web page text from the wireframes so that you don’t have to type it all. This should help you to avoid typos.
</div>

## Task 1 - Setup Project
The starter files for the case study are found in the [ptCaseStudy](https://github.com/htc-ccis1301/ptCaseStudy) repository on GitHub.  Fork this repository, and clone it to your computer to begin working on it.

In the project folder, create two new HTML pages - one for the Home page (index.html) and one for the Yurts page (yurts.html).


## Task 2 - Home Page

###Edit HTML
In this section, we will focus just on the HTML for the home page.  It will not yet look like the wireframe when you are done, as it won't have the CSS for the colors and styling yet. As you write the HTML, use the *Live Preview* feature in Brackets to watch your page take shape.

1. Open the home page (index.html) in the editor and update it with the HTLM 5 template code.

2. Set the title to "Pacific Trails".

3. Update the body to reflect the content shown in the wireframe, adding the HTML5 Structural elements shown by the boxes and call-outs. (This is similar to Hands-On Practice 2.11 on page 47 of your textbook.)  

  - Add the banner using the `<header>` tag with a child `<h1>` tag for the company name.
  - Add the nav using hyperlinks for each page. (For the moment, do not use a `<ul>` for the nav.)  While we do not yet have requirements for the Activities and Reservations pages, you can still code the links. If you like, you can add blank or "under construction" pages for them.
  - Add a div for the main content (`<div id="content">`) to contain the page text shown in the wireframe. The "Enjoy Nature..." heading should be an h2.
  - Put the address information into a `<div>` that is located inside (as a child of) the content div.
  - Add the footer with the text as shown, using your first and last name in the email. Be sure to use an entity for the copyright symbol.  Do NOT just past in the character!


### Test & Validate
Check your page by viewing it in the browser.  At this point, it should look as follows:

<img src="{{ "/assets/assignments/cs-pt/pt1-home-html.png" | prepend:site.baseurl }}" title="Pacific Trails Home Page"
      alt="The current state of the Home page without CSS." />

In the browser, you will not see the boxes representing the HTML5 structural elements, that are shown in the wireframes.  These are only in the wireframes to help you visualize the structure.

However you can use Brackets to see that you have everything in the right place. If you select one of the structural elements, such as the header or nav in Brackets, then in the *Live Preview* a blue box will show the bounds of the element.

<img src="{{ "/assets/assignments/cs-pt/bracketsHtmlStructure.jpg" | prepend: site.baseurl }}"
    title="HTML Structure in Brackets"
    alt="Screen capture showing Live Preview in Brackets with the nav element highlighted." />

Validate the page using the W3C validator.


## Task 3 - Add the CSS

1.  In the project folder, add a new external CSS file called pacific.css.

2. Open your index.html and add a `<link>` tag to configure the external CSS file.

3. Open your CSS file in an editor.

4. The wireframe shows that the default text should have a dark grey color (#666666). Add CSS to configure the text color using the body selector. By using the body selector, all child elements will inherit this configuration for their text.

5. The header is shown with a dark blue (#000033) background and a white text color. Add CSS to configure the background and text colors for the header.

6. View the Home page in the browser to make sure that the CSS and HTML are linked correctly. You should see that the text is dark grey and the header is dark blue with white text.

7. Add CSS for the nav. It is shown with a sky blue background color (#90C7E3).

8. Add CSS to configure the second level heading with a medium blue text color (#3399CC).

9. Check that you are now seeing the blue background on the nav and the blue text for the h2 heading. There will be a space between the header and the nav until we learn to configure margins and padding in a later lesson.
<img src="{{ "/assets/assignments/cs-pt//homeP2_header.jpg" | prepend: site.baseurl }}" title="Pacific Trails Header with CSS Colors" style="width: 300px; height: auto;" alt="The header, nav and h2 with the background and text colors applied." />

10.  This is a good point to validate your CSS file with the W3C validator.

### Add the Resort Style Class
There is a note on the wireframe for the Home page calling out a resort style class for the Pacific Trails company name. Adding this style class will be similar to the Hands-On-Practice 4.5 on pages 116-117 of your textbook.

1. Open the Home page for editing.

2. Find the Pacific Trails company name at the beginning of the first paragraph of text.

3. Add a `<span>` surrounding the "Pacific Trails" company name.

4. Add the `class` attribute to the `<span>` giving it a value of "resort".

5. Repeat these steps where the company name is found in the contact information div.

6. Next we need to update the CSS file. Open it in your editor.

7. Add CSS to change the text color to medium dark blue (#5C7FA3).  Add a rule for the "resort" style class using a style class selector. Remember that style class selectors have a . before the selector name.

### Test & Validate
Check your page by viewing it in the browser.  At this point, it should look as follows:

<img src="{{ "/assets/assignments/cs-pt/pt1-home-css.png" | prepend:site.baseurl }}" title="Pacific Trails Home Page"
      alt="The current state of the Home page without CSS." />
Validate the both the HTML page and the CSS stylesheet using the W3C validators.

## Task 4 - Yurts Page

### Edit HTML

1. Open the yurts.html page in the editor and update it with the HTML 5 template.

2. Change the title to "Pacific Trails :: Yurts".

3. Update the body to reflect the content shown in the wireframes, again adding the HTML 5 Structural elements similar to the home page.

4. For the main content, the questions should be coded as third level headings. The answers that follow should be paragraphs.

5. Open your yurts.html page and add a `<link>` tag to configure your external CSS file.

6. Add CSS to configure the third level heading with the dark blue text color (#000033).


### Test & Validate
Check your page by viewing it in the browser.  At this point, it should look as follows:

<img src="{{ "/assets/assignments/cs-pt/pt1-yurts-css.png" | prepend:site.baseurl }}" title="Pacific Trails Home Page"
      alt="The current state of the Home page without CSS." />
Validate the both the HTML page and the CSS stylesheet using the W3C validators.


## Submit the Assignment
Before you turn your project in:

1. Double check that you have saved all your files and close your editor.

2. Find your project folder in the file system, and open the index.html page in the Chrome browser. Re-check that it matches the wireframe.

3. Click the navigation link to go to the Yurts page. If the link did not work, edit the file to fix it and then re-check the link.

4. Verify the Yurts page matches the wireframe.

5. Click the navigation link to return to the home page. If the link did not work, edit the file to fix it and then re-check the link.

6. Next open the web page in a different browser such as Firefox, Internet Explorer, or Safari. Again re-check that both pages match the display in Chrome and the wireframes.  Note any differences.

7. Use the W3C Validator to re-validate the CSS file and both HTML pages.

When everything looks good, commit and push your files up to GitHub and submit a pull request to have your work graded.  
