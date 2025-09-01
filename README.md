# Texture Map Editing Tutorial
A tutorial repository for Texture map editing in Krita.

## Edit the Texture Map in Krita
To edit the texture map of a 3D object, you can you use any software that can draw on a .png file. Because it is free and simple I will be using Krita for this tutorial. Below is a piece of a texture map for a traffic barrier:

![image](https://github.com/user-attachments/assets/9d7a2b7a-ba62-4bb5-adcb-fb385b133f99)

As you can see it is covered in markers which need to be removed. Here is another texture map for a metallic object:

![image](https://github.com/user-attachments/assets/e3f93f42-2a89-4f5d-a8b9-181e9e08e76c)

It has been partially edited, but as you can see the issue with this map is the yellowey tones. Because this is a metallic silver object, we need to remove the yellow spots. The creality raptor is not as good at getting texture maps as it is with getting dimensions. So, this yellowy pattern will likely show up on every metallic object. This could be because of the scanner or because of the way the creality software creates texture maps. So, let's start fixing these in Krita.

When you open Krita, this is what you will see:
![image](https://github.com/user-attachments/assets/bd50db96-bd94-453a-a739-072ebb37d29a)

Click Open Image and navigate to the .png file texture map you want to edit. In this example I will edit the metallic object. It is helpful to have the object open in blender with the texture map showing as a reference. When you open your file, you will see something like this:
![image](https://github.com/user-attachments/assets/40ae0ca6-8344-419e-a3ce-c7d320341210)

To fix texture maps, you need to know how to use the pen tool, the blend tool, the eyedropper tool, how to lock the transparency of the texture map, and how to filter the image.

On the left side of the screen, there is this toolbar:

![image](https://github.com/user-attachments/assets/42328e8c-d5e1-46e7-8ee1-77c5221df6e7)

Circled in red is the brush tool ![image](https://github.com/user-attachments/assets/93e25815-cd5f-4a16-b432-8ecf18dac71e) and the eyedropper tool ![image](https://github.com/user-attachments/assets/4b8de83c-0f16-4800-9922-8e9a8a2e1fd3)

You can think of this toolbar as different modes for your mouse cursor. All we will need to use is the brush and eyedropper tools. Toward the bottom right of your screen, you will see favorited brushes:

![image](https://github.com/user-attachments/assets/32412a47-babc-4638-8d38-d713617972d2)

You can hover your mouse over each brush to see what it does. On this computer I have favorited an airbrush tool, a pen tool, a soft pen tool, a blend tool, and a blur tool. These are all the brushes you will need to fix texture maps. When you have selected ![image](https://github.com/user-attachments/assets/93e25815-cd5f-4a16-b432-8ecf18dac71e) from the toolbar you can click on any of the brush icons to use them. In the provided screenshot I have selected the pen tool. 

At the top of the screen:

![image](https://github.com/user-attachments/assets/ddee2b6f-67bc-4bbd-ba0d-339d29f82764)

You can change the opacity (meaning how "see-through" your brush is) and size of your current brush

When you select the ![image](https://github.com/user-attachments/assets/4b8de83c-0f16-4800-9922-8e9a8a2e1fd3) from the toolbar you will be able to click any part of the image to copy that color. When you do this and switch back to your brush tool you will be able to draw with that color.

Now you need to know how to keep the transparency of the texture map while you are editing it. In the middle right of your screen is your layers panel:

![image](https://github.com/user-attachments/assets/669bc184-a2d7-478b-b8af-77870511982b)

Here you can change manage everything about your layers. When you open a .png in Krita, it will create one layer to work on called "Background." When we edit texture maps we need to make sure we leave the empty spaces empty, so we have to lock the transparency. To do this, click on your layer in the layer panel. Press this button ![image](https://github.com/user-attachments/assets/2bee91af-5f2c-4bbc-8a08-a1af41238927) to duplicate your layer. Now, press this button ![image](https://github.com/user-attachments/assets/814ed247-b49b-4d8a-bc86-4458f0ea45a7)

Once you have followed the above instructions, your layers panel should look like this:

![image](https://github.com/user-attachments/assets/b261a039-e3ef-4b11-b11c-0380b520fb10)

Now the copy of your layer is looking at the original layer for its transparency values. This means that now you can draw anywhere in the file and it will only draw over the texture that was already there. This step is very important. You are now ready to edit the texture map.

Helpful keyboard shortcuts:
* CTRL+A is select all
* CTRL+C is copy
* CTRL+V is paste
* CTRL+T is transform
* CTRL+SHIFT+A deselect all
* B switches to the brush tool
* P switches to the eyedropper tool

### Erasing markers from texture maps

**Draw-over method**
- Use the eyedropper tool to pick the color you want to replace the marker with
- Use the pen tool to draw over the marker with the selected color
- Use the blend tool to blur the edges of the marker covers to make them look natural

**Copy-paste method**
- Press ![image](https://github.com/user-attachments/assets/db67045b-5845-41d2-901a-9023a04796c0) on the toolbar
- Draw around a texture you want to copy
- Copy it with CTRL+C
- Paste it with CTRL+V
- Press CTRL+T to move the copied section over your marker
- Press enter to complete the move
- Blend in the edges of the pasted texture


### Fixing "glitchy" tone patterns in texture maps

The method to fix this depends on the object. Usually you can will use a combination of the Draw-over and Copy-paste methods listed above along with filtering the image. You can filter an image in Krita by pressing ![image](https://github.com/user-attachments/assets/c901f322-8575-4c6b-a6ec-4e16a0e4abfe) 

The following link provides documentation on how to use every filter from the official Krita manual.
https://docs.krita.org/en/reference_manual/filters/adjust.html

### Export your edited texture map
* Go to File > Save As 
* Name your file
* Save it as a .png with the following settings:
  
  ![image](https://github.com/user-attachments/assets/8e898373-c1a9-4709-9891-42e6edf440cd)

* Make sure that you edit the .mtl file of your object to tell it to use the new texture map.
