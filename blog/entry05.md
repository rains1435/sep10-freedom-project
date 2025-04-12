# Entry 5: The ULTIMATE Tool (Personal Finance)
##### 04/11/25

## I made up my mind...

Sadly, JQuery was not chosen to be my forever until the very end; A-Frame was and is my final choice. Starting on the 4th of March, 2025, I began to tinker with other features A-Frame offered because I've already learned the basics of A-Frame: `entity`, their `position`, `rotation`, `color`, and `scale` (**Shown in [Entry 4](entry04.md)**). Anyways, let's begin...

**Here's a TL;DR list of what I've learned**

MUST READ->(Don't worry; I will be doing a full breakdown after this. Also I am only going to be covering NECESSARY ones, not easy ones; easy ones as in literally inputting texture or a already built background.)

**TOP 4:**

1) Creating a Custom Background
2) Animating an Entity(s)
3) Adding Text
4) Creating an Asset

Let's start at 4 to 1 (**It'll make more sense; trust me**)

---

### 4. Creating an Asset
Right after creating an `<a-scene>`, create an `<a-asset>` inside the scene.
``` html
<a-scene>
<!-- INSIDE HERE -->
    <a-asset>
        ...
    </a-asset>
    ...
</a-scene>
```

**The Importance:** Instead of conveniently inputting a texture, audio, or videos into `src` attributes, take the time to put all of those into an `<a-asset>`as it can help **preload** what ever you've inputted (**textures, videos, audio etc**).

``` html
<!-- Example: -->

<!-- This would load texture immediately (with asset) -->
<a-scene>
    <a-asset>
        <img id="shapePattern" src="shape.jpg">
    </a-asset>
    <a-box id="#shapePattern" scale="2 2 2" position="0 2 -5"></a-box>
</a-scene>

<!-- This would load texture with delay (without asset) -->
<a-scene>
    <a-box src="shape.jpg" scale="2 2 2" position="0 2 -5"></a-box>
</a-scene>
```
---
### 3. Adding Text
Having text in an A-Frame presentation is extremely important so here's a breakdown:
* The main focus, **the text** `text= "value: (input-text);"`

    * You may also add a color -> `color: (given-color);`
    * The width (**NOT IN px; HAS NOT UNIT**) -> `width: (numerical-value);`
    * The text-alignment similar to google doc's (**in a way**) -> `align: (set-alignment);`
    * ALL OF THIS SHOULD EXIST IN THE `text= "(in here)"`

**Code:**
``` html
<!-- In this example, I put the text above the box by using `align: center` and setting their x and z position the same while the text has a higher y value (to put it above).-->
<a-scene>
    <a-box position="-0.9 0.2 -3" scale="2 2 2" color="pink"></a-box>
    <a-entity text="value: Hello, A-Frame; color: #000000; width: 5; align: center"
    position="-0.9 2.4 -3"
    scale="1.5 1.5 1.5">
    </a-entity>
</a-scene>
<!-- IMPORTANT: text is an entity so it can have a position, rotation, color, and scale -->
```

**Output:**

![alt text](../tool/image-holder/add-text.png)

---
### 2. Animating an Entity
Imagine random shapes moving in an A-Frame presentation. Wouldn't that be cool or dynamical? That's why animation is #2.

**Breakdown:**
* `animation="property: object3D.position.x` = specify the object being animated
* `to: (numerical-value)`= distance object will travel based on position (**position.x or y**) (negative values move left, positive values move right).
* `dir: (direction-value)` = direction of object's movement
* `dur: (numerical-value)` = duration of animation (**in milliseconds**)
* `loop: (true-false)` = to loop animation

**Code:**

``` html
<a-scene>
  <a-box src="textures/wood.jpg" position="0 2 -5" scale="2 2 2" animation="property: object3D.position.x; to: 10; dir: alternate; dur: 1000; loop: true;"><a-box>
</a-scene>
```

**Output:**

https://github.com/user-attachments/assets/e2a6bd95-7846-4a49-8e67-36c986056e5a

---
### 1. Creating a Custom Background
This is a no brainer; this is most important as it is basically combining everything we've learned onto an A-Frame presentation but with a little extra steps.

**Breakdown:**

* `<a-sky>` + `color="..."` or `src="..."` gives the sky a color or if `src`, gives sky a texture or video or audio; depends on what file you put in there or whatever you put in `<a-asset>`. **Same applies for the steps that are below.**

* `<a-plane>` + `rotation= "-90 0 0"` <-- (**Note: this rotation configuration is default for ground**) + `color="..."` or `src="..."`  + `width="..."` + `height="..."` (**NOT IN "px", just numbers with no unit**)

    * Add `repeat="10 10"` if width and height is 100. If more, set increase both values of `repeat="v1 v2"` to your liking (**APPLIES TO GROUNDS WITH TEXTURES, COLOR**). `repeat` repeats the applied textures across an entity; pattern.

* `<a-light>` (**Create two separate ones; The order doesn't matter**)

    * First `a-light`, give it a `type= "ambient"` (**applied to all**) + `color="..."` (**NO TEXTURE NEEDED FOR `a-light`**)

    * Second `a-light`, give it a `type= "point"` (**light bulb**) + `intensity= "(numerical; no unit)"` + `position="x y z"` <-- (**in numerical; no unit**)

**Code:** LET'S PUT EVERYTHING TOGETHER, INCLUDING THE BASICS AND THE PREVIOUS.

``` html
<a-scene>
    <a-assets>
        <img id="grassTexture" src="textures/grass.jpg">
        <img id="logTexture" src="textures/tree-log.jpg">
        <img id="galaxyTexture" src="textures/galaxy.jpg">
        <img id="autumnleavesTexture" src="textures/tree-leaves-fall.jpg">
        <img id="ufoTexture" src="textures/ufo.jpg">
    </a-assets>
    <a-light type= "ambient" color= "#0000ff"></a-light>
    <a-light type= "point" position= "0 0 0" intensity= "1" ></a-light>
    <a-sky src= "#galaxyTexture"></a-sky>
    <a-plane src= "#grassTexture" rotation= "-90 0 0" width= "100" height= "100" repeat="10 10"></a-plane>
    <a-cylinder src= "#logTexture" width= "3" height= "10" position= "0 2 -8"></a-cylinder>
    <a-sphere src= "#autumnleavesTexture" scale= "3 3 3" position= "0 7 -8"></a-sphere>
    <a-sphere src= "#ufoTexture" position="-400 200 -300" scale="25 2 25" animation="property: object3D.position.x; to: 400; dir: alternate; dur: 5000; loop: true;"></a-sphere>
    <a-entity text="value: LOOK, THERE'S A UFO IN THE SKY!!!; color: #FFFFFF; width: 5; align: center" position="0 2 -5" scale="1.5 1.5 1.5"></a-entity>
<a-scene>
```

**Output:**

https://github.com/user-attachments/assets/1f5b045f-8fb3-43e6-a37e-f1c51b8f2290




[Previous](entry04.md) | [Next](entry06.md)

[Home](../README.md)
