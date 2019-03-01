# Building High performance React Applications
@joekarlsson1

Only render when you need

Benchmarks - measure perf
34MS 

`?react_perf` perf dev tools

keys - don't use index or random
recommended: hash algo of the object

## What to Use

`shouldComponentUpdate()` - define exactly when component should render

-or-

Extend `PureComponent` instead of component - Shallow comparison of all props/state
If using immutable data, checks for new object

## Use Immutable Data
Makes tracking changes cheap

New object - pointer reference contains data
Instead of checking differences between contents of object, JS looks to see if the pointer is the same

## Isomorphic react

Initial render on server

Downsides:
- Debugging is harder
- Managing configs
- No DOM

## Prod build

Renders ~2-8x faster
Removes dev tools

## Stateless Components

Faster....

## Misc

- Gzip all the plaintext
- Compress images - png and lossless
- Use CDN
- Analyze webpack bundle during build process

Make it work, then make it fast

- Use key correctly
- Manage shouldComponentUpdate for deeply nested props and state
- Extend Purecomponents for shallow data
- Use immutable data
- Using stateless components
- Build for prod
- Analyze webpack bundle
- Render whenreally needed
- Make it work, then make it fast




