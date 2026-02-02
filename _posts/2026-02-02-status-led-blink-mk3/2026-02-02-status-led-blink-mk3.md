---
title: "현재 상태 LED로 표시하기 (blink mk3)"
author: jeongsang-ryu
date: 2026-02-02 12:00:00 +0900
categories: [build, advanced]
tags: [blink, horn]
image:
  path: /assets/img/posts/status-led-blink-mk3/overview.png
lang: ko
lang_ref: status-led-blink-mk3
---

LED로 현재 상태를 표시하는 여러 방법을 소개합니다. 최종적으로는 **Blink mk3**를 추천합니다.

저희는 팀 상징인 뿔에 현재 상태를 나타내는 LED를 넣고 싶었습니다. ForzaETH 팀을 참고했지만, 더 간단한 구성이 필요했습니다.

## 방법 1: Jetson GPIO 포트 이용하기

![Jetson GPIO 방식](/assets/img/posts/status-led-blink-mk3/method-gpio.png)

Jetson 개발자 키트는 GPIO 포트를 이용해 LED를 제어할 수 있습니다. 하지만 저희의 주력 컴퓨팅 유닛은 NUC이어서 GPIO 포트가 없습니다. 그래서 USB 포트로 제어할 수 있는 방법이 필요했습니다.

## 방법 2: 아두이노 이용하기

![아두이노 방식](/assets/img/posts/status-led-blink-mk3/method-arduino.png)

USB를 아두이노에 연결하고, 아두이노에서 LED를 제어하는 방식도 있습니다. ForzaETH는 이 방식을 사용하는 것으로 알려져 있습니다.

다만 구성 요소가 늘어나고 복잡해져서, 저희는 USB로 직접 연결되는 LED를 찾았습니다.

## 방법 3: blink 사용하기 (our method)

![Blink mk3 방식](/assets/img/posts/status-led-blink-mk3/method-blink.png)

USB 형식의 LED는 많지만, 개발자용 API나 드라이버를 제공하는 제품은 많지 않습니다. 여러 제품을 확인한 뒤 **Blink mk3**를 사용하기로 했습니다.

Blink는 ROS 드라이버까지 제공하므로 구현이 간편합니다. 뿔은 3D 프린팅으로 별도 설계가 필요합니다.

## 참고자료

- [https://github.com/HMCL-UNIST/unicorn-racing-stack/tree/main/sensors/blink](https://github.com/HMCL-UNIST/unicorn-racing-stack/tree/main/sensors/blink)
- [https://www.amazon.com/ThingM-Blink-USB-RGB-BLINK1MK3/dp/B07Q8944QK?th=1](https://www.amazon.com/ThingM-Blink-USB-RGB-BLINK1MK3/dp/B07Q8944QK?th=1)
- [https://wiki.ros.org/blink1](https://wiki.ros.org/blink1)
- [https://bitbucket.org/castacks/blink1_node/src/master/](https://bitbucket.org/castacks/blink1_node/src/master/)
