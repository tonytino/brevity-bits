# Getting Started With Jekyll

## Installing Jekyll

You install Jekyll, you need to run the following command in your terminal (console):
{% highlight ruby %}
  gem install jekyll (if issue with permissions, have 'sudo' before 'gem')
{% endhighlight %}

## Creating A New Jekyll Site (Project)

To create a new blog website:
{% highlight ruby %}
  jekyll new [name]
{% endhighlight %}

## About Your New Project

### config.yml file
- Determines how your site is built, i.e. the guidelines.

### _includes directory
- Files that manage the consistent parts of the website, such as:
  - The Head
  - The Header
  - The Footer

### _layouts directory
- Files that manage the primary templates of your website, such as a post.

### _site directory

All files and folders that do not begin with an underscore will be built and placed into here. This is what is used for your actual site - nothing outside of this folder is accessible.

### _drafts directory

1. Create a folder called _drafts

2. Create a regular post file within this directory. Note that the default settings will not apply to this due to it existing in a different folder from `_posts`.

3. Use `jekyll serve --drafts` to serve and preview what the posts would look like.

## Hosting via GitHub Pages

### About GitHub Pages

- Allows you to host static websites (those without server-side languages) for free. These websites typically only contain HTML, CSS, and JavaScript.

- Jekyll is an exception to the statement above, as GitHub provides additional support for Jekyll websites. GitHub will take your Jekyll project and build it into a static website for you.

- You can use GitHub Pages for two types of websites: user pages and project pages.

- You are allocated one free user page website with your GitHub account, which can serve as a portfolio website or the website of an organization.

- Repositories can also have their own websites, known as project websites. This allows you to have a website for each project you create (this can be extremely powerful - open-source projects like ZURB's Foundation are built using project websites through GitHub/Jekyll).

- The URLs designated for user pages and project pages are different. The key difference is that the name of the respository will be inserted after the username and the GitHub Pages domain (e.g. "tonytino.github.io/repo-name"). However, both user pages and project websites can have custom domain names.

### Setting Up A Project Page

1. Make sure you have a GitHub account

2. Initialize a local repository

    - run `git init` within Terminal when your inside the proper working directory (that of the project)

    - run `git add .`

    - run `git commit -m "your message here"`


3. Add the repository to GitHub

    - On GitHub, create a repository for your project

    - In Terminal, set up the remotes for this project based on the repository you just made on GitHub

    - run `git push -u origin master`, assuming you're working on the master branch

4. Create a GitHub Pages branch

    - In order for GitHub to know what to host, you must create a branch that's specifically tasked with this purpose. You will not be using the master branch in this case. You must name it 'gh-pages'

    - Run `git checkout -b gh-pages`

    - Run `git push origin gh-pages`

5. Wait for GitHub Pages to build the site (rather quick, ~10 mins).

    - You must also set a baseurl within the _config.yml file of your project. Example: `baseurl: '/brevity-bits'`

    - Also, you must open up the header.html file within the _includes directory and change the homelink href value to `{{ site.baseurl }}/`. You should be able to find this in an anchor tag within the first 10 lines of the file.

    - Push your changes up for the gh-pages branch after committing `git push origin gh-pages`. Don't panic if it's not available right away like I did. :P


**When building a user page, make sure you name the repository like this: 'username.github.io'.** This is a required convention. Just about everything else is the same, except you do NOT need a gh-pages branch for your user page. Instead, you use the master branch.

If you make a GitHub account to build a user page for an organization and want to be able to contribute to it through your primary GitHub account, you must assign yourself as a contributor to such repository (Settings > Collaborators).

### Publishing a New Post

Assuming you have a draft post (and assuming you have a directory to the effective of '_draft', where you save your drafts), you can use Terminal to quickly move and rename the file.

```
mv _drafts/file-name.md _posts/2015-07-02-file-name.md
```

### Publishing a New Page

Pages can be things like your about me or contact me pages, and can be written in either html or markdown. You still put a front matter block at the top in both cases.

1. Make a new file in your root directory (e.g. contact.md)

2. Add a front matter block at the top of the file.

*Note: Remember that default variables are typically scope specific.*

### Pagination

[See Jekyll Docs.](http://jekyllrb.com/docs/pagination/)

### Common Liquid Tags

[Liquid Docs](https://github.com/Shopify/liquid/wiki/Liquid-for-Designers)

- **assign** - Assigns some value to a variable

- **capture** - Block tag that captures text into a variable

- **comment** - Block tag, comments out the text in the block

- **cycle** - Cycle is usually used within a loop to alternate between values, like colors or DOM classes.

- **for** - For loop

- **break** - Exits a for loop

- **continue** - Skips the remaining code in the current for loop and continues with the next loop

- **if** - Standard if/else block

- **include** - Includes another template; useful for partials

## Additional Resources

[Improved Code Snippets](https://demisx.github.io/jekyll/2014/01/13/improve-code-highlighting-in-jekyll.html)