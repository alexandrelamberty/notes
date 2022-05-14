---
author: Alexandre Lamberty
title: Jq
description: JSON processor
category: Software
tags: [json, processor, linux]
created: 2021-10-23T20:38:59+02:00
updated: 2021-10-23T20:38:59+02:00
---

# Jq

# Sorting

```bash
cat plant_types.json | jq  -c 'sort_by(.name)' | jq
```

## References
