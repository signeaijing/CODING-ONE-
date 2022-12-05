<h2> PROJECT DESCRIPTION </h2>

This project was inspired by The Adams Family and in particular the cello scene from the new Netflix adaption made by Tim Burton with Jenna Ortega, Catherine Zeta-Jones and The OG Christina Ricci. It's uncanny spooky camp. 

<h3> THE CODE </h3>

I build the whole thing with THREE JS by building a world made up by a Sphere Geometry and a Plane Geometry. I tried first to go with the Skybox textures that allows for a more infinite feeling, but I couldn't find any free SkyBox Texture packages online. It worked out in my favour as I have the final vibe feels more claustophobic as if you're too close to the objects. 

I created functions with groups for each different group of objects needed for the scene. This is both done for a smoother read of the code as well as the control of the lightning and animation. My objects are created in three different functions, createWorld() holds the sphere and plane, createGhosts() holds the groups of ghosts, createBubbles() holds the main Ghost. Then all of them are called in the createMain(scene). This one is maybe redundant as I along the way needed most of the functions to be called into a global variable in order to be animated on. All the animation is going on in the draw() function. 

One of the tricky things was to get the small ghosts to fly around in something that didn’t seem too planned. This was finally done by ghosts.rotation.xy += 0.002; 
Because each geometry has an individual starting position they move differently around the sphere. 

<h3> MAXIMILIAN </h3>

If you have ever silenced a horror movie you would know that half the horror lies in the soundtrack. Therefore, I found it vital to incorporate sound to the project. I imported cello chords as my main sound and on top of that violins and real sounds. It was a struggle to get it to work in the beginning as Maximilian has updated it's syntax since week 2 where we were introduced to it. It finally worked by loading my samples and putting the play function in a initial audioscript and then the actual AudioEngine in the main script along with the THREE JS code. It needs to be done this way because the whole thing needs to be passed onto the AudioEngine by the setAudioCode() 
