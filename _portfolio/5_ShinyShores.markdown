---
layout: post
title: Shiny Shores
permalink: /shinyshores
img: /documentation/2024_shinyshores/v2_captures/gameplay_rushingwave.gif
img_hover: /documentation/2024_shinyshores/v2_captures/title_loop.gif
---

A summery beach game where you collect sparkly treasures while avoiding crashing waves!

Developed in a week with <a href="https://thuleanx.github.io/">Thuleanx</a> and <a href="https://www.willbertiz.com/">Whullum</a> for Brackeys Game Jam 2024.2, and rated 15th out of 1500+ entries. <br>I created all the art, including models, rigs, animations, environment, UI, shaders, and VFX.

You can play Shiny Shores on itch.io <a href="https://ayucinna.itch.io/shiny-shores">here!</a>

<div class="img_row">
	<img class="col three" src="{{ site.baseurl }}/documentation/2024_shinyshores/v2_captures/gameplay_4.gif"/>
</div>

Collect shiny seashells, seaglass, and more while dodging the incoming waves by running back to the pier or using rocks as cover. The rocks are washed up by the wave, and sink in increments with following waves.

<div class="img_row">
	<img class="col three" src="{{ site.baseurl }}/documentation/2024_shinyshores/waveshader.gif"/>
</div>

Wave shader incorporating UV masks and multiple layers of noise and voronoi for the foam and edge. <br> I added a color gradient to add depth to the teal, blended between unposterized and posterized looks for a softened stylization, and layered voronoi at the wave edge to create rough edges emulating the brush texture in my concept art. 
<br>
The tech of the rock obstacles stopping sections of the wave was handled by Thuleanx.

<div class="img_row">
	<img class="col half" src="{{ site.baseurl }}/documentation/2024_shinyshores/debris_ref2.png"/>
	<img class="col half" src="{{ site.baseurl }}/documentation/2024_shinyshores/debristurntable.gif"/>
</div>

Debris concepts and final in-game models, with custom shaders to accentuate the shininess of the seaglass and pearl.

<div class="img_row">
	<img class="col three" src="{{ site.baseurl }}/documentation/2024_shinyshores/clementine_ref_ingame.png"/>
</div>

Concepts/turnarounds and final model in game of the player character, Clementine.

<div class="img_row">
	<img class="col quarter" src="{{ site.baseurl }}/documentation/2024_shinyshores/clem_anim_pickupidle.gif"/>
	<img class="col quarter" src="{{ site.baseurl }}/documentation/2024_shinyshores/clem_anim_run.gif"/>
	<img class="col quarter" src="{{ site.baseurl }}/documentation/2024_shinyshores/clem_anim_drown.gif"/>
	<img class="col quarter" src="{{ site.baseurl }}/documentation/2024_shinyshores/clem_anim_wakeupidle.gif"/>
</div>

Pickup, running, drowning, and revive animations; the pick up and revive are blended with an idle.

<div class="img_row">
	<img class="col three" src="{{ site.baseurl }}/documentation/2024_shinyshores/v2_captures/title_loop_HQ.gif"/>
</div>

<div class="img_row">
	<img class="col quarter" src="{{ site.baseurl }}/documentation/2024_shinyshores/v2_captures/button_hover_2_crop.gif" style="float:right"/>
	<br><br> Title screen and UI that sparkles on hover!
</div>

<div class="img_row">
	<img class="col three" src="{{ site.baseurl }}/documentation/2024_shinyshores/v2_captures/gameover_2.gif"/>
</div>

End score screen and more button UI that sparkles on hover. You can see all the treasure you collected here!

<div class="img_row">
	<img class="col three" src="{{ site.baseurl }}/documentation/2024_shinyshores/env_beachwave.gif"/>
</div>

Initial concept art for the environment and wave, which set the foundation for the feel and layout of the game.

