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
1. Local create `public_key` & `private_key`
2. Only `private_key` can understand `public_key`
3. Remote sends message encrypted based on `public_key`
4. Local has to use `private_key` to understand (decrypt) remote's message
## Generate a SSH key

```shell
# generate rsa key
ssh-keygen -t rsa -b 4096 -C "your_email@example.com"

# without email
ssh-keygen -t rsa -b 4096
```

The default of location **SSH Key**:
- **Windows:** `C:\Users\namnh198\.ssh`
- **Linux & MacOS:** `~/.ssh => /home/namnh198/.ssh`
### Multiple SSH Key
1. Create a key different names, e.g `id_rsa_magento_cloud`,...
2. Add to `~/.ssh/config`
   
```
Host magento_cloud
Hostname *.github.com # match with all subdomain github.com
IdentityFile ~/.ssh/id_rsa_github
User <your_username>
...
```
