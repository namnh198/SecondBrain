---
title: Alpine.Js
createDate: 2024-12-14
published: true
draft: true
tags:
  - Javascript
---
## References
- [Official Docs](https://alpinejs.dev/start-here)
## What's Alpine?
- A modern lightweight Javascript framework - A jQuery replacement
- Despite being lightweight, it manages to encapsulate almost all the functionalities
## Installation
### Use CDN

```html showLineNumbers title="index.html" ins={3,6}
<html>
<head>
	<script defer src="https://cdn.jsdelivr.net/npm/alpinejs@3.x.x/dist/cdn.min.js"></script>
</head>
<body>
	<h1 x-data="{ message: 'Hello Worlds' }" x-text="message"></h1>
</body>
</html>
```
### Import

```shell
npm install alpinejs
```

```js showLineNumbers title="main.js"
import Alpine from 'alpinejs'
window.Alpine = Alpine
Alpine.start()
```

## How to use
### `x-data`
`x-data` defines a chunk of HTML as an Alpine component and provides the reactive data for that component to reference.

```html title="index.html"
<div x-data="{ message: "Hello Worl" }">
	<button
</div>
```

```html title="index.html"
<div x-data="{ count: 0 }">
	<button x-on:click="count++">Increment</button>
	<span x-text="count"></span>
</div>
```
## Use Plugin

```html showLineNumbers title="index.html" ins={5, 9-14}
<html>
<head>
	<!-- .... -->
	<!-- import collapse script -->
	<script defer src="https://cdn.jsdelivr.net/npm/@alpinejs/collapse@3.x.x/dist/cdn.min.js"></script>
</head>
<body>
	<!-- .... -->
	<div x-data="{ expanded: false }">
		<button @click="expanded = !expanded">Toggle Content</button>
		<p id="foo" x-show="collapse" x-collapse>
			Lorem ipsum....
		</p>
	</div>
</body>
</html>
```

## Alpine in Astro
### Installation

```shell
npx astro add alpinejs
```

The `@astrojs/alpine` integrations adds `Alpine` to the global window object. For IDE autocompletion, add the following to your `src/env.d.ts`

```ts title="src/env.d.ts"
interface Window {
	Alpine: import('alpinejs').Alpine
}
```

### Configuration Options
You can extend Alpine by setting the `endpoint` option to root-relative

```js title=astro.config.mjs ins={5}
import { defineConfig } from 'astro/config';
import alpine from '@astrojs/alpinejs';
export default defineConfig({
	// ...
	integrations: [alpine({ entrypoint: '/src/entrypoint' })],
});
```

```ts title="src/entrypoint.ts"
import type { Alpine } from 'alpinejs'
import intersect from 'alpinejs/intersect'

export default (Alpine: Alpine) => {
	Alpine.plugin(intersect)
}
```
