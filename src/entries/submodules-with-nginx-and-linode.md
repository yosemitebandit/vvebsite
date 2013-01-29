title: configuring submodules with nginx and linode
created: January 28, 2012
blurb: settin up this note collection
tags:
    - nginx

css:
    - bootstrap.min.css
---

I wanted to setup a custom subdomain to serve static content on nginx and a linode.
The nginx config file looked as you might expect.

In the Linode DNS manager, I had to setup the A records.
And this last part tripped me up: I also had to delegate nameservers for the subdomain.
I made `ns5` and `ns6.linode.com` point to my new subdomain and it all worked out.
