## Responsive Web Design with HTML5 and CSS3  :art:



### 🏁 Getting started with HTML5, CSS3 and Responsive Web Design 🏁



#### 1. Why smartphones are important

Nowadays, with smartphones capable of offering an enjoyable browsing experience, there is a greater difference between the measures of the smallest screens and the measures of the biggest screens. A responsive web design, built with HTML5 and CSS3, allows a website to look just the way it should look, in any screen size. Small screen devices' web browsers work by shrinking a standard website to fit the visible area (the **viewport**) of the device. To really see any part of the content, the user must zoom in on the area they are interested, which is tedious and frustrating, and moving the page left and right to see the rest of a sentence causes many "missclicks".



#### 2. Are there times when a responsive design isn't the right choice?

A true "mobile" version of a website could be a good option to show different content, design and interactions based on the device, and even use the device's technical capabilities (like the phone's GPS). However, most projects don't need that kind of sophistication, so providing a tailored view of the content depending on the size of the viewport should be the best option: for smaller screens highlighting important content, maybe even hiding less important content, altering buttons to accommodate finger presses, scaling typography to increase readability, etc..



#### 3. Defining responsive web design

**Responsive web design** is a unified approach that comprises three existing techniques: flexible grid layout, flexible images, and media and media queries. 



#### 4. Why stop at responsive design?

HTML5 offers more meaningful semantic elements and many CSS3 modules allow lean flexible graphics. 



#### 5. Examples of responsive web design

In responsive web design, pixels as a measurement unit aren't flexible enough. Instead, we should work with relative measurement units, typically "em"/"ems" and percentages. 

**Screen size** is the physical display area of a device. **Viewport** is the content area within the browser window, excluding toolbars, tabs, etc. 



#### 6. HTML5 - why it's so good

HTML5 offers sleeker and more focused syntax, which translates in, at least, some data saving so that our website can load faster. The new semantics of elements provide more meaningful code and HTML5 also enables feedback to the user, sometimes sparing the need to process with JavaScript (heavy). 

The first line of any document starts with the Doctype Declaration: <!DOCTYPE html>. Then, adding links to JavaScript or CSS is done with:  <script src="js/jquery-1.6.2.js"></script>. There is no need to specify the type of the link. HTML5 is case insensitive and allows some syntax variants such as omitting quotation marks, to make it easier for the developers (still not a good practice to do this, I assume).

 Common structural sections such as header and navigation get their own element tags. This improves the semantics of the code and helps search engines to understand and rank web pages better. 



#### 7. CSS3 enables responsive designs and more

**Cascading Style Sheets** (CSS) work as a way of separating design from content. CSS3 introduced more modern effects, such as the `border-radius` property or the `linear-gradient` property. This last one is not as well supported and might need to be repeated with some prefixes like `-moz-` for Mozilla Firefox. The prefix `-webkit-` allows different browser vendors to experiment on their own implementations.

 

#### 8. Look Ma' - no images!

Using CSS3 rather than JavaScript or Flash makes the animation lightweight, maintainable, and therefore perfect for a responsive design.



#### 9. Can HTML5 and CSS3 work for us today?

Does the client want to support the largest growing market of Internet users? Does the client want the cleanest, fastest, and most maintainable code base? Does the client understand that experience can and should be subtly different across different browsers? If so, responsive methodology is suitable.

  

#### 10. Responsive web design are not magic bullets

The specifics of a project (namely budget, target demographic, and purpose) should dictate the implementation. However, if the budget is limited, responsive web design almost always provides a better and more inclusive user experience than a standard, fixed-width design.



#### 11. Educating our clients that websites shouldn't look the same in all browsers

By allowing older browsers to display the pages slightly differently, the code becomes more maintainable and cheaper to update in the future, and decreases the amount of images to a website, which makes it faster and less expensive to produce. Leaner code that modern browsers understand equates to a faster website, which ranks higher in search engines than a slow one.

