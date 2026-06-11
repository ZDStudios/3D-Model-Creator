# 🔶 ShapeForge — 3D Model Maker

A lightweight, browser-based 3D modeller. No install, no account — just open the HTML file and start building. Export straight to your slicer or 3D app when you're done.

---

## Getting Started

1. Open **shapeforge.html** in any modern browser (Chrome, Firefox, Edge, Safari).
2. Click a shape in the left panel to add it to the workplane.
3. Drag it around, resize it in the inspector on the right, change its colour.
4. Export when you're happy — STL and 3MF go straight to most slicers.

That's it. No sign-up required, works fully offline after the first load.

---

## Shapes

Click any shape in the left panel to drop one onto the workplane:

Box · Cylinder · Sphere · Dome · Cone · Pyramid · Wedge · Donut · Tube · Star · Heart · Gem

---

## Moving Things Around

| Action | How |
|---|---|
| Move shape on the plane | Drag it |
| Lift / lower a shape | Ctrl + drag up or down |
| Orbit the camera | Drag empty space |
| Pan the camera | Right-click drag, or Shift + drag |
| Zoom | Scroll wheel |
| Nudge with precision | Arrow keys (X/Z), PgUp / PgDn (height) |

---

## Inspector (right panel)

Select any shape to edit:

- **Name** — rename it anything you like
- **Colour** — 12 presets or pick a custom colour
- **Size** — width, depth, height in your chosen unit
- **Position** — X, Y on the plane, plus lift off the workplane
- **Rotation** — tilt and spin on all three axes
- **Spin 45°** button — quick rotate in Y
- **Drop to plane** — snaps a floating shape back down to Z = 0
- **Duplicate** — copies the shape with a small offset
- **Delete** — removes it (undo brings it back)

---

## Units & Snapping

Both controls sit in the top bar.

**Units:** mm (default) · cm · m · inches · feet — all inspector values update automatically when you switch, and exports are always written in real millimetres so prints come out the right size.

**Snap:** Off · 0.5 mm · 1 mm · 5 mm · 10 mm — shapes and nudge steps align to the grid.

---

## Views

Buttons in the top-right corner of the viewport:

| Button | What it does |
|---|---|
| Iso | Return to the default isometric angle |
| Top | Look straight down |
| Front | Look straight at the front face |
| Fit | Zoom to fit all shapes in view |

---

## Keyboard Shortcuts

| Shortcut | Action |
|---|---|
| R | Spin selected shape 45° |
| D | Drop shape to workplane |
| Delete / Backspace | Delete selected shape |
| Arrow keys | Nudge shape in X / Z |
| PgUp / PgDn | Lift or lower shape |
| Ctrl + D | Duplicate |
| Ctrl + Z | Undo |
| Ctrl + Y | Redo |

---

## Exporting

Click **⬇ Export** in the top-right corner and choose a format:

| Format | Best for |
|---|---|
| **STL** | 3D printers — most slicers (Cura, PrusaSlicer, Bambu, etc.) |
| **3MF** | Modern slicers — preserves more metadata |
| **OBJ** | Blender, Maya, general 3D apps |
| **PLY** | Point cloud / mesh tools |
| **Project file (.json)** | Save and re-open for further editing |

All geometry exports use **millimetres and Z-up**, the convention slicers and CAD tools expect.

---

## Saving & Opening Projects

- **💾 Save** — downloads a `.json` project file with all your shapes, sizes, positions, and colours.
- **📂 Open** — loads a previously saved project file back into ShapeForge.

---

## Tips

- Use **Fit** view after adding several shapes to get your bearings.
- **Ctrl + D** to duplicate a shape, then reposition — faster than adding from scratch.
- Switch to **Top** view when aligning shapes precisely on the X/Z plane.
- A shape can be lifted below zero to fake a recessed slot — just lower it into another shape.
- The **Objects** list on the bottom-left updates as you add shapes — click any row to select it.

---

## Browser Compatibility

Tested in Chrome 120+, Firefox 122+, Edge 120+, Safari 17+. Requires WebGL (enabled by default in all modern browsers). Does not require any server — open directly from your local file system.

---

## Limitations

- No boolean operations (no "hole" carving like Tinkercad) — shapes sit alongside each other but don't subtract.
- No texture or material assignment beyond flat colour.
- Large scenes (200+ shapes) may slow down on older hardware.

---

*Built with Three.js r128. Single HTML file, no build step, no dependencies to install.*
