# Ocsigen Web site

The Web site content lives in a [Git repository][repo], 
and gets served by means of the [GitHub Pages][githubpages] infrastructure.

## Pages
Pages are generated by html_of_wiki, from the wiki documentation in each project.
Any change in html files here will be overwritten. The wikis are in the `manual`
directory.

* `make local` --- generates the website with links supporting local navigation. (*For testing only!*)
* `make website` --- generates the files to upload on GitHub Pages.
* `make commit` --- `make website` + `git add` the files + `git commit -v` (opens your `$EDITOR` for editing commit message).
* `make deploy` --- `make commit` + `git push origin master`.
* `make open` --- opens `index.html` in your default web browser.

The content of the main website is not refreshed automatically (unlike individual projects).
**On each modification/addition of a .wiki file, you have to** `make deploy`.

## Blog

This repository also contains the Ocsigen blog.
We welcome contributions! Fork the repository, add a
[Markdown][markdown]-formatted article under `_posts/`, and initiate a
[pull request][githubpr].

To previsualize locally, you can use:

```
jekyll serve
```

[githubpages]: https://pages.github.com/
[githubpr]: https://help.github.com/articles/using-pull-requests/
[repo]: https://www.github.com/ocsigen/ocsigen.github.io
[markdown]: https://help.github.com/articles/github-flavored-markdown/
