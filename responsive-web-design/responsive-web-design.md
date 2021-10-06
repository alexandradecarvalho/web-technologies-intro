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