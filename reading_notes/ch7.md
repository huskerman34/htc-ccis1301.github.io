---
title:  "Chapter 7: Page Layout Basics"
layout: notes
---

## Page Flow

### Normal Flow
To make interesting and responsive layouts, we'll need to be able to move elements around on the page.  To do this, you need to understand how the browser positions elements by default.  This is called *normal flow* - and is based on the order that the elements occur in the HTML file.  

The browser places each element after the previous:

- *inline* elements flow across the width of the browser window until they wrap onto the next line
- *block* elements take up the entire width of the browser display, causing the next element to start a new line

### Float
The CSS `float` property allows us to alter the normal flow by first positioning them using normal flow, then shifting them to either the right or the left side of *their container*.  It is important to remember that elements that are floated are still kept inside of their parent element.

You can end a float by using either the CSS `clear` property or the `overflow` property.  While both work, using the `clear` property is more intuitive as `overflow` is intended for a different purpose - scrolling content.


## Page Layout & Positioning

### Two-Column Layout
The float property is used to create the sidebar in a standard two-column layout.  While you could float the sidebar to either the left or the right, it is more common to position the sidebar on the left. Since in English we read left to right, we will notice that content first, which is often what is intended.

As you are working through the two-column layout examples, notice that the background color is not configured for the `nav` element.  It is configured for its container. Since the `nav` does not have a background set, it is transparent, allowing the parent container's background color to show.  

This is important, as we can set the width of the nav, but it is trickier to try and set a height that can change based on the height of the browser display. By setting the color on the container, we get the illusion of the background color on the `nav`.  Try setting and unsetting a background color on the `nav` to see what is happening in those examples.

### Positioning
The CSS float property allows us to shift things right or left, but sometimes that isn't enough.  If you want more control over where an element will be placed, you can use the CSS `position` property.  There are a few options:

 - static - This is the default, so if you want to *un-do* and override something that is positioned outside of normal flow, you would use `position: static`.  

 - fixed - This causes something to stay in the same position on the browser display. Other content *may* scroll, but `fixed` content will remain in the same spot while the other items scroll.

 - relative - This allows you to shift an item relative to where it would have been placed by default using normal flow.  

 - absolute - This is used to precisely position an element.

 Try out the examples of each and make sure that you understand how each works.  Think about how and when you might use each type of positioning.  Share and discuss some ideas in the chat room.
 
The image gallery from Hands-On Practice 7.8 will be used in the Case Study.