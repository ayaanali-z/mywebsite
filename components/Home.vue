<template>
<div>
<center>
<link rel="stylesheet" href="style.css">

<div class = "container"> 
	<div class = "HEADER"> 
		<h1>
			<span style="color: #e4bb68">System</span><span style="color:white;">.<span style="color:#e06c75;">out</span>.</span><span style="color:#61afef;">println</span><span style="color: #e4bb68">("</span><div style="display: inline-block" v-bind:class="currentClass" v-bind:style="{color: currentColor}" display: inline>{{currentWord}} </div><span style="color: #e4bb68">");</span>
		</h1>
</div>
	<h1 id = "me"> My name is Ayaan. </h1>

</div>

<div class = "links" style = "color: white"> 
	<h2 id = "aboutme"> <NuxtLink to= "about"> About Me </NuxtLink> </h2>
	<h2> <a href = "https://drive.google.com/file/d/1NKvvGXsVPl-6mN4HticsgsRLneTVQ-tS/view?usp=sharing"> Resume </a> </h2>
	<h2> <a href = "mailto: aa4688@columbia.edu">Email</a></h2>
	
</div> 

	<div class = "socials"> 

	</div>

<div class = "container2"> 
	<h2> <span>Astronomy Picture of the Day</span></h2>

         <img :src="apod.url" alt="Astronomy Photo"  id = "NASA" >
		    <h3> {{ apod.title }}</h3>
			<p> {{ apod.date }}</p>
			<p> {{ apod.copyright }}</p>
		
</div> 
	<div class = "credits">
		<p> Built in Nuxt.js by Ayaan Ali</p>

	</div>
</center>
</div>  
</template> 
 
<style>
@import url('https://fonts.googleapis.com/css2?family=Anton&family=EB+Garamond&family=Fredoka+One&family=JetBrains+Mono:wght@500&display=swap'); 


.container { 
	color: white; 
	font-family: 'JetBrains Mono', monospace; 
}
.container2 {  
	font-size: 25px; 
	font-family: 'JetBrains Mono', monospace;
	color: white;
	margin: 50px; 
	display: flex;
	flex-direction: column; 
  	justify-content: center;
  	align-items: center;
}
.HEADER h1 {
	font-size: 50px; 
	font-family: 'JetBrains Mono', monospace;
	word-wrap: break-word; 
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
	margin-left: auto; 
	margin-right: auto; 

}


#sequence { 
	display: inline; 
}
#me { 
	font-size: 40px; 
	font-family: 'JetBrains Mono', monospace;
	color: white;
	margin: 50px; 
}
.credits { 
	font-size: 20px; 
	font-family: 'JetBrains Mono', monospace; 
	color: white; 
}

div { 
	background-color: black; 
 }
body { 
	background-color: black;
	margin-bottom: 100px; 
	animation: fadeInAnimation ease 3s;
    animation-iteration-count: 1;
    animation-fill-mode: forwards;
}
@keyframes fadeInAnimation {
            0% {
                opacity: 0;
            }
            100% {
                opacity: 1;
            }
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

.slide-enter-active, .slide-leave-active {
  transition: all .5s;
}
.slide-enter, .slide-leave-to {
  transform: translateX(-100%);
}
</style>

<script>

export default {
  data() {
    return {
      example: [
        { word: "Hello World!", class: "color1" },
        { word: "Bonjour monde!", class: "color2" },
        { word: "Hallo Welt!", class: "color3" },
        { word: "Hola mundo!", class: "color4" },
        { word: "こんにちは世界!", class: "color5" },
        { word: "Привет мир!", class: "color6" },
        { word: "你好世界!", class: "color7" },
      ],
      currentIndex: 0,
      apod: []
    };
  },
  computed: {
    currentWord() {
      return this.example[this.currentIndex].word;
    },
    currentClass() {
      return this.example[this.currentIndex].class;
    },
	currentColor() {
      return this.example[this.currentIndex].color;
    }
  },
  mounted() {
    this.textSequence();
    this.fetchAPOD();
  },
  methods: {
    textSequence() {
      setTimeout(() => {
        this.currentIndex++;

        if (this.currentIndex === this.example.length) {
          this.currentIndex = 0;
        }

        this.textSequence();
      }, 1000);
    },
    async fetchAPOD() {
      this.apod = await fetch(
        'https://api.nasa.gov/planetary/apod?api_key=w0vDPcwgC3slJiZ9wAHQyJ6oD0ZAf6AXg24FqrTe'
      ).then(res => res.json())
    }
  },
};

</script>

