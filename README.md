# BitNixelet Shader Pack

## ⚠️ BETA VERSION ⚠️
**Hey! This shader is still in development, so there might be bugs and weird stuff. If something breaks - don't panic, that's normal for beta :)**

## What is this?

Basically, I'm making a shader that turns Minecraft into an old-school pixel game from the 90s. You know, like on old consoles - everything square and with huge pixels? Something like that.

*For now only pixelation works, I'll add the rest later*

## What it does

### 🎮 Makes everything pixelated
- You can adjust how much to "pixelate" (from 1 to 100)
- I set 32 by default - looks pretty good
- Works simply: takes a bunch of pixels, mixes them into one big one making an 8-bit game analog

### 🎨 Old colors
- Cuts the palette down to 16 shades per color (like in old games)
- Creates those "steps" between colors
- Just like on ancient computers

### ✨ Tweaks the picture
- Slightly changes brightness so it's not too dark
- Makes colors 20% brighter
- Generally tries to make it look good

### 📺 TV Noise (optional)
- Adds old CRT TV static noise effect
- Animated grain that moves over time
- Can be turned on/off in shader settings
- Makes it feel like playing on an old television

## How to configure

### Main settings
- `PIXELATION` - how much to pixelate (1-100)
  - 1 = almost no pixelation (very fine)
  - 100 = strong pixelation (big squares)
- `NOISE` - TV static effect (0/1)
  - 0 = no noise
  - 1 = old TV static noise

### How it works inside
1. Takes the picture and "rounds" pixels into blocks
2. Cuts the number of colors to 16 per channel
3. Adjusts brightness and saturation so it doesn't look ugly

## What it runs on

- Need Iris (won't work without it)
- Minecraft 1.16+ (haven't tested on older versions, might not work), recommend playing on 1.20.1
- Doesn't lag even on weak computers
- OpenGL 2.1 is enough (that's a very old standard)

## How to install

1. Download and install Iris if you don't have it yet
2. Drop the `BitNixelet` folder into the `shaderpacks` folder
3. In Iris settings select this shader
4. Adjust the pixelation setting as you like

## What's currently buggy

- Sometimes artifacts appear if you pixelate too much
- Some blocks might look weird
- Interface gets blurry with strong pixelation (don't know how to fix this yet)

## Fixed bugs

- Fixed wrong pixelation math that caused weird scaling
- Fixed edge artifacts by preventing texture sampling outside bounds
- Fixed pixel centering for cleaner pixelation blocks
- Fixed potential crashes from division by zero in color calculations
- Fixed color overflow issues with proper clamping
- Fixed inverted pixelation logic (now higher values = more pixelation)
- Fixed NOISE setting not working properly with true/false values
- Optimized luminance calculations for better performance

---

*Made for those who miss pixel games from childhood*
