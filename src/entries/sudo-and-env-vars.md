title: preserving env vars with sudo
created: February 26, 2013
blurb: terribly clever
tags:
    - servers
    - notes
---

Saw this [SuperUser answer](http://superuser.com/a/422962/27119) 
on "preserving" environmental variables when running commands as `sudo`.
Very handy, I had to make a quick note.

I often get caught up with supervisord and my flask deployments.
Most of my flask work is configured with env vars.
But supervisord wants to run as sudo, modifying the env path..
