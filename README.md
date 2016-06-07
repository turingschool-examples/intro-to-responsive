---
title: Responsive Web Design and Media Queries
length:
tags: front-end
---

### Goals

By the end of this lesson, you will:

* have an understanding of the history of responsive web design
* be familiar with the various types of media queries and page layouts and how to use them
* have the skills and understanding to implement media queries and add breakpoints effectively and as needed and feel confident that you understand how to control how your site looks on every screen size.

### Structure

We can't control how our users interact with our products, but we *can* make sure that our work looks good and functions correctly on all screen sizes.

A general understanding of responsive website design and how to use media queries and when to add breakpoints so your page layout resizes nicely is a great skill to have in your toolbelt.

#### Overview

In this session, we'll be diving into responsive page layouts and using media queries to control your page content at all screen sizes.

#### History of Responsive Layouts

Responsive web design is a strategy for building websites that work on all devices and screen sizes. In the not so distant past, the standard was to build sites for desktop or laptop screen resolutions. The introduction of smart phones turned this approach on its head, and designers were faced with a whole new set of challenges. In May 2010, Ethan Marcotte outlined an approach called [Responsive Web Design](http://alistapart.com/article/responsive-web-design/) that would become the gold standard in how to handle designing for such a large range of screen sizes and devices.

In a nutshell, this approach uses relative units to set the width and size of the page contents combined with specific breakpoints in the CSS that set styles based on the dimensions of the screen.

There are four primary page layout types:

###### Static Page Layout
A static layout is fixed width and sits in the center of the screen -- it is the traditional web layout. It works on one screen size and one screen size only. It will fail on screens any amount smaller or larger than the original design.

###### Liquid Page Layout
A liquid (also called 'fluid') page layout uses relative units instead of fixed units (think percentages instead of pixels).

Liquid layouts fill the whole page, regardless of the screen or browser width. It's an approach that doesn't take as much thought and planning as other techniques, making it quick and easy to implement. However, this ease of implementation comes with major disadvantages. These layouts fail at screen sizes significantly larger or smaller than the original design.

###### Adaptive Page Layout
An adaptive layout uses CSS media queries to detect the width of the browser and make layout adjustments accordingly. Unlike liquid layouts, adaptive layouts use fixed units like pixels to define widths. They behave like a series of static layouts defined by specific media queries.

Because adaptive layouts typically take less time to build than true responsive layouts, they are a great option for quickly updating an existing static layout to make it compatiable with mobile devices.

The primary drawback to this strategy is that screen widths that fall between the set breakpoints can feel awkward, with contents looking either too crowded or with far too much space.

###### Responsive Page Layout
At first glance, a response site looks a lot like an adaptive site. But start resizing your screen, and you'll see why it's the best solution. A true responsive page layout combines the best parts of a liquid layout and an adaptive layout to create the best experience for your users as they move between devices and screen sizes. By using both relative units and media queries, a responsive site allows us to transition through screen sizes seamlessly and effortlessly.

The site (Liquidapsive)[http://www.liquidapsive.com/] is a great resource showing simple examples of these layout types in action.


#### Using Media Queries

We know we want to build a site that works well on a variety of screen sizes, but we keep talking about "media queries" and "setting breakpoints". What does that mean?

**Media queries** are a Boolean chunk of logic that lives in your CSS, and when you write a series of media queries you are creating a very basic algorithm. They control at what screen size specific styles will be applied.

The W3C recognizes (several different media types)[https://www.w3.org/TR/CSS2/media.html#media-types], but for our purposes we'll primiarly use ``screen``. This indicates that the media query is intended for computer screens.

Other media types that can come in handy include ``print``, which adjusts styles for screened documents that are being printed, and ``handheld``, which is indended for handheld devices. There are also media types that focus on accessiblity by providing tactile braille feedback or working with speech synthesizers.

**Break points** are the pixel widths the media queries reference. When the media query is true (i.e. when the screen size matches what is specified by the break point), the styles specified in that media query will be applied.

If you want a much deeper dive into the how's and why's behind media queries, (Smashing Magazine)[https://www.smashingmagazine.com/2014/07/breakpoints-and-the-future-websites/] has an old, but good, article on the topic.

#### Guided Practice (We do)
#### Putting it into Practice

Let's try this out! We'll build a one-page site made up of layout elements that don't play all that nicely on all screen sizes. We'll have to consider how we want them to look on small, medium, and large screens and add the appropriate media queries and breakpoints so the layout adjusts appropriately.

To get started, we'll set up our HTML skeleton so we have a roadmap of where we're heading with the page before we start adding styles.

```html
<!doctype html>
<html>
<head>
    <title></title>
</head>
<body>

</body>
</html>
```

Now that we have our basic HTML page structure written, we can think about how we want to structure the cotents. We know we want to have nav main content, some secondary content in a sidebar on the right side of the screen, and a footer so we'll go ahead and add the appropriate tags for those chunks of content.

Working in index.html, let's start at the top and work our way down the page. For our primary navigation, we'll use the semantic ``header`` tag to wrap a ``nav`` tag that contains the unordered list that will become our navigation links.

```html
<body>
    <header>
        <nav>
            <ul>
                <li></li>
            </ul>
        </nav>
    </header>
</body>
```

Next, we'll add an ``article`` tag to hold the main content, and an ``aside`` to hold our secondary content.

```html
<body>
    <header>
        <nav>
            <ul>
                <li></li>
            </ul>
        </nav>
    </header>
    <article></article>
    <aside></aside>
</body>
```

All that's left now is the ``footer``, and we have a basic roadmap of how we want to structure our content.

```html
<body>
    <header>
        <nav>
            <ul>
                <li></li>
            </ul>
        </nav>
    </header>
    <article></article>
    <aside></aside>
    <footer></footer>
</body>
```

Starting our page this way helps us think through our layout which helps us keep our styles clean and organized.









### Slides

* [Link to optional slides]()

### Video

* [Link to optional video]()

### Repository

* [Link to optional repo]()

### Outside Resources / Further Reading

* [Link to first outside resource]()
