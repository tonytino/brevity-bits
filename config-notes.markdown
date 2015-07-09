# Config File

## Inside The Config File

Variables that define your website's settings, including personal details, build details, etc. Examples include:

- Your twitter handle, email, etc., all of which usually appear in within the footer

- Your url (hostname and protocol), baseurl, title, site description

- How your markdown files are converted

A powerful example of how you can customize your site is by using the variable `permalink` to an effect like such: `permalink: pretty`.

[Jekyll's docs rock; check out more formatting styles for permalinks here.](http://jekyllrb.com/docs/permalinks/)

## Updating The Config File

When you update the config file while the server is running (i.e. jekyll serve), you need to cease the hosting and restart it (i.e. simultaneously pressing Control and C stops the hosting, if local) for the changes to take effect.


