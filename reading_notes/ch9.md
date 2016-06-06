---
title:  "Chapter 9: Table Basics"
layout: notes
---

## Using Tables
Tables are a common feature on web pages.  Tables can organize information, making it easier to read and understand.  With the addition of some JavaScript (not covered in this course), the data can also sorted and filtered.  This can allow data that was once printed and distributed as reports, or emailed out in spreadsheets to be accessible on the web any time and anywhere.  

### Basic Table Structure
<div class="alert alert-warning" role="alert">
:warning: The example tables below are styled with the CSS for this site, so they will look different without CSS applied.
</div>

A basic table `<table>` is just made of rows `<tr>` and cells `<td>` (which make up the columns).

<code class="gist" data-gist="5785c6e9534e956b79d7" data-gist-file="basicTable.html">
</code>

That produces a table that is structured like this:
<table>
    <tr>
        <td>Row 1, Column 1</td><td>Row 1, Column 2</td><td>Row 1, Column 3</td>
    </tr>
    <tr>
        <td>Row 2, Column 1</td><td>Row 2, Column 2</td><td>Row 2, Column 3</td>
    </tr>
    <tr>
        <td>Row 3, Column 1</td><td>Row 3, Column 2</td><td>Row 3, Column 3</td>
    </tr>
</table>


### Table with Headings and Caption

To make the table a little fancier, you can also add headings and a caption or title.

<code class="gist" data-gist="5785c6e9534e956b79d7" data-gist-file="basicTable2.html">
</code>


That produces a table that is structured like this:
<table>
    <caption>Basic Table with Headings</caption>
    <tr>
        <th>Heading 1</th><th>Heading 2</th><th>Heading 3</th>
    </tr>
    <tr>
        <td>Row 1, Column 1</td><td>Row 1, Column 2</td><td>Row 1, Column 3</td>
    </tr>
    <tr>
        <td>Row 2, Column 1</td><td>Row 2, Column 2</td><td>Row 2, Column 3</td>
    </tr>
    <tr>
        <td>Row 3, Column 1</td><td>Row 3, Column 2</td><td>Row 3, Column 3</td>
    </tr>
</table>


### Spanning Rows & Columns
It's not uncommon to want a row or column to take up the space of more than one *cell*.  This can improve the table display when there are things like grouped rows or columns. This is not something used for evey table, but it is important to know that you *can* do this. 

### Accessibility
Make sure to use the `id` and `headers` attributes in your tables to support accessibility. Remember that it is your job to know that you need to include these pieces to make your pages accessible. Don't wait for someone to tell you to do it.