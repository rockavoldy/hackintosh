---
title: "Sebelum Instalasi"
date: 06-12-2019
slug: "sebelum-instalasi"
---

## Kebutuhan Instalasi
1. Flash drive dengan kapasitas minimal 8GB.
2. Koneksi internet (Untuk keperluan mendownload macOSnya).
3. 

## Menyiapkan bootable USB
Terdapat beberapa cara untuk mendownload file macOS, diantaranya:
1. Download langsung dari App Store
   Cara ini cara paling baik untuk membuat installer macOS, tetapi harus mempunyai device yang sudah terinstall macOS (bisa apple device atau hackintosh lain). langkah-langkahnya:
   1. Download file macOS dari App Store, setelah beres maka akan muncul di /Applications sesuai versinya, dalam kasus ini saya download macOS Mojave, maka hasil download akan berada di folder /Applications/Install macOS Mojave.app/
   2. Siapkan flash drive dengan kapasitas minimal 8GB, lalu format dengan GUID Partition Map dan partisi dengan Mac OS Extended (HFS) menggunakan Disk Utility
   3. Setelah berhasil diformat, jalankan command ini di terminal:
      ```Shell
      $ sudo /Applications/Install\ macOS\ Mojave.app/Contents/Resources/createinstallmedia --volume /dev/Untitled
      ```
      NOTE:
      > Ubah lokasi folder hasil download menyesuaikan dengan lokasi folder installer yang ada di komputermu. dan nama flash drive yang sebelumnya telah diformat (defaultnya Untitled).
   4. Tunggu sampai selesai, dan ketika sudah selesai, *mount* partisi EFI dan masuk ke langkah selanjutnya, menyiapkan *bootloader* beserta konfigurasi awal agar bisa *booting* kedalam installer. <!-- TODO: link ke menyiapkan konfigurasi bootloader. -->
2. Bootable image dari Olarila
   Versi vanilla tetapi sudah dikemas dalam bentuk raw, sehingga bisa dilakukan di OS lain seperti Windows dan Linux. bedanya adalah dari Olarila lebih besar sizenya karena file dijadikan bootable tanpa dikompres. langkah-langkahnya:
   1. Download Olarila images dari sini [New Olarila Images](https://olarila.com/forum/viewtopic.php?f=51&t=10412).
   2. Extract file .raw.bz2
   3. Flash dengan menggunakan balenaEtcher (tersedia di macOS, Linux, dan Windows) ke dalam flash drive 16GB.
   4. Setelah selesai, *mount* partisi EFI dan masuk ke langkah selanjutnya, menyiapkan *bootloader* beserta konfigurasi awal agar bisa *booting* kedalam installer.
3. Distro
   Saya tidak akan menuliskan "jalan" distro disini, silahkan ke webnya masing-masing, resourcesnya mungkin lebih lengkap untuk distro itu sendiri.

## Menyiapkan Bootloader
Sekarang ini banyak pilihan bootloader untuk hackintosh, tetapi yang populer dan "mudah" untuk setidaknya booting sampai masuk ke instalasi adalah Clover, maka untuk panduan disini akan menggunakan Clover bootloader (OpenCore akan dibahas nanti di page lain).
1. Pertama, download terlebih dahulu Clover bootloader di sini [CloverHackyColor/CloverBootloader/releases](https://github.com/CloverHackyColor/CloverBootloader/releases). terdapat beberapa versi clover, ada yang berbentuk installer dengan ekstensi .pkg dan yang sudah jadi EFI Folder dengan ekstensi .zip (untuk latest release saat tulisan ini ditulis (V2-5100)).
2. Mount partisi EFI dari flash drive yang sudah dilakukan pada section **Menyiapkan bootable USB**. Terdapat beberapa cara sesuai OSnya, yaitu:
      - macOS
      terdapat tool diskutil pada terminal, langkah-langkahnya:
      1. buka terminal, ketik `diskutil list` dan akan muncul list storage yang ada di komputer, contoh dalam komputer saya seperti:
      ```Shell
      ➜  ~ diskutil list
      /dev/disk0 (internal, physical):
      #:                       TYPE NAME                    SIZE       IDENTIFIER
      0:      GUID_partition_scheme                        *500.1 GB   disk0
      1:                        EFI EFI                     209.7 MB   disk0s1
      2:                 Apple_APFS Container disk1         499.9 GB   disk0s2

      /dev/disk1 (synthesized):
      #:                       TYPE NAME                    SIZE       IDENTIFIER
      0:      APFS Container Scheme -                      +499.9 GB   disk1
                                    Physical Store disk0s2
      1:                APFS Volume macOS                   113.9 GB   disk1s1
      2:                APFS Volume Preboot                 64.1 MB    disk1s2
      3:                APFS Volume Recovery                510.4 MB   disk1s3
      4:                APFS Volume VM                      2.1 GB     disk1s4

      /dev/disk2 (external, physical):
      #:                       TYPE NAME                    SIZE       IDENTIFIER
      0:      GUID_partition_scheme                        *15.5 GB    disk2
      1:                        EFI EFI                     209.7 MB   disk2s1
      2:                  Apple_HFS Untitled                15.1 GB    disk2s2

      ➜  ~
      ```
      1. dari list diatas, bisa menentukan mana yang flash drive atau storage yang digunakan pada system, dalam kasus ini flash drive saya ada di /dev/disk2. kita akan menggunakan identifier dari setiap partisi untuk mount partisi EFI.
      2. mount partisi EFI dengan cara `sudo diskutil mount /dev/disk2s1`. dari command disamping, maksud dari `/dev/disk2s1` adalah lokasi si partisi itu, sesuaikan dengan partisi hasil dari `diskutil list` kamu.
      3. setelah di mount, buka di Finder, lalu 
<!-- TODO: menyiapkan folder EFI Clover -->