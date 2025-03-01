# Entry 4: Choosing my CS Tool (Personal Finance)
##### 02/24/25

## The ULTIMATE Tool I chose and why...

I had many choices about what tools to choose **[based on the tools](https://docs.google.com/document/d/1zk4vM_UA_RsFvwL_suia-W7FNIXsDTqOurXGuCnnhsg/preview?tab=t.0)** Mr. Mueller gave us. I was hesitant and a little bit confused about my path/ what to choose at first because everything seemed so mysterious and new to me. For that, I had to tinker around with the tools to find my top 3 **AND THEN** narrow it down to my final choice. I found 3 tools I was interested in based on their description: jQuery, Aframe, and CSS grid.

First, I tinkered with jQuery first which was a tough yet fun experience and a little foreshadowing is that I didn't choose this as my final tool. For example, I learned how to hide text by clicking a button or alerting the user if they clicked a certain element on the webpage. **Learned from [w3schools](https://www.w3schools.com/jquERy/default.asp)**

**CODE:**

``` js
        <script>
            //click h2 text to reveal message/ alert user

            $(document).ready(function(){
                $("h2").mousedown(function(){
                    alert("YOU'VE ENTERED THE SCARY DUNGEON");
                });

            //click button to hide p tag

                $("button").click(function(){
                    $(".hide").hide();
                });
            });
        </script>
```
**RESULT:**

<video controls src="Screen recording 2025-02-28 10.30.05 AM.mp4" title="Title"></video>

---

Secondly, I tinkered with AFrame and it was AWESOME + surprisingly easy/ flexible for me. Why? It was 3D and it looked visually cool to my eyes so I might've chosen this over jQuery. I made different colored boxes around me with different rotations and positions. **[Learned from A-Frame Introduction](https://aframe.io/docs/1.5.0/introduction/)**

**CODE:**

``` html
        <a-scene>
            <!--rotated blue cube under user-->
            <a-box color="blue" rotation="0 30 0" scale="1 1 1" position="0 0 0"></a-box>
            <!--rotated yellow cube above user-->
            <a-box color="yellow" rotation="0 30 30" scale="1.1 1.5 1" position="0 3 0"></a-box>
            <!--rotated red cube in front of user-->
            <a-box color="red" rotation="20 0 40" scale="1.3 1 1.2" position="0 1.5 -5"></a-box>
            <!--rotated violet cube to the right of user-->
            <a-box color="violet" rotation="0 10 50" scale="2 1 1.4" position="5 1.5 0"></a-box>
            <!--rotated green cube behind user-->
            <a-box color="green" rotation="0 70 -25" scale="1.8 1.7 1" position="0 1.5 5"></a-box>
            <!--rotated brown cube to the left of user-->
            <a-box color="brown" rotation="-10 0 50" scale="2 2 2" position="-5 1.5 0"></a-box>
        </a-scene>
```
**RESULT:**

https://github.com/user-attachments/assets/7856902b-165d-46e5-a6e1-2a260e9b70d9

---
Lastly, I tried out CSS Grid, the one I found most helpful yet it was boring to be honest however still tinkered with. I created a table with 5 columns and 2 rows, each with its own ranking to the "How was your day?" (Spacing and color included). Learned from **[w3schools](https://www.w3schools.com/css/css_grid.asp)**

**CODE:**

``` html
<html>
    <head>
        ...
        <style>
            /* CSS */
            .center {
                text-align: center;
            }
            .container {
                display: grid;
                grid-template-columns: auto auto auto auto auto;
                background-color: lightblue;
                padding: 10px;
                gap: 10px;
            }

            .container > div {
                background-color: white;
                padding: 10px;
                text-align: center;
            }
        </style>
    </head>
    <body>
        <!-- HTML -->
        <h1 class="center"> How was your day?</h1>

         <div class="container">
            <div>1/10 WORST THAN WORSE</div>
            <div>2/10 REALLY BAD</div>
            <div>3/10 BAD</div>
            <div>4/10 I guess it was bad</div>
            <div>5/10 Neutral</div>
            <div>6/10 It was fine</div>
            <div>7/10 It was okay</div>
            <div>8/10 GOOD</div>
            <div>9/10 BEST DAY EVER</div>
            <div>10/10 I WANT TO EXPERIENCE IT AGAIN</div>
         </div>
    </body>
</html>
```
**RESULT:**

![alt text](<Screenshot 2025-02-28 10.22.18 AM.png>)
---

## Engineering Design Process (EDP)

In the EDP steps, I am at **step 3.5** (**in the middle of 3 and 4**) and this is because I am not planning the MOST promising solution (**Step 4**) or brainstorming possible solutions as I've completed my brainstorm session.  Recently, I haven't been that much focused on finding a solution for teenage personal finance, rather I have been focused on **CS/SEP-related work**. However, I am closer to step 4 than step 3 which is **GOOD** and that means I will be able to find the best solution for personal financing, targeted at teenagers. For now, I will have to test out all these awesome tools and fully understand certain attachments of CS such as familiarizing myself with bootstrap so that I can create an even better webpage! *__STEP 4! I AM COMING!!!__*

## Skills

To be honest, I have greatly improved in **LEADERSHIP**, **PROBLEM DECOMPOSITION**, and **HOW TO LEARN**

### LEADERSHIP
I am **SO PROUD** of my huge improvements in leadership skills over the span of a month (beginning of the 2nd semester). Remember the CYOA project and how I am required to work with a partner? For some context, I wasn't so sure of completing this project with a partner (**Winnie C.**) because I am not a huge "teamwork" person sometimes. However, I **gave it a shot** and the result was that I was the leader, leading and giving advice such as telling them to create images for each result file to my partner, without the fear of embarrassing myself (common fear I had if I led a group/ worked in a team). Therefore, I learned from that day on, I am an amazing leader in team projects (**can be reflected of our final grade which was an 100%**)

### PROBLEM DECOMPOSITION

This is one of the skills I am most grateful for in the long term and why? Now I won't have to overanalyze a problem as a whole but instead, I can break it down into digestable pieces. What I mean is I can somewhat easily find the solution to a problem **(Struggling with SEP H.W or C.W)**. The secret is to **TRY IT OUT!!** *WOAH IT WAS THAT SIMPLE??? THANKS RAIN*. I was in the library, doing my SEP10 homework (**F 2/28: Bootstrap Grid Practice**) and I couldn't process out a plan to the problem (**creating a webpage, testing out Bootstrap**) so without wasting time, I tried to break everything down into pieces: *What is the easiest step that I can complete?* *What can I add on those changes?* *What else can be added?* and **FOLLOW THE SLIDE'S INSTRUCTIONS!!!**. I added my title and more info (`<h1>FACTORS OF 12</h1>` `<h2>VISUAL DEMO</h2>` `<p>INSTRUCTIONS:</p>`) and styled it the way I felt most appropriate (`text-align`, `color`, etc). Then I added `container-fluid, container, row(s), and col(s)` with the right indentations and breakpoints. *What else can I add?* I went to the **[Grid Example](https://bmuellerhstat.github.io/solo/bootstrap-grid-example.html)** by Mr. Mueller and took inspiration on the changing phrases each time the columns and rows changed (**EXTRA LARGE -> LARGE -> MEDIUM -> SMALL**) by inspect element (`#id:after` and `@media (max-width: 767px  or 1199px)`). At the end, I looked at my little webpage I've made with Bootstrap and other CSS/HTML knowledge and wow... IT LOOKED AMAZING! **Thus, breaking down the problem is a free guide to success!**

### HOW TO LEARN (*#loyo*)

*#loyo*= Learn on your own. Keep this in mind as I explain why this skill is a useful to me and will 100% benefit others. To learn on your own, is to search on google and learn on there. Right? Yep, no plot twist. Before the mid-winter break, we had to understand a little about our tools (**A-Frame, jQuery, SASS, etc**) before selecting one. I used the websites Mr. Mueller gave us to learn about those tools and tinker with the information given to us. For jQuery, I had a hard time understanding the guide website so I went to Google and searched up, jQuery tutorial and found **[Learn jQuery in 6 minutes](https://www.youtube.com/watch?v=JjIvF0yikGU)** by blondiebytes. After watching the video, I had an easier time re-reading the guide wesbite (**w3schools**). Essentially, *#loyo* was useful and I accidentally did it without me noticing (*I didn't really like searching up a tutorial because I already had to read guide website and it felt like too much work*). So **if you're ever stuck** and you don't know what to do, **learn it yourself** and **don't be stubborn** on reading the guide given by the teacher as it's their recommendation and that might not **fit your style**.

## Next Step

**For step 4,** I am going to finalize my final plan, the best one yet: I am going to create fun, strict, and education personal financing system (**with the manifestation of a hardware ever releasing to the public**). Note that the hardware is an idea for the future generations to see so that they can try to create one similar or the same one as mine (*to carry on my amazing legacy*). But on a serious note, I am planning to create a webpage, introducing this idea of the **DroidNosMoney** hardware and other personal financing related things (**educational, softwares, etc**).

[Previous](entry03.md) | [Next](entry05.md)

[Home](../README.md)
