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

##### 

##### Exercise 1.1 - Write a well-structured English sentence with invalid tokens in  it. Then write another sentence with all valid tokens but with invalid  structure.

- Í like the sün. (Í and ü are not valid tokens in English but "I like the sun" is a well-structured sentence)
- Sun me likes. (all valid tokens but invalid structure)

##### 

##### Exercise 1.4 - If you run a 10 kilometer race in 43 minutes 30 seconds, what is  your average time per mile? What is your average speed in miles per  hour? (Hint: there are 1.61 kilometers in a mile)

```
>>> 43*60 + 30 # 10 km time in seconds
2610
>>> 2610*1.61 / 10 # 1 mile time in seconds
420.21000000000004
>>> 420.21 / 60 # 1 mile time in minutes 
7.0035
```

### 

### 📣 Variables, expressions and statements 📣

#### 

#### 1. Values and Types

A **value** is one of the basic units of a program. There are different **types** of values: `2` is a whole number, an **integer**, so its type is `int`;  `2.5` is a number with a fractional part but its type is called `float` because these numbers are represented in a format called **floating-point**; and `"Hello, World!"` is a `string`, because it contains a **"string"**  (sequence) of letters. If you are not sure what type a value has, the interpreter can tell you: