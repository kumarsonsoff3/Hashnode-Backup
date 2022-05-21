## Animation is Fun with GSAP

When it comes to CSS animations, we know these are the most complicated yet important ones for a webpage/web app. Animations help the webpage to interact with the users and keep them engaged. Sometimes while creating complex animations using the CSS `transform`, `animations`, `keyframes`, etc, etc, you might have felt that there should be an alternative for this, that make it a lot easier to create such Animations. Didn’t you!?

Okay, I feel the same, and not only me, animations suck a lot to many developers and cost them a lot of their precious time, exploring the internet I came across the **GreenSock Animation Platform (GSAP)**. GSAP makes it a lot easier to create animations, handle their `duration`, `eases`, `delays`, and much more. 

Initially, you might feel like if we can do this all with native CSS, then why to load an extra library, but believe me, after using and exploring a bit about GSAP, you'll be a huge fan of it, and will fall in love with GSAP animations.


![oh-boy-here-we-go-again.gif](https://cdn.hashnode.com/res/hashnode/image/upload/v1653008848356/2SgATnBVQ.gif align="center")

 ## Scope of the Article

- In this article, we are gonna give you a brief intro to the GSAP animation which would be enough for you to get started with GSAP. 

- Next to the introduction, we will create some animations for some real-world scenarios, which will gonna be a lot fun.

- Article does not claim to explain completely about the GSAP. (You know that, but you can say it as a beginner-friendly tutorial for you to get started! 😊)

## Prerequisites
Before we get started, have a look at the following prerequisites. If you are the one who satisfies the following prerequisites, then only move ahead - 

- You should have a basic knowledge of JavaScript (with basic what I mean is that you should know the JavaScript fundamentals).  
- Should have a laptop with an Internet connection. 😄

You are Good to go now! 

GSAP
-------

GSAP is an animation library that can animate anything that JavaScript can touch (CSS properties, SVG, React, Canvas, etc, etc.) and solves countless cross-browser inconsistencies with a blazing speed up to [20X faster than jQuery](https://greensock.com/js/speed.html) so that you can focus on animating.

## Installation
You can install GSAP in too many ways, we are only gonna discuss the `npm install`, `cdn`, and `In codepen`.

If you are a beginner at npm and all, you should go with the CDN or CodePen installation.

### 1. CDN install 
1. Add the following snippet to your HTML file just above your main `script.js` file.

```html
<script src="https://cdnjs.cloudflare.com/ajax/libs/gsap/3.10.4/gsap.min.js"></script>
```

I personally prefer CDN because it *will be cached on most browsers as it's used by a lot of other websites*, *reduces the bandwidth* and has some other benefits too.

**Note:** You can always add extra GSAP plugins from the [official installation page](https://greensock.com/docs/v3/Installation#CDN) as per your needs. We are just going with the basic ones for now.

### 2. NPM install

- Download the ZIP from the official installation page [here](https://greensock.com/docs/v3/Installation#ZIP).
- Run the following command in your terminal.

```
npm install gsap
```

or with yarn

```
yarn add gsap
```

- Import GSAP it in your project.

```jsx
import { gsap } from "gsap";
```

### 3. Installation in CodePen

If you are using CodePen, then go with the following steps.

- Go to settings.
- Click on the JS from the sidebar.
- Add `External Script/Pens`
- Then in the search bar, search for the GSAP, and add the latest version to your pen.
- Save & Close


Now that you've installed the GSAP library, so let's jump on the Basics.

## GSAP Basics to get started

When it comes to the GSAP, the very first and the most important thing to know about are the `Tweens` and `Timelines`. First, we'll go for the `Tweens`. 

### 1. Tweens

In simple terms, a **Tween** is a declaration that can change one or more properties of single or multiple objects with staggered or not staggered start times. This is where all the animation work is done.

The common methods for creating a tween are `gsap.to()`, `gsap.from()`, `gsapFromTo()`, as their name suggests are their functions.

#### 1. gsap.to()

It is a tween declaration that defines the final position or the final state of a `class`, `id`, or an `element` where the animation is gonna end.

Here is the basic syntax for the `gsap.to` tween:

```jsx
gsap.to(".class", {duration: 2, x: 250, y: 100, rotate: 720})
```

In this one, the `class` is the one which is going to be animated, `duration` defines the time that how long will it take to complete the animation, and you are smart enough to know what the `x`, `y`, `rotate` are. 😉

**Look at the CodePen demo for the tween:** 
In case it's already loaded, you can click anywhere in the body to **restart** it.

%[https://codepen.io/Kumar_Sons_off/pen/MWQbBwK]

Here in this Demo, I've used the `gsap.to()` method to define the tween which animates the **Twitter** SVG. 

#### 2. gsap.from(): 

It's another common method to declare a tween, but the difference is that here we declare the initial variables from where the tween has to start, to come to its original position.

The basic syntax for `gsap.from()` method is quite similar to the `gsap.to()`, just the initial values are used for the variables instead of the final ones.

```jsx
gsap.from(" ", { duration: 2, x: 150, y: 100, rotate: 720})
```

**Let's now have a look at the live demo to understand better that how the `gsap.from()` method works:**

%[https://codepen.io/Kumar_Sons_off/pen/XWZNPZy]

The `gsap.from()` method is kinda opposite of the `gsap.to` method, and initial values are used from where the animation starts to reach the origin/normal position.

#### 3. gsap.fromTo()

The `gsap.fromTo()` method is the sum of both the above methods. We define both the initial and final variables for the tween.

The basic syntax for the `gsap.fromTo()` tween:

```jsx
gsap.fromTo(".class", {duration: 2, x: 400, y: 200}, {duration: 1, x: 200, y: 80})
```

You might be getting the idea from the syntax that here, both the initial and the final points are defined. Let's understand it better with the help of an example: 

%[https://codepen.io/Kumar_Sons_off/pen/zYRoJQQ]

*(P.S: As I already mentioned that in case if CodePen preview is already loaded, you can always click anywhere in the body to restart it)*

Here in the above illustrations, you might have noticed that I'd some extra code to restart the tweens, this could only be made easier due to the GSAP `restart()` method to control the tween. There are several other methods like `play()`, `pause()`, `resume()`, `progress()`, etc. 

**Here is how we use the controls methods in gsap:**

```jsx
// Tween which we need to control ~~ 
const tweenTwitter = gsap.fromTo(".Twitter", {duration: 0.5, x: 150}, {duration: 1, x: 0, y: 150})

// triggering an eventListener for the event when the action should take place
document.body.addEventListener("click", () => tweenTwitter.restart())

// you can also use a button or an element to trigger the event, just use the event listener for them in a similar way!
```

You can just use several other controllers in the same way. The most common and frequently used ones are: 
- pause()
- play()
- progress()
- Seek()
- reverse()
- restart()
- duration()
- timeScale()
- time()
- kill()

I'll not gonna give you examples for each one, as you can understand that it's hard to pack complete library in a 12 minutes article, but you can always go through the [official documentation page](https://greensock.com/docs/) to explore more about GSAP. 

Okay, now I guess, we have discussed enough about the Tweens yet, so now it's time to move on the Timelines. 


### 2. Timeline

A **Timeline** is a container for all the *tweens*, which executes the tweens one after another. Timeline makes it a lot easier to control multiple tweens, like to `reverse`, `restart`, `pause`, `progress`, etc these all could be done in one go for all the tweens in a timeline. 

We need not to reverse the **tweens** one by one when they are in the timeline. Without timelines, building complex animation sequences is far more difficult & bulky because you need to define a lot of similar properties multiple times, but timelines make it a lot easier for you.

**Timelines could be created with the basic syntax:** 

```jsx
// Here we have set the defaults for the timeline, so we have no longer need 
// to repeat these properties for the each one.
const timeline = gsap.timeline({defaults: {duration: 2, delay: 0.6}})

timeline
// 1. the tweens execute one after other due to certain default delay
  .to(".Twitter", {x: 160, y: 130, ease: "elastic"})
  .to("h1, p", {x: 160, y: 130, ease: "elastic"})

// 2. the h1 & p tween execute a bit earlier due to the reduced delay by "0.4"
  .to(".Twitter", {x: 0, ease: "bounce"})
  .to("h1, p", {x: 0, ease: "bounce"}, "<0.4")

// 3. All three goes simultaneously, as they are selected in the same tween, and executed as a single piece.
  .to("h1, p, .Twitter", {x: 130, y: 0, ease: "elastic"})

// 4. We use stagger, to add a time interval between the starting points of the tweens
  .to("h1, p, .Twitter", {x: 0, y: 0, stagger: 0.2});

//  . similar tweens as much you want can be added here.

// Click anywhere in the body to reverse the whole timeline.
// here we use the reverse function to reverse the whole timeline
const reverseTimeline = document.querySelector("body");

reverseTimeline.addEventListener("click", function () {
  timeline.timeScale(2);
  timeline.reverse();
});

```

%[https://codepen.io/Kumar_Sons_off/pen/BaYQGBM]

*(P.S: Click anywhere in the body to Reverse)*

In a  timeline, we set some defaults so that we need not to repeat those ones again & again. The *tweens* in the *timeline* execute one after another in a sequence.

In the above example, we've used the `ease`, which is to define how the transition should go on. Ease is simply the `animation-timing-function`. You can explore more about ease [here](https://greensock.com/docs/v3/Eases). 

Also, we have used the `stagger`, which allows us to add a timed lap between the start of each tween, like if `stagger: 0.2`, then there would be a `0.2` second between the start times of each tween. 

In simple language, `stagger`, prevent the different tweens to act simultaneously by adding a timed lap between their starting point. Hope this one is clear to you. 

So, now I believe that you have a basic idea of what GSAP is, and how it affects your animation process. So, finally, we have done with the boring theory part and reached the most awaited part of this article, let's now jump into an exciting project. 

## Fun Project with GSAP

### GSAP Tab Animation Slidebar

GSAP made it a lot easy to create a  tab animation sidebar ( mean if one tab is open then the other will be closed, like only one or none of them will stay open ). In this one you'll need your JavaScript Skills to handle events.

**Look at the following demo of the project to get an idea of what I'm talking about.**

<iframe width="560" height="315" align="center" src="https://www.youtube.com/embed/YnIYlS9pxmo" title="YouTube video player" frameborder="0" allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture" allowfullscreen></iframe>


So now, without further delay let's dive into this one. Grab the HTML code below required for this project.

```html
    <div class="Home_Container">
      <div class="intro">
        <h1 class="gradient">Hey there, Priyanshu Kumawat here</h1>
        <p>This is a simple Tab Animation Expander</p>
      </div>

      <div class="wrapper">
        <div class="expander">
          <div class="close">&times;</div>
        </div>

        <div class="expander">
          <div class="close">&times;</div>
        </div>

        <div class="expander">
          <div class="close">&times;</div>
        </div>

        <div class="expander">
          <div class="close">&times;</div>
        </div>

        <div class="expander">
          <div class="close">&times;</div>
        </div>

      </div>
    </div>
```

Now, it's time for some CSS, to style the above elements. You can modify the CSS styles in the way you want, it's totally up to you! 😊

```CSS
/* import a google font to make it more attractive */
@import url("https://fonts.googleapis.com/css2?family=Pacifico&display=swap");

/* Set the default values for the webpage */
html,
body {
  width: 100%;
  height: 100%;
  overflow: hidden;
  background-color: antiquewhite;
  margin: 0;
}

/* These are the simple CSS required for the slidebar. */
.wrapper {
  height: 100%;
  width: 100%;
  background-color: antiquewhite;
  display: flex;
  align-items: center;
  justify-content: center;
  flex-direction: rows;
}

.expander {
  width: 50px;
  height: 60vh;
  border-radius: 25px;
  background: black;
  overflow: hidden;
  margin-top: 30vh;
  margin-left: 20px;
}

.close {
  font-family: "Pacifico", cursive;
  font-size: 20px;
  line-height: 30px;
  width: 30px;
  transform: translate(450px, 10px);
  background: rgba(255, 255, 255, 0.8);
  border-radius: 20px;
  text-align: center;
  cursor: pointer;
  box-shadow: 1px 1px 4px #333;
}

.intro {
  position: fixed;
  text-align: center;
  font-family: "Pacifico", cursive;
  width: 100%;
  font-weight: 400;
  height: 15vh;
}

/* This one is just to create an animation effect in the text */
/* although we can create the same effect with GSAP, but just have it in CSS */

.gradient {
  background-image: linear-gradient(
    90deg,
    rgba(94, 114, 235, 1) 0%,
    rgba(255, 145, 144, 1) 56%,
    rgba(254, 193, 149, 1) 100%
  );
  color: transparent;
  background-clip: text;
  -webkit-background-clip: text;

  animation: move 1s infinite;
}

@keyframes move {
  50% {
    background-image: linear-gradient(
      262deg,
      rgba(94, 114, 235, 1) 0%,
      rgba(255, 145, 144, 1) 56%,
      rgba(254, 193, 149, 1) 100%
    );
  }
}

```

That's done with Styling and source, this is how it looks at this point. But still the main portion is remaining.


![image.png](https://cdn.hashnode.com/res/hashnode/image/upload/v1652603289402/Oiwc_VNEv.png align="center")

Let's now, add life to the project, I mean to add JavaScript to it to make it alive. 🤩 Here is the JavaScript code we need. 

```jsx
let active;

// toArray method is used to convert the certain collection into an Array!
// here it converts the set of expander elements into an Array.
let expanders = gsap.utils.toArray(".expander");
// gsap.util provides access to surprisingly helpful utility functions in GSAP

// forEach method in JavaScript is used to call a function for each element of an Array

expanders.forEach(function (expander, index) {
  let close = expander.querySelector(".close");
  let animation = gsap.timeline({ paused: true });

// animation applied to each element of the array = expander
  animation.to(expander, { width: 500, duration: 0.3 });

  // assign the animation to the current element
  expander.animation = animation;

  expander.addEventListener("click", function () {
    if (active) {
      active.animation.reverse(); // Reverse active Elements animation to close
    }

    // Play the clicked element's animtion to open
    expander.animation.play();

    active = expander;
  });

  close.addEventListener("click", function (event) {
    event.stopPropagation();  
// stopPropogation() method of an Event interface prevents it's further propogation

    expander.animation.reverse();
// reverse() is used to reverse the complete animation when the close is clicked.
  });

  console.log(expander);
});

// gsap.set() immediately set the properties for the target elements
// here we have set the bgColor to the elements of the expander array! 
gsap.set(".expander", {
  backgroundColor: gsap.utils.wrap([
    "#0993d3cc",
    "#024307",
    "#e1f326",
    "#1d134dee",
    "#e3117a",
  ]),
});
```

Okay now, finally we have done with the final JavaScript part too. I tried my best to explain you the *events*, *function*, *methods* used in the above JavaScript code using the comments, Also, I assume that you already know JavaScript fundamentals.

**Lastly let's have a look to the live CodePen view:** 

%[https://codepen.io/Kumar_Sons_off/pen/dydRYLz]

So finally, we have covered the basic fundamentals of GSAP and implemented them in a fun project. Hope you get a quick feel to GSAP animation library.

![That's wrap up!](https://cdn.hashnode.com/res/hashnode/image/upload/v1653020000422/VSp-HO5Xf.webp align="center")

<hr/>

## Conclusion

- We have covered the basic yet the most important functionalities of the GSAP.
- I highly recommend you to keep your CSS strong too, this is something that is really really important, and keep learning. 😊
- If you enjoyed this one, and If you find this helpful, consider sharing it with your friends & audience. 
- I'm still experimenting with GSAP, so more crazy articles can come in the upcoming days, so follow @[Priyanshu](@kumarsonsoff3) to stay tuned. 😉
- You can Join me on [🐦 Twitter](https://twitter.com/Kumar_Sons_off) to get the latest updates, tips, insights, and developer resources from me more frequently.

That's wrap up, Thank you for Reading. See you in the next one! 😊