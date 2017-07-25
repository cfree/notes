# Marko

@psteeleidem

http://markojs.com/

Node.js entirely on the front-end
HTML rendering using Marko

Node 6.x
200 apps and growing
Node.js platform team of 7 devs
Very vibrant internal community - internal open source
80 platform modules
330 total modules

Marko UI library
Nodejs can stream HTML to the browser to help improve page load times

Streaming is a preqed for progressive HTML rendering
Break up rendering to flush things in multiple chunks

Allows browser to fetch/paint page earlier. Increase page load time
Only helpful with async rendering, otherwise gzip compressed

Progressive HTML rendering - buffered on the server
Out-of-order flushing - best load time for users

Express view engine does not support streaming
Bypass view layer

## Marko
- Template rendering engine 
- Isomorphic rendering - same code on server/browser
- Async and streaming rendering
- VDOM rendering
- Clean syntax with zero boilerplate
- Tiny runtime (~10kb gzipped)
- Single-file UI components

Can be used in Node and in browser

React-equivalent?

[Marko-cli](https://www.npmjs.com/package/marko-cli)

Code generated optimized for streaming. Renders as a VDOM tree instead of stream.








