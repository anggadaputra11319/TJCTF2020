# TJCTF2020 - Miscellaneous

### A First Step
Pada soal A First Step kita hanya perlu menginput flag yang telah disediakan oleh panitia sebagai poin pertama. Flagnya yaitu: tjctf{so0p3r_d0oper_5ecr3t}

### Discord
Pada soal Discord, kita hanya perlu untuk join ke discord tjctf 2020. Flagnya berada pada announcement di discord. Flagnya yaitu:tjctf{we_love_wumpus}


### Censorship
Pada soal Censorship, kita memasukkan jawaban dari pertanyaan yang ditanyakan.
Jika nilai yang benar dimasukkan, maka flag akan muncul, tetapi disensor. Jika kita memasukkan nilai non-numerik, maka kita dapat memeriksa kesalahannya.
```sh
Traceback (most recent call last):
  File "/censorship.py", line 10, in <module>
    if int(res)==rand1+rand2:
ValueError: invalid literal for int() with base 10: '12asdf'
```
Kita dapat memeriksa data yang dikirim dan diterima dalam mode debug.
```sh
from pwn import *

context.update(arch='amd64', os='linux', log_level='debug')

p = remote('p1.tjctf.org', 8003)

import re
pt = re.compile('[0-9]+ \+ [0-9]+')
_recv = p.recvrepeat(1)
mt = pt.findall(_recv)
p.sendline(str(eval(mt[0])))
p.interactive()
```
Dan akhirnya flagnya dapat kita lihat dari data yang diterima. Ternyata CENSORED pada flag sebelumnya menimpa nilai dari flag karena return value (r). Flagnya yaitu tjctf{TH3_1llum1n4ti_I5_R3aL}


