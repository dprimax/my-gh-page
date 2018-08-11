---
title: "Find and Kill Process Locking on Mac's Specific Port"
date: 2018-08-11
tags: ["handy-script", "shell-script", "bash", "mac"]
draft: false
---

For example we want to kill a process locking at port `8080`<br/><br/>

1. With `netstat`

    * `$ kill -9 $(netstat -vanp tcp | grep 8080 | grep LISTEN | awk '{print $9}')`<br/><br/>

2. With `lsof` *(this command may need `sudo` operation)*

    * `$ sudo kill -9 $(echo $(lsof -i tcp:8080 | awk '{print $2}') | cut -d' ' -f 2)`

<br/><br/><br/>
*```Credits: https://stackoverflow.com/questions/3855127```*