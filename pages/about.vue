<template> 
    <div id = "AboutMe"> 
    <center> 
        <h1> About me </h1> 
        <img src = "LinkedinPhoto.png" alt = "A picture of Ayaan" width = "250" height = "250" id="homepic"/>

        <p id = "bio"> Hi! I'm an aspiring developer from Queens, NYC currently studying computer science and mathematics @ Columbia University. 
            I'm progressively proficient in Java, Python, HTML5/CSS/Javascript, specifically the Vue and Nuxt JS frameworks. I'm also 
            skilled in constructing LaTeX documentation. Academically, I'm interested in mathematical finance, probability theory, AI/ML, and 
            backend engineering.</p> 

        <p id = "passion"> Outside of school, I'm deeply passionate about journalism. I'm a staff reporter in University News for Columbia Daily Spectator. A 
            full list of my coverage can be found <a href = "https://www.columbiaspectator.com/contributors/Ayaan-Ali/"> <b> here.</b></a> Any tips can be sent to 
                <a href = "mailto: ayaan.ali@columbiaspectator.com">ayaan.ali@columbiaspectator.com</a>
        </p>

        <p> <span style = "color: lightgreen"> Spring 2023: </span> Data Structures & Algorithms (<span style = "color: #b5651d">Java</span>), Accelerated Multivariable Calculus (III-IV), Linear Algebra, Literature Humanities II, and University Writing: Contemporary Essays. </p>
        <p> <span style = "color: #C4A484"> Fall 2022: </span> Introduction to Computer Science and Programming (<span style = "color: #b5651d">Java</span>), Calculus II, Calculus-Based Introduction to Statistics, Literature Humanities I, and Frontiers of Science. </p>
        <p> <span style = "color: lightseagreen"> 2021-22:</span> AP Calculus AB, AP Computer Science Principles (<span style = "color: green">Python</span>).</p>

        <p> Please feel free to follow me on any platforms and message me for any inquiry. </p>
        
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
    padding-right: 80px;
    padding-bottom: 80px;
    padding-left: 50px;
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