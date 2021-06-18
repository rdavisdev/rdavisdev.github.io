<h1 style="text-align: center;">Hello and Welcome!</h1>
<hr>

<div class="aspect-ratio" style="width:100%;">  
    <div style="position: absolute; width: 100%; height: 100%;">

        {% include slideshow.html 
        class="HomeSlides" index="0"
        img1="IslesOfLimbo/IslesOfLimbo_Gameplay2.PNG" caption1="test caption"
        img2="Behemyth/Neon11.PNG" caption2="test caption"
        img3="Liftoff/Liftoff3.JPG" caption3="test caption"
        img4="CloudSim/CloudSim2.PNG" caption4="test caption"
        %}

    </div>
</div>

My name is Ryan, a senior programmer at the DigiPen Institute of Technology. I'm studying real-time interactive simulation and loving every bit of it. Past titles I've worked on while here are [Chromatic Split](https://rdavisdev.github.io/games#ChromaticSplit), [Isles of Limbo](https://rdavisdev.github.io/games#IslesOfLimbo), and [Project Neon](https://rdavisdev.github.io/games#ProjectNeon). In addition, I often work on independent projects which can be seen [here](https://rdavisdev.github.io/projects). **NOTE: This site is currently under developement, some projects and code samples will not be available.**

My experiences and interests are in the following areas: 

- Graphics 
- Gameplay Programming
- Engine Development

I'm looking to start working professionally in one of these fields. Hopefully on something where I'll be able to learn and help produce some great results! Above you can find links for my [resume](https://rdavisdev.github.io/info), info about past and in-progress [games](https://rdavisdev.github.io/games), as well as personal programming [projects](https://rdavisdev.github.io/projects) I've tackled. Feel free to [contact](https://rdavisdev.github.io/info) me if you'd like to chat about my work or future opportunities.

I hope you enjoy your visit!







<div id="Modal" class="modal">
    <img id="Modal_img" class="modal-content">
    <div id="modal_caption" class="modal-caption"></div>
</div>

<script>

var images = document.getElementsByClassName("slideshow-image");
for(var i = 0; i < images.length; i++)
{  
    images[i].onclick = function(){
        document.getElementById("Modal").style.display = "block";
        document.getElementById("Modal_img").src = this.src;
        document.getElementById("Modal_caption").innerHTML = this.alt;
    }
}

document.getElementById("Modal").onclick = function(){
    document.getElementById("Modal").style.display = "none";
}

</script>

<script>
var slideIndex = [4];
var slideId = ["HomeSlides"]
var advanceLock = [false];
showSlides(1, 0);

advanceSlides();
function advanceSlides()
{
    for(var i = 0; i < slideId.length; i++)
    {
        if(!advanceLock[i])
            plusSlides(1, i);
        advanceLock[i] = false;
    }
    setTimeout(advanceSlides, 6000);
}

function plusSlides(n, no) {
    showSlides(slideIndex[no] += n, no);
    advanceLock[no] = true;
}

function showSlides(n, no) {
    var i;
    var x = document.getElementsByClassName(slideId[no]);
    if (n > x.length) {slideIndex[no] = 1}    
    if (n < 1) {slideIndex[no] = x.length}
    for (i = 0; i < x.length; i++) {
        x[i].style.display = "none";  
    }
    x[slideIndex[no]-1].style.display = "block";  
}
</script>