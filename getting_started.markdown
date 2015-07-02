# Getting Started With Jekyll

## Installing Jekyll

You install Jekyll, you need to run the following command in your terminal (console):
```
  gem install jekyll (if issue with permissions, have 'sudo' before 'gem')
```

## Creating A New Jekyll Site (Project)

To create a new blog website:
```
  jekyll new [name]
```

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


## Hosting via GitHub Pages

### About GitHub Pages

- Allows you to host static websites (those without server-side languages) for free. These websites typically only contain HTML, CSS, and JavaScript.

- Jekyll is an exception to the statement above, as GitHub provides additional support for Jekyll websites. GitHub will take your Jekyll project and build it into a static website for you.

- You can use GitHub Pages for two types of websites: user pages and project pages.

- You are allocated one free user page website with your GitHub account, which can serve as a portfolio website or the website of an organization.

- Repositories can also have their own websites, known as project websites. This allows you to have a website for each project you create (this can be extremely powerful - open-source projects like ZURB's Foundation are built using project websites through GitHub/Jekyll).

- The URLs designated for user pages and project pages are different. The key difference is that the name of the respository will be inserted after the username and the GitHub Pages domain (e.g. "tonytino.github.io/repo-name"). However, both user pages and project websites can have custom domain names.

### Setting Up

1. Make sure you have a GitHub account

2. Initialize a local repository

    - run `git init` within Terminal when your inside the proper working directory (that of the project)

    - run `git add .`

    - run `git commit -m "your message here"`


3. Add the repository to GitHub

    - On GitHub, create a repository for your project

    - In Terminal, set up the remotes for this project based on the repository you just made on GitHub

    - run `git push origin master`, assuming you're working on the master branch

4. Create a GitHub Pages branch

5. Wait for GitHub Pages to build the site (rather quick).