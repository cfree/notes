# Node.js Cloud Functions

[Infrastructure as code](https://arc.codes)

WTFjs
Brian LeRoux

Functions as a service

3 current options:
- Terraform - HCL, proprietary language. Key/value pairs, nested braces. Provisions lambdas in AWS
- Serverless - YAML - wires lambdas and DynamoDB table. Lots of config knowledge
- AWS SAM - YAML

Infrastructure as code. Committing build artifacts
Prefer achitecture as text - .arc

Manifest goes in the root of repo
Comments start with #
Sections start with @
Everythign afterwards becomes infrastructure

```
@app
helloapp

@html
get /
```

Tooling is local to the project using npm scripts
Like express, but response is a function

`npm start` runs in memory, offline
`npm run deploy` deploys to staging



Definition of insanity or devops



