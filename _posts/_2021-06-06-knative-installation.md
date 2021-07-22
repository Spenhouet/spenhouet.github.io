---
layout: post
title: "Installing Knative on WSL2"
excerpt: "How I installed Knative on WSL2."
date: 2020-06-06 14:41:00 +0200
background: '/img/blog/2021-06-06-knative-installation.jpg'
credits: Photo by <a href="https://unsplash.com/@tvick?utm_source=unsplash&utm_medium=referral&utm_content=creditCopyText">Taylor Vick</a> on <a href="https://unsplash.com/s/photos/server?utm_source=unsplash&utm_medium=referral&utm_content=creditCopyText">Unsplash</a>
---

# Test

Test

* Mention book I'm following
* TODO: How to do references?

https://github.com/csantanapr/knative-minikube

https://minikube.sigs.k8s.io/docs/start/

https://knative.dev/docs/install/install-serving-with-yaml/

https://github.com/dewitt/knative-docs/blob/master/install/Knative-with-Minikube.md


https://github.com/kubernetes/minikube/issues/11574

# Issues with WSL2

```
unexpected EOF while looking for matching `"'
```


* `unexpected EOF while looking for matching ```"'` -> https://github.com/DamionGans/ubuntu-wsl2-systemd-script
* DNS -> https://gist.github.com/coltenkrauter/608cfe02319ce60facd76373249b8ca6
        https://github.com/microsoft/WSL/issues/5336#issuecomment-653881695

https://github.com/microsoft/WSL/issues/5336#issuecomment-815606920

root@spen:/mnt/c/Users/spenh# echo "nameserver 8.8.8.8" > /etc/resolv.conf
bash: /etc/resolv.conf: Operation not permitted



https://github.com/microsoft/WSL/issues/3438

<!-- spen@spen:~$ sudo apt update
Err:1 http://security.ubuntu.com/ubuntu focal-security InRelease
  Temporary failure resolving 'security.ubuntu.com'
Err:2 http://archive.ubuntu.com/ubuntu focal InRelease
  Temporary failure resolving 'archive.ubuntu.com'
Err:3 http://archive.ubuntu.com/ubuntu focal-updates InRelease
  Temporary failure resolving 'archive.ubuntu.com'
Err:4 http://archive.ubuntu.com/ubuntu focal-backports InRelease
  Temporary failure resolving 'archive.ubuntu.com'
Reading package lists... Done
Building dependency tree
Reading state information... Done
All packages are up to date.
W: Failed to fetch http://archive.ubuntu.com/ubuntu/dists/focal/InRelease  Temporary failure resolving 'archive.ubuntu.com'
W: Failed to fetch http://archive.ubuntu.com/ubuntu/dists/focal-updates/InRelease  Temporary failure resolving 'archive.ubuntu.com'
W: Failed to fetch http://archive.ubuntu.com/ubuntu/dists/focal-backports/InRelease  Temporary failure resolving 'archive.ubuntu.com'
W: Failed to fetch http://security.ubuntu.com/ubuntu/dists/focal-security/InRelease  Temporary failure resolving 'security.ubuntu.com'
W: Some index files failed to download. They have been ignored, or old ones used instead. -->