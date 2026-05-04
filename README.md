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

### /VFX: `CRT_Emulation.dctl`
Cathode Ray Tube (CRT) monitor emulator. Processed in a single pass without heavy spatial loops, optimized to avoid overloading the GPU.
*   **Distortion Curve:** Spherical barrel geometry.
*   **Chromatic Aberration:** Red and Blue channel phase offset at the edges.
*   **Scanlines:** LFO applied to the Y-axis with adjustable frequency and depth.

### /Color: `Saturation_Curve.dctl`
Advanced saturation control based on pure luminance isolation. Outperforms the standard program saturation slider.
*   **Saturation Boost:** Chroma increase or decrease (using standard Rec.709 weights).
*   **Protect Shadows/Highlights:** Uses a sine wave over the luminance to apply the effect only to midtones, protecting blacks from color noise and whites from clipping.

### /Utility: `Channel_Splitter.dctl`
Analytical tool to isolate specific image channels using a native dropdown menu.
*   Allows you to quickly view the Red, Green, or Blue channels (ideal for detecting digital camera noise) or pure luminance in grayscale.

---

## 📄 License
This project is licensed under the MIT License. Use it, modify it, and break it as you wish.