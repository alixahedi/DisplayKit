<div align="center">

<!-- Badges -->

<a href="https://github.com/cifertech/DisplayKit" title="Go to GitHub repo"><img src="https://img.shields.io/static/v1?label=cifertech&message=DisplayKit&color=cyan&logo=github" alt="cifertech - DisplayKit"></a>
![GitHub Downloads (all assets, all releases)](https://img.shields.io/github/downloads/cifertech/DisplayKit/total)
<a href="https://github.com/cifertech/DisplayKit"><img src="https://img.shields.io/github/stars/cifertech/DisplayKit?style=social" alt="stars - DisplayKit"></a>
<a href="https://github.com/cifertech/DisplayKit"><img src="https://img.shields.io/github/forks/cifertech/DisplayKit?style=social" alt="forks - DisplayKit"></a>
   
<h4>
    <a href="https://twitter.com/techcifer">TWITTER</a>
  <span> · </span>
    <a href="https://www.instagram.com/cifertech/">INSTAGRAM</a>
  <span> · </span>
    <a href="https://www.youtube.com/c/techcifer">YOUTUBE</a>
  <span> · </span>
    <a href="https://cifertech.net/">WEBSITE</a>
  </h4>
</div> 
 
<br />

# 🎨 DisplayKit

**DisplayKit** is a modern web-based drag-and-drop UI designer for embedded display development.

Design screens visually → generate clean **Arduino** drawing code → run it on boards like **ESP32 / ESP8266 / STM32 / Arduino / RP2040** (and more).

## Quick start (recommended)

- **Use it online (recommended)**: click the GitHub Pages link in the repository, or open: `https://cifertech.github.io/DisplayKit/`


## How to use

- **Pick display driver**: choose **TFT_eSPI** or **U8g2 OLED** from the sidebar (and set your display resolution)
- **Create screens**: add as many as you like and name the generated function (e.g. `drawHomeScreen`)
- **Add elements**: click an element type to add it, then drag / resize and edit properties
- **Export**:
  - **Copy** the generated code from “Generated Code (TFT_eSPI / U8g2)”
  - **Export JSON** to save a project snapshot (great for versioning)
  - **Import JSON** to restore a saved project

## Built-in tools

DisplayKit includes tool pages under `tools/` and can open them inside the app overlay:

- **PixelForge** (`tools/pixelforge/`): image converter (generate RGB565 headers and import into DisplayKit)
- **BitCanvas Studio** (`tools/bitcanvas-studio/`): animation tool (export and copy to clipboard)
- **Shared tool theming**: `tools/theme.css` keeps tool pages visually consistent with DisplayKit

## Keyboard shortcuts

- **Undo / Redo**: `Ctrl/Cmd + Z` / `Ctrl/Cmd + Shift + Z`
- **Duplicate**: `Ctrl/Cmd + D`
- **Cycle selection**: `Tab` / `Shift + Tab`
- **Align selected**: `Ctrl/Cmd + 1..6` (left / center / right / top / middle / bottom)
- **Move selected**: Arrow keys (hold **Shift** for bigger steps)
- **Delete selected**: `Delete` / `Backspace`
- **Close Tools overlay**: `Esc`

## 🚀 Features

### 🖥 Multi-Screen UI Builder
- Create unlimited screens (Home, Settings, About…)
- Auto-generates `drawScreenName()` functions
- Visual screen switching system

### 🧱 Drag-and-Drop Elements
- Rect, RoundRect, Circle
- Labels, Buttons, Headers
- Cards, Dividers
- Progress Bars, Sliders, Toggles
- Images (PNG/JPG → RGB565 or monochrome)

### 🖼 Image Engine
- Upload PNG/JPG
- Auto-converts to **RGB565** for TFT_eSPI
- Auto-converts to **monochrome bitmap** for U8g2
- Stores as PROGMEM arrays
- Real preview inside editor

### 🔠 Full Font Support
#### TFT_eSPI
- Text size control
- Text color, stroke, fill

#### U8g2
- Complete font selector (hundreds of fonts)
- Auto-generates correct `u8g2.setFont()` code

### 🧰 Editor Tools
- Undo / Redo
- Duplicate element
- Align (Left, Right, Center, Top…)
- Snap-to-grid
- Zoom 50–200%
- JSON project import/export

### ⚙ Code Output
#### TFT_eSPI Mode:
- `fillRect`, `drawRoundRect`, `drawString`
- `pushImage()` for bitmaps
- Optional **TFT_eSprite** rendering

#### U8g2 Mode:
- `drawBox`, `drawRBox`, `drawDisc`
- Monochrome bitmaps
- Full font rendering

### 🔌 Actions & Navigation
- Buttons can “Go to Screen”
- Generates logic-ready comments for touch input

&nbsp;

## 🛠 Compatibility

| Display Library | Status | Notes |
|-----------------|--------|-------|
| **TFT_eSPI**    | ✅ Full | RGB565, sprites, images, colors |
| **U8g2**        | ✅ Full | Monochrome + full font system |
| **Adafruit_GFX** | ⚠ Planned | Not implemented yet |

## Project structure

```text
.
├─ index.html        # Main app UI
├─ style.css         # Main app styling
├─ app.js            # App logic (editor + code generation)
└─ tools/
   ├─ pixelforge/       # Image converter tool
   ├─ bitcanvas-studio/ # Animation tool
   └─ theme.css         # Shared theme tokens for tool pages
```

## License

See `LICENSE`.

&nbsp;

## 🤝 Contribute

Want to help make DisplayKit better?

- Submit bug reports  
- Suggest new features  
- Improve documentation  
- Contribute code or UI elements  
- Star ⭐ and share the project  

Every contribution helps. Thank you! ❤️


