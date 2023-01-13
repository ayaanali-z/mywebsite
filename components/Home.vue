<template>

<div>
<center>
<link rel="stylesheet" href="style.css" />
<div class = "container"> 
	<div class = "HEADER"> 
		<h1><span style="color: #e4bb68">System</span><span style="color:white;">.<span style="color:#e06c75;">out</span>.</span><span style="color:#61afef;">println</span><span style="color: #e4bb68">("</span><div id = "sequence"></div><span style="color: #e4bb68">");</span></h1>
</div>
</div>

<div class = "links"> 
	<h2 id = "aboutme"> <NuxtLink to= "about"> About Me </NuxtLink> </h2>
	<h2> <a href = "https://drive.google.com/file/d/1NKvvGXsVPl-6mN4HticsgsRLneTVQ-tS/view?usp=sharing"> Resume </a> </h2>
	<h2> <a href = "mailto: aa4688@columbia.edu">Email</a></h2>
</div> 

<div class = "container2"> 
	<h2> Daily Astronomy </h2>
         <img :src="apod.url" alt="Astronomy Photo"  id = "NASA" > 
		    <h3> {{ apod.title }}</h3>
			<p> {{ apod.copyright }}</p>
			<p> {{ apod.date }}</p>
		
</div> 

</center>
</div>  
</template> 
 
<style>
@import url('https://fonts.googleapis.com/css2?family=Anton&family=EB+Garamond&family=Fredoka+One&family=JetBrains+Mono:wght@500&display=swap'); 
.container { 
	display: inline-block; 
	text-align: center; 
}
.container2 { 
	font-size: 25px; 
	font-family: 'JetBrains Mono', monospace;
	color: white;
	margin: 50px; 
}
.HEADER h1 {
	font-size: 50px; 
	font-family: 'JetBrains Mono', monospace;
}

.string {
  text-align: center;
}
.greeting {
  position: relative;
  top: 8.6vmin;
}

.links { 
	color: white; 
    font-family: 'JetBrains Mono', monospace; 
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
#sequence { 
	display: inline; 
}
div { 
	background-color: black; 
 }
body { 
	background-color: black;
}

.color1 {
  color: #fa8231;
}

.color2 {
  color: white;
}

.color3 {
  color: green;
}

.color4 {
  color: yellow;
}
.color5 {
  color: orange;
}
.color6 {
  color: pink;
}
.color7 {
  color: purple;
}

</style>

<script>

var example = [{'word':'Hello World!', 'class':'color1'},    
					{'word':'Bonjour monde!', 'class':'color2'},     
					{'word':'Hallo Welt!', 'class':'color3'},    
					{'word':'Hola mundo!', 'class':'color4'},    
					{'word':'こんにちは世界!', 'class':'color5'},     
					{'word':'Привет мир!', 'class':'color6'},    
					{'word':'你好世界!', 'class':'color7'}];

textSequence(0);
function textSequence(i) {

	if (example.length > i) {
		setTimeout(function() {
			document.getElementById("sequence").innerHTML = example[i].word;
			document.getElementById("sequence").setAttribute("class", example[i].class);
			textSequence(++i);
		}, 1000); // 1 second (in milliseconds)

	} else if (example.length == i) { // Loop
		textSequence(0);
	}

}
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