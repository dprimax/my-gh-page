---
title: "Remove All git Files From a Directory Recursively"
date: 2018-07-29
tags: ["handy-script", "shell-script", "bash", "git"]
draft: false
---

1. Go to your directory

    `$ cd to/my/directory`

2. Find all git related files recursively and remove all

```
( find . -type d -name ".git" \
  && find . -name ".gitignore" \
  && find . -name ".gitmodules" ) | xargs rm -rf
```

<br/><br/><br/>
*```Credits: https://stackoverflow.com/questions/4822321```*