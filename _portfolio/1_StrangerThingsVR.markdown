---
layout: post
title: Stranger Things VR
permalink: /stvr
img: /documentation/2024_stvr/stvr_thumbnail.jpeg
img_hover: /documentation/2024_stvr/stvr_elpush.gif
---

<iframe width="560" height="315" src="https://www.youtube.com/embed/Xo5SDo8rNjE?si=nH0G-63Qf1RV9obd" title="YouTube video player" frameborder="0" allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture; web-share" referrerpolicy="strict-origin-when-cross-origin" allowfullscreen></iframe>

As a technical artist at <a href="https://tenderclaws.com">Tender Claws</a>, I created, implemented, and optimized a wide variety of art in engine.<br>
This includes VFX, lighting, shaders, procedural creature animations, set dressing, environments and interactive props, <br>and implementing story sequences.

Released February 2024.

See my lighting work on this project <a href="https://allisonkyeh.com/lighting/">here.</a>

{% include video id="1068981717" provider="vimeo" %}

I programmed a state machine that allows these spiders to traverse any uneven surfaces, cross inner and outer corners, drop downwards on a thread, ragdoll if telekinetically grabbed by the player, and be crushed to death on impact.

<br>

{% include video id="1069020397" provider="vimeo" %}

I created a hallway system that repositions the Rainbow Room behind every interactive door. Because of this only one copy of the Rainbow Room is needed, preventing overlapping meshes in limited space and cutting down on geometry.
<br>As part of this system, I also wrote the door behavior; the doors can be opened on either side, automatically close if the player moves out of range, can be grabbed open again before it fully closes, lock and unlock throughout the narrative sequence, and works as a single door or double doors.

More info here: <a href="https://tenderclaws.com/strangerthingsvr">https://tenderclaws.com/strangerthingsvr</a>