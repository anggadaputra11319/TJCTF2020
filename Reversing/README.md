# TJCTF2020 - Reversing

### Forwarding
Pada soal Forwarding kita hanya perlu melakukan “cat [filename] | grep tjctf” untuk mendapatkan flagnya. Flagnya yaitu: tjctf{just_g3tt1n9_st4rt3d}


### Gym
Pada soal gym, pertama kita input nc p1.tjctf.org 8008 pada terminal linux. Kemudian akan muncul 7 rencana diet yang diharapkan bisa membantu Aneesh untuk menurunkan berat badan. Kita hanya perlu menginput nilai 2 3 3 3 3 3 3 pada 7 rencana diet tersebut. Setelah itu flagnya kita dapatkan. Flagnya yaitu: tjctf{w3iGht_l055_i5_d1ff1CuLt}


### Chord Encoder
Pada soal Chord Encoder kita harus melakukan konversi https://static.tjctf.org/c29857b8d4d1b2dfe502b5053d73844a08358ae681b2af8de6829b765dc2c28e_notes.txt menjadi notes.txt, lalu notes.txt tersebut dikonversi berdasarkan chords.txt atau https://static.tjctf.org/67be5bd036a4be8323314d1da6ad2e673963f76634a62ec47d53fb07a04a3722_chords.txt sehingga didapatkan song.txt. Lalu jalankan chord_encoder.py yang disediakan dan flagnya ditemukan. Flagnya yaitu: flag{zats_wot_1_call_a_meloD}

