# Blog Guide

## Creating a New Blog Post

1. Copy the template file: `_posts/TEMPLATE.md`
2. Rename it with the format: `YYYY-MM-DD-your-post-title.md`
3. Update the front matter:
   - `title`: Your post title
   - `date`: Publication date (YYYY-MM-DD)
   - `permalink`: URL path for the post
   - `tags`: List of relevant tags
   - `read_time`: Set to `true` to show reading time

4. Write your content in Markdown
5. Save the file in the `_posts/` directory

## Example

```markdown
---
title: "My First Blog Post"
date: 2025-01-20
permalink: /posts/2025/01/my-first-blog-post/
tags:
  - AI
  - research
  - machine learning
read_time: true
---

Your content here...
```

## Blog Page

The blog page is available at `/blog/` and automatically lists all posts from newest to oldest.

## Features

- Automatic reading time calculation
- Tag support
- Responsive design
- Beautiful card-based layout
- Smooth animations and hover effects
