# #12837

- Related issue: [#12837]([https://github.com/strapi/strapi/issues/12837#partial-timeline#)

This is a problem I've only encountered in pnpm workspace so far, and this repository is an example of what can be replicated. It also contains two examples where neither works:

- As a workspace package: [strapi-graphql-starter](packages/strapi-graphql-starter/)
- As a sub-folder inside project, which is not regarded as a workspace package, but use a shared lock file(pnpm-lock.yaml):  [strapi-project](strapi-project/).

To reproduce, you can run:

```bash
pnpm install
pnpm run develop --filter="strapi-graphql-starter"

cd strapi-project

pnpm install
pnpm run develop
```

