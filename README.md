# Struktur Data H Praktikum 1 2021
## Cari Tanah
### Verdict
Terminated due to timeout
#### Bukti
![VCT](./Verdict/CariTanah.JPG)
### Penjelasan Soal
Diminta untuk menentukan ada atau tidaknya lokasi petak sesuai dengan denah yang di input
### Penjelasan Solusi



## Malur Rajin
### Verdict
Wrong Answer
#### Bukti
![VMR](./Verdict/MalurRajin.jpg)
### Penjelasan Soal
Diminta untuk menentukan jumlah buku yang malur harus pisahkan dengan diikuti nama buku
### Penjelasan Solusi


## Garasi Mobil Saha
### Verdict
AC saat Revisi
#### Bukti
![VGMS](./Verdict/GarasiMobilSaha.jpg)
### Penjelasan Soal
Diminta untuk menentukan apakah mobil pertama yang masuk garasi berhasil keluar ketika jadwalnya telah tiba tanpa melebihi batas mobil yang ada di garasi, dengan kata lain tidak boleh ada mobil yang masuk tanpa ada mobil yang keluar jika garasi sudah penuh
### Penjelasan Solusi
Program akan meminta untuk menginput batas test case, jumlah mobil, dan kapasitas garasi. Lalu program akan meminta jadwal masuk dari mobil dan jadwal keluar. Jika jadwal mobil masuk tidak bersamaan dengan mobil keluar ketika garasi penuh, maka `ganti_garasi` dirubah menjadi true lalu output program akan berupa *Hmm harus renovasi garasi nich*. Jika tidak, mobil yang masuk akan di masukkan ke `Mobil_baru`. Urutan mobil akan dicek, bila mobil berada di bagian terluar dan memang sudah jadwal nya keluar, mobil akan dikeluarkan. Jika ada mobil yang masuk dan garasi belum penuh, garasi akan diisi dengan mobil baru. Kedua urutan tersebut akan berulang sesuai dengan `Jam_sekarang` sampai hari habis. Jika sampai habis `ganti_garasi` berupa false, output berupa *Hore gausah renov garasi*.
### Visualisasi Solusi


## Genjil Ganap
### Verdict
AC saat revisi
#### Bukti
![VGG](./Verdict/GenjilGanap.JPG)
### Penjelasan Soal
Diminta untuk mengurutkan plat mobil Roy berdasarkan Ganjil dan Genap plat mobil, Genap di depan dan Ganjil di belakang
### Penjelasan Solusi
Pertama program akan meminta input untuk jumlah plat yang diinginkan `n`, lalu program akan meminta plat yang dimiliki sebanyak `n`. Jika plat yang dimasukkan berupa Genap, plat akan dimasukkan kedalam Queue `genap.push(plat)`, sementara jika plat berupa ganjil, plat akan dimasukkan ke Stack `ganjil.push(plat)`. Setelah semua plat dimasukkan, proses untuk mengeluarkan plat dari queue dilakukan `genap.pop()`, setelah Queue habis, baru plat dari stack dikeluarkan `ganjil.pop()`
### Visualisasi Solusi
![VSGG](./Solusi/GenjilGanapSolusi.jpg)

## Bread Problemo
### Verdict
Wrong Answer
#### Bukti
![VBP](./Verdict/BreadProblemo.JPG)
### Penjelasan Soal
Diminta untuk menggambarkan pemindahan roti oleh ibu dengan output roti yang telah dipindahkan apakah sesuai dengan permintaan Ray atau tidak
### Penjelasan Solusi
Program akan meminta `N_jumlah_roti` dan `T_banyaknya_pemindahan_roti`. Program akan membuat stack `tumpukan_ray` dan `tumpukan_kakak` lalu `N_jumlah_roti` akan di push ke `tumpukan_ray`. Program akan meminta instruksi pemindahan berdasarkan input user. Program akan meminta input berupa angka 1 dan 2.

- Bila input berupa 1, maka program akan mengecek apakah `tumpukan_ray` habis. Bila tidak habis, maka `roti_yang_dipindah` akan disamakan dengan `tumpukan_ray`, dipush ke `tumpukan_kakak` lalu `tumpukan_ray` akan mengalami *pop*.
- Input 2 sama seperti input 1, dengan perbedaan berupa `tumpukan_ray` yang mengalami *push*, dan `tumpukan_kakak` mengalami *pop*.
- Apabila instruksi yang di input bukan 1 dan 2, maka program akan keluar dari loop dengan output "*TumpukAnnya saLah!*".

Setelah diberi input ke program, program akan mengecek roti milik Ray dan kakaknya.
- Apabila `tumpukan_ray` dicek ternyata kosong, program akan mengeluarkan output "*Ray SangaT MaraH!*".

Program akan mengecek kosong nya `tumpukan_ray` dengan iterasi seperti berikut.

- Bila `tumpukan_ray` kosong, dan `tumpukan_kakak` tidak kosong, program akan output "-"
- ketika `tumpukan_ray` tidak kosong, program akan mengecek top untuk di output pada string lalu di pop

Setelah selesai, program akan mengecek `tumpukan_kakak`

- Bila `tumpukan_kakak` kosong, program akan output ":("
- Bila tumpukan kakak tidak kosong, program akan output top dari `tumpukan_kakak`, lalu di pop.



## Nadut & Cayo
### Verdict
Wrong Answer
#### Bukti
![VN&C](/Verdict/Nadut&Cayo.JPG)
### Penjelasan Soal
Diminta untuk menyusun balok berdasarkan angka, jika angka sebelumnya lebih kecil, angka sebelum nya sampai angka pertama dihapus dan diganti dengan angka yang baru
### Penjelasan Solusi
Program akan meminta input berupa banyaknya Testcase, Banyak Digit yang diinginkan, dan isi dari digit berupa `buffer`. Program akan mengecek apabila `angka` tidak kosong, dan `buffer` lebih besar daripada `angka`, maka isi dari `angka` akan di keluarkan. Jika tidak, maka `buffer` akan dimasuk kan ke dalam `angka`. Jika digit yang dimasukkan sudah habis, maka `angka` akan di keluarkan 1 1 lalu di input kedalam program, lalu program akan berlanjut ke testcase selanjutnya.
