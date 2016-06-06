---
title: Simple Form Page
---

## Overview
For this assignment, you will make a web page for a simple newsletter subscription form.  

*Important*: There is no "back-end" for this form page, so you should set up the URL for the form tag, but understand that it will not function.


## GitHub
The GitHub repository for this assignment is [simple-form](https://github.com/htc-ccis1301/simple-form).

The repository contains the standard Readme.md and .gitignore files and an empty index.html file.


## Requirements
Create a web page for the Moonflower's Coffee Newsletter.  The web page should include the following:

- A header/h1 for Moonflower's Coffee
- A heading "Newsletter", followed by the text: "Register for our weekly or monthly newsletter by submitting the following form."
- A heading for the subscription form "Newsletter Subscription" followed by text that indicates required fields are marked with an asterisk
- The subscription form as described below


### Form Details
Form fields:

- A fieldset with radio buttons for Weekly (selected by default), Monthly, or Specials Only
- Required textfields for the first name, last name and email address
- A text area for any comments
- A submit button

Use the following id and names exactly (case-sensitive) for the input controls:

- weekly, monthly, specials
- fName, lName, email
- comments

Style the form so that:

- the labels have a width of 120px are right aligned to sit before the input fields
- the text fields are sized to be 35 characters
- the comments area has 5 rows and 34 characters per line
- the width of the fieldset is 350px with a grey lined border
- the submit button aligns with the input fields

On a mobile device, adjust the styles so that the labels sit above the input fields and the input fields have a width of 100%.

You may apply other styles as you see fit, so long as the above requirements are met.

### Sample Page
The full sized page should look similar to the following image:
<img src="{{ "/assets/images/simple-form-full.png" | prepend:site.baseurl }}" title="Sample Form" />

The mobile sized page should look similar this image:
<img src="{{ "/assets/images/simple-form-mobile.png" | prepend:site.baseurl }}" title="Sample Mobile Form" />


## Submit the Assignment
Before submitting the assignment, you should double check that your page is valid using the W3C HTML & CSS Validators.  
When complete, the assignment must be submitted using a GitHub pull request with a screen shot of that pull request placed in the D2L dropbox.  Pay attention to the assignment due date found on D2L.
