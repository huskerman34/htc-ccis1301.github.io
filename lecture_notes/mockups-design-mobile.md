---
title:  "Mockups, Web Design & Mobile"
---

## Web Design Roles
In industry there web development is often split into two groups:  the designers & the developers.  The distinctions between the groups can often be blurred, with some people filling both roles, but it is common (especially with larger, commercial projects) to have both roles addressed separately.  On smaller projects however, it is not uncommon for one person to fill both roles, or to have the design tasks distributed throughout the team.

Web Designers, are often graphic designers who work with digital media.  They usually consider themselves as artists and are the creative inspiration behind the vision of the web site. They may also have an understanding of web specific issues, such as site usability, accessibility and responsive design, but this is not always the case. They to will often use wireframe tools to sketch out the design of a website, then use an art/design tool such as Photoshop, to paint a view of the website to *sell* that design concept to a customer.

User Experience Designers focus on how people interface with and interact with the web site. They  focus more strongly on site usability, navigation and site organization. They also have a good understanding of accessibility issues and considerations.They will often study how people use the site, perhaps presenting something one way to one group, and a different way to another to see which option gets the desired result.

Web Developers focus more on the technical skills and the building of the website with HTML, CSS, and JavaScript, and potentially other "back-end" programming languages such as Java, .Net, PHP or Python. They tend to work on larger interactive websites or web applications that store and present data and support business processes. They often have responsibilities for developing both the web user interface, as well as the back-end data systems. They may also work with various web content management systems to publish and maintain content.

In reality while there may be separate *ideal* roles, often these responsibilities are blended and blurred across a team.  Some people may do more artistic design, some may focus more on usability, others may focus more on writing the code.  But generally everyone has some expertise in one area, but some basic ability or knowledge of all. The smaller the project, the more roles one person must fill.

## Wireframes & Mockups
Generally the initial discussions of web site design results in the creation of a simple sketch of the layout. This is often a simple black and white line drawing on paper. At this phase, many changes occur to the design, and the design is usually evolving too rapidly to vest much time into details. A very simple wireframe example is shown in your textbook for the case study layouts. (See Figure 7.40 on page 241 for an example.)

As more information and details of the design are discussed and determined, these wireframes are refined into a more detailed mockup that shows a clearer picture of what the site will look like. There is a lot of variety in what people consider a mockup. This can include everything from a more detailed sketch on paper to a highly detailed Photoshop image of what the final site will look like.

Mockups are also used to communicate design choices for colors. Even pencil sketch mockups will usually include information on the colors to be used for the site. Clients tend to care greatly about the color scheme selected, as it is usually is tied into branding and has a large impact on the feel of the site.

Regardless of the level of detail, it is important that the customer can look at the wireframe or mockup and immediately understand the design. The basic layout of key pieces of content and functionality should be clear even in the most basic wireframe. Clear communication of the design and intent is key to customer satisfaction.

### Tools
While design can be done with paper, there are many tools available to support the wireframe and mockup design process.  

- [25 Free Mockup and Wireframe Tools for Web Designers](http://codecondo.com/free-wireframe-tools/)
- [Mashable: 9 Excellent Tools for Design Mockups](http://mashable.com/2012/06/07/mockup-tools/#NFXeCEzg_Sqn).

## Mobile First Design
A hot topic recently is the notion of designing for mobile devices first. Until recently, the focus for web designers was the presentation of the web site on a computer monitor. As the spread of smart phones and mobile devices with internet access grew, people began to consider how websites might be viewed on these smaller devices, but that was historically secondary to the desktop view.

Today, the mobile phone is increasingly the main (or in some parts of the world only) way people access the internet. Some people do not have access to a desktop or laptop computer at all, but do have and use a smart phone to access the web.  This growing trend to use a mobile device as the primary path to access the internet is resulting in a shift to focus on designing <em>first</em> for mobile devices and then secondarily enhancing that design for larger displays.

In this session, we will begin to explore responsive design which allows a website to flex and change its display based on the available display size. We will first learn how to implement this type of responsive design using media queries. Later in the semester we will explore a web framework that provides a library of CSS styles to manage the responsive layout for us.

Responsive websites are only one way to design and target a site for mobile device users. It is also possible to build an independent web site that mobile users are directed to, based on information sent about the client that is included in the web page request. A mobile phone apps might also be developed for mobile users, replacing the need for them to view a website through the device's web browser.

Responsive sites have the advantage of keeping everything in one place. There is only one copy of the web site that adjusts to various device sizes.  However, designing a responsive site can pose challenges as well, and might result in design compromises that would not have to be made for a mobile only site or a mobile application.

In the textbook, the examples show desktop first development, where the CSS is first written for a desktop display and then altered using media queries for tablet and mobile.  An alternate approach is to design the CSS "mobile first" for the display on smaller devices and then use media queries to alter that display for larger devices.  Both approaches are supported by the CSS media queries, so be careful to look at the screen sizes that the media queries apply to.  Don't just assume that the CSS that is not inside a media query must be for the desktop display of a site.

## Single Page Design
A current trend is a single page design, where a single page is sectioned by content into <em>slide</em> or flip-book like areas that you scroll down to.  There is also generally a navigation tool that allows you to quickly move between sections.  This is often used for a main landing page for the site and there may be links to other pages found within that content or in the footer.  This style is often used with mobile first design and sometimes includes "optional" items to fill side space on larger displays.

#### Example 1 - The home page for [Heroku](https://www.heroku.com/)

This site has typical navigation along the top, but the layout of the homepage frames each section to be visually separate as you scroll down the page.

  <img src="{{ "/assets/images/ch3/design-heroku1.png" | prepend: site.baseurl }}" alt="Screen capture of the Tumblr welcome page." />

Scrolling down makes me think of *streaming* content.  It flows from one section to the next, often aided with small animations.

  <img src="{{ "/assets/images/ch3/design-heroku3.png" | prepend: site.baseurl }}" alt="Screen capture of the third section of the Heroku page, obtained by scrolling further down." />

#### Example 2 - The welcome page for [Tumblr](https://www.tumblr.com/)

Notice the typical banner and navigation are missing from the top of the page.

  <img src="{{ "/assets/images/ch3/design-tumblr1.png" | prepend: site.baseurl }}" alt="Screen capture of the Tumblr welcome page." />

Scrolling down is like flipping a page.  Notice the dots down the left side that indicate where you are, and can be clicked to move forward and back.  

  <img src="{{ "/assets/images/ch3/design-tumblr2.png" | prepend: site.baseurl }}" alt="Screen capture of the next Tumblr page, obtained by scrolling down." />
