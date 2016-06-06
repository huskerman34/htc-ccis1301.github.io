---
title: Pacific Trails - Part 2
---

<div class="alert alert-danger" role="alert">
  :exclamation: Overall the Pacific Trails Case Study will follow the case study from the textbook, but how we get from beginning to end will be a little different. Please use this assignment sheet to direct your work. The instructions from the end of chapter case studies in the book do not match my assignments.
</div>

## Grading
This assignment is worth 50 points and will be graded as follows:

- All HTML & CSS files are valid - 10 pts (all or nothing)
- Correct HTML5 template and structure elements - 5 pts each, 15 points total
- Page display/functionality in browser matches wireframes - 5pts each, 15 points total
- External Stylesheet is correct - 10 pts

The planned site map:
<img src="{{ "/assets/assignments/cs-pt/sitemap.png" | prepend:site.baseurl }}" title="Pacific Trails site map"
      alt="The site map - a Home Page with sub pages for Yurts, Activities, and Reservations." />


Current wireframes:
<a target="_blank" href="{{ "/assets/assignments/wireframes/PacificTrailsP2-Wireframes.pdf" | prepend:site.baseurl }}">PacificTrailsP2-Wireframes.pdf</a>

## Task 1 - Add Activities Page

### Edit HTML

1. In the project folder, add a new HTML page for Activities (activities.html).

2. Since the layout of the Activities page is very similar to the Yurts page, start by copying and pasting the HTML from the yurts.html file into the activities.html file.

3. Edit the content of the Activities page to reflect the content shown in the wireframes, ignoring the image for now. Be sure to edit the page title as well as body content.

### Validate & Test
Validate the page using the W3C validator. Check your page by viewing it in the browser and comparing it to the wireframes.


## Task 2 - Add Images

### Explore the images folder
To keep web projects neat and orderly, images are typically placed in a folder to keep them separate from the html pages. This is just for file system organization, as web sites typically have many images. Sometimes however, there are also practical reasons, such as hosting images that change infrequently separately from HTML content that may change more often.

For this assignment we will be using the following images.

- marker.gif
- sunset.jpg
- coast.jpg
- yurt.jpg
- trail.jpg

When adding the images to your HTML pages, you will need to know the dimensions of the image. To determine the dimensions (height and width) of an image, find the image in the file system. If you are on Windows, right-click on the file and select Properties, then click on the Details tab. On a Mac, right-click on the file and select the Get Info option.

### Add the Content Images
The large images in the content area of each of the web pages will be added using HTML `<img>` tags. The image element is covered in Chapter 5 of your textbook.

1. Open the Home page for editing.

2. Add an `<img>` tag for the coast.jpg. Add the `alt` attribute with good descriptive text for the image. Don't just use the image name. Set the height and width properties based on the actual image file size.

3. Open the home page in the browser and verify the display of the image. If you are not seeing the image, double check the path on the `src` attribute of the `<img>` tag. This path should be relative from the HTML file location, so it will need to include the folder name.

4. Once the image displays properly on the Home page, validate the Home page using the W3C validator. Remember that even though a page displays properly, the actual HTML may not be valid.

5. Repeat these steps to add the images to the Yurts and Activities pages.

6. Open each page in the browser (use the nav links to go from page to page) to be sure that the images are showing.

7. Validate the Yurts and Activities page to double-check that there are no errors.


### Add the Header Image
Decorative images, such as the sunset in the header, can be configured using CSS. Configuring these images in the CSS allows them to be modified as part of the *theme*, or visual style, of the page.

Notice that the sunset.jpg has coloration that blends it into the background color of the header. If the background color were to change, then the image would need to be edited as well to achieve the same effect. Configuring this image alongside the other header styles in the CSS can be a reminder of this.

1. Open the style sheet for editing.

2. Locate the existing style rule for the header.

3. Add the property for the background image. Set it to not repeat, and position it on the right.

4. Verify the display of the header image by viewing a page in the browser. If you are not seeing the image, double check the url. (Remember it is a relative url. Did you include the folder name?)


### Add the Image Bullets
Images for list bullets are also decorative images, and are configured using CSS. Changing list markers to use images is covered in your textbook on page 145.</p>

1. Open the style sheet for editing.

2. Add a new rule to select *only* the `<ul>` tags that are in the content div, and set the list-style-image to use the marker.gif file.

3. Open the Home page in the browser and verify the display of the new list bullet images. If you are not seeing the image, double check the url. (Again, remember it is a relative url.)


### Validate & Test

1. Make sure to save all of your files and close your editor.

2. Validate all of your HTML pages and the external CSS file using the appropriate W3C validator.

3. Open the Home page in the browser.

4. Check each of the pages, carefully comparing it to the wireframes.

5. Use the links to navigate between pages to ensure they are not broken.

Once everything looks good, this would be a good point to commit your changes, and optionally push them to the GitHub repository.


## Task 3 - CSS for Text Styling

### Add CSS for fonts
The wireframes indicate several notes on text styling.  We will use <a href="http://www.cssfontstack.com/" target="_blank">CSS Font Stack</a> to assist us with creating the appropriate font families.

1. Open the style sheet for editing.

2. Locate the existing style declaration for the `<body>` tag. We will configure the default font here, along with the default color we set up in the previous assignment.

3. Use <a href="http://www.cssfontstack.com/" target="_blank">CSS Font Stack</a> to get an appropriate list of fall-back fonts to use for Arial.  You can click the icon to have CSS for the font family copied to your clipboard so that you can paste the font family CSS into the existing body rule it into the CSS file.
  <img src="{{ "/assets/assignments/cs-pt/pt2-usingCssFontStack.jpg" | prepend: site.baseurl }}" alt="Screen capture showing how to use CSS font stack." />

4. Verify the change to the font shows in the browser. Note that Arial is a sans-serif font and does not have the serifs (or marks) on the tips of the letters.
  <img src="{{ "/assets/assignments/cs-pt/pt2-defaultFont.png" | prepend: site.baseurl }}" alt="Screen capture showing the sans-serif default font." />

5. Next we will add the CSS for the heading fonts.  Locate the existing style declarations for the `<h2>` and `<h3>` tags.  You will need to add one for the `<h1>`. Use <a href="http://www.cssfontstack.com/" target="_blank">CSS Font Stack</a> to get an appropriate list of fall-back fonts to use for Georgia and update all three heading declarations to use these fonts.

6. Verify the change to the heading fonts is shown in the browser.
  <img src="{{ "/assets/assignments/cs-pt/pt2-headingFont.png" | prepend: site.baseurl }}" alt="Screen capture showing the serif heading font." />

7. Next, locate the declaration for the `<nav>` tag.  Add CSS to style the text bold.

8. The links are not underlined in the new wireframes, so we should add CSS to remove the underline *only* for those hyperlinks that are within the `<nav>`.

9. The contact information should be smaller, 90%.  In the HTML, make sure you have an an id of "contact" on the div surrounding the address information. In the CSS file, add a style rule using that ID to reduce the font size *only* for the contact information.  

10. The footer information should also be smaller, 75%.  It should also be italic and should use the Georgia/serif fonts, similar to the headings.  Update the CSS file, then verify the reduced font size and updated styling of the footer information in the browser.

11. We got some feedback from the customer that the resort style on the company name is hard to see. Update the CSS for the resort style class to make the font bold, then verify the company name has a bold font when displayed in the browser.

12. There is also a note to apply text shadow to the second level heading.  Locate the `<h2>` style rules and add a 1px text shadow using the dk grey color from the wireframe palette.

#### Validate & Test

1. Make sure to save all of your files and close your editor.

2. Validate the HTML for the home page and the external CSS file using the appropriate W3C validator.

3. Open the Home page in the browser. Double check all of the items in the font styling note from the wireframes.

4. Check each of the other pages carefully, using the links to navigate between pages.  Pay attention to the h3 styling as there is not an h3 on the home page.

Once everything looks good, this would be another good point to commit your changes, and optionally push them to the GitHub repository.

## Task 4 - Adjust the Layout & Spacing

### Center the Content
Next we will add a new 'wrapper' to allow us to center the content in the browser.  Then we will add a background image to the body area.  This will frame the content better and help it stand out on the page.

1. Open all of your HTML pages for editing.

2. Add a new `<div>` tag with an id of "wrapper" that will *wrap*, or include, everything in the body - the header, nav, content div, and footer.  The open tag will follow the open `<body>` tag, and the close tag will come just before the close `</body>` tag.

4. Open the CSS file and locate the existing style rule for the body.  Add a rule to set the background image to the `ptrbackground.jpg`.

5. Add a new rule for the wrapper div that will set the background color to white, set the width to 80% and the minimum width to 960px.

6. The wrapper should also be centered in the browser window.  Configure the margins on the wrapper div to do this.  

7. There is also a note for box shadow.  No specifics are given, so we'll just aim for a pretty standard configuration of about 5px and use the dark blue color from the wireframe color palette.

### Validate & Test
Validate the HTML & CSS using the W3C validator. Check your page by viewing it in the browser.  It should look similar to the image below.  <img src="{{ "/assets/assignments/cs-pt/pt2-wrapper.png" | prepend: site.baseurl }}" alt="Screen capture of Home page with centered content." />


### Fix the Spacing
While our page is looking good, things are a bit squished, and we still have that gap between the header and the nav.  We'll fix this up by configuring margins and padding.

1. Open the CSS file in Brackets. Use the *Live Preview* feature to watch the changes as you make them.

2. Let's start by removing the ugly gap.  If you examine the header element using the browser dev tools, you can see that there is a large bottom margin on the h1 element.
<img src="{{ "/assets/assignments/cs-pt/pt2-headerGapDevTool.jpg" | prepend: site.baseurl }}" alt="Screen capture of Chrome Dev Tools showing the h1 box model and the large margin configured." /> To remove the gap, edit the CSS to set the bottom margin on the `<h1>` to 0.

3. Update the `<h1>` style to add 10px of padding on all sides.  This makes the heading look less squished.

4. The content is also squished, particularly along the left side. Configure the padding on the content div to add 1 px of padding to the top, and 20px of padding on all other sides.

4. Update the styles for the nav to add 20px of padding to the left, and 5px to all other sides.

5. Update the styles for the footer to add 20px of padding all sides. Note that if you had previously used line breaks in the HTML to separate the content from the footer, you should remove those.

<div class="alert alert-info" role="alert">
:question: Why do we increase the padding as opposed to the margin?
<p>Recall that gap between the header and the nav. That was caused by margin. Margin space is "outside" the element boundaries, so the background color does not fill that space.</p>
<p>By increasing the space "inside" the element boundaries, padding, the element background color fills that space and the text or other content moves away from the apparent edge of the element.  (Review the box model in your textbook.)</p>
</div>

### Validate & Test
Validate the CSS using the W3C validator. Check your page by viewing it in the browser.  It should look similar to the image below.  <img src="{{ "/assets/assignments/cs-pt/pt2-home-final.png" | prepend: site.baseurl }}" alt="Screen capture of Home page with centered content." />


## Submit the Assignment
Before you turn your project in:

1. Double check that you have saved all your files and close your editor.

2. Find your project folder in the file system, and open the index.html page in the Chrome browser. Re-check that it matches the wireframe.

3. Using the navigation links, verify all pages against the wireframes.

4. Next open the web page in a different browser such as Firefox, Internet Explorer, or Safari. Again re-check that all pages match the display in Chrome and the wireframes.  Note any differences.

5. Use the W3C Validator to re-validate the CSS and all HTML pages.  Remember that validation errors are a big loss of points!


When everything looks good, commit and push your files up to GitHub and submit a pull request to have your work graded.  

Also, zip the project folder and upload to the D2L dropbox.
