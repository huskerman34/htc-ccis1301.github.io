---
title: Ms B's Veggies Part 2

---

To wrap up the Ms B's Veggies site, we'll customize the CSS to make the site look more unique.
Your site should currently look like this:
<img src="{{ "/assets/images/bootstrap/ex-bootstrap-veggies-footer-no-css.png" | prepend:site.baseurl }}" alt="Screenshot of Ms B's Veggies footer before CSS is added.">

In this part, we'll add custom CSS so that in the end it'll look like this:
<img src="{{ "/assets/images/bootstrap/ex-bootstrap-veggies-styles-final.png" | prepend:site.baseurl }}" alt="Screenshot of Ms B's completed website made with Bootstrap.">

## GitHub
The project is found on the HTC CCIS 1301 organization on GitHub [veggies-bootstrap repository](https://github.com/htc-ccis1301/veggies-bootstrap).  

You do not need to fork the repository again. Continue working with the files you had from part 1.


#### Add a Custom Stylesheet
Create a new styles.css file for the project, and add it to the Home page after the Bootstrap stylesheet.  Order is important as we will want to customize (override) some of the default Bootstrap styles to get our final version of the site.

In the stylesheet file, add the following:

{% highlight css %}
html {
   /* Needed to fix footer at bottom of browser */
   position: relative;
   min-height: 100%;
}

body {
   /* Move down content because of fixed navbar at top */
   padding-top: 50px;
   /* Set margin bottom allow for footer height */
   margin-bottom: 50px;
}

footer {
   position: fixed;
   bottom: 0;
   height: 50px;
   width: 100%;
   background-color: #222222;
   color: #9d9d9d;
   text-align: center;
   padding: 15px;
}
{% endhighlight %}

The `background-color` and `color` in the footer are set to match the Navbar, and the `width` and `height` properties match the width and height of the Navbar.  The `padding` and `text-align` are just to make it look good.  The other styles (first 2) are the ones that - along with the html styles at the top - are responsible for fixing the footer to the bottom of the page.

Your page should now look like as follows.  As you scroll both the Navbar and footer should remain on the page.
<img src="{{ "/assets/images/bootstrap/ex-bootstrap-veggies-footer-css.png" | prepend:site.baseurl }}" alt="Screenshot of Ms B's Veggies footer after CSS is added.">

## Final Cleanup
To wrap up our site, let's give it a more friendly and homey look and feel.  Ms. B loves minty green and purple, so we've got a color scheme worked up just for her from the [Paletton](http://paletton.com/palette.php?uid=32S0u0kcglL4Zvw8Eq6eXhmkwen) website.  We'll use this and the fancy tartan background image (generated from the Paletton site) to transform this into a site even Benji will love.

### Customize the CSS
Update the stylesheet to:

1. Add the background image to the body, and set a fall back background-color of #A2C0A7.
2. In the html file, give our "main" Bootstrap container div the id of "main" so that we can custom style it.
3. Add css to style the "main" div with the background-color of #FBE7D4, bottom padding of 25px, and round the bottom borders only with a radius of 6px.
4. Add spacing below each `row` in our main div by adding bottom margin of 15px.
5. Adjust the color on the footer to be #CEAEBF and the background-color to #5E2241.
6. For `.navbar-inverse`, set both the background-color and border-color to #5E2241.
7. For `.navbar-inverse .navbar-brand`, set the color to #CEAEBF.
8. For `.navbar-inverse .btn`, set the background-color to #CEAEBF and the color to #5E2241.

Your site should now look like this:
<img src="{{ "/assets/images/bootstrap/ex-bootstrap-veggies-styles1.png" | prepend:site.baseurl }}"
   alt="Screenshot of Ms B's Veggies with updated styles.">

### Customize the Jumbotron
Overall things look pretty good, but let's wrap up by updating that Jumbotron.  Add the following styles for the Jumbotron:

- a top margin of 15px
- set bottom padding to 25px
- set the text color to black and center align the text
- add a drop shadow on the text using the color #FBE7D4, for sizing use 3px horizontal, 3px vertical, and 4px blur
- add the 'veggies-background' background image, have it cover the container and clip on the border

Some of the text is still a little hard to read.

- change the color of the jumbotron `small` text to #1F5829
- change the font size on the jumbotron paragraphs to be 1.3em and make the text bold

With the jumbotron updates, our final site should look like this:
<img src="{{ "/assets/images/bootstrap/ex-bootstrap-veggies-styles-final.png" | prepend:site.baseurl }}"
   alt="Screenshot of Ms B's Veggies with updated styles for jumbotron.">
