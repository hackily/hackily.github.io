---
title: "Speedlimiter"
excerpt: "Your guardian on the Pebble"
header:
  image: /assets/images/pebble-app.png
  teaser: /assets/images/pebble-app.png
sidebar:
  - title: ""
    image: /assets/images/pebble-loading.png
    image_alt: "logo"
    text: "Your guardian on the Pebble"
gallery:
  - url: /assets/images/pebble-loading.png
    image_path: assets/images/pebble-loading.png
    alt: "Loading the Speedlimiter app"
  - url: /assets/images/pebble-app.png
    image_path: assets/images/pebble-app.png
    alt: "Speedlimiter in action"
---

SpeedLimiter is an application for your Pebble smartwatch.

{% include gallery caption="Images of the application in use" %}

The app will borrow the GPS on your phone to determine where you are, how fast you are going, and what the current speedlimit of the road is.

In the event that you start going over 5mph above the speedlimit, the application will cause your Pebble smartwatch to vibrate, alerting you.

The application queries the OpenMaps API to determine which road you are, and the speed limit of the road.

## Inspiration

It's very easy to accidentally speed, and sometimes it can be difficult to identify the speed limit of the road. There are times when the police may be lying in wait to catch drivers at a downhill.
Ideally, this application would warn the driver that they are going too fast, so they can drive at a safer speed.
