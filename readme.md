# appdaemon-rpi - [![Build Status](https://travis-ci.org/stevebargelt/appdaemon-rpi.svg?branch=master)](https://travis-ci.org/stevebargelt/appdaemon-rpi)

[@stevebargelt](http://www.twitter.com/stevebargelt)

## Raspberry Pi (2,3. Not 1 or Zero/Zero W - coming soon) AppDaemon Image

## Submodule?

I decided to have the Travis CI (via .travis.yml) grab/update the appdaemon submodule on every build.

* Pro: this image will always have the latest appdaemon bug fixes.
* Con: This image could introduce bugs from appdaemon master.

## Docker Compose Example

```
version: '3.1'
services:
  appdaemon:
    image: stevebargelt/appdaemon-rpi
    restart: always
    ports:
      - "5050:5050"
    volumes:
      - ./appdaemon/conf:/conf
      - /etc/localtime:/etc/localtime:ro
```

## What is AppDaemon?

