# TJCTF2020 - Reversing

### Forwarding
Pada soal Forwarding kita hanya perlu melakukan “cat [filename] | grep tjctf” untuk mendapatkan flagnya. Flagnya yaitu: tjctf{just_g3tt1n9_st4rt3d}


### Gym
Pada soal gym, pertama kita input nc p1.tjctf.org 8008 pada terminal linux. Kemudian akan muncul 7 rencana diet yang diharapkan bisa membantu Aneesh untuk menurunkan berat badan. Kita hanya perlu menginput nilai 2 3 3 3 3 3 3 pada 7 rencana diet tersebut. Setelah itu flagnya kita dapatkan. Flagnya yaitu: tjctf{w3iGht_l055_i5_d1ff1CuLt}


### Chord Encoder
Pada soal Chord Encoder kita harus melakukan konversi https://static.tjctf.org/c29857b8d4d1b2dfe502b5053d73844a08358ae681b2af8de6829b765dc2c28e_notes.txt menjadi notes.txt, lalu notes.txt tersebut dikonversi berdasarkan chords.txt atau https://static.tjctf.org/67be5bd036a4be8323314d1da6ad2e673963f76634a62ec47d53fb07a04a3722_chords.txt sehingga didapatkan song.txt. Lalu jalankan chord_encoder.py yang disediakan dan flagnya ditemukan. Flagnya yaitu: flag{zats_wot_1_call_a_meloD}

### Rap God
Pada soal Rap God kita diberikan sebuah audio dari BigY. Pertama untuk memproses audio tersebut kita membutuhkan audio converter to image file. Saya menggunakan https://convert.ing-now.com/mp3-audio-waveform-graphic-generator/ untuk melihat wave graphic dari audio tersebut. Setelah melakukan konversi dari audio ke spectrogram saya menemukan 10 simbol. Symbol symbol tersebut ternyata adalah wingdings font. Saya menggunakan https://lingojam.com/WingdingsTranslator untuk mendapatkan huruf dari setiap symbol tersebut dan akhirnya menemukan flagnya. Flagnya yaitu tjctf{QUICKSONIC}

### Is This Crypto?
Pada soal “Is This Crypto?” kita diberikan cipher teks. Untuk dapat menemukan flagnya kita dapat menggunakan metode XOR File. Saya menggunakan online tools untuk mencari flag dari cipher teks tersebut. Saya menggunakan https://wiremask.eu/tools/xor-cracker/ untuk mendapatkan flagnya. File yang diinput yaitu file download (CTRL+S) dari https://static.tjctf.org/e141851decd4f7afab034c7055db229bd54011d2860ebd622302088fd4e062ae_file.txt. Kemudian didapatkan bahwa keynya yaitu 91 dan kita sudah dapat membaca teks tersebut. Flagnya yaitu tjctf{n0_th15_is_kyl3}

### RSABC
Pada soal RSABC kita diberikan cipherteks (c), totient (n), dan public exponent (e). Saya menggunakan RsaCTFTools pada python untuk mendapatkan flagnya. Command line yang dapat kita inputkan ke terminal yaitu sebagai berikut:
```sh
python3 RsaCTFTools.py –n 57772961349879658023983283615621490728299498090674385733830087914838280699121
 -e 65537 –-uncipher 36913885366666102438288732953977798352561146298725524881805840497762448828130
```
Setelah itu flagnya akan ditemukan. Flagnya yaitu tjctf{BOLm1QMWi3c}

### Gamer W
Pada soal Gamer W kita direkomendasikan untuk menggunakan cetus. Cetus berfungsi untuk memanipulasi value dari suatu memory yang tersimpan. Hal pertama yang kita lakukan untuk mendapatkan flagnya yaitu dengan memanipulasi value dari darah player. Caranya sebagai berikut pertama kita berpindah ke ruangan bagian kiri (untuk melawan musuh) lalu kita search value health point dengan comparison operator EQ dan value types f32. Setelah itu biarkan musuh melakukan serangan terhadap kita dan search kembali value health point namun comparison operatornya diubah menjadi LT. Setelah itu pilih hasil search yang sesuai dengan value health point. Lalu buka bookmarks dan freeze value health point tersebut. Cheat HP telah diaktifkan. Kemudian lawan semua musuh selain boss untuk mendapatkan gold. Lalu dengan cara yang sama kita akan mengaktifkan cheat gold. Caraya yaitu dengan pergi ke shop lalu search value gold saat ini dengan comparison operator EQ dan value type f32. Kemudian beli sesuatu sehingga gold berkurang. Lalu cari kembali value gold namun comparison operatornya diubah menjadi LT. Sama seperti cheat HP, kita akan mencentang freeze pada bookmarks value gold. Setelah itu upgrade semua stat player hingga maksimal. Kemudian aktifkan kembali cheat HP dengan cara mencentang freeze pada bookmarks value HP. Lawan Bossnya hingga dengan cara menyerang terus hingga bossnya meminum potion merah dan saat itu juga tekan tombol P agar kita teleport ke tempat shop. Jika tidak maka boss akan memindahkan kita dan membuat dinding yang tidak dapat dilewati. Namun karena kita sudah teleport duluan maka dia tidak akan melakukan hal tersebut. Lalu kita hanya perlu menyerang bossnya dan flagnya akan muncul. Flagnya yaitu tjctf{c3tus_del3tus_ur_m3ms_g0ne}.
