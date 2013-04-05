title: arduino command line setup
created: April 5, 2013
blurb: compile and upload sketches from the command line with arduino 1.5.2
tags:
    - arduino
    - linux
---

My friends and I are using the new ARM-based Arduino Due for our sphere project.
To use the Due, you have to run v1.5.2 of the Arduino software.
This version also comes with some new
[command line support](https://github.com/arduino/Arduino/wiki/Arduino-IDE-1.5-from-command-line)
which seems to work well.. although it opens up a GUI and that's annoying
(asking around for a [fix](http://superuser.com/questions/578691)).

In the past I've used [ino](http://inotool.org/), and that was nice,
but the current official release of ino doesn't support Arduino v1.5.2.
[This fork](https://github.com/rogue-hack-lab/ino) *almost* works for me,
just had a small problem using it with the Leonardo.
Might also try [this idea](http://www.martyndavis.com/?p=335) for something ino-esque.

The very first step to getting Arduino 1.5.2 working on Ubuntu 12.04 was to just test the Arduino IDE.
I had the "greyed out serial port" problem.
This was solved by adding my username to the `dialout` group via:
`sudo adduser matt dialout`.
Then I had to restart my machine
(just logging in to a new terminal session wasn't working..).

Then I could compile and upload from the command line like so:

    $ arduino --verify /path/to/sketch
    $ arduino --upload /path/to/sketch

This uses the last-used values for the serial port and board.
Check the [docs](https://github.com/arduino/Arduino/wiki/Arduino-IDE-1.5-from-command-line)
for more switches.
