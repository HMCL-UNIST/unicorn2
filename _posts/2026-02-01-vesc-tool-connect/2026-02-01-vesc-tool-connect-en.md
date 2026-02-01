---
title: Connect VESC Using VESC Tool
authors: [jeongsang-ryu, hyeongjoon-yang]
date: 2026-02-01 02:33:19 +0900
categories: [Getting Started, Stage1]
tags: [vesc]
image:
  path: /assets/img/posts/vesc-tool-connect/image.png
lang: en
lang_ref: vesc-tool-connect
---

This post summarizes how to launch VESC Tool and connect to VESC.

![VESC Tool connection screen](/assets/img/posts/vesc-tool-connect/image.png)

![VESC Tool initial screen](/assets/img/posts/vesc-tool-connect/image-1.png)
*VESC Tool initial screen*

When you connect for the first time, you should see a screen similar to the above.

## Fixing permission errors

If a permission error appears after clicking `Connect`, grant access with the command below.

```bash
# Replace the port name with your own.
# 666 grants read/write permissions.
sudo chmod 666 /dev/ttyACM0
```

You can apply the same command when VESC ROS driver reports a permission error.

> You can also use udev rules to automatically grant permissions based on the VESC port manufacturer.
> Reference: [https://github.com/HMCL-UNIST/unicorn-racing-stack/blob/main/INSTALLATION.md#udev-rules-setup](https://github.com/HMCL-UNIST/unicorn-racing-stack/blob/main/INSTALLATION.md#udev-rules-setup)
{: .prompt-info }

> You cannot use VESC Tool and the VESC ROS driver at the same time.
{: .prompt-warning }

## Summary

This post covered how to connect VESC using VESC Tool and how to fix permission errors.
You can resolve permission issues with `chmod`, or automate it with udev rules.
Also note that VESC Tool and the ROS driver cannot be connected simultaneously.
