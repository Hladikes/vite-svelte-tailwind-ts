# Vite + Svelte + Tailwind + TypeScript project setup

## **How to setup this type of project on your own**

## Step 1
`npm init vite@latest`

## Step 2
Select svelte and then svelte-ts

## Step 3 - Install Tailwind
```npm install -D tailwindcss@latest postcss@latest autoprefixer@latest```

```npx tailwindcss init -p```

This will generate `postcss.config.js` and `tailwind.config.js`

## Step 4

Configure purge for `.svelte` files
```js
purge: ['./src/**/*.svelte']
```

*tailwind.config.js*
```js
module.exports = {
  mode: 'jit',
  purge: ['./src/**/*.svelte'],
  darkMode: 'media', // or 'media' or 'class'
  theme: {
    extend: {},
  },
  variants: {
    extend: {},
  },
  plugins: [],
}
```

## Step 5
Had issues with tailwind and ES modules:

`Tailwind CSS: Must use import to load ES Module ...`

I removed `type: "module"` from `package.json` and rewrote `svelte.config.js` from this
```js
import sveltePreprocess from 'svelte-preprocess'

export default {
  // Consult https://github.com/sveltejs/svelte-preprocess
  // for more information about preprocessors
  preprocess: sveltePreprocess()
}
```
To this
```js
const sveltePreprocess = require('svelte-preprocess')

module.exports = {
  // Consult https://github.com/sveltejs/svelte-preprocess
  // for more information about preprocessors
  preprocess: sveltePreprocess()
}
```

Or you can just clone this template `¯\_(ツ)_/¯`.

## *TODO*
Rename the title in **index.html**