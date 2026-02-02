---
title: "VESC Servo Output 활성화 및 테스트 방법"
author: jeongsang-ryu
date: 2026-02-03 00:56:17 +0900
categories: [build, beginner]
tags: [servo, vesc]
image:
  path: /assets/img/posts/vesc-enable-servo-output/overview.png
lang: ko
lang_ref: vesc-enable-servo-output
---

이번 글에서는 VESC에서 서보 모터를 연결하고, 출력 신호가 정상적으로 나오는지 확인하는 방법을 정리했습니다.

## VESC와 서보 연결하기

VESC는 PPM 포트를 통해 5V 전압과 신호를 내보낼 수 있습니다. 해당 포트는 **JST-PH 3pin** 규격인데, 대부분의 서보는 이 형식이 아닙니다. 따라서 아래 중 하나가 필요합니다.

- 변환 커넥터 제작
- 서보 모터 케이블을 JST-PH 3pin에 맞게 재작업

![VESC 위 PPM 포트(빨간 박스)](/assets/img/posts/vesc-enable-servo-output/ppm-port.png)

서보 선이 얇아 보여도 큰 전류가 흐르므로 **고전류용 전선**을 사용하지 않으면 쉽게 탈 수 있습니다.

## VESC에서 서보 출력 테스트하기

### 테스트 영상

{% include embed/youtube.html id='E8Ni4vZ97wo' %}

**AppSettings-General - General** 탭에서 서보 출력을 활성화할지 선택할 수 있습니다.

![General 탭 설정](/assets/img/posts/vesc-enable-servo-output/general-tab.png)

**General - Controls** 탭에서 서보 제어를 테스트할 수 있습니다.

![Controls 탭 테스트](/assets/img/posts/vesc-enable-servo-output/controls-tab.png)
