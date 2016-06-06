---
title:  "Developer Tools Lab 3"
---

## Instructions
For this lab, you will use the browser developer tools to analyze your case study web pages.  This should be done after completing and pushing the work for the third part of the case study (Ch 8) to GitHub.  You should use your live web site for this lab, not a file or live preview on your computer.

Create a MS Word (any version) or RTF document for your lab solution. _Important:_ Any file type that I cannot read will receive no credit for the assignment.  

As you go through the tasks below, you will need to both answer any questions and provide a screenshot showing how you got the answer. The screenshots _must_ show both the page content in the browser and the same content in the developer tools. Be sure to clearly label each screenshots with the task that it corresponds to.

### Task 1
Open the home page in the browser and open the Developer Tools. Dock the tools at the right side of the screen.  

If your page is not displayed in tablet size, reduce the width of the page until it is small enough to show the tablet view of the web site.

### Task 2
Locate the HTML element for the wrapper div in the DOM.  Locate the styles that are explicitly applied to this element by your pacific.css file when the page width is tablet sized.  


### Task 3
While still looking at the wrapper div, locate the styles for the desktop sized page.  How many styles are overridden by the tablet CSS?  List the original CSS values and next to them show the overridden values.

It is important to realize that the CSS in the media queries alters the CSS already applied to the element. This is just another part of the *cascade* in the Cascading Style Sheet rules.


### Task 4
While still looking at the wrapper div, adjust the width of the page so that it transforms into the mobile display.  Is any new CSS applied to the wrapper div for the mobile display?


### Task 5
Adjust the page width back to the tablet size and select the nav element. Locate the styles that are explicitly applied to this element by your pacific.css file when the page width is tablet sized.


### Task 6
While still looking at the nav, locate the styles for the desktop sized page.  How many styles are overridden by the tablet CSS?  List the original CSS values and next to them show the overridden values.


### Task 7
While still looking at the nav, adjust the width of the page so that it transforms into the mobile display.  Is any new CSS applied to the nav for the mobile display?


### Task 8
While still looking at the nav in the mobile view, locate the styles for the tablet and desktop sized page.  List the desktop CSS values and next to them show the overridden values first for tablet, then for mobile.

### Task 9
If you uncheck any of the overridden styles, you'll notice that it does not affect the display of the page.  Why not?

### Task 10
Which of the elements contained in the nav do not have overrides for tablet or mobile display?


## Submit Assignment
Make sure that you have labeled each task in your document and have saved it as a MS Word or RTF file. Any file type that I cannot read will receive no credit for the assignment.  

Upload the file to the dropbox on D2L.
