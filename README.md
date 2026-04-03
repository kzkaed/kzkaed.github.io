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

## Creating content

```
$ hugo new content posts/your-post-title.md
```

Edit the file in `content/posts/`, set `draft: false` when ready to publish.

## Deploy

Push to `main` — GitHub Actions builds and deploys automatically.

```
$ git add .
$ git commit -m "your message"
$ git push
```
