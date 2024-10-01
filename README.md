# bytesize_animate_subway_map

Animating subway maps in SVG.

The aim of this bytesize will be to animate a subway map in SVG.
The subway map will be a simple one, with only two stations and one line to illustrate the `Hello Nextflow` training.
Files are already provided:

SVG:

![Nextflow hello metro map](hello-nextflow_metro_map.svg)

PNG:

![Nextflow hello metro map](hello-nextflow_metro_map.png)

In `VS Code` (or any other text editor), add this snippet in the SVG, just before the closing `</svg>` tag,
Make sure to use the id of the path you want it to follow (in the `href` of the `animateMotion` tag).

```html
<circle
   style="fill:#000000;stroke-width:9.17687"
   id="circle2"
   cx="-1.4115639"
   cy="-0.80445743"
   r="4.5884361">
    <animateMotion
   begin="0s"
   dur="2s"
   repeatCount="indefinite">
      <mpath
   href="#path1" />
    </animateMotion>
  </circle>

Visualize the animation in your browser.
In `Inkscape`, move along your circle so that it starts at the first station.
Note that's it's not usually the actually starting point of the path.
So you might need to go back and forth between moving the circle and go back to your browser to see the animation.

You can then duplicate the updated snippet to create a second circle, and play with `begin` to have a delay.
Or duplicate and make the circle follow a different path.

Animated SVG:

![Nextflow hello metro map](hello-nextflow_metro_map_animated.svg)
