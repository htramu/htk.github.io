---
layout: post
title:  "HedgeShot"
---
<style>
* {box-sizing: border-box}
body {font-family: Verdana, sans-serif; margin:0}
.mySlides {display: none}
img {vertical-align: middle;}

/* Slideshow container */
.slideshow-container {
  max-width: 1000px;
  position: relative;
  margin: auto;
}

/* Next & previous buttons */
.prev, .next {
  cursor: pointer;
  position: absolute;
  top: 50%;
  width: auto;
  padding: 16px;
  margin-top: -22px;
  color: white;
  font-weight: bold;
  font-size: 18px;
  transition: 0.6s ease;
  border-radius: 0 3px 3px 0;
  user-select: none;
}

/* Position the "next button" to the right */
.next {
  right: 0;
  border-radius: 3px 0 0 3px;
}

/* On hover, add a black background color with a little bit see-through */
.prev:hover, .next:hover {
  background-color: rgba(0,0,0,0.8);
}

/* Caption text */
.text {
  color: #f2f2f2;
  font-size: 15px;
  padding: 8px 12px;
  position: absolute;
  bottom: 8px;
  width: 100%;
  text-align: center;
}

/* Number text (1/3 etc) */
.numbertext {
  color: #f2f2f2;
  font-size: 12px;
  padding: 8px 12px;
  position: absolute;
  top: 0;
}

/* The dots/bullets/indicators */
.dot {
  cursor: pointer;
  height: 15px;
  width: 15px;
  margin: 0 2px;
  background-color: #bbb;
  border-radius: 50%;
  display: inline-block;
  transition: background-color 0.6s ease;
}

.active, .dot:hover {
  background-color: #717171;
}

/* Fading animation */
.fade {
  animation-name: fade;
  animation-duration: 1.5s;
}

@keyframes fade {
  from {opacity: .4} 
  to {opacity: 1}
}

/* On smaller screens, decrease text size */
@media only screen and (max-width: 300px) {
  .prev, .next,.text {font-size: 11px}
}
</style>


 <!-- Slideshow container -->
<div class="slideshow-container">

  <!-- Full-width images with number and caption text -->
  <div class="mySlides fade">
    <div class="numbertext">1 / 6</div>
    <img src="/assets/hedgeShot_1.jpg" style="width:100%">
    <div class="text">Screenshots</div>
  </div>

  <div class="mySlides fade">
    <div class="numbertext">2 / 6</div>
    <img src="/assets/hedgeShot_2.jpg" style="width:100%">
    <div class="text">Screenshots</div>
  </div>

  <div class="mySlides fade">
    <div class="numbertext">3 / 6</div>
    <img src="/assets/hedgeShot_3.jpg" style="width:100%">
    <div class="text">Screenshots</div>
  </div>
  
    <div class="mySlides fade">
    <div class="numbertext">4 / 6</div>
    <img src="/assets/hedgeShot_4.jpg" style="width:100%">
    <div class="text">Screenshots</div>
  </div>
  
    <div class="mySlides fade">
    <div class="numbertext">5 / 6</div>
    <img src="/assets/hedgeShot_5.jpg" style="width:100%">
    <div class="text">Screenshots</div>
  </div>
  
      <div class="mySlides fade">
    <div class="numbertext">6 / 6</div>
    <img src="/assets/hedgeShot_6.jpg" style="width:100%">
    <div class="text">Screenshots</div>
  </div>

  <!-- Next and previous buttons -->
  <a class="prev" onclick="plusSlides(-1)">&#10094;</a>
  <a class="next" onclick="plusSlides(1)">&#10095;</a>
</div>
<br>

<!-- The dots/circles -->
<div style="text-align:center">
  <span class="dot" onclick="currentSlide(1)"></span>
  <span class="dot" onclick="currentSlide(2)"></span>
  <span class="dot" onclick="currentSlide(3)"></span>
  <span class="dot" onclick="currentSlide(4)"></span>
  <span class="dot" onclick="currentSlide(5)"></span>
  <span class="dot" onclick="currentSlide(6)"></span>
</div> 

<script>
let slideIndex = 1;
showSlides(slideIndex);

function plusSlides(n) {
  showSlides(slideIndex += n);
}

function currentSlide(n) {
  showSlides(slideIndex = n);
}

function showSlides(n) {
  let i;
  let slides = document.getElementsByClassName("mySlides");
  let dots = document.getElementsByClassName("dot");
  if (n > slides.length) {slideIndex = 1}    
  if (n < 1) {slideIndex = slides.length}
  for (i = 0; i < slides.length; i++) {
    slides[i].style.display = "none";  
  }
  for (i = 0; i < dots.length; i++) {
    dots[i].className = dots[i].className.replace(" active", "");
  }
  slides[slideIndex-1].style.display = "block";  
  dots[slideIndex-1].className += " active";
}
</script>


---


This is a submission for [GDFG TEAM JAM #4](https://itch.io/jam/gdfg-team-jam-4), developed using the Unreal 5 engine via Blueprints. The overall theme for the game jam was "Strange Power Ups" and the jam ran for a month. 

Our team consisted of four people, including me. We choose genre to be a First Person Shooter, in a hedge maze like environment where player shoots hordes of zombies, in "boomer shooter" style. A dark and nighttime setting is chosen, with a green color prevalent across the gameplay arena, to create a sickly and unnatural feeling to the player. We limited game to be a just a level in order to meet up with the restrictions (jam duration, resources etc.).

My primary responsibility was Game Design, but I also undertook the roles of the Director, Level Designer and Sound Designer, and done some small coding tasks.

What I've done in this jam can be listed as follows:

Designed the power-up system, level flow, main loop, weapon characteristics and the flow of the level. First draft of my design notes can be found here and the settled (together with the team) flow of the gameplay can be found below:

Made key decisions such as removal of the store idea, ingredient drops, loot drops and crafting (which all of them were in the first ideation process), curbed out over-the-scope ideas (like 2-3 more enemy types which would've overwhelmed our 3D artist) and made sure the all team members were on the same page. 

Designed the whole level layout. I have done the basic block-out, using in engine tools of Unreal Engine. I took inspiration from [The labyrinth of Versailles](https://en.wikipedia.org/wiki/The_labyrinth_of_Versailles) when I started to design the level, and iterate on the design process, instead of copying the real life place. Our 3D artist later filled the block-out and finished the level.

Set up a miro page in order to create the roadmap for our development, set duties for all team members, create a pool for ideation process. Set the MVP goals (can be seen below) of the team and the MVP deadline, which the team accomplished finishing the MVP one day before the deadline.


Created sound effects via AI tools, as all of us lacked the skills or experience to create sound effects using conventional tools. 

Programming tasks:
Created the sine movement sphere object in Unreal Engine using blueprints. Movement, destroy event
Created a rotating box shaped object in Unreal Engine using blueprints. Which later turned into the weapon pickup.
Created main menu layout.
Implemented sounds and synchronize them with various animations and events.




### Game Page on itch.io

<iframe frameborder="0" src="https://itch.io/embed/2878493?linkback=true&amp;border_width=0" width="206" height="165"><a href="https://winter-witch.itch.io/hedgeshot">HedgeShot by Winter Witch, Umarth, meowroz, dragonmushu3</a></iframe>