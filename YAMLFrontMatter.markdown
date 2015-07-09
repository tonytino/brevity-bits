# Front Matter

- This is a form of YAML [LMGTFY](https://www.google.com/search?client=safari&rls=en&q=yaml&ie=UTF-8&oe=UTF-8).

- Used for information about page and its contents.

- Found at the top of every post-related file, which starts and ends with triple dash lines (referred to as the YAML Front Matter Block ("YFMB"), the front matter being whats in between the triple dash lines).

- There are predefined variables that can be used within the YFMB, each of which end with a colon, and followed by some text representing configuration settings (e.g. `layout: post`)

## Common YFMB Variables and Their Purpose

- layout
  Determines which template (found in the _layouts folder) to use

- title
  Title that is used on your blog post

- date
  Date that is used on your blog post (overrides the date used in the filename, which is the default date used on your blog post otherwise); format: YYYY-MM-DD [HH:MM:SS]

- categories
  Used for the organization of blog posts on your blog, such as if you have a search feature related to specific topics

- author
  Adds the author name to the post

- permalink
  Similar to date, overrides the title used in the filename, resulting in the url being based on the title you provide in your YFMB rather than the filename.
  *As a side note, if you include the following in your _config file, this would be based on your post's title: `permalink: /:title`*

  - [Jekyll's docs rock; check out more formatting styles for permalinks here.](http://jekyllrb.com/docs/permalinks/)

## Custom Variables

You can create custom front matter variables just by writing them inside the YFMB. For example, you could simply add `image: imageName.jpg` and it would be available for use. Note: you would have to edit your post.html file in order for you to utilize this new variable. For example, you could add the following:

```
{% if page.image %}
    <img class="" src="/img/{{ page.image }}">
{% endif %}
```

## Default Variables

[Jekyll Config Docs (Front Matter Defaults)](http://jekyllrb.com/docs/configuration/#front-matter-defaults)

If you happen to be using the same variables over and over in each post, you can make it a default by adding the following code snippet from Jekyll's docs into your _config.yml file.

```

defaults:
  -
    scope:
      path: "" # an empty string here means all files in the project
      type: "posts" # previously `post` in Jekyll 2.2.
    values:
      layout: "default"

```

*This would be responsible for containing all default variables pertaining to posts.*

Of course, **you can override these** just by redefining your defaults within the YMFB for a specific post.