---
layout: post
title: "Lenovo's Miix 700 and Linux"
description: ""
date: 2017-01-31
tags: [linux, fedora]
comments: true
---

I recently purchased the Miix 700-12ISK to replace my ThinkPad X230. I wanted to get something ultra portable and the Surface Pro came to mind. But it was a bit pricey for my taste. So a knock-off would work just fine. There was very little information on the Miix 700 running Linux, so I thought I'd share my findings. This isn't going to be a hardware review, but an overview of an out-of-the-box Fedora 25 install.
## What Just Worked

### Installation
First I reinstalled Windows 10 to get rid of the bloat-ware and applied Lenovo's firmware. Then to access the bios press you need to press Vol Up + Power, which let me boot from a Fedora 25 USB and install as usual. Now GRUB shows by default and I can still boot into Windows. Pretty typical install.

### Keyboard and Touchpad
Worked. It's important to do the firmware update since the keyboard use to have issues. No multi-touch gestures, but I'm sure with a little tinkering they would work.

### Wireless
No problems here, both WiFi and Bluetooth just work. Bluetooth is important since there's only 2x USB, really only 1x since the power adapter uses one.

## What Kinda Worked

### Touchscreen
The touch works, even GRUB brings up an on-screen keyboard surprisingly (LUKS didn't, so still need the keyboard on boot). But while GNOME handled touch with ease. Many applications wouldn't even bring up the on-screen keyboard. So using it as a tablet to browse the internet is a pain because you can't type. Auto-rotation surprisingly almost worked in Wayland (not X11). The display would rotate but the input wouldn't.

### Pen
Didn't work at all in Wayland. I didn't look into it too heavily because switching to X11 solved the problem.

### HiDPI
I didn't realize this before I bought it, but the screen is pretty high res for its size (2160 x 1440 for a 12" screen). While GNOME and most apps work fine. Some apps just ignore HiDPI settings so they end up looking ugly or are even unusable.

## What Didn't

### Cameras
The cameras didn't function at all. They look to be similar to the ones on the Surface Book(Multimedia controller: Intel Corporation Skylake Imaging Unit). Which there are apparently patches floating around for. I don't use a web-cam too often, so I'm satisfied until they are supported without needing a patch.

## Final Thoughts

Less painful than I imagined, was expecting less functionality. As a portable laptop, it works fine. The hardware specs are great considering it's a passively cooled tablet (which is a bonus, no annoying fan). Any really heavy lifting will be done in a remote session anyway. My biggest gripe would be the keyboard, but that's to be expected on the flimsy cover. Overall, Linux works with it pretty well and makes a good alternative to the Surface Pros.


Feel free to leave any questions or input below.