---
title: "Bootstrap Tutorial: Learn Bootstrap 5 in 10 minutes"
subtitle: "After decades of struggling, the light has arrived!! With this Bootstrap tutorial, designing a website will be a piece of cake. It's almost stupid, and, also impossible to think about doing a website without a CSS framework like Bootstrap 5."
cover_local: "https://github.com/breatheco-de/content/blob/master/src/content/lesson/../../assets/images/4cc6fa0b-2530-4052-aa7e-8dac03788ac3.png?raw=true"
textColor: "white"
date: "2020-10-19T16:36:30+00:00"
tags: ["bootstrap", "html-and-css"]
status: "published"

---

## Bootstrap fixed all CSS major problems

There is light at the end of the tunnel, and it is NOT Chuck Norris holding a flashlight.  Finally, someone fixed CSS.  This is a library made by [Mark Otto](https://twitter.com/mdo) and [Jacob Thornton](https://twitter.com/fat) – normal people – developers like you and me, and they did great!

These two guys working on Twitter were suffering the same problems we have been dealing with in HTML and CSS.  Fed up with the situation, they decided to build a **base CSS Sheet designed to be imported into any website**.  It makes every front-end development work 4x’s easier.

![bootstrap 5](https://github.com/breatheco-de/content/blob/master/src/content/lesson/../../assets/images/335ed387-cbf9-4ffa-9529-1ccf2084e393.jpeg?raw=true)

Besides, Bootstrap gives you a dozen of new elements that you would normally want to use but don’t actually exist in CSS+HTML: The Bootstrap components.

## Layouts: Solving the Box Model


One of the broken things in CSS is the way that layouts work – working with **float**, **display** and **position** sucks.  This is how Bootstrap solved it:

## Everything is now divided into Rows and Columns.

Bootstrap creators replicated the same concept that `<table>` had, but instead of using tables, they used `<div>` (boxed containers). They can’t create their own HTML tags because that will require a new HTML version and would make Bootstrap incompatible with current browsers. Tags must stay the same, that's why they decided to override the `<div>` default behaviors with classes.

```html
This is a row: <div class="row">
This is a column: <div class="col–sm–x">
```
![bootstrap tutorial](https://github.com/breatheco-de/content/blob/master/src/content/lesson/../../assets/images/3884f515-dd7a-48f2-b238-9e2ec26de02d.png?raw=true)

Bootstrap has divided the screen's width into `12 slots` – each of them with 8.33% of the total width of the row.  The size of 1 column, can be between 1 and 12 slots.

On the flip side, columns were made to live within the rows (just like what happens between `<td>` and `<tr>`).   You always need to open a row before opening a column.  All columns in a row must always add up to a maximum of 12 slots.

![bootstrap tutorial](https://github.com/breatheco-de/content/blob/master/src/content/lesson/../../assets/images/1b7f5dc4-029a-475d-8bfd-fac1b739966c.png?raw=true)

## Our first Layout example:

Just like we did in the Layout chapter of the course, let’s create one page with 2 big sections: one sidebar on the right and one main content on the left.

<iframe width="100%" height="300" src="//jsfiddle.net/BreatheCode/th7uLrow/6/embedded/html,css,result/" allowfullscreen="allowfullscreen" allowpaymentrequest frameborder="0"></iframe>

<div align="right"><small><a href="//jsfiddle.net/BreatheCode/th7uLrow/6/embedded/html,css,result/">Click here to open demo in a new window</a></small></div>

## Bootstrap is 100% Responsive

It’s very easy to decide how your website will render in different screen sizes; when you add each column into the rows you need to assign a class with the following format:

```html
<div class="col–md–x">
```

|**Col**   |**md**   |**x**
|:---------|:--------|:----|
|Means that this element should behave like a Bootstrap column.   |Means that it is specified only for the devices with a "medium" sized screen.   |Specifies how many slots I want this column to take (remember you can take a max of 12 slots per row).   |


Bootstrap device sizes:   

|Phones   |Big-phone/small-tablet   |Tablets   |Desktops   |Extra-large desktops   |Extra extra large   |
|:----------|:---------------|:-------------|:-----------|:------------|:---------|
| Nothing    |sm       |md       |lg      |xl        |xxl      |

>👆 Note: if you don’t specify the screen size (ex. by using 'sm', 'md', or 'xl'), the website will be rendered for mobile phones by default.

## Defining Mobile, Tablet, and Desktop at the same time

We are going to set the layout (using the sm, md, and lg column classes) for  two rows in all the devices at the same time:

![bootstrap 5 columns example](https://github.com/breatheco-de/content/blob/master/src/content/lesson/../../assets/images/e15c594c-9b46-4c27-bf5a-a5bbb5ef952a.png?raw=true)

```html
<!-- Stack the columns on mobile by making one full-width and the other half-width --> 
<div class="row">
  <div class="col-12 col-md-8">.col-12 .col-md-8</div>
  <div class="col-6 col-md-4">.col-6 .col-md-4</div>
</div>

<!-- Columns start at 50% wide on mobile and bump up to 33.3% wide on desktop --> 
<div class="row">
  <div class="col-6 col-md-4">.col-6 .col-md-4</div>
  <div class="col-6 col-md-4">.col-6 .col-md-4</div>
  <div class="col-6 col-md-4">.col-6 .col-md-4</div>
</div>

<!-- Columns are always 50% wide, on mobile and desktop --> 
<div class="row">
  <div class="col-6">.col-6</div>
  <div class="col-6">.col-6</div>
</div>
```

## Basic Bootstrap 5 Skeleton

We already know the basic HTML5 skeleton that any website needs to have.  Now you just have to add a few lines in your skeleton to make it "Bootstrap compatible":

```html
<!doctype html>
<html lang="en">
  <head>
    <!-- Required meta tags -->
    <meta charset="utf-8">
    <meta name="viewport" content="width=device-width, initial-scale=1, shrink-to-fit=no">

    <!-- Bootstrap CSS -->
    <link href="https://cdn.jsdelivr.net/npm/bootstrap@5.2.1/dist/css/bootstrap.min.css" rel="stylesheet" integrity="sha384-iYQeCzEYFbKjA/T2uDLTpkwGzCiq6soy8tYaI1GyVh/UjpbCx/TYkiZhlZB6+fzT" crossorigin="anonymous">


    <title>Hello, world!</title>
  </head>
  <body>
    <h1>Hello, world!</h1>

    <!-- Optional JavaScript -->
    <!-- Popper.js, then Bootstrap JS -->
    <script src="https://cdn.jsdelivr.net/npm/@popperjs/core@2.11.6/dist/umd/popper.min.js" integrity="sha384-oBqDVmMz9ATKxIep9tiCxS/Z9fNfEXiDAYTujMAeBAsjFuCZSmKbSSUnQlmh/jp3" crossorigin="anonymous"></script>
    <script src="https://cdn.jsdelivr.net/npm/bootstrap@5.2.1/dist/js/bootstrap.min.js" integrity="sha384-7VPbUDkoPSGFnVtYi0QogXtr74QeVeeIs99Qfg5YCF+TidwNdjvaKZX19NZ/e6oz" crossorigin="anonymous"></script>

  </body>
</html>
```

Remember, Bootstrap is just a stylesheet.  That’s why it is very simple to include in your website.  You use the `<link>` tag to include the styles, and, optionally, use the JavaScript `<script>` tag to include the Bootstrap JavaScript files.

The Bootstrap JavaScript functionality requires the Popper JavaScript library to be included first.  You don’t need to know the details about this yet.  Just include the JS libraries using the script tag and later you will understand.

> 🔗 Here you can find the [Bootstrap documentation to get you started.](https://getbootstrap.com/docs/5.2/getting-started/introduction/)

## Bootstrap 5 Components

HTML is so basic that it only has a few tags – we know that already.  But when you browse the web today you see a different thing: websites today have menus, icons, load-bars, navbars, labels, etc.  Where are those tags?  None of those tags are defined in HTML!

Every developer has to fake these additional elements every time they create a new website.  They have to do everything from scratch, and it takes a lot of time.

When you import Bootstrap into your website, you will have a new set of components at your disposal.  This is just a small part of those elements:

![bootstrap 5 components](https://github.com/breatheco-de/content/blob/master/src/content/lesson/../../assets/images/8e9ff37a-28f7-4179-8f5d-9278ff7efd55.png?raw=true)


### These are the most important and Used Components in this Bootstrap tutorial:

#### The NavBar

This is so popular that it’s on the menu of 99% of all websites.  It normally has the logo of the company and a series of links – depending on each website’s business logic.

Here is an example of how a NavBar may look on a website:

![bootstrap 5 navbar](https://github.com/breatheco-de/content/blob/master/src/content/lesson/../../assets/images/6351de1c-6d90-4502-8823-4b751981db9f.png?raw=true)

> 🔗 [**Read more about the NavBar here**](https://getbootstrap.com/docs/5.2/components/navbar/)

```html
<nav class="navbar navbar-expand-lg bg-light">
    <div class="container">
        <a class="navbar-brand d-flex align-items-center gap-1" href="#">
            <i class="fa-brands fa-instagram"></i>
            <span>Instagram</span>
        </a>
        <button class="navbar-toggler" type="button" data-toggle="collapse" data-target="#navbarNavDropdown"
            aria-controls="navbarNavDropdown" aria-expanded="false" aria-label="Toggle navigation">
            <span class="navbar-toggler-icon"></span>
        </button>
        <div class="collapse navbar-collapse justify-content-end" id="navbarNavDropdown">
            <ul class="navbar-nav align-items-center">
                <li class="nav-item active">
                    <a class="nav-link" href="#">
                        <span class="btn btn-success">
                            Create a new post
                        </span>
                    </a>
                </li>
                <li class="nav-item dropdown">
                    <a class="nav-link dropdown-toggle" href="#" id="navbarDropdownMenuLink"
                        data-bs-toggle="dropdown" aria-haspopup="true" aria-expanded="false">
                        Menu
                    </a>
                    <div class="dropdown-menu" aria-labelledby="navbarDropdownMenuLink">
                        <a class="dropdown-item" href="#">Action</a>
                        <a class="dropdown-item" href="#">Another action</a>
                        <a class="dropdown-item" href="#">Something else here</a>
                    </div>
                </li>
            </ul>
        </div>
    </div>
</nav>
```

#### The Card

This is probably the most used Bootstrap component, every website has a few cards because they are ideal for listing items in a beautiful way. Some examples of the Card used can be:

+ The "team" section of a website, where you list the different employees.
+ The typical Pinterest wall.
+ The feed in any social media like Instagram, Facebook, Twitter, etc.

Here is an example of how "The Card" may look on a website:

![bootstrap 5 cards](https://github.com/breatheco-de/content/blob/master/src/content/lesson/../../assets/images/39d36b52-330f-4ce9-beab-2004e325749c.png?raw=true)

> 🔗 [**Read more about the card here**](https://getbootstrap.com/docs/5.2/components/card/)

```html
<div class="card" style="width: 18rem;">
  <img src="..." class="card-img-top" alt="...">
  <div class="card-body">
    <h5 class="card-title">Card title</h5>
    <p class="card-text">
      Some quick example text to build on the card title and make up the bulk of the card's content.
    </p>
    <a href="#" class="btn btn-primary">Go somewhere</a>
  </div>
</div>
```


#### The Modal

Everyone hates a modal. It's super annoying, always asking you to subscribe to a newsletter! 🙂

Here is how a modal looks by default on Bootstrap.

![bootstrap 5 modal](https://github.com/breatheco-de/content/blob/master/src/content/lesson/../../assets/images/6bcba673-a543-4bf1-a80b-083914b91bef.png?raw=true)

>  🔗 [**Read more about modal here**](https://getbootstrap.com/docs/5.2/components/modal/)

```html
<div class="modal" tabindex="-1">
  <div class="modal-dialog">
    <div class="modal-content">
      <div class="modal-header">
        <h5 class="modal-title">Modal title</h5>
        <button type="button" class="btn-close" data-bs-dismiss="modal" aria-label="Close"></button>
      </div>
      <div class="modal-body">
        <p>Modal body text goes here.</p>
      </div>
      <div class="modal-footer">
        <button type="button" class="btn btn-secondary" data-bs-dismiss="modal">Close</button>
        <button type="button" class="btn btn-primary">Save changes</button>
      </div>
    </div>
  </div>
</div>
```


> ☝️ Important! The Modal needs JavaScript in order to work. Remember to include the three JavaScript files that are needed in a typical Bootstrap Skeleton: JS, Popper, and Bootstrap.js

## What you really need to know about Bootstrap

The Bootstrap official documentation is amazing!  We don’t need to start copying and pasting all their posts.  Please visit the following and focus on reading these topics:

+ [The grid system.](https://getbootstrap.com/docs/5.2/layout/grid/)
+ [Styling Forms.](https://getbootstrap.com/docs/5.2/forms/overview/)
+ [List of components available to use on your website.](https://getbootstrap.com/docs/5.2/components/accordion/)
+ [Utilities or Helper classes:](https://getbootstrap.com/docs/5.2/utilities/background/) Very useful and constantly used classes to do stuff like centering the text, centering a column or container, adding a background, etc.

Bootstrap has many versions, always check if you are using the latest version of Bootstrap on your project, here you can find all the available versions: [https://getbootstrap.com/docs/versions/](https://getbootstrap.com/docs/versions/).


We recommend using a CDN to import bootstrap in your HTML like this one: [https://www.bootstrapcdn.com/](https://www.bootstrapcdn.com/)

If you are migrating your project to a newer Bootstrap version, remember to check its documentation.
