---
title:  "Chapter 6: More CSS"
layout: notes
---


## Spacing & Layout
The CSS box model shows an element's size, padding, border, and margin.  Remember that the browser developer tools will illustrate the box model for you for a selected element.  In the image below, you can see the element's size (in the blue area in the center), the padding (the inner green area), the border (the yellow area separating the padding and margin), and the margin (the orange outer area).

<img src="{{ "/assets/images/ch6/css-box-model-ex.png" | prepend:site.baseurl }}"
    alt="Image of the CSS box model diagram from the Chrome developer tools.">

Remember that padding picks up the element's background color, while the margin is transparent and thus shows the color of the parent or containing element.

Key properties:
- width and height
- margin (note both the shorthand and individual properties)
- padding (note both the shorthand and individual properties)
- border (note both the shorthand and individual properties)

Understanding the box model and how it affects the layout of HTML elements is important to creating a *theme* or look-and-feel for your web site.  It controls the size and spacing of elements, which can have a significant effect on your page layout.  It is especially important to consider the visible (padding) and invisible (margin) spacing when moving and *floating* elements outside of their normal positions.  (We will look at in the next session.)  

## More CSS
These are all topics you should be aware of, but may not want or need to memorize.  They're easy to look up if you need them, and aren't used as frequently as others.

Keep in mind that this is all relatively new stuff and you'll want to pay attention to browser support for these features.  Ensure that an acceptable fall-back is in place when these properties are unsupported.

### Rounded Corners
Rounded corners were a *thing* a few years ago, but the trend more recently has leaned back towards square.  The current *buzz* style varies year-by-year and individual style varies site-by-site. Rounded corners used to be a more difficult thing to achieve.  You needed to actual set them up with images for the corners, with the right background color and position.  It was tricky and made sites stand out a bit more if they could pull it off.  (If you bump into this old-style stuff, be sure to speak up about the newer, better way.)

Today it's simple to set up in minutes using CSS.  Perhaps that's why it's less of a trend?  Who knows.  But if you like the look and it works for your site, use it.  If you (or your customer) prefer the sharp, square corners, use those. Worry more about what works for your site's style than the latest *buzz* trends.


### Box and Text Shadow
A good application of these styles can really make a website *pop* or stand out.  However don't get too carried away with them.  If you start applying it to everything, you just might get dizzy looking at your page.  If everything starts floating off the screen, it can get a little disconcerting.  Use it sparingly for the best effect.


### Opacity & Colors
Using semi-transparent `<div>` or headings over a photographic background can make for a really lovely look for a web page, especially one that might be travel or art focused.  Just like with the shadows though, this is probably best applied in smaller amounts.  Large areas of text for example will be much harder to read if there's an image in the background. You can achieve this semi-transparent look by using either the opacity property or the background and color properties with RGBA or HSLA colors.  


### Gradients
Being able to configure gradients in CSS is awesome!  This is another one of those things that we used to do using images.  Applying gradients through CSS is much more flexible.  The radial gradient provides a nice spot-light effect that is pretty neat, while the linear gradient makes for a simple but interesting background.  Often we will use a gradient background for the body, and place a solid white (or light-colored) content area over top of it.  That light, solid color makes it easier to read any text.  
