# A Gentle Introduction to WebGL

Joanne Cheng
@

Rendering 2D, 3D graphics in the browser using computer's GPU

Single thread on the CPU, calculations can be done at once with GPU

Mostly Chrome, Firefox until recently. Now has good support, including for mobile

"Practical" 3D graphs. Each view can tell a story 

Three.js: WebGL wrapper library


### Scene, Camera, Render before you can draw objects

Scene controls lights

Camera describes how objets in scene will be viewed. Perspective

- Vertical field of view
- Horizontal field of view 

Render 

- Plane geometry


## WebGL and Maps

Mapbox.gl
Renders maps with WebGP, render at a high framerate

Deck.gl = React + Mapbox.gl + Philogl (WebGL wrapper, low-level)

Example: Plotting longitude / latitude of each earthquake. Wanted to include magnitude

JS -> GPU: Create shaders, initiate buffers

Shaders: 

- Vertex shader retrieves collection fo verticies
- Fragment shader, executed after for each pixel

Send specific attriutes (array of objects), turn into flat attributes


Chrome Experiments


