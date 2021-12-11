---
layout: post
title: "Intellisense stops working after uninstalling ReSharper"
date: 2012-10-29
categories: tech
---

My ReSharper trial ran out this morning, and despite uninstalling ReSharper (via **Control Panel > Add/Remove Programs**) and resetting my Visual Studio 2010 settings (**Tools > Import > Export Settings > Reset all settings**), intellisense refused to return – until I deleted this folder from my project root:

```
_ReSharper.MyWebsite
```

I hope that saves someone the 2 hours it took me to figure out.