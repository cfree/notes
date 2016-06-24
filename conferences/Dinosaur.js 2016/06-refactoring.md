# Making it Better Without Making it Over

Rebecca Murphey, Indeed.com
@

Evangelize FE best practices

Monolithic frameworks c. 2007, 08: Dojo, YUI, Sproutcore (Ember), ExtJS
Backbone.js made things accesible for jQuery devs

"Growth is not bad, growth without a strategy for managing it is"
"Its easy to feel like the only way to make things better is to start over"

Can be easy to fall into the same traps you're in by starting from scratch with something new if you've never used it before.

Example:
- 40 parameters on initialization
- Moved parameters to an object (model), may use Redux to manage state
- Added ESLint to project, fix errors. "Guardrails"
	- Elevated JS among team, there is a right way that can be verified
- Instrumenting key user features, real-time analytics
	- What's important? What will be bad if broken?
	- What are the key actions that a user can take?
- Added `package.json`
	- Added Git hooks for Jenkins to leverage
		- Run ESLint

Lessons Learned:
- Tessa Thornton article. "Its unrealistic for you ... to learn a framework that solves a problem you've never experienced"
- "Every technology decision is eventually regretable" made in good faith with best information they had at the time
	- Doing web development is an exercise in empathy
- Can't avoid JS growth, have to manage complexity
- Education is a powerful enabler. Teaching how to care and what to care about is immensely transformative. 
- "Building for the web is better today" than it was 10 years ago, for example.

Easier to teach someone how to use a framework than to teach the fundamental problem solving skills



