# filfreire.com

This is the repo for my personal page [filfreire.com](https://filfreire.com)

I use [Jekyll](https://jekyllrb.com/).

For styling the blog uses [Tacit CSS framework](https://yegor256.github.io/tacit/). For hosting I use [Github Pages](https://pages.github.com/).

## How to build

```
# Make sure to have installed on your machine (bellow example for ubuntu):
sudo apt install ruby make gcc g++ ruby-dev zlib1g-dev

# install bundle
gem install bundle && bundle install

# Could be necessary to also:
sudo gem install github-pages
```

## How to run locally

```
jekyll serve

# How to run (with drafts)
jekyll serve --drafts
```

## How to run locally with docker

```
# add to .bashrc or .bash_aliases:
alias jekyll="docker run -it --rm -v $(pwd):/usr/src/app -p 4000:4000 starefossen/github-pages"
```

## Notes

Feel free to contribute with fixes for typos, grammatical errors or suggestions.

**Useful stuff for sharing posts**

Stuff to preview the "Open Graph" cards for when I share blog posts):
- [Linkedin post inspector](https://www.linkedin.com/post-inspector/inspect/),
- [Twitter post inspector](https://cards-dev.twitter.com/validator),
- [Open Graph](https://ogp.me/),
- [The Essential Meta Tags for Social Media](https://css-tricks.com/essential-meta-tags-social-media/).