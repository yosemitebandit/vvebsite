title: ssl setup
created: February 12, 2013
blurb: 443's the way to be
tags:
    - servers
    - drafts

css:
    - bootstrap.min.css
---

I keep forgetting how to do this, so here are some notes:

1. you're going to buy a comodossl cert from namecheap or something
2. your server needs a cert-signing request but first we need an associated private key: `openssl genrsa -aes256 4096 > server.key`
3. move and rename the key based on your site: `sudo mv server.key /etc/ssl/private/procession_org.key`
4. ..and protect it: `sudo chmod 400 /etc/ssl/private/procession_org.key`
5. now use the key to make a csr: `sudo openssl req -sha256 -new -key /etc/ssl/private/procession_org.key -out server.csr`
6. this opens a rare unix wizard and the trick here is to put "procession.org" or whatever as the Common Name
7. give the generated csr to the commercial provider and wait for their reply..

Hm, the [linode guide](http://library.linode.com/web-servers/nginx/configuration/ssl) is quite good.
