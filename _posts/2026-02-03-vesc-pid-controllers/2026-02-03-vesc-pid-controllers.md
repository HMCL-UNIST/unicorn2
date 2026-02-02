---
title: "VESC PID Controllers 튜닝 가이드"
authors: [hyeongjoon-yang]
date: 2026-02-03 00:56:17 +0900
categories: [build, beginner]
tags: [motor, vesc, vesc-tools]
image:
  path: /assets/img/posts/vesc-pid-controllers/overview.png
lang: ko
lang_ref: vesc-pid-controllers
---

FOC 세팅으로 모터 제어 준비가 끝났다면, 이제 제어 정밀도를 높일 차례입니다. VESC Tool은 모터 전류를 정밀하게 제어하기 위한 PID 튜닝 도구를 제공하며, 이를 통해 모터 반응을 원하는 방향으로 조정할 수 있습니다. 이 글에서는 PID 게인 튜닝 방법과 주의사항을 정리했습니다.

## PID 튜닝이 필요한 경우

Sensorless 모터를 사용하는 경우에는 PID 튜닝을 진행하는 것을 추천합니다. Sensored 모터는 기본 설정에서도 큰 차이가 나지 않을 수 있습니다.

## 튜닝 환경 설정

- 아래 인터페이스에서 PID 게인을 튜닝할 수 있습니다.
- 왼쪽 탭의 **Data Analysis → Realtime Data → RPM**에서 변화를 관측합니다.
- 실시간 변화를 보기 위해 우측 메뉴바의 **Stream realtime data**를 활성화해야 합니다.

![PID 튜닝 인터페이스](/assets/img/posts/vesc-pid-controllers/tuning-interface.png)

## 모터 구동 방법

하단 RPM 옆의 재생 버튼으로 모터를 구동할 수 있고, 오른쪽의 **STOP** 버튼으로 정지할 수 있습니다.

![모터 구동 화면](/assets/img/posts/vesc-pid-controllers/rpm-control.png)

![잘 튜닝된 그래프의 모습](/assets/img/posts/vesc-pid-controllers/tuned-graph.png)

## PID 게인 튜닝 방법

PID 게인은 **P와 D 위주로 튜닝**하는 것을 추천합니다.

- P를 점진적으로 높여, 다양한 RPM 범위에서 반응 속도와 오버슈트를 관측합니다. 오버슈트가 심하지 않을 수준으로 조정합니다.
- D를 점진적으로 키워 큰 진동을 줄이는 방향으로 튜닝합니다.
- D가 너무 크면 잔진동에도 민감해질 수 있으므로 조금씩 키우는 것을 권장합니다.

## 주의사항

전류를 다루는 작업이기 때문에 항상 조심해야 합니다. 값을 급격하게 변화시키는 것은 지양해야 합니다.

## 마무리

PID 튜닝은 모터 제어 품질을 결정짓는 중요한 과정입니다. 튜닝이 잘 되어 있으면 차량이 명령에 빠르고 안정적으로 반응하지만, 튜닝이 부족하면 반응이 느리거나 진동이 발생할 수 있습니다. 시간을 들여 다양한 RPM 범위에서 테스트하며 최적의 게인 값을 찾는 것을 권장합니다.
