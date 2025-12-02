# Procedural Bird Wings

|![](Renders/Render2.png)|
|:--:|
| *Karma Render of Procedural Houdini Wing* |

|![](NewImages/BlueJayWing3.png)
|:--:|
| *Another Procedural Wing Displayed With Bluejay Feathers* |
## Milestone #1

For Milestone 1 I've been focused on creating and modeling base feathers to work off of in Houdini. 

|![](References/BirdWingDiagram.webp)|
|:--:|
|*Bird Wing Reference Image*|

As can be seen in the above diagram, different parts of a birds' wings have different types of feathers. The largest groups are the flight wings which consist of the primaries, secondaries, and tertials (sticking out to the left of the secondaries), and as we move closer to the base of the wing there are the different types of covert feathers—greater covert, median covert, lesser covert, and primary covert (Grouped into secondary and marginal vs primary covert feathers in this diagram).

|![](References/FeatherReferences/EuropeanGoldfinchFeathers.jpg)|![](References/FeatherReferences/CommonBuzzardFeathers.jpg)|
|:--:|:--:|

We can more easily see the differences between the kinds of feathers through real life layouts like those above. The different types of feathers have differing shapes, patterns, and barbs to them.

Now to actually model feathers in Houdini, I started off with a simple feather without much variation using Houdini 20's feather workflow.

![](Images/SimpleFeather.png)

From there, working from the feather layouts above I created different base feather's corresponding to each of the types of feathers. Moving forward I'll use these as bases to procedurallly generate feathers to place on my wing.
![](Images/MultipleFeathersNoTexture.png)

Right now, while I haven't hit all of my project goals for having most of the generator created, I was able to make the feathers themselves a lot more detailed than what I was expecting. Because of this though they took up most of my time, but it means I'll be able to produce higher quality wings moving forward. Most of what's been giving me trouble so far is just working within Houdini's feather workflow because, while it is very powerful, all of the nodes are new to me and there aren't a lot of good resources on the many ways to use them. Lastly, the bulk of the wings will be based on procedurally placing the feathers I've created, so even though I haven't gotten to that yet I believe I should still be on track. 

## Milestone #2

This milestone I focused on the process of procedurally placing and altering the feathers. As a first step, from my base feathers I created a feather layout similar to my references from milestone 1. I also created uvs for my feathers so that they could be textured from a reference image of a bird called a Kea.
![](NewImages/FeatherSpread.png)

The next step was to actually create a wing from the feathers. I settled on the base wing shape below to start with, but my base feathers had a lot of problems based on their thickness and having their barbs poke through eachother.
|![](Images/PokeyWingSpread.png)|
|:--:|

I first focused on adjusting the way I procedurally placed the feathers to be based on two curves, one for the base of the feathers and one for the tips, so that I could then raise the latter curve on the covert feathers so that they could be seen on top of the main flight feathers.

![](Images/BadWing4.png)

I also adjusted the width and noise used for the barbs of the feathers so that they were less vertical and wouldn't interfere with eachother. 
|![](Images/BaseWingSpread.png)|![](Images/AngledWingSide.png)|
|:--:|:--:|

Lastly I also experimented with grooming to procedurally place a bunch of feathers at once which I'll use in the future for the base of my wing.

|![](Images/SphereGroomNoTexture.png)|![](Images/SphereGroom.png)|
|:--:|:--:|

I think I'm pretty on track for my milestone 2 goals, allthough I would like to make the wing I generate look more cohesive and grounded which I think adding the base of the wing will help a lot with before the final submission. Additionally now that I have most of the tools for creating the wing set up, I want to expirement more with different textures and wing poses moving forward.

## Final Results

Before sharing the final results, I made some additional updates to my procedural bird wings. The main change I made was using a groom to create the base of the wing like I mentioned in the last milestone. The groom by itself for my default wing is shown below.
|![](NewImages/Groom.png)|![](NewImages/Groom2.png)|
|:--:|:--:|

And with uvs for Kea feathers it looks like the following.
![](NewImages/UVGroom.png)

Combining this with my feather output from before I get a full wing!
|![](Images/FullWingNoUVS.png)|![](Images/FullWingNoUVS3.png)|
|:--:|:--:|

Here are some additional outputs for my full default wing again using the Kea feather textures.
|![](Images/FullWingAltGroom.png)|![](Images/FullWingTop.png)|
|:--:|:--:|
|![](Images/FullWingTop2.png)|![](Images/FullWing5.png)|

Lastly I also set up a uv texture for Bluejay feathers for more variation and displayed them on the same base wing.

![](Images/FullWing)

![](NewImages/BlueJay1.png)

And now for my final results I created three different wing presets using my generator


|![](NewImages/BlueJayBlack2.png)|![](NewImages/KeaBlack.png)|
|:--:|:--:|
|![](NewImages/BlueJayWing2.png)|![](NewImages/KeaWing2.png)|
|![](NewImages/BlueJayWing3.png)|![](NewImages/KeaWing3.png)|

And I additionally did some renders of my wings without uvs in Houdini's Karma Renderer.


|![](Renders/Render3.png)|![](Renders/Render2.png)|
|:--:|:--:|
|![](Renders/Render4.png)|![](Renders/Render5.png)|

## Post Mortem

Overall I am very happy with my final results. I feel like I had a slow start on getting my generator for the wings up and running, but it let me add more detail and put more effort into creating the wings themselves. I'd love to expirement some more with rendering in Karma as it was a process I was very unfamiliar with before this project, but even just the base outputs I created were really satisfying. Additionally, I think it would be cool to create procedural textures of some kind for the feathers instead of relying on uvs and expirement with different color gradients and wing shapes. While my generator functions and excels at procedurally placing feathers, setting up the different wing poses still takes work for users, and I had to compromise on providing an easy editing interface. I experimented a bit with having parameters to control the different wing curves, but because of the abundance of types of feathers needing to be grouped differently and the intricate nature of the wings themselves, it just wasn't able to create good enough outputs while keeping the parameters broad enough to easily control. The wings I finetuned myself though for my final renders turned out great and overall I accomplished my goals for the project!

## References
* [Avian Report: Ornithology and Bird Biology](https://avianreport.com/ornithology-bird-biology/)
* [Everything You Need To Know About Feathers](https://academy.allaboutbirds.org/feathers-article/)
* [The Form and Motion of Real Birds: Morphology of Aves](https://falconsongstudios.com/bird-anatomy)
* [Birdify: Wing Shapes](https://www.birdfy.com/blogs/blogs/types-of-bird-wings-everything-you-need-to-know?srsltid=AfmBOooqPglGS5LFMCmoPbHOaWTLjkM7Vb7iix4vRPwi86O1jhLUzl7k)
* [How To Draw Wings](https://www.clipstudio.net/how-to-draw/archives/168451)
* [Featherbase](https://www.featherbase.info/en/species/Erithacus/rubecula)
* [Feathers - Simulating and Rendering](https://www.youtube.com/watch?v=rmIA-krfvXk&list=PLe0XlBlHzrpWeE5Mip7AOyXdEyR8jbrXe&index=9)
