**A collection of work-in-progress 720x720 overlays for the RG CubeXX and other devices. Tested on muOS Pixie.**

# Contents
1. [Game Boy Pocket & Light](https://github.com/mugwomp93/720x720_overlays/tree/main#game-boy-pocket--light)
2. [Game Boy Color](https://github.com/mugwomp93/720x720_overlays/tree/main#game-boy-color)
3. [Game Gear](https://github.com/mugwomp93/720x720_overlays/tree/main#game-gear)
4. [Assorted 1playerinsertcoin Grid Overlays](https://github.com/mugwomp93/720x720_overlays/tree/main#assorted-1playerinsertcoin-grid-overlays) - GBA, GBC, GG, NGPC, PICO-8

# Notes
I normally wouldn't upload anything that wasn't finished; however, I likely won't be completing these any time soon so I thought I would make them available in case anyone wants to use them. I'll update with additional, revised, and/or final overlays as time and interest permit.

- I haven't uploaded anything that I wouldn't use myself, but be aware that there are still a number of minor visual issues that need to be resolved. Please let me know if you want to take a shot at fixing them - I'm happy to provide my working materials (as messy as they are). Otherwise, I'll get to them eventually. Probably.

- With the exception of the GB overlays, the overlay grids were created by [1playerinsertcoin](https://www.reddit.com/u/1playerinsertcoin/s/yhapRMwOJz). Since they don't have a 720x720 device, I fixed the alignment where necessary and reviewed different versions. As such, credit for all of the good qualities of these grids (and there are many!) goes to 1playerinsertcoin. Any deficiencies are my own.

### Important notes regarding sample images:
- ***Gridlines:***<br>
The apparent (un)evenness of gridlines in the images below depends on a number of factors, including the size, resolution, and % zoom of the viewing display, as well as any scaling applied by Github. Your best bet to avoid scaling artifacts is to download the individual images and view at 100% zoom. For best viewing, I've found that 100% zoom on a 14" QHD screen gives a fairly accurate representation of real-life size and appearance.
- ***Colors:***<br>
Screenshots are recorded at a default brightness. As a result, images with dark overlays appear very dark. I've altered the brightness, contrast, and saturation of the sample images to better approximate what you can expect to see on device, but they're not completely accurate to real life. For the images with dark overlays, I've included insets of the raw, unedited screenshots to give a better idea of the relative effects of the grid overlays as playing with the image parameters can alter the apparent strength etc. of the gridlines relative to the image behind them. Note also that ymmv depending on your viewing display.

# [Game Boy Pocket & Light](https://github.com/mugwomp93/720x720_overlays/tree/main/720x720%20overlays/GB)
![GBP_composite](https://github.com/user-attachments/assets/2d685d1d-fc20-47b8-bd4e-e7da518a7416)
![GBL-Teal_composite](https://github.com/user-attachments/assets/3087a755-916e-47e7-ac5e-7ff7f908a2ae)
![GBL-Blue_composite](https://github.com/user-attachments/assets/559a4d03-7060-46c7-bacf-e425b2cf0f25)
*I've noticed that the colors of the Game Boy Light palettes in the images above vary significantly depending on the display they're being viewed on. If they appear desaturated, be assured that they're not when viewed on device.*<br><br>

These overlays work with a shader preset to produce custom palettes and a subtle pixel shadow effect. The shader preset is a combination of the [sharp-shimmerless interpolation shader](https://github.com/Woohyun-Kang/Sharp-Shimmerless-Shader) and gb-pass4 from Gameboy Shader 0.2.2. I've bundled copies of these shaders up in their own folder, both to keep everything tidy and because I modified the gb-pass4 palette files, but any credit should go to their original creators.

I'm also working on a DMG version but it's not as far along.<br>

## Configuration
<details>
  <summary>Click for installation and settings</summary>

  ### Installation:

  - [Download](https://github.com/mugwomp93/720x720_overlays/tree/main/720x720%20overlays/GB/GB.zip) GB.zip and copy the contents of the shaders and overlays folders to your retroarch > shaders and retroarch > overlays folders, respectively.

  ### Settings:

  #### 1. Core Options

    Quick Menu > Core Options:

        GB Colorization > Off

        Interframe Blending	> Simple (NOTE: If you don't like the image ghosting, turn it OFF, but you may see flickering elements in games.)

        Manage Core Options > Save Content Directory Options
  
  #### 2. Apply the Overlay:
  
    Quick Menu > On-Screen Overlay

         Display Overlay > ON

         Overlay Preset...
           > Navigate to retroarch > overlays > mugwomp93 > 720x720 and select your preferred overlay (GB Pocket, GB Light - Teal, GB Light - Blue)

         Overlay Opacity > 1.00

  #### 3. Apply the Shader Preset:
  
    Quick Menu > Shaders

        Video Shaders ON

        Load Preset...
          > Navigate to retroarch > shaders > mugwomp93 and select the preset that corresponds to the overlay you selected (GB Pocket, GB Light - Teal, GB Light - Blue)

        Apply Changes

        Save Preset > Save Content Directory Preset

  #### 4. Scaling Settings:
    
    Main Menu > Settings > Video > Scaling
    
        Integer Scale > OFF
    
        Integer Scale Axis > (shouldn't matter)
    
        Integer Scale Scaling > (shouldn't matter)
    
        Aspect Ratio > Custom
    
            Custom Aspect Ratio (X Position) > 0
    
            Custom Aspect Ratio (Y Position) > 25
    
            Custom Aspect Ratio (Width) > 720
    
            Custom Aspect Ratio (Height) > 648
    
        Viewport Anchor Bias X > 0.50
    
        Viewport Anchor Bias Y > 1.00 (try 0.00 if the image isn't properly aligned with 1.00)
    
        Bilinear Filtering > OFF
    
        Crop Overscan > OFF

  #### 5. Save an Override

    Quick Menu > Overrides > Save Content Directory Overrides  
</details>

### Notes:
- ***These are bright overlays. You'll want to decrease your screen brightness for best results.***
- The colors aren't intended to be 100% true to the original devices. Consider them "inspired by" instead of accurate representations.
- Pixellate and pixel_aa produce slightly better interpolation results than sharp-shimmerless, but they're more resource intensive and can produce lag and audio issues in more demanding games on the CubeXX (e.g., Donkey Kong Land) so I've stuck with sharp-shimmerless.
- You may notice that some of the pixel shadows are bisected by the grid lines. I don't really notice this on device (it's much more apparent in the screenshots), but if it bothers you, you can adjust Shadow Offset Vert in the shader parameters to +4.50. This will position the shadows at a full 1 game pixel offset, 45 degrees down and left of their respective pixels.
- I suggest leaving Shadow Offset Horiz at 4.50 as the preset value adds a shadow on the right edge of the screen that the overlays are design to complement. They may look weird if you reduce the horizontal shadow or change the direction. Similarly, the edge shadows on the overlay may look strange if used without the shader preset.

# [Game Boy Color](https://github.com/mugwomp93/720x720_overlays/tree/main/720x720%20overlays/GBC)
![GBC_composite](https://github.com/user-attachments/assets/681377bf-286f-447e-8095-c6781f2463b2)

1playerinsertcoin was kind enough to create a number of iterations of this overlay grid for testing. I think the final version looks fantastic, which is especially impressive considering they don't have a 720x720 device. I'm not 100% happy with the edge shadow so I may revisit it at some point, but otherwise this is as close to finished as any of these overlays.

## Configuration
<details>
  <summary>Click for installation and settings</summary>

  ### Installation:

  - [Download](https://github.com/mugwomp93/720x720_overlays/tree/main/720x720%20overlays/GBC) both GBC_720x720.png and GBC_720x720.cfg and save them to your retroarch > overlays folder<br>
  - *Note: You can make subfolders if desired; I save mine to retroarch > overlays > mugwomp93 > 720x720 to help keep things organized*

  ### Settings:

  #### 1. Core Options

    Quick Menu > Core Options:

        GB Colorization > GBC

        Color Correction > GBC Only

        Color Correction Mode > Accurate

        Color Correction - Frontlight Position > Above Screen (lighter, more realistic GBC colors) or Central (darker, more vibrant colors)

        Interframe Blending	> Simple (NOTE: If you don't like the image ghosting, turn it OFF, but you may see flickering elements in games.)

        Manage Core Options > Save Content Directory Options
  
  #### 2. Apply the Overlay:
  
    Quick Menu > On-Screen Overlay

         Display Overlay > ON

         Overlay Preset...
           > Navigate to where you saved the .png and .cfg files and select GBC_720x720.cfg

         Overlay Opacity > 1.00

  #### 3. Apply Shaders:
  
- *Note 1: If you're using muOS, sharp-shimmerless is applied by default. There's no need to change the shader settings.*
  
- *Note 2: If sharp-shimmerless isn't available on your device, you can use interpolation > sharp-bilinear instead. Or you can download sharp-shimmerless from [here](https://github.com/Woohyun-Kang/Sharp-Shimmerless-Shader).*
    
      Quick Menu > Shaders

          Video Shaders ON

          Shader Passes > 1
        
              Shader #0: shimmerless > shaders > sharp-shimmerless.glsl

              Shader #0 Filter: Linear

              Shader #0 Scale: Default

          Apply Changes

          Save Preset > Save Content Directory Preset
 
  #### 4. Scaling Settings:
    
      Main Menu > Settings > Video > Scaling
    
          Integer Scale > OFF
    
          Integer Scale Axis > (shouldn't matter)
    
          Integer Scale Scaling > (shouldn't matter)
    
          Aspect Ratio > Custom
    
              Custom Aspect Ratio (X Position) > 0
    
              Custom Aspect Ratio (Y Position) > 25
    
              Custom Aspect Ratio (Width) > 720
    
              Custom Aspect Ratio (Height) > 648
    
          Viewport Anchor Bias X > 0.50
    
          Viewport Anchor Bias Y > 1.00 (try 0.00 if the image isn't properly aligned with 1.00)
    
          Bilinear Filtering > OFF
    
          Crop Overscan > OFF

  #### 5. Save an Override

      Quick Menu > Overrides > Save Content Directory Overrides
</details>

### Notes:
- ***This is a dark overlay. You'll want to increase your screen brightness for best results.***
- A version of this overlay without border graphics and shadows is available below in [assorted 1playerinsertcoin grid overlays](https://github.com/mugwomp93/720x720_overlays/tree/main#assorted-1playerinsertcoin-grid-overlays). A 4x integer version is also available.

# [Game Gear](https://github.com/mugwomp93/720x720_overlays/tree/main/720x720%20overlays/GG)
![GG_composite](https://github.com/user-attachments/assets/38eecb2b-b9f6-45e9-be67-3cbbc1dbbe9d)

Another 1playerinsertcoin grid. This one doesn't specifically emulate the Game Gear screen (it's also not 4:3, so we've already deviated from reality) but it includes some really nice enhanced LCD subpixel effects. Same issue with the edge shadow as for GBC.

## Configuration
<details>
  <summary>Click for installation and settings</summary>

  ### Installation:

  - [Download](https://github.com/mugwomp93/720x720_overlays/tree/main/720x720%20overlays/GG) GG_720x720.png and GG_720x720.cfg (and/or GG_720x720_alt.png and GG_720x720_alt.cfg) and save them to your retroarch > overlays folder<br>
  - *Note: You can make subfolders if desired; I save mine to retroarch > overlays > mugwomp93 > 720x720 to help keep things organized*

  ### Settings:

  #### 1. Apply the Overlay:
  
    Quick Menu > On-Screen Overlay

         Display Overlay > ON

         Overlay Preset...
           > Navigate to where you saved the .png and .cfg files and select GG_720x720.cfg or GG_720x720_alt.cfg

         Overlay Opacity > 1.00

  #### 2. Apply Shaders:
  
- *Note 1: If you're using muOS, sharp-shimmerless is applied by default. There's no need to change the shader settings.*
  
- *Note 2: If sharp-shimmerless isn't available on your device, you can use interpolation > sharp-bilinear instead. Or you can download sharp-shimmerless from [here](https://github.com/Woohyun-Kang/Sharp-Shimmerless-Shader).*
    
      Quick Menu > Shaders

          Video Shaders ON

          Shader Passes > 1
        
              Shader #0: shimmerless > shaders > sharp-shimmerless.glsl

              Shader #0 Filter: Linear

              Shader #0 Scale: Default

          Apply Changes

          Save Preset > Save Content Directory Preset
   
  #### 3. Scaling Settings:
    
    Main Menu > Settings > Video > Scaling
    
        Integer Scale > OFF
    
        Integer Scale Axis > (shouldn't matter)
    
        Integer Scale Scaling > (shouldn't matter)
    
        Aspect Ratio > Custom
    
            Custom Aspect Ratio (X Position) > 0
    
            Custom Aspect Ratio (Y Position) > 25
    
            Custom Aspect Ratio (Width) > 720
    
            Custom Aspect Ratio (Height) > 648
    
        Viewport Anchor Bias X > 0.50
    
        Viewport Anchor Bias Y > 1.00 (try 0.00 if the image isn't properly aligned with 1.00)
    
        Bilinear Filtering > OFF
    
        Crop Overscan > OFF

  #### 4. Save an Override

      Quick Menu > Overrides > Save Content Directory Overrides
</details>

### Notes:
- ***This is a dark overlay. You'll want to increase your screen brightness for best results.***
- This version uses 1playerinsertcoin's grid at 90% opacity. There's also an alt version that I've mucked around with to desaturate the colors a bit.
- The base version of this overlay at 100% opacity and without border graphics and shadows is available below in [assorted 1playerinsertcoin grid overlays](https://github.com/mugwomp93/720x720_overlays/tree/main#assorted-1playerinsertcoin-grid-overlays). A 4:3 version (no more skinny Sonic) is also available.

# [Assorted 1playerinsertcoin Grid Overlays](https://github.com/mugwomp93/720x720_overlays/tree/main/720x720%20overlays/1playerinsertcoin%20Assorted%20Overlays)
As you may have gathered, 1playerinsertcoin has been very generous with their time in creating overlays for a device they don't even own. In addition to the overlays listed above, they've also created versions for GBA, NGPC, and PICO-8. Since I don't know when I'll get around to making borders for these, I've decided to upload all of the 720x720 overlays they've created for me so others can enjoy. These overlays don't have any border decorations, shadows, etc, and, with one exception, are all centered. Please credit 1playerinsertcoin if you use these to create your own versions.<br>
### Game Boy Advance
- 3x integer<br><br>  
  ![GBA_1pic](https://github.com/user-attachments/assets/763d2ce7-38f4-49da-9d74-23b39f6979c5)<br><br>

### Game Boy Color
- Non-integer (720x648)
- 4x integer
- 4x integer offset<br><br>

  ![GBC_1pic](https://github.com/user-attachments/assets/cb05f167-f631-41d2-a8f9-3bb37f154884)<br><br>

### Game Gear
- Non-integer (720x648; square pixels)
- Non-integer 4:3 (720x540; rectangular pixels)<br><br>

  ![GG_1pic](https://github.com/user-attachments/assets/7090374a-c84f-4445-8ed8-6e9c2d72249f)<br><br>

### Neo Geo Pocket Color
- Non-integer (720x684)
- 4x integer<br><br>

  ![NGPC_1pic](https://github.com/user-attachments/assets/16ccf033-48ea-424b-a61a-d5df7cd3bb9e)<br><br>

### PICO-8
- Non-integer (720x720)<br><br>

  ![PICO_1pic](https://github.com/user-attachments/assets/bd37afd6-17d8-49be-b799-808ee60975eb)<br><br>

## Configuration
<details>
  <summary>Click for installation and settings</summary>
  
  ### Installation:

  - [Download](https://github.com/mugwomp93/720x720_overlays/tree/main/720x720%20overlays/1playerinsertcoin%20Assorted%20Overlays) the .png and .cfg files for the overlay(s) you're interested in and save them to your retroarch > overlays folder.
  - *Note: You can make subfolders if desired; e.g., retroarch > overlays > mugwomp93 > 720x720 > 1playerinsertcoin*

  ### Settings:

  #### 1. Apply the Overlay:
  
    Quick Menu > On-Screen Overlay

         Display Overlay > ON

         Overlay Preset...
           > Navigate to where you saved the .png and .cfg files and select your chosen overlay

         Overlay Opacity > 1.00

  #### 2. Apply Shaders:
  
- *Note 1: If you're using muOS, sharp-shimmerless is applied by default. There's no need to change the shader settings.*
  
- *Note 2: If sharp-shimmerless isn't available on your device, you can try using interpolation > sharp-bilinear (or other interpolation shader) instead. Or you can download sharp-shimmerless from [here](https://github.com/Woohyun-Kang/Sharp-Shimmerless-Shader).*
    
      Quick Menu > Shaders

          Video Shaders ON

          Shader Passes > 1
        
              Shader #0: shimmerless > shaders > sharp-shimmerless.glsl

              Shader #0 Filter: Linear

              Shader #0 Scale: Default

          Apply Changes

          Save Preset > Save Content Directory Preset
   
  #### 3. Scaling Settings (click to expand):
    
  <details><summary>i. Integer scale overlays - except for Perfect_GBC-720p(4x offset)</summary>
    
      Main Menu > Settings > Video > Scaling

          Integer Scale > ON

          Integer Scale Axis > (shouldn't matter)

          Integer Scale Scaling > Underscale

          Aspect Ratio > Core provided

          Viewport Anchor Bias X > 0.50

          Viewport Anchor Bias Y > 0.50

          Bilinear Filtering > OFF

          Crop Overscan > OFF
  </details>

  <details><summary>ii. Perfect_GBC-720p(4x offset)</summary>

      Main Menu > Settings > Video > Scaling

          Integer Scale > ON

          Integer Scale Axis > (shouldn't matter)

          Integer Scale Scaling > Underscale

          Aspect Ratio > Custom

              Custom Aspect Ratio (X Position) > 0

              Custom Aspect Ratio (Y Position) > 41

              Custom Aspect Ratio (Width) > 640 (4x)

              Custom Aspect Ratio (Height) > 576 (4x)

          Viewport Anchor Bias X > 0.50

          Viewport Anchor Bias Y > 0.00

          Bilinear Filtering > OFF

          Crop Overscan > OFF
  </details>	

  <details><summary>iii. Non-integer scale overlays</summary>

      Main Menu > Settings > Video > Scaling

          Integer Scale > OFF

          Integer Scale Axis > (shouldn't matter)

          Integer Scale Scaling > (shouldn't matter)

          Aspect Ratio > Core Provided or 4:3 for Perfect_GG-720p(4x3)

          Viewport Anchor Bias X > 0.50

          Viewport Anchor Bias Y > 0.50

          Bilinear Filtering > OFF

          Crop Overscan > OFF
  </details>

  #### 4. Save an Override

      Quick Menu > Overrides > Save Content Directory Overrides
</details>

### Notes:
- ***These are dark overlays. You'll want to increase your screen brightness for best results.***
- The PICO-8 overlay produces a striking effect, but I find it's more comfortable to play at reduced opacity. I usually use ~70-75% depending on the game.
