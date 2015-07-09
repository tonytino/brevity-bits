---
layout: post
title:  "No Monkey Business"
date:   2015-06-04 21:11:03
categories: template notes category1 category2
author: Bee Mo
---

This post talks about YAML Front Matter, locally serving your blog, post naming convention, highlighting code snippets (and adding numbering), and acts as a general post example.

## Key YAML Front Matter:
layout: specifies what template to use from `_layouts`
title: overrides the title within the file name when appearing on your blog
date: similar to title, overrides that date that appears on your blog
categories: should be separated by spaces
author: overrides the author name that appears on your blog
permalink: overrides what is used within the url for this post (normally the file name)

*Note: You technically don't have to have anything in your front matter block thanks to liquid templating.*

Handles are used significantly by Jekyll (check out the post.html file for example). When you surround a variable by two sets of curly braces, its value takes its place. They can also be used for logic, except that instead of two sets of curly braces, you would only have one set, each with a % and the insides (where they open), meaning you could do an if statement. To close the if statement, you will need an "endif" surrounded by the same style of handles.

Handles can be used to access variables such as those defined within the front matter (e.g. author name). A great example of how you can use logic is available within the index.html file (see the for loops regarding posts).

You’ll find this post in your `_posts` directory. Go ahead and edit it and re-build the site to see your changes. You can rebuild the site in many different ways, but the most common way is to run `jekyll serve`, which launches a web server and auto-regenerates your site when a file is updated.

To add new posts, simply add a file in the `_posts` directory that follows the convention `YYYY-MM-DD-name-of-post.ext` and includes the necessary front matter. Take a look at the source for this post to get an idea about how it works.

Jekyll also offers powerful support for code snippets:

{% highlight ruby %}
def print_hi(name)
  puts "Hi, #{name}"
end
print_hi('Tom')
#=> prints 'Hi, Tom' to STDOUT.
{% endhighlight %}

Check out the [Jekyll docs][jekyll] for more info on how to get the most out of Jekyll. File all bugs/feature requests at [Jekyll’s GitHub repo][jekyll-gh]. If you have questions, you can ask them on [Jekyll’s dedicated Help repository][jekyll-help].

[jekyll]:      http://jekyllrb.com
[jekyll-gh]:   https://github.com/jekyll/jekyll
[jekyll-help]: https://github.com/jekyll/jekyll-help
