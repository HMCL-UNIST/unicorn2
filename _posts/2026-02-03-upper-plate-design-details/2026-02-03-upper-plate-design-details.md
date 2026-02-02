---
title: "Upper plate 설계도 공유 및 적용 가이드"
author: yunho-lee
date: 2026-02-03 01:12:52 +0900
categories: [build, beginner]
tags: [Chassis]
image:
  path: /assets/img/posts/upper-plate-design-details/overview.png
lang: ko
lang_ref: upper-plate-design-details
---

## Upper plate 적용 시 주의사항

Upper plate는 **Serpent SRX8 GTE '23 1/8 4WD EP**와 **Traxxas 740544 Ford Fiesta ST Rally 1/10** 차량에 적용 가능한 설계를 다룹니다.

설계도는 Solidworks 기반으로 제작했으며, **SLDPRT와 STL 형식**을 공유해 두었습니다.

각 plate는 휘어짐으로 인한 센서 데이터 불확실성을 줄이기 위해 **5T~5.5T**로 설계했습니다. 3D 프린팅 시 Infill과 재료에 따라 강성이 달라지므로, 필요하다면 환경에 맞게 수정할 수 있습니다. (Infill 20%, 삼각형 패턴, ABS 기준)

BEC를 고정할 별도의 공간은 두지 않았고, Upper plate 하단에 **양면 실리콘 테이프**로 고정했습니다.

## Upper plate 적용 시 예상 모습

![Serpent SRX8 GTE '23 1/8 4WD EP](/assets/img/posts/upper-plate-design-details/srx8-plate.png)

![Traxxas 740544 Ford Fiesta ST Rally 1/10](/assets/img/posts/upper-plate-design-details/traxxas-plate.png)

## Upper plate 파일 공유

각 plate는 사용한 **Chassis**와 **PC 구성**에 따라 분류되어 있습니다.

- [Upper Plate 설계 및 장착 가이드 (SRX + NUC + VESC)]({{ site.baseurl }}/posts/upper-plate-srx-nuc-vesc/)
- [Upper Plate 설계 및 장착 가이드 (SRX + NUC + No_VESC)]({{ site.baseurl }}/posts/upper-plate-srx-nuc-no-vesc/)
- [Upper Plate 설계 및 장착 가이드 (Traxxas + Orin NX + VESC)]({{ site.baseurl }}/posts/upper-plate-traxxas-orin-nx-vesc/)
- [Upper Plate 설계 및 장착 가이드 (Traxxas + NUC + VESC)]({{ site.baseurl }}/posts/upper-plate-traxxas-nuc-vesc/)
