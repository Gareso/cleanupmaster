
## Changelog

---

### v1.2.6 - June 2026

<h3 style="color:#e94934">IMPROVED</h3>

<strong>:: ISOLATE MASKS ::</strong>

- Isolated masks are now locked with expressions, making them distinct from regular masks..

<strong>:: TWEAK PATHS ::</strong>

- Overall logic updated with improved results.
- Collapsed vertices in the baseline stay collapsed across the entire animation.
- Separate shapes now automatically follow their parent shape's deformation, and joint connection points stay welded across keyframes.

<strong>:: ALIGN & COLLAPSE POINTS ::</strong>

- Undo history is now clean: one step per operation, no invisible intermediate steps.

---

### v1.2.5 - May 2026

<h3 style="color:#e94934">ADDED</h3>

<strong>:: SOLO SELECTED SHAPES ::</strong>

- New modifier: OPT/ALT + SHIFT selects all points in the parent shape group of the current selection. If the selection is at root level (no parent group), selects all points in the entire layer.

<strong>:: CREATE CLIPPING MASKS ::</strong>

- New mode dropdown: choose the Merge Paths blend mode before applying (Merge, Add, Subtract, Intersect, Exclude Intersections). Defaults to Intersect.
- New Include strokes option: adds an Offset Paths modifier to the mask group, with the offset linked to the stroke widths of both shapes. Inside − (default) offsets inward; Outside + offsets outward. The offset respects stroke visibility dynamically.

<strong>:: CREATE MASKS FROM PATHS ::</strong>

- A dialog now always opens (no modifier needed) with all options in one place:
  - **Target layer** dropdown: choose **New shape layer** to create a dedicated mask layer above the source, or pick any existing layer to apply masks directly to it.
  - **Subtract**: applies masks in Subtract mode.
  - **Include strokes** + **Inside −** / **Outside +**: sets Mask Expansion linked to the shape's stroke width. Expansion is expression-driven and respects stroke visibility dynamically.
  - All choices persist between sessions.

<h3 style="color:#e94934">CHANGED</h3>

<strong>:: COPY / PASTE SHAPE STATES ::</strong>

- Paste modifier changed from OPT/ALT to CMD/CTRL (and SHIFT + OPT/ALT to SHIFT + CMD/CTRL). OPT/ALT is now consistently used for delete/remove across all buttons.

<h3 style="color:#e94934">FIXED</h3>

<strong>:: ADD KEYFRAMES ::</strong>

- Now correctly adds keyframes across all selected shape layers simultaneously (previously only affected the first selected layer).

<strong>:: RENAME ::</strong>

- Updates to the renamer engine to prevent expression breaking in some situations.

---

### v1.2.3 - May 2026

<h3 style="color:#e94934">ADDED</h3>

<strong>:: MASK SUPPORT ::</strong>

The following tools now work on mask paths, in addition to shape layer paths:

- **Visibility Tools** (Solo, Hide Selected, Restore Visibility): solo/hide now includes selected mask paths
- **Copy / Paste Shape State**: copies and pastes mask path shapes
- **Align Points (Collapse Points)**: works on selected mask points
- **Tweak Path**: registers and applies delta to mask points
- **Isolate Selection**: locks/unlocks unselected mask paths; selecting only mask paths will also lock all shape paths, and vice versa
- **Create Nulls to Follow Points**: creates nulls linked to mask path vertices
- **Trace Path**: creates a null that travels around a mask path
- **Renamer**: renames mask paths and updates `.mask("name")` references in expressions; also updates layer names that reference the mask

> Mask support respects the **Affect Masks** setting (see Settings below).

<strong>:: SETTINGS: "AFFECT MASKS" TOGGLE ::</strong>

A new **Tool-wide options** section appears at the top of the Settings dialog. It contains a single checkbox:

☑ **Affect Masks**: when enabled, all buttons that support masks will also work on mask paths. Uncheck to revert all tools to shape-only behavior.

<strong>:: SHADE GROUP: NEW MODIFIERS ::</strong>

The Create Shade Group button now has three modifier behaviors:

| Modifier | Behavior |
| -------- | -------- |
| CMD/CTRL | Creates the shade group and hides the selected original shapes (eye off). The clone's opacity dynamically references the original's opacity; keyframes and static values are respected live. |
| SHIFT | Toggles the hidden originals visible/hidden for editing. Use this when you need to access the original shapes. |
| OPT/ALT on shade group layer | Deletes the shade group and restores all hidden originals on the source layer. |
| OPT/ALT on source layer | Restores only the selected hidden groups on that layer. |

<h3 style="color:#e94934">CHANGED</h3>

<strong>:: ISOLATE SELECTION ::</strong>

- Paths locked by Isolate Selection are now also immune to **Free Transform** (the double-click transform operation in the comp viewer). Previously the lock could be bypassed this way.

<h3 style="color:#e94934">FIXED</h3>

<strong>:: ISOLATE SELECTION ::</strong>

- Selecting only one mask path (with more shapes present): now correctly locks the shapes.
- Selecting one mask path out of several alongside shape paths: now locks both the other mask paths and all shape paths.

---

### v1.2.2 - Apr 2026

<h3 style="color:#e94934">CHANGED</h3>

<strong>:: ISOLATE SELECTION ::</strong>

- Releasing isolation now unlocks locked paths across **every layer in the comp**, not just the active one. Ensures no stale locks are left behind after switching layers.
- Auto-release on layer switch has been removed. Click the button explicitly to release isolation.

<strong>:: ADD KEYFRAMES ::</strong>

- Default behavior flipped: now adds a keyframe to **selected paths only**. If no path is selected, adds to all paths in the layer.

<h3 style="color:#e94934">FIXED</h3>

<strong>:: ISOLATE SELECTION ::</strong>

- Added guard for unactionable selections: if the layer has only one path, or all paths are selected, the button now shows a clear message instead of locking nothing silently.

<strong>:: GENERAL ::</strong>

- Fixed "Cannot run a script while a modal dialog is waiting for response" errors. Button states (Tweak Path, Isolate Selection) now sync on mouseover instead of background polling.

---

### v1.2.1 - Apr 2026

<h3 style="color:#e94934">CHANGED</h3>

- Updated licensing framework.

---

### v1.2.0 - Mar 2026

<h3 style="color:#e94934">ADDED</h3>

<strong>:: ISOLATE SELECTION ::</strong>

- New tool. Select the paths you want to keep editable and click to lock everything else in the layer. Click again to release all locks.
- SHIFT + selection: Add paths to the current isolated set.
- OPT/ALT + selection: Remove paths from the isolated set.
- SHIFT (nothing selected): Restore the previous isolated selection.

<strong>:: TWEAK PATH ::</strong>

- New tool. Make a shape correction on a single frame and apply that same delta to all keyframes within the work area.
- Hold SHIFT on apply to keep the baseline active for further tweaks.
- Hold OPT/ALT to clear the baseline without applying.

<strong>:: COPY / PASTE SHAPE STATES - COPY / PASTE SELECTED POINTS TO WORK AREA ::</strong>

- Hold SHIFT to copy selected points only (partial copy).
- Hold SHIFT + OPT/ALT to paste those points to every keyframe within the work area.

<strong>:: COLLAPSE POINTS - COLLAPSE TO LINE ::</strong>

- Hold SHIFT to collapse selected points to a line. Direction is detected automatically based on the spread of the selection.

<strong>:: SETTINGS PANEL ::</strong>

- Click the gear icon at the bottom of the panel to open the Settings dialog.
- Choose which features are visible in the panel. Rows are hidden automatically when all their buttons are turned off.

---

### v1.1.3 - Sep 2025

<h3 style="color:#e94934">FIXED</h3>

- Fixed issues where some functions were not working on WINDOWS PCs.
- Renamer now ignores inverted opacity pairs.

---
### v1.1.2 - Sep 2025

<h3 style="color:#e94934">ADDED</h3>

<strong>:: STROKE TO SHAPES ::</strong>

- Added checkbox to hide converted shapes for easier editing.

<strong>:: COLLAPSE POINTS ::</strong>

- Collapsing points in parented shape groups is now supported.

<strong>:: PARENT SHAPE GROUP TO NULLS ::</strong>

- Hold SHIFT to parent Groups



<h3 style="color:#e94934">CHANGED</h3>

<strong>:: MASKS FROM PATHS ::</strong>

- Open paths now create closed Masks by default.
- Masks can now be created from parented shape groups.
- Created Shape Layers with masks now have the same in/out points and is created on top of the original layer.

<strong>:: SOLO OPT/ALT ::</strong>

- Select all points now respects current visibility.

<strong>:: CREATE NULLS TO FOLLOW POINTS :: </strong>

- Created Nulls now have the same in/out points of the original Shape Layer



<h3 style="color:#e94934">FIXED</h3>

<strong>:: CLIPPING MASKS ::</strong>

- Slider values are not reset after converting a new stroke to shape.
- Converted Strokes to Shapes, now parent to nulls properly
- More robust inverted opacity deletion (holding alt/opt)
- Nested groups now work with parented shape groups

<strong>:: ADD KEYFRAMES ::</strong>

- Now it skips masks and any path with expressions.

<strong>:: DELETE POINTS ::</strong>

- Now ignores "inverted opacity" pairs in the selection.

<strong>:: STACKING :: </strong>

- Fixed opacity not inverting when no non-zero keyframes were available
- Group toggle fixed

<strong>:: PARENT SHAPE GROUP TO NULLS ::</strong>

- More robust remove Parent (holding alt/opt)



---

### v1.1.1 - Aug 2025

#### Bug Fixes:
<strong>:: CLIPPING MASKS ::</strong>

- Fixed issue where stroke to shape broke at 1st point with different bezier angles.

---
### v1.1.0 - Aug 2025

#### New features:
<strong>:: CLIPPING MASKS ::</strong>

- Use other shapes in the same layer as clipping masks with merge paths – even fewer layers needed.
- Hold CMD/CTRL to convert strokes to fills, so strokes are cut as well.
<br><br>

<strong>:: PARENT GROUPS with SHIFT ::</strong>

[Stacking]
- Hold SHIFT + Invert Opacity → apply to parent groups.
- SHIFT + OPT/ALT → delete parent group pairs.
- SHIFT + CMD/CTRL → zero out opacity of parent groups.

[Renamer]
- Hold SHIFT to rename parent groups.

[Shade Groups]
- Shade groups now fully respects parent groups and inverted opacity pairs.
<br><br>

<strong>:: CREATE MASKS FROM PATHS → ADD MASKS TO LAYER ::</strong>

-  OPT/ALT now adds masks directly to the layer, with choice of Add or Subtract mode.
-  Target layer can be moved, rotated, or scaled while keeping the mask perfectly aligned.

---
### v1.0.1 - Jul 2025

#### New features:
- Hold OPT/ALT and press the Solo Button to select all points in the selected paths instantly.
- Hold CMD/CTRL and press the Renamer Button to nest selected paths into a new group (and name the group)
<br>

#### Bug Fixes:
- Fixed issue with nested groups and inverted opacity
- CMD/CTRL option on Invert Opacity now reverts back to the original value when clicking more than once

---

### v1.0 - Jul 2025

* Initial release with full suite of cleanup and shape layer tools.