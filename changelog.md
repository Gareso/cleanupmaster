
## Changelog

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