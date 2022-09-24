# Jarkom-Modul-1-B12-2022

**soal no.8**

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

**soal no.9**
terdapat laporan yang isinya pertukaran file yang dilakukan kedua mahasiswa filenya ditemukan di sini lalu kita save file tersebut dalam bentuk raw dengan nama
"[nama_file].des3"

seperti ini:

![image](https://user-images.githubusercontent.com/73664125/192090384-745303b9-857e-4aab-aa4a-7448343b787d.png)

lalu kita membuka wsl terminal dan membuat command " openssl des3 -d -in [nama_file] -out [file.txt] -k [password]

lalu akan terbuat file seperti ini 

![image](https://user-images.githubusercontent.com/73664125/192090629-6a36a850-8b14-47b9-8f6f-4d5164f24180.png)

**soal no.10**

Lalu untuk jawaban nomor 10 berupa isi yang ada fi file txt tadi

yaitu:
![image](https://user-images.githubusercontent.com/73664125/192092189-d0599007-1790-47b4-80e3-087c673838b7.png)

