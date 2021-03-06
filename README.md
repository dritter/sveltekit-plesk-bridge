![](https://img.shields.io/badge/-Svelte-000?&logo=Svelte) ![](https://img.shields.io/badge/-Plesk-000?&logo=Plesk)

# sveltekit-plesk-bridge

This project bridges ES modules to CommonJS to avoid the following Error:
```
Error [ERR_REQUIRE_ESM]: require() of ES Module build/index.js from node-loader.js not supported.
Instead change the require of index.js in helper-scripts/node-loader.js to a dynamic import() which is available in all CommonJS modules.
```

## Installation

The package must be added as a production dependency if you build on your production server!

NPM

```bash
npm install svelte-plesk-bridge
```

Yarn

```bash
yarn add svelte-plesk-bridge
```

After that is done, append to your `build` script in the `package.json`:

```
    "build": "svelte-kit build && cp node_modules/sveltekit-plesk-bridge/entry.cjs build/",
```

## Credits

Go to [LessBorders](https://stackoverflow.com/users/18592470/lessborders), who suggested this fix on [StackOverflow](https://stackoverflow.com/a/71632513).

