VAIO-P Touchpoint Control
=========================

This repository contains two small Upstart jobs (for Ubuntu and other systems
running upstart as session init) that detect the insertion and removal of
external mouse and in turn disable and enable the built-in touchpoint/touchpad
of the 2nd-gen VAIO-P laptops.

Why?
====

VAIO-P touchpoints are notoriously broken. Even the official warranty specifies
that they may "move uncontrollably" and this is "normal operation". In practice
many VAIO-P owners resort to external mouse and disable the utterly broken
internal mouse all the time.

This tiny project makes that process automatic, whenever an external mouse is
plugged in the built-in "mouse" is automatically disabled. When the external
mouse is removed the built-in "mouse" is re-enabled.

Installation
============ 

On Ubuntu 14.04 you can just use my PPA:

```
$ sudo add-apt-repository ppa:zkrynicki/ppa
$ sudo apt-get update
$ sudo apt-get install vaiop-touchpoint-control
```

As a quick alternative to adding yet-another-ppa just clone this repository,
run 'dpkg-buildpackage' and install the resulting package on your system.
