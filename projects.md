---
title:"Projects"
layout:page
permalink:"/projects/"
---
<style>
    #card{
        border:2px;
        border-radius:5px;
        border-color: black;
        border-spacing:10px;
        background-color:aliceblue;
        float: left;
        padding:10px;
        text-decoration: none;
        font-family: sans-serif;
        width:33.3%;
    }
    #cssbutton{
        background-color: black; /* Green */
        border: none;
        color: whitesmoke;
        padding: 5px 10px;
        text-align: center;
        text-decoration: none;
        display: inline-block;
        font-size: 16px;
        border-radius: 2px;
    }
</style>
<div id=cards></div>
<script>
    function gencard(name,description,link,image){
        if(image!=''){
            document.getElementById("cards").innerHTML+=`
            <div id=card>
            <img src=${image} width=100% style="border-radius:2px">
            <h1>${name}</h1>
            <p>${description}</p>
            <button id="cssbutton" onClick="location.href='${link}'">View</button>
            </div>
            `;
        }
        else{
            document.getElementById("cards").innerHTML+=`
            <div id=card>
            <h1>${name}</h1>
            <p>${description}</p>
            <button id="cssbutton" onClick="location.href='${link}'">View</button>
            </div>
            `;
        }

    }
gencard('ReMapper','Interactive Map Generation for Trip Recording','','');
gencard('Kalictric','Digitally-enabled Kalimba','','');
gencard('Cricket Pi','Little "Cute" MIDI Player','','');
gencard('Conductor','Conduct a virtual orchestra with digital baton','','');
</script>
