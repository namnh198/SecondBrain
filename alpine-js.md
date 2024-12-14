---
title: Alpine.Js
createDate: 2024-12-14
published: 
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

```html title="index.html"
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

```js
import Alpine from 'alpinejs'
window.Alpine = Alpine
Alpine.start()
```

If you use `typescript`, you should define property Alpine for `window` object

```ts title="src/env.d.ts
interface Window {
	Alpine: import('alpinejs').Alpine
}
```