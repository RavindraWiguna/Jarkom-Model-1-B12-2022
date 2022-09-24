# Jarkom-Modul-1-B12-2022

## Soal-Shift
![](.//images/FULLSOAL.png)

## Soal 1

### Wireshark filter expression
```ip.dst == monta.if.its.ac.id```

Di sini kita mencari ip yang destinasinya adalah monta.if.its.ac.id, sebenarnya tidak harus dst, ada banyak cara, ini adalah salah satunya<br>

Hasil Filter <br>
![](/images/Picture1.png)

lalu pilih salah satu dan follow, berikut contohnya <br>
![](/images/Picture2.png)

dapat dilihat servernya adalah:<br>
```nginx/1.10.3```

## Soal 2

### Wireshark filter expression
```ip.dst == monta.if.its.ac.id and http```

Melanjutkan dari soal nomor 1, karena kita mencari data detail topik yang berada pada html halaman yang dibuka, maka kita tambahkan ```and http``` untuk memfilter protokol http yang menuju ```monta.if.its.ac.id```. <br>

Hasil Filter<br>
![](/images/Picture3.png)

Lalu untuk mendapatkan laman http, kita tinggal export HTTP Object yang ada dari paket yang telah di capture <br>
![](/images/Picture4.png)

Kemudian cocokan filename tersebut dengan info yang kita dapat dari display filter, didapatkan filename ```194``` adalah laman tempat detailTopik yang dibuka, maka kita simpan html tersebut dan kita buka untuk mencari tahu judul topik TA yang dibuka<br>

![](/images/Picture5.png)

Setelah dibuka didapatkan bahwa judul TA yang dilihat adalah ```Evaluasi unjuk kerja User Space Filesystem (FUSE)```

## Soal 3

### Wireshark filter expression
```udp.dstport == 80 or tcp.dstport == 80```

Kita dapat memfilter paket-paket yang menuju port 80 dengan mengecek jika dstport == 80 baik upd maupun tcp<br>

Hasil filter<br>
![](/images/Picture6.png)

## Soal 4

### Wireshark filter expression
```udp.srcport == 21 or tcp.srcport == 21```

Serupa dengan di atas, hanya saja yang berasal, maka dari itu kita filter yang srcport == 21, baik udp maupun tcp<br>

Hasil filter<br>
![](/images/Picture7.png)

## Soal 5

### Wireshark filter expression
```udp.srcport == 443 or tcp.srcport == 443```

Serupa dengan di atas, hanya saja yang berasal dari port 443<br>

Hasil filter<br>
![](/images/Picture8.png)

## Soal 6

### Wireshark filter expression
```ip.dst == 203.160.128.158```

Jawab: 
1. Mencari ping lipi.go.id di command prompt.
2. memfilter pada display filter resource "soal3-6"

Hasil command prompt<br>
![](/images/Picture9.png)

Hasil filter<br>
![](/images/Picture10.png)

## Soal 7

### Wireshark filter expression
```src host 193.168.1.26```

1. input "ipconfig" pada command prompt untuk mencari ip kita.
2. memfilter pada capture filter wifi di wireshark

Hasil command prompt<br>
![](/images/Picture11.png)

Hasil filter<br>
![](/images/Picture12.png)

### Soal 8

Telusuri aliran paket dalam file .pcap yang diberikan, cari informasi berguna berupa percakapan antara dua mahasiswa terkait tindakan kecurangan pada kegiatan praktikum. Percakapan tersebut dilaporkan menggunakan protokol jaringan dengan tingkat keandalan yang tinggi dalam pertukaran datanya sehingga kalian perlu menerapkan filter dengan protokol yang tersebut.

Jawab:

1. Menggunakan filter TCP
2. Identifikasi karakteristik, percakapan kedua mahasiswa
3. Follow menggunakan TCP Stream
4. Didapatkan semua paket dengan tampilan seperti di bawah
5. Melakukan filter dengan port 9002, maka akan ditemukan paket yang dikirim
6. Melakukan follow TCP Stream pada paket tersebut
7. Melakukan pengecekan ulang pada flag push, didapatkan port baru, yaitu 60258, melakukan follow TCP Stream pada paket
8. Mengecek kembali port 9002 dengan flag push

![image](https://user-images.githubusercontent.com/73664125/192088822-56e0f1c7-4f7a-48c6-9142-c0f3501a8f0f.png)

### Soal 9
terdapat laporan yang isinya pertukaran file yang dilakukan kedua mahasiswa filenya ditemukan di sini lalu kita save file tersebut dalam bentuk raw dengan nama
"[nama_file].des3"

seperti ini:

![image](https://user-images.githubusercontent.com/73664125/192090384-745303b9-857e-4aab-aa4a-7448343b787d.png)

lalu kita membuka wsl terminal dan membuat command " openssl des3 -d -in [nama_file] -out [file.txt] -k [password]

lalu akan terbuat file seperti ini 

![image](https://user-images.githubusercontent.com/73664125/192090629-6a36a850-8b14-47b9-8f6f-4d5164f24180.png)

### Soal 10

Lalu untuk jawaban nomor 10 berupa isi yang ada fi file txt tadi

yaitu:
![image](https://user-images.githubusercontent.com/73664125/192092189-d0599007-1790-47b4-80e3-087c673838b7.png)

### Kendala

Belum ada kendala
