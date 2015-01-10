title: getting started with hugo
created: January 10, 2015
blurb: the static-site generator
tags:
    - linux
    - golang

---

* download the hugo binary for 64 bit linux

```shell
mkdir -p archive
cd archive
wget https://github.com/spf13/hugo/releases/download/v0.12/hugo_0.12_linux_amd64.tar.gz
tar -xvf hugo_0.12_linux_amd64.tar.gz
sudo ln -s /home/matt/archive/hugo_0.12_linux_amd64/hugo_0.12_linux_amd64 /usr/local/bin/hugo
```

* setup a test site and the themes

```shell
hugo new test-site
hugo new about.md
hugo new posts/first.md
git clone --recursive https://github.com/spf13/hugoThemes themes
```

* start the server, building drafts and selecting a theme
  * the `watch` flag will automatically reload pages when they change..cool

```shell
hugo server --theme=hyde --buildDrafts --port=8080 --watch
```
