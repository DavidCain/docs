---
title: Node.JS API Tutorial
name: Node.js API
thirdParty: false
alias:
  - node
  - nodejs
  - node.js
languages:
  - Javascript
image: /media/platforms/node.png
tags:
  - quickstart
snippets:
  dependencies: server-apis/nodejs/dependencies
  setup: server-apis/nodejs/setup
  use: server-apis/nodejs/use
---

## NodeJS API Tutorial

<%= include('../_includes/_package', {
  pkgRepo: 'node-auth0',
  pkgBranch: 'master',
  pkgPath: 'examples/nodejs-api',
  pkgFilePath: null,
  pkgType: 'server' + account.clientParam
}) %>

**Otherwise, Please follow the steps below to configure your existing NodeJS app to use it with Auth0.**

### 1. Add express-jwt dependency

You need to add the express-jwt dependency.

Just run the following code to install the dependency and add it to your `package.json`

${snippet(meta.snippets.dependencies)}

### 2. Configure express-jwt with your Auth0 account

You need to set the ClientID and ClientSecret in `express-jwt`'s configuration so that it can validate and sign [JWT](/jwt)s for you.

${snippet(meta.snippets.setup)}

### 3. Secure your API

Now, you need to specify one or more routes or paths that you want to protect, so that only users with the correct JWT will be able to do the request.

${snippet(meta.snippets.use)}

### 4. You're done!

Now you have both your FrontEnd and Backend configured to use Auth0. Congrats, you're awesome!
