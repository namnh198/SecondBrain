---
title: SSH
createDate: 2024-12-15
published: true
tags:
  - Skills
  - Git
  - Docker
  - Backend
---
## How it works?
1. Local create `public_key` & `private_key` (`id_rsa`)
2. Only `private_key` can understand `public_key`
3. Remote sends message encrypted based on `public_key`
4. Local has to use `private_key` to understand (decrypt) remote's message
## Generate a SSH key

```shell
ssh-keygen -t rsa -b 4096 -C "your_email@example.com"

# without email
ssh-keygen -t rsa -b 4096
```