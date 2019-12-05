---
title: Supported Hardware
date: 2019-06-12
slug: supported-hardware
---

## Processor
1. Intel
   1. Laptop
      - Core Duo/Solo (codename "Yonah" dengan Graohics card GMA950): dari 10.4.6 - 10.6.8
      - Core 2 Series:
        - codename "Merom" dengan GMA950 atau X3100: dari 10.4.8 - 10.7.5
        - codename "Penryn" dengan X3100: dari 10.5.2 - 10.7.5
        - codenam "Penryn" selain X3100: dari 10.5.5 - 10.11.x
      - Core i Series dan beberapa Xeon mobile:
        - codename "Arrandale": dari 10.6.3 - 10.13.x
        - codename "Sandy Bridge": dari 10.6.6 - 10.13.x
        - codename "Ivy Bridge": dari 10.7.3 - 10.4.4
        - codename "Haswell": dari 10.9 - terbaru
        - codename "Broadwell": dari 10.10.2 - terbaru
        - codename "Skylake": dari 10.11 - terbaru
        - codename "Kabylake": dari 10.12.5 - terbaru
        - codename "Kabylake-R": dari 10.13.6 - terbaru
        - codename "Amberlake (seri Y)": dari 10.14.1 - terbaru
        - codename "Coffelake": dari 10.13.6 - terbaru
        - codename "Whiskeylake": dari 10.13.6 - terbaru
        - codename "Cannonlake": dari 10.13.6 - terbaru
      - Atom: dengan patch sampai Snow Leopard (10.6.8)
      - Pentium: tidak disupport
      - Celeron: tidak disupport
   2. Desktop
      - Pentium 4: dengan patch
      - Core Duo/Solo (codename "Yonah" dengan Graphics card GMA950): dari 10.4.6 - 10.6.8
      - Core 2 Series:
        - codename "Merom": dari 10.4.8 - 10.7.5
        - codename "Penryn": dari 10.5.2 - 10.7.5
        - codenam "Wolfdale": dari 10.6.1 - 10.13.x
      - Core i series:
        - codename "Lynnfield": dari 10.6.2 - 10.13.x
        - codename "Sandy Bridge": dari 10.6.6 - 10.13.x (bisa jalan di 10.14 keatas dengan tambahan Graphics Card)
        - codename "Ivy Bridge": dari 10.7.3 - 10.4.4
        - codename "Haswell": dari 10.9 - terbaru
        - codename "Broadwell": dari 10.10.2 - terbaru
        - codename "Skylake": dari 10.11 - terbaru
        - codename "Kabylake": dari 10.12.5 - terbaru
        - codename "Coffelake": dari 10.13.6 - terbaru
      - Xeon:
        - codename "Woodcrest": dari 10.4.7 - 10.7.5
        - codename "Clovertown": dari 10.4.9 - 10.7.5
        - codename "Harpertown": dari 10.5.1 - 10.11.x
        - codename "Nehalem": dari 10.5.6 - terbaru (tergantung dengan Graphics Card tambahan)
        - codename "Westmere": dari 10.6.4 - terbaru (tergantung dengan Graphics Card tambahan)
        - codename "Ivy BridgeEP": dari 10.9.1 - terbaru (tergantung dengan Graphics Card tambahan)
        - codename "Skylake-W": dari 10.13.3 - terbaru (tergantung dengan Graphics Card tambahan)
        - codename "Cascade Lake (???): mungkin akan datang di MacPro terbaru, mungkin mulai disupport dari 10.15 and later (tergantung dengan Graphics Card tambahan)
      - Pentium: Hanya CPU, membutuhkan tambahan Graphics Card. kompatibilitas mengacu pada codename di Core i series, dan membutuhkan fake CPU di bootloader
      - Celeron: Hanya CPU, membutuhkan tambahan Graphics Card. kompatibilitas mengacu pada codename di Core i series, dan membutuhkan fake CPU di bootloader
  
  Data diambil dari Mac asli, kompatibilitas mungkin berbeda, harus dicoba.

2. AMD

   Akan lebih susah daripada dengan processor Intel, tetapi bisa dengan mengikuti [Vanilla AMD-OSX](https://vanilla.amd-osx.com)
   - Work
     - AMD Ryzen (17H) dan FX CPU (15H/16H, Bulldozer dan Jaguar)
     - Native USB
     - Native Audio
     - Apple Online Services (iCloud, iMessage, Siri, dll)
   - Tidak work
     - Aplikasi 32bit
     - CPU lama tanpa SSE4.1 CPU Instruction
     - CPU Power Management
     - Internal Graphics seperti Vega 8, Vega 11.


## Graphics Card