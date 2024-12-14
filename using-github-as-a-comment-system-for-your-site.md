---
title: Using Github as a Comment system for your site
tags:
  - Web-Dev
  - SSG
published: true
createDate: 2024-07-15
---

> [!todo] In this note, we will explore both [utterances](https://github.com/utterance/utterances) and [giscus](https://github.com/giscus/giscus). However, I prefer **giscus**.
## Why choose giscus over utterances?
- giscus is actively maintained while utterances is not.
- giscus utilizes discussions, whereas utterances uses issues.
- giscus supports "reply" in comments, but utterances doesn't.
- giscus provides wrappers for popular frameworks, unlike utterances, which only uses js (requiring manual implementation, though not overly complicated).
## How to use giscus
If you are using plain JS, simply follow the [official guide](https://giscus.app/).
For those wanting to use it with Web Frameworks like React or Vue, refer to this [giscus-component](https://github.com/giscus/giscus-component).
### Migrating from utterances
To integrate **giscus** into your website, follow the instructions provided in the [official guide](https://giscus.app/).

You can convert each issue to the corresponding discussion. Make sure what you choose in the config of Mapping between posts and discussions (giscus) or issues (utterances) is consistent. In my case, I choose "page title".

> [!tip] 
> Before migrating, consider creating a new discussion with the exact name you will use for the comments. Then add some comments to that discussion. After reloading your page, you should see the comments. Remember to remove this test before migrating to avoid any conflicts. 

In each issue, an option "Convert to discussion" is available at the bottom right.

If you wish to convert multiple issues at once:
1. Ensure the issues are open.
2. Create a new label (in the label overview page — `github.com/username/your-repo/labels`), for example, "comments".
3. Return to the issues page, select all the pages you want, and then add the label "comments" to them.
4. Navigate back to the label overview page, where you will see a button "Convert to discussions" next to the label "comments".