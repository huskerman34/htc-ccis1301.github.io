---
title: Pacific Trails - Part 4
name:  case-study-pacific-pt4-v1
---

<div class="alert alert-danger" role="alert">
  :exclamation: Overall the Pacific Trails Case Study will follow the case study from the textbook, but how we get from beginning to end will be a little different. Please use this assignment sheet to direct your work. The instructions from the end of chapter case studies in the book do not match my assignments.
</div>

## Grading
This assignment is worth 50 points and will be graded as follows:

- All website HTML &amp; CSS is valid (all or nothing) - 10 points
- Page structure, display, &amp; functionality consistent and correct on all pages for desktop, tablet &amp; mobile size - 15 pts
- New Reservation page (HTML &amp; CSS) - 10 points
- Yurts page table (HTML &amp; CSS) - 10 pts
- Home page video for desktop &amp; tablet - 5 pts

Remember that because this is the final submission for this case study, it cannot be submitted late.

The planned site map:
<img src="{{ "/assets/assignments/cs-pt/sitemap.png" | prepend:site.baseurl }}" title="Pacific Trails site map"
      alt="The site map - a Home Page with sub pages for Yurts, Activities, and Reservations." />

Current wireframes:
<a target="_blank" href="{{ "/assets/assignments/wireframes/PacificTrailsP4-Wireframes.pdf" | prepend:site.baseurl }}">PacificTrailsP4-Wireframes.pdf</a>

In this part of the case study, we'll be adding the Reservations page, pricing information, a new video, and features for search engine support.

## Task 1 - Vacation Packages Table
Check the wireframes for the new rates table to add to the yurts.html page.

### HTML
On the yurts page, add the new heading for "Yurt Packages", and add the paragraph text from the wireframe below it.  Add the table using the content below.
  <table>
  <tbody>
  <tr><th>Package Name</th><th>Description</th><th>Nights</th><th>Cost per Person</th></tr>
  <tr>
      <td>Weekend Escape</td>
      <td>Two breakfasts, a trail map, and a picnic snack</td>
      <td>2</td>
      <td>$450</td>
  </tr>
  <tr>
      <td>Zen Retreat</td>
      <td>Four breakfasts, a trail map, a picnic snack, and a pass for the daily sunrise Yoga session</td>
      <td>4</td>
      <td>$600</td>
  </tr>
  <tr>
      <td>Kayak Away</td>
      <td>Two breakfasts, two hours of kayak rental daily, and a trail map.</td>
      <td>2</td>
      <td>$500</td>
  </tr>
  </tbody>
  </table>

On each of the cells containing the description *data* (not the heading), configure a style class called "text".  We will configure this in the CSS to left align the text in these cells.

### CSS

1. In the CSS file, add a new style rule for the table so that it has a 1 pixel med blue border (#3399CC), a width of 80%, and no cellspacing (border-spacing: 0;).

2. Add a rule for the table cells to have 5 pixels of padding on all sides and a 1 pixel med blue border, and centered text.

3. Set up the "text" style class to have left-aligned text.  (This is used for the Description column.)

4. Set up zebra (alternate row) striping on the table rows using a light blue (#F5FAFC) background color.

### Validate & Test
1. Make sure to save all of your files and close your editor.

2. Validate both the HTML for the yurts page and the stylesheet file using the appropriate W3C validator.

3. Open the Yurts page in the browser. Verify the display of the table.  All data should be centered except for the text in the Description column.  Note the heading should center, but the text in that column should be left-aligned.

4. Check each of the other pages to ensure there are no display problems.


## Task 2 - Reservation Page
Check the wireframes for the new reservation form.

###HTML
1. Add a new reservations.html page to your project.  It should have the same general layout as your other pages.  The title should be "Pacific Trails :: Reservations".  Refer to the wireframe for the page content.

2. Set up the form as shown in the wireframe using HTML 5 form controls.  Set up the controls to have the following values for both the name and id fields:  `myFName`, `myLName`, `myEmail`, `myPhone`, `myArrival`, `myNights` and `myComments`

3. Make sure to use the required attribute to indicate the required fields.

4. The form action should be set to: `http://webdevbasics.net/scripts/pacific.php`


### CSS

1. Add a CSS style rule for the form labels.  The labels should float left, have block display, right-aligned text and a width of 120px.  Configure a small amount of padding on the right to separate them from the form controls.

2. Add a CSS style rule for the input elements and text area so that they have block display and 20px of bottom margin.

3. Alter the form display on mobile devices (480px or smaller) so that the labels display above the input controls instead of to the left. (Hint: remove the float and alter the alignment.)


### Validate &amp; Test

1. Make sure to save all of your files and close your editor.

2. Validate the HTML and CSS files using the appropriate W3C CSS validator.

3. Open the Reservations page in the browser. Test the form to confirm that the controls and required fields are functioning correctly. Test the form submission.

4. Verify that when you reduce the widow width to less than 480px the form layout correctly shifts to position the labels above the entry fields.

5. Check each of the other pages to ensure there are no display problems.


## Task 3 - Multimedia & Polish

### Navigation Transition
Update the CSS that controls the navigation hover color change so that it has a 3-second ease-out transition.  This should provide a more gradual change in the color when you hover over each item.

### Video

Below the image on the homepage, add an HTML5 video control.  Configure the video, source, and embed elements to work with the following files:

- pacifictrailsresort.mp4
- pacifictrailsresort.ogv
- pacifictrailsresort.swf
- pacifictrailsresort.jpg

The dimensions of the video are 320 pixels wide by 240 pixels high.

Locate the `#content img` selector which is configured in the stylesheet. Add the `#content video` and `#content embed` selectors to the style rule as follows:  

{% highlight css %}
  #content img, #content video, #content embed {
      float: left;
      padding-right: 20px;
  }
{% endhighlight  %}
Recall that using a comma between the selectors applies the rules to each of the selectors in the list.  This is different than a descendent selector.

Update the HTML and CSS so that at desktop and tablet sizes only the video will display, and at mobile device sizes only the image displays.

### Search Engine Description
Add a description meta tag for each page of the Pacific Trails site.  You'll need to write a description for each page.  Keep in to a few sentences, about 25 words or less.


### Validate & Test

1. Make sure to save all of your files and close your editor.<

2. Validate the HTML and CSS files using the appropriate W3C CSS validator.

3. Open the Home page in the browser. Ensure that the video displays and functions at both desktop and table sizes.  Verify that when you reduce the widow width to less than 480px that the video is replaced by the image.

4. Check each of the other pages to ensure there are no display problems.



## Submit the Assignment
Before you turn your project in:

1. Double check that you have saved all your files and close your editor.

2. Find your project folder in the file system, and open the index.html page in the Chrome browser. Re-check that it matches the wireframe.

3. Using the navigation links, verify all pages against the wireframes.

4. Next open the web page in a different browser such as Firefox, Internet Explorer, or Safari. Again re-check that all pages match the display in Chrome and the wireframes.  Note any differences.

5. Use the W3C Validator to re-validate the CSS and all HTML pages.  Remember that validation errors are a big loss of points!


When everything looks good, commit and push your files up to GitHub and submit a pull request to have your work graded.  

Also, zip the project folder and upload to the D2L dropbox.
