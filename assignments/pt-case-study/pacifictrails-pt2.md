---
title: Pacific Trails Case Study
---

<div class="alert alert-danger" role="alert">
  :exclamation: Overall the Pacific Trails Case Study will follow the case study from the textbook, but how we get from beginning to end will be a little different in places. Please use these instructions to direct your work.
</div>

## Grading
This assignment is worth 50 points and will be graded as follows:

- All HTML and CSS files are valid - 10 pts (all or nothing - one error means 0 points for validation)
- Conversion of description list on Yurts page to headings & paragraphs - 5 pts
- Removal of all non-sematic HTML tags (inline *syle* tags such as bold and italics used before learning CSS) - 5 pts
- File readability and page display & functionality in browser matches expectations - 5pts each, 15 points total
- Page content is correct (includes spelling, capitalization, correct images, etc.)  - 5pts each, 15 points total

This assignment includes the case study work from both Chapter 5 & 6 in your textbook.


Make sure to check the feedback for your previous assignment on GitHub. Note that errors that are not fixed will continue to have points deducted each week.


## GitHub
Continue working with your forked copy of the [ptCaseStudy](https://github.com/htc-ccis1301/ptCaseStudy) repository.  There is no need to fork the repository again.

<div class="alert alert-warning" role="alert">
<strong>Do NOT make multiple folders for each section of the assignment.  You want each version to update and add to the same directory and files.</strong><br>
GitHub will track versions of your files at each commit, so you can always go back to any previous committed version. If you would like (this is not required) you may create a release for each part of the assignment.  See this <a href="https://help.github.com/articles/creating-releases/">GitHub Release</a> article for information on how to do this.
</div>


## Chapter 5 - Tips
The case study instructions from the end of Chapter 5 have you add small images to each page that you will remove in the Chapter 6 case study.  __You can skip adding the images in Chapter 5.__

Test your links!  You are creating a new activities.html page in this part of the case study.  Make sure to verify that all of the links to and from this new page work correctly.

<div class="alert alert-warning" role="alert">
Remember to treat all file names as case sensitive. If you work on a Windows computer, your local computer will not care if you call the file Activities.html in one place and activities.html in another. However the GitHub web server, my computer (which I grade on) and nearly all other operating systems will care. This is a main source of broken links and will result in a lower score on the assignment.
</div>

Most of the work for this chapter is removing the tags used previously to add bold and italics to the text.  Make sure all of these tags are removed and that the same styling is now applied using CSS. I will be specifically looking for this while grading.  You should only use `<b>` and `<i>` (or the equivalent `<strong>` and `<em>` tags) when needed to mark or highlight specific text for semantic reasons, not just for visual display or design.

Double and triple check your spelling, punctuation, and layout. You might think that these are not important, but imagine if you were the business owner who found their name, address or phone number on the page was incorrect.  Would you hire that person again?

## Chapter 6 - Tips
The instructions at the end of Chapter 6 have you make some pretty dramatic visual changes to the layout of the Pacific Trails pages.  There is a lot of CSS work here.  Take your time and pay attention to the details.

The new CSS depends on adding a new wrapper div to the page that *wraps* all of the page content inside of the body - everything from the header to the footer. Adding this div incorrectly in the HTML can result in the page not looking correct, as can not selecting it properly by id in the CSS file.  As you add the new CSS be aware of when you are selecting items by tag name, by id, and by style.

I strongly encourage you to write a little CSS, then test your page before continuing on. Students who have the most trouble with this assignment (as well as the next) tend to write all of the CSS then test. Then when something does not appear correct, they struggle to know what part to fix.  

By working in smaller pieces, it is easier to know what to change. However this also requires you to understand how the CSS you are writing should change the look of your page.  Being able to do this is a key part of doing the reverse - seeing what you want the page to look like and knowing what CSS to write to have it look that way. There will not always be a book there to tell you.  

Make sure to beautify and validate your files and test your work.  There are images in the textbook to show you what the pages should look like. I would even recommend committing your changes and pushing them to GitHub.

Make to re-validate all of the HTML and CSS files.  Even a small or accidental change could cause an error which will result in a large loss of points on the assignment.



## Submit the Assignment
When everything looks good, commit your changes and push your files up to GitHub.  Verify your changes have been pushed, then test your updated site on the web.

Retest your links and double check your page layout and display. I also encourage you to re-validate your HTML and CSS using the link to your live page.  Paste the URL from your live page (not the GitHub view of the text) into the W3C Validator - Validate by URI tab.

When everything looks good, create the pull request to have your work graded.

While you can continue working on the case study locally, I encourage you not to push any additional changes to GitHub until the assignment has been graded.  Your pull request will automatically update to include any additional commits that are pushed to GitHub.  Local commits stay local, but pushed commits will update the pull request.
