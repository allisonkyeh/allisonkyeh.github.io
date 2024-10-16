---
layout: post
title: Lighting
permalink: /lighting/
---

My lighting work for Stranger Things VR encompassed scenes throughout all 9 chapters and a mixed reality chapter.<br>
The technical restrictions of VR meant I had to rely on combining techniques including glow cards, volumetric light beams, emissive materials, shader lighting properties, and environmental fog, all working cohesively with a very limited number of lights. <br>I also did all the set dressing throughout these scenes.

<div class="img_row">
	<img class="col half" src="{{ site.baseurl }}/documentation/2024_stvr/lighting/attic-flip.gif"/>
	<img class="col half" src="{{ site.baseurl }}/documentation/2024_stvr/lighting/attic_reference.webp"/>
</div>

The before and first pass comparison, with the show reference on the right. My first pass served to push the lighting to match the show using colder blues, volumetric beams, and more focused lighting in the area where the player will be most active.

{% include video id="1020050086" provider="vimeo" %}

In the final game, the attic becomes a hub from which the player can enter Vecna's red Mind Lair at the ceiling. The beams had to be moved to make way and instead framed this red area to direct the player. 
Using fog tech, I could match the show's blue streaks of light seeping through the attic cracks while transitioning to a dark night outside if the player walks near a window- shown in the video.

<div class="img_row">
	<img class="col one" src="{{ site.baseurl }}/documentation/2024_stvr/lighting/creelhouse_8before.png"/>
	<br>Before and after of the Creel House memory flashback in Chapter 2. By adjusting environmental fog, I pulled the saturated blue back into a more subdued teal and decreased visibility to emulate dusk time. To create a focus on the house, I used a combination of volumetric beams and glow cards for fake window lights. Fireflies add some peaceful ambience and the upper left glow is from a light post shining on the player's active area.
</div>

<div class="img_row">
	<img class="col three" src="{{ site.baseurl }}/documentation/2024_stvr/lighting/creelhouse_8after.png"/>
</div>

<div class="img_row">
	<img class="col half" src="{{ site.baseurl }}/documentation/2024_stvr/lighting/hopperext1.png"/>
	<img class="col half" src="{{ site.baseurl }}/documentation/2024_stvr/lighting/hopperext3.png"/>
</div>

Before and after of Hopper's cabin in Chapter 7, where you play as the giant spider monster attacking the human characters trapped inside. This moment references a dark moonlit forest scene in the show, with warm lights spilling out from inside indicating signs of life and targets to attack.

<div class="img_row">
	<img class="col half" src="{{ site.baseurl }}/documentation/2024_stvr/lighting/MR_portal_arcadeA.png"/>
	<img class="col half" src="{{ site.baseurl }}/documentation/2024_stvr/lighting/MR_portal_labA.png"/>
</div>
<div class="img_row">
	<img class="col half" src="{{ site.baseurl }}/documentation/2024_stvr/lighting/MR_portal_scoopsA.png"/>
	<img class="col half" src="{{ site.baseurl }}/documentation/2024_stvr/lighting/MR_portal_interrogationA.png"/>
</div>
These spaces show up within portals that open up in the mixed reality chapter. Since multiple portals could be open at the same time, each space could only have a single light and I optimized all these scenes to under 40k vertices, some of which were above 140k vertices. Then I used a combination of glow cards, emissive materials, environment fog, and set dressing to hide the low poly nature of the optimizations and make the spaces feel distinct.

<div class="img_row">
	<img class="col one" src="{{ site.baseurl }}/documentation/2024_stvr/lighting/MR_portal_ingame.png" style="float:right"/>
	<br><br><br>
	Example of the lab shown in a mixed reality portal on the right. <br> The one light in each space working with the previously mentioned techniques created a focal point which would be framed in the portals and emphasize grabbable props within.
</div>

<div class="img_row">
	<img class="col half" src="{{ site.baseurl }}/documentation/2024_stvr/lighting/MR_portal_arcadeFront_flip.gif"/>
	<img class="col half" src="{{ site.baseurl }}/documentation/2024_stvr/lighting/MR_portal_genstore_flip.gif"/>
</div>

Before and after comparison. I adjusted environment fog colors and depth and added a variety of glow cards to emphasize the electronic lights of the arcade and sunlight streaming into the store, to support the one light allowed.

<div class="img_row">
	<img class="col half" src="{{ site.baseurl }}/documentation/2024_stvr/lighting/MR_portal_bathroomA.png"/>
	<img class="col half" src="{{ site.baseurl }}/documentation/2024_stvr/lighting/MR_portal_bathroomB.png"/>
</div>

These MR portals also needed a blue corrupted version where Vecna's vines take over. However there was the technical restriction that geometry and materials had to be the same, so the environment fog did most of the work in creating constrast.


<!--
<div class="img_row">
	<img class="col three" src="{{ site.baseurl }}/documentation/2020_college/ayeh2_shader_final.png"/>
</div>
-->

<div class="img_row">
	<img class="col half" src="{{ site.baseurl }}/documentation/2024_stvr/lighting/alicebedroom_flickerlights_1.gif"/>
	<img class="col half" src="{{ site.baseurl }}/documentation/2024_stvr/lighting/creelhouse_chandelier_spot.gif"/>
</div>

I created dynamic lights in C# that flicker based on proximity to the player's hands, like how lights react to Vecna in the show. The flicker consists of the emissive material's color and intensity in addition to the light's color and range. I included flickering for bloom as well, before post processing was scrapped for performance reasons. The dynamic lights component also had a smoother, slower pulsing setting and a more intense setting that shattered the bulb, though these were not featured in the game.

The chandelier has the dynamic light script as well as a constraint setup that allowed the player to grab and swing the chandelier.