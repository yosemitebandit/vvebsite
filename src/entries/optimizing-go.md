title: optimizing go
created: December 22, 2014
blurb: ashish gandhi from cloudflare
tags:
    - linux
    - go
    
---

https://www.youtube.com/watch?v=JkgQJrodSpI#t=94

* part of their anti-DDOS system
* they examine User Agents and 'Referer' (hah, a misspelled part of the HTTP header that persists)
* they use kafka extensitvely, incidentally
* benchmarking results showed a ton of calls to 'external code'
* note the cpu profiler: `go test -bench=. -cpuprofile=cpu.out`
..but this was just some virtualbox artifact
* switched to vmware
* string manipulation produced a lot of garbage
