# Angular 2 Quickstart

CLI generates:
* Applications
* Components
* Directives
* Pipes
* Services
* Routes
* Unit Tests
* Protractor Tests

Tools included:
* Build tool
* Unit Tests
* Protractor tests
* Deployment
* Lint
    * Style guide checker
* Type definitions
* Code formatter (removed)
* CSS preprocessors

Install: `npm install -g angular-cli`

## Commands
Can generate your own add-ons (Bootstrap, color-scheme, OAuth, logo, etc.)

ng-completion allows double-tab to see options

Help: `ng --help`
New project: `ng new PROJECT_NAME`
Serve w/ LiveReload at [http://localhost:4200](http://localhost:4200): `ng serve`

## Lifecycle

### Bootstrapping - How does the app start itself?

```
./src/index.html
   /main.ts
```

#### Config

`./angular-cli.json` aka Bower - third party libraries (Lodash, Bootstrap, etc.)
`./package.json` - dev library
`./tslint.json` - configure TypeScript rules
`./typings.json` - configure type-checking tools
`./config/` - test runner config, etc.

Base required for router (relative to server, not including server)
`<base href="/">`

index.html is the template for the root component

Load System.js polyfill:

```
System.import('system-config.js').then(function() {
	System.import('main');
}).catch(console.error.bind(console));
```


## Tools

Build: `ng build`

Stored in `dist/`

Unit tests: `ng test` - watches for changes

E2E tests: `ng e2e` - server must be running

Lint: `ng lint`

Generate componenet: `ng generate component my-new-component` or `ng g component my-new-component`

Hook up:
- import into root component
- put a selector in the root component
- add a directive in the root component













