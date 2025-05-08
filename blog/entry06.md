# Entry 6: MVP Webpage (Personal Finance)
##### 5/7/25

## I kept it simple, for now...
**FINALLY!** We're here after a long time **(7 months to be exact)**. CREATING MY WEBPAGE FOR SOMETHING I AM PASSIONATE ABOUT: Personal Finance. Enough celebrating because this isn't the end of my journey; *work now, celebrate later.*

For some context, I am working on draft, **not finalizing my webpage** in one run or in other words, this is called a MVP **(Minimum Viable Product)**.

### BLUEPRINT (Wireframe)
* [Wireframe for desktop #1](../prep/wireframes/wireframe_desktop_1.png)
* [Wireframe for desktop #2](../prep/wireframes/wireframe_desktop_2.png)
* [Wireframe for mobile #1](../prep/wireframes/wireframe_mobile_1.png)
* [Wireframe for mobile #2](../prep/wireframes/wireframe_mobile_2.png)

## Parts of the MVP
Note: the code examples are just the **IMPORTANT** parts of the code. **ADDITIONALLY, I AM NOT GOING TO BREAK EVERYTHING DOWN ABOUT THE MVP, ONLY SIMPLE FUNDAMENTALS**

---
### The Home Section (my favorite part)
![home](b-images/home.png)

This is my favorite section because it looks satisfyingly simple, especially the green part. Additionally, the Navbar's black color blends so well with the green.

**For the Navbar, I copied and pasted the navbar template from [Bootstrap](https://getbootstrap.com/docs/5.3/components/navbar/#:~:text=Here%E2%80%99s%20an%20example%20of%20all%20the%20sub%2Dcomponents%20included%20in%20a%20responsive%20light%2Dthemed%20navbar%20that%20automatically%20collapses%20at%20the%20lg%20(large)%20breakpoint.)**
* I edited the id and name for each `nav-link` to my preference (e.g, **`#home`/ home** or **`#about`/ about**)
* I added `fixed-top` class to the `nav` and removed `bg-body-tertiary` so that I can use `style.css` to style the color of my navbar: Black.

**For the 'Green Section', I designed it myself**
* I used `padding`, `container`, and `d-flex justify-content-center` to create the structure of this section

``` html
<style>
    /* WORKS IF YOU REMOVE THE `bg-body-tertiary` */
    nav {
        background-color: #000000;
    }
    /* padding for the green section */
    .home-section {
        background-color: #165226;
        padding: 16em;
    }
</style>

<!-- NAVBAR -->
<nav class="navbar navbar-expand-lg fixed-top">
    ...
    <ul class="navbar-nav me-auto mb-2 mb-lg-0">
        <!-- nav-links -->
        <li class="nav-item">
            <a class="nav-link" aria-current="page" href="#home">Home</a>
        </li>
        <li class="nav-item">
            <a class="nav-link" href="#about">About</a>
        </li>
    </ul>
</nav>

<!-- GREEN SECTION -->
<header class= "container-fluid home-section" id="home">
    <!-- Container is used to box and center things -->
    <div class="container">
        <!-- d-flex justify-content-center is basically align center -->
        <h1 class="d-flex justify-content-center text-white resp-title">Personal Finance</h1>
        <p class="text-center d-flex justify-content-center text-white resp-desc">Ignorance is bliss or is it not? Your Journey Begins...</p>
        <div class="d-flex justify-content-center">
        <a href="#about" class="btn btn-light btn-lg mt-3">Learn More</a>
    </div>
</header>
```

### Information-Packed Sections
![info](b-images/info-packed.png)
I kept it with a simple and organized order for the information-packed sections: **The Left and Right Format**.

**I used alot of `col` and `order` bootstrap classes to organize it like this but it's easier than it seems, just a lot of copy and pasting and editing.**
* Using `order-lg-1` and `order-lg-2` are important in making it left and right because those classes literally mean order something first or second, starting from the left.
* `col-lg-6` and `col-md-12` are used for responsiveness; For larger (`lg`) screen sizes, information and image are each taking up half the space in their row thus two in one row. For medium (`md`) or lower screen sizes, the information and image stack on top of each other, each taking up a whole row.

``` html
<div class="container">
    <div class="row">
        <!-- title -->
        <h2 class="text-center ex-title-spacing display-6">...</h2>
        <!-- image #1 / first part -->
        <div class="col-lg-6 col-md-12 order-lg-2 text-center">
            <img src="images/nerdwallet.png" height="500" width="500">
        </div>
        <!-- information #1 -->
        <div class="col-lg-6 col-md-12 order-lg-1">
            <div class="spacing-bottom">
                <p>...</p>
                <p>...</p>
                <p>...</p>
                <p>...</p>
            </div>
        </div>
    </div>
    <div class="row ex-spacing">
        <!-- image #2 / second part -->
        <div class="col-lg-6 col-md-12 text-center">
            <img src="images/goodbudget.png" height="500" width="500">
        </div>
        <!-- information #2 -->
        <div class="col-lg-6 col-md-12">
            <div class="spacing-bottom text-lg-end">
                <p>...</p>
                <p>...</p>
                <p>...</p>
                <p>...</p>
            </div>
        </div>
    </div>
</div>
```
### Preview of Hardware ([A-Frame](https://aframe.io/))
![preview](b-images/mvp-preview.png)
### ↓
![scene](b-images/mvp-scene.png)

Pretty plan preview section and scene but it's something. I am planning to improve this via embedded scene instead of linking it.

**I created a section with a title and a button underneath it that links it to the A-Frame scene via href. The A-Frame Scene uses the basic entity/ shapes to form the model shown above including:**
* `<a-sky>`: used for background color.
* `<a-box/sphere>`: used for the head **(box)**, face **(sphere)**, and eyes **(sphere)**.
* `<a-entity text>`: used for text simply.

``` html
<!-- Preview section -->
<section class="mb-5">
    <h1 class="display-1 text-center mb-5">PREVIEW OF HARDWARE</h1>
    <div class="row d-flex justify-content-center">
        <div class="col-4">
            <div class="d-grid">
                <!-- Button that links to A-Frame scene -->
                <a class="btn btn-primary" href="aframe_scene.html" role="button">Open Preview</a>
            </div>
        </div>
    </div>
</section>
<!-- A-Frame Scene -->
<a-scene>
    <!-- gray background -->
    <a-sky color="gray"></a-sky>
    <!-- Model design begins -->
    <a-box position="0 2 -6" scale="3 3 3"></a-box>
    <a-sphere position="0 2 -4.5" scale="1.3 1 0.1" color="#141414"></a-sphere>
    <a-sphere position="-0.5 2 -4.5" scale="0.6 0.6 0.1" color="white"></a-sphere>
    <a-sphere position="0.5 2 -4.5" scale="0.6 0.6 0.1" color="white"></a-sphere>
    <!-- Model design ends -->
    <!-- The Greeting Text -->
    <a-entity text="value: Hello, I am DroidNosMoney! How can I help you?; color: #000000; width: 6; align: center"
    position="0 4 -4"
    scale="1.5 1.5 1.5">
    </a-entity>
</a-scene>
```

[Previous](entry05.md) | [Next](entry07.md)

[Home](../README.md)
