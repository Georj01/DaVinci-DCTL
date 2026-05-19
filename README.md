# DaVinci Resolve DCTLs

A collection of visual tools and effects programmed in DaVinci Color Transform Language (DCTL). 

This repository follows a strictly minimalist philosophy: lightweight tools, no heavy graphical interfaces, and no external dependencies. Direct mathematical processing on the pixel to guarantee maximum VRAM optimization on modest hardware.

## ⚙️ Installation

The `.dctl` files do not require compilation. Simply copy them to the corresponding DaVinci Resolve folder for your operating system.

**Windows:**
`%APPDATA%\Blackmagic Design\DaVinci Resolve\Support\LUT\`

**Mac:**
`Library/Application Support/Blackmagic Design/DaVinci Resolve/LUT/`

Once copied:
1. Restart DaVinci Resolve.
2. Go to the Color or Edit page.
3. Drag the **DCTL** effect (from the OpenFX effects library) onto your node or clip.
4. In the Inspector, select the corresponding file from the DCTL dropdown menu.

---

## 🛠️ Included Tools

### /Color
*   **`Color_Isolation.dctl`**: Mathematical hue isolation (Sin City effect). Desaturates unselected hues without complex masking.
*   **`Film_Halation.dctl`**: Simulates analog film halation by isolating high-luminance areas and applying a highly optimized spatial blur with a red/orange color bias.
*   **`Gradient_Map_Duotone.dctl`**: Direct pixel-level gradient mapping mapping luminance to a user-defined duotone spectrum.
*   **`Saturation_Curve.dctl`**: Midtone-targeted saturation boosting via sine wave luminance masks to protect shadows and highlights.
*   **`Variable_Pivot_Contrast.dctl`**: Pure contrast adjustment with an explicitly definable pivot point.

### /Utility
*   **`Channel_Splitter.dctl`**: Analytical tool to isolate specific image channels (R, G, B) or pure luminance.
*   **`False_Color.dctl`**: Professional exposure analyzer mapping IRE luminance values to distinct structural color bands.
*   **`Safety_Grids.dctl`**: Compositional overlay tool generating title-safe and action-safe aspect ratio grids.

### /VFX
*   **`Action_Cam_Fisheye.dctl`**: Extreme wide-angle barrel distortion mimicking sports camera optics.
*   **`CMYK_Halftone.dctl`**: Mathematical printing press simulator generating anti-aliased CMYK dot matrices through UV coordinate rotation.
*   **`CRT_Emulation.dctl`**: Single-pass CRT monitor emulator featuring barrel geometry, chromatic aberration, and scanlines.
*   **`Radial_Chromatic_Aberration.dctl`**: Spatial RGB channel separation driven exponentially by the distance from the frame center.
*   **`Sobel_Edge_Neon.dctl`**: High-performance spatial edge detection utilizing an optimized 3x3 Sobel matrix with neon color mapping.
*   **`Visual_Bitcrusher.dctl`**: Retro digital degradation effect applying heavy color quantization and pixel-block decimation.

---

## 📄 License
This project is licensed under the MIT License. Use it, modify it, and break it as you wish.