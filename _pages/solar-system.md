---
title: "Solar System simulator"
layout: single
permalink: /solar-system/
author_profile: true
toc: true
header:
  video:
    id: 3WnC4eRY0bg
    provider: youtube
markdown: extra
---
{% comment %} 
header:
  overlay_image: /assets/images/JamesWebbDeepField.png
  overlay_filter: rgba(0, 0, 100, 0.1)
  image_description: "James Webb Telescope deep field."
{% include video id="1vbS_uvebSwWS90nSidgK0yrv_36H_FXq" provider="google-drive" %}  
(You can increase the video quality)  
{: .text-center .style="font-size= 5px;"}
{% endcomment %}

<a href="https://github.com/VascoCorreia/Solar-System-Simulator-No-Application" target="_blank"> <i class="fab fa-brands fa-github fa-2x"></i></a>
{: .text-right}
<hr>
### <i class="fa fa-solid fa-sun" style="color: #ae0c4e;"></i> Overview

My Solar system gravity simulator. All celestial bodies in the simulation move according to Newtons gravitation law that states:  

*Newton's law of universal gravitation is usually stated as that every particle attracts every other particle in the universe with a force that is proportional to the product of their masses and inversely proportional to the square of the distance between their centers.*   
{: .notice--primary}  
This said, every celestial bodies is influenced and influences all other celestial bodies depending on the gravitational constant, their masses and the distance to each other.  
The simulation starts using a normal time scale but can be sped up to a maximum value of 1 year per second.  

It includes our beautifull star and all the planets in the solar system!  

Everything is scaled except the planet diameters.  

<hr>
### <i class="fa fa-solid fa-gamepad" style="color: #ae0c4e;"></i> Controls  

<ul class="accordion">
    <li>
        <input type="checkbox" name="accordion" id="first">
        <label for="first">Expand</label>
        <div class="content">
            <table>
              <thead>
                <tr>
                    <th style="text-align: center">Action</th>
                    <th style="text-align: center">Key</th>
                </tr>
              </thead>
              <tbody>
                  <tr>
                    <td style="text-align: center">WASD</td>
                    <td style="text-align: center">Fast camera movement</td>
                  </tr>
                  <tr>
                    <td style="text-align: center">Precise movement</td>
                    <td style="text-align: center">Mouse2 + scroll wheel</td>
                  </tr>
                  <tr>
                    <td style="text-align: center">Camera Rotation</td>
                    <td style="text-align: center">Mouse2 + mouse movement</td>
                  </tr>
               </tbody>
            </table>
        </div>
    </li>
</ul>
### <i class="fa fa-solid fa-download" style="color: #ae0c4e;"></i> Download Builds  

| Build | Download |
| :--------: | :--------: |
| Windows | [Download](https://drive.google.com/uc?export=download&id=1qS1jXzYUGeWKUKw24gKRrmEz78PUUwBe){: .btn .btn--primary}   |
| MacOs  | [Download](https://drive.google.com/uc?export=download&id=1x8Xj9vCgC0vJ8hooV_ReoqcK6oU9yt0V){: .btn .btn--primary}   |

<style>
.accordion
{
    padding-inline-start: 0px;
    width: 100%;
}

.accordion li{
    list-style: none;
    width: 100%;
    overflow: hidden;
    border-radius: 8px;
    box-shadow: 0 0 10px rgba(0,0,0,0.15);
}

.accordion li label:hover{
    background: #ac0e69;
}

.accordion li label{
    display: flex;
    align-items: center;
    padding: 10px;
    margin: 0;
    background: #b60e4e;
    cursor: pointer;
}

label::before{
    content: "+";
    margin-right: 10px;
    font-size: 24px;
    font-weight: 600;
}

input[type="checkbox"]{
    display: none;
}

.accordion .content{
    max-height:0;
    overflow: hidden;
    transition: max-height 0.5s, padding 0.5s;
}

.accordion input[type="checkbox"]:checked + label + .content{
    max-height: 800px;
}
</style>
