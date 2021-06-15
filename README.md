# eScience academy page
This repo contains the starting page for eScience academy.

## New Posts
To add new posts, simply add a file in the `_posts` directory that follows the convention `YYYY-MM-DD-name-of-post.md` and include the necessary front matter (as explained [here](https://jekyll.github.io/minima/2016/05/20/welcome-to-jekyll.html)).

## Jekyll Themes
Your Pages site will use the layout and styles from the Jekyll theme you have selected in your [repository settings](https://github.com/escience-academy/escience-academy.github.io/settings). The name of this theme is saved in the Jekyll `_config.yml` configuration file. Current template used: [jekyll/minima](https://github.com/jekyll/minima)

For more information on theme selection see:
https://blog.github.com/2017-11-29-use-any-theme-with-github-pages/

## Local development
If you want to edit these pages and check your results locally, you can do so using `jekyll`. The first time you edit these pages you might need to run:
```
bundle install
```

Afterwards you can just run:
```
jekyll serve
```
(or `jekyll serve --destination TMPDIR`) if you want to use a different destination directory.

And then browse to `http://127.0.0.1:4000`

## Running jekyll in docker
It is also possible to serve the site locally from a docker container.
To do this, run this command from the repository directory:
```
docker run -v $PWD/:/srv/jekyll -e JEKYLL_VERSION=3.8 -p 4000:4000 jekyll/jekyll:3.8 jekyll serve
```
* `-v $PWD/:/srv/jekyll`: Mount the current working directory to `/srv/jekyll` inside the docker 
container. This is where the jekyll docker image expects the source files to be.
