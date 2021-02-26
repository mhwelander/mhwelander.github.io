---
layout: post
title: "Pipe Sphinx Doc build results to text file"
date: 2016-12-21
categories: tech
---

I wanted to pipe the results of the Sphinx Doc build into a text file so that I could address any errors or warnings. I started with this (I’m using Windows 8.1):

```
c:\path\to\doc\root>make html > log.txt
```

When I opened the file, there were no errors or warnings listed – and it wasn’t because I’m fabulous.

It turns out that there are two output streams: `STDOUT` (Standard Out) and `STDERR` (Standard Error). The example above only redirects `STDOUT` to file. In order to redirect both streams, you need to do this:

```
c:\path\to\doc\root>make html > log.txt 2>&1
```

To write only the warnings and errors to a file, you can do this:

```
c:\path\to\doc\root>make html 2> log.txt
```

**Note**: This is not specific to Sphinx Doc; that is just the context in which I learned about `STDOUT` and `STDERR`.
