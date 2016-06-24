# Single-Page Access: The Road to Using Our Power for Good

Suz Hinton
@noopkat

"We have a multiplier effect on what we do" - Rob Deluca

Our work should be a positive impact on people's lives, but we don't always reach everyone

Lots of tools to choose from: AngularJS, React.js, Ember, etc.
Frontend frameworks introduced a paradigm shift in how we approah applications, but present new challenges
Are they accessible?

1. Motor Ability: how we use our bodies to access applications, how we interact with the computer
	Assumption: everyone is using a mouse
	Is a mouse necessary for your site? Should be able to use tab key

`<li>`, `<p>`, etc. are not keyboard-accessible
Should use `<button>` and `<a>` for JavaScript-based functionality. 
Semantic HTML is your friend!

Template linting can ensure you have these accessibility items in place:

- react-a11y
- ember-template-lint
- Angular: Protractor a11y plugin


1. Vision + Motor Ability: Blindness, screen-reader
	Lots of dynamic content
	How to handle loss of cursor location?
	Buttons should have focus states, but that can be lost and the 
	cursor goes to the top of the page.Disorientation!
	Can pass along the focus from one element to another on "click"

- react-focus-trap
- ember-component-focus - which element in component should receive focus
- angular - custom? call `.focus()` on something

1. Screenreaders talk to accessibility model from server-side changes, but nothing occurs on front-end routing
	We can fix it! Use a11y plugins

Material2 comes with 'LiveAnnouncer'

"Help users find their way"

Humans are not edge cases. Estimate tasks with a11y in mind. Ask for research time

Incorporate a11y testing in your test suite. Recommends that the build breaks if accessibility breaks

Are we moving the web forward if we're leaving people behind?

"Computers do exactly what we tell them, and no more" - anon

0-20% of Internet users have some kind of disability

`Cmd + F5` fires up built-in Mac screenreader w/ tutorial
Jaws on Windows and IE/Edge
NVDA for Firefix







