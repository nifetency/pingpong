# Overview [![Docker Image Status][docker-image]][docker] [![License][license-image]][license]

A cognitive assistant that recommends a side to hit the ball to during a match of pingpong.

[![Demo Video](https://img.youtube.com/vi/_lp32sowyUA/0.jpg)](https://www.youtube.com/watch?v=_lp32sowyUA)

[docker-image]: https://img.shields.io/docker/build/cmusatyalab/gabriel-pingpong.svg
[docker]: https://hub.docker.com/r/cmusatyalab/gabriel-pingpong

[license-image]: http://img.shields.io/badge/license-Apache--2-blue.svg?style=flat
[license]: LICENSE

# Installation
## Client
An Android client is available on [Google Play](https://play.google.com/store/apps/details?id=edu.cmu.cs.gabrielclient). The source code is available [here](https://github.com/cmusatyalab/gabriel-instruction/tree/master/android).

## Server
Running the server application using Docker is advised. If you want to install from source, please see [Dockerfile](Dockerfile) for details.

# How to Run
## Client
From the main activity one can add servers by name and IP/domain. Subtitles for audio feedback can also been toggled. This option is useful for devices that may not have integrated speakers (like ODG R-7).
Pressing the 'Play' button next to a server will initiate a connection to the Gabriel server at that address.


Note that the server maintains the state of the application. Therefore, one server cannot support multiple clients and the server must be restarted in between uses. In the future, it would be good to move application state to the the protobuf messages that get passed between the client and server. 
