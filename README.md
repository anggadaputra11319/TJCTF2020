# TJCTF2020

### A First Step
Pada soal A First Step kita hanya perlu menginput flag yang telah disediakan oleh panitia sebagai poin pertama. Flagnya yaitu: tjctf{so0p3r_d0oper_5ecr3t}

### Discord
Pada soal Discord, kita hanya perlu untuk join ke discord tjctf 2020. Flagnya berada pada announcement di discord. Flagnya yaitu:tjctf{we_love_wumpus}

### Broken Button
Pada soal Broken Button kita hanya perlu melakukan inspect element (CTRL+SHIFT+C) pada firefox, kemudian cari bagian button yang memiliki class=”hidden” dan href=”...”, lalu copy nilai hrefnya dan masukkan ke url address (https://broken_button.tjctf.org/find_the_flag!.html). Flagnya akan muncul. Flagnya yaitu: tjctf{wHa1_A_Gr8_1nsp3ct0r!}

### Cirles
Pada soal Circles disediakan gambar lingkaran yang tiap lingkaran memiliki pola dan maknanya sendiri. Untuk mendapatkan flag pada soal ini kita perlu mengidentifikasi pola setiap lingkaran dan pada 5 lingkaran pertama memiliki makna tjctf. Setelah diperhatikan maka flagnya berupa tjctf{???#??f#?_f??t}.
Saya menggunakan online tools word detector http://worddetector.com untuk mencari kata yang tepat untuk flag tersebut dan saya menemukan kata yang paling tepat yaitu beautiful_font. Namun beautiful_font bukanlah flagnya. Setelah itu saya mencoba melakukan substitusi ke setiap karakter dan akhirnya menemukan flag sebagai berikut: tjctf{B3auT1ful_f0Nt}

### Speedrunner
Pada soal Speedrunner kita hanya perlu melakukan dekrip dengan metode Caesar cipher. Saya menggunakan https://cryptii.com/ untuk mencari flagnya dengan mencoba kunci 1-26, saya mendapatkan flagnya pada kunci ke 17. Flagnya yaitu: TJCTF{NEW_TECH_NEW_TECH_GO_FAST_GO_FAST}

### Forwarding
Pada soal Forwarding kita hanya perlu melakukan “cat [filename] | grep tjctf” untuk mendapatkan flagnya. Flagnya yaitu: tjctf{just_g3tt1n9_st4rt3d}

### Ling Ling
Pada soal Ling Ling kita hanya perlu melihat metadata pada image file tersebut. Kita dapat menggunakan online tools untuk melihat metadatanya. Saya menggunakan http://exif.regex.info/exif.cgi untuk melihat metadata image tersebut dan mendapatkan flag sebagai berikut: tjctf{ch0pln_fl4gs}

### Gym
Pada soal gym, pertama kita input nc p1.tjctf.org 8008 pada terminal linux. Kemudian akan muncul 7 rencana diet yang diharapkan bisa membantu Aneesh untuk menurunkan berat badan. Kita hanya perlu menginput nilai 2 3 3 3 3 3 3 pada 7 rencana diet tersebut. Setelah itu flagnya kita dapatkan. Flagnya yaitu: tjctf{w3iGht_l055_i5_d1ff1CuLt}

### Hexillology
Pada soal Hexillology kita membutuhkan color picker untuk melihat code hex pada setiap warna yang ada pada gambar. Saya menggunakan https://imagecolorpicker.com/ untuk melihat code hex pada setiap warna yang ada pada gambar tersebut. Pada warna pertama akan didapatkan code hex sebagai berikut: #746a63. Kemudian pada warna kedua #74667b. Pada warna ketiga #70594a. Pada warna keempat #726651. Pada warna kelima #4b3064. Pada warna keenam #626154. Dan terakhir pada warna ketujuh #50477d. Kemudian convert code hex tersebut ke ascii dan rangkai menjadi sebuah flag. Flagnya yaitu: tjctf{pYJrfQK0dbaTPG}

### Tap Dancing
Pada soal Tap Dancing diberikan dance move berupa code morse berikut: 1101111102120222020120111110101222022221022202022211.Kita hanya perlu melakukan dekripsi pada code tersebut. Saya menggunakan https://www.dcode.fr/morse-code untuk melakukan dekripsi dan hasil dari dekripsi itu yaitu M0RSEN0TB4SE3. Flagnya yaitu: tjctf{M0RSEN0TB4SE3}

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

### Typewriter
Pada soal Typewriter ini kita diberikan flag yang telah dienkripsi.
Berikut flag tersebut: zpezy{ktr_gkqfut_hxkhst_tyukokkgotyt_hoftqhhst_ykxoz_qxilrtxiyf}. Hint yang ada yaitu a menjadi q, b menjadi w, c menjadi e, dan seterusnya. Kita dapat melihat keyboard kita yang awalnya QWERTYUIOP berubah menjadi ABCDEFGHIJ dan seterusnya berarti kita hanya perlu melakukan replace pada setiap huruf pada flag yang telah dienkripsi. Hasil dekripsi flagnya yaitu:
tjctf{red_orange_purple_efgrirroefe_pineapple_fruit_auhsdeupfn}

### Login
Pada soal Login kita diberika sebuah website dan kita perlu login ke website tersebut. Namun untuk mendapatkan flagnya kita hanya perlu melihat script yang tersedia. Pertama kita buka inspect element untuk melihat scriptnya. Pada inspect element tersebut kita mendapat sebuah kata yang dihash dengan algoritma MD5 kemudian passwordnya tersebut harus ditambah dengan +890898. Saya menggunakan https://www.md5online.org/md5-decrypt.html untuk mendecrypt kata yang telah dihash tersebut dan mendapatkan kata “inevitable”. Sehingga flagnya adalah tjctf{inevitable890898}

### Sarah Palin Page 
Pada soal Sarah Palin Page kita hanya perlu memasuki laman VIP area untuk mendapatkan flagnya. Namun kita harus melakukan like terhadap top 10 moments untuk mendapatkan akses ke VIP area. Kita hanya perlu melihat browser cookies dan melihat value dari “data”. Value dari “data” tersebut diencode dengan base64. Jika kita memanipulasi valuenya, semua boolean menjadi true dan melakukan encode ulang pada JSON maka kita dapat mengakses VIP area. Setelah dapat mengakses VIP area maka flagnya ditemukan. Flagnya yaitu: tjctf{wkDd2Pi4rxiRaM5lOcLo979rru8MFqVHKdTqPBm4k3iQd8n0sWbBkOfuq9vDTGN9suZgYlH3jq6QTp3tG3EYapzsTHL7ycqRTP5Qf6rQSB33DcQaaqwQhpbuqPBm4k3iQd8n0sWbBkOf}

### Titanic
Pada soal Titanic hal pertama yang saya lakukan untuk mendapatkan flagnya yaitu dengan mendownload subtitle film Titanic 1997 dalam bahasa inggris. Kemudian saya melakukan hashing pada setiap kata yang ada pada teks subtitle yang telah didownload. Hint yang diberikan pada soal yaitu semua kata yang ada pada flag itu dalam bentuk lowercase. Saya menemukan satu kata yang hasil hashnya sama dengan yang diberikan oleh soal. Flagnya yaitu tjctf{marlborough's}

### Chord Encoder
Pada soal Chord Encoder kita harus melakukan konversi https://static.tjctf.org/c29857b8d4d1b2dfe502b5053d73844a08358ae681b2af8de6829b765dc2c28e_notes.txt menjadi notes.txt, lalu notes.txt tersebut dikonversi berdasarkan chords.txt atau https://static.tjctf.org/67be5bd036a4be8323314d1da6ad2e673963f76634a62ec47d53fb07a04a3722_chords.txt sehingga didapatkan song.txt. Lalu jalankan chord_encoder.py yang disediakan dan flagnya ditemukan. Flagnya yaitu: flag{zats_wot_1_call_a_meloD}

### Rap God
Pada soal Rap God kita diberikan sebuah audio dari BigY. Pertama untuk memproses audio tersebut kita membutuhkan audio converter to image file. Saya menggunakan https://convert.ing-now.com/mp3-audio-waveform-graphic-generator/ untuk melihat wave graphic dari audio tersebut. Setelah melakukan konversi dari audio ke spectrogram saya menemukan 10 simbol. Symbol symbol tersebut ternyata adalah wingdings font. Saya menggunakan https://lingojam.com/WingdingsTranslator untuk mendapatkan huruf dari setiap symbol tersebut dan akhirnya menemukan flagnya. Flagnya yaitu tjctf{QUICKSONIC}

### Is This Crypto?
Pada soal “Is This Crypto?” kita diberikan cipher teks. Untuk dapat menemukan flagnya kita dapat menggunakan metode XOR File. Saya menggunakan online tools untuk mencari flag dari cipher teks tersebut. Saya menggunakan https://wiremask.eu/tools/xor-cracker/ untuk mendapatkan flagnya. File yang diinput yaitu file download (CTRL+S) dari https://static.tjctf.org/e141851decd4f7afab034c7055db229bd54011d2860ebd622302088fd4e062ae_file.txt. Kemudian didapatkan bahwa keynya yaitu 91 dan kita sudah dapat membaca teks tersebut. Flagnya yaitu tjctf{n0_th15_is_kyl3}

### RSABC
Pada soal RSABC kita diberikan cipherteks (c), totient (n), dan public exponent (e). Saya menggunakan RsaCTFTools pada python untuk mendapatkan flagnya. Command line yang dapat kita inputkan ke terminal yaitu sebagai berikut:
Python3 RsaCTFTools.py –n 57772961349879658023983283615621490728299498090674385733830087914838280699121
 -e 65537 –-uncipher 36913885366666102438288732953977798352561146298725524881805840497762448828130

Setelah itu flagnya akan ditemukan. Flagnya yaitu tjctf{BOLm1QMWi3c}

### Gamer W
Pada soal Gamer W kita direkomendasikan untuk menggunakan cetus. Cetus berfungsi untuk memanipulasi value dari suatu memory yang tersimpan. Hal pertama yang kita lakukan untuk mendapatkan flagnya yaitu dengan memanipulasi value dari darah player. Caranya sebagai berikut pertama kita berpindah ke ruangan bagian kiri (untuk melawan musuh) lalu kita search value health point dengan comparison operator EQ dan value types f32. Setelah itu biarkan musuh melakukan serangan terhadap kita dan search kembali value health point namun comparison operatornya diubah menjadi LT. Setelah itu pilih hasil search yang sesuai dengan value health point. Lalu buka bookmarks dan freeze value health point tersebut. Cheat HP telah diaktifkan. Kemudian lawan semua musuh selain boss untuk mendapatkan gold. Lalu dengan cara yang sama kita akan mengaktifkan cheat gold. Caraya yaitu dengan pergi ke shop lalu search value gold saat ini dengan comparison operator EQ dan value type f32. Kemudian beli sesuatu sehingga gold berkurang. Lalu cari kembali value gold namun comparison operatornya diubah menjadi LT. Sama seperti cheat HP, kita akan mencentang freeze pada bookmarks value gold. Setelah itu upgrade semua stat player hingga maksimal. Kemudian aktifkan kembali cheat HP dengan cara mencentang freeze pada bookmarks value HP. Lawan Bossnya hingga dengan cara menyerang terus hingga bossnya meminum potion merah dan saat itu juga tekan tombol P agar kita teleport ke tempat shop. Jika tidak maka boss akan memindahkan kita dan membuat dinding yang tidak dapat dilewati. Namun karena kita sudah teleport duluan maka dia tidak akan melakukan hal tersebut. Lalu kita hanya perlu menyerang bossnya dan flagnya akan muncul. Flagnya yaitu tjctf{c3tus_del3tus_ur_m3ms_g0ne}.
