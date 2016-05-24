# Angular 2 Observables
@geofffilippi

Observables, change detection, AsyncPipe, forms, RxJS

===

Hiring:
- Dish - Java, JavaScript (Angular, React) - William Johnson
- homebuy @ Galvanize

Authorization with JWTs and Macaroons

===

Fundamentals
Related concepts
Angular 2

## Fundamentals

### Reactive Programming

Data flows - how to get data through application
Propagation of change

[Reactive Manifesto](reactivemanifesto.org) 

* Responsive
* Resilient
* Elastic
* Message driven


### Functional Reactive Programming (FRP)

Combination of reactive programming *and* functional programming

Functions are first-class in JavaScript, can pass functions as data


## Related concepts

Observer Design Pattern

* Subject tracks observers
* Subject notifies observers of state changes


Object can change, subject reacts

* Subject, Observable, Producer - same, can be observed and produces events
* Observers, Consumer - same, watches for events


Other info:

* [Object.observe](arv.github.io) is not the same of observables, proposal withdrawn
	Criticisms:
    * Big changes to Object internals
    * Bad performance
    * Not well-supported or adopted
    * Ecosystem moved in different direction
* Promises, callbacks, etc.
* RxJS v5.0 implements the TC39 Observable spec (implementation used in Angular 2)


## Observable

Differences between Object.observe:
* Observables are a wrapper around what you care about
* Object.observe mutates the object data


### Comparison

* Promises:
	* like an sync variable - single value
	* cannot be cancelled
	* not lazy
	* good for some AJAX calls (unless you want to cancel)
	* `.catch()`, `.finally()`
* Observables:
	* like an async array - multiple values over time
	* streams
	* can be unsubscribed
	* lazy, until you call `.subscribe()`
	* better for events
		* WebSockets
		* Animations
		* AJAX you want to cancel
	* Can be retried
	* `.catch()`, `.finally()`
	* `throttle()`


Turn something async turn into observable:

* Promises `.from()`
* Generator `.from()`
* Events `.fromEvent()`
* DOM
	* AJAX
	* WebSocks `.fromWebSocket()`
* Node streams
* Other observable implementations: bacon.js, kefir.js
* Arrays (or other non-async concepts) `.of()` 


`.then()` of Promises is `.subscribe()` of Observables

Observables do not need to complete, can go on forever


## Angular 2

Used for:

* Forms, inputs - can be processed as it changes
* `Http` - can be canceled, returns observable
	* "Typeahead" example of stream results
	* `.retry(3)`
* AsyncPipe - like a filter, data liable to change over time. `{{ observerVariable | async }}`
* Change detection - new digest cycle?s
	* Apps are reactive
	* Change detection is directional
	* You can skip walking parts of the tree
		* Immutable objects
		* Observables


Reactive extensions for Angular 2
`ngrx/store` can be used to implement elm/redux-style applications in Angular 2

Questions:
* New digest cycle?
* `$q.all()` ?a





