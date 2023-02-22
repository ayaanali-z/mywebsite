<template> 
    <div id = "AboutMe"> 
  
        <h1> About me </h1> 

        <p id = "bio"> Some key points: 
            <ul>
                <li>I'm from <span style = "color: #8142f5">NYC</span>.</li>
                <li>I study computer science + mathematics @ <span style = "color: #2B4593">Columbia University</span>.</li>
                    <ul>
                        <li>My most proficient language is <span style = "color: chocolate">Java</span>.</li>
                    </ul>
                <li> On the internet, I often go by <mark>ayaandotcom</mark>.</li>
                <li> I like pulling data from random APIs on my sites. </li>
                <li> I'm a staff reporter in University News for Columbia Daily Spectator. </li>
                    <ul> 
                       <li>A full list of my coverage can be found <a href = "https://www.columbiaspectator.com/contributors/Ayaan-Ali/"> <b> here.</b></a></li> 
                    </ul>
                <li> I like doing the NYT Crossword and sudoku.</li>
            </ul>
                    Professional interests: 
                <ul> 
                    <li> Backend SWE, quantitative finance, AI/ML, and mathematical modeling.</li>
                    <li> My experience and technical skills can be found on my 
                        <a href = "https://drive.google.com/file/d/1BTnWIeztgcPq6ZX9_UeliO_2LvXBFY4z/view?usp=sharing">resume</a>.</li>
                    <li> I'm actively seeking new opportunities. Please feel free to reach out on <a href = 
                        "https://www.linkedin.com/in/ayaan-ali-089848208/">Linkedin</a>.</li>
                </ul>
        </p>

     </div> 
</template> 
<style> 
    @import url('https://fonts.googleapis.com/css2?family=Anton&family=EB+Garamond&family=Fredoka+One&family=JetBrains+Mono:wght@500&display=swap'); 

div { 
    background-color: black;
}
mark{
 background-color:#c2c2c2;
}
li {
  margin-bottom: 10px; 
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
    display: flex;
	flex-direction: column; 
  	justify-content: center;
  	align-items: center;
}
#bio { 
    font-size: 20px; 
    font-family: 'JetBrains Mono', monospace; 
    color: white; 
}
#tips { 
    text-align: center; 
}

  #homepic {
    text-align:center;
    margin: 0 auto; 
  }

a:hover, a:visited, a:link, a:active
{
    text-decoration: none;
    color: lightblue; 
}
</style> 