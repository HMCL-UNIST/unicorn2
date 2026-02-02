---
title: "VESC Servo Output Enable & Test Guide"
author: jeongsang-ryu
date: 2026-02-03 00:56:17 +0900
categories: [build, beginner]
tags: [servo, vesc]
image:
  path: /assets/img/posts/vesc-enable-servo-output/overview.png
lang: en
lang_ref: vesc-enable-servo-output
---

This post explains how to connect a servo to the VESC and verify that the output signal works correctly.

## Connect a servo to the VESC

VESC outputs 5V power and signal through the PPM port. The connector is **JST-PH 3-pin**, which most servos do not use. You will need one of the following:

- build an adapter cable, or
- re-terminate the servo cable to JST-PH 3-pin

![PPM port on the VESC (red box)](/assets/img/posts/vesc-enable-servo-output/ppm-port.png)

Even if the servo wires look thin, they can carry high current, so use **high-current wire** to avoid melting.

## Test servo output on the VESC

### Test video

{% include embed/youtube.html id='E8Ni4vZ97wo' %}

You can enable or disable servo output in **AppSettings-General → General**.

![General tab settings](/assets/img/posts/vesc-enable-servo-output/general-tab.png)

You can test servo control in **General → Controls**.

![Controls tab test](/assets/img/posts/vesc-enable-servo-output/controls-tab.png)
