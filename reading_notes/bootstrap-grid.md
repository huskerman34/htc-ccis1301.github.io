---
title: Bootstrap Grid Basics
---
Bootstrap's responsive [Grid System](http://getbootstrap.com/css/#grid) is one of its best features.  The grid allows you to layout your content in rows of up to 12 columns.  These columns can vary in size from 1 column width to 12 columns widths.  The grid utilizes CSS style classes to allow you to control the layout and positioning for various display sizes.

The key thing you need to know to use the grid is that you specify how many of the 12 columns you want your information to span.  Don't think of this as a table where each bit of data goes into one column and you have 12 of them.  These columns are meant to be spanned and their width will vary based on the display size.

Look at the demo [Grid Example Basics](http://getbootstrap.com/css/#grid-example-basic) and adjust the width of your display, noticing how the columns shift based on the display width.  

<div class="alert alert-warning" role="alert">
:warning: Pay attention to how the device sizes correspond to the <a href="http://getbootstrap.com/css/#grid-media-queries">grid class media queries</a>.  A <em>medium</em> device is a desktop, while a <em>large</em> device is a desktop with a larger display.  A <em>small</em> device is tablet sized, while a phone is considered <em>extra small</em>.  
</div>

## Mobile First
If you do not specify a specific `col-xs-*` class, then on a mobile device (or a device up to the size of the class you do specify) that column will use the full display width.  The other columns will stack underneath.  If this is the behavior you want for a mobile (or xs) device, then you do not need to add a `col-xs-*` class for your column.  

As you start to consider the larger displays, you can then decide when (at what device size) you want more than one column in a row.  Then  add the appropriate class specifying the size and number of columns to span.  You can add more than one class to a column to change the display for different device sizes.  For example if you have three columns, and they should be stacked on mobile, two per row on tablet, and 3 per row on desktop, you could have the following:

{% highlight html %}
<div class="container">
  <div class="row">
    <div class="col-sm-6 col-md-4"> Col 1 </div>
    <div class="col-sm-6 col-md-4"> Col 2 </div>
    <div class="col-sm-6 col-md-4"> Col 3 </div>
    <div class="col-sm-6 col-md-4"> Col 1 </div>
    <div class="col-sm-6 col-md-4"> Col 2 </div>
    <div class="col-sm-6 col-md-4"> Col 3 </div>
  </div>
</div>
{% endhighlight %}

## Rows and Wrapping
Note that in the previous example the columns were all set up in one row.  That means the one row had more than 12 columns in width.  When this happens, the columns will wrap onto the next row.  For the example above, this means that:

 - on a mobile device I would see all 6 columns stacked taking up the full display width
 - on a tablet device I would see __three__ rows of two columns side by side
 - on a desktop device I would see __two__ rows of three columns side by side

 Try this out on a simple page and play around with it until you are comfortable with how it works.  Then notice how the code below behaves differently as the columns are separated into two rows.

{% highlight html %}
<div class="container">
  <div class="row">
    <div class="col-sm-6 col-md-4"> Col 1 </div>
    <div class="col-sm-6 col-md-4"> Col 2 </div>
    <div class="col-sm-6 col-md-4"> Col 3 </div>
  </div>
  <div class="row">
    <div class="col-sm-6 col-md-4"> Col 1 </div>
    <div class="col-sm-6 col-md-4"> Col 2 </div>
    <div class="col-sm-6 col-md-4"> Col 3 </div>
  </div>
</div>
{% endhighlight %}

For this example, with two separate rows:

- on a mobile device I would see all 6 columns stacked taking up the full display width
- on a tablet device I would see __four__ rows, the first and third with two columns side by side, the second and fourth with one
- on a desktop device I would see __two__ rows of three columns side by side

## Column Ordering
The last thing I want to call out about the table is one of the most awesome features, modifying the [column ordering](http://getbootstrap.com/css/#grid-column-ordering).  The push and pull modifier classes can be used to shuffle columns around for different display sizes.  This is great when focusing on not just shrinking content for mobile, but ensuring that it is displayed appropriately based on importance.

For example, let's imagine that I've got a main paragraph of crucial information that I obviously want right in front of my mobile users.  But I'd also like to have two smaller ads or images (less important information) follow one on top of the other on mobile, but on tablet where there is a little more width I want them to follow but be side-by-side in one row.  Then when there is even more width on a desktop, I want to have a 3-column layout where these ads/images flank the main content one on each side.  

I really don't want to try to write those media queries myself, but with Bootstrap this is simple to set up.  Check out the demo code below and make sure that you understand how it is working.

{% highlight html %}
<div class="container">
  <div class="row">
    <div class="col-sm-12 col-md-push-3 col-md-6">
      <b>Crucial information</b>
    </div>
    <div class="col-sm-6 col-md-pull-6 col-md-3">
      Not important 1
    </div>
    <div class="col-sm-6 col-md-3">
      Not important 2
    </div>
  </div>
</div>
{% endhighlight %}
