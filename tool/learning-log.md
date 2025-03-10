# Tool Learning Log

## Tool: **A-Frame**

### 3/4/25:
* I learned how to change the location/ environment in A-Frame and it was pretty easy. Lets go over the process!
  * I went onto [Bootstrap](https://aframe.io/docs/1.7.0/guides/building-a-basic-scene.html#:~:text=The%20environment%20component%20procedurally%20generates%20a%20variety%20of%20entire%20environments%20for%20us%20with%20a%20single%20line%20of%20HTML.) Environment section (**highlight linked**). I clicked on the *linked* [environment component](https://github.com/supermedium/aframe-environment-component/) (**linked**) and it took me to a short tutorial on how to change my environment.
  ``` html
    <!--Copy and paste into your <head></head> // Note: need latest version of A-Frame-->
    <script src="https://unpkg.com/aframe-environment-component@1.5.x/dist/aframe-environment-component.min.js"></script>
    <!-- Then create a ... -->
    <a-scene>

    </a-scene>
    <!-- Lastly, type in this into the <a-scene></a-scene> -->
    <a-entity environment></a-entity>
  ```
  **Output:**

  ![alt text](image-holder/baseplate.png)

  * The baseplate seems too plain? Here's something to change the landscape!

  ``` html
    <!-- use presets to change your landscape! -->
    <a-scene>
      <a-entity environment= "preset: forest;"></a-entity>
    </a-scene>
  ```
  **Output:**
  ![alt text](image-holder/forest.png)

### X/X/XX:
* Text


<!--
* Links you used today (websites, videos, etc)
* Things you tried, progress you made, etc
* Challenges, a-ha moments, etc
* Questions you still have
* What you're going to try next
-->
