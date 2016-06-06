---
title: Graduation Plan
---

## Overview
For this assignment, you will make a web page that outlines the courses you plan to take for graduation. If you are not in a program for a degree or certificate, you can borrow any of our programs and make things up.  While I'd like this information to be useful, the real intent is to build an HTML table.


## GitHub
The GitHub repository for this assignment is [grad-plan-table](https://github.com/htc-ccis1301/grad-plan-table).

The repository is initially empty, except for the standard Readme.md and .gitignore files and an empty index.html file.


## Requirements
Create a web page to outline your plans for graduation.  The page should include the following:

- Nav links that include a link to your GitHub profile page, information about this program on the web, and anything else you would like to highlight
- A page header titled something like "My Graduation Plan"
- A section heading calling out the program you are working toward
- A short paragraph with a description of the program and why you are interested in it
- A table with your graduation plan as outlined below
- A footer with your copyright and contact info - it is fine to do a fake mailto like in the case study.


### Table
Build an HTML table to outline the courses required for graduation from your program and when you plan to take them.

Organize the table so that there is a row for each course and they are ordered by semester. Each course should have a semester (when you intend to take the course), the course number, name and number of credits.  These should be reflected as column headings.  Instead of repeating the same semester across multiple rows, have the cell span multiple rows so that information appears only once.

At the bottom of the table, add a summary row showing the total number of credits. Add a table caption with the title and make sure to use the table sections for the headings and the summary information in the footer.

Style the table so that:

- the title is in large text similar to a page heading
- the column headings have a darker background color and bold text
- there is an alternate background color on every other row (use CSS3 Structural Pseudo-classes)
- the text in the Semester column (use a style class) stands out - different text color, size, weight, and/or background color
- apply a darker background color to the summary row so that it also stands out

You may apply other styles as you see fit, so long as the above requirements are met.

### Sample Page
<img src="{{ "/assets/images/sample-grad-table.png" | prepend:site.baseurl }}" title="Sample Table" />


## Submit the Assignment
Before submitting the assignment, you should double check that your page is valid using the W3C HTML & CSS Validators.  
When complete, the assignment must be submitted using a GitHub pull request with a screen shot of that pull request placed in the D2L dropbox.  Pay attention to the assignment due date found on D2L.
