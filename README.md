# TinkerCAD Crash Course
A crash course in the Tinker CAD tools library.

## Purpose
The purpose of this tutorial is to teach core TinkerCAD tools tools in effective and practical ways. The way we create our Sticky Note To-Do Stencil today is not necessarily the most optimal way to do it (ie, the fewest steps). Instead, the focus is to look at the use cases for different TinkerCAD tools, especially in regards to creating 3D printable models.

## Goal
The goal of today is to answer 2 important questions for creating models to 3D print with CAD software.

### How do I effectively use the TinkerCAD tools?
This tutorial will showcase some of the most important tools we can use in TinkerCAD, but it won't show all of them. Instead, it focuses on the following principles for an effective and efficient TinkerCAD workflow:

#### 1. Shapes (the physical representation of geometry in TinkerCAD) are either a `solid` or a `hole`.

![alt text](image-10.png)

#### 2. Geometry is the shape of a shape.

![alt text](image-11.png)

#### 3. Grouping `solids` and `holes` together is how specialized geometry is created.

![alt text](image-12.png)

#### 4. TinkerCAD does not allow you to adjust the faces, edges, or vertices of geometry directly (which is different from most other 3D modeling or CAD software).

![alt text](image-13.png)

#### 5. TinkerCAD uses a grid that snaps shapes into place.

![alt text](image-14.png)

#### 6. TinkerCAD allows for specific dimensions and angles to be applied to shapes. Typing dimensions is always better than eyeballing it.

![alt text](image-16.png)

![alt text](image-17.png)

#### 7. Alignment tools are your best friend.

![alt text](image-18.png)

#### 8. Throwaway shapes can help you align shapes when you don't already have a shape to align to.

![alt text](image-19.png)

### How do I ensure that 3D models are as printer friendly as possible?
3D printers have come a long way, and we have some at STEM Collegiate that are cutting edge. But 3D printers aren't magic. The following principles will be considered throughout the design of our model:

#### 1. Printers print layer by layer, starting from the bottom of the model and moving upwards.

![alt text](image-20.png)

#### 2. Printer waste is harmful for the environment and increases costs of operation.
CONTENT WARNING: Image of the innards of a bird that swallowed plastic waste.

<details><summary>Click to View</summary>

![alt text](image-21.png)

</details>

#### 3. Printers cannot print in midair. If part of a layer is not directly on top of the layer beneath it, the printer adds support which increases printer waste.

![alt text](image-23.png)

![alt text](image-27.png)

#### 4. Printers have a hard time with steep overhangs (anything over a 45° angle). Adding support increases printer waste, and not adding support often results in failed prints which also increases waste.

![alt text](image-24.png)

![alt text](image-28.png)

#### 5. Printers have a hard time keeping sharp edges adhered to the print bed (90° sharp angles sometimes stick properly, but not always. Less than 90° will likely not stick at all). Adding a brim increases print waste, and not adding a brim can result in a failed print which also increases waste.

![alt text](image-25.png)

![alt text](image-26.png)

#### 6. Printers are not perfect in their dimensions, and have a very small margin of error. This can be avoided by adding tolerances that are a fraction of a mm to your model. Printing pieces that are supposed to slot into one another or fit together, but do not fit increase printer waste.

![alt text](image-29.png)

## Workflow
The best workflow for designing in TinkerCAD is:

1. Sketching the idea (my sketches are never to scale, but I do recommend including dimensions).
2. Consider 3D printer limitations and decide on an orientation for the model to print.
3. Design the model with that orientation in mind.
4. Export model.
5. Slice and print!

## Sketch (I did this for you)
When sketching your idea, have some measurements ready for anything that needs to fit a specific way. With many sketches, you'll also want a top, front, and side sketch so that you are thinking about how you model will look in 3 dimensions. In the sketches provided to you, there are the following views:

### Sticky Note
This view is just to keep in mind that a typical pad of Post-It Notes is `75mm` * `75mm`. We won't include the front or side view because we mostly just care about length and width.

![alt text](image.png)

### Stencils
Here we have a top view of the dimensions of our stencils. We won't include the front or side view because we mostly just care about length and width.

Our stencils have `76mm` * `76mm` squares so they will be just a little bit larger than our sticky notes.

The stencil tabs have a length and width of `10mm` * `20mm`.

![alt text](image-1.png)

### Holder Top View
With the top view, we have an open front so that our tabs have room to hang out the front. This makes the length of our hole `79mm`.

The width of the hole is `76.5mm` to account for fitting in the stencils which are `76mm`. `0.5mm` makes a world of difference when considering margin of error!

The outer walls of the holder will have a dimension of `82mm` * `82mm`.

![alt text](image-2.png)

### Holder Front View
Our front view shows the slots that will hold our stencils. If we assume our stencils will have a height of `1mm`, then `1.5mm` will have enough clearance for them to fit nicely.

We also have the width of the slots as `76.5mm` to allow for clearance.

The holder has a height of `30mm`.

![alt text](image-5.png)

### Holder Side View
Our side view just has our length and height dimensions.

![alt text](image-4.png)

## Orientation (I also did this for you)
When I think of how our 3d model should print, the biggest limiting factor is going to be those deep narrow slots in the front of our stencil holder. If those are printed horizontally, it would be impossible to get any support out, and without support it would sag resulting in a failed print. So printing with the bottom of the model on the build plate is a bad idea.

If we orient the model with the front face touching the build plate, we reduce this risk significantly. However, having our adhesion rely on those big slots could result in our print detaching from the bed and making the print fail.

With this in mind, we will plan to print this model with the back touching the buildplate. This should allow us to minimize our waste and risk of a failed print.

## Design (Now you have something to do)
With a plan in mind, it's time to design!

### Creating a New Document
1. Open up TinkerCAD and create a new 3D design.

![alt text](image-6.png)

2. By default, TinkerCAD gives files a ridiculous name. Change the name of your document so its easy to find later.

![alt text](image-7.png)

3. By default, TinkerCAD opens in `perspective` view. This is how the world appears to us normally with close things looking larger than far things, but it makes it nearly impossible to place shapes where we want. Click the little cube in the bottom corner to change to `orthographic` view. This view shows shapes in their measured dimensions no matter how far away they are.

![alt text](image-8.png)

4. To navigate the view in TinkerCAD, clicking your `middle mouse button` allows you to pan. Scrolling your `middle mouse button` allows you to zoom. Your `right mouse button` allows you to rotate. Using these buttons to navigate will make your life much easier.

![alt text](image-9.png)

### Creating Our Stencils

1. Find the `box` in the shapes menu.

![alt text](image-31.png)

2. Drag the box to the center of the work plane.

![alt text](image-32.png)

3. According to our sketch, the stencil dimensions are `76mm` * `76mm` * `1mm`.

![alt text](image-33.png)

4. Right now, a big flat square will likely have its corners peel off of the buildplate. We can cut the corners into rounded shapes! Open the search bar and search for a "MetaFillet". This will be useful for creating round corners.

![alt text](image-34.png)

5. Drag the fillet out and set the radius to `5`. It's okay for the height to be 8 because we will be cutting it out shortly.

![alt text](image-35.png)

6. Click and drag to select both of our shapes.

![alt text](image-36.png)

7. Select the `align` tool. A shortcut for the `align` tool is `L`.

![alt text](image-37.png)

8. With the `align` tool selected, we have some nodes pop into view. A good practice is to click on the shape you want other shapes to align to, which will sometimes move the nodes. Clicking on the nodes will align shapes according to their vertical and horizontal positions. Shapes can either have their edges aligned or their middles aligned. We want our fillet in the corner, so we will click on the nodes displayed below.

![alt text](image-38.png)

9. We need to cut all 4 of our corners, so we need more fillets! Click on the fillet to select it (you may need to click somewhere on the grid to deselect first). Then duplicate it with the `duplicate` tool. A shortcut for the `duplicate` tool is `Ctrl` + `D`.

![alt text](image-39.png)

10. Both fillets are overlapped right now, but the new duplicate is selected by default. By holding `Shift` we can add the stencil to our selection, and align it to the next corner with the `align` tool!

![alt text](image-41.png)

11. We can rotate our fillet by selecting it and clicking on the curved arrow. Dragging the curved arrow will rotate the fillet. Holding the `Shift` key will force it to rotate in `45°` increments.

![alt text](image-42.png)

12. We will repeat that process 2 more times so that all of our corners have a fillet.

![alt text](image-43.png)

13. Next, we turn the fillets into hole pieces. Select the 4 fillets and turn them into holes.

![alt text](image-44.png)

14. To cut the holes out we can select everything and use the `Union Group` tool. The shortcut for `Union Group` is `Ctrl` + `G`. Our hole shapes will be removed from our main stencil shape.

![alt text](image-45.png)

15. We are creating 3 stencils today, so we will duplicate our main stencil twice.

![alt text](image-46.png)

16. Next we will add in our tabs. Our tabs are 10mm * 20mm * 1mm boxes. Because we will also want these rounded, we will start by making one rounded tab, then duplicate it twice.

![alt text](image-47.png)

17. To round it, we will cut the front 2 corners with hole fillets, but smooth the back corners out with solid fillets. The fillets will have a radius of `5` and a height of `1`. Grid snapping and `align` will help us ensure all of our shapes are connected properly.

![alt text](image-48.png)

18. We will group these tab pieces together with `Union Group` and duplicate it 2 times.

![alt text](image-49.png)

19. To simplify, `align` the 3 stencil bases so they overlap. We will align 1 of our tabs `5mm`from the edge of a stencil template. Grid snapping will make this pretty easy.

![alt text](image-50.png)

20. Our second tab will get snapped to the other side.

![alt text](image-51.png)

21. A trick we can do to put our 3rd tab in the middle is group our first 2 tabs, and then align our 3rd tab to it. Once it's alligned, we can ungroup the other 2 tabs. (You will need to click the button, `Ctrl` + `G` will not ungroup).

![alt text](image-52.png)

22. For each of our stencils, we will group 1 stencil with 1 tab. To make sure we don't accidentally put 2 tabs on one stencil, we will hide each stencil with `Ctrl` + `H` after we group each one.

![alt text](image-53.png)

23. `Ctrl` + `Shift` + `H` will show all of our hidden shapes again. 

![alt text](image-54.png)

24. Time to add some stencil lines! We will start with square checkboxes, and we can do this by making a box (hole) that is `6mm` * `6mm` * `6mm` with a corner radius of `1mm`. The lines will be created wit a box that is `1.5mm` * `60mm` * `6mm`, and will also have a corner radius of `1mm`. Both shapes will need to be moved down `2mm` to ensure they cut through the stencil properly.

![alt text](image-55.png)

25. Once you are happy with the placement of the 2 holes, select both and duplicate them. Hold `Shift` and move them backward on the workplane until they are a distance away that feels right. Then, without clicking anything else, duplicate again. Duplicate should create multiple copies that move back the same amount each time!

![alt text](image-56.png)

26. We don't want to redraw our lines for each stencil, so select all of our lines and duplicate them. With the duplicate holes selected, group them with 1 of the stencils. Once they are grouped, hide the stencil that has the holes cut out.

![alt text](image-57.png)

27. Next we will replace the square holes with cylinder holes. We can align some `6mm` * `6mm` * `20mm` cylinders where our boxes were, and then delete our boxes.

![alt text](image-58.png)

28. Again, we will duplicate the holes to save ourselves some work, then group the duplicates with our stencil and hide it.

![alt text](image-59.png)

29. Last but not least, we will shorten our boxes for the stencil lines to `22mm` in width so we can create 2 columns of check list items.

![alt text](image-60.png)

30. Group the last stencils with the holes, unhide everything with `Ctrl` + `Shift` + `H`, and now we have 3 stencils!

![alt text](image-61.png)

### Creating Our Holder

1. We will start with creating our outer box, which has the dimensions of `82mm` * `82mm` * `30mm`.

![alt text](image-62.png)

2. Next, we will cut out our sticky note slot. Our sketch measurements are ~~`79mm` * `76.5mm` * `20mm`~~, but we are actually going to start with `76.5mm` * `76.5mm` * `20mm` so we can add some guides here in a minute. We will align this hole with the top center of the main box.

![alt text](image-63.png)

3. Our guides will be created with a roof piece, because the roof piece will allow us to keep our overhang below 45°. Rotate the roof piece, then set the dimensions to `76.5mm` * `38.25mm` * `20mm`.

![alt text](image-65.png)

4. First we will align it with our sticky note hole, then use the grid snapping so that the sticky note hole becomes a house shape.

![alt text](image-66.png)

5. Cut the holes out by grouping everything together!

![alt text](image-67.png)

6. For the slots to hold our stencils, we need a box hole that measures `76.5mm` * `76.5mm` * `1.5mm`. Then duplicate it 3 times.

![alt text](image-68.png)

7. We will align our 3 slot holes, and then stack them on top of eachother so they are `1.5mm` away from eachother (one will move up `3mm` and the other will move up `6mm`). Then we will group them.

![alt text](image-69.png)

8. To vertically align everything, we will create a throwaway box that has a height of `10mm`. This is the height between the base of our holder and the bottom of the sticky note hole. We want our slots to be in the middle of those. Once the box is created, align the slots vertically with it. Then delete the throwaway box.

![alt text](image-70.png)

9. Finally, align the slots with the front of the main box, and cut them out!

![alt text](image-71.png)

### Extension - Decorating A Print
Secretly, I had a 3rd goal in mind: How do I make ***cool*** 3D prints?

By creating flat `1mm` thick decorations, you can put shapes, text, or even images on the faces of a 3D print!

#### Main Steps

1. Create a shape that is `1mm` thick. It can be any shape, and below there will be ***fancy*** shapes you can use. The shape needs to be flat on 2 sides. This example will use a cylinder, but you can use anything.

![alt text](image-73.png)

2. Rotate the shape so it has the same orientation as the face you are putting it on. These shapes **cannot** be placed on the face that will be put on the build plate.

![alt text](image-74.png)

3. Align the shape how you would like, then pull it out `0.5mm`. With grid snapping on, you either need to change the snap grid value or type in the amount you want to move it by.

![alt text](image-75.png)

4. With a `1mm` thick shape overlapping by `0.5mm`, you can now either emboss (raise) or engrave (cut out) the decoration. These measurements create a `0.5mm` overhang, which is shallow enough that it doesn't cause print issues, but deep enough that it can be clearly seen.

![alt text](image-76.png)

5. To emboss, leave the decoration as a solid. To engrave, turn the decoration into a hole. Then, group it with the face and *voila!* your print is now cool!

![alt text](image-77.png)

#### Basic Text
1. The basic text tool can be searched for.

![alt text](image-72.png)

2. Once text is created, you can change what it says with the `text` parameter, and change the way it looks with the `font` parameter.

![alt text](image-79.png)

3. Scale your text to fit the face it goes on. Once the width and length are correct, set the height to `1mm`. Then follow the Main Steps above.

![alt text](image-80.png)

#### Custom Fonts
TinkerCAD has a very limited font selection. If you want a custom font, you can import an SVG of the text that you want. If you aren't familiar with making SVGs, then a quick and easy process is outlined below:

1. Visit [https://text-to-svg.com/](https://text-to-svg.com/).

![alt text](image-81.png)

2. Type in your desired text and choose your desired font. Embossing and engraving works best with a solid font as opposed to one with lots of little pieces coming off.

![alt text](image-83.png)

3. Download the SVG (make sure to save it somewhere you can find it!).

![alt text](image-84.png)

4. Back in TinkerCAD, click `Import`.

![alt text](image-85.png)

5. Click `Choose a file` and find the SVG you just created.

![alt text](image-86.png)

6. The dimension sizes length and width are linked, so figure out which one is too big or too small for the face you want to put it on and change the value as needed. Then click `Import`.

![alt text](image-87.png)

7. Set the thickness to `1mm` and follow the Main Steps above.

![alt text](image-88.png)

#### Charms
TinkerCAD has some premade decorative shapes called "charms".

1. Search "charm" and find one that looks cool.

![alt text](image-89.png)

2. Add it to the workplane, set the thickness to `1mm`, and follow the Main Steps above.

![alt text](image-90.png)

#### Custom SVGs
Any 2 color image can be turned into an SVG for you to decorate faces with. This can be images you find online or even ones you sketch yourself. If you aren't familiar with making SVGs, then a quick and easy process is outlined below:

1. Have an image that can easily be converted to 2 colors. I sketched this rocket just for today!

![alt text](image-91.png)

2. Visit [https://picsvg.com/](https://picsvg.com/). Don't accidentally misclick on this website because it has a lot of fake ads.

![alt text](image-92.png)

3. Click `UPLOAD A PICTURE` and find your picture.

![alt text](image-93.png)

4. Scroll down and click `DOWNLOAD SVG`. Make sure you save it somewhere you can find!

![alt text](image-94.png)

5. Back in TinkerCAD, click `Import`.

![alt text](image-85.png)

6. Click `Choose a file` and find the SVG you just created.

![alt text](image-86.png)

7. The dimension sizes length and width are linked, so figure out which one is too big or too small for the face you want to put it on and change the value as needed. Then click `Import`.

![alt text](image-95.png)

8. Set the thickness to `1mm` and follow the Main Steps above.

![alt text](image-96.png)

## Export (This is the last thing we are doing together)

1. With the model selected, click `Export`.

![alt text](image-99.png)

2. Make sure that you have `The selected shape.` selected. Then chose `.STL` for the file type. By default the file name will be set to your main file's name, so rename it accordingly so you don't just overwrite the same file over and over again. Repeat these steps for each model in your file.

![alt text](image-100.png)



## Slice and Print (This is your homework)
With  your STL saved, you are ready to print!

I'd love to make more of a tutorial with screen shots, but slicingg and printing is a whole new kettle of fish. This tutorial should be able to get you started, but there are also some experts around the school who would love to help!

Good luck, and have fun printing!

[Tutorial Video](https://www.youtube.com/watch?v=xUi54VpSeek)
