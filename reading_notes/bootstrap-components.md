---
title:  Bootstrap Components
---

Bootstrap includes many helpful [components](http://getbootstrap.com/components/).  We'll discuss a few below.  This should be enough for you to get a feel for how to read the docs and get comfortable with some basics.  The intent is to build enough confidence that you can then read about the other components on the Bootstrap site and use them on your own.

## Navigation & Navbar
There are several different options for setting up and organizing a site's links and navigation - many of which are shown in the various examples on the [Getting Started](http://getbootstrap.com/getting-started/#examples) page.  Again, I encourage you to view the source for the examples and resize your display to view their responsive behavior.

### Navbar Examples

- [Regular Navbar](http://getbootstrap.com/examples/navbar/) - use links for positioning options: default, static and fixed
- [Carousel using Inverted Navbar](http://getbootstrap.com/examples/carousel/) with default positioning - inverted refers to the flipped colors (darker background) vs the default
- [Jumbotron using Inverted Navbar](http://getbootstrap.com/examples/jumbotron/) - inverted navbar with fixed positioning and a form

Notice that content aside, all of the differences in the examples above come from which style classes are applied.  Want the navbar to be fixed at the top, then apply the `navbar-fixed-top` class.  Want to swap (invert) colors, then apply the `navbar-inverse` class.

### Collapsed Mobile Navbar
You should also notice that the Navbar is intended to collapse for smaller devices.  By default this is configured to occur only for xs (or phone sized) devices, but the size where the collapse occurs is customizable.  When the Navbar is collapsed, it is condensed into a button which you can click to show the navbar content.
<img src="{{ "/assets/images/bootstrap/bootstrap-navbar-collapsed-links.png" | prepend:site.baseurl }}"
        alt="Screenshot of Bootstrap Navbar collapsed." style="max-width: 50%">
<img src="{{ "/assets/images/bootstrap/bootstrap-navbar-collapsed-form.png" | prepend:site.baseurl }}"
        alt="Screenshot of Bootstrap Navbar collapsed with a form." style="max-width: 50%">

<div class="alert alert-warning" role="alert">
:warning: The Navbar component requires JavaScript in order for the responsive <em>collapse</em> behavior to function correctly on mobile devices, but it will still function at full-size without JavaScript.
</div>

## Other Navigation Options
While you can customize the Navbar look to some extent, many *fancier* Bootstrap sites choose to use other components for the navigation.  I assume that a big reason is to avoid a certain *standard* Bootstrap look.  Just because everyone wants the benefits of using a great component library doesn't mean they all want the site to look the same as the next guys.  

### Navigation without the Navbar component

- [Blog Template](http://getbootstrap.com/examples/blog/) - shows a customized nav that is not using the Navbar component
- [Justified Links](http://getbootstrap.com/examples/justified-nav/) - another customized nav that uses [justified links](http://getbootstrap.com/components/#nav-justified)

Don't be afraid to think out of the box.  There are no *rules* that say you must use a particular Bootstrap component for a certain thing.  It's just a library of options. Check out some of these [real world examples](http://expo.getbootstrap.com/) and count how many you see with a Navbar.  None of them look anything like the examples.

## Jumbotron and Carousel
The [Jumbotron](http://getbootstrap.com/components/#jumbotron) component is intended for displaying a large marketing message to catch the attention of visitors right away.  It's pretty straightforward component, but it's appearance will change based on whether it is inside of a the Bootstrap container or if it has a Bootstrap container inside of it.  

- [Jumbotron Example](http://getbootstrap.com/examples/jumbotron/) - full width, not in a container
- [Narrow Jumbotron](http://getbootstrap.com/examples/jumbotron-narrow/) - padded with rounded corners, inside of a container

The [Carousel](http://getbootstrap.com/javascript/#carousel) component is another option for displaying a prominent, eye catching marketing message.  It is similar to the Jumbotron, but it allows you to rotate through a series of different messages.  Check out the [Carousel Demo](http://getbootstrap.com/examples/carousel/).

Notice that you don't see the [Carousel](http://getbootstrap.com/javascript/#carousel) component in the list of CSS components with the Jumbotron.  That is because it is one of the jQuery plug-in components that require JavaScript.  (Yes, the Navbar required JavaScript too, for the collapse behavior, but would still function full-size without it.)  The components that rely on [jQuery](https://jquery.com/) and JavaScript to function are on the [Bootstrap JavaScript](http://getbootstrap.com/javascript/) page.
