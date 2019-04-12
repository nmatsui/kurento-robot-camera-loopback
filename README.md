# kurento-robot-camera-loopback
This application loops back your own camera stream to your browser by using [Kurento](http://www.kurento.org/).

[![Docker image size](https://img.shields.io/microbadger/image-size/nmatsui/kurento-robot-camera-loopback.svg)](https://hub.docker.com/r/nmatsui/kurento-robot-camera-loopback/)

## Description
This Kuento application is inspired by the Kurento [magic mirror](https://github.com/Kurento/kurento-tutorial-js/tree/master/kurento-magic-mirror) sample application.

## Requirements
||version|
|:--|:--|
|kurento|6.9.0|
|nodejs|8.15|
|docker|18.09.2|

## How to build
1. `npm install`
2. `npm run build`

## Environment Variables

|env|sample value|
|:--|:--|
|`PORT`|3000|
|`APPSERVER_URL`|http://`LOCAL_IP_ADDRESS`:3000|
|`KURENTO_URL`|http://`LOCAL_IP_ADDRESS`:8888/kurento|
|`OVERLAY_IMG_PATH`|static/img/mario-wings.png|
|`STUN_LIST`||
|`TURN_LIST`||

## How to run
1. start Kurento container
    * `docker run -d -p 8888:8888 kurento/kurento-media-server:6.9.0`
2. set environment variables
3. start Loopback application
    * `node ./dist/server.js`
4. open browser the loopback page http://localhost:3000/
5. click `start` button

## License

[Apache License 2.0](/LICENSE)

## Copyright
Copyright (c) 2019 Nobuyuki Matsui <nobuyuki.matsui@gmail.com>
