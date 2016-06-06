---
title: Pacific Trails - Part 3
name:  case-study-pacific-pt3-v1
---

<div class="alert alert-danger" role="alert">
  :exclamation: Overall the Pacific Trails Case Study will follow the case study from the textbook, but how we get from beginning to end will be a little different. Please use this assignment sheet to direct your work. The instructions from the end of chapter case studies in the book do not match my assignments.
</div>

## Grading
This assignment is worth 50 points and will be graded as follows:

- All HTML & CSS files are valid - 10 pts (all or nothing)
- Activities Page - Image Gallery Display & Behavior - 5 pts
- Older Browser HTML 5 Compatibility - 5 pts
- Desktop display/functionality - 10 points total
- Tablet display/functionality - 10 points total
- Mobile display/functionality - 10 points total

The planned site map:
<img src="{{ "/assets/assignments/cs-pt/sitemap.png" | prepend:site.baseurl }}" title="Pacific Trails site map"
      alt="The site map - a Home Page with sub pages for Yurts, Activities, and Reservations." />


Notice that the wireframes have been updated to show different layouts for desktop, tablet and mobile.
Current wireframes:
<a target="_blank" href="{{ "/assets/assignments/wireframes/PacificTrailsP3-Wireframes-v2.pdf" | prepend:site.baseurl }}">Pacific Trails Wireframes for Part 3</a>

In this part of the case study, we'll be adding an image gallery and a responsive layout to the website.  

## Task 1 - Feedback updates
We've gotten a few feedback items from our customer we need to address before we dive into our new changes.

### Old Browser Compatibility
We ran into some trouble when one of our customers used an older browser to check out our latest release of the website.  We need to provide some fall-back for browsers that don't support HTML5.

First, add the following CSS to the stylesheet.  Recall that these are new HTML5 elements that have block display.  Adding this CSS will cause those elements to have block display in browsers that do not yet support HTML5.  It is a good habit to include this in all of your CSS pages.  

<code class="gist" data-gist="5785c6e9534e956b79d7" data-gist-file="html5.css">
</code>

Next, update the HTML pages to include the HTML5 shim script if the viewer is using a version of IE less than version 9.  Add the following HTML into the `<head>` section of each page.

<code class="gist" data-gist="5785c6e9534e956b79d7" data-gist-file="html5shim.html">
</code>

