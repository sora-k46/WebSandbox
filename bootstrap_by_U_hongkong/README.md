# Full Stack Web Development Course By University of Hongkong

## What is Full Stack Developer?

Someone who works with the back end -- or server side -- of the application as well as front end, or client side

further reading:

- [What is a Full Stack developer?](https://www.laurencegellert.com/2012/08/what-is-a-full-stack-developer/)
- [Multitier architecture](https://en.wikipedia.org/wiki/Multitier_architecture)
    - (is a client–server architecture in which presentation, application processing and data management functions are physically separated. The most widespread use of multitier architecture is the three-tier architecture.)
- [What is 3-tier Architecture?](http://www.tonymarston.net/php-mysql/3-tier-architecture.html)

## Nodejs and NPM
- Nodejs is based on Javascript runtime built on Chrome V8 Javascript Engine to run on the desktop
- Built around event-driven, non-blocking I/O model

## Node Package Manager
- NPM is manager for node modules and packages
- A package contains:
    - JS files
    - package.json (manifest)

## package.json
- It serves as documentation for what packages your project depends on.
- It allows you to specify the versions of a package that your project can use using **semantic versioning rules**.
- Make your build reproducible, which means that its way easier to share with other developers.

## Creating package.json
- Use `npm init` to initialize a package.json

## Using npm to install package
- Use `npm install <package name> <options>`

    Example:
    `npm install lite-server --save-dev`

NOTE: --save-dev means we want to use this package in our development dependencies.

## Front-End Web UI Framework
- Collection of ready-to-use HTML, CSS and Javascript templates for UI components.

## Why  Front-End Web UI Framework?
- Responsive Design
    - Mobile first
- Cross-browser compatibility
    - Dealing with quirks of browsers
- Increased productivity
    - Easy to get started
- Community support
    - Resources and web page templates

## Foundation for Responsive Design
- Grid system
- Fluid images
- Media queries

## Bootstrap Grid
- !It's built with flexbox and is fully responsive.
- container class will automatically adapt itself for various viewport
```html
<div class="container">
```
- inside the container class the content will be layout as row
```html
<div class="container">
    <div class="row">
```
- in each row can be divided into 12 equally columns
```html
<div class="container">
    <div class="row">
        <div class="col">
        <div class="col">
        <div class="col">
        ...
        ...
        ...
```

### screen size class
- default targets all screen sizes
- `sm` for small >= 576px
- `md` for medium >= 768px
- `lg` for large >= 992px
- `xl` for extra large >= 1200px

Using screen size class
```html
<div class="col-xx-yy">
<!-- xx = screen size class -->
<!-- yy = no. column this div will occupied (optional) -->
<!-- bootstrap can automatically adjust col for you if the yy not specified -->
```

The `col` class can also be nested and still applied the 12 grid system

### Reordering the content

```html
<div class"col-sm-7 order-sm-first">
<div class"col-sm-5 order-sm-last">
```
#### Offsetting content
Can be done in 2 ways
- `offset` class
- margin utilities

With `offset`
```html
<div class="row">
  <div class="col-md-4">.col-md-4</div>
  <div class="col-md-4 offset-md-4">.col-md-4 .offset-md-4</div>
</div>
<div class="row">
  <div class="col-md-3 offset-md-3">.col-md-3 .offset-md-3</div>
  <div class="col-md-3 offset-md-3">.col-md-3 .offset-md-3</div>
</div>
<div class="row">
  <div class="col-md-6 offset-md-3">.col-md-6 .offset-md-3</div>
</div>
```

With margin
```html
<div class="row">
  <div class="col-md-4">.col-md-4</div>
  <div class="col-md-4 ml-auto">.col-md-4 .ml-auto</div>
</div>
<div class="row">
  <div class="col-md-3 ml-md-auto">.col-md-3 .ml-md-auto</div>
  <div class="col-md-3 ml-md-auto">.col-md-3 .ml-md-auto</div>
</div>
<div class="row">
  <div class="col-auto mr-auto">.col-auto .mr-auto</div>
  <div class="col-auto">.col-auto</div>
</div>
```
## Navigation bar
Contains links to various pages within the website
- Do(s)
    - Use simple, User friendly terms
    - Standardize navigation
    - Provide indication of the location within the navigation hierarchy
    - Use standard web conventions:
- Don't(s)
    - Have many items
    - Use generic labels

## Breadcrumbs
Secondary navigation
- Usually place below the primary navigation and above the content
- Indicator of the current page's location within a navigational hierarchy
    - Path based: set of steps
    - Location based: hierarchy
    - Attribute based: set of choices