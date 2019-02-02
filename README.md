# Cheatsheets for AI

This project is heavily inspired by this project: https://github.com/rstacruz/cheatsheets

## Launch the server

```bash
bundle exec jekyll serve
```

## Install

To run it locally, you first need to install some dependencies.

node.js: https://nodejs.org/en/download/package-manager/
ruby: https://www.ruby-lang.org/en/documentation/installation/
yarn: https://yarnpkg.com/en/docs/install
bundler: https://bundler.io/
Jekyll: https://jekyllrb.com/

### Ubuntu

```bash
sudo apt-get install ruby-full

curl -sS https://dl.yarnpkg.com/debian/pubkey.gpg | sudo apt-key add -
echo "deb https://dl.yarnpkg.com/debian/ stable main" | sudo tee /etc/apt/sources.list.d/yarn.list
sudo apt-get update && sudo apt-get install yarn

sudo apt-get install nodejs

gem install bundler jekyll
```

### MacOS


### Install packages

```bash
yarn install
bundle install
env PORT=4001 yarn run dev
```
