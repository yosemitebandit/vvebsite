title: hacking tip.golang.org
created: January 14, 2015
blurb: with fitz and gerrand
tags:
    - golang

---

hacking tip.golang.org with Brad Fitzpatrick and Andrew Gerrand

https://www.youtube.com/watch?v=1rZ-JorHJEY

* hah, never even thought of connecting an external keyboard for pair programming
* the source of what they built (and I guess I wrote this too): https://github.com/golang/tools/blob/master/cmd/tipgodoc/tip.go
* nice examples of os/exec
* I later used cmd.Run() rather than cmd.Start() to make execution wait until the cmd finished
* this of course is nicely explained in the docs, the lesson being that I should've read those more carefully
before my other trial-and-error attempts
* kind of comforting that their hacked proto is just that..hacky and undocumented and hand-tested
* the whole architecture is kind of cool too: there are two "worlds" and only one of them is presented at any given time.
If golang's master changes, the second (still-hidden) world is rebuilt with those docs' changes. when this build is done,
we switch to showing this new world and destroy the old one.
* it's also a nice demo of mutexes
* and there used to be some content on the flag package, but no more
