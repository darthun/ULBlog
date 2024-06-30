+++
title = "Summer hit and cute shapes"
date = 2024-06-30T08:34:40-04:00
draft = false
+++

### Summer Hit and Cute Shapes

Hi there!

This post is a follow-up to 'Scanning Gyms,' but you don't need to have read it. Today, I'm sharing how I experienced my first heartbreak in Blender while modeling stuff for the gym.

I wanted to start with something "simple" in 3D modeling. Back then, I was blissfully unaware of the iPhone's magical powers and planned to model everything from scratch. So, I chose the most crucial piece of equipment in the boxing gym. The first thing we clients see when we walk in.

No, it's not the ring or Bri's swag.

It's this magnificent piece:

![Initial_Drawer](/initial_meuble.png)

Behold, this wonderfully simple shelf! *slaps roof* You're looking at a six-cube object with an X-shaped rail behind. It took me an entire afternoon to learn Blender and create this. And man, was I PROUD of it. If everything went this smoothly, the game was gonna move fast.

I showed my cool creation to my mentor, like a proud child showing the world's worst stick figure drawing to their parents.
He immediately pointed out that I had the scaling wrong and asked me to turn on some "facing" option.

![meuble_face](/meuble_face.png)

Just like in school, red usually means something is wrong. In this case, red means the program thinks the red side is the "inside" of whatever you're looking at.

"Yeah, that sounds about right? The blue is on the outside, the red is inside!"

Nope. It means the literal inside of the wood panels. You should never see anything red when looking at an object. This happened because I used a bunch of 2D rectangles and then grew them into 3D shapes. Apparently, you're not supposed to do that. You're supposed to build things like you would in real life. I'm no Sabrina Carpenter, I guess so; I just drink the espressos.

With that newfound knowledge, I rebuilt the shelf. No pictures yet.

##The iPhone Gym

Here's our nicely scanned 3D gym from the iPhone:

![gym](/gym.png)

You see where this is going. Let's show the face orientation:

![gym_face](/gym_face.png)

Yup, it can see through the reception walls. If the gym ever gets haunted outside Halloween, that's where your ghosts will be. That's also bad for light reflection and textures. The doors are also wrong.

##Geometry

There are pros and cons to having a lot of geometry in a simple wall. A big pro is that you can have fancy textures on it. A bigger con is that you're turning a simple shape into a bunch of shapes. It's harder on the computer. Sometimes you want all that fancy detail; sometimes you just don't care about having a 4K full HD black wall.

The iPhone creates very weird geometry. It doesn't even make sense. Look at how the entrance wall is split above the rightmost window. Why so many triangles there? That can't be good for light reflections.

![geometry](/geometry.png)

## Normals

Normals are like if you wanted to pin a nail into a part of the wall. The nail should always be straight. In this picture, they're the little teal lines. They should only point left-right or up-down like nintendo. But we see a lot of angled ones around the bathroom area. Vanessa thinks it's all the Febreze; it's distorting space-time. Anyways, it has to go.

![Normals](/normals.png)

## At What Cost?

Here are the stats for this scene:

![vertex](/vertex.png)

That's 5000 faces for 20 walls. I was expecting something like 200 faces. Lots of room for improvement.

So, just like the gym had to move next door to become bigger, I will have to rebuild the 3D gym to make it smaller.