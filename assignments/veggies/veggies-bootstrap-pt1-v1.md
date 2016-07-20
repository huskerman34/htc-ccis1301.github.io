---
title: Ms B's Veggies Part 1
---

To learn how to use Bootstrap, we'll make a simple website together to get a feel for how everything works.  We'll build a simple site for Ms. B and Benji, some local heirloom gardeners.  

It'll look like this when it is all finished.
<img src="{{ "/assets/images/bootstrap/ex-bootstrap-veggies-styles-final.png" | prepend:site.baseurl }}" alt="Screenshot of Ms B's completed website made with Bootstrap.">

## Get Starter Files
To get started, there are some files for you out on GitHub in the HTC-CCIS 1301 [veggies-bootstrap repository](https://github.com/htc-ccis1301/veggies-bootstrap).  Fork the starter repository to your account, then clone the repository to your computer to get started.

## Make the Home Page
Make a new index.html page inside the project folder.  Use the Basic Bootstrap Template below - note that this includes the CDN files - to get started.

<code class="gist" data-gist="5785c6e9534e956b79d7" data-gist-file="basicBootstrap.html">
</code>

Next, we'll customize the site for our new customer, Ms. B and her veggie stand.

1. Change the title to "Ms. B's Veggies".

2. Remove the `<link>` for the optional Bootstrap theme CSS.

3. Open the page and check the Console in the Browser Developer Tools to make sure that there are no errors getting the files from the CDN.  It should look like this:  
<img src="{{ "/assets/images/bootstrap/ex-bootstrap-veggies-template.png" | prepend:site.baseurl }}"
        alt="Screenshot of Bootstrap template with Ms B's Veggies title.">

Make sure that you didn't miss the title (shown on the browser tab) and if the font seems different, you may not be getting the Bootstrap CSS files.  Check the Console in the Developer Tools for errors or missing files.

4. Set up a div to hold our page contents and serve as our required Bootstrap container.  We will use the fixed width container (so apply the `container` class), as we'll center the container allowing that cool tartan background to show along the edges.  Begin the div just after the `<body>` tag, and end the div just before the `<script>` tags.

5. Once the container is added, you should notice that there is now some padding and "Hello World!" is no longer squished along the left side of the browser display.

## Main Content Area - Grid Layout
We'll use the Bootstrap Grid to set up the main content area for Ms. B and Benji.  They've got information on the featured vegetables for the week that should obviously come first on a smaller device, but they'd like to have their pictures displayed next to this information on a desktop.  

### Set up the Grid
If that sounded familiar, it should as it's very similar to what we did in the [grid demo from the reading](http://htc-ccis1301.github.io/reading_notes/bootstrap-grid.html) for column ordering.  Remove the "Hello World" text from the content container and set up a grid with 3 columns.  The first column should be wider than the others and contain the following information on the featured veggies.  Make the heading a `<h3>` and the veggies should be set up in an unordered list.  Use an inline style on the `ul` to hide the list marker.  Center the text for this column div.  You can use one of the Bootstrap [Typography Alignment classes](http://getbootstrap.com/css/#type-alignment) to do this.

<blockquote>
Featured This Week
  <ul style="list-style-type: none;">
        <li>Jenny Lind Melon</li>
        <li>Yellow Pear Tomatoes</li>
        <li>Mortgage Lifter Tomatoes</li>
        <li>Henderson's Black Valentine Beans</li>
        <li>Chioggia Beet</li>
        <li>Fairytale Eggplant</li>
  </ul>
</blockquote>

The next two columns should contain the pictures, one for Ms. B and the other for Benji.  You'll find image files for each of them in the images folder from the starter repository.  For the images, we'll use Bootstrap to make the images responsive, with rounded corners, centered in their container.  Information on how to do that is found here:  Bootstrap [Responsive Images](http://getbootstrap.com/css/#images-responsive).

Apply the appropriate styles to the columns so that:

- on a mobile and tablet sized device, you see the featured veggies, followed by Ms. B and Benji underneath but side-by-side.
- on a desktop device, you see Ms. B on the left, the featured veggies in the middle, and Benji on the right.

### Second Row
Add a second row to contain the following text:
<blockquote>
Ms. B's Veggies is a run by Ms. B, a local gardener and her trusty dog Benji. They've taken to the web to spread the word about their locally grown premium produce. Please show your support by stopping by to visit their vegetable stand.
</blockquote>

This data should always be full width. It should always take up the entire row.

You're site should now look as follows for the different display widths.

<img src="{{ "/assets/images/bootstrap//ex-bootstrap-veggies-grid-xs.png" | prepend:site.baseurl }}"
     alt="Screenshot of Ms B's Veggies at mobile size." style="max-width: 50%;">
<img src="{{ "/assets/images/bootstrap/ex-bootstrap-veggies-grid-sm.png" | prepend:site.baseurl }}"
     alt="Screenshot of Ms B's Veggies at tablet size." style="max-width: 80%;">
<img src="{{ "/assets/images/bootstrap/ex-bootstrap-veggies-grid-md.png" | prepend:site.baseurl }}"
     alt="Screenshot of Ms B's Veggies at desktop size.">


### Add the Jumbotron
We're going to add the Jumbotron inside of our existing Bootstrap container to give it the nice rounded corners and padding, like the [Narrow Jumbotron](http://getbootstrap.com/examples/jumbotron-narrow/) example.

Add the Jumbotron inside our Bootstrap container, above the row we added previously. It should contain the heading "Ms B's Heirloom Vegetables <small>Fresh to your table</small>" use a `<h1>` for the entire heading, and add the `<small>` tag around the "Fresh to your table" sub-text. Add a `<br>` before the sub-text to break the line nicely.  This should be followed by a paragraph that says:
<blockquote>
Every Friday from noon - 3PM at:
<br>123 Garden Ave
<br>St. Paul, MN 55123
</blockquote>

Your site should now look like this:
<img src="{{ "/assets/images/bootstrap/ex-bootstrap-veggies-jumbotron.png" | prepend:site.baseurl }}" alt="Screenshot of Ms B's Veggies with Jumbotron.">


### Add the Navbar
Refer back to the [Navbar](http://getbootstrap.com/components/#navbar) documentation to add a fixed Navbar that looks like this:
<img src="{{ "/assets/images/bootstrap/ex-bootstrap-veggies-navbar.png" | prepend:site.baseurl }}"
    alt="Screenshot of the Navbar for Ms B's Veggies.">

The *brand* link, "Ms. B's Veggies" should link to this Home page.  The other links can just go to "#" for the moment.  We may add more pages later, but we will not add them for this assignment.  

Note that the `navbar` class should be placed on a `<nav>` tag. Since the Navbar contains a `container`, it should be positioned before the Bootstrap container that we added earlier.

Check that the Navbar remains positioned at the top while you scroll.

Verify the mobile Navbar.  When collapsed, the Navbar should look like this when activated:
<img src="{{ "/assets/images/bootstrap/ex-bootstrap-veggies-navbar-collapsed.png" | prepend:site.baseurl }}" alt="Screenshot of Ms B's Veggies collapsed Navbar for mobile size." style="max-width: 50%;">


### Add the Footer
We will also add a fixed footer to the page.  This will be similar to the [Sticky Footer with Navbar](http://getbootstrap.com/examples/sticky-footer-navbar/) example.

Add a `<footer>` tag below our main Bootstrap container, just before the `<script>` tags.  Then in the footer, add a new div with the `container` class.  Add the footer text, "Copyright &copy; 2015 Ms. B's Veggies", inside this div.

Your page should now look like as follows.
<img src="{{ "/assets/images/bootstrap/ex-bootstrap-veggies-footer-no-css.png" | prepend:site.baseurl }}" alt="Screenshot of Ms B's Veggies footer before CSS is added.">
Notice the footer has no styling.  Unlike the Navbar, styles for the footer aren't part of the Bootstrap framework.  We'll need to add them ourselves, and we'll address that in part 2.
