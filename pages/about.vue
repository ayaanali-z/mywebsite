<template> 
    <div id = "AboutMe"> 
    <center> 
        <h1> About me </h1> 
        <img src = "LinkedinPhoto.png" alt = "A picture of Ayaan" width = "250" height = "250" id="homepic"/>

        <p id = "bio"> Hi! I'm an aspiring developer from Queens, NYC currently studying computer science and mathematics @ Columbia University. Academically, I'm interested in mathematical finance, probability theory, AI/ML, and 
            backend engineering.
        </p> 

        <p id = "passion"> Outside of school, I'm deeply passionate about journalism. I'm a staff reporter in University News for Columbia Daily Spectator. A 
            full list of my coverage can be found <a href = "https://www.columbiaspectator.com/contributors/Ayaan-Ali/"> <b> here.</b></a> 
        </p>

        <p>Any tips can be sent to <a href = "mailto: ayaan.ali@columbiaspectator.com"> ayaan.ali@columbiaspectator.com</a></p>

        <p>
            Technical skills: <span style= "color: #994C00">Java</span>, <span style = "color: lightgreen">Python</span>, <span style = "color: lightcoral">HTML5/CSS/Javascript</span>, Nuxt.js, Vue.js, and LaTeX. 
        </p>

        <p> Please feel free to follow me on any platforms and message me for any inquiry. I'm most active on <a href = https://www.linkedin.com/in/ayaan-ali-089848208>Linkedin.</a></p>
        
    </center> 
     </div> 
</template> 
<style> 
    @import url('https://fonts.googleapis.com/css2?family=Anton&family=EB+Garamond&family=Fredoka+One&family=JetBrains+Mono:wght@500&display=swap'); 

div { 
    background-color: black;
}
#AboutMe { 
    background-color: black; 
    color: white; 
    font-family: 'JetBrains Mono', monospace; 
    padding-top: 25px;
    padding-right: 100px;
    padding-bottom: 100px;
    padding-left: 50px;
    margin-left: 50px; 
    margin-right: 50px; 
    color: white; 
}
#bio { 
    font-family: 'JetBrains Mono', monospace; 
    color: white; 
}

a:hover, a:visited, a:link, a:active
{
    text-decoration: none;
    color: lightblue; 
}
</style> 