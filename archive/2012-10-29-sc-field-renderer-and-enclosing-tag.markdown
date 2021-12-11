---
layout: post
title: "sc:FieldRenderer and EnclosingTag"
date: 2012-10-29
categories: tech
---

If you have a piece of content that requires a surrounding tag (like `h2` around a heading, or `p` around the contents of a multi-line text field), you can use `EnclosingTag` on the `FieldRenderer` control; it will not display the enclosing tag if the field is empty.

```html
<sc:FieldRenderer FieldName="Heading" EnclosingTag="h2" runat="server" />
```
Produces:

```html
<h2>My heading content</h2>
```

Strangely, it does not exist on the more specialised controls, like `sc:Text` or `sc:Link`.

