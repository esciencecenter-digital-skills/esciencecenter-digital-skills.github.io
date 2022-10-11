# eScience academy page
This repo **used to be** the starting page for eScience academy. Now it is:
1. archive of workshop links
2. a simple webpage with links to pages in www.esciencecenter.nl 

## Adding new links
To add new links, edit the `links.csv` file. 
Add a new line with the slug and the url (you don't need to add something to 'other_url' that is just for older workshops).

## Backup of old _posts
All data should be in `links.csv`, but if you miss anything you can always have 
a look at the old posts in the `_posts` folder [here](https://github.com/esciencecenter-digital-skills/esciencecenter-digital-skills.github.io/tree/29cf5c53fb94e9b1868b88bac0f5dde90068d63b)

## Jekyll Themes
Your Pages site will use the layout and styles from the Jekyll theme you have selected in your [repository settings](https://github.com/esciencecenter-digital-skills/esciencecenter-digital-skills.github.io/settings). The name of this theme is saved in the Jekyll `_config.yml` configuration file. Current template used: [jekyll/minima](https://github.com/jekyll/minima)

For more information on theme selection see:
https://blog.github.com/2017-11-29-use-any-theme-with-github-pages/

## Local development
If you want to edit this page and check your results locally, you can do so using `jekyll`. The first time you edit these pages you might need to run:
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
