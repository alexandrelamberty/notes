---
author: Alexandre Lamberty
title: Cronie
description: | 
Implementation for Cron, the time-based job scheduler in Unix-like computer
operating systems 
category: Software
tags: [cron,task,schedule,linux]
created: 2021-11-11T17:30:39+01:00
updated: 2021-11-11T17:30:39+01:00
---

# Cronie

## Schedule a new job

```bash
   /etc/
     |----- cron.d/
              | ----- 0hourly
     |----- cron.minutely/
     |----- cron.hourly/
              | ----- 0anacron
     |----- anacrontab
     |----- cron.daily/
     |----- cron.monthly/
     |----- cron.weekly/
     |----- crontab
     |----- cron.deny
```

View crontabs

```bash
crontab -l
```

Edit crontabs

```bash
crontab -e
```
