---
title: "Delete .DS_Store recursively"
date: 2018-06-24
tags: ["handy-script", "shell-script", "bash"]
draft: false
---

1. Go to your directory

    `$ cd to/my/directory`

2. Find all `.DS_Store` files recursively and remove all

    `$ find . -name '.DS_Store' -type f -delete`


Credits: https://jonbellah.com/articles/recursively-remove-ds-store