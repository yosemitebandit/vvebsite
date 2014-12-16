the start of a new blog - built with [bugle](https://github.com/yosemitebandit/bugle).


### first

    $ source ~/path/to/venv/bin/activate
    $ pip install -r requirements.txt
    $ git submodule init
    $ git submodule update


### later building / testing / deploying

    $ fab prod clean build
    $ fab prod serve
    $ fab prod deploy


### sample nginx config file

```nginx
server {
  listen 80;
  root /home/matt/notes.yosemitebandit.com/public;
  index index.html;
  server_name notes.yosemitebandit.com;
  location / {
    try_files $uri $uri/ /index.html;
  }
}
```

### other subdomain config

* linode has to know about the subdomain
* and of couse namecheap has to point to linode, but that's very normal
