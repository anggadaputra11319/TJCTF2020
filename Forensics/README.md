# TJCTF2020 - Forensics

### Ling Ling
Pada soal Ling Ling kita hanya perlu melihat metadata pada image file tersebut. Kita dapat menggunakan online tools untuk melihat metadatanya. Saya menggunakan http://exif.regex.info/exif.cgi untuk melihat metadata image tersebut dan mendapatkan flag sebagai berikut: tjctf{ch0pln_fl4gs}


### Hexillology
Pada soal Hexillology kita membutuhkan color picker untuk melihat code hex pada setiap warna yang ada pada gambar. Saya menggunakan https://imagecolorpicker.com/ untuk melihat code hex pada setiap warna yang ada pada gambar tersebut. Pada warna pertama akan didapatkan code hex sebagai berikut: #746a63. Kemudian pada warna kedua #74667b. Pada warna ketiga #70594a. Pada warna keempat #726651. Pada warna kelima #4b3064. Pada warna keenam #626154. Dan terakhir pada warna ketujuh #50477d. Kemudian convert code hex tersebut ke ascii dan rangkai menjadi sebuah flag. Flagnya yaitu: tjctf{pYJrfQK0dbaTPG}


### Rap God
Pada soal Rap God kita diberikan sebuah audio dari BigY. Pertama untuk memproses audio tersebut kita membutuhkan audio converter to image file. Saya menggunakan https://convert.ing-now.com/mp3-audio-waveform-graphic-generator/ untuk melihat wave graphic dari audio tersebut. Setelah melakukan konversi dari audio ke spectrogram saya menemukan 10 simbol. Symbol symbol tersebut ternyata adalah wingdings font. Saya menggunakan https://lingojam.com/WingdingsTranslator untuk mendapatkan huruf dari setiap symbol tersebut dan akhirnya menemukan flagnya. Flagnya yaitu tjctf{QUICKSONIC}


