# TJCTF2020


### Cirles
Pada soal Circles disediakan gambar lingkaran yang tiap lingkaran memiliki pola dan maknanya sendiri. Untuk mendapatkan flag pada soal ini kita perlu mengidentifikasi pola setiap lingkaran dan pada 5 lingkaran pertama memiliki makna tjctf. Setelah diperhatikan maka flagnya berupa tjctf{???#??f#?_f??t}.
Saya menggunakan online tools word detector http://worddetector.com untuk mencari kata yang tepat untuk flag tersebut dan saya menemukan kata yang paling tepat yaitu beautiful_font. Namun beautiful_font bukanlah flagnya. Setelah itu saya mencoba melakukan substitusi ke setiap karakter dan akhirnya menemukan flag sebagai berikut: tjctf{B3auT1ful_f0Nt}

### Speedrunner
Pada soal Speedrunner kita hanya perlu melakukan dekrip dengan metode Caesar cipher. Saya menggunakan https://cryptii.com/ untuk mencari flagnya dengan mencoba kunci 1-26, saya mendapatkan flagnya pada kunci ke 17. Flagnya yaitu: TJCTF{NEW_TECH_NEW_TECH_GO_FAST_GO_FAST}

### Tap Dancing
Pada soal Tap Dancing diberikan dance move berupa code morse berikut: 1101111102120222020120111110101222022221022202022211.Kita hanya perlu melakukan dekripsi pada code tersebut. Saya menggunakan https://www.dcode.fr/morse-code untuk melakukan dekripsi dan hasil dari dekripsi itu yaitu M0RSEN0TB4SE3. Flagnya yaitu: tjctf{M0RSEN0TB4SE3}


### Typewriter
Pada soal Typewriter ini kita diberikan flag yang telah dienkripsi.
Berikut flag tersebut: zpezy{ktr_gkqfut_hxkhst_tyukokkgotyt_hoftqhhst_ykxoz_qxilrtxiyf}. Hint yang ada yaitu a menjadi q, b menjadi w, c menjadi e, dan seterusnya. Kita dapat melihat keyboard kita yang awalnya QWERTYUIOP berubah menjadi ABCDEFGHIJ dan seterusnya berarti kita hanya perlu melakukan replace pada setiap huruf pada flag yang telah dienkripsi. Hasil dekripsi flagnya yaitu:
tjctf{red_orange_purple_efgrirroefe_pineapple_fruit_auhsdeupfn}


### Titanic
Pada soal Titanic hal pertama yang saya lakukan untuk mendapatkan flagnya yaitu dengan mendownload subtitle film Titanic 1997 dalam bahasa inggris. Kemudian saya melakukan hashing pada setiap kata yang ada pada teks subtitle yang telah didownload. Hint yang diberikan pada soal yaitu semua kata yang ada pada flag itu dalam bentuk lowercase. Saya menemukan satu kata yang hasil hashnya sama dengan yang diberikan oleh soal. Flagnya yaitu tjctf{marlborough's}


### Is This Crypto?
Pada soal “Is This Crypto?” kita diberikan cipher teks. Untuk dapat menemukan flagnya kita dapat menggunakan metode XOR File. Saya menggunakan online tools untuk mencari flag dari cipher teks tersebut. Saya menggunakan https://wiremask.eu/tools/xor-cracker/ untuk mendapatkan flagnya. File yang diinput yaitu file download (CTRL+S) dari https://static.tjctf.org/e141851decd4f7afab034c7055db229bd54011d2860ebd622302088fd4e062ae_file.txt. Kemudian didapatkan bahwa keynya yaitu 91 dan kita sudah dapat membaca teks tersebut. Flagnya yaitu tjctf{n0_th15_is_kyl3}

### RSABC
Pada soal RSABC kita diberikan cipherteks (c), totient (n), dan public exponent (e). Saya menggunakan RsaCTFTools pada python untuk mendapatkan flagnya. Command line yang dapat kita inputkan ke terminal yaitu sebagai berikut:
```sh
python3 RsaCTFTools.py –n 57772961349879658023983283615621490728299498090674385733830087914838280699121
 -e 65537 –-uncipher 36913885366666102438288732953977798352561146298725524881805840497762448828130
```
Setelah itu flagnya akan ditemukan. Flagnya yaitu tjctf{BOLm1QMWi3c}

