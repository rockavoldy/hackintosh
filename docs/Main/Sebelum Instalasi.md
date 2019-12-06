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
   2. Siapkan flash drive dengan kapasitas minimal 8GB, lalu format menjadi Mac OS Extended (HFS) menggunakan Disk Utility
   3. Setelah berhasil diformat, jalankan command ini di terminal:
      ```Shell
      $ sudo /Applications/Install\ macOS\ Mojave.app/Contents/Resources/createinstallmedia --volume /dev/Untitled
      ```
      NOTE:
      > Ubah lokasi folder hasil download menyesuaikan dengan lokasi folder installer yang ada di komputermu. dan nama flash drive yang sebelumnya telah diformat (defaultnya Untitled).
   4. Tunggu sampai selesai, dan ketika sudah selesai, *mount* partisi EFI dan masuk ke langkah selanjutnya, menyiapkan *bootloader* beserta konfigurasi awal agar bisa *booting* kedalam installer. <!-- TODO: link ke menyiapkan konfigurasi bootloader. -->