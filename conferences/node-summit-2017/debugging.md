# Debugging in 2017

Paul Irish - @paulirish

`console.log`
`printf`

## Basics

`node --inspect hello.js`
`node --inspect-brk hello.js` - pause on first statement

 Chrome: `about:inspect`
 > Open dedicated tools not Node

Interesting features:
- Column breakpoints(!)
- Blackbox (avoid stepping through)
- Live editing

june07.com/nim
github.com/jaridmargolin/inspect-process
github.com/darcyclarke/rawkit


- Debug an existing Node process
`process._debugProcess(pid);`

- Use GDB -like CLI debugger
`node inspect hello.js`

- Drive the DevTools protocol via WS port

- Drive with DevTools protocol via `require('inspector)`


## Tracing in Node
`node --trace-events-enabled index.js` - creates json file, open in chrome via `chrome://tracing`

Breakdown of network request latency (sitting on top of Async wrap in core)

https://github.com/nodejs/node/pull/14347

"Explore, think beyond console log"