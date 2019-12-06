---
title: Pendahuluan
date: 2019-04-12
slug: pendahuluan
---

## Apa itu Hackintosh?
Hackintosh adalah sistem yang dipasang dengan macOS pada sistem yang bukan keluaran dari Apple (Macbook, iMac, Mac Pro) dengan bantuan Bootloader. Singkatnya adalah menjalankan laptop atau PC yang bukan keluaran dari apple tetapi menjalankan OS yang ada khusus untuk hardware keluaran dari Apple.

> **Jika kamu malas membaca, tidak mau mencari, tidak mau mencoba, Saya tekankan Hackintosh bukan untukmu, dan sebaiknya jangan lanjut karena akan banyak bahan bacaan dan waktu yang tidak sebentar bahkan hanya untuk membuat OS bisa masuk ke dalam menu Installer.**

Sebelum lanjut, jawab beberapa pertanyaan dibawah ini:
- Processor
  - Merk apa? (Intel/AMD/Via..)
  - Model apa? (Xeon/i7/i5)
  - Generasi keberapa? (i7-7700K => generasi ke-7, Ryzen 7 2700X => Ryzen generasi ke-2)
- RAM
  - Berapa kapasitasnya?
  - Frekuensi yang digunakan? (1600MHz, 2333MHz, 2400MHz)
- Motherboard
  - untuk Desktop
    - Apa chipset yang digunakan? (Intel H100, B150, Z170)
    - Apa saja port external yang tersedia? (Video output, Audio, USB Port)
    - Apa saja interface/port internal yang tersedia? (slot M.2 beserta tipe slotnya, slot PCIe, slot SATA)
    - Apa firmware yang disupport oleh Motherboard? (UEFI, BIOS Legacy)
- Storage
  - Apa penyimpanan yang digunakan?
    - Jika SSD, apa itu NVMe atau SATA?
    - Jika Hard Disk, apa itu SATA atau PATA?
- Graphics dan Display
  - Jika desktop
    - Apa GPU yang digunakan? (Intel, Nvidia, AMD)
    - Ada berapa GPU yang tersedia? (1, 2)
  - Jika laptop
    - Apa GPU yang digunakan? (Intel, Nvidia, AMD)
    - Ada berapa GPU yang tersedia?
    - Jika lebih dari 1, apa saja? (Intel + Nvidia, Intel + AMD)
    - Jika Intel dan Nvidia, apa mendukung fitur Optimus? (fitur Optimus tidak akan berjalan di macOS, sehingga harus di disable, dan GPU AMD pada laptop tidak ada yang disupport)
  - Berapa resolusi native monitornya?
- Audio
  - Apa ada chipset onboard?
  - apa Codecnya? (pada Windows, bisa dengan tool bantuan seperti Aida64, dan pada linux, silahkan searching caranya)
- Wifi/Bluetooth
  - Apa motherboard/laptopnya terdapat WiFi?
  - Apa interface yang dipakai? (mPCIe, M.2, Half Mini)
  - Jika Laptop
    - Apa bisa diganti?
    - Apa terdapat whitelist? (HP sebelum Intel generasi ke-4 dan Lenovo menerapkan whitelist pada laptopnya)

Jika kamu bisa menjawabnya, silahkan lanjut baca, selain itu, baca-baca dan kenali lagi spesifikasi Desktop/Laptopmu sebelum lanjut.

## Spesifikasi minimal
Tidak ada spesifikasi minimal untuk bisa dan lancar menjalankan Hackintosh, yang terpenting adalah bagaimana setiap komponen hardware tersebut di support. Tetapi CPU dari Intel lebih mudah karena produk dari Apple sendiri menggunakan Intel. Untuk lebih jelasnya, silahkan ke [Supported Hardware](supported-hardware).
> Search dulu project yang sudah dilakukan orang lain, jika ada laptop atau desktop yang spesifikasinya sama, terserah apapun itu brandnya, besar kemungkinan laptop atau desktopmu juga bisa menjalankannya.


<!-- TODO: Butuh tambahan, juga riset lebih jauh untuk ini, jika punya saran, silahkan buat PR atau issues -->

## Istilah dalam Hackintosh
<!-- TODO: tambah lebih banyak Istilah, help wanted -->
- Bootloader: Program untuk menjalankan OS. Linux seperti ubuntu juga menggunakan bootloader bernama grub. Dalam hackintosh, bootloader saat ini yang masih jalan pengembangannya ada Clover dan juga OpenCore.
- ACPI Tables: Singkatnya, sebuah tabel berisi identitas dan konfigurasi Hardware yang akan dipakai oleh BIOS untuk mengenali komponen yang terpasang.
- Kext: Driver yang dipakai pada macOS untuk mengenali hardware.

## Bagaimana cara install Hackintosh?
Ada 2 versi cara penginstallan hackintosh
- Distro (seperti Niresh, iAtkos, dan sejenisnya)
- Vanilla (versi asli dari macOS, yang didapat dari App Store langsung)

dari kedua cara itu, versi Distro biasanya muncul paling pertama pada pencarian google. Mereka menawarkan OS yang telah dimodifikasi dengan klaim dapat mudah di install pada sistem apapun. Tetapi ketika muncul masalah, kamu harus menanyakan masalah itu pada mereka lagi, karena OS yang telah dimodifikasi dan tidak ada yang mengetahui modifikasi apa saja pada OS tersebut kecuali mereka. Kebanyakan forum, grup tidak mau membantu masalah pada OS Distro, karena masalah pribadi dan/atau memang tidak mengetahui masalah tersebut karena jarang terjadi atau tidak mungkin terjadi jika memang patch yang dilakukan benar.

Versi vanilla biasanya lebih sulit untuk mendapatkan installernya dan juga konfigurasi awal yang lumayan ribet. Kamu harus mengenali hardware kamu sendiri (dan itu wajib jika kamu mau install hackintosh) tetapi jika kamu menemukan masalah, bertanya pada forum atau grup biasanya akan mendapatkan jawaban, apalagi jika hardware dan komponen yang kamu pakai banyak dipakai juga. Bahkan mungkin kamu bisa menemukan orang baik hati yang sudah menginstall hackintosh pada laptop yang sama persis dari merk, model, sampai spesifikasinya dan menyimpan patch-patch yang diperlukan online.

## Dimanakah mendapatkan installer Vanilla?
Untuk mendownloadnya bisa pakai tool python [corpnewt/GibMacOS](https://github.com/corpnewt/gibMacOS) atau ke forum [Olarila](https://olarila.com).