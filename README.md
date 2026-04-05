# topology.work

A writing site built with Hugo, deployed to GitHub Pages.

## Stack

- [Hugo](https://gohugo.io/) — static site generator
- [GitHub Pages](https://pages.github.com/) — hosting
- [GitHub Actions](https://github.com/features/actions) — automated deploy on push
- Custom layouts and CSS — no theme

## Dependencies

- Hugo extended latest
- Git

## Set up

```
$ git clone git@github.com:kzkaed/kzkaed.github.io.git

$ cd kzkaed.github.io

$ hugo server
```

Site will be available at `http://localhost:1313`

## Hugo commands

```
hugo server                  # start dev server at localhost:1313
hugo server --buildDrafts    # include draft posts
hugo server --port 3000      # use a specific port
hugo new content posts/my-post.md   # create a new post
hugo build                   # build the site to public/
hugo --minify                # build with minified output
hugo list drafts             # list all draft posts
hugo list all                # list all content
```

## Creating content

```
$ hugo new content posts/your-post-title.md
```

Edit the file in `content/posts/`, set `draft: false` when ready to publish.

Images go in `assets/images/` and are referenced in markdown as:

```
![alt text](images/your-folder/image.png)
```

Hugo's image pipeline automatically resizes them to 680px at build time.

## Deploy

Push to `main` — GitHub Actions builds and deploys automatically.

```
$ git add .
$ git commit -m "your message"
$ git push
```
