# What is Responsive Web Design
- Designing the website with multiple screen size/resolutions in mind.
- Sites should work under any platform, any browser size, any orientation. The user should have the power.

# Concepts to consider
- Media Queries - detecting the viewport size
- Flexible grid-based layout for relative sizing
- Flexible images

# Responsive Options
- RWD - fluid measurements, flexible grids, and varying CSS rules
- Adaptive Design (dynamic serving) - returns one of multiple version of a page based on the type of devices
- Separate Mobile site (.m) - a separate page URL for the mobile site

# Fonts Responsive
- `px` (pixel) - fixed size
- `em` - An `em` is the equivalent of the size (in pixels) defined in the CSS rule font-size.
- percentage - relative to the its container
- `rem` (root em) - size relative to the root element (`<html>`)

### Ex. em 
#### HTML
```html
<body>
    <div class="parent">
        <div class="child">This is a paragraph</div>
    </div>
</body>
```
#### CSS
```css
.parent {
    font-size: 20px;
    /* 
        2em = 40px
        1em = 20px
        0.5em = 10px
        0.25em = 5px
    */
}

.child {
    font-size: 2em;
}

```

## How to use `em` and `rem` together
Each modules use `rem` to set font-size relative to the root element (`<html>`)
Then inside the module use the `em` to set the font-size relative to its parent.

```css

html {
    font-size: 20px;
}

.parent {
    font-size: 1rem;
    /* set the font size to be 20px (1rem) relative to the root */
}

.child {
    font-size: 0.5em;
    /* use the em (0.5 rem or 10px) to set the size relative to the parent */
}

```

Note: use [pxtoem.com](http://pxtoem.com/) to convert `px` to `em`

# Viewport Height and Width
- `vh` - viewport height
- `vw` - viewport width

# Media Queries
  
## 2 components of query
- A media type
    - screen, print, all, ...
- Actual query of a media feature and 'trigger' size
    - width, height, orientation, resolution, ...

#### Example
```css
screen and (max-device-width: 480px) and (resolution: 163dpi)
```

# Implement media queries
- use the @import rule
```css
@import url(smallstyle.css) screen and (min-width: 600px)
```
- Put media query directly in the style sheet (most use!)
```css
@media screen and (min-width: 500px) {...}
```
- Include query in the link
```html
<link rel="stylesheet" media="screen and (min-width: 400px) and (orientation: portrait)">
```

#### Examples
```css

@media screen and (min-width: 500px) {
    p.desc {
        display: block;
        font-size: 150%;
    }
}

@media screen and (min-width: 900px) {
    p.desc {
        display: inline-block;
        width: 35%;
        font-size: 125%;
    }
}

```

### breakpoints
- Breakpoints are sized that define a change in your site layout or content.
- Used to provide best possible experience for users based on device information.

# meta viewport
- The meta viewport tag tells mobile browser's viewport how to behave.
```html
<meta name="viewport" content="width=device-width, initial-scale=1">
```

# Framework
- make your job easier!

#### Front-end developers
- CSS, Javascript, jQuery

#### Back-end developers
- Routing, Resources, Security
