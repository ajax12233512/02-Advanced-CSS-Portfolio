# 02-Advanced-CSS-Portfolio
Portfolio Website made in behalf of SMU

## 8/7/2021 6:00PM: Starting
I will be documenting my progress on this Homework Assignment from start to finish. It is imperative that I accurately depict every thought processes that I encure, so that myself and others can understand what I intend. I'm currently trying to learn how to write a markdown file. It will be very useful in the future so I can be capable of implementing easy-to-read markdown for my fellow developers. I will provide links to resources that I harnessed valuable information from, below. For now, I have initialized my project via gitBash and will start with the mark up. I was thinking of a smooth, easy-to-read, bubbly-ish, kind of website. I will iron out the details once I get to it. For now I want to think carefully about how I set up my `<div>` and `container` elements. Given that I intend on utilizing as much CSS as I can, I want to tactical in that aspect. I want to have 3 or 4 links or navbar items. Something like this
````HTML
    <ul>
        <li><a href="#">HOME</a></li>
        <li><a href="#">ABOUT ME</a></li>
        <li><a href="#">PROJECTS</a></li>
        <li><a href="#">CONTACT</a></li>
    </ul>
```` 
I also want to have a unique background. Simple colors, but pleasing to look at. Okay. 

### 6:20PM Quick Note
I will begin this project by taking a mobile-first approch. Doing so will help me start simple and build on from there. 

### 9:45PM Quick Note
Got the basic nav bar and header layout. Thinking of styling themes.


### GOOD RESOURCES
---
[MDN WEB DOCKS](https://developer.mozilla.org/en-US/ "MDN WEB DOCKS")

[UI GRADIENTS.COM](https://uigradients.com "UI GRADENTS.COM")


## 8/8/21 24 HOURS IN
Okay so I got a fair bit into the portfolio. Since this morning I assisted a fellow student better understand our HW assignment. He seems to be a cool dude. I also refactored the CSS code so that I can simplify some things and save some time. So the first thing I want to explain is this class="container" because it is very important to this layout.  

````HTML
 <div class="container">
````

````CSS
.container{
    box-sizing: border-box;
    text-align: center;
    padding: 5%;/*Could be used for all subsquent containers*/
    margin: 5%;
    border: 2px solid black;
}
````

This class will be used frequently throughout the html. Here I set the standard 'look' of every bit of infomation and text. I added a border and I also styled subsquent typographic parts. Upon further analysation, I could probably save lines of code by combining them some clever way. I'll save a copy of it here tho.

````CSS
.container figure{
    background-color: rgba(37, 37, 37, 0.3);
    box-sizing: border-box;
    padding: 1%;
    margin: 10%;
    border-radius: .3em;
}

.container h3{
    font-size: 1.75em;
    text-transform: uppercase;
}

.container h2{
    /* padding-bottom: 0.9em; */
    font-size: 2.5em;
}

.container p{
    font-size: 1.3em;
}

.container blockquote{
    padding-bottom: 1em;
}

.container figcaption{
    font-size: 1.2;
    padding-bottom: 1em;
}

.container blockquote p{
    font-size: 1.2em;
}
````

Another thing I was thinking of changing was the way I set up these divs and container within my projects section

````HTML
<section id="projects">
        <h2 id="sectiontag">My Projects</h2>
        <div class="projects-container"><!--This is a container class(Used for layout purposes and sizing into larger screen sizes), not meant to be confused with the .container rule in my CSS file; hence the dash(-)-->
            <div class="container">
                <div class="project-display-tip-calculator">
                    <h3>Tip Calculator</h2>
                </div>
            </div>
            <div class="container">
                <div class="project-display-javascript-calculator" >
                    <h3>Javascript Calculator</h3>
                </div>
            </div>
            <div class="container">
                <div class="project-display-portfolio">
                    <h3>Portfolio Draft</h3>
                </div>
            </div>

        </div>
    </section>
````

I'm not sure why I it up this way. It seems to me that I could probably put the class="project-display-portfolio" into the div with the class="container". Doing so would look like this:
````HTML
<section id="projects">
        <h2 id="sectiontag">My Projects</h2>
        <div class="projects-container"><!--This is a container class(Used for layout purposes and sizing into larger screen sizes), not meant to be confused with the .container rule in my CSS file; hence the dash(-)-->
            <div class="container project-display-tip-calculator">               
                <h3>Tip Calculator</h2>                
            </div>
            <div class="container display-javascript-calculator">               
                <h3>Javascript Calculator</h3>               
            </div>
            <div class="container project-display-portfolio">                
                <h3>Portfolio Draft</h3>               
            </div>

        </div>
    </section>
````

One thing I'm proud of since starting is my background gradient affect on my projects section

````CSS
.project-display-tip-calculator{
    background: linear-gradient(to right, rgb(29, 43, 100, .5), rgb(248, 205, 218, .5)), url(img/tipcalculator.jpg);
    box-sizing: border-box;
    padding-top: 20%;/*Had to add this to bring <h2>s down to the middle of the image*/
    color: white;
    /* background-image: url(img/tipcalculator.jpg); */
    background-size: 400px;
    background-repeat: no-repeat;
    background-position-x: center;
    background-position-y: center;
    width: 100%;
    height: 280px;
}

.project-display-javascript-calculator{
    background: linear-gradient(to right, rgb(29, 43, 100, .5), rgb(248, 205, 218, .5)), url(img/calculatorjs.JPG);
    box-sizing: border-box;
    padding-top: 20%;/*Had to add this to bring <h2>s down to the middle of the image*/
    color: white;
    /* background-image: url(img/tipcalculator.jpg); */
    background-size: 400px;
    background-repeat: no-repeat;
    background-position-x: center;
    background-position-y: center;
    width: 100%;
    height: 280px;
}

.project-display-portfolio{
    background: linear-gradient(to right, rgb(29, 43, 100, .5), rgb(248, 205, 218, .5)), url(img/otherportfolio.JPG);
    box-sizing: border-box;
    padding-top: 20%;/*Had to add this to bring <h2>s down to the middle of the image*/
    color: white;
    /* background-image: url(img/tipcalculator.jpg); */
    background-size: 400px;
    background-repeat: no-repeat;
    background-position-x: center;
    background-position-y: center;
    width: 100%;
    height: 280px;
}
````

It turned out really great and I'm happy with it. I'm really eager to add an animmation here where it zooms in on the background image slowly when you hover over it. I'll think about it. For now I need to finish up the contact section. 