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
- It also easy to use
## Installation

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
