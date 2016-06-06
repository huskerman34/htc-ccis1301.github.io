---
title:  "Developer Tools"
---

## Introduction to Browser Developer Tools
The browser developer tools are perhaps the single most valuable tool in web development. They allow you to see your HTML and CSS (and later JavaScript) as the browser itself does. It can help you adjust and modify the page layout and design, debug problems, improve page load time, and so much more. The more you use and learn about these tools, the happier your web developer self will be.


## Open the Dev Tools
Access the Developer Tools in Chrome from the Chrome menu in the top right corner of the window. Select Tools  > Developer Tools. (It is helpful to learn the shortcuts.)
<img src="{{ "/assets/images/dev-tools/open-dev-tools-menu.png" | prepend:site.baseurl }}" alt="Screenshot - Use menu to open Chrome Developer Tools." />

The DevTools window will appear (usually) at the bottom of the browser window. You can have it open in a separate window (click on) or move it to the side (click and hold for sub menu) by using the window pop out button in the upper right.
<img src="{{ "/assets/images/dev-tools/dev-tools-dock.png" | prepend:site.baseurl }}" alt="Screenshot - How to dock, pop-out, or move the Chrome Developer Tools display." />

## Panels
The main window has eight main groups of features accessible as panels along the top.
<img src="{{ "/assets/images/dev-tools/dev-tools-panels.png" | prepend:site.baseurl }}" alt="Screenshot - Panels in the Developer Tools display." />

These each support a particular feature that is useful to web developers. We will focus mainly on the Elements panel, but you can learn more about the DevTools and the other panels from the [Google Chrome DevTools Site](https://developers.google.com/web/tools/chrome-devtools/).

## The Elements Tab
This tab is the most valuable tab when working with HTML and CSS. The left side of the view shows you the DOM tree and allows you to view and modify and remove elements. If you select an element on the left, you can see the CSS applied to that element in the window on the right.
<img src="{{ "/assets/images/dev-tools/elements-panel.png" | prepend:site.baseurl }}" alt="Screenshot - Elements Panel, with DOM on the left and CSS on the right." />

There are multiple tabs on the right side. We will only be using the first two - Styles and Computed.

The Styles tab shows all of the styles applicable to the selected element. Click on an element in the DOM tree, and you will see the CSS applied to that element. Notice that the display includes where the CSS is from - the stylesheet name and the line number in that stylesheet. The checkboxes next to each property allows you to turn various styles off and on. This can be very helpful in determining if a style property is actually affecting the element's display or doing what you intend.

### CSS Cascade
The styles are displayed in order of the highest priority to the lowest. You’ll notice that some lower priority styles will have strikethrough text. This means that style is overridden by a rule with a higher priority.  
<img src="{{ "/assets/images/dev-tools/overriden-style.png" | prepend:site.baseurl }}" alt="Screenshot - Elements Panel, showing overridden style with strikethrough text." />

Generally speaking styles will *cascade* by the following rules, where number one has the highest priority:

1. Inline style (inside an HTML element)
2. Internal style sheet (in the head section)
3. External style sheet
4. Browser default


### CSS Box Model
Click on an element in the DOM tree. Notice that when you click on the element in the DOM tree, it highlights in the main browser window.
<img src="{{ "/assets/images/dev-tools/element-highlight.png" | prepend:site.baseurl }}" alt="Screenshot - Elements Panel, showing DOM element selected and highlighted on page." />

While the Styles tab shows you every single style, even if it is overridden, the Computed tab only displays the final applied CSS. While this does not show you where those styles come from, it is a much cleaner view.
<img src="{{ "/assets/images/dev-tools/elements-computed-css.png" | prepend:site.baseurl }}" alt="Screenshot - Elements Panel, showing DOM element selected and highlighted on page." />

It also has a very helpful display of the CSS box model for margins, border & padding. We’ll be talking more about this later on, but for now you can see that it shows the size of various parts of the element style:

- blue (in the center): the size of the element itself
- green: the size of the element's padding
- gold: the size of the element's border
- orange: the size of the element's margin

Note sizes shown are in pixels and the size for the padding, border, and margin may vary on each side (top, right, bottom, & left). The colors used here correspond to the color used to highlight the element on the page when you hover with your mouse over the DOM element in the left side of the Elements panel.


### Editing CSS
You can experiment with getting your styles right by editing them directly in the DevTools. For example, you can edit the background color of the footer by clicking on the little color block which brings up a color chooser.
<img src="{{ "/assets/images/dev-tools/open-color-picker.png" | prepend:site.baseurl }}" alt="Screenshot - Elements Panel, Style Tab - Edit color by using the color picker." />

Editing directly in the browser dev tools can also be particularly helpful when trying to find the best size for margins, padding and positioning when you aren’t sure exactly how many pixels you need. You can edit an existing style by clicking on it. You can also add new properties to an existing rule or use the + (in the upper right) to add a new style.  

Note: While editing in the browser can help you get the look you want, these styles will be gone when you refresh the page. Make sure to manually update your HTML or CSS files with the updates or setup a [Workspace](https://developers.google.com/web/tools/setup/setup-workflow?hl=en) so the Developer Tools have access to update the files.


### Modifying the DOM
You can also modify the HTML structure or the DOM from the Elements panel in the developer tools. If you select an element and right click on it in the DOM tree view, you will see options to edit or delete that element. You can also cut and paste and drag and drop to reorder elements.  If you double click on the element, you can also add or edit attributes, edit the HTML, or copy it to the clipboard.  


## Console
The console, also known as the JavaScript console, will show you any errors that occurred as your page was loaded. This is a great place to go to see if any CSS or image files were not found as the page was loaded. This could indicate a typo in your path or URL in your HTML or CSS file.
<img src="{{ "/assets/images/dev-tools/console-errors.png" | prepend:site.baseurl }}" alt="Screenshot - Console Panel showing an error for an image that was not found." />

This feature becomes more useful once you have learned some JavaScript, as you can actually enter JavaScript in here to test or debug your page. However, checking this page for errors is good habit to develop now.


## Network
The network panel will show you all of the items that are requested by the browser to display your page. For each item, you can see if the request was successful, the size of the resource and the time it took to get the resource. While we will not spend a lot of time here in this class, this is a great resource for looking at the timing of loading various components of your page.
<img src="{{ "/assets/images/dev-tools/network.png" | prepend:site.baseurl }}" alt="Screenshot - Network Panel showing the resource load times." />

In the example above, notice the one image is particularly large and taking a lot of time to load. Depending on the purpose of the image, it might be a good idea to reduce the file size by either reducing the actual image size or the image quality.

## Learn More
We've only covered a small portion of what you can do with the Developer Tools, but this should be enough to get you through this course.  If you are interested in learning more, you can find more information on the [Google Chrome DevTools Site](https://developers.google.com/web/tools/chrome-devtools/).
