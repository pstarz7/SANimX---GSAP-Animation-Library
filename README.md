[![Open Source](https://badges.frapsoft.com/os/v1/open-source.svg?v=103)](https://opensource.org/)
![Green Sock](https://img.shields.io/badge/green%20sock-88CE02?style=for-the-badge&logo=greensock&logoColor=white)
[![Free to Use](https://img.shields.io/badge/Free-🚀-orange)](https://github.com/your-repo)


# **SANimX:** Open-Source GSAP Animation Library
A ready-to-use GSAP animation library that you can simply copy and paste into your projects.

## Screenshots

![logo](https://github.com/pstarz7/SANimX---GSAP-Animation-Library/blob/364c64b3ec189d8043724d2557d3d68983662385/Screenshot%202025-04-22%20121216.png)



## Features

- Easy Installation
- Comprehensive Animation Properties
- Quick Start Examples
- Animation Catalog
- Easing Functions Reference
- Advance GSAP Effect's


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

# SIMPLE NAV ANIMATIONS 

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


# Cards Effects

### 3D Card Flip on Scroll

```CSS
   .card-container {
      display: flex;
      justify-content: center;
      gap: 30px;
      padding: 100px 0;
      perspective: 1000px;
    }
    
    .card {
      width: 300px;
      height: 400px;
      position: relative;
      transform-style: preserve-3d;
      transition: transform 0.5s;
    }
    
    .card-front, .card-back {
      position: absolute;
      width: 100%;
      height: 100%;
      backface-visibility: hidden;
      border-radius: 15px;
      display: flex;
      align-items: center;
      justify-content: center;
      font-size: 24px;
      color: white;
    }
    
    .card-front {
      background: linear-gradient(45deg, #6E40F7, #00F0B5);
    }
    
    .card-back {
      background: linear-gradient(45deg, #FF4D4D, #F9CB28);
      transform: rotateY(180deg);
    }
```

```HTML
  <div class="card-container">
    <div class="card">
      <div class="card-front">Front Content</div>
      <div class="card-back">Back Content</div>
    </div>
    <!-- Add more cards as needed -->
  </div>
```
```javascript
   gsap.registerPlugin(ScrollTrigger);
    
    gsap.utils.toArray(".card").forEach((card, i) => {
      gsap.to(card, {
        scrollTrigger: {
          trigger: card,
          start: "top 80%",
          toggleActions: "play none none none"
        },
        rotationY: 180,
        duration: 1.5,
        ease: "power3.out"
      });
    });
```

### Gradient Shift Parallax
```CSS
   .gradient-section {
      min-height: 300vh;
      background: linear-gradient(135deg, #6E40F7, #00F0B5);
      position: relative;
    }
    
    .content {
      position: sticky;
      top: 0;
      height: 100vh;
      display: flex;
      align-items: center;
      justify-content: center;
      color: white;
      font-size: 3rem;
      mix-blend-mode: overlay;
    }
    
    @media (max-width: 768px) {
      .content {
        font-size: 2rem;
      }
    }
```

```HTML
 <section class="gradient-section">
    <div class="content">
      <h1>Scroll to Shift Colors</h1>
    </div>
  </section>
```
```javascript
    gsap.registerPlugin(ScrollTrigger);
    
    gsap.to(".gradient-section", {
      background: "linear-gradient(135deg, #FF4D4D, #F9CB28)",
      scrollTrigger: {
        trigger: ".gradient-section",
        start: "top top",
        end: "bottom bottom",
        scrub: true
      }
    });
```


###  Perspective Tilt Scrolling

```CSS
.tilt-section {
      min-height: 200vh;
      perspective: 1000px;
      padding: 20vh 0;
    }
    
    .tilt-card {
      width: 80%;
      max-width: 600px;
      height: 400px;
      margin: 0 auto 50vh;
      background: linear-gradient(45deg, #6E40F7, #00F0B5);
      border-radius: 20px;
      display: flex;
      align-items: center;
      justify-content: center;
      color: white;
      font-size: 2rem;
      transform-style: preserve-3d;
      box-shadow: 0 30px 50px rgba(0,0,0,0.2);
    }
    
    @media (max-width: 768px) {
      .tilt-card {
        width: 90%;
        height: 300px;
      }
    }
```

```HTML
 <section class="tilt-section">
    <div class="tilt-card">Card 1</div>
    <div class="tilt-card">Card 2</div>
    <div class="tilt-card">Card 3</div>
  </section>
```
```javascript
  gsap.registerPlugin(ScrollTrigger);
    
    gsap.utils.toArray(".tilt-card").forEach((card, i) => {
      gsap.to(card, {
        rotationX: -15,
        rotationY: i % 2 ? 20 : -20,
        scrollTrigger: {
          trigger: card,
          start: "top bottom",
          end: "top center",
          scrub: 1
        }
      });
      
      // Reset on mobile
      ScrollTrigger.matchMedia({
        "(max-width: 600px)": () => {
          gsap.set(card, { rotationX: 0, rotationY: 0 });
        }
      });
    });
```
    
### Perspective Tilt Card (Hover + Scroll Reveal)
```CSS
   .cards-container {
      display: grid;
      grid-template-columns: repeat(auto-fit, minmax(300px, 1fr));
      gap: 30px;
      padding: 2rem;
      max-width: 1400px;
      margin: 0 auto;
      perspective: 1000px;
    }

    .card {
      background: white;
      border-radius: 16px;
      padding: 2rem;
      box-shadow: 0 10px 30px rgba(0,0,0,0.1);
      transform-style: preserve-3d;
      will-change: transform;
      opacity: 0;
      transform: translateY(50px);
    }

    @media (max-width: 768px) {
      .cards-container {
        grid-template-columns: 1fr;
      }
    }
```

```HTML
  <div class="cards-container">
    <div class="card">
      <h3>Card 1</h3>
      <p>Hover and scroll to see effects</p>
    </div>

 <div class="card">
      <h3>Card 2</h3>
      <p>Hover and scroll to see effects</p>
    </div>

<div class="card">
      <h3>Card 3</h3>
      <p>Hover and scroll to see effects</p>
    </div>
    <!-- Duplicate 5-6 cards -->
  </div>
```
```javascript
 gsap.registerPlugin(ScrollTrigger);

    // Scroll reveal
    gsap.to(".card", {
      scrollTrigger: {
        trigger: ".cards-container",
        start: "top 80%",
        toggleActions: "play none none none"
      },
      y: 0,
      opacity: 1,
      duration: 1,
      stagger: 0.1,
      ease: "back.out(1.2)"
    });

    // Hover tilt
    document.querySelectorAll('.card').forEach(card => {
      card.addEventListener('mousemove', (e) => {
        const rect = card.getBoundingClientRect();
        const x = e.clientX - rect.left;
        const y = e.clientY - rect.top;
        
        gsap.to(card, {
          rotationY: gsap.utils.mapRange(0, rect.width, -5, 5, x),
          rotationX: gsap.utils.mapRange(0, rect.height, 5, -5, y),
          duration: 0.5
        });
      });
      
      card.addEventListener('mouseleave', () => {
        gsap.to(card, {
          rotationY: 0,
          rotationX: 0,
          duration: 0.7,
          ease: "elastic.out(1, 0.5)"
        });
      });
    });
```
    
###  Card Stack Expansion
```CSS
  .stack-container {
      max-width: 1200px;
      margin: 0 auto;
      padding: 2rem;
    }

    .card {
      background: linear-gradient(135deg, #6E40F7, #00F0B5);
      color: white;
      padding: 2rem;
      border-radius: 12px;
      margin-bottom: 20px;
      box-shadow: 0 4px 20px rgba(0,0,0,0.15);
      transform-origin: center top;
    }

    @media (min-width: 768px) {
      .stack-container {
        display: grid;
        grid-template-columns: repeat(3, 1fr);
        gap: 30px;
      }
      .card {
        margin-bottom: 0;
        transform: scale(0.9);
        opacity: 0;
      }
    }
```

```HTML
  <div class="stack-container">
    <div class="card">
      <h3>Feature 1</h3>
      <p>Responsive card that transforms layout</p>
    </div>

  <div class="card">
      <h3>Feature 2</h3>
      <p>Responsive card that transforms layout</p>
    </div>

  <div class="card">
      <h3>Feature 3</h3>
      <p>Responsive card that transforms layout</p>
    </div>
 
    <!-- Add 5-6 cards -->
  </div>
```
```javascript
   gsap.registerPlugin(ScrollTrigger);

    // Only animate on desktop
    if (window.innerWidth >= 768) {
      gsap.to(".card", {
        scrollTrigger: {
          trigger: ".stack-container",
          start: "top 70%",
          toggleActions: "play none none none"
        },
        scale: 1,
        opacity: 1,
        duration: 0.8,
        stagger: {
          each: 0.15,
          from: "random"
        },
        ease: "back.out(1.7)"
      });
    }

    // Handle resize
    window.addEventListener('resize', () => {
      ScrollTrigger.refresh();
    });
```

### Horizontal Scrolling Gallery
```CSS
.horizontal-section {
      height: 100vh;
      overflow: hidden;
      position: relative;
    }
    
    .horizontal-container {
      display: flex;
      height: 100%;
    }
    
    .panel {
      min-width: 100vw;
      height: 100%;
      display: flex;
      justify-content: center;
      align-items: center;
      font-size: 5rem;
      color: white;
      position: relative;
    }
    
    .panel:nth-child(odd) { background: #6E40F7; }
    .panel:nth-child(even) { background: #00F0B5; }
    
    .parallax-element {
      position: absolute;
      width: 200px;
      height: 200px;
      background: #FF4D4D;
      border-radius: 50%;
    }
```

```HTML
  <section class="horizontal-section">
    <div class="horizontal-container">
      <div class="panel">
        <h2>Slide 1</h2>
        <div class="parallax-element" style="top:20%; left:20%"></div>
      </div>
      <div class="panel">
        <h2>Slide 2</h2>
        <div class="parallax-element" style="bottom:30%; right:15%"></div>
      </div>
      <div class="panel">
        <h2>Slide 3</h2>
        <div class="parallax-element" style="top:50%; left:50%"></div>
      </div>
    </div>
  </section>
```
```javascript
  gsap.registerPlugin(ScrollTrigger);
    
    let panels = gsap.utils.toArray(".panel");
    let container = document.querySelector(".horizontal-container");
    
    // Horizontal scroll
    gsap.to(panels, {
      xPercent: -100 * (panels.length - 1),
      ease: "none",
      scrollTrigger: {
        trigger: ".horizontal-section",
        pin: true,
        scrub: 1,
        end: () => "+=" + (container.offsetWidth - window.innerWidth)
      }
    });
    
    // Parallax elements
    gsap.utils.toArray(".parallax-element").forEach(el => {
      gsap.to(el, {
        y: 100,
        scrollTrigger: {
          containerAnimation: ScrollTrigger.getById("horizontal-scroll"),
          trigger: el,
          scrub: true
        }
      });
    });
```
    
### Staggered Grid Reveal
```CSS
 .grid-container {
    display: grid;
    grid-template-columns: repeat(auto-fit, minmax(250px, 1fr));
    gap: 20px;
    padding: 30px;
    width: 90%;
    margin: 0 auto;
  }
  
  .grid-item {
    background: linear-gradient(135deg, #6E40F7, #00F0B5);
    aspect-ratio: 1/1;
    border-radius: 10px;
    opacity: 0;
    transform: scale(0.8);
  }

  @media (max-width: 600px) {
    .grid-container {
      grid-template-columns: 1fr;
      padding: 20px 15px;
      gap: 15px;
    }
  }
```

```HTML
  <div class="grid-container">
    <!-- 9 grid items -->
    <div class="grid-item"></div>
    <div class="grid-item"></div>
    <div class="grid-item"></div>
    <div class="grid-item"></div>
    <div class="grid-item"></div>
    <div class="grid-item"></div>
    <div class="grid-item"></div>
    <div class="grid-item"></div>
    <div class="grid-item"></div>
  </div>
```
```javascript
 gsap.registerPlugin(ScrollTrigger);
  
  const gridAnimation = () => {
    gsap.to(".grid-item", {
      scrollTrigger: {
        trigger: ".grid-container",
        start: "top 80%",
        toggleActions: "play none none none",
        markers: false
      },
      opacity: 1,
      scale: 1,
      duration: 0.8,
      stagger: {
        each: window.innerWidth < 600 ? 0.05 : 0.1,
        grid: "auto",
        from: "center"
      },
      ease: "back.out(1.2)"
    });
  };

  // Initialize and refresh on resize
  gridAnimation();
  window.addEventListener('resize', () => {
    ScrollTrigger.refresh();
    gsap.killTweensOf(".grid-item");
    gridAnimation();
  });
```


### Morphing Card (Mobile-Friendly)

```CSS
    .morph-container {
      padding: 100px 2rem;
      display: flex;
      justify-content: center;
    }

    .morph-card {
      width: 90%;
      max-width: 500px;
      height: 300px;
      background: #6E40F7;
      border-radius: 20px;
      display: flex;
      align-items: center;
      justify-content: center;
      color: white;
      will-change: border-radius, background;
    }

    @media (max-width: 600px) {
      .morph-card {
        height: 200px;
      }
    }

```

```HTML
 <div class="morph-container">
    <div class="morph-card">
      <h2>Scroll Down</h2>
    </div>
  </div>
```


```javascript
   gsap.registerPlugin(ScrollTrigger);

    // Set up the animation timeline
    const tl = gsap.timeline({
      scrollTrigger: {
        trigger: ".morph-container",
        start: "top center",
        end: "+=1000",
        scrub: 1,
        pin: true,
        anticipatePin: 1,
        markers: false // Set to true for debugging
      }
    });

    // Morph animation sequence
    tl.to(".morph-card", {
      borderRadius: "50%",
      background: "#00F0B5",
      duration: 0.5
    })
    .to(".morph-card", {
      borderRadius: "10px",
      background: "#FF4D4D",
      duration: 0.5
    })
    .to(".morph-card", {
      borderRadius: "0",
      background: "#F9CB28",
      duration: 0.5
    })
    .to(".morph-card", {
      borderRadius: "20px",
      background: "#6E40F7",
      duration: 0.5
    });

    // Mobile fallback
    if (window.innerWidth < 768) {
      ScrollTrigger.getById(tl.scrollTrigger.id).kill();
      gsap.to(".morph-card", {
        scrollTrigger: {
          trigger: ".morph-container",
          start: "top center",
          toggleActions: "play none none none"
        },
        background: "#00F0B5",
        duration: 1
      });
    }
```

# Forms Effects

### Floating Label Input (3D Tilt on Focus)

```CSS
  .input-section {
      padding: 4rem 2rem;
      max-width: 800px;
      margin: 0 auto;
    }
    
    .input-group {
      position: relative;
      margin-bottom: 2rem;
      perspective: 1000px;
      opacity: 0;
      transform: translateY(30px);
    }
    
    .input-field {
      width: 100%;
      padding: 1.2rem 1rem 0.5rem;
      border: none;
      border-bottom: 2px solid #6E40F7;
      background: rgba(110, 64, 247, 0.05);
      border-radius: 8px 8px 0 0;
      font-size: 1rem;
      transition: all 0.3s;
      transform-style: preserve-3d;
    }
    
    .input-label {
      position: absolute;
      left: 1rem;
      top: 50%;
      transform: translateY(-50%);
      color: #6E40F7;
      transition: all 0.3s;
      pointer-events: none;
    }
    
    .input-field:focus {
      outline: none;
      background: rgba(110, 64, 247, 0.1);
      box-shadow: 0 5px 15px rgba(110, 64, 247, 0.2);
    }
    
    .input-field:focus + .input-label,
    .input-field:not(:placeholder-shown) + .input-label {
      top: 0.8rem;
      transform: translateY(0) scale(0.8);
      color: #00F0B5;
    }
    
    @media (max-width: 600px) {
      .input-section {
        padding: 2rem 1rem;
      }
    }
```

```HTML
  <section class="input-section">
    <div class="input-group">
      <input type="text" class="input-field" id="name" placeholder=" ">
      <label for="name" class="input-label">Full Name</label>
    </div>
    
    <div class="input-group">
      <input type="email" class="input-field" id="email" placeholder=" ">
      <label for="email" class="input-label">Email Address</label>
    </div>
    
    <div class="input-group">
      <input type="password" class="input-field" id="password" placeholder=" ">
      <label for="password" class="input-label">Password</label>
    </div>
  </section>
```
```javascript
    gsap.registerPlugin(ScrollTrigger);
    
    // Scroll-triggered entrance
    gsap.to(".input-group", {
      scrollTrigger: {
        trigger: ".input-section",
        start: "top 70%",
        toggleActions: "play none none none"
      },
      y: 0,
      opacity: 1,
      duration: 0.8,
      stagger: 0.15,
      ease: "back.out(1.7)"
    });
    
    // 3D tilt on focus
    document.querySelectorAll('.input-field').forEach(input => {
      input.addEventListener('focus', () => {
        gsap.to(input, {
          rotationY: 5,
          rotationX: 2,
          duration: 0.5,
          ease: "power2.out"
        });
      });
      
      input.addEventListener('blur', () => {
        gsap.to(input, {
          rotationY: 0,
          rotationX: 0,
          duration: 0.7,
          ease: "elastic.out(1, 0.5)"
        });
      });
    });

```


### Neon Glow Input (Scroll-Triggered Wave Effect)
```CSS
    .neon-section {
      padding: 4rem 2rem;
      background: #1a1a2e;
      color: white;
      min-height: 100vh;
      display: flex;
      flex-direction: column;
      justify-content: center;
    }
    
    .neon-input {
      width: 100%;
      max-width: 500px;
      margin: 2rem auto;
      position: relative;
    }
    
    .neon-input input {
      width: 100%;
      padding: 1rem;
      background: transparent;
      border: none;
      border-bottom: 2px solid #00F0B5;
      color: white;
      font-size: 1.1rem;
      opacity: 0;
      transform: translateX(-50px);
    }
    
    .neon-input input:focus {
      outline: none;
    }
    
    .neon-input::after {
      content: '';
      position: absolute;
      bottom: 0;
      left: 0;
      width: 0;
      height: 2px;
      background: linear-gradient(90deg, transparent, #00F0B5, #FF4D4D, transparent);
      box-shadow: 0 0 10px #00F0B5, 0 0 20px #FF4D4D;
      transition: width 0.3s;
    }
    
    .neon-input input:focus::after {
      width: 100%;
    }
    
    @media (max-width: 768px) {
      .neon-section {
        padding: 2rem 1rem;
      }
    }
```

```HTML
  <section class="neon-section">
    <div class="neon-input">
      <input type="text" placeholder="Username">
    </div>
    <div class="neon-input">
      <input type="email" placeholder="Email">
    </div>
    <div class="neon-input">
      <input type="password" placeholder="Password">
    </div>
```

```javascript
 gsap.registerPlugin(ScrollTrigger);
    
    // Wave animation on scroll
    gsap.utils.toArray(".neon-input").forEach((input, i) => {
      gsap.to(input.querySelector("input"), {
        scrollTrigger: {
          trigger: input,
          start: "top 80%",
          toggleActions: "play none none none"
        },
        x: 0,
        opacity: 1,
        duration: 0.8,
        delay: i * 0.2,
        ease: "power3.out"
      });
      
      // Animate the neon line
      ScrollTrigger.create({
        trigger: input,
        start: "top 90%",
        onEnter: () => {
          gsap.fromTo(input.querySelector("input"), 
            { boxShadow: "0 0 5px #00F0B5" },
            { 
              boxShadow: "0 0 20px #00F0B5, 0 0 40px #FF4D4D",
              duration: 1,
              yoyo: true,
              repeat: 1 
            }
          );
        }
      });
    });
```

### Material Input with Ripple Effect

```CSS
   .material-section {
      padding: 4rem 2rem;
      max-width: 600px;
      margin: 0 auto;
    }
    
    .material-input {
      position: relative;
      margin: 2rem 0;
      overflow: hidden;
      border-radius: 4px;
      background: #f5f5f5;
      transform: scale(0.95);
      opacity: 0;
    }
    
    .material-input input {
      width: 100%;
      padding: 1.5rem 1rem 0.5rem;
      border: none;
      background: transparent;
      font-size: 1rem;
    }
    
    .material-input label {
      position: absolute;
      left: 1rem;
      top: 1rem;
      color: #666;
      transition: all 0.3s;
    }
    
    .material-input .ripple {
      position: absolute;
      background: rgba(110, 64, 247, 0.2);
      border-radius: 50%;
      transform: scale(0);
      pointer-events: none;
      opacity: 0;
    }
    
    .material-input input:focus + label {
      top: 0.3rem;
      font-size: 0.8rem;
      color: #6E40F7;
    }
    
    @media (max-width: 600px) {
      .material-section {
        padding: 2rem 1rem;
      }
    }
```

```HTML
  <section class="material-section">
    <div class="material-input">
      <input type="text" id="m-name" required>
      <label for="m-name">Full Name</label>
    </div>
    
    <div class="material-input">
      <input type="email" id="m-email" required>
      <label for="m-email">Email</label>
    </div>
    
    <div class="material-input">
      <input type="password" id="m-pass" required>
      <label for="m-pass">Password</label>
    </div>
  </section>
```

```javascript
  gsap.registerPlugin(ScrollTrigger);
    
    // Scroll entrance
    gsap.to(".material-input", {
      scrollTrigger: {
        trigger: ".material-section",
        start: "top 70%",
        toggleActions: "play none none none"
      },
      scale: 1,
      opacity: 1,
      duration: 0.7,
      stagger: 0.15,
      ease: "elastic.out(1, 0.5)"
    });
    
    // Ripple effect
    document.querySelectorAll('.material-input').forEach(container => {
      const input = container.querySelector('input');
      
      input.addEventListener('focus', (e) => {
        const ripple = document.createElement('span');
        ripple.classList.add('ripple');
        container.appendChild(ripple);
        
        const rect = container.getBoundingClientRect();
        const size = Math.max(rect.width, rect.height);
        const x = e.clientX - rect.left - size/2;
        const y = e.clientY - rect.top - size/2;
        
        gsap.set(ripple, {
          width: size,
          height: size,
          left: x,
          top: y
        });
        
        gsap.to(ripple, {
          scale: 3,
          opacity: 1,
          duration: 0.6,
          ease: "power2.out",
          onComplete: () => {
            ripple.remove();
          }
        });
      });
    });
```
# Video Scroll Effects
###  Scroll-Activated Video Parallax
Effect: Video playback speed tied to scroll position


```CSS
.video-section {
      height: 300vh;
      position: relative;
    }
    
    .video-container {
      position: sticky;
      top: 0;
      height: 100vh;
      overflow: hidden;
    }
    
    video {
      width: 100%;
      height: 100%;
      object-fit: cover;
    }
    
    .overlay {
      position: absolute;
      top: 0;
      left: 0;
      width: 100%;
      height: 100%;
      background: rgba(0,0,0,0.3);
      display: flex;
      align-items: center;
      justify-content: center;
      color: white;
      font-size: 3rem;
    }
    
    @media (max-width: 768px) {
      .overlay {
        font-size: 2rem;
      }
    }
```

```HTML
  <section class="video-section">
    <div class="video-container">
      <video src="parallax-video.mp4" muted loop></video>
      <div class="overlay">
        <h1>Scroll to Control Video</h1>
      </div>
    </div>
  </section>

```

```javascript
  gsap.registerPlugin(ScrollTrigger);
    
    const video = document.querySelector('video');
    video.playbackRate = 0.5;
    
    ScrollTrigger.create({
      trigger: ".video-section",
      start: "top top",
      end: "bottom bottom",
      onUpdate: (self) => {
        video.currentTime = video.duration * self.progress;
      }
    });
    
    // Mobile fallback
    ScrollTrigger.matchMedia({
      "(max-width: 600px)": () => {
        video.playbackRate = 1;
        video.autoplay = true;
      }
    });
```


### Parallax Video Reveal (Mask Animation)
Effect: Video reveals through dynamic shapes as you scroll


```CSS
 .video-mask-section {
      height: 300vh;
      position: relative;
      background: #000;
    }
    
    .video-container {
      position: sticky;
      top: 0;
      height: 100vh;
      display: flex;
      align-items: center;
      justify-content: center;
      overflow: hidden;
    }
    
    .masked-video {
      width: 80%;
      height: 80%;
      object-fit: cover;
      clip-path: circle(10% at 50% 50%);
    }
    
    .content {
      position: absolute;
      top: 50%;
      left: 50%;
      transform: translate(-50%, -50%);
      color: white;
      text-align: center;
      z-index: 10;
      mix-blend-mode: difference;
    }
    
    @media (max-width: 768px) {
      .masked-video {
        width: 100%;
        height: 60%;
      }
    }
```

```HTML
  <section class="video-mask-section">
    <div class="video-container">
      <video class="masked-video" src="reveal-video.mp4" muted loop></video>
      <div class="content">
        <h1>Scroll to Reveal</h1>
      </div>
    </div>
  </section>
```
```javascript
 gsap.registerPlugin(ScrollTrigger);
    
    const video = document.querySelector('.masked-video');
    
    // Video scrub
    ScrollTrigger.create({
      trigger: ".video-mask-section",
      start: "top top",
      end: "bottom bottom",
      onUpdate: self => {
        video.currentTime = video.duration * self.progress;
      }
    });
    
    // Mask animation
    gsap.to(".masked-video", {
      clipPath: "circle(100% at 50% 50%)",
      scrollTrigger: {
        trigger: ".video-mask-section",
        start: "top center",
        end: "bottom center",
        scrub: true
      }
    });
    
    // Mobile fallback
    ScrollTrigger.matchMedia({
      "(max-width: 600px)": () => {
        gsap.set(".masked-video", { clipPath: "circle(75% at 50% 50%)" });
        video.autoplay = true;
      }
    });
```
    


### Video Depth Wipe (Foreground/Background)
Effect: Foreground video scrubs while background video plays continuously


```CSS
 .video-wipe-section {
      height: 400vh;
      position: relative;
    }
    
    .background-video, .foreground-video {
      position: fixed;
      top: 0;
      left: 0;
      width: 100%;
      height: 100%;
      object-fit: cover;
      z-index: 1;
    }
    
    .foreground-video {
      z-index: 2;
      clip-path: polygon(0 0, 100% 0, 100% 0, 0 0);
    }
    
    .content {
      position: relative;
      z-index: 3;
      color: white;
      padding: 20vh 10vw;
      mix-blend-mode: difference;
    }
    
    @media (max-width: 768px) {
      .foreground-video {
        display: none;
      }
      .content {
        padding: 10vh 5vw;
      }
    }
```

```HTML
  <section class="video-wipe-section">
    <video class="background-video" src="bg-loop.mp4" muted loop autoplay></video>
    <video class="foreground-video" src="fg-scrub.mp4" muted></video>
    <div class="content">
      <h1>Scroll to Wipe Between Videos</h1>
    </div>
  </section>
```
```javascript
  gsap.registerPlugin(ScrollTrigger);
    
    const foregroundVideo = document.querySelector('.foreground-video');
    
    // Foreground video scrub
    ScrollTrigger.create({
      trigger: ".video-wipe-section",
      start: "top top",
      end: "bottom bottom",
      onUpdate: self => {
        foregroundVideo.currentTime = foregroundVideo.duration * self.progress;
      }
    });
    
    // Wipe animation
    gsap.to(".foreground-video", {
      clipPath: "polygon(0 0, 100% 0, 100% 100%, 0 100%)",
      scrollTrigger: {
        trigger: ".video-wipe-section",
        start: "top center",
        end: "bottom center",
        scrub: true
      }
    });
```





# Button Hover Effects

###  Minimal Border Draw Effect

```CSS
   .btn-draw {
      position: relative;
      padding: 1rem 2rem;
      background: transparent;
      border: none;
      color: #222;
      font-size: 1rem;
      cursor: pointer;
      overflow: hidden;
    }
    
    .btn-draw::before,
    .btn-draw::after {
      content: '';
      position: absolute;
      width: 0;
      height: 2px;
      background: #222;
      transition: width 0.3s ease;
    }
    
    .btn-draw::before {
      top: 0;
      left: 0;
    }
    
    .btn-draw::after {
      bottom: 0;
      right: 0;
    }
    
    .btn-draw:hover::before,
    .btn-draw:hover::after {
      width: 100%;
    }
    
    @media (max-width: 768px) {
      .btn-draw {
        padding: 0.8rem 1.5rem;
      }
    }
```

```HTML
 <button class="btn-draw">Explore</button>
```

###  Subtle Fill Animation   
```CSS
 .btn-fill {
      position: relative;
      padding: 1rem 2rem;
      border: 2px solid #222;
      background: transparent;
      color: #222;
      font-size: 1rem;
      cursor: pointer;
      overflow: hidden;
      transition: color 0.3s;
      z-index: 1;
    }
    
    .btn-fill::before {
      content: '';
      position: absolute;
      top: 50%;
      left: 50%;
      width: 0;
      height: 0;
      background: #222;
      border-radius: 50%;
      transform: translate(-50%, -50%);
      transition: width 0.4s, height 0.4s;
      z-index: -1;
    }
    
    .btn-fill:hover {
      color: white;
    }
    
    .btn-fill:hover::before {
      width: 200%;
      height: 200%;
    }
    
    @media (max-width: 768px) {
      .btn-fill {
        padding: 0.8rem 1.5rem;
      }
    }
  </st
```

```HTML
  <button class="btn-fill">Discover</button>

```


### Underline Swipe Effect

```CSS
 .btn-swipe {
      position: relative;
      padding: 1rem 2rem;
      border: none;
      background: transparent;
      color: #222;
      font-size: 1rem;
      cursor: pointer;
    }
    
    .btn-swipe::after {
      content: '';
      position: absolute;
      bottom: 0;
      left: 0;
      width: 100%;
      height: 1px;
      background: #222;
      transform: scaleX(0);
      transform-origin: right;
      transition: transform 0.4s cubic-bezier(0.65, 0, 0.35, 1);
    }
    
    .btn-swipe:hover::after {
      transform: scaleX(1);
      transform-origin: left;
    }
    
    @media (max-width: 768px) {
      .btn-swipe {
        padding: 0.8rem 1.5rem;
      }
    }
```

```HTML
  <button class="btn-swipe">View Collection</button>

```


### 3D Lift Effect

```CSS
  .btn-lift {
      padding: 1rem 2rem;
      border: none;
      background: #222;
      color: white;
      font-size: 1rem;
      cursor: pointer;
      transition: transform 0.3s, box-shadow 0.3s;
      box-shadow: 0 4px 6px rgba(0,0,0,0.1);
    }
    
    .btn-lift:hover {
      transform: translateY(-3px);
      box-shadow: 0 6px 12px rgba(0,0,0,0.15);
    }
    
    .btn-lift:active {
      transform: translateY(1px);
      box-shadow: 0 2px 4px rgba(0,0,0,0.1);
    }
    
    @media (max-width: 768px) {
      .btn-lift {
        padding: 0.8rem 1.5rem;
      }
    }
```

```HTML
  <button class="btn-lift">Add to Cart</button>

```


###  Text Swap Animation
```CSS
    .btn-swap {
      position: relative;
      padding: 1rem 2rem;
      border: 1px solid #222;
      background: transparent;
      color: #222;
      font-size: 1rem;
      cursor: pointer;
      overflow: hidden;
    }
    
    .btn-swap span {
      display: inline-block;
      transition: transform 0.4s cubic-bezier(0.65, 0, 0.35, 1);
    }
    
    .btn-swap span:last-child {
      position: absolute;
      top: 50%;
      left: 50%;
      transform: translate(-50%, 150%);
    }
    
    .btn-swap:hover span:first-child {
      transform: translateY(-150%);
    }
    
    .btn-swap:hover span:last-child {
      transform: translate(-50%, -50%);
    }
    
    @media (max-width: 768px) {
      .btn-swap {
        padding: 0.8rem 1.5rem;
      }
    }
```

```HTML
 <button class="btn-swap">
    <span>Subscribe</span>
    <span>Thank You!</span>
  </button>
```

# MARQUEE Effects
```CSS
 .partners-section {
      padding: 4rem 0;
      background: #f8f8f8;
      overflow: hidden;
    }
    
    .marquee-container {
      display: flex;
      width: 100%;
      position: relative;
    }
    
    .marquee-track {
      display: flex;
      align-items: center;
      gap: 4rem;
      padding: 1rem 0;
      will-change: transform;
    }
    
    .marquee-item {
      flex: 0 0 auto;
      width: 160px;
      height: 80px;
      display: flex;
      align-items: center;
      justify-content: center;
      filter: grayscale(100%);
      opacity: 0.7;
      transition: all 0.3s ease;
    }
    
    .marquee-item:hover {
      filter: grayscale(0);
      opacity: 1;
      transform: scale(1.05);
    }
    
    .marquee-item img {
      max-width: 100%;
      max-height: 100%;
      object-fit: contain;
    }
    
    @media (max-width: 768px) {
      .marquee-item {
        width: 120px;
        height: 60px;
      }
      .marquee-track {
        gap: 2rem;
      }
    }
    
    @media (max-width: 480px) {
      .marquee-item {
        width: 100px;
        height: 50px;
      }
    }
```

```HTML

  <section class="partners-section">
    <div class="marquee-container">
      <div class="marquee-track" id="marquee1">
        <!-- Partner Logos - Duplicate for seamless loop -->
        <div class="marquee-item"><img src="logo1.svg" alt="Partner 1"></div>
        <div class="marquee-item"><img src="logo2.svg" alt="Partner 2"></div>
        <div class="marquee-item"><img src="logo3.svg" alt="Partner 3"></div>
        <div class="marquee-item"><img src="logo4.svg" alt="Partner 4"></div>
        <div class="marquee-item"><img src="logo5.svg" alt="Partner 5"></div>
        <div class="marquee-item"><img src="logo6.svg" alt="Partner 6"></div>
        <!-- Mirrored for seamless loop -->
        <div class="marquee-item"><img src="logo1.svg" alt="Partner 1"></div>
        <div class="marquee-item"><img src="logo2.svg" alt="Partner 2"></div>
        <div class="marquee-item"><img src="logo3.svg" alt="Partner 3"></div>
        <div class="marquee-item"><img src="logo4.svg" alt="Partner 4"></div>
        <div class="marquee-item"><img src="logo5.svg" alt="Partner 5"></div>
        <div class="marquee-item"><img src="logo6.svg" alt="Partner 6"></div>
      </div>
    </div>
  </section>
```
```javascript
    document.addEventListener('DOMContentLoaded', () => {
      const marquee = document.getElementById('marquee1');
      const items = gsap.utils.toArray('.marquee-item');
      const speed = 100; // pixels per second
      
      // Calculate total width
      let totalWidth = 0;
      items.forEach(item => {
        totalWidth += item.offsetWidth + parseInt(getComputedStyle(item).marginRight);
      });
      
      // Duplicate items for seamless looping
      const clone = marquee.cloneNode(true);
      marquee.parentNode.appendChild(clone);
      
      // Animation
      const tl = gsap.timeline({
        repeat: -1,
        defaults: { ease: "none" }
      });
      
      tl.to([marquee, clone], {
        x: `-=${totalWidth/2}`,
        duration: totalWidth / speed,
        modifiers: {
          x: gsap.utils.unitize(x => parseFloat(x) % (totalWidth/2))
        }
      });
      
      // Responsive handling
      function handleResize() {
        totalWidth = 0;
        items.forEach(item => {
          totalWidth += item.offsetWidth + parseInt(getComputedStyle(item).marginRight);
        });
        tl.invalidate();
      }
      
      window.addEventListener('resize', handleResize);
      
      // Cleanup
      return () => {
        window.removeEventListener('resize', handleResize);
        tl.kill();
      };
    });
```

###
```CSS
 body {
      cursor: none;
      margin: 0;
      overflow-x: hidden;
      min-height: 100vh;
      background: #0f0f1a;
    }
    
    .cursor-dot {
      width: 8px;
      height: 8px;
      background: #00F0B5;
      border-radius: 50%;
      position: fixed;
      pointer-events: none;
      mix-blend-mode: exclusion;
      z-index: 9999;
    }
    
    .cursor-particle {
      position: fixed;
      width: 4px;
      height: 4px;
      background: #6E40F7;
      border-radius: 50%;
      pointer-events: none;
      mix-blend-mode: exclusion;
      z-index: 9998;
    }
    
    @media (max-width: 768px) {
      body {
        cursor: default;
      }
      .cursor-dot, .cursor-particle {
        display: none;
      }
    }
```
## 𝗖𝗿𝗲𝗮𝘁𝗶𝘃𝗲 𝗖𝘂𝗿𝘀𝗼𝗿 𝗧𝗿𝗮𝗶𝗹 𝗘𝗳𝗳𝗲𝗰𝘁 

#Particle Trail Cursor
```HTML
Effects are applied to the <body> tag
```
```javascript
 // Main cursor dot
    const cursorDot = document.createElement('div');
    cursorDot.classList.add('cursor-dot');
    document.body.appendChild(cursorDot);
    
    // Particle array
    const particles = [];
    const particleCount = 12;
    
    // Create particles
    for (let i = 0; i < particleCount; i++) {
      const particle = document.createElement('div');
      particle.classList.add('cursor-particle');
      document.body.appendChild(particle);
      particles.push({
        element: particle,
        x: 0, y: 0,
        delay: i * 0.02,
        size: Math.random() * 3 + 2
      });
    }
    
    // Track mouse position
    let mouseX = 0, mouseY = 0;
    
    document.addEventListener('mousemove', (e) => {
      mouseX = e.clientX;
      mouseY = e.clientY;
    });
    
    // Animation loop
    gsap.ticker.add(() => {
      // Main cursor
      gsap.to(cursorDot, {
        x: mouseX - 4,
        y: mouseY - 4,
        duration: 0.2,
        ease: "power2.out"
      });
      
      // Particles
      particles.forEach((particle, i) => {
        const delay = particle.delay;
        const targetX = mouseX - particle.size/2;
        const targetY = mouseY - particle.size/2;
        
        gsap.to(particle.element, {
          x: targetX,
          y: targetY,
          duration: 0.5,
          delay: delay,
          ease: "power2.out",
          width: particle.size,
          height: particle.size,
          opacity: 0.7 - (i/particleCount * 0.5)
        });
      });
    });
    
    // Disable on touch devices
    const isTouchDevice = () => {
      return 'ontouchstart' in window || navigator.maxTouchPoints;
    };
    
    if (isTouchDevice()) {
      document.body.style.cursor = 'default';
      cursorDot.style.display = 'none';
      particles.forEach(p => p.element.style.display = 'none');
    }
```


# Stay Update with SANimX For Upcoming Effects

###
```CSS

```

```HTML

```
```javascript

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


![Logo](https://github.com/pstarz7/gsap-animation-library/blob/9f19a8cdc33e69e3761bd3b93cdf9297a93ce870/SANimX.png)


## Tech Stack

**Animation:** javaScript, GSAP, HTML AND CSS





