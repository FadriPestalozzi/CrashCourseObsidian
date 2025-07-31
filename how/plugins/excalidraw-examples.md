Excalidraw is an amazingly flexible drawing tool 💖
I'm a big fan of its flexibility and intuitive user experience. 
The examples below illustrate different drawing features in action. 

# create drawing elements 

to quickly create elements, 
- either type the associated number
  <img src="../../pics/excalidraw-create-element-by-number.png" width="300">
- or the assigned letter (e.g. R for Rectangle)
  hovering over a symbol reveals the assigned letter
  <img src="../../pics/excalidraw-create-element-by-letter.png" width="400">


# insert image
- use Ctrl+V to paste images into an Excalidraw drawing
- to modify a pasted image (e.g. rename or move to another location) just right-click inside drawing and select "Open Link"

<img src="../../pics/excalidraw-open-pasted-image.png" width="400">

## pasted image

file of any file is shown on top center location

<img src="../../pics/excalidraw-pasted-image.png" width="300">


# selecting any element opens sidebar to modify:
- Stroke = choose color
- Font family
- Font size
- Text align
- Opacity --> make element partially transparent
- Layers --> how to arrange content if image elements overlap each other
- Actions = copy, delete, link

<img src="../../pics/excalidraw-select-element-sidebar.png" width="500">

## different color

<img src="../../pics/excalidraw-change-color.png" width="400">



# lines and arrows can be customized

- select "Arrowheads" to change beginning and end of arrow
- deform by dragging mid-point --> new sub-sections with new midpoints created --> can further deform

<img src="../../pics/excalidraw-arrow-create.png" width="400">

## evolution of an arrow
<table style="border-collapse: collapse;">
  <tr>
    <td style="border: 1px solid black; text-align: center; vertical-align: top;">
      <span style="font-size: 1.25em; font-weight: bold; display: block; margin-bottom: 0.5em;">step 1</span>
      <img src="../../pics/excalidraw-arrow-1.png" width="400">
    </td>
    <td style="border: 1px solid black; text-align: center; vertical-align: top;">
      <span style="font-size: 1.25em; font-weight: bold; display: block; margin-bottom: 0.5em;">step 2</span>
      <img src="../../pics/excalidraw-arrow-2.png" width="400">
    </td>
  </tr>
  <tr>
    <td style="border: 1px solid black; text-align: center; vertical-align: top;">
      <span style="font-size: 1.25em; font-weight: bold; display: block; margin-bottom: 0.5em;">step 3</span>
      <img src="../../pics/excalidraw-arrow-3.png" width="400">
    </td>
    <td style="border: 1px solid black; text-align: center; vertical-align: top;">
      <span style="font-size: 1.25em; font-weight: bold; display: block; margin-bottom: 0.5em;">step 4</span>
      <img src="../../pics/excalidraw-arrow-4.png" width="400">
    </td>
  </tr>
</table>


# insert link

1. highlight / select any element
2. click onto "link" symbol (or use hotkey to insert link)

<img src="../../pics/excalidraw-symbol-link.png" width="100">

3. type link into input field above element

<img src="../../pics/excalidraw-link-input-field.png" width="300">

4. example link to other note

<img src="../../pics/excalidraw-link-to-other-note.png" width="400">


5. non-selected element with link has link-symbol on top right corner

<img src="../../pics/excalidraw-element-linked.png" width="400">

## following link opens new tab

left-click onto link-symbol to follow link --> this opens link target in new tab


<img src="../../pics/excalidraw-follow-link.png" width="600">


### Maybe you noticed: The same file is now open multiple times

Use "Split right" to work on different sections within the same file 😉

<img src="../../pics/excalidraw-note-split-right.png" width="500">

This layout arrangement can be useful when working on a note which is too long for your display. 

<img src="../../pics/excalidraw-note-split-right-in-action.png" width="400">



# export entire drawing to svg

I recommend working with SVG = scalable vector graphics. 
No matter how small or large, the image will always be of perfect quality (no pixelation by zoom). 

To export your drawing, select the 3 dots on the top right and select "Export Image". 

<img src="../../pics/excalidraw-export.png" width="300">

Then select "Export SVG" in the popup window. 

<img src="../../pics/excalidraw-export-svg.png" width="300">


# Several SVG files can be combined into a single note using HTML (advanced)

```html
<div style="display: flex; gap: 12px; align-items: flex-start;">
  <img src="excalidraw-examples/excalidraw-example-the-circle-of-git-flow.svg" width="400">
  <img src="excalidraw-examples/excalidraw-example-the-circle-of-git.svg" width="300">
</div>
```

<div style="display: flex; gap: 12px; align-items: flex-start;">
  <img src="excalidraw-examples/excalidraw-example-the-circle-of-git-flow.svg" width="400">
  <img src="excalidraw-examples/excalidraw-example-the-circle-of-git.svg" width="300">
</div>
