---
permalink: /about-me/
title: "About"
author_profile: true
layout: single
toc: true
---

Meet me, a Portuguese professional game developer and programmer. With a strong passion for technology, cosmology, and astronomy, my curiosity is piqued by the recent advancements in machine learning and artificial intelligence, and the potential impact they will have on the world.

The vastness and enigmatic nature of the cosmos never fail to amaze me. With each passing year, I find myself more intrigued by the mysteries of the universe and the continuous (almost inherent) efforts of humanity to unravel its secrets.

If you'd like to say hello or engage in a conversation, feel free to reach out to me all my deatils are in my *[Contact Page](https://www.vascocorreia.github.io/contact/)*.

![Vasco](/assets/images/FotoPerfil.jpg){: .align-center}  

## <i class="fa fa-solid fa-toolbox fa-beat-fade" style="color: #b60e4e;"></i> Skills

<ul class="accordion">
    <li>
        <input type="checkbox" name="accordion" id="first">
        <label for="first">Coding</label>
        <div class="content">
            <div class="skill-bars">
                <div class="bar">
                    <div class="info">
                        <span>C#</span>
                    </div>
                    <div class="progress-line csharp">
                        <span></span>
                    </div>
                </div>
                <div class="bar">
                    <div class="info">
                        <span>SQL</span>
                    </div>
                    <div class="progress-line mysql">
                        <span></span>
                    </div>
                </div>
                <div class="bar">
                    <div class="info">
                        <span>HTML</span>
                    </div>
                    <div class="progress-line html">
                        <span></span>
                    </div>
                </div>
                <div class="bar">
                    <div class="info">
                        <span>CSS</span>
                    </div>
                    <div class="progress-line css">
                        <span></span>
                    </div>
                </div>
                <div class="bar">
                    <div class="info">
                        <span>C++</span>
                    </div>
                    <div class="progress-line cpp">
                        <span></span>
                    </div>
                </div>
             </div>
        </div>
    </li>
    <li>
        <input type="checkbox" name="accordion" id="second">
        <label for="second">Software</label>
        <div class="content">
            <div class="skill-bars">
                <div class="bar">
                    <div class="info">
                        <span>Unity</span>
                    </div>
                    <div class="progress-line unity">
                        <span></span>
                    </div>
                </div>
                <div class="bar">
                    <div class="info">
                        <span>Unreal Engine 4</span>
                    </div>
                    <div class="progress-line ue4">
                        <span></span>
                    </div>
                </div>
                <div class="bar">
                    <div class="info">
                        <span>Visual Studio</span>
                    </div>
                    <div class="progress-line vs">
                        <span></span>
                    </div>
                </div>
                <div class="bar">
                    <div class="info">
                        <span>Word</span>
                    </div>
                    <div class="progress-line word">
                        <span></span>
                    </div>
                </div>
                <div class="bar">
                    <div class="info">
                        <span>Git</span>
                    </div>
                    <div class="progress-line git">
                        <span></span>
                    </div>
                </div>
                <div class="bar">
                    <div class="info">
                        <span>Powerpoint</span>
                    </div>
                    <div class="progress-line powerpoint">
                        <span></span>
                    </div>
                </div>
                <div class="bar">
                    <div class="info">
                        <span>Excel</span>
                    </div>
                    <div class="progress-line excel">
                        <span></span>
                    </div>
                </div>
                <div class="bar">
                    <div class="info">
                        <span>Photoshop</span>
                    </div>
                    <div class="progress-line photoshop">
                        <span></span>
                    </div>
                </div>
             </div>
        </div>
    </li>
        <li>
        <input type="checkbox" name="accordion" id="third">
        <label for="third">Miscellaneous</label>
        <div class="content">
            <div class="skill-bars">
                <div class="bar">
                    <div class="info">
                        <span>Agile</span>
                    </div>
                    <div class="progress-line agile">
                        <span></span>
                    </div>
                </div>
             </div>
        </div>
    </li>
</ul>

## <i class="fas fa-solid fa-school fa-beat-fade" style="color: #b60e4e;"></i> Education

My educational journey began at Instituto Superior de Engenharia de Lisboa (ISEL), where I studied Electrical, Communication, and Computer Engineering for two years. However, during that time, I realized that something was missing for me in that particular degree.  

After careful consideration, I made a bold decision to change my course of study to pursue something that truly brought me joy. That's when I embarked on the path of Games and Apps Development at the Faculty of Design, Technology, and Communication (Iade), and graduated in 2023 and I have never looked back since.

In this new field of study, I found the perfect blend of my logical thinking abilities and my passion for creativity. It was a refreshing change that allowed me to engage my mind in a way that resonated with my interests.  

![Iade](/assets/images/iade.jpg){: .align-center}


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
    padding: 0 10px;
    max-height:0;
    overflow: hidden;
    transition: max-height 0.5s, padding 0.5s;
}

.accordion input[type="checkbox"]:checked + label + .content{
    max-height: 800px;
    padding: 10px 10px 20px;
}

.skill-bars{
  padding: 25px 30px;
  box-shadow: 5px 5px 20px rgba(0,0,0,0.2);
  border-radius: 10px;
  border-style: solid;
}
.skill-bars .bar{
  margin: 20px 0;
}
.skill-bars .bar:first-child{
  margin-top: 0px;
}
.skill-bars .bar .info{
  margin-bottom: 5px;
}
.skill-bars .bar .info span{
  font-weight: 500;
  font-size: 17px;
  opacity: 0;
  animation: showText 0.5s 1s linear forwards;
}
@keyframes showText {
  100%{
    opacity: 1;
  }
}
.skill-bars .bar .progress-line{
  height: 10px;
  width: 100%;
  background: #f0f0f0;
  position: relative;
  transform: scaleX(0);
  transform-origin: left;
  border-radius: 10px;
  box-shadow: inset 0 1px 1px rgba(0,0,0,0.05),
              0 1px rgba(255,255,255,0.8);
  animation: animate 1s cubic-bezier(1,0,0.5,1) forwards;
}
@keyframes animate {
  100%{
    transform: scaleX(1);
  }
}
.bar .progress-line span{
  height: 100%;
  position: absolute;
  border-radius: 10px;
  transform: scaleX(0);
  transform-origin: left;
  background: #f21368;
  animation: animate 1s 1s cubic-bezier(1,0,0.5,1) forwards;
}
.bar .progress-line.csharp span{
  width: 80%;
}
.bar .progress-line.css span{
  width: 30%;
}
.bar .progress-line.html span{
  width: 40%;
}
.bar .progress-line.cpp span{
  width: 30%;
}
.bar .progress-line.mysql span{
  width: 50%;
}
.bar .progress-line.unity span{
  width: 80%;
}
.bar .progress-line.ue4 span{
  width: 30%;
}
.bar .progress-line.vs span{
  width: 70%;
}
.bar .progress-line.word span{
  width: 80%;
}
.bar .progress-line.powerpoint span{
  width: 80%;
}
.bar .progress-line.git span{
  width: 70%;
}
.bar .progress-line.excel span{
  width: 40%;
}
.bar .progress-line.photoshop span{
  width: 30%;
}
.bar .progress-line.agile span{
  width: 70%;
}
.progress-line span::before{
  position: absolute;
  content: "";
  top: -10px;
  right: 0;
  height: 0;
  width: 0;
  border: 7px solid transparent;
  border-bottom-width: 0px;
  border-right-width: 0px;
  border-top-color: #000;
  opacity: 0;
  animation: showText2 0.5s 1.5s linear forwards;
}
.progress-line span::after{
  position: absolute;
  top: -28px;
  right: 0;
  font-weight: 500;
  background: #000;
  color: #fff;
  padding: 1px 8px;
  font-size: 12px;
  border-radius: 3px;
  opacity: 0;
  animation: showText2 0.5s 1.5s linear forwards;
}
@keyframes showText2 {
  100%{
    opacity: 1;
  }
}
.progress-line.csharp span::after{
  content: "80%";
}
.progress-line.css span::after{
  content: "30%";
}
.progress-line.html span::after{
  content: "40%";
}
.progress-line.cpp span::after{
  content: "30%";
}
.progress-line.mysql span::after{
  content: "50%";
}
.progress-line.unity span::after{
  content: "80%";
}
.progress-line.ue4 span::after{
  content: "30%";
}
.progress-line.vs span::after{
  content: "70%";
}
.progress-line.word span::after{
  content: "80%";
}
.progress-line.powerpoint span::after{
  content: "80%";
}
.progress-line.git span::after{
  content: "70%";
}
.progress-line.excel span::after{
  content: "40%";
}
.progress-line.photoshop span::after{
  content: "30%";
}
.progress-line.agile span::after{
  content: "70%";
}
</style>


