---
title: "Spawn Tty Shell"
date: 2020-07-20T22:21:32+07:00
draft: false
tags: [
    "linux",
    "command",
]
---

Seringkali selama *pentest* Anda dapat memperoleh shell tanpa tty, namun ingin berinteraksi lebih jauh dengan sistem. Berikut adalah beberapa perintah yang akan memungkinkan Anda untuk memanggil shell tty. Jelas beberapa hal ini akan tergantung pada lingkungan sistem dan paket yang diinstal.

* Python `python -c 'import pty; pty.spawn("/bin/sh")'`
* Echo : `echo os.system('/bin/bash')`
* sh : `/bin/sh -i`
* Perl : `perl —e 'exec "/bin/sh";' atau exec "/bin/sh";`
* Ruby : `exec "/bin/sh"`
* lua : `os.execute('/bin/sh')`
* From within IRB : `exec "/bin/sh"`
* From within vi : :`!bash atau :set shell=/bin/bash:shell`
* From within nmap : `!sh`