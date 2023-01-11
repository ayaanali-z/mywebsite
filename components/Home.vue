<template> 
<div>
<center>
<div class = "container"> 
	<div class = "typewriter"> 
		<h1>Hi! my name is Ayaan. </h1>
	</div> 
</div>

	<div class = "links"> 
	<h2> <NuxtLink to= "about"> About Me </NuxtLink> </h2>
	<h2> <a href = "https://drive.google.com/file/d/1NKvvGXsVPl-6mN4HticsgsRLneTVQ-tS/view?usp=sharing"> Resume </a> </h2>
	</div> 

</center>
</div>  
</template> 
 
<style>
@import url('https://fonts.googleapis.com/css2?family=EB+Garamond&display=swap'); 

.container { 
	display: inline-block; 
}
.typewriter h1 {
	font-size: 100px; 
	font-family: 'EB Garamond', serif; 
	color: white;
  	overflow: hidden; /* Ensures the content is not revealed until the animation */
  	border-right: .15em solid white; /* The typwriter cursor */
  	white-space: nowrap; /* Keeps the content on a single line */
  	margin: 150px auto;
  	letter-spacing: .10em; /* Adjust as needed */
  	animation: 
    typing 3.0s steps(40, end),
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

div { 
	background-color: black; 
 }
body { 
	background-color: black;
}
</style>