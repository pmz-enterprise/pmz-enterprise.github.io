# Writing a blog post

Create a Markdown file in this directory with the filename format:

```text
YYYY-MM-DD-title.md
```

Start the file with front matter, then write the post in Markdown:

```yaml
---
layout: post
title: Your post title
date: YYYY-MM-DD
description: A short description
tags: [research]
categories: [notes]
---
```

Posts are listed automatically on `/blog/` and are published when the change is pushed to GitHub.
