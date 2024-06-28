+++
title = "Scanning People"
date = 2024-06-24T15:24:40-04:00
draft = false
+++

## The Problem

Replicating someone's likeness in a video game is like trying to paint the Mona Lisa with a paint-by-numbers kit—except the paint is in invisible ink. Professional game studios have entire armies of artists to design the hair, the clothes, and everything in between.

I, on the other hand, have a budget that could be comfortably described as "nonexistent" and skills that are "developing." So, I need a shortcut to get realistic models into the game without turning into a hermit for months to learn new software. Enter MetaHuman, a free asset from Unreal Engine that helps make models that are, well, pretty useful.

### Requirements
- Has to work with the Unreal 5 default skeletal mesh (Manny)
- Has to work with the boxing animation pack (Oh lord, the anim graph)
- Has to be simple enough to edit ( spoilers : It's not simple)
- Has to look like the people I'm trying to replicate ( Mo's face as the new Lena of 3d modeling.)

## The Solution

I found a few sites that offer to create scans from pictures, and other cool 3D tools and plugins:

### Blender Plugin
Blender has this paid plugin where you can upload a bunch of real photos from different angles and sculpt the default Blender face into the references. It works okay if you have really good reference photos and your face looks like the default model. It stops working if you have a beard or if you have two ears...

![Blender Plugin](/images/blender-plugin-image.png)

on the left you see the final result, on the right you see the starting mesh.

### Hyperhuman by Deemos
Hyperhuman by Deemos is a website that offers to transform a picture into a MetaHuman model. [Hyperhuman](https://hyperhuman.deemos.com/). I used it to try to get Mo's face, and it does a great static mesh for Blender. No facial hair, but "we'll add that in post" like they say in the movie industry.

![Hyperhuman Result](/images/hyperhuman-image.png)

### Then why not use that ?

Well I tried ! But even with the best mesh, you lose quality during the promote frame step of MetaHuman generation.
Those beautiful details get lost when you transform the mesh into a picture, and from the picture into the MetaHuman.
I must avoid the promote frame step at all cost, or else Mo gets transformed into a generic metahuman.

![Mesh to Picture](/images/mesh-to-picture-image.png)

### AI 3D Object Modeling Tools
I also tried some 3D object modeling tools by AI, and it gave me a super realistic, PlayStation 1 era looking Michael. I love the fidelity of this technique, even if the quality is super low. I can't use it in the game because it doesn't make a full model.

I lost the picture, sorry !

## Future Techniques

The last technique on my to-do list is using the depth perception camera on the iPhone to take a normal video of someone (Hi Mo!) and use that to generate the MetaHuman directly, bypassing the dreaded "promote frame" process.

There's also a method involving Polycam to scan the body and Bellus 3D Faceapp to scan the face. This approach keeps the body size and clothing intact, and the face should look realistic. The downside? You get a mesh that isn't a MetaHuman. Following the tutorial, you end up with a Mixamo character, which has a different rigging and bone structure than the UE5 character, making animations as compatible as a square peg in a round hole.

To fix that, there's supposedly a 'mesh-to-metahuman plugin' but I suspect it uses the promote frame approach, which, as we've established, is the arch-nemesis of detail preservation.

## Conclusion

This exploration of 3D modeling people has given me a bigger appreciation for good 3D models. In a world where my coding experience used to make me think " that's just code, I can see how they did that." 

I leave you with my upgraded Mo Face Scanning Station:
![Face Station](/images/facestation.jpg)


##Delete below, image testing

1
![Blender Plugin](ULBlog/images/blender-plugin-image.png)
2
![Blender Plugin](ULBlog/blender-plugin-image.png)
3
![Blender Plugin](blender-plugin-image.png)
4
![Blender Plugin](/blender-plugin-image.png)
5
![Blender Plugin](/assets/blender-plugin-image.png)
6
![Blender Plugin](assets/blender-plugin-image.png)
7
![Blender Plugin](ULBlog/assets/blender-plugin-image.png)
