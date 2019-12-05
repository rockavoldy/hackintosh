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
      - Pentium: **TIDAK DISUPPORT**
      - Celeron: **TIDAK DISUPPORT**
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

NOTE:
> Jalur analog seperti VGA dan DVI Analog hanya di support dari Intel HD4000 sampai yang terbaru. Dan **TIDAK BISA DIPAKAI** pada Graphics card Nvidia dan AMD. maka gunakan jalur digital seperti HDMI, DVI-D, atau Display Port.

1. Intel
   - Intel GMA950: sampai 10.7.5
   - Intel X3100: sampai 10.7.5
   - Intel HD Graphics generasi pertama (codename "Arrandale"): sampai 10.13.x
   - Intel HD Graphics 2000: **TIDAK DISUPPORT**
   - Intel HD Graphics 3000: sampai 10.13.x
   - Intel HD Graphics 2500 (codename "Ivy Bridge"): **TIDAK DISUPPORT** (hanya bisa dipakai untuk QuickSync)
   - Intel HD Graphics 4000: sampai yang terbaru
   - Intel HD Graphics 4200, 4400, 4600, 5000, 5100, 5200 dan Iris: sampai yang terbaru
   - Intel HD Graphics 5300, 5500, 5600, 6000 dan Iris/Pro: sampai yang terbaru
   - Intel HD Graphics HD510 sampai 550: sampai yang terbaru
   - Intel HD Graphics P530 (dan mungkin P555 dan P580): sampai yang terbaru
   - Intel HD Graphics HD610(GT1): **TIDAK DISUPPORT**
   - Intel HD Graphics HD615 sampai HD650: sampai yang terbaru
   - Intel HD Graphics UHD620 sampai UHD655: sampai yang terbaru
   
   **SEMUA** Intel HD Graphics dari processor Atom/Celeron/Pentium **TIDAK DISUPPORT**

2. Nvidia
   - Tesla Series: 8XXX dan terbaru support sampai 10.13.x, 7XXX mungkin tidak akan lebih dari 10.11.x
   - Fermi Series: sampai 10.13.x, tetapi banyak masalah sehingga beberapa hanya sampai 10.12.x
   - Kepler: 10.8.3 - terbaru
   - Maxwell: 10.10.0 - 10.13.6 (dengan WebDriver)
   - Pascal: 10.12.4 - 10.13.6 (dengan WebDriver)
   - Turing: **TIDAK DISUPPORT**

  TLDR: Support untuk WebDriver Nvidia sudah tidak akan ada update terbaru lagi, sebaiknya gunakan AMD

3. AMD

    Detailnya bisa ke thread ini [Radeon Compatibility Guide - ATI/AMD Graphics Card](https://www.tonymacx86.com/threads/radeon-compatibility-guide-ati-amd-graphics-cards.171291/)
    <!-- TODO: alih bahasa dan sesuaikan dengan format diatas dan tambah beberapa card yang belum di cover diatas -->


## Wireless Card

INTEL, REALTEK, Ralink, Mediatek, dan lainnya **TIDAK DISUPPORT**. ***KECUALI***:
- Sampai 10.14.x:
  - PCIe/x1: 
    - BCM94360CD: native WiFi/ac dan BT4LE (3 antena) (Native, Mac card)
    - BCM94331CD: native WiFi dan BT4LE (Native, tidak disupport mulai dari 10.15, Mac card)
  - M.2 NGFF:
    - BCM943602BAED/DW1830: native WiFi/ac dan BT4LE (3 antena) (Native, NOTE: ukurannya 3042 berbeda dengan M.2 NGFF yang 2242)
    - BCM94352Z/DW1560: support WiFi/ac dan BT4LE (untuk slot dengan key A/E)
    - BCM9452Z/Lenovo Part: 04X6020: support WiFi/ac dan BT4LE (untuk slot dengan key E)
    - BCM94350ZAE/DW1820A: native WiFi/ac dan BT4LE (Banyak versi, dan banyak masalah)
  - Half Mini: 
    - BCM94360HMB/AzureWave AW-CB160H: native WiFi/ac dan BT4LE (3 antena)
    - BCM94352HMB/AzureWave AW-CE123H/DW1550: support WiFi/ac dan BT4LE
- Sampai 10.13.x:
  - BCM943224HMB: support Airport dan BT3
  - AR9285/AR5B195: 2.4GHz 54/75Mbps (bisa jalan di 10.14.x dengan sedikit patch)
  - AR9287/AR5B197: 2.4GHz 108/150Mbps (bisa jalan di 10.14.x dengan sedikit patch)
  - AR9280: 2.4/5GHz 300Mbps (native, bisa jalan di 10.14.x dengan sedikit patch)
  - AR9380: 2.4/5GHz 450Mbps (native, bisa jalan di 10.14.x dengan sedikit patch)

NOTE:
> List diatas tidak menjamin wireless card akan jalan, tergantung dari firmware wifi itu sendiri, merk laptop (beberapa merk seperti Lenvoo ada disebut Whitelist).