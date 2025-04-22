# SANimX - GSAP Animation Library

A ready-to-use GSAP animation library that you can simply copy and paste into your projects.

## Features

- Easy Installation
- Comprehensive Animation Properties
- Quick Start Examples
- Animation Catalog
- Easing Functions Reference

## Installation

### CDN Method

```javascript
<!-- GSAP Core -->
<script src="https://cdnjs.cloudflare.com/ajax/libs/gsap/3.12.2/gsap.min.js"></script>

<!-- Optional Plugins -->
<script src="https://cdnjs.cloudflare.com/ajax/libs/gsap/3.12.2/ScrollTrigger.min.js"></script>

```
    


## NPM Method

```bash
npm install gsap


```

## Core Animation Properties
#### Summary Cheat Sheet




Property | Example  | What It Does             |
| :-------- | :------- | :------------------------- |
| **duration** | `duration: 2` | Animation length (seconds) |
| **delay**    | `delay: 1` | Pause before starting |
| **ease**     | `ease: "power2.out"` | Speed curve |
| **stagger**  | `stagger: 0.2` | Delay between elements |
| **x, y**     | `x: 100, y: "50%"` | Movement |
| **rotation**    | `rotation: 360` | Spin effect |
| **scale**    | `scale: 1.5` | Resize |
| **opacity**    | `opacity: 0` | Fade in/out |
| **scrollTrigger**    | `scrollTrigger: { trigger: ".box" }` |Scroll-based animation  |
| **scrub**    | `scrub: true` | Smooth scroll sync |
| **element**    | ` #id, .class, tag` | Target element selector  |


## GSAP Easing Functions Reference

### Basic Power Eases
| Type | Description |
|------|-------------|
| `"power0"` / `"linear"` | Constant speed (no easing) |
| `"power1.in"` | Starts slow, ends fast |
| `"power1.out"` | Starts fast, ends slow |
| `"power1.inOut"` | Smooth acceleration & deceleration |
| `"power2.in"` | Stronger slow start |
| `"power2.out"` | Stronger fast finish |
| `"power2.inOut"` | More pronounced smooth easing |
| `"power3.in"` | Very slow start |
| `"power3.out"` | Very fast end |
| `"power3.inOut"` | Dramatic smooth easing |
| `"power4.in"` | Extremely slow start |
| `"power4.out"` | Extremely fast end |
| `"power4.inOut"` | Most intense smooth easing |

### Special Effect Eases
| Type | Description |
|------|-------------|
| `"bounce.in"` | Bouncy start |
| `"bounce.out"` | Bouncy ending |
| `"bounce.inOut"` | Bounces at both start and end |
| `"elastic.in(1, 0.5)"` | Springy start |
| `"elastic.out(1, 0.5)"` | Elastic spring effect |
| `"elastic.inOut(1, 0.5)"` | Springy both directions |
| `"back.in"` | Pulls back before starting |
| `"back.out"` | Overshoots at end |
| `"back.inOut"` | Overshoots both directions |

### Smooth Motion Eases
| Type | Description |
|------|-------------|
| `"sine.in"` | Gentle slow start |
| `"sine.out"` | Gentle slow end |
| `"sine.inOut"` | Gentle wave-like motion |
| `"circ.in"` | Circular slow start |
| `"circ.out"` | Circular fast end |
| `"circ.inOut"` | Smooth circular motion |
| `"expo.in"` | Extremely slow start |
| `"expo.out"` | Extremely fast end |
| `"expo.inOut"` | Sharp acceleration/deceleration |

### Customizable Parameters
| Type | Parameters | Description |
|------|------------|-------------|
| `"elastic"` | `(intensity, period)` | `(1, 0.5)` = default spring effect |
| `"back"` | `(overshoot)` | `(1.7)` = default overshoot amount |

> **Note**: All eases work with `gsap.to()`, `gsap.from()`, and `gsap.fromTo()`.  
> Try them in the [GSAP Ease Visualizer](https://greensock.com/docs/v3/Eases).

```javascript
// Bounce example
gsap.to(".box", { 
  x: 100, 
  ease: "bounce.out" 
});
```

## Quick Start Example

#### Besic  gsap  syntax

```javascript
gsap.to("element", {
  duration: 2, // Takes 2 seconds to complete
  x: 200,
});
```


#### gsap with scrollTrigger syntax

```javascript
// Fade in and slide up on scroll
gsap.from("element", {
  duration: 1,
  delay: 0.2,
  y: 50,
  opacity: 0,
  ease: "power2.out",
  stagger: 0.1,
  scrollTrigger: {
    trigger: "element",
    start: "top 90%", //scrollTriggring pont. you can adjust
    toggleActions: "play none none none",
  },
});
```




    
## ✨ Animation Catalog



 ###   Text Animations
 ```HTML
        <div class="text fade-up">Fade Up</div>
        <div class="text slide-in">Slide In</div>
        <div class="text pop-in">Pop In</div>
        <div class="text wave-text">Wave Motion</div>
        <div class="text stretch">Stretch Effect</div>
```
```javascript
        gsap.from(".fade-up", { opacity: 0, y: 30, duration: 1, ease: "power2.out" });
        gsap.from(".slide-in", { opacity: 0, x: -50, duration: 1, ease: "power2.out" });
        gsap.from(".pop-in", { scale: 0.5, opacity: 0, duration: 0.8, ease: "back.out(1.7)" });
        gsap.to(".wave-text", { rotation: 5, duration: 1.5, repeat: -1, yoyo: true, ease: "power1.inOut" });
        gsap.from(".stretch", { scaleX: 0.5, opacity: 0, duration: 1, ease: "power2.out" });
 ```






##  Animations For All element's

### Fade in
```javascript
  gsap.from(element, {
    opacity: 0,
    duration: 1,
    delay: 0,
    ease: "power2.out"
  });

```
### Slide in Left
```javascript
  gsap.from(element, {
    x: -100,
    opacity: 0,
    duration: 1,
    delay: 0,
    ease: "back.out(1.7)"
  });

```
### Slide in Right
```javascript
 gsap.from(element, {
    x: 100,
    opacity: 0,
    duration: 1,
    delay: 0,
    ease: "back.out(1.7)"
  });
 
```
### Bounce In
```javascript
 gsap.from(element, {
    y: -100,
    opacity: 0,
    duration: 1,
    delay: 0,
    ease: "bounce.out"
  });
 
```

### Scale Up
```javascript
gsap.from(element, {
    scale: 0,
    opacity: 0,
    duration: 1,
    delay: 0,
    ease: "elastic.out(1, 0.5)"
  });
 
```

### Rotate In
```javascript
gsap.from(element, {
    rotation: -180,
    opacity: 0,
    duration: 1,
    delay: 0,
    ease: "back.out(1.7)"
  });
 ```

 ### Staggered List Items
```javascript
gsap.from(container.children, {
    opacity: 0,
    y: 20,
    duration: 0.5,
    delay: 0,
    stagger: 0,
    ease: "power2.out"
  });
 ```

  ### Text Reveal
```javascript
gsap.from(element, {
    y: "100%",
    duration: 1,
    delay: 0,
    ease: "power3.out"
  });
 ```

   ### Flip In
```javascript
gsap.from(element, {
    rotationX: 90,
    opacity: 0,
    duration: 1,
    delay: 0,
    ease: "back.out(1.7)",
    transformOrigin: "50% 50%"
  });
 ```

   ###  Color Change
```javascript
gsap.to(element, {
    color:"#eeeeee" newColorNameInHexacode,
    duration: 1,
    delay: 0,
    ease: "power2.inOut"
  });
}
 ```

   ###  Background Color Change
```javascript
gsap.to(element, {
    backgroundColor: "#eeeeee" newColorNameInHexacode ,
    duration: 1,
    delay: 0,
    ease: "power2.inOut"
  });
 ```


   ###  Hover Pulse
```javascript
element.addEventListener("mouseenter", () => {
    gsap.to(element, {
      scale: 1.05,
      duration: 0.3,
      ease: "power2.out"
    });
  });
  
  element.addEventListener("mouseleave", () => {
    gsap.to(element, {
      scale: 1,
      duration: 0.3,
      ease: "power2.out"
    });
  });
 ```

  ###  Infinite Float
```javascript
gsap.to(element, {
    y: 10,
    duration: 3,
    repeat: -1,
    yoyo: true,
    ease: "sine.inOut"
  });
 ```

  ###  Infinite Rotation
```javascript
gsap.to(element, {
    rotation: 360,
    duration: 5,
    repeat: -1,
    ease: "none"
  });
 ```

  ###  Parallax Scroll
```javascript
function parallaxScroll(element, speed = 0.5) {
  gsap.to(element, {
    yPercent: speed * 100,
    ease: "none",
    scrollTrigger: {
      trigger: element,
      scrub: true
    }
  });
}
 ```

   ###  Scroll Triggered Fade In
```javascript
gsap.from(element, {
    opacity: 0,
    y: 50,
    duration: 1,
    scrollTrigger: {
      trigger: element,
      start: "top 80%",
      toggleActions: "play none none none"
    }
  });
 ```

 ###  Sequential Card Reveal
```javascript
function cardReveal(cards, stagger = 0.1, duration = 0.5) {
  return gsap.from(cards, {
    opacity: 0,
    y: 50,
    duration: duration,
    stagger: stagger,
    scrollTrigger: {
      trigger: cards[0].parentElement,
      start: "top 70%",
      toggleActions: "play none none none"
    }
  });
}
 ```

## SIMPLE NAV ANIMATIONS 
 ###  Navigation Animations Up-Down

```CSS
nav{
    width: 100%;
    height: 50px;
    display: flex;
    align-items: center;
    justify-content: space-between;
    padding: 3vw;
}

#nav-links{
  
    display: flex;
    align-items: center;
    justify-content: center;
    gap: 2vw;
}
```
 
```HTML
        <nav>
           <h1>pstar</h1>
                <div class="nav-links">
                    <a href="#">course</a>
                    <a href="#">about</a>
                    <a href="#">contactUs</a>
                    <a href="#">home</a>
              </div>
        </nav>
```

```javascript
var tl = gsap.timeline()

tl.from("#page1 h1",{
    y:-20,
    opacity:0,
    duration:1,
    dealy:0.5,
})


tl.from("a",{
    y:-20,
    opacity:0,
    duration:1,
    stagger:0.3
})


 ```


  ###  Navigation Animations Down-Up
```CSS
 nav { display: flex;
 justify-content: center; 
 gap: 20px; width: 100%;
}
 nav a {
 color: #bebebe;
 text-decoration: none;
 padding: 10px 15px;
 display: inline-block;
 position: relative;
 font-size: 1.2rem;
 }
```


 
```HTML
        <nav>
            <a href="#" class="nav-item">Home</a>
            <a href="#" class="nav-item">About</a>
            <a href="#" class="nav-item">Services</a>
            <a href="#" class="nav-item">Portfolio</a>
            <a href="#" class="nav-item">Contact</a>
        </nav>
```

```javascript
         gsap.from(".nav-item", { opacity: 0, y: 20, duration: 0.6, stagger: 0.2, ease: "power2.out" });

 ```

## 🚀 About Me
**Papu Badatya**
Frontend Developer | GSAP Animation Enthusiast

Hello! I’m a passionate frontend developer specializing in creating engaging web experiences. My toolkit includes:

Core: HTML5, CSS3, JavaScript (ES6+)

Frameworks: React, Tailwind CSS

Animation: GSAP + ScrollTrigger (expert-level implementations)

I built this **SANimX** library to help developers easily integrate stunning animations into their projects without the steep learning curve. Whether you’re a beginner or a seasoned dev, these ready-to-use GSAP snippets will save you hours of work!

### Why I made this?

- Simplify complex animations for everyone

- Provide copy-paste-friendly solutions

- Boost engagement through motion design

Let’s connect!
## 🔗 Links
[![portfolio](https://img.shields.io/badge/my_portfolio-000?style=for-the-badge&logo=ko-fi&logoColor=white)](https://my-portfolio-pb7.netlify.app/)
[![linkedin](https://img.shields.io/badge/linkedin-0A66C2?style=for-the-badge&logo=linkedin&logoColor=white)](https://www.linkedin.com/in/papu-badatya-759767254/)
[![twitter](https://img.shields.io/badge/twitter-1DA1F2?style=for-the-badge&logo=twitter&logoColor=white)](https://twitter.com/)


![Logo](https://github.com/pstarz7/gsap-animation-library/blob/9f19a8cdc33e69e3761bd3b93cdf9297a93ce870/SANimX.png)


## Tech Stack

**Animation:** javaScript, GSAP, HTML AND CSS



