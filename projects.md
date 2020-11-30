
<h1 style="text-align: center;">Projects</h1>
<hr>

# Volumetric Clouds (HSLS)

<br>

<div class="aspect-ratio" style="float: right; width:50%; margin: 15px 15px 15px;">  
    <div style="position: absolute; width: 100%; height: 100%;">

        {% include slideshow.html 
        class="CloudSimSlides" index="0"
        img1="CloudSim/CloudSim1.PNG" caption1="test caption"
        img2="CloudSim/CloudSim2.PNG" caption2="test caption"
        img3="CloudSim/CloudSim3.PNG" caption3="test caption"
        img4="CloudSim/CloudSim4.PNG" caption4="test caption"
        %}

    </div>
</div>

Over the Summer of 2020, I had a short period of free time during which I began this project. Following my passion for natural enironment rendering, I set out to create a real-time volumetric cloud-scape. Taking inspiration from the [cloud showcase](https://youtu.be/5tHzP00qZMQ?t=69) of a game called HawkVR, I've been learning from creator through his [development blog](https://blog.uhawkvr.com/). Credit to Felix Westin. Thank you!

Using a method of bipolar ray marching, Felix was able to create a performative, photorealistic, and volumetric cloud-scape. While my implementation still has a ways to go, I'm excited to continue work on this as time allows. Coincidentally, the [game](https://rdavisdev.github.io/games) I'm working on for school this year ended up having an aerial setting, giving me a practical oportunity to implement what I've learned from this. Stay tuned for updates!

<div style ="clear:both; display: block;">
</div>








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
var slideIndex = [4,4,4];
var slideId = ["CloudSimSlides", "IslesOfLimboSlides", "ChromaticSplitSlides"]
var advanceLock = [false, false, false];
showSlides(1, 0);
showSlides(1, 1);
showSlides(1, 2);

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
    