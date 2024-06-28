+++
title = "Scanning Gyms"
date = 2024-06-26T15:00:40-04:00
draft = false
+++

## To make a Boxing Gym

When I first started this project, I wanted to keep it a surprise. Half the cool points of making a "so-bad-it's-good" video game would come from the shock value. Once people have expectations, it's harder to impress them. It's like trying to make a follow-up to a viral De Niro meme video !

Anyway, to make a boxing game, you need a ring. And that ring needs a gym. And that gym needs walls. And those walls need dimensions. Lots of numbers. My buddy, who works in video games, suggested, "Why don't you just show up at the gym with a measuring tape?" But I didn't want to look any weirder than I already do. There's only so much fairy drawing one can bring to a boxing gym before people start questioning your brain health.

So, I decided to learn a whole new framework to hide my social awkwardness.

### FSpy : When you don't wanna measure things the normal way.

Enter fSpy, an absolutely amazing (and free!) Blender plugin. It's simple, it works, and it's amazing. You take a bunch of pictures, ideally with no zoom. It works best if you have 'something, anything' that appears in all the pictures, like a dumbbell or a pillar or a roller cushion. This object becomes the ultimate center of the universe.

For big rooms: as long as two pictures share a common feature, you can create a mosaic juxtaposition and move your reference point. It's like shifting the center of the universe for each picture until everything is perfectly balanced, as it should be. (but it won't be)

### Pictures into virtual cameras 
To achieve this, you have a bunch of pictures and a bunch of virtual cameras. The goal is to place the virtual camera in the virtual world such that what they see matches the real-life picture they are associated with. You can then move between cameras in the virtual world and see the gym from different points of view.

With everything aligned, you can easily draw any shape on top of the picture, and the proportions will be right in the virtual world. It's basically a big coloring book where you just add shapes on top of the image. It works like magic once you get your ducks in a row.

![Blender Cameras](/bunchcamera.png)

### Linear Algebra for boxers.

To align the camera, you just need to draw lines representing an orthonormal base for the 3D space of the picture. Super easy, right? Especially when you're working with a room full of nice 90-degree corners.

![Camera Base](/camerabase.png)

In this example, you can see I mapped the first arrow (red) to the depth, the second arrow (green) to the lenght, and the height (blue) is automatically computed by vector multiplication. The white dot is a preview of the result, which I placed on a wall corner to make sure everything is aligned correctly.

### Where's Eliam ?

I'm not a photographer, and I don't know what an f parameter is, or how FOV can be distorted, or anything like that. fSpy needs the dimensions of your camera sensor to work. Most phones don't provide that information. They tell you the focal distance and the lens size, but not the sensor size. Who cares about that stuff, anyway?

I found the lens size info for my trusty Samsung A50 on a database for phones: 

![Camera Base](/A50-1.png)

But as you can see, it doesn't have the sensor size. Knowing the picture dimensions, the lens size, and other info, I thought I could calculate the sensor size. And yes, we have the technology ! I asked ChatGPT to do it for me, expecting a simple calculation, but it turned out to be two pages of math with some integrals.

 Crazy stuff. The result was close, but the floating precision was off, and Vanessa's office ended up with a punching bag in it ! The math is correct, she's just too far from the origin of the universe (a blue rolling thingy by the ring stairs that day).

### Google's GoldenEye.

One weaker minded individual would have given up by now and revealed their need for a measuring tape. But not me. 

Google map has a 360 view of the world, and I obtained the ring size from Joey, so I thought it would be enough information to recreate the rest of the gym.
With google map, you can measure anything : 

![Sat Image](/gymsat.png)

That's a nice approximation, but I wasn't super happy. 

### Get your shit together

Eventually, I had to come clean to the coaches about my clandestine measuring tape endeavours. Now, I can't step into the gym without everyone quizzing me about the game's progress. Which is also why I started this blog : to keep everyone in the loop and, let's be honest, to keep myself accountable.

One such day, Malik who was doing nothing at the reception casually asked: "Did you try scanning things with the new iPhones?" Ten minutes later, after borrowing Joey's phone, I had this model.

![Sat Image](/iphonegym.png)

So I bought an iPhone.

Of course, I still need to redo everything from scratch, but I'll save that saga for another post.
