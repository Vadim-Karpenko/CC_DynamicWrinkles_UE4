# Dynamic Wrinkles system for Unreal Engine 4 & CC3\iClone characters.
<a href="https://www.buymeacoffee.com/vadimkarpenko" target="_blank">
  <img src="/README_ASSETS/support.svg?raw=true" width="140" />
</a>

## Overview
- [Demo](#demo)
- [Currently added wrinkles](#currently-added-wrinkles)
- [How it works?](#how-it-works)
- [Requirements](#requirements)
- [Installation](#installation)
- [How to use](#how-to-use)

### Demo
(Youtube links)

<a href="http://www.youtube.com/watch?v=uWozhgB1Ass" target="_blank">
  <img alt="Dynamic wrinkles demo 1 (Unreal Engine 4, Character Creator 3, iClone)" src="http://img.youtube.com/vi/uWozhgB1Ass/0.jpg" width="370" />
</a>
<a href="http://www.youtube.com/watch?v=daqsdB_arvo" target="_blank">
  <img alt="Dynamic wrinkles demo 2 (Unreal Engine 4, Character Creator 3, iClone)" src="http://img.youtube.com/vi/daqsdB_arvo/0.jpg" width="370" />
</a>

### Currently added wrinkles

- Forehead.
- Cheeks laugh lines.
- Eye laugh lines.
- Lips


### How it works?
If you open the CC_Textures folder, you will find a set of normal maps that is used by this Asset.
In short, on every time when curve of your face is changed the material function will get those curve values and use them to generate a single normal map and apply it on the character. It will not affect your mesh in any way, only normal maps are used in this package.


### Requirements
- In order to use this package you need to install a [Reallusion`s Auto setup plugin](https://www.reallusion.com/character-creator/unreal-engine-auto-setup.html "Reallusion's Auto setup plugin") into your **project**.
- This package was tested only in Unreal Engine 4.26, so keep in minds that older versions might not work.


### Installation
- Clone or download this repository.
- Move **DynamicWrinkles** folder from this repository into your **YourProject/Content** folder.


### How to use
- Open your **DynamicWrinkles** folder and locate **AddWrinkles_CC** material function, we'll need it later.
    <img src="/README_ASSETS/1.png?raw=true" width="500" />
- Go to **Content/CC_Shaders/SkinShader** and open **RL_HQSkin** material.
    <img src="/README_ASSETS/2.png?raw=true" width="500" />
- Locate the pin connected to the Normal input
    <img src="/README_ASSETS/3.png?raw=true" width="500" />
- Follow the pin to the bottom
    <img src="/README_ASSETS/4.png?raw=true" width="500" />
- Drag & Drop **AddWrinkles_CC** function from the **DynamicWrinkles** folder into this place and connect correspondingly.
    <img src="/README_ASSETS/5.png?raw=true" width="500" />
- Go to the place where your character is located and open Skeletal Mesh of your character.
    <img src="/README_ASSETS/11.png?raw=true" width="500" />
- At the left side of the screen locate the Material instance for character's head.
    <img src="/README_ASSETS/12.png?raw=true" width="500" />
- At the Material Instance enable the wrinkles option. Please note that default settings below will require configuration for each idividual character.
    <img src="/README_ASSETS/14.png?raw=true" width="500" />
- Now we need to create an Animation Blueprint for your character. Left click on your Skeletal mesh -> Create -> Anim Blueprint
    <img src="/README_ASSETS/7.png?raw=true" width="600" />
- In the Event Graph connect **Event Blueprint Update Animation** node with **Process Wrinkle Curves CC** node. Use "wrinkle" keyword to find it in the search.
    <img src="/README_ASSETS/8.png?raw=true" width="600" />
- Connect **Self** node to the **Target** input.
    <img src="/README_ASSETS/9.png?raw=true" width="600" />
- Open the **AnimGraph** tab and drag & drop your animation (You can use for testing the animation from the Example folder). If the wrinkles on the face is barely visible in the preview window, it is possible that you need to tweak settings in the Material Instance of your head.
    <img src="/README_ASSETS/10.png?raw=true" width="600" />