# Exercise 2.2—Physics Bodies

Exercise for MSCH-C220

In this exercise, you will play with some of the 2D physics bodies available in Godot 4.

The expectations for this exercise are that you will

 - [ ] Fork and clone this repository
 - [ ] Import the project into Godot
 - [ ] Create a CollisionPolygon2D for the Walls that encloses the play area
 - [ ] Add the Godot icon.svg as a Sprite2D node in Object1 and Object2
 - [ ] Use the "Create CollisionPolygon2D Sibling" menu item to create collision information for Object1
 - [ ] Manually create an appropriately sized CollisionShape2D For Object2
 - [ ] Manually create a CollisionPolygon2D For Object3
 - [ ] Create a circular CollisionShape2D for the Gravity node
 - [ ] Set parameters for Object1, Object2, and Gravity
 - [ ] Edit the LICENSE and README.md
 - [ ] Commit and push your changes back to GitHub. Turn in the URL of your repository on Canvas.

## Instructions

Fork the repository. When that process has completed, make sure that the top of the repository reads `[your username]/Exercise-2-2-Physics-Bodies`. *Edit the LICENSE and replace BL-MSCH-C220 with your full name.* Commit your changes.

Press the green "Code" button and select "Open in GitHub Desktop". Allow the browser to open (or install) GitHub Desktop. Once GitHub Desktop has loaded, you should see a window labeled "Clone a Repository" asking you for a Local Path on your computer where the project should be copied. Choose a location; make sure the Local Path ends with "Exercise-2-2-Physics-Bodies" and then press the "Clone" button. GitHub Desktop will now download a copy of the repository to the location you indicated.

Open Godot. In the Project Manager, tap the "Import" button. Tap "Browse" and navigate to the repository folder. Select the project.godot file and tap "Open".

You will now see a fairly-empty scene with six placeholder nodes: Game, Walls, Object1, Object 2, Object 3, and Gravity.

Select the Walls node, and add a CollisionPolygon2D child node. Select the CollisionPolygon2D node, and using the new tools in the toolbar, create a box around the play area. When you are done, if you have done it correctly, you should see a multi-colored hollow rectangle around the window-size indicator in the viewport.

Next, select Object1 and add a Sprite2D child node. Drag the icon.svg from the FileSystem panel into the sprite's Texture property in the Inspector. Select the Sprite2D, and in the Sprite2D menu, select "Create CollisionPolygon2D Sibling". The defaults are fine, so you can press the "Create CollisionPolygon2D" button.

Make sure you have selected the Object1 node, and then position it at 100,100.

Next, select Object2 and add a Sprite2D child node. Drag the icon.svg from the FileSystem panel into the sprite's Texture property in the Inspector. Selecting Object2, add another child node, this time select CollisionShape2D. That CollisionShape should be of type RectangleShape2D, and its size should be 100,100 (accessed by editing the RectangleShape2D in the Inspector). Position Object2 at 600,200.

Select Object3 and add the Godot icon as its sprite. Selecting Object3, add a CollisionPolygon2D, and then draw around the outline of the image. Rotate Object3 by 45 degrees, and set its position at 700,500.

Now, select the Gravity node. It won't have a sprite associated with it, but it will have a collision shape. Add a CollisionShape2D, make that collision shape a CircleShape2D and set its radius at 100 pixels. Position the Gravity node at 150,300.

Now we need to describe each node's behaviors. Object1 needs a new PhysicsMaterial. Editing that PhysicsMaterial, set the Friction at 0.01 and the Bounce at 1. Leave Rough and Absorbent unchecked.

Create a new PhysicsMaterial for Object2. Editing that PhysicsMaterial, set the Friction at 0.05 and the Bounce at 0.5. Leave Rough and Absorbent unchecked. Then, back in the Inspector for the Node, give it an initial Linear Velocity of 100,100 and an Angular Velocity of 1 degree.

Select the Gravity node, and in the Gravity submenu in the Inspector, set the Space Override to Replace, and set Gravity to 100.

Run the simulation. See how each of the objects behaves.

Quit Godot. In GitHub desktop, you should now see the updated files listed in the left panel. In the bottom of that panel, type a Summary message (something like "Completes the exercise") and press the "Commit to master" button. On the right side of the top, black panel, you should see a button labeled "Push origin". Press that now.

If you return to and refresh your GitHub repository page, you should now see your updated files with an indication of when they were changed.

Now edit the README.md file. When you have finished editing, commit your changes, and then turn in the URL of the main repository page (`https://github.com/[username]/Exercise-2-2-Physics-Bodies`) on Canvas.

The final state of the file should be as follows (replacing my information with yours):
```
# Exercise 2.2—Physics Bodies

Exercise for MSCH-C220

A physics playground, experimenting with different types of 2D physics nodes in Godot 4.

## Implementation

Created using [Godot 4.1.1](https://godotengine.org/download)

## References
None

## Future Development
None

## Created by
Jason Francis
```
