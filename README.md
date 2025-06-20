**A collection of work-in-progress 720x720 overlays for the RG CubeXX and other devices. Tested on muOS Pixie.**

I normally wouldn't upload anything that wasn't finished; however, I likely won't be completing these any time soon so I thought I would make them available in case anyone wants to use them. I'll update with additional and/or revised overlays as time and interest permit.

*Note: I don't plan to upload anything that I wouldn't use myself, but be aware that there are a number of issues that still need to be resolved (mostly interactions between shadows and gridlines that need to be adjusted manually, but others as well). I'll label final versions as such if and when I upload them.*

# Contents
1. [Game Boy](https://github.com/mugwomp93/720x720_overlays/edit/main/README.md#game-boy)
2. [Game Boy Color](https://github.com/mugwomp93/720x720_overlays/edit/main/README.md#game-boy-color)
3. [Game Gear](https://github.com/mugwomp93/720x720_overlays/edit/main/README.md#game-gear)
4. [1playerinsertcoin Assorted Overlays](https://github.com/mugwomp93/720x720_overlays/edit/main/README.md#1playerinsertcoin-assorted-overlays)

## Game Boy
These overlays work with a shader preset to create custom palettes and a subtle pixel shadow effect. The shader preset is a combination of the [sharp-shimmerless interpolation shader](https://github.com/Woohyun-Kang/Sharp-Shimmerless-Shader) and gb-pass4 from Gameboy Shader 0.2.2. I've bundled copies of these shaders up in their own folder, both to keep everything tidy and because I modified the gb-pass4 palette files, but any credit should go to their original creators.

I'm also working on a DMG version, but it's more complex and I'm not as far along in tuning it.<br><br> 
![GB](https://github.com/user-attachments/assets/7cf4faa7-3e26-461c-8e1a-da672c1103dc)
*Note: The apparent evenness of the gridlines in these images is heavily affected by scaling, display size, and resolution.*

Notes:
- The colors aren't intended to be 100% true to the original devices. Consider them "inspired by" instead of accurate representations.  
- Pixellate and pixel_aa produce slightly better interpolation results than sharp-shimmerless, but they're more resource intensive and can produce lag and audio issues in more demanding games on the CubeXX (e.g., Donkey Kong Land) so I've stuck with sharp-shimmerless.
- You may notice that some of the pixel shadows are bisected by the grid lines. I don't really notice this on device (it's much more apparent in the screenshots), but if it bothers you, you can adjust Shadow Offset Vert in the shader parameters to +4.50. This will position the shadows at a full 1 game pixel offset, 45 degrees down and left of their respective pixels.
- I suggest leaving Shadow Offset Horiz at 4.50 as the preset value adds a shadow on the right edge of the screen that the overlays are design to complement. They may look weird if you reduce the horizontal shadow or change the direction. Similarly, the edge shadows on the overlay may look strange if used without the shader preset.

## Game Boy Color
1playerinsertcoin was kind enough to create a number of iterations of this overlay grid. I think the final version looks great, which is especially impressive considering they don't have a 720x720 device. I'm not 100% happy with the edge shadow so I may revisit it at some point, but otherwise this is as close to finished as any of these overlays.

![GBC](https://github.com/user-attachments/assets/880701cc-ed7e-4917-a938-50da715529c5)

Notes:
- A version of this overlay without border graphics and shadows is available in the [1playerinsertcoin assorted overlays bundle](https://github.com/mugwomp93/720x720_overlays/edit/main/README.md#1playerinsertcoin-assorted-overlays). A 4x integer version is also available.

## Game Gear
Another 1playerinsertcoin grid. This one doesn't specifically emulate the Game Gear screen (it's also not 4:3, so we've already deviated from reality) but it includes some really nice enhanced LCD subpixel effects.

![GG](https://github.com/user-attachments/assets/092f76a3-0859-4c02-8eac-46aeae164139)

Notes:
- A version of this overlay without border graphics and shadows is available in the [1playerinsertcoin assorted overlays bundle](https://github.com/mugwomp93/720x720_overlays/edit/main/README.md#1playerinsertcoin-assorted-overlays). A 4:3 version (no more skinny Sonic) is also available.

## 1playerinsertcoin Assorted Overlays
As you may have noticed from the descriptions above, 1playerinsertcoin has been very generous with their time in creating overlays for a device they don't even own. Given how long it takes to create high quality overlays, limited free time, etc, I thought it would be unfair to keep these to myself until I was done creating my versions. These overlays don't have any border decorations, shadows, etc, and, unlike my versions, should all be centered. Please credit 1playerinsertcoin if you use these to create your own versions.

Overlays include:
- GBA 3x integer
- GBC 4x integer
- GBC non-integer (720x648) 
- GG non-integer (720x648; square pixels)
- GG non-integer 4:3 (720x540; rectangular pixels)
- NGPC 4x integer
- NGPC non-integer (720x684)
- PICO-8 non-integer (720x720)