The number of users with older browsers is shrinking, the number of users with modern browsers is growing—let's support them! Most importantly, by supporting modern browsers, you can enjoy a responsive web design that responds to the differing viewports of browsers on different devices.



### :tv: Media queries: supporting differing viewports :tv:



#### 1. You can use media queries today

**Media queries** is a CSS3 module that allow target specific styles depending on the device's display capabilities. 



#### 2. Why responsive design needs media queries

Media queries can change CSS styles based on particular device capabilities/features, such as viewport width.

Media queries can be written inside CSS files and look like this:

```css
body {
  background-color: grey;
}

@media screen and (max-width: 320px) {
  body {
    background-color: green;
  }
}
```

Media queries can also conditionally load stylesheets into the stylesheet they are in:

```css
@import url("phone.css") screen and (max-width:360px);
```

They can also be inside the <head> tag to conditionally load a style sheet:

```html
<link rel="stylesheet" media="screen and (orientation: portrait) and 
(min-width: 800px), projection" href="800wide-portrait-screen.css" />
```

Using separate files called by media queries increases the number of HTTP requests needed to render a page, which in turn makes the page slower to load.

Media queries can test a device for the viewport's `width` and `height`, the device's size (`viewport-width` and `viewport-height`), the device's current orientation, its `aspect-ratio` (based upon the viewport width and height) and `device-aspect-ratio` (based upon the width and height of the device rendering surface), the number of bits per `color` component, the `color-index` (number of entries in the colour lookup table of the device), the number of bits per pixel in a `monochrome` frame buffer, the screen's `resolution`, the `scan` (which can be progressive or interlace TV features), and whether or not the device is `grid` or bitmap based.

All the above features, with the exception of `scan` and `grid`, can be prefixed with `min` or `max` to create ranges.

Styles further down a cascading stylesheet override equivalent styles higher up.  



#### 3. Our first responsive design

"Reset" styles are a set of CSS declarations that reset the different default styles of  different browsers so that they can all become the same base style and, therefore, further styles can be applied equally. They are usually added in the beginning of the main stylesheet. is a CSS3 module that allow target specific styles depending on the device's display capabilities. 



#### 4. Stopping modern mobile browsers from auto-resizing the page

Mobile browsers, instead of cropping the exceeding page, squeeze the whole page to fit the viewport. While the previous behaviour (cropping) could be solved with responsive design, the second one leaves the page awkward and difficult to navigate. So we can override that default canvas shrinking behaviour. The <meta> tag is simply added within the <head> tags of the HTML. It can be set to a specific width (which we could specify in pixels, for example) or as a scale, for example 2.0 (twice the actual size):

```html
<meta name="viewport"  content="initial-scale=2.0,width=device-width"/>
```

`content="initial-scale=2.0` section means to scale the content to twice the size, whilst the `width=device-width` part tells the browser that the `width` of the page should be equal to `device-width`.

The <meta> tag can also be used to control the amount a user can zoom in and out of the page:

```html
<meta name="viewport" content="width=device-width, maximum-scale=3, minimum-scale=0.5"/>
```

You could also disable zooming at all:

```html
<meta name="viewport" content="initial-scale=1.0, user-scalable=no"/>
```



#### 5. Fixing the design for different viewport widths

```css
@media screen and (max-width: 768px) {
  #wrapper { 
    width: 768px; 
  }
  #header,#footer,#navigation {
    width: 748px; 
  }  
}
```

This media query is re-sizing the width of the wrapper, header, footer, and navigation elements if the viewport size is no larger than 768 pixels.



#### 6. With responsive designs, content should always come first

We want to retain as many features of our design across multiple platforms and viewports, but it's also important to consider the order in which things appear. A user with a more limited viewport should get the main content before the sidebar or other secondary elements. 



#### 7. Media queries - only part of the solution

The problem with the media queries shown above is that they cover a very narrow spectrum of viewports. Media queries work when there is a specific target device. They make the design be static until a size "break point" is reached, at which point the design "snaps" to the new styles. We need a more fluid layout than this.



### :ocean: Embracing fluid layouts:ocean:



#### 1. Fixed layouts aren't future proof

Media queries work when we know the sizes of the targeted screens. This means media queries are not "future proof", since they don't adapt automatically to new screen sizes.



#### 2. Why proportional layouts are essential for responsive designs

When a viewport falls between two fixed-width sizes of our media queries, the design might require horizontal scrolling. We want a fluid design, that flexes and adapts proportionally to any viewport size, not only the few ones specified in a media query.



#### 3. Amending a design from fixed to proportional layout

> target + context = result

Let's take that we have a `div` within a `div`. The inner `div`, our *target* (what we want to convert from fixed size to proportional layout), has a width of **x** px. The outer `div`, our *context*, has a width of **y** px. The inner `div`'s width will be x/y. Some say not to round this number up, in order to display a more accurate response. Now, we must be careful with the context as it is the element immediately outside our target element. 



#### 4. Using ems rather than pixels for typography

"em" is an alternate font size to pixels, it is the percentage of the font in relation to the context element. If we set the body font size to 100% and use "ems" in all following typography, they will all be in proportion to that 100%, so to increase or decrease all font sizes is a simple task of decreasing the initial body statement, and all the fonts will increase/decrease proportionally. By default, the font size is 16px, so 100% or 1em will be equivalent to 16px. 

"em" is meant to express the leter m pronunciation. This letter was used to establish the size of a font because it is the largest letter. 



#### 5. Fluid images

Images, and other media, when its `max-width` is set to 100, will automatically scale up to 100% of their context element. Then, using CSS specificity can help define different sizes for specific elements. Sometimes, the `max-width` not go beyond its original size, which affect rendering.



#### 6. Serving different images for different screen sizes

Most of the time, stored images are be much bigger than they need to, wasting a lot of space. The "Adaptive Images" automatically creates, at defined size breakpoints, a resized version of the images based on their full size. This solution requires Apache 2, PHP 5.x, and GD Lib. With this solution, it is advisable to separate background images (and others that shouldn't be resized) from the rest of the images, usually in another folder called "assets". 



#### 7. Where fluid grids and media queries come together

Media queries help where fluid layouts lack, and fluid layouts ease the change from one set of defined styles within a media query to another.



#### 8. CSS grid systems

Many CSS grid systems use specific CSS classes. The Columnal grid system is based on dividing the viewport into 12 columns. f the time, stored images are be much bigger than they need to, wasting a lot of space. The "Adaptive Images" automatically creates, at defined size breakpoints, a resized version of the images based on their full size. This solution requires Apache 2, PHP 5.x, and GD Lib. With this solution, it is advisable to separate background images (and others that shouldn't be resized) from the rest of the images, usually in another folder called "assets". 



### :five: HTML5 for Responsive Designs :five:



#### 1. What parts of HTML5 can we use today?

HTML5 provides specifications for dealing with web applications, helps building better responsive web pages, and has tools to handle forms and user input. This allows avoiding other resource heavy technologies, such as JavaScript for validation. A ***polyfill*** is a JavaScript shim that replicates the characteristics of new browsers in older browsers. queries** is a CSS3 module that allow target specific styles depending on the device's display capabilities. 



#### 2. How to write HTML5 pages

The HTML5 doctype is the shortest method of telling the browser to render a page in "standard mode". Like the rest of HTML5, it is supposed to be efficient. Then, in the <html> tag, we specify the primary language for the elements' contents and textual attributes. Finally, the character encoding is specified in the <meta> tag, almost always being UTF-8. Valid HTML5 doesn't need end tags nor slashes in void tags, nor quotations marks. However, it can increase readability. Also, HTML5's <a> tag can wrap around groups of elements, except for other <a> tags, or forms. Conforming features, like the `border` attribute on an image, are obsolete features that still work (with warnings, so they should be avoided). Non-conforming features, however, are features that shouldn't be used anymore despite still being rendered in some older browsers.



#### 3. New semantic elements in HTML5

Semantics is "the branch of linguistics and logic concerned with meaning". So, giving our *markup* meaning. With general `div` sections, user agents, like browsers or search engine crawlers, don't understand the purpose of the different sections. Now, generic sections are defined through the <section> element. This is intended to separate contents, and not used for styling purposes, in which case, <div>'s are still probably the best. The <nav> element is used to define major navigational blocks, with links to other pages or parts of the page. The <article> element is used to wrap a self-contained piece of content, such as a blog post. The <aside> element is used for content that is not closely related to the content around it, such as sidebars or advertising. Many consecutive headings and subheadings can be wrapped inside a <hgroup> to hide the secondary elements from the HTML outline. Each <hgroup> section can have its own set of headings. The <header> tag should be used as an introduction to content. The <footer> element should contain information about the section above. The <address> element should be used for contact information.



#### 4. Practical usage of HTML5's structural elements

Even though there is no element to define the main content, since everything else can be defined, what's left is automatically denoted as the main content.



#### 5. HTML5 text-level semantics

**Inline** elements can also be called text-level semantics. The <b> element is meant to define a section of text to which one should draw its attention to, and in most browsers styles it with bold letters. The <em> element emphasizes the given content. Alternately, <i> defines a different quality of text, in an variant mood, and browsers render that text in italics. 



#### 6. Adding accessibility to your site with WAI-ARIA

WAI-ARIA means to make dynamic content on a page accessible, describing dynamic elements' roles, states and properties. ARIA's landmark roles allow screen readers to switch between the different regions of the page. They exist for the following regions:

* `application` - to specify the region of a web application
* `banner` - to specify a small region with the width of the site, such as the header or the logo
* `complementary` - to specify a complementary area than the main section of the page
* `contentinfo` - to specify an area of information about the main page, like the footer
* `form` - to specify a form
* `main` - to specify the main content of the page
* `navigation` - to specify navigation links for current or related documents
* `search` - to specify an area that performs a search

Like any attribute, it's possible to style ARIA roles, using the attribute selector:

```css
nav[role="navigation"]{
    ...
}
```

However, ARIA isn't limited to landmark roles only. 



#### 7. Embedding media in HTML5

Because of Apple, HTML5 can perfectly handle rich media rendering, striping Flash technology from its reign. 



#### 8. Adding video and audio the HTML5 way

The syntax for adding video to a page is much like adding an image: <video src="myVideo.ogg"></video>. It is also possible to add text in between the opening and closing tags, to be displayed when the browser can't render the media. There are also additional attributes, such as `width` and `height`. To get the default playback controls, we need to add the `controls` attribute. There is also an `autoplay` attribute:

```html
<video src="video/myVideo.mp4" width="640" height="480" controls autoplay>Some text ot be displayed when video rendering fails</video>
```

Some other attributes are `preload` to control pre-loading of media, `loop` to repeat the media in loop, and `poster` to define a poster frame for the media. Audio works the same way, with the <audio> tag. It just doesn't have the `width`, `height` and `poster` attributes, and obviously doesn't have a playback area for visible content.



#### 9. Offline Web applications

Because responsiveness is tied to mobile usage, providing the means to users accessing our web application while *offline* seems useful. This works by having a `.manifest` file with pointers to all pages that can be accessed *offline*. The file also lists all resources needed (images, JS, etc). The browser then reads the `.manifest` file and downloads the resources listed, caching them locally. In the opening HTML tag, we point to the `.manifest` file: 

<html lang="en" manifest="/offline.manifest">

The file must start with `CACHE MANIFEST`. Then, the `CACHE:` section lists the relative (or absolute) paths for the files needed *offline*. Also, all HTML files that point to the *offline* manifest are added automatically, but with this method they are only downloaded and cached once visited. The `NETWORK:` section lists resources that should not be used from cache while online, so it's usually the `*` character, which is the **online whitelist wildcard flag**. 

Another way of making the pages available *offline* is by adding `manifest="/offline.manifest"` to the opening <html> tag. However, this makes available only the HTML page, and not other resources such as JavaScript files, images, etc. If these are essential, they should be specified in the `CACHE:` section.

When there are changes in the website, the manifest file should be changed somehow, in order for it to be "rerun", and load the changed files again. One way of doing this is by increasing the version in the header comment.



### :paintbrush: CSS3: Selectors, Typography and Color Modes :paintbrush:



#### 1. What CSS3 offers the frontend developer

With just a few lines of code, CSS3 can help the responsive design to load faster, not relying on resources (images, JavaScript,...) as much anymore, and be easier to maintain and change - mostly because the visual effects are done through code and not images, changing some parameters like colors can be done in seconds.



#### 2. Anatomy of a CSS rule

```css
.round{
	border-radius: 10px;
}
```

Above, is a CSS rule. In this rule, `.round` is the **selector**, the rest being the **declaration**. In this declaration, the `border-radius:` part is the **property**, and the `10px` part is the **value**. 



#### 3. Vendor prefixes and how to use them

**Vendor prefixes**, such as `-webkit-` for Webkit based browsers and `-ms-` for Microsoft (IE), are used by browsers to test "experimental" CSS features. Browsers ignore the prefixes that aren't meant for them and apply the ones they can. This is faster and more elegant and robust than using images, but still leads a little to code bloat. If time/budget are tight, one might decide to omit prefixes for any browser with, for example, less than 3% of usage at the moment. 



#### 4. Quick and useful CSS3 tricks

Markup with text that we want to span across multiple columns:

```html
<div id="main" role="main">
<p>
    Text goes here
</p>
<p>
    Text goes here
</p>
</div>
```

If we want to define a given column width, and make the number of columns with that width dependable of the viewport width, the code can be as such:

```css
#main {
	column-width: 12em;
}
```

If, however, we want to define a fixed number of columns, and make their width dependable of the viewport width, the code can be as such:

```css
#main {
	column-count: 4;
}
```

We can even customize the gap and a divider between columns:

```css
#main {
    column-gap: 2em;
    column-rule: thin dotted #999;
    column-width: 12em;
}
```

There is also an attribute to divide a big word into several lines if it doesn't fit in one: `word-wrap: break-word;`. 



#### 5. New CSS3 selectors and how to use them

We can apply a rule to an element with a given attribute value:

```css
img[alt="atwi_oscar"] {
	border: 3px dashed #e15f5f;
}
```

We can select elements whose given attribute *starts* with a certain value:

```css
img[alt^="film"] {
	border: 3px dashed #e15f5f;
}
```

Or, we can select elements whose given attribute *ends* with a certain value:

```css
img[alt$="film"] {
	border: 3px dashed #e15f5f;
}
```

We can also select elements whose given attribute *contains* a matching substring:

```css
img[alt*="film"] {
	border: 3px dashed #e15f5f;
}
```

There's a selector for the first item in a list - `li:first-child` - and also one for the last item in a list - `li:last-child`. There is also a selector for a nth element, selecting the element based on a position (passing an integer) - `nth-child(n)` - or range of positions, like `:nth-child(even)`. We can also pass numerical expressions to express a range of positions, like `:nth-child(3n+1)`.

The selector `(:not)` is used to select everything that isn't something else:

```css
nav ul li:not(.internal) a {
	color: #fe0208;
}
```

Besides pseudo-classes, there are also pseudo-elements, separated by double colon. A particularly handy example: 

```css
p::first-line {
	color: #ff0cff;
}
```



#### 6. Custom web typography

`@font-face` is a rule for adding custom fonts. Because there are many font formats, like the **Embedded OpenType**
**(EOT)**, the **TrueType (TTF)**, the **Scalable Vector Graphics (SVG)**, or the **Web Open Font Format (WOFF)**, it is necessary to cover all implementations.



#### 7. Help - my CSS3 @font-face headings look messy

While using `@font-face` fonts in heading elements, it is important to always define the `font-weight`. Something to take in consideration is the font file size. The most lightweight ones add an extra 70KB of data. CSS3 allows us to use the **RGB** and **HSL** methods for declaring color, allowing the use of an alpha channel alongside (**RGBA** and **HSLA** respectively). RGB (Red, Green, and Blue) is a coloring system that defines different values for the red, green, and blue components of a color. In the CSS, after defining the color mode (for example, rgb) each of the three values separated by commas inside the parenthesis. HSL (Hue, Saturation, and Lightness - not the same as HSB!) works on a 360° color wheel. The first value in a HSL color, represents Hue, and has Yellow at 60°, Green at 120°, Cyan at 180°, Blue at 240°, Magenta at 300° and Red at 360° -  mnemonic "Young Guys Can Be Messy Rascals".  The following two values, in percentages, are for saturation and lightness. An element with an alpha transparency will show what's beneath it. An HSLA/RGBA has the same syntax as the HSL/RGB, but one last field for the oppacity, with a value between 0 and 1. 



### :open_mouth: Stunning Aesthetics With CSS3 :open_mouth:



#### 1. Text shadows with CSS3

To add shadows, we can use `text-shadow`:

```css
.element {
	text-shadow: 1px 1px 1px #cccccc;
}
```

The first value is the shadow to the right, the second one is the shadow below, and the third one is the blur but can be omitted. These values can be expressed in pixels, em or rem, but because they are often very small values, pixels tend to look good across all viewports. The final value is the colour of the shadow, written in HEX, RGB(A) or HSL(A).

Shadows to the left and above can be achieved using negative values: `text-shadow: -4px -4px 0px #dad7d7;`. It's possible to add multiple text shadows, separated by a comma.



#### 2. Box shadows

Box shadows follow the same syntax as text shadows: horizontal offset, vertical offset, blur and color. They can be used to create an "inset" shadow, which applies to the inside of the element, and not the outside: `box-shadow:inset 0 0 40px #000000;`. It's possible to add multiple box shadows, separated by a comma. 



#### 3. Background gradients

To set a background gradient for an element, we don't need to use graphical resources, we can just do it with CSS3. This background automatically fits the element, as it expands or shrinks.

```css
background: linear-gradient(90deg, #ffffff -50%, #e4e4e4 50%, #ffffff 100%);
```

In linear backgrounds, inside the parenthesis, the first optional value refers to the direction of the gradient, the default being vertical, top to bottom. Next up is the colour at the start and the percentage of the length at which the first colour would start fading into the next. Next is the colour at the end of the gradient and the percentage of the length at which the penultimate colour starts fading into this last one.

Radial backgrounds also begin from a central point, but spread out smoothly in an elliptical or circular shape.

```css
background: radial-gradient(center, ellipse cover, #ffffff 72%, #dddddd 100%);
```

Within the parenthesis, we firstly specify the starting point. Then, we define the shape (circle or ellipse) and the size. The size can be `closest-side` (also known as `contain`, the shape goes all the way until it meets a side of the box that is nearest from the centre), `closest-corner` (the shape goes all the way until it meets the closest corner from the centre), `farthest-side` (the shape goes all the way until it meets a side of the box that is furthest from the centre), and `farthest-corner` (also known as `cover`, the shape goes all the way until it meets the furthest corner from the centre). Then, we can define the colour points for each percentage of the radius. 

The gradients can be repeated throughout the background, by adding the prefix `repeating-`. 



#### 4. Background gradient patterns

Both linear and radial gradients can be used to create complex background patterns. 



#### 5. Responsive considerations for CSS

Different declarations can be used for different *viewports*, through media queries. linear and radial gradients can be used to create complex background patterns.



#### 6. Bringing CSS3 properties together

All these abstract features implementations can be put together to create cohesive website designs in a rapid way, while providing changes on the fly. Plus, if correctly written,  it can contain whatever content is needed, without breaking.



#### 7. Multiple background images

Many times, the top and the bottom of a page, or of a section, have different background images. 

```css
background: url('../img/1.png'), url('../img/2.png'), url('../img/3.png');
```

The syntax shows a stack of images. The image listed first appears nearest to the top. If the last declaration is a colour, this will show below the images above, being seen if the images are PNG files and have (partially) transparent backgrounds. 

These images don't need to be the same size. We can set different sizes for each image, using the `background-size` property. The size values wanted for each image are declared, in the format width and height (in that order), separated by commas and in the order of the declarations above. The values can be pixels, percentages, auto (which sets the image as its native size), cover (which expands the image to cover the area of the element, preserving the ratio), or contain (which expands the image to fit the longest side of the element, preserving the ratio):

```css
background-size: 100% 50%, 300px 400px, auto;
```

It is also possible to specify different positions for the images, the default position being the top left corner. 



#### 8. More CSS3 features

These are not all the features available, but are some of the ones that give most benefit while being efficient and flexible. 



#### 9. Sizeable icons which are perfect for responsive design

`@font-face` icons are fonts specifically made to create responsive icons. 



### :zap: CSS3 Transitions, Transformations and Animations :zap:



#### 1. What CSS3 transitions are and how we can use them

It's common to create a hover state on hyperlinks, so that the users understand they are hovering over a link. Traditionally, these transitions between states are abrupt - either one state or the other is shown. However, "transitions" allow a smooth transition between two states - not just applied to hover states. The transition is applied to the original element, not the hover state, so that different states such as `:active` can also have different styles and still enjoy the transition.

A `transition` can be defined by the transition-property (the name of the CSS property to be transitioned, such as `background-color`, `text-shadow`, or `all` if applied to all possible properties), the transition-duration (the length of time over which the transition should occur), the transition-timing-function (how the speed of the transition varies through its duration), and the transition-delay (an optional value to determine a delay before the transition starts).

Where a rule has multiple properties declared they don't have to transition in the same way:

```css
#content a {o
	transition-property: border, color, text-shadow;
	transition-duration: 2s, 3s, 8s;
}
```

The durations' order match the order of the properties we want to transition.

Because it's necessary to employ transition effects subtly, unless there is a compelling reason to do otherwise, using the default transition (ease) over a short interval (1 second max) is often best.

An easy way to make everything pretty:

```css
* {
	transition: all 1s;
}
```



#### 2. CSS3 2D transformations

CSS transformations (both 2D and 3D) define what the element will become. The CSS3 2D Transforms Module allows the following transformations: `scale ` (scales an element to appear larger or smaller), `translate` (moves an element on the screen), `rotate` (rotates the element by the given degrees), `skew` (skews an element with its X and Y coordinates), and `matrix` (moves and shapes transformations with pixel precision). 

There si also a `transform-origin` property to amend the point from which the transformations are applied, the default being the center of the element. 



#### 3. Dabbling in CSS3 3D transformations

The first important point is to set the `perspective` on the parent element, which activates the 3D space. The larger the perspective value is, the deeper the 3D space is, from the user viewing point. So, for a subtler effect, this value should be higher. This value, however, only applies to the first direct descendent of the element. To pass this perspective on, we can use `-webkit-transform-style: preserve-3d;`. 



#### 4. Animating with CSS3

CSS3 employs animation keyframing conventions found in Flash. A CSS3 animation has a keyframes declaration, then used in an animation property. Let's see an example:

```css
@keyframes warning {
    0% {
    	text-shadow: 0px 0px 4px #000000;
    }
    50% {
    	text-shadow: 0 0 20px #000000;
    }
    100% {
    	text-shadow: 0px 0px 4px #000000;
    }
}
```

In the example above, we define the `@keyframes` and give it a name: "warning". Then, we set some percentage points. After declaring the keyframe, we can use reference it: `animation: warning 1.5s infinite ease-in;`. The second value is the `animation-iteration-count` (using infinite makes the animation continuous), and the third value is the timing function.

It is also possible to specify `animation-delay` (to delay when the animation starts), `animation-play-state` (can be set to running or paused) and `animation-fill-mode`.



### :pencil: Conquer Forms with HTML5 and CSS3 :pencil:



#### 1. HTML5 forms

Besides standard input fields and text areas, there is also available a number spinner and a range slider. The default range goes from 0 to 100, but can be changed with the `min` and `max` properties. 

<input id="howYouRateIt" name="howYouRateIt" type="range" min="1" max="10" value="5" >

Input types can be "email", to match the syntax of an email address, "number", that receives a number as input, "url", that tells some browsers it expects a URL, "tel", to expect a telephone number, "color", that produces a color picker, or "search", which sometimes appears differently. We can define some text as a placeholder for a field, to appear when it is empty. There is also some client-side validation to stop users from sending a form without an answer in a required field, defined by `required aria-required="true"`.  If the form is submitted without the field, a warning message should be displayed.

Another HTML5 form attribute that can be added to input fields is `autofocus`, that makes the form load with that field already focused (selected). 

Most browsers auto-complete the values of form fields, where possible, if that setting is turned on. For sensitive data, or to ensure users pay attention when filling out that field, we can disable that option by writing the attribute `autocomplete="off"`. This attribute also works on the <form> tag.

The `pattern` attribute expects a regular expression and ensures the value passed on that field respects the regex. 

<input id="date" type="date" name="date" /> is a date input. If the type is "data", the date picker is used to select a day of the month within a year.  If the type is "month", the date picker is used to select a month of a year. If the type is "week", the date picker is used to select a week within a year. If the type is "time", the date picker is used to select a time, in the 24h format. If the type is "datetime", the date picker is used to select a time of a certain day (a day of the month within a year). The type "datetime-local" is the same, but omits the time zone information.



####  2. How to polyfill non-supporting browsers

"Webshims Lib" loads the form polyfills needed to make non-supporting browsers handle them. 



####  3. Styling HTML5 forms with CSS3

To style forms, we could add `border-radius` and `background` gradients, and a subtle box-shadow. There are some form-specific pseudo selectors: 

* `input:required:` for required fields
* `input:focus:invalid:` for focused fields with an invalid value
* `input:focus:valid:` for focused fields with a valid value

We can use these to give users instant feedback.



### :crossed_flags: Resolving Cross-browser Responsive Challenges :crossed_flags:



#### 1. Progressive enhancement versus graceful degradation

**Graceful degradation** means creating a site for modern browsers but ensuring older versions (untill a certain cut-off point) have a usable experience, or, at least, get a warning about the problems they will face while using that browser.

**Progressive enhancement** start by writing code that is usable by all browsers, and from there enhances it through CSS and, if needed, JavaScript. This is currently considered the best practice. 



#### 2. Should you fix older versions of Internet Explorer?

It is possible to polyfill the majority of features to older browsers, but it could worsen the performance and it certainly is a time-consuming task, which won't give a lot of benefits, because the use of older browsers is diminishing, while the usage of modern browsers is increasing. 



#### 3. Modernizr - the frontend developer's Swiss army knife

Modernizr is an open source JavaScript library that "feature tests" a browser's capabilities, to find out whether a browser supports a certain feature. This automatically fixes styling issues for older browsers and also allows us to conditionally load additional CSS or JS files, only when needed.



#### 4. Changing navigation links to a drop menu conditionally

Having many navigation links on a page can take up a big portion of the screen, which is a problem in smaller viewports, so it would be better to have a drop menu when a viewport is below a certain limit. There are a few pre-written scripts for achieving this.



#### 5. High resolution devices 

Devices are changing all the time, and it is not just viewport size that can differ, the resolution can too. To adapt, media queries can also target different resolutions. However, many large images equate to longer download times, so this means there is, as always, a tradeoff to consider.