---
title: Pacific Trails Case Study
---

<div class="alert alert-danger" role="alert">
  :exclamation: Overall the Pacific Trails Case Study will follow the case study from the textbook, but how we get from beginning to end will be a little different in places. Please use these instructions to direct your work.
</div>

## Grading
This assignment is worth 50 points and will be graded as follows:

- All HTML and CSS files are valid - 10 pts (all or nothing - one error means 0 points for validation)
- Correct HTML5 template elements (html, body, head, meta, title) - 5 pts each page, 10 points total
- Correct HTML5 structure elements (header, nav, main, footer) - 5 pts each page, 10 points total
- Page display and functionality in browser matches expectations - 5 pts each, 10 points total
- Page content is correct (includes spelling, capitalization, correct images, etc.)  - 5pts each, 10 points total

This assignment includes the case study work from both Chapter 2 & 4 in your textbook.

## Introduction
The case study projects are included at the end of most chapters of your text book. Generally speaking, you will follow the instructions in the textbook, but you should check here for notes that have you modify or change parts of the assignment. I will add general information and tips here, but I *__may__* also modify the assignment to prevent re-work later or to better match current best practices.

Please read the introduction to the case study found at the bottom of page 61. At the top of page 62, you can see the planned site map for the website and the initial wireframe layout of the pages.

We will treat this case study much like a real world iterative web development project.  You can imagine me as your go-between with the actual client.  I will handle getting the details worked out while you handle the coding work.  

We will deliver something (your completed assignment) to the client on a regular schedule.  The first deliverable is due in only one week, but is only a small amount of the final site.

<iframe width="420" height="315" src="https://www.youtube.com/embed/jVDqs_CgueM" frameborder="0" allowfullscreen></iframe>

## GitHub
To do this project, you will begin by forking and cloning the ptCaseStudy repository from our class GitHub page.  This repository includes the images and media files that you will use later for the project, but you will add all of the html and css files.

__Repository__:  [ptCaseStudy](https://github.com/htc-ccis1301/ptCaseStudy)

You will only need to fork the repository once, then you will continue updating the code for each part of the assignment by committing and pushing to the same repository.  


## Working with Brackets
When you use Brackets, be sure that you are opening the entire folder (look for the Open Folder command in the File menu) and not just opening single files. This is generally required for the Live Preview feature to work correctly, and will help you to get the file names correct as you build links in your pages.

The Live Preview feature requires the Chrome browser to work. You can start it from the menu or from the lightning bolt icon on the right side of the application window. Live preview allows you to make changes to your HTML and/or CSS and see the results immediately in the browser without needing to save your file.

<img src="{{ "/assets/assignments/cs-pt/bracketsHtmlStructure.jpg" | prepend: site.baseurl }}"
    title="HTML Structure in Brackets"
    alt="Screen capture showing Live Preview in Brackets with the nav element highlighted." />

It will also put a blue outline around the section of the page that you are working on to help call attention to it.  The blue outline move based on your cursor position in the editor.  It will not be shown on your final page when opened outside of Brackets.

## Beautify: Code Readability
Another extremely handy feature of brackets is a plug-in or extension called Beautify. More information on Plugins is available on the [Brackets Wiki: Extensions](https://github.com/adobe/brackets/wiki/Brackets-Extensions). Use the extension manager to search for and install Beautify. This will add Beautify as an option in your right-click context menu as well as the Edit menu.  There is also an option in the Edit menu to Beautify on Save.  I highly recommend this.

Please use Beautify to help format your code for readability before turning it in. Clear and consistent use of indentation helps prevent errors and allows me to give better feedback on your work.  Points for assignments may be reduced if I find your files hard to read or comment on.  

## Chapter 2 - Tips
The case study instructions from the end of Chapter 2 have you create the home page and the yurts page.  This should be pretty straightforward.

Make sure to call the Home page index.html.  This is an important file name, as it is used by most web servers as the default page when a specific HTML page is not requested.

Remember to treat all file names as case sensitive. If you work on a Windows computer, your local computer will not care if you call the file Index.html in one place and index.html in another. However the GitHub web server, my computer (which I grade on) and nearly all other operating systems will care. This is a main source of broken links and will result in a lower score on the assignment.

Make sure to note the layout of the contact information in the home page image. There should be a blank line between the address and phone number. Also note the company name is considered part of the contact information.

For the Yurts page, in step 3c, the book asks you to use the `<dl>`, `<dd>`, and `<dt>` tags in Chapter 2, but then convert that to `<h3>` and `<p>` tags later on.  It is easier (and more semantically correct) to just start by using the <h3> tags for the headings and use <p> tags for the text that follows.

Test your links!  The link from the Home to the Yurts page should work and the link from Yurts to the Home page should work.  Make sure these are relative links and do not include any drive letters from your local computer.

Double and triple check your spelling, punctuation, and layout. You might think that these are not important, but imagine if you were the business owner who found their name, address or phone number on the page was incorrect.  Would you hire that person again?

Make sure to beautify and validate your files and test your work before moving on to Chapter 4.  There are images in the textbook to show you what the pages should look like. I would even recommend committing your changes and pushing them to GitHub.

## Chapter 4 - Tips
<div class="alert-danger" role="alert">
<strong>Do not create a new folder for this work as instructed in the textbook.</strong>
It is important that you continue working in the same directory where you cloned down the files from GitHub.
</div>

The instructions at the end of Chapter 4 have you add CSS to improve the look of the pages you created in Chapter 2. Again, this is pretty straightforward, but there are a few things to watch out for.

Make sure that you correctly code the `<link>` tag or you will not see any results from adding the CSS.  A relative path should be used. Again, no drive letters should be present in the path.

If you have used the `<h3>` and `<p>` tags, make sure to set up the CSS for the <h3> to be dark blue in task 2 not the `<dt>` tag.

Pay attention to the instructions for the resort style class. This requires HTML tags be added to the html file in addition to the changes in the CSS. The intent of this is to change the display of the company name so that it stands out on the page. That means that it should be used every time the company name is used in the web page text through out the entire web site.  

Make sure to beautify and validate your files and test your work.  There are images in the textbook to show you what the pages should look like. I would even recommend committing your changes and pushing them to GitHub.

While you did not change much of the HTML here, do not neglect to re-validate the HTML files.  Even a small or accidental change could cause an error which will result in a large loss of points on the assignment.


## Submit the Assignment
When everything looks good, commit your changes and push your files up to GitHub.  Verify your changes have been pushed, then test your updated site on the web.

Get the your webpage URL from the GitHub Settings and open your page live on the web.  I strongly recommend that you copy this URL and edit your repository description to include this link so that you can open your page again easily.  You will be testing it many times over the semester, so this small effort now will payoff long term.

Retest your links and double check your page layout and display. I also encourage you to re-validate your HTML and CSS using the link to your live page.  Paste the URL from your live page (not the GitHub view of the text) into the W3C Validator - Validate by URI tab.

When everything looks good, create the pull request to have your work graded.

While you can continue working on the case study locally, I encourage you not to push any additional changes to GitHub until the assignment has been graded.  Your pull request will automatically update to include any additional commits that are pushed to GitHub.  Local commits stay local, but pushed commits will update the pull request.
