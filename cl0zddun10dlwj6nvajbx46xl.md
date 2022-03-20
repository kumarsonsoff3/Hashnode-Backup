## CSS Interview Questions

Hey Readers, hope you all are good and doing great. In today's world of tech, it's not easy to land a job while it's impossible to know answers to all questions that an interviewer may ask you. 

People have no idea of what kind of questions should they expect when they apply for a Job. 🤷‍♂️ In this article, I'll be sharing some frequently asked CSS questions. These are the ones that are asked in different interviews from many different developers and programmers at different levels. 😀

Before we go, I let you remind that **Cascading Stylesheet Sheet ** is a stylesheet language that determines how the elements and content should look on the page. CSS is used to develop a consistent look and feel to the webpage. 😉

## Here is the list of the most frequently asked CSS interview questions 

<img src="https://media4.giphy.com/media/JRmKnYCDaAHOQFUeW1/giphy.gif?cid=e826c9fcyd4w59j0g2nlennzmi2w4d8sq2wz5skoxyrmzn74&rid=giphy.gif&ct=g" />

### What are the advantages of using CSS?
The main advantages of using CSS are the following:

- CSS provides a way to present the same content in multiple presentations formats on mobile, desktop, or laptop. 
- Used effectively, the style sheet will be stored in the browser cache and they can be used on multiple pages, without having to download again.
- CSS is built effectively such that it can be used to change the look and feel completely by making small changes. To make a global change, simply change the style, and all elements in all web pages will be automatically updated.

### What do you know about CSS sprites?
A sprite is a collection of many images put into a single image file to be used in a webpage, these are used because a webpage with too many images may take too long to load as it generates several server requests.

Using image sprites we can reduce the number of server requests and save bandwidth. 

### What is Box Model in CSS? Which properties are a part of it?
This is the most basic and most frequent question asked multiple times in multiple interviews, you should know.

CSS draws boxes during the layout process. Everything in CSS has a box around it, this is known as the box model. Each box is made up of four areas which are `content`, `padding`, `border`, `margin`.

**This is how a box model looks like:**
![image.png](https://cdn.hashnode.com/res/hashnode/image/upload/v1647763699189/1fO46vIta.png)
- 𝗖𝗼𝗻𝘁𝗲𝗻𝘁: The content area contains just that: the content! **For example:** a text element's content area would be the `text content`.
- 𝗣𝗮𝗱𝗱𝗶𝗻𝗴: Padding area is the amount of empty space between its content and its border. This can be changed just by changing the element's padding, using the `padding-left`, `padding-right`, `padding-top`, `padding-bottom` properties or by using the shorthand property which is more common `padding: top, right, bottom, left` in their respective units)
- 𝗕𝗼𝗿𝗱𝗲𝗿: Area surrounding the padding. We can change an element’s border using the `border-width`, `border-style`, and `border-color` properties, or the shorthand property border.
- 𝗠𝗮𝗿𝗴𝗶𝗻: This is the outermost area of the **box model**.  Similar to the others, we can also change the margin size.

### What are the limitations of using CSS?
Main Disadvantages with CSS are:
- 𝗕𝗿𝗼𝘄𝘀𝗲𝗿 𝗰𝗼𝗺𝗽𝗮𝘁𝗶𝗯𝗶𝗹𝗶𝘁𝘆 𝗶𝘀𝘀𝘂𝗲𝘀 - Some style selectors are not supported in many old browsers. We have to determine whether the style we are using is supported or not using the `@support` selector.
- 𝗡𝗼 𝗽𝗮𝗿𝗲𝗻𝘁 𝘀𝗲𝗹𝗲𝗰𝘁𝗼𝗿 - Currently using CSS, you can't select a parent.
- 𝗖𝗿𝗼𝘀𝘀 𝗕𝗿𝗼𝘄𝘀𝗲𝗿 𝗶𝘀𝘀𝘂𝗲𝘀 - Some of the selectors behave differently in different browsers.

### What are CSS preprocessors? What are Sass, Less, and Stylus? Why do people use them?

CSS preprocessors are the tools that help us to extend the basic functionality of the default CSS through their own scripting language. This helps us to use complex logic syntax like - functions, mixins, code nesting, inheritance to name a few in your default vanilla CSS.

SASS stands for **Syntactically Awesome Style Sheet**. SASS can be written in two different syntaxes using SASS or SCSS.

**SASS Syntax:**

``` 
$font-color: #ffe41e 
$bg-color: #00f

#box
	color: $font-color
	background: $bg-color
```

**SCSS Syntax**

```
$font-color: #ffe41e;
$bg-color: #fcba03;

#box{
	color: $font-color;
	background: $bg-color;
}

```
- 𝗦𝗔𝗦𝗦 uses `.sass` while 𝗦𝗖𝗦𝗦 uses `.scss` extension.
- 𝗦𝗔𝗦𝗦 doesn't use curly braces or semicolons while 𝗦𝗖𝗦𝗦 uses these, just like CSS.

**𝗟𝗘𝗦𝗦:** less stands for **Leaner Stylesheets**. LESS is easy to add to any JavaScript project by using NPM or less.js file. This file uses `.less` extension.

𝗟𝗘𝗦𝗦 syntaxis the same as the SCSS with some exceptions. LESS uses `@` to define the variable.

```
@font-color: #ffe41e;
@bg-color: #fcba03

#box{
	color: @font-color;
	background: @bg-color;
}
```

**Stylus:** Stylus offers a great flexibility in writing syntax, supports native CSS as well as allows omission of brackets, colons, and semicolons. It doesn’t use `@` or `$` for defining variables.

```
/* STYLUS SYNTAX WRITTEN LIKE NATIVE CSS */
font-color= #ffe41e;
bg-color = #fcba03;

#box {
	color: font-color;
	background: bg-color;
}

/* OR */

/* STYLUS SYNTAX WITHOUT CURLY BRACES */
font-color= #ffe41e;
bg-color = #fcba03;

#box
	color: font-color;
	background: bg-color;
```

### Is it important to test the webpage in different browsers?
It's most important to test a website in different browsers when you're first designing it, or making major changes.

However, it's also important to repeat these tests periodically, since browsers go through a lot of updates and changes, and we know that some of the CSS properties do not support in many browsers.

### What is viewport height and viewport width in CSS?
It's used to measure the height and width in percentage concerning the viewport.

If the height of the browser is equal to 1000px, 1vh is equal to 10px, similar for the width.

### Difference between reset vs normalize CSS? How do they differ?
𝗥𝗲𝘀𝗲𝘁 𝗖𝗦𝗦 - CSS reset aims to remove all built-in browser styling. **For example**, `paddings`, `margin`, `font-size` of all elements back to the same.
𝗡𝗼𝗿𝗻𝗮𝗹𝗶𝘇𝗲 𝗖𝗦𝗦 - aims to make built-in browser styling consistent across browsers. It also corrects bugs for common browser dependencies.

<hr/>

⚠ **You can also modify answers as per your convenience, it's not recommended to cram these ones. Also, this article does not claim that you will find the exact same questions in your interview.** 

It's totally ok to feel stressed in interviews and everyone does, but just be yourself, you will gonna make it.

Also, a more important thing is that there is no one who knows all the answers and all frameworks of a language. So don't be shy to say no about the thing you don't know. This will not take your image down, but if you try to frame something that you don't know about, then there is a possibility that the interviewer will caught you. 😅 I'm saying again....just be yourself.

Ok! It's wrap-up time, that's pretty much for this blog. I'm getting late for an important meeting, see you in the next one.

<hr/>

## Conclusion
- We have covered some of the **frequently asked interview questions**.
- If you find this useful, then please let me know in the comments below, and consider sharing it with your audience.
- More blogs related to this are about to come, follow @[Priyanshu](@kumarsonsoff3) to stay tuned. 😉
- Also, You can Join me on 🐦 [Twitter](https://twitter.com/Kumar_Sons_off), where I tweet more frequently about Tips and Resources for web developers. 
- Good luck for your interview. 👍
- Thanks for Reading. 😊

**You can extend your Support by Buying me a coffee here.**🌴
[![yellow-button.png](https://cdn.hashnode.com/res/hashnode/image/upload/v1644160648145/jcCO-V5ENx.png)
](https://www.buymeacoffee.com/Kumar_sons_off)

**Published on: 03/20/2022.**