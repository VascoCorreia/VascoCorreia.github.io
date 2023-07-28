---
title: "Spirit, A World Beneath"
layout: single
permalink: /spirit-a-world-beneath/
author_profile: true
toc: true
header:
  video:
    id: xhcFo2AvP_U?vq=hd1080
    provider: youtube
---
{% comment %} 
overlay_filter: rgba(0, 0, 100, 0.1)
# overlay_image: /assets/images/SpiritBanner2.png
# image_description: "James Webb Telescope deep field." 

{% include video id="1hr_v41a_SVjEYDWhFd6z2Gh-yxX1XIUJ" provider="google-drive" %}  
(You can increase the video quality)  
{: .text-center .style="font-size= 5px;"}

{% endcomment %}
<a href="https://github.com/VascoCorreia/Spirit-A-World-Beneath" target="_blank"> <i class="fab fa-brands fa-github fa-2x"></i></a>
{: .text-right}
<hr>
## <i class="fa fa-solid fa-ghost" style="color: #ae0c4e;"></i> Overview
Spirit, A World Beneath is a 3D third-person game designed for local multiplayer split-screen gameplay, where you and your friend can team up to tackle the challenges together.  

Play as Rory and as a mysterious spirit and uncover the secrets of the ancient Scottish underground tunnels.

As you explore the tunnels, you will need to search for the key components to overcome each puzzle room.  

Along the way, you can use the Spirit to possess enemies and objects to access different behaviours, also you must use Rory's whistle to distract and attract enemies.  

Cooperation is key to sucess. You will need to work together to navigate the tunnels and overcome obstacles on your journey to the final room.  

Get ready for a thrilling adventure that will put your puzzle solving skills and teamwork to the test!

**Important:** Two Ps4 controllers are required to play! Intended to change.
{: .notice--danger .text-center}  

## <i class="fas fa-solid fa-gamepad" style="color: #ae0c4e;"></i> Gameplay  
<ul class="collapsible">
<li>
<input type="checkbox" name="collapsible" id="first">
<label for="first">Expand</label>
<div class="content" markdown="1">
### Movement
Players can move freely in the X and Z axis and Jump to move in the Y axis, the movement is done using a **Character Controller** component and a custom script since the movement of the game is not heavily relying on physics.  
The movement is **camera-relative**.  

After necessary calculations the movementis handled by the `CharacterControler.Move()` method inside the **Character Controller** object.  

Rory             |  Spirit
:-------------------------:|:-------------------------:
![RoryMovement](/assets/images/Spirit/RoryMovement.gif)  |  ![SpiritMovement](/assets/images/Spirit/SpiritMovement.gif)
{: .align-center}  

To simulate gravity the vector Y component that is be passed as a parameter for the `CharacterController.Move()` is updated every frame:

`_ySpeed = Physics.gravity.y * Time.deltaTime;`

If Rory is touching the ground he should stop moving in the Y component, to achieve this a check is made.

`if (_onGround)
{
     _ySpeed = -0.01f;
}`  

This hack resets the player speed allowing the is grounded condition to work properly.  
To check if the character a **Spherecast** is made on the bottom of the character controller collider to check if it checking if it collides with the world.

### Interactions with the environment
Rory can interact with physical objects, contrary to the spirit.  
Interactions have a 1 second cooldown.

#### Pulling crates.
The crate is parented to Rory and has a **Rigibody** component that is set to kinematic when the player is pulling.  

![RoryPullCrate](/assets/images/Spirit/RoryPullCrate.gif){: .align-center}  

#### Pushing Buttons
Buttons are directly connected to a barrier. They are used to deactivate them.

Barries are designed to function in two ways: either the player must continuously press the button to keep it open, or a single click on the button will suffice to keep it open.

#### Calling Bats
Rory is able to whistle to call the mobs in the level, this can be done by clicking R1 in the controller.
When Rory whistles an event is fired, and the first thing the bat class does is check the distance between its instance and Rory, if it's below a certain threshold the bat will enter its Check State.  

![RoryWhistle](/assets/images/Spirit/RoryWhistle.gif){: .align-center}  

This should be used to make a bat come close enough for the spirit to perform a possession.

### Bats
The bat is controlled by Artificial Intelligence, more specifically a **Finite state machine**. 

This state machine has 4 states: Wander, Called, Chase, and Return.

#### 1) Wander
In the Wander State, bats will fly around in a certain position, meaning they will not fly around all the areas of the map.  

#### 2) Called State
When Rory whistles all colliders inside a defined sphere are detected, then the colliders are filtered to only keep the ones that belong to a bat.

With this, all bat objects are added to a list, and the bat that occupies index 1 will go to the position where the whistle was performed.  

#### 3) Chase State
When Rory or a possessed bat enters a predifined sphere (with the bat at its center), the bat will start chasing Rory (or the Spirit if it's possessing another bat).  
If the bat collides with Rory the level is restarted. If it collides with the spirit the current possession is exited.

#### 4) Return State
The condition to enter this state is met when the bat leaves either the called state or the chase state.
When the bats are in the return state, they will quickly go back to the wander state radius, either by just going back and wandering, or going to the center of this radius and wandering.

### Possession
The spirit is able to possess various things in the cave.

#### 1) Bats
Possessing bats allows the spirit to control them, which it turns gives him the ability to fly and press buttons.

#### 2) Mushrooms
Possessing a mushroom allows the spirit to grow the mushroom or make it shrink.

#### 3) Crystals
Possessing a crystal allows the spirit to emit a powerfull light to iluminate paths.

### Camera
Camera utilize the Unity <a href="https://unity.com/unity/features/editor/art-and-design/cinemachine" target="_blank">Cinemachine</a> package.
There are 2 FreeLookCameras, each following one player.  

Each cameras is made out of 3 rigs (bottom, middle, and top) and a spline connecting the rigs.  

![Camera](/assets/images/Spirit/CameraMockup.png){: .align-center}  

#### Camera Collision
A raycast is done between the camera position and the player position if there is a gameobject between them the camera moves to an alternate point of view while attempting to keep the camera at its original height.
This means that on detection the camera will damp to the closest point that is not occluded and is as close as possible to the height of the "original" camera.  

![CameraCollision](/assets/images/Spirit/CameraCollision.gif){: .align-center}

#### Objects Invisible
When the camera is between objects and the player these objects will become transparent. This is done by changing attributes inside the shaders of the objects.
</div>
</li>
</ul>

<hr>
## <i class="fa fa-solid fa-gamepad" style="color: #ae0c4e;"></i> Controls  

<ul class="collapsible">
    <li>
        <input type="checkbox" name="collapsible" id="second">
        <label for="second">Expand</label>
        <div class="content">
            <table>
              <thead>
                <tr>
                    <th style="text-align: center">Action</th>
                    <th style="text-align: center">Key</th>
                </tr>
              </thead>
              <h2>Rory</h2>
              <tbody>
                  <tr>
                    <td style="text-align: center">Gamepad 1 Left Analog</td>
                    <td style="text-align: center">Movement</td>
                  </tr>
                  <tr>
                    <td style="text-align: center">Gamepad 1 Right Analog</td>
                    <td style="text-align: center">Move camera</td>
                  </tr>
                  <tr>
                    <td style="text-align: center">Gamepad 1 X</td>
                    <td style="text-align: center">Jump</td>
                  </tr>
                  <tr>
                    <td style="text-align: center">Gamepad 1 Square</td>
                    <td style="text-align: center">Interact</td>
                  </tr>
                  <tr>
                    <td style="text-align: center">Gamepad 1 R1</td>
                    <td style="text-align: center">Whistle</td>
                  </tr>
               </tbody>
            </table>
            <table>
              <thead>
                <tr>
                    <th style="text-align: center">Action</th>
                    <th style="text-align: center">Key</th>
                </tr>
              </thead>
              <h2>Spirit</h2>
              <tbody>
                  <tr>
                    <td style="text-align: center">Gamepad 2 Left Analog</td>
                    <td style="text-align: center">Movement</td>
                  </tr>
                  <tr>
                    <td style="text-align: center">Gamepad 2 Right Analog</td>
                    <td style="text-align: center">Move camera</td>
                  </tr>
                  <tr>
                    <td style="text-align: center">Gamepad 2 X</td>
                    <td style="text-align: center">Jump</td>
                  </tr>
                  <tr>
                    <td style="text-align: center">Gamepad 2 Square</td>
                    <td style="text-align: center">Interact</td>
                  </tr>
                  <tr>
                    <td style="text-align: center">Gamepad 2 R1</td>
                    <td style="text-align: center">Possession</td>
                  </tr>
               </tbody>
            </table>
        </div>
    </li>
</ul>
## <i class="fa fa-solid fa-download" style="color: #ae0c4e;"></i> Download Builds  

| Build | Download |
| :--------: | :--------: |
| Windows | [MISSING FILE](){: .btn .btn--primary}   |
| MacOs  | [MISSING FILE](){: .btn .btn--primary}   |

## <i class="fa fa-solid fa-book" style="color: #ae0c4e;"></i> Documentation 

| Document | Download |
| :--------: | :--------: |
| Game Design Document   | [View](https://drive.google.com/file/d/1wmc88soNyg0D2Mzbw1NCY5drLffhZJh1/view?usp=sharing){: .btn .btn--primary}   |
| Spec Sheet   | [View](https://drive.google.com/file/d/1UGSFAZr6QGnFzS--s0V5b6pZ76flO1oK/view?usp=sharing){: .btn .btn--primary}   |