---
title: VESC Tool에서 VESC 연결하기
author: jeongsang-ryu
date: 2026-02-01 02:33:19 +0900
categories: [Getting Started, Stage1]
tags: [vesc]
image:
  path: /assets/img/posts/vesc-tool-connect/image.png
lang: ko
lang_ref: vesc-tool-connect
---

VESC Tool을 처음 실행하고 VESC를 연결하는 과정을 정리했습니다.

![VESC Tool 연결 화면](/assets/img/posts/vesc-tool-connect/image.png)

![VESC Tool 초기화면](/assets/img/posts/vesc-tool-connect/image-1.png)
*VESC tool 초기화면*

처음 연결하면 위와 같은 화면이 표시됩니다.

## 연결 권한 설정

`Connect` 버튼을 클릭했는데 권한 문제가 나온다면 아래 명령어로 권한을 부여합니다.

```bash
# 포트는 자신의 포트 번호에 맞춰 변경합니다.
# 666은 읽기/쓰기 권한을 부여합니다.
sudo chmod 666 /dev/ttyACM0
```

이 명령어는 VESC ROS driver에서 권한 문제가 발생할 때도 동일하게 적용합니다.

> 컴퓨터에서 VESC 포트의 Manufacturer 정보를 읽어 자동으로 권한을 부여하는 방법도 있습니다.
> 참고: [https://github.com/HMCL-UNIST/unicorn-racing-stack/blob/main/INSTALLATION.md#udev-rules-setup](https://github.com/HMCL-UNIST/unicorn-racing-stack/blob/main/INSTALLATION.md#udev-rules-setup)
{: .prompt-info }

> VESC Tool 연결과 VESC ROS driver는 동시에 사용할 수 없습니다.
{: .prompt-warning }

## 마무리

이 글에서는 VESC Tool에서 VESC를 연결하는 방법과 권한 문제 해결 방법을 정리했습니다.
권한 오류가 발생하면 `chmod`로 해결할 수 있고, udev 규칙으로 자동화할 수도 있습니다.
또한 VESC Tool과 ROS driver는 동시에 연결할 수 없으니 사용 환경에 맞게 번갈아 연결해 주세요.
