---
title: "Why You Should Attach the Servo Horn After Wheel Alignment"
authors: [heedo-kim, jeongsang-ryu]
date: 2026-02-03 01:07:19 +0900
categories: [build, beginner]
tags: [Chassis, servo]
image:
  path: /assets/img/posts/servo-horn-after-alignment/overview.png
lang: en
lang_ref: servo-horn-after-alignment
---

This post explains **why the servo horn should be attached after wheel alignment**.

## When this applies

- Replacing the servo on an existing chassis
- Building a chassis from scratch and installing a servo

If you are using a pre-built Traxxas Fiesta, this may not be critical.

## Example steps

{% include embed/youtube.html id='oBQq5EqffXY' %}

- You can manually move the servo motor in VESC. Click **Center** in that menu to move the servo to its neutral position.

![Servo center position](/assets/img/posts/servo-horn-after-alignment/servo-center.png)

- Align the front wheels to straight ahead so the vehicle also points straight while the servo outputs its center value.

![Attach the servo horn](/assets/img/posts/servo-horn-after-alignment/horn-attach.png)

- Attach the servo horn while keeping that state.

## Caution

If you skip this process, the car may not just steer off-center. The servo can hit its mechanical limit while the steering is still not aligned, or the servo may turn beyond the steering limit. This can **damage the servo or steering shaft**.