If you have an [HTML5 template Gist](https://gist.github.com/mbMosman/5785c6e9534e956b79d7#file-structuredhtml5-html), you may want to update it to include this.

### Image &amp; Layout Updates
Our customer would like a larger feature image on the main pages of the site.  This type of image is often referred to as a [hero image](https://en.wikipedia.org/wiki/Hero_image).

The hero image is like a banner image and is separate from the main page content.  Since this image is not vital page content, we will use CSS to add it as a background image.  This allows us the option of later adding text over top of the image, similar to the banner in the header.  Recall that you should not use CSS to add images that convey information, but as this banner image is decorative only, using CSS is fine.

To add the hero images:

1. Remove the existing images from each page.
2. Before the `<main>` tag, add a new `<div>` tag.  The div should have a different id for each page:  homehero (on index.html), yurthero (on yurts.html), and trailhero (on activities.html).
3. Add CSS to the stylesheet to configure the div (using the id values) to have a 300px height, and use the corresponding jpg image from the images folder as the background image.  It should not repeat and be configured to fill the entire space by using the background-size property.


### Nav Improvements
The customer also had some complaints regarding the navigation links.  They would like to have the color change when the mouse is over a link, and they do not like the default link colors.

1. The wireframes now indicate text colors to use for the unvisited, visited, and hover hyperlink states.  Add CSS for these, using the pseudo-classes for the `<a>` tags.   Make sure that this affects *only* those links  that are within the `<nav>`.  

2. Verify the changes to the nav are shown in the browser.  If your links are not displaying correctly, double-check the order of your styles in the CSS.  The order for these is important. (Review the configuration of the hyperlink CSS pseudo-classes in the textbook if needed.)
  <img src="{{ "/assets/assignments/cs-pt/pt3-nav-updates.png" | prepend: site.baseurl }}" alt="Screen capture showing the updated nav fonts." />


## Task 2 - Images Gallery

The image gallery setup for the Activities page is is similar to Hands-On Practice 7.7 on pages 218-219. (In the 3rd edition of the book this is Hands-On Practice 7.8 on pages 236-237.)  

The thumbnail images will be links that will display the larger image in the browser when you click on them.  Hovering over an image should cause a larger image to display in the area to the right of the thumbnails.

#### Set up the HTML
Refer to the Hands-On Practice if you need additional help.

1. Open the Activities page in Brackets.

2. Add a new div with the id "gallery" at the end of the main content.  The gallery div should be *inside* the `<main>` element.

3. Inside the gallery div, add the larger placeholder image (use photo 5) giving it an id of "placeholder". Set the size for the image to be 200 pixels wide by 150 pixels high.  

4. The thumbnail images will be set up inside the gallery div using an unordered list.  Add the list with four list items, one for each thumbnail image. Use images 2, 3, 4 and 6. The thumbnail size should be 100 x 75.  The larger image should be 200 x 150.  The captions for use in the span for each image is provided below:
  - Image 2 - Rocky Coastline
  - Image 3 - Coastal Mountains
  - Image 4 - Turquoise Waters
  - Image 6 - Sunset on the Coast

5. Check the display in the browser to make sure the images display. Don't worry about the layout. It will look messy without the CSS.  For now just make sure all the images are showing.

#### Set up the CSS
Refer to the Hands-On Practice if you need additional help.

1. Open the stylesheet in Brackets.  Use the *Live Preview* feature to watch the layout as you add the CSS.  (You will need to be viewing the activities page when you start the *Live Preview*, then switch to the CSS file.)

2. Set the gallery to use relative positioning and give it a height of 200px.

3. The gallery images are already floated (outside of our list positioning) due to the content image style rule.  Add CSS to override the content image style rule. Set the float to none and the padding to 0 for `<img>` tags within the gallery.

4. Add CSS for the placeholder image (use its id).  Use absolute positioning to place it at top 15px and left 320px.  Set its opacity to .25.  

5. Add CSS so that unordered lists *only* in the gallery have no list marker and a width of 250px. (Enough room for two thumbnail images, with some padding, side by side.)

6. Add CSS so that list items *only* in the gallery display inline, float left and have 10px of padding on all sides.

7. Add CSS to the footer to clear the float.

8. Add CSS to configure links *only in the gallery* to have no underline, dark grey text color, and italic font.

9. We want to hide the `<span>` initially, showing it only when we hover over the thumbnail.  Add CSS to hide span elements *only in the gallery* by setting the display to none.

10. Add a hover rule for links in the gallery so the span will display block, with absolute position top 15px and left 320 px, and have center aligned text. (Refer to the Hands-On Practice if needed.)

11. Check the display in the browser to make sure the images display. Things should look much better with the final CSS added.
  <img src="{{ "/assets/assignments/cs-pt/pt3-image-gallery-v2.png" | prepend: site.baseurl }}" alt="Screen capture of image gallery after CSS.  The thumbnail images are in a 2x2 grid on the left and the placeholder displays on the right." />

### Validate & Test
1. Make sure to save all of your files and close your editor.

2. Validate both the HTML for the activities page and the stylesheet file using the appropriate W3C validator.

3. Open the Activities page in the browser. Be sure to test the hover *and* link behavior of all of the images.  Watch for any strange positioning or display.

Once everything looks good, this would be another good point to commit your changes, and optionally push them to the GitHub repository.


## Task 3 - Desktop Two-Column Layout
Our next task is to configure the CSS for the desktop's two-column layout.  First, we will need to restructure the HTML for the nav to use an unordered list. Then we can configure the remainder of the layout using CSS.

Use the *Live Preview* feature in Brackets to watch the updates as you make them.

### Restructure the nav

1. Open the index.html file. Put the `<nav>` links inside an unordered list, so that each link is inside a list item. Remove any extra spacing.

2. Check the display in the browser.  Without CSS it should look similar to the image below:
  <img src="{{ "/assets/assignments/cs-pt/pt3-2col-nav-no-css-v2.png" | prepend: site.baseurl }}" alt="Screen capture of the nav as a list. The display is vertical and centered and the image bullet list markers display." />

3. Validate the HTML, then copy it onto the other two pages.  Verify the display and link functionality works on all pages.


### Update the CSS

1. Open the stylesheet. Make sure that the CSS to set the marker.gif image for the unordered list bullets is configured *only* for lists that are in the main content. (Use a descendant selector.)

2. Add CSS to remove the bullets for *only* unordered lists in the nav.  Since the links are shifted a bit too far left, set both the padding and margin on the ul elements in the nav to zero.

3. Check the display of the Home page in the browser.  The nav list should show no list marker, but the list in the content should still show the image bullet.

4. Next, remove the CSS to center the nav text, and set the padding to 15px on all sides.

4. Add CSS to float the nav to the left and give it a width of 160px.  We will also give the main content, the hero divs, and the footer a left margin of 190px to *reserve* this space for the floated nav. (Note that the width of 160 + 15 for right padding + 15 for left padding = the 190px reserved space.)

5. Check the display in the browser.  You'll notice that the nav does not fill the entire height of the page.
  <img src="{{ "/assets/assignments/cs-pt/pt3-2col-nav-short-v2.png" | prepend: site.baseurl }}" alt="Screen capture of the nav floated to the left. The background color does not extend the full height of the window." />

6. The window height is determined by the length of the content, but the nav height is determined by the size of the nav list.  Rather than try to force the nav to have the same height as the content, we will pull a little trick and apply the nav background color to the wrapper div.

7. Remove the background color from the nav, and set the sky blue background color on the wrapper div instead.

8. Check the page display in the browser and you'll notice that the whole page is now blue.  That's not what we want either.  Update the CSS to set the background color for the main content and the footer to white.

9. Re-check the page display in the browser.  The blue should now extend the full height of the content.
  <img src="{{ "/assets/assignments/cs-pt/pt3-2col-nav-fullht-v2.png" | prepend: site.baseurl }}" alt="Screen capture of the nav floated to the left. The background color extends the full height of the window." />

10. With the new larger space, the font is appears a bit small now, so update the font size to be 1.2 em.

11. The links also appear a bit squished horizontally, so add a padding of 5px to the list items.
  <img src="{{ "/assets/assignments/cs-pt/pt3-2col-nav-final-v2.png" | prepend: site.baseurl }}" alt="Final screen capture of the nav display for the desktop." />

### Validate & Test
1. Make sure to save all of your files and close your editor.

2. Validate all the HTML pages and the stylesheet file using the appropriate W3C validator.

3. Check *all* of the pages in the browser. Look for any strange positioning or display.

Once everything looks good, this would be another good point to commit your changes, and optionally push them to the GitHub repository.


## Task 4 - Tablet Display

### Add the Tablet Media Query
Look at the updated wireframe showing the tablet display. The tablet display will apply to a window with max-width of 768px.

Open the style sheet for editing. We will add the tablet styles in a media query _*after*_ our existing desktop CSS. Order is important, as we will override and change the existing styles. Add the media query as follows. Make sure to configure all of the tablet CSS that follows inside the curly braces { } for this media query.

{% highlight css %}
@media only screen and (max-width: 768px) {

}
{% endhighlight %}

Let's start with some simple changes to ensure the media query is setup correctly.  Add CSS to remove the float on the nav by setting the float to none. This will override the desktop style that floats the nav to the left.

Save the file and test that your media query is working by opening the home page in the browser and resizing the window so that the width is less than 768px.  When the browser gets small enough, the nav should appear at the top left above the hero image instead of on the left side of the hero image.

If you do not see this happening, re-check your media query.  It must be at the end of the CSS file and the new nav rule should be inside the media query curly braces { }.  Run your CSS through the validator to help identify any errors.

Note that the window may have horizontal scrolling.  That is OK for now, we will be removing that as we continue.

Once you have this working, let's continue updating the tablet CSS.  __Do not continue until you get the above changes to work.__  It won't help to be writing all of the CSS in the wrong place.  

### Add the Tablet CSS
<div class="alert alert-warning" role="alert">
:warning: Note that the following are all overrides of the desktop CSS configured inside of the tablet media query.  Do not change the original desktop styles at the top of the CSS file!  To remove a property that was previously set, change the value to none as we did above with the nav.
</div>

1. Update the body to have 0 margin, no background image, and a white background color.

2. Update the wrapper div to have a min-width of zero and a width of auto. Remove the box-shadow.

3. Update the h1 to have a top margin of 0 to remove the space above the header.

3. Update the nav to set the width to auto, the padding to 0.5em, and center the text.

4. Configure the nav list items to have inline display, top and bottom padding to 0, and right and left padding to 0.75em.

5. Set the main content, the hero image divs, and the footer to have a left margin of 0.  (We just moved the nav back to horizontal along the top, so this is not needed.)


### Validate & Test
1. Make sure to save all of your files and close your editor.

2. Validate the CSS file using the W3C CSS validator.

3. Open the Home page in the browser. Adjust the browser window size to less than 768px in width. The page should look similar to the following, though your text may wrap differently based on width:
<img src="{{ "/assets/assignments/cs-pt/pt3-tablet-final-v2.png" | prepend: site.baseurl }}" alt="Screen capture showing tablet sized home page with no margins on the sides." />

4. Check all of the pages to ensure there are no display problems.

Once everything looks good, this would be another good point to commit your changes, and optionally push them to the GitHub repository.

## Task 5 - Mobile Display

### Add the Mobile Media Query
Look at the updated wireframe showing the mobile display. The mobile display will apply to a window with max-width of 480px.

Open the style sheet for editing. We will add the mobile styles in a media query _*after*_ the tablet CSS. Order is important, as the mobile display builds on the overrides of the tablet display. Add the media query as follows. Make sure to configure all of the mobile CSS that follows inside the curly braces { } for this media query.

{% highlight css %}
@media only screen and (max-width: 480px) {

}
{% endhighlight %}

Add CSS to the media query to set the nav list items to have block display.

Save the file and test that your media query is working by opening the home page in the browser and resizing the window so that the width is less than 480px.  The nav items should display stacked vertically instead of in one line.

If you do not see this happening, re-check your media query.  It must be at the end of the CSS file and the CSS you added should be inside the media query curly braces.  Make sure this media query is not nested inside the curly braces for the tablet query.  Run your CSS through the validator to help identify any errors.

Once you have this working, let's continue updating the mobile CSS. __Do not continue until you get the above changes to work.__   It won't help to be writing all of the CSS in the wrong place.  

### Add the Mobile CSS
<div class="alert alert-warning" role="alert">
:warning: Note that the following are all overrides of the desktop CSS configured inside of the tablet media query.  Do not change the original desktop styles at the top of the CSS file, and be careful not to add the following CSS to the tablet media query by mistake.
</div>

1. Set the main content to have top and bottom padding of 0.1em, left and right padding of 1em, a margin of 0, and font size of 90%.

2. Remove the hero images (unset the background image) and set the height to 0.

3. Update the nav to have no padding and set the font-size to 1em.

4. Update the nav list items to have a margin of 0, padding of 0.3em, and a solid 2px bottom border in dark blue (#330000).

5. Set the nav links (anchors) to block display to provide a larger click area.

6. Reduce the header size by setting the h1 font size to 1.5em.

7. Add CSS to hide the image gallery div.  Because the image gallery no longer displays correctly when the window is less than 550px (a size in between the tablet and mobile sizes), add a new media query to support this.  It should be placed above the mobile media query but below the tablet media query.

### Validate & Test

1. Make sure to save all of your files and close your editor.

2. Validate the CSS file using the W3C CSS validator.

3. Open the Home page in the browser. Adjust the browser window size to less than 480px in width. The page should look similar to the following, though your text may wrap differently based on width:
<img src="{{ "/assets/assignments/cs-pt/pt3-mobile-final-v2.png"  | prepend: site.baseurl }}" alt="Screen capture showing mobile sized home page." />

4. Confirm that you can click anywhere in the bordered nav area for each link, not just on the text itself.  

5. Check the activities page to ensure that the image gallery does not display and that there are no display problems.  Note that the image gallery should disappear and show at 550px.

6. Check the yurts page as well, just to confirm there are no display problems.

### Mobile Only Display Items
On the wireframe, there is a note to update the contact phone number so that it will become a phone link in the mobile display.  We are also to display smaller content images for the mobile display.  To do this we set up new style classes for  the desktop view and the mobile view.

#### Update the HTML

1. Add the images into the HTML for the index, yurts and activities pages as indicated in the wireframes.  Add a style class of "mobile" to the images. Check the display in the browser to ensure the images appear.  Until we add the CSS, they will display at all sizes.

2. Open the index.html page and find the phone number in the contact div.

2. Wrap the phone number with a span that has the style class of "desktop".

3. Below this, add a second span with the style class "mobile".  Inside the span, add a telephone link for the phone number.

<div class="alert alert-warning" role="alert">
:warning: The two spans should be siblings; they should not be nested one inside the other.  We will use CSS to show and hide them so that only one appears at any given time.
</div>

Without the CSS, you should see the phone number twice in the contact information.  Once as text, and once as a phone link.
<img src="{{ "/assets/assignments/cs-pt/pt3-mobile-phone-double.png"  | prepend: site.baseurl }}" alt="Screen capture showing contact information with the phone repeated twice." />

#### Update the CSS
Open the style sheet in Brackets. Use the *Live Preview* feature to show the Home page and watch the updates as you make them.

First we need to add a style rule to the <em>desktop</em> CSS at the top (above the media queries) to hide the mobile span.

- Add CSS to hide the mobile style class by setting the display to none.

Next we need to override that CSS for the mobile display. Scroll down to the mobile media query CSS, and inside the curly braces add:

- CSS to hide the desktop style class
- CSS to show the mobile style class

Finally, setup the mobile image to be responsive by setting the width to 100%.

### Validate & Test

1. Make sure to save all of your files and close your editor.

2. Validate the HTML and CSS file using the appropriate W3C validator.

3. Open the Home page in the browser. Adjust the window size, if needed, to be larger than 768px wide. Confirm that the phone number is only shown once in the contact information.  It should __*not*__ be a link.

4. Adjust the window size, to be smaller than 768px wide. Confirm that the phone number is only shown once in the contact information.  Again, it should not be a link.

5. Adjust the window size to be smaller than 480px wide. Confirm that the phone number is only shown once in the contact information, and that this time it __*is*__ a link.

6. Adjust the window size again to be larger than 480px wide. Confirm that the phone number is once again not a link.


## Submit the Assignment
Before you turn your project in:

1. Double check that you have saved all your files and close your editor.

2. Find your project folder in the file system, and open the index.html page in the Chrome browser. Re-check that it matches the wireframe.

3. Using the navigation links, verify all pages against the wireframes.

4. Next open the web page in a different browser such as Firefox, Internet Explorer, or Safari. Again re-check that all pages match the display in Chrome and the wireframes.  Note any differences.

5. Use the W3C Validator to re-validate the CSS and all HTML pages.  Remember that validation errors are a big loss of points!


When everything looks good, commit and push your files up to GitHub and submit a pull request to have your work graded.  

Also, zip the project folder and upload to the D2L dropbox.


## Wrap-up Topic - The Image Gallery
Why did we just remove it for the smaller view sizes?  Can we not have a mobile image gallery?

To answer this question, look back at how the image gallery was configured.  By using fixed positioning and floats, we are "hard-coding" in a sense a specific size and position that that images in the gallery must be for the display to look the way we intended.  If the images were bigger or smaller, the positioning and size of the elements would need to change to maintain the same look.  The current set up is just not flexible.

To have an image gallery for a mobile sized device we would need to set it up very differently.  While we could recode the absolute positioning for a phone, it would be better to just use a flexible layout instead of a fixed layout.  

Unfortunately, as your layout becomes more complex, writing custom CSS to do this can become increasingly difficult.  Often developers will turn to third-party code and frameworks, such as [Bootstrap](http://getbootstrap.com/) which we will look at later in the course, to assist with this.  [Bootstrap](http://getbootstrap.com/) has a wonderful CSS grid system that allows you to easily configure very complex layouts that are responsive.
