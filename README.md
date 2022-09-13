# Nuxt 3 Cloudflare Workers

Install dependencies

```bash
yarn install
```

## cloudflare

Edit `.env` file and set `NITRO_PRESET=cloudflare`. Run `rm -rf .nuxt dist functions && yarn generate`.


Output:

```bash
 WARN  To preserve the export signature of the entry module "node_modules/nitropack/dist/runtime/entries/cloudflare.mjs", an empty facade chunk was created. This often happens when creating a bundle for a web app where chunks are placed in script tags and exports are ignored. In this case it is recommended to set "preserveEntrySignatures: false" to avoid this and reduce the number of chunks. Otherwise if this is intentional, set "preserveEntrySignatures: 'strict'" explicitly to silence this warning.


 ERROR  addEventListener is not defined                                                                                                                                                                             07:25:04

  at .output/server/chunks/nitro/cloudflare.mjs:414:1
  at ModuleJob.run (node:internal/modules/esm/module_job:193:25)
  at async Promise.all (index 0)
  at async ESMLoader.import (node:internal/modules/esm/loader:533:24)
  at async prerender (node_modules/nitropack/dist/shared/nitro.ce47800e.mjs:2668:26)
  at async node_modules/nuxt/dist/index.mjs:1399:7
  at async build (node_modules/nuxt/dist/index.mjs:1946:5)
  at async Object.invoke (node_modules/nuxi/dist/chunks/build.mjs:45:5)
  at async Object.invoke (node_modules/nuxi/dist/chunks/generate.mjs:31:5)
  at async _main (node_modules/nuxi/dist/cli.mjs:50:20)

error Command failed with exit code 1.
info Visit https://yarnpkg.com/en/docs/cli/run for documentation about this command.
```

## cloudflare_pages

Edit `.env` file and set `NITRO_PRESET=cloudflare_pages`. Run `rm -rf .nuxt dist functions && yarn generate`.


Output: 

```bash
 ERROR  Cannot find module '/Users/mca/dev/private/nuxt-cloudflare/functions/index.mjs' imported from /Users/mca/dev/private/nuxt-cloudflare/node_modules/nitropack/dist/shared/nitro.ce47800e.mjs                  07:26:15

  at new NodeError (node:internal/errors:387:5)
  at finalizeResolution (node:internal/modules/esm/resolve:429:11)
  at moduleResolve (node:internal/modules/esm/resolve:1006:10)
  at defaultResolve (node:internal/modules/esm/resolve:1214:11)
  at nextResolve (node:internal/modules/esm/loader:165:28)
  at ESMLoader.resolve (node:internal/modules/esm/loader:844:30)
  at ESMLoader.getModuleJob (node:internal/modules/esm/loader:431:18)
  at ESMLoader.import (node:internal/modules/esm/loader:528:22)
  at importModuleDynamically (node:internal/modules/esm/translators:110:35)
  at importModuleDynamicallyCallback (node:internal/process/esm_loader:35:14)

error Command failed with exit code 1.
info Visit https://yarnpkg.com/en/docs/cli/run for documentation about this command.
```