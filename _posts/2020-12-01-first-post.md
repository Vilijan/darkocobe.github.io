---
title: Writing a New Post
author: Cotes Chung
date: 2019-08-08 14:10:00 +0800
categories: [Blogging, Tutorial]
tags: [writing]
---

## Naming and Path

Create a new file named `YYYY-MM-DD-TITLE.EXTENSION` and put it in the `_post/` of the root directory. Please note that the `EXTENSION` must be one of `md` and `markdown`. From `v2.4.1`, you can create sub-directories under `_posts/` to categorize posts.

## Front Matter

Basically, you need to fill the [Front Matter](https://jekyllrb.com/docs/front-matter/) as below at the top of the post:

```yaml
---
title: TITLE
date: YYYY-MM-DD HH:MM:SS +/-TTTT
categories: [TOP_CATEGORIE, SUB_CATEGORIE]
tags: [TAG]     # TAG names should always be lowercase
---
```

> **Note**: The posts' ***layout*** has been set to `post` by default, so there is no need to add the variable ***layout*** in Front Matter block.

### Timezone of date

In order to accurately record the release date of a post, you should not only setup the `timezone` of `_config.yml` but also provide the the post's timezone in field `date` of its Front Matter block. Format: `+/-TTTT`, e.g. `+0800`.

### Categories and Tags

The `categories` of each post is designed to contain up to two elements, and the number of elements in `tags` can be zero to infinity.

The list of posts belonging to the same *category*/*tag* is recorded on a separate page. At the same time, the number of these *category*/*tag* type pages is equal to the number of `categories` / `tags` elements for all posts, which means that the two number must be exactly the same.

For instance, let's say there is a post with front matter:

```yaml
categories: [Animal, Insect]
tags: bee
```

Then we should have two *category* type pages placed in folder `categories` of root and one *tag* type page placed in folder `tags`  of root:

```sh
.
├── categories
│   ├── animal.html         # a category type page
│   └── insect.html
├── tags
│   └── bee.html            # a tag type page
