---
title: "타이어 정렬 후 서보 암을 결합해야 하는 이유"
authors: [heedo-kim, jeongsang-ryu]
date: 2026-02-03 01:07:19 +0900
categories: [build, beginner]
tags: [Chassis, servo]
image:
  path: /assets/img/posts/servo-horn-after-alignment/overview.png
lang: ko
lang_ref: servo-horn-after-alignment
---

이번 포스트에서는 **타이어 정렬 후 서보 암을 결합해야 하는 이유**를 정리했습니다.

## 적용 케이스

- 기존 샤시에 새로운 서보로 교체할 때
- 샤시를 직접 빌드하고 서보를 장착할 때

이미 다 빌드되어 사용하는 Traxxas Fiesta 사용자는 큰 영향을 받지 않을 수 있습니다.

## 예시 절차

{% include embed/youtube.html id='oBQq5EqffXY' %}

- VESC에서 서보 모터를 수동으로 조작할 수 있습니다. 이 메뉴에서 **Center**를 클릭해 서보 모터를 중앙 값으로 이동시킵니다.

![서보 센터 위치](/assets/img/posts/servo-horn-after-alignment/servo-center.png)

- 이후 앞바퀴를 직진 방향으로 맞춰, 서보가 중앙 값을 출력하는 상태에서 차량도 직진하도록 맞춥니다.

![서보 혼 결합](/assets/img/posts/servo-horn-after-alignment/horn-attach.png)

- 위 상태를 유지한 채 서보 혼을 결합합니다.

## 주의사항

위 과정을 거치지 않으면 차량이 단순히 직진하지 않는 문제를 넘어, 서보가 기계적 한계까지 작동하고 있는데 조향이 따라오지 않거나, 차량 조향 한계보다 서보가 더 꺾이는 상황이 발생할 수 있습니다. 이 경우 **서보나 조향축이 파손**될 위험이 있습니다.
