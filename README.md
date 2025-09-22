# What grace Is

🔮 grace (stylized as lowercase) is a small generic [OpenColorIO](https://opencolorio.org/) config for rendering, photography, and other stuff involving color management or tone mapping.

🧪 grace is a personalized combination of several OCIO configs and view transforms:
- [Troy Sobotka's new AgX](https://github.com/sobotka/SB2383-Configuration-Generation)
- [Eary Chow's version of AgX](https://github.com/EaryChow/AgX/releases/tag/v11.9)
- [flim](https://github.com/bean-mhm/flim)

⚠️ grace is not a professional config, nor am I a professional!

# What grace Contains

### 🌀 Color Spaces
- **XYZ Spaces**. Example: `Linear CIE-XYZ I-E`
- **Linear Spaces**. Examples: `Linear BT.709 I-D65`, `Linear DCI-P3 I-D65`.
- **Display Formats**. Examples: `sRGB 2.2`, `Display P3 2.2`.

### 🎞️ View Transforms
- [**flim**](https://github.com/bean-mhm/flim)
- [**AgX**](https://github.com/sobotka/SB2383-Configuration-Generation)

### 🧫 Working Space
- As of now, grace uses `Linear BT.2020 I-E` as its working space (the `scene_linear` role).
- Be careful not to directly copy and use RGB triplets that are intended to work in Rec.709 when the working space is BT.2020.
- You can switch to `Linear BT.709 I-D65` (or anything else) as the working space by modifying the `scene_linear` space in `roles`.

# Where to find grace
- 🔗 https://github.com/bean-mhm/grace

# How to use grace

Make sure your DCC (Digital Content Creation) software supports [OpenColorIO](https://opencolorio.org/) for color management
and look up how you can switch the OCIO config. In [Blender](https://www.blender.org/), for example, you can swap the contents of the `colormanagement` folder with the contents of the config you want to use, after making a backup of Blender's default config.

> `[Blender Installation Path]/X.X/datafiles/colormanagement`
