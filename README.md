# `beforeRouteUpdate` is called after `asyncData`

## Reproduction steps

```sh
git clone git@github.com:moltar/route-hooks.git
cd route-hooks
npm i
npm run dev
open http://localhost:3000/foo/1
```

1. Open browse console
2. Click Next Page
3. Observe `console.log` output
