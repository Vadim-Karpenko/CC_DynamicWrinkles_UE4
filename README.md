## Dynamic Wrinkles system for Unreal Engine 4 & CC3\iClone characters.
<a href="https://www.buymeacoffee.com/vadimkarpenko">
  <img src="/README_ASSETS/support.svg?raw=true" width="140" />
</a>

- [Currently added wrinkles](#currently-added-wrinkles)
- [How it works?](#how-it-works)
- [Requirements](#requirements)

#### Currently added wrinkles

- Forehead.
- Cheeks laugh lines.
- Eye laugh lines.
- Lips


#### How it works?
If you open the CC_Textures folder, you will find a set of normal maps that is used by this Asset.
In short, on every time when curve of your face is changed the material function will get those curve values and use them to generate a single normal map and apply it on the character. It will not affect your mesh in any way, only normal maps are used in this package.


#### Requirements
- In order to use this package you need to install a [Reallusion`s Auto setup plugin](https://www.reallusion.com/character-creator/unreal-engine-auto-setup.html "Reallusion's Auto setup plugin") into your **project**.
- This package was tested only in Unreal Engine 4.26, so keep in minds that older versions might not work.