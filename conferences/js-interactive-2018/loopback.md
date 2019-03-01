#  The Art of Building Node.js Projects at Scale
- Raymond Feng, IBM @cyberfeng

Loopback 4 is now GA!

https://developer.ibm.com/tutorials/create-rest-apis-minutes-with-loopback-4/

## Organizing code base

Loopback v1-3:
- Large number of packages and repos
- Npm link - many PRs in different repos for one fix
- CI complexity
- Hidden contracts - only the dev knows the intention of the code

Loopback v4:
- Lerna - 1 repo, multiple packages
- - TypeScript project references
- TypeScript
- - provides contracts
- - self-documenting
- - compiler/IDE support

## Managing artifacts

Core - IoC container
- Universal knowledgebase - Single registry for runtime, tooling
- Key based binding
- DI

Lots of artifacts
Unknown future extensions
Unknown roadmap

Contribute artifacts

Circuit breakers component?

Chaining responsibilities
- Sequence of actions - middleware style (one way vs cascading)
- A coordinator, such as bootstrapper, to walk through multiple phases and invoke different methods
- Functional composition

Improving user productivity
- Establish conventions
- CLI (app, extension, controller, datasource, model, repository, service, example, openapi)
- - Templates

Large-scale node.js projects have:
- Scale the code base with modulatory w/o complexity
- Scale the devs with language/IDE productivity
- Scale the runtime with patterns
- Scale the users with conventions and tools


