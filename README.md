# Dynamic Wrinkles system for Unreal Engine 4 & CC3\iClone characters.

## Overview
- [Demo](#demo)
- [Currently added wrinkles](#currently-added-wrinkles)
- [How it works?](#how-it-works)
- [Requirements](#requirements)
- [Installation](#installation)

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
- Open your **DynamicWrinkles** folder and locate **AddWrinkles_CC** material function, we'll need it later.

    <img src="/README_ASSETS/1.png?raw=true" width="800" />
- Go to **Content/CC_Shaders/SkinShader** and open **RL_HQSkin** material.

    <img src="/README_ASSETS/2.png?raw=true" width="800" />
- Locate the pin connected to the Normal input

    <img src="/README_ASSETS/3.png?raw=true" width="800" />
- Follow the pin to the bottom

    <img src="/README_ASSETS/4.png?raw=true" width="800" />
- Drag & Drop **AddWrinkles_CC** function from the **DynamicWrinkles** folder into this place and connect correspondingly.

    <img src="/README_ASSETS/5.png?raw=true" width="800" />
- Go to the place where your character is located and open Skeletal Mesh.

    <img src="/README_ASSETS/11.png?raw=true" width="800" />
- At the left side of the screen locate the Material instance for character's head.

    <img src="/README_ASSETS/12.png?raw=true" width="800" />
- Enable the wrinkles. Settings below may require configuration later.

    <img src="/README_ASSETS/14.png?raw=true" width="800" />
- Create an Animation Blueprint for your character. Left click on your Skeletal mesh -> Create -> Anim Blueprint. Note that if you're planning to use new ARKit curves from CC 3.4, you probably already have Animation blueprint from <a href="https://forum.reallusion.com/476282/How-to-Animate-CC3--Character-with-Unreal-Live-Link-Face">this guide</a>

    <img src="/README_ASSETS/7.png?raw=true" width="800" />
- In the Event Graph connect **Event Blueprint Update Animation** node with **Process Wrinkle Curves CC** node. Use "wrinkle" keyword to find it.

    <img src="/README_ASSETS/8.png?raw=true" width="800" />

    # Dynamic Wrinkles system for Unreal Engine 4 & CC3\iClone characters.

## Overview
- [Demo](#demo)
- [Currently added wrinkles](#currently-added-wrinkles)
- [How it works?](#how-it-works)
- [Requirements](#requirements)
- [Installation](#installation)

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
- Open your **DynamicWrinkles** folder and locate **AddWrinkles_CC** material function, we'll need it later.

    <img src="/README_ASSETS/1.png?raw=true" width="800" />
- Go to **Content/CC_Shaders/SkinShader** and open **RL_HQSkin** material.

    <img src="/README_ASSETS/2.png?raw=true" width="800" />
- Locate the pin connected to the Normal input

    <img src="/README_ASSETS/3.png?raw=true" width="800" />
- Follow the pin to the bottom

    <img src="/README_ASSETS/4.png?raw=true" width="800" />
- Drag & Drop **AddWrinkles_CC** function from the **DynamicWrinkles** folder into this place and connect correspondingly.

    <img src="/README_ASSETS/5.png?raw=true" width="800" />
- Go to the place where your character is located and open Skeletal Mesh.

    <img src="/README_ASSETS/11.png?raw=true" width="800" />
- At the left side of the screen locate the Material instance for character's head.

    <img src="/README_ASSETS/12.png?raw=true" width="800" />
- Enable the wrinkles. Settings below may require configuration later.

    <img src="/README_ASSETS/14.png?raw=true" width="800" />
- Create an Animation Blueprint for your character. Left click on your Skeletal mesh -> Create -> Anim Blueprint. Note that if you're planning to use new ARKit curves from CC 3.4, you probably already have Animation blueprint from <a href="https://forum.reallusion.com/476282/How-to-Animate-CC3--Character-with-Unreal-Live-Link-Face">this guide</a>

    <img src="/README_ASSETS/7.png?raw=true" width="800" />
- In the Event Graph connect **Event Blueprint Update Animation** node with **Process Wrinkle Curves CC** node. Use "wrinkle" keyword to find it. 
    <img src="/README_ASSETS/8.png?raw=true" width="800" />
    
    For the blueprint from ARKit, just place the node at the very end of the BP logic.
    <img src="/README_ASSETS/16.jpg?raw=true" width="800" />
- Connect **Self** node to the **Target** input.

    <img src="/README_ASSETS/9.png?raw=true" width="800" />
- Open the **AnimGraph** tab and drag the animation, or use the [test animation](https://github.com/Vadim-Karpenko/CC_DynamicWrinkles_UE4/tree/master/Example) provided by this repository. If the wrinkles on the face is barely visible in the preview window, it is possible that you need to tweak settings in the Material Instance.

    <img src="/README_ASSETS/10.png?raw=true" width="1000" />
- To see your animation during gameplay you will need to select your character in the World Outliner and select your Anim Blueprint in the settings.

    <img src="/README_ASSETS/15.png?raw=true" width="1000" />

- Connect **Self** node to the **Target** input.

    <img src="/README_ASSETS/9.png?raw=true" width="800" />
- Open the **AnimGraph** tab and drag the animation, or use the [test animation](https://github.com/Vadim-Karpenko/CC_DynamicWrinkles_UE4/tree/master/Example) provided by this repository. If the wrinkles on the face is barely visible in the preview window, it is possible that you need to tweak settings in the Material Instance.

    <img src="/README_ASSETS/10.png?raw=true" width="1000" />
- To see your animation during gameplay you will need to select your character in the World Outliner and select your Anim Blueprint in the settings.

    <img src="/README_ASSETS/15.png?raw=true" width="1000" />
