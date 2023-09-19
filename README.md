# generate_image.py

Generates challenge-related images for the Glyphs and Alphabets discord server. Assumes a Linux environment, and invokes `pdftoppm`, `convert` (part of `imagemagick`), `lualatex` and `fc-match` (for local font information). 

All images should be stored in a folder named `Images`. For quick testing, copy `sample_images` to `Images`. The usage examples below use the sample images. The format of this directory is as follows:

* Glyph submissions should have the filenames `Glyph_1`, `Glyph_2`, etc (with any image file extension).
* Ambigram submissions are likewise `Ambi_1`, `Ambi_2`, etc.
* User profile pictures should have filenames matching the user's names and should be stored in a subdirectory `Images/pfp`. Note that LaTeX doesn't like the characters `&%$#{}~^\` in filenames, so these should simply be removed from usernames.
* The winning submissions should be copied to files named `GlyphWinnerFirst`, `GlyphWinnerSecond`, `GlyphWinnerThird` for the glyph challenge, and likewise `AmbiWinnerFirst`, `AmbiWinnerSecond`, `AmbiWinnerThird` for the ambigram challenge. 


## Example Usage
```
>>> generate_image.py glyph_announcement 🐱
```
Date and background colour (which is on a weekly cycle) are automatically determined. For this example character, the font `Twemoji Mozilla` is automatically selected and will be used so long as it is present on the system.
<div align=center><img src="https://github.com/sungodmoth/generate_image/assets/128005279/cbc64190-32ca-4b1c-940d-b26d79210a89" width="600"/></div>

```
>>> generate_image.py glyph_poll 🐱
```
Glyph submissions are pulled from the `Images` directory as above. 
<div align=center><img src="https://github.com/sungodmoth/generate_image/assets/128005279/cfbc01c4-ffac-46bf-b0f3-b6369d6e3360" width="600"/></div>

<!---
![glyph_poll](https://github.com/sungodmoth/generate_image/assets/128005279/cfbc01c4-ffac-46bf-b0f3-b6369d6e3360)
![glyph_first](https://github.com/sungodmoth/generate_image/assets/128005279/808ddae7-d250-4bca-acd3-7ce6d2d28630)
![glyph_second](https://github.com/sungodmoth/generate_image/assets/128005279/9d66f9e9-7ee2-4bda-b305-e7c6267bffce)
![glyph_third](https://github.com/sungodmoth/generate_image/assets/128005279/1050f16d-1fde-4d0a-aa2a-2fadaaf52216)
![glyph_suggestions](https://github.com/sungodmoth/generate_image/assets/128005279/f9f62a26-f608-4e8b-906e-d656f28cf759)
--->
