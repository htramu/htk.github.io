---
layout: post
title:  "Whispers in the Wild"
summary: "Game Designer /Director"
date:   2024-03-21 00:00:00
preview: /assets/wiw.png
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
    <div class="numbertext">1 / 5</div>
    <img src="/assets/wiw_1.jpg" style="width:100%">
    <div class="text">Screenshots</div>
  </div>

  <div class="mySlides fade">
    <div class="numbertext">2 / 5</div>
    <img src="/assets/wiw_2.jpg" style="width:100%">
    <div class="text">Screenshots</div>
  </div>

  <div class="mySlides fade">
    <div class="numbertext">3 / 5</div>
    <img src="/assets/wiw_3.jpg" style="width:100%">
    <div class="text">Screenshots</div>
  </div>
  
    <div class="mySlides fade">
    <div class="numbertext">4 / 5</div>
    <img src="/assets/wiw_4.jpg" style="width:100%">
    <div class="text">Screenshots</div>
  </div>
  
    <div class="mySlides fade">
    <div class="numbertext">5 / 5</div>
    <img src="/assets/wiw_5.jpg" style="width:100%">
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
<!-- ![Picture 1](/assets/wiw_1.jpg)
![Picture 2](/assets/wiw_2.jpg)
![Picture 3](/assets/wiw_3.jpg)
![Picture 4](/assets/wiw_4.jpg) -->


This is a submission for [Easter Jam 2024](https://itch.io/jam/easter-jam-2024), developed using the Unity (2022.3.22f1) engine. The overall theme for the game jam was "hunting" and the jam ran for a week. The game aimed to be a 3rd person 3D auditory hunting game, where the player follows audio cues of animals and catches them with a rhythm mini-game.

Our team consisted of ten people, including me.

My primary responsibility was Game Design along with the role of the Director.

The tasks I undertook can be can be grouped as follows:

<table style="border-collapse: collapse;">
	<tr>
		<td style="vertical-align:top;">
			<h4 style="text-align: center;">Game Designer</h4>
				<ul>
				  <li>
					Designed the Core Gameplay Loop
					<ul>
					  <li>Designed a game "day" where actual gameplay occurs</li>
					  <li>Designed the playthrough of 5 "days"</li>
					  <li>Designed a simple score system on game over</li>
					</ul>
				  </li>
				  <li>
					Designed Player Mechanics
					<ul>
					  <li>Movement (WASD-Mouse)</li>
					  <li>Camera positioning</li>
					  <li>Dash mechanic</li>
					  <li>Stealth mechanic</li>
					</ul>
				  </li>
				  <li>
					Designed World Map Mechanics
					<ul>
					  <li>Designed audio clue mechanic</li>
					</ul>
				  </li>
				  <li>
					Designed Animal Mechanics
					<ul>
					  <li>Designed number of the animal types and animal variables</li>
					  <li>Designed a mechanic called "behavior groups" to add variety</li>
					  <li>Designed Animal positioning and patrol behavior</li>
					</ul>
				  </li>
				  <li>
					Designed Gameplay Mechanics
					<ul>
					  <li>Designed animal "hunting" mechanic</li>
					  <li>Designed photography mode mechanics</li>
					  <li>Designed mini-games and mini game UIs</li>
					</ul>
				  </li>
				</ul>		
		</td>
		<td style="vertical-align:top">
				<h4 style="text-align: center;">Director</h4>
				 <ul>
				  <li>Come up with the main game idea and mechanics to set the vision of the game</li>
				  <li>Mediated the ideation process</li>
				  <li>Finalized decisions about:
				<ul>
				  <li>Camera (3rd person)</li>
				  <li>Graphic style (3D)</li>
				  <li>Mini-games, etc.</li>
				</ul>
				  </li>
				  <li>Managed a team of ten people in a 7 days deadline</li>
				  <li>Set up the development teams</li>
				  <li>Created a development roadmap</li>
				  <li>Managed administrative tasks:
					<ul>
					  <li>Setting up a Github repository</li>
					  <li>Creating an itch.io page</li>
					  <li>Handling team member invites, etc.</li>
					</ul>
				  </li>
				</ul>
		</td>
	</tr>
</table>

[Mechanics Design Document](/assets/winwMechanics.pdf)


### Game Page on itch.io

<iframe frameborder="0" src="https://itch.io/embed/2583046" width="552" height="167"><a href="https://htramu.itch.io/whispersinthewild">Whispers in the Wild</a></iframe>