---
layout: post
title: Shaders
permalink: /shaders/
---

<div class="img_row">
	<img class="col one" src="{{ site.baseurl }}/documentation/2021_baz/baz_turnaround_compress.gif" alt=""/>
	<img class="col one" src="{{ site.baseurl }}/documentation/2024_shinyshores/clem_anim_run.gif"/>
	<img class="col one" src="{{ site.baseurl }}/documentation/2025_secretflorist/clover_pose3.png" alt=""/>
</div>

My toon shaders thus far! I love making stylized toon shaders that feel simplified but slightly soft.
<br>Starting from the left, this was my first deep dive into shaders which got me interested in stylized game art. It uses layers of glows apart from bloom to soften the hard cuts of toon shading, with an outline post processing effect using sobel edge detection.
<br>The center shader is unlit, and focuses more on textured fresnels that match the ocean waves style of the game.
<br>The last shader is my most recent lit toon shader that improves greatly upon the left one. In addition to rim lighting, I also used other techniques to support the shader such as tweaking vertex normals and the gradients in the texture itself to create a soft appearance.

<div class="img_row">
	<img class="col half" src="{{ site.baseurl }}/documentation/2024_vfxa/casestudy_lightningzap_secondpass_variation_small.gif"/>
	<img class="col half" src="{{ site.baseurl }}/documentation/2024_vfxa/casestudy_lightningzap_shader.gif"/>
</div>
Procedural lightning VFX and nodes in ShaderGraph.
<br>This shader uses UV masking, UV distortion, and vertex displacement with custom vertex data to create unique lightning bolts for each particle, including the surrounding secondary bolts.
<br>Inspired by studying the lightning effects in Breath of the Wild.


<div class="img_row">
	<img class="col three" src="{{ site.baseurl }}/documentation/2024_vfxa/elemental_waterfallfinal_still.png"/>
</div>

I made all components of this stylized waterfall that uses a couple shaders with scrolling noise, refraction, vertex displacement, depth based foam, and slightly softened toon shading to prevent it from feeling too cartoon-y.

<div class="img_row">
	<img class="col one" src="{{ site.baseurl }}/documentation/2024_shinyshores/debristurntable_reflective.gif"/>	
	<img class="col two" src="{{ site.baseurl }}/documentation/2024_shinyshores/waveshader.gif"/>
</div>

A couple shaders from <a href="https://allisonkyeh.com/shinyshores/">Shiny Shores!</a>
<br>For this reflective seaglass shader, I wanted the highlight to be visible at all angles so it depends on view direction instead of light.
<br>This wave shader incorporates UV masks and multiple layers of noise and voronoi to make the foam and edge more rough and varied.
<br> I added a color gradient to add depth to the teal, blended between unposterized and posterized looks for a softened stylization, and layered voronoi at the wave edge to create rough edges emulating the brush texture in my concept art. 
<br>

<div class="img_row">
	<img class="col half" src="{{ site.baseurl }}/documentation/2022_dp/dp-spawn.gif"/>
	<img class="col half" src="{{ site.baseurl }}/documentation/2022_dp/dp-purple-short.gif"/>
</div>

This dissolving shader was done early on in my game dev journey to experiment with ethereal character effects and hidden spaces that reveal in proximity.

<div class="img_row">
	<img class="col half" src="{{ site.baseurl }}/documentation/2024_stvr/cleanse.gif"/>
	<img class="col half" src="{{ site.baseurl }}/documentation/2025_fj/fj_ghostwaves.gif"/>
</div>

My work with Tender Claws included building upon and maintaining HLSL shader code.
<br>I modified our stylized toon shader to create the area of effect for this cleanse attack in <a href="https://allisonkyeh.com/stvr/">Stranger Things VR</a>, as well as other toon lighting adjustments.
<br>In <a href="https://allisonkyeh.com/facejumping/">Face Jumping</a>, I added this effect that pulls geometry in the scene to create a bouncy fisheye transition.