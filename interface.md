# Interface

<img
  src="assets/UI.svg"
  alt="Cleanup Master UI"
  width="1000"
  style="max-width:100%; height:auto; align: center;"
/>

---

## Settings

<img
  src="assets/settings_updated_2.png"
  alt="Settings Panel"
  width="100%"
  style="max-width:400px; height:auto; align: center;"
/>

<br>

Click the **gear icon** at the bottom of the panel to open the Settings window. It's a floating window, so you can keep it open while you work; click the gear again to bring it to the front.

### Tool-wide Options

At the top of the Settings dialog, a **Tool-wide options** section contains global behavior toggles:

| Option | Description |
| ------ | ----------- |
| ☑ **Affect Masks** | When enabled, all buttons that support masks will also work on mask paths. Uncheck to revert all tools to shape-only behavior. |

### Control Nulls

Sets up the Nulls the linking tools create, in two side-by-side sections so you can tell them apart: **Points Follow Nulls** on the left, **Nulls Follow Points / Trace** on the right. Each has the same options. Changes apply to new Nulls and to the existing ones in the active comp.

| Option | Description |
| ------ | ----------- |
| **Null Layers / Shape Layers** | **Shape Layers** (default): small guide shape layers. No Solids in the project, even outlines at any scale, and a line from each handle Null to its point.<br>**Null Layers**: real Null layers, all sharing one Solid per kind.<br>Switching only affects new Nulls. Either way, the **Hide Nulls** checkbox in the Linking panel hides them. |
| **Size (px)** | Size of the Nulls. Handle Nulls are 40% of it. With Null Layers, this resizes every control Null of that kind in the project. |
| **Stroke width** | Outline thickness (Shape Layers only). |
| **Color** (Point / Handle color for Points Follow Nulls) | Click a swatch to pick a color. With Null Layers, the Null uses the closest of your After Effects label colors. |

### Feature Visibility

From the Settings dialog you can also choose which features are visible in the panel. Unchecking a feature hides its button entirely, freeing up space and keeping the toolbar focused on what you actually use.

Features are grouped by section:

| Section | Features |
| ------- | -------- |
| **Main Panels** | Visibility Tools, Linking Tools |
| **Other Tools - Row 1** | Onion Skin, Isolate Selection, Rename / Group, Inverted Opacity, Copy / Paste Path, Tweak Path, Align Points |
| **Other Tools - Row 2** | Add Keyframes, Delete Points, Masks, Clipping Mask, Shade Group, Zero Transforms, Remove Expressions |

Rows are hidden automatically when all their buttons are turned off. Click **Reset Defaults** to turn everything back on and restore the default Control Nulls.

