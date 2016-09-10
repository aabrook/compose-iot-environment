# compose-iot-environment

Previously I would manage my IoT services on my own hardware but that has become unstustainable. This will build a docker environment
that I can host on any VPS and will meet my IoT needs.

#Services

## CouchDB

A document store that I use for data and as a HTML/JS app host. [http://couchdb.apache.org/] My project I have configured administrators
so an admin party will not be present

## MQTT

A queue broker that is the defacto standard for IoT devices. I use my own image as I do not want anonymous access by default. [aabrook/mqtt](https://github.com/aabrook/mqtt)

## Subscribers

A service that has subscribed to the queue and will forward data into couchdb. This was the biggest pain with my own infrastructure so
getting it online should improve stability. [aabrook/mqtt-subscribers](https://github.com/aabrook/mqtt-subscribers)

## Deployer

A service that will pull/clown repositories and run an embedded script. Used to simplify CD. [aabrook/deployer](https://github.com/aabrook/deployer)

## nginx

We all know nginx, we love nginx. This acts as a proxy to my other services. [nginx](https://nginx.org/)

