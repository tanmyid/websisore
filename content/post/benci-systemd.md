---
title: "Pro Kontra Systemd"
date: 2020-05-24T22:26:12+07:00
draft: false
tags: [
    "linux",
    "daemon",
]
---

Systemd mengklaim sebagai pengganti yang baik dan modern untuk SysVinit - yang disebut daemon init. Biasanya daemon init adalah proses pertama yang dimunculkan oleh kernel dan karenanya memiliki PID # 1 dan bertanggung jawab untuk menghasilkan daemon lain yang diperlukan agar OS dapat beroperasi, mis. jaringan, cron, syslog dll.

Systemd memang mejadi kontroversi karena beberapa hal. Pertama, sebagian orang menganggap systemd tidak menghormati filosofi Unix. saya ingat ketika awal sekali mengenal Linux, bahwa Linux adalah sistem operasi yang Unix-like dan Unix terkenal dengan filosofi-nya :

1. Tugas sebuah program adalah melakukan satu hal dan melakukannya dengan baik.
2. Sistem yang besar dan kompleks merupakan gabungan dari program-program kecil yang bekerja bersama.
3. Teks adalah interface yang universal
4. Segalanya di Unix adalah file.

Beberapa kritik terhadap systemd, systemd tidak hanya menjadi init system tapi juga mengambil alih banyak fungsi. Misalnya systemd berusaha mengatur network, cron, fstab, syslog/rsyslog, dll. Artinya systemd bukanlah sebuah program yang melakukan satu hal saja, tapi banyak hal. Kemudian, systemd dikritik karena logging filenya tidak berbasis teks seperti Unix dan Linux log pada umumnya, tapi binary log file.

Daftar daemon selain systemd :
* SysVinit
* OpenRC
* Upstart
* InitNG
* cinit
* runit
* minit

Daftar distro linux yang tidak menggunakan systemd :

1. [Devuan](https://devuan.org/)
2. [Void Linux](https://voidlinux.org/)
3. [Artix](https://artixlinux.org/)
4. [Gentoo](https://gentoo.org/)
5. [Alpine](https://www.alpinelinux.org/)
6. [Slackware](https://www.slackware.com/)
7. [antiX](https://antixlinux.com/)
8. [Venomlinux](https://venomlinux.org/)
9. [PClinuxOS](https://www.pclinuxos.com/)
10. [Gobolinux](https://www.gobolinux.org/)
11. [K1SS](https://k1ss.org)
12. [Ibislinux](https://ibislinux.or.id)

Dan masih banyak lagi, tulisan ini hanya catatan semata :D