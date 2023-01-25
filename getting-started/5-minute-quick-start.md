---
description: >-
  Graphweaver comes with its own CLI, so it is simple to get up and running
  immediately.
---

# 5 Minute Quick Start

Create a new project by running

```shell
npm init @exogee/graphweaver
```

This will invoke the **Graphweaver Init CLI** which will respond with a series of prompts. These will ask you which backends to install, and create a scaffold project with schema folders ready to create a schema.

```shell-session
$ npm init @exogee/graphweaver
GraphWeaver

? What would your like to call your new project? 
test-project

? Which GraphWeaver backends will you need? 
(Press <space> to select, <a> to toggle all, <i> to invert selection, and <enter> to proceed)
 ◯ MikroORM - PostgreSQL Backend
 ◉ REST Backend



? OK, we're ready- I'm going to create a new app in /Users/username/Projects- is that OK?
Yes

All Done!
Make sure you npm install / yarn install / pnpm install, then pnpm start to get started

$ pnpm install

$ pnpm start
```

For the graphweaver default test project, running install and then `pnpm start` (as above) will launch the **Apollo Playground** at `localhost:4000` where you can run test queries. By default the only schema supplied will allow the following query and expected response:

```graphql
query {
    ping
}

{
  "data": {
    "ping": true
  }
}
```

If you can supply the above query and the application response is as above, the installation has been successful!

Use the supplied templates at `index.ts` and `schema/index.ts` to build your application.

