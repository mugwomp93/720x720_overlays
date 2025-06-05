A collection of work-in-progress 720x720 overlays for the RG CubeXX and other devices. Tested on muOS Pixie.

I normally wouldn't upload anything that wasn't finished, but I likely won't be completing these any time soon so I thought I would make them available in case anyone wants to use them. I haven't seen many options for 720x720 overlays, especially non-integer scale overlays, so I thought more might be appreciated. *This isn't a commentary on other people's work - the overlays I have seen are high quality (in most cases higher quality than mine); there just aren't many of them.*

I'll update with additional and/or revised overlays as time and interest permit. I don't plan to upload anything that I wouldn't use myself, but be aware that there are a number of issues that still need to be resolved (mostly interactions between shadows and grids, but others as well). I'll label final versions as such if and when I upload them.

## Game Boy
These overlays work in tandem with a shader preset to create custom palettes and a subtle pixel shadow effect. The shader preset is a combination of the [sharp-shimmerless interpolation shader](https://github.com/Woohyun-Kang/Sharp-Shimmerless-Shader) and gb-pass4 from Gameboy Shader 0.2.2. I've bundled copies of these shaders up in their own folder to keep everything tidy and because I modified the gb-pass4 palette files, but credit for these shaders should go to their original creators. Note that I'm also working on a DMG version, but it's more complex (it uses a custom palette file) and the manual tuning isn't quite as far along yet.<br><br> 
![GB](https://github.com/user-attachments/assets/798751c6-59b0-4263-8d64-3cc3910cdcc3)

Notes:
- The colors aren't intended to be 100% true to the original devices. Consider them "inspired by" instead of accurate representations.  
- Pixellate and pixel_aa produce slightly better interpolation results than sharp-shimmerless, but they're more resource intensive and can produce lag and audio issues in more demanding games on the CubeXX (e.g., Donkey Kong Land) so I've stuck with sharp-shimmerless.
- You may notice that the overlay grid doesn't quite blend in with the background color in the example pictures. This was a deliberate choice as I find it introduces some subtle texture that's not consciously noticeable when playing (it's not as pronounced on the device as it is in the screenshots). You can adjust the shader parameters (Contrast, Ambient Screen Light, Shadow Opacity) to fully blend the overlay with the background if desired.
- You may also notice that some of the pixel shadows are bisected by the grid lines. I don't really notice this in practice (again, it's much more apparent in the screenshots), but if it bothers you, you can adjust Shadow Offset Vert in the shader parameters to +4.50. This will position the shadows at a full 1 game pixel offset, 45 degrees down and left of their respective pixels.
- I suggest leaving Shadow Offset Horiz at 4.50 as the preset value adds a shadow on the right edge of the screen that the overlays are design to complement. They may look weird if you reduce the horizontal shadow or change the direction. Similarly, the edge shadows on the overlay may look strange if used without the shader preset.
- That said, you may sometimes notice bright bands at the edges of text boxes and other large, linear features. If these bother you, you can try adjusting the shader parameters to change the shadow position or reduce the shadow opacity. I'm still working on optimizing the shader parameter settings to reduce these types of artifacts.

## Game Boy Color
![GBC](https://github.com/user-attachments/assets/880701cc-ed7e-4917-a938-50da715529c5)

## Sega Game Gear
![GG](https://github.com/user-attachments/assets/092f76a3-0859-4c02-8eac-46aeae164139)

## Neo Geo Pocket Color
![NGPC](https://github.com/user-attachments/assets/e7a4704b-a2f8-406e-80b8-43b5302c500c)

## PICO-8
![PICO_100](https://github.com/user-attachments/assets/b1ca6ccd-bc3d-493f-b66e-56e6539c4d89)
![PICO_70](https://github.com/user-attachments/assets/5e01e7d4-ca2a-4a39-bb14-0a799299c2ae)
![PICO_55](https://github.com/user-attachments/assets/95c3d45c-9a4d-4274-9a36-e1a4f2f9a499)

## 1playerinsertcoin Blank Pack
As you may have noticed from the descriptions above, 1playerinsertcoin has been very generous with their time in creating overlays for a device they don't even own. Given how long it takes to create high quality overlays, limited free time, etc, I thought it would be unfair to keep these to myself until I was done creating my versions. I'm providing the bare overlays (no border decorations, shadows, etc) in a single zip file without instructions, but the individual overlays have descriptive names and, unlike my versions, should all be centered. If you use these to create your own versions, please credit 1playerinsertcoin if you decide to share them.

Overlays in the bundle include:
- GBC 4x integer
- GBC non-integer (720x648)
- GBA 3x integer
- GG 4x integer (720x648; square pixels)
- GG 4:3
- NGPC 4x integer
- NGPC non-integer (720x684)
- PICO-8 non-integer (720x720)

