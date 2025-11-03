# Linking Tools
---
<h4  id="parent" style="display: flex; align-items: center; gap: 10px;">
  <img src="assets/bt-parent.svg" width="50" style="max-width: 50px;" />
  <span>1. Parent Shape Groups to Null</span>
</h4>
<img
  src="assets/gifs/parent.gif"
  alt="Visibility Tools"
  width="100%"
  style="max-width:400px; height:auto; align: center;"
/>
<br>
<br>
This function allows you to parent shape groups to a null, from within any shape layer.<br>
It has triple function:
<br><br>

| Modifier       | Function | Action                       |
| ------------- | :--------: | --------------------------- |
| -      |    Parent Shape Groups to a Null    | <img src="assets/gifs/parent_dialog.jpg" width="100%" style="max-width:600px; height:auto; align: center;"/><br><br>**How to use:**<br>1. Select one or more points in the comp viewer or shape groups in the timeline<br>2. Click the button<br>3. A dialog will appear with a dropdown. Select the Null you want to parent your shape groups to.  |
| OPT/ALT |   Remove Parent from selected     | Removes the parent from the selected shape groups, keeping current position.|
| SHIFT |  Parent 'Parent' Group   | If the selected shape(s) are nested within another group, when holding shift, the function will target the parent group, not the selected shapes. |

```
💡 TIP: Use this function to add details to your character and speed up cleanup by reusing animations from other elements.
```
---
<h4  id="nulls" style="display: flex; align-items: center; gap: 10px;">
  <img src="assets/bt-null.svg" width="50" style="max-width: 50px;" />
  <span>2. Create Nulls to Follow Points</span>
</h4>
<img
  src="assets/gifs/create_nulls.gif"
  alt="Visibility Tools"
  width="100%"
  style="max-width:400px; height:auto; align: center;"
/>
<br><br>
This button has double function:
<br><br>

| Modifier       | Function | Action                       |
| ------------- | :--------: | --------------------------- |
| -      |    Create Nulls to follow selected points   |  Similar to the traditional Create Nulls to Follow Points script, with a few key differences:<br><br>- Create Nulls for selected points only <br>- Nulls are linked to shape groups names (not indices) so you can change the stacking order without breaking the connection.<br>- Each null comes with a Point Index slider, allowing you to reposition it if you edit the path by adding or removing points.<br><br><img src="assets/gifs/pointSlider.jpg" width="100%" style="max-width:400px; height:auto; align: center;"/>|
| OPT/ALT |  Ignore rotation  | Removes the parent from the selected shape groups, keeping current position.|


---

<h4  id="trace" style="display: flex; align-items: center; gap: 10px;">
  <img src="assets/bt-trace.svg" width="50" style="max-width: 50px;" />
  <span>3. Trace Path</span>
</h4>
This button has double function:
<br><br>

| Modifier       | Function | Action                       |
| ------------- | :--------: | --------------------------- |
| -      |    Create Nulls to trace selected paths   |  Similar to the traditional Trace Path script: it creates a Null that moves around the edge of the path. Has a few key differences compared to the original:<br><br>- Nulls are linked to shape group names, so you can change stacking order without breaking connection <br>- Progress is controlled with an Angle Control, not a slider. That means it's easier to control how many times an element moves around the shape.<br><br><img src="assets/gifs/angle_control.jpg" width="100%" style="max-width:400px; height:auto; align: center;"/>|
| OPT/ALT |  Ignore rotation  | Removes the parent from the selected shape groups, keeping current position.|

**Use this to:**
1. Attach other shapes to a path where there's no point and you don't want to create one
2. Have a shape move around another shape

