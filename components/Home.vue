<template> 
<div>
<center>
<link rel="stylesheet" href="style.css" />
<div class = "container"> 
	<div class = "typewriter"> 
		<h1> Hi! my name is Ayaan. </h1>
	</div> 
</div>

<div class = "links"> 
	<h2> <NuxtLink to= "about"> About Me </NuxtLink> </h2>
	<h2> <a href = "https://drive.google.com/file/d/1NKvvGXsVPl-6mN4HticsgsRLneTVQ-tS/view?usp=sharing"> Resume </a> </h2>
	<h2> <a href = "mailto: aa4688@columbia.edu">Email</a></h2>
</div> 

<div class = "container2"> 
	<h2> <a href = "https://apod.nasa.gov/apod/astropix.html"> Daily Astronomy </a> </h2>
         <img :src="apod.url" alt="Astronomy Photo"  id = "NASA" > 
		    <h3> {{ apod.title }}</h3>
			<p> {{ apod.explanation }}</p>
		
</div> 
<router-view v-slot="{ index }">
  <transition name="fade">
    <component :is="about" />
  </transition>
</router-view>

</center>
</div>  
</template> 
 
<style>
@import url('https://fonts.googleapis.com/css2?family=Anton&family=EB+Garamond&family=Fredoka+One&display=swap');
.container { 
	display: inline-block; 
	text-align: center; 
}
.container2 { 
	font-size: 25px; 
	font-family: 'EB Garamond';
	color: white;
	margin: 50px; 
}
.typewriter h1 {
	font-size: 100px; 
	font-family: 'EB Garamond', cursive;
	color: white;
	position: relative; 
  	overflow: hidden; /* Ensures the content is not revealed until the animation */
  	border-right: .15em solid white; /* The typwriter cursor */
  	white-space: nowrap; /* Keeps the content on a single line */
  	margin: 50px auto;
  	letter-spacing: .10em; /* Adjust as needed */
  	animation: 
    typing 4.15s steps(40, end),
	blink-caret .75s step-end infinite;
}

@keyframes typing {
  from { width: 0 }
  to { width: 100% }
}
@keyframes blink-caret {
  from, to { border-color: transparent }
  50% { border-color: white; }
}
.links { 
	color: white; 
    font-family: 'EB Garamond', serif; 
    font-size: 25px;  
}
a:hover, a:visited, a:link, a:active
{
    text-decoration: none;
    color: white; 
}

#NASA { 
	width: 500px; 
	height: auto; 
}
div { 
	background-color: black; 
 }
body { 
	background-color: black;
}
 
</style>

<script>
    export default {
    data() {
      return {
        apod: []
      }
    },
    async fetch() {
      this.apod = await fetch(
        'https://api.nasa.gov/planetary/apod?api_key=w0vDPcwgC3slJiZ9wAHQyJ6oD0ZAf6AXg24FqrTe'
      ).then(res => res.json())
    }
  }
</script>