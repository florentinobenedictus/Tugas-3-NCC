# Tugas-3-NCC
## Soal 1
### 1A.
1. Buka `soal1.pcap`
2. Gunakan display filter `ip.src == 192.168.1.158` pada Wireshark
3. Export object as HTTP
4. Jika file pertama diinspect sebagai html akan mengarah ke [http://aka-cdn-ns.adtechus.com/images/ATCollapse.gif) dan halaman error yahoo [2](http://19.at.atwola.com/adlink/5113.1/395191/0/5/AdId=-3;BnId=0;itime=421506930;kvmn=93245558;kvadtc%5Fdvmktname=unknown;kvadtc%5Fdvosplt=windows%5F7;kvadtc%5Fdvbrand=mozilla;kvadtc%5Fdvtype=desktop;kvadtc%5Fdvmodel=firefox%5F%2D%5Fwindows;kvrepo%5Fdvosplt=windows%5F7;kvadtc%5Fdvosversion=NT%206%2E1;kvadtc%5Fcrmcc=UNKNOWN;kvadtc%5Fcrmnc=UNKNOWN;gdpr=0;](http://aka-cdn-ns.adtechus.com/images/ATCollapse.gif) dan halaman error yahoo [http://19.at.atwola.com/adlink/5113.1/395191/0/5/AdId=-3;BnId=0;itime=421506930;kvmn=93245558;kvadtc%5Fdvmktname=unknown;kvadtc%5Fdvosplt=windows%5F7;kvadtc%5Fdvbrand=mozilla;kvadtc%5Fdvtype=desktop;kvadtc%5Fdvmodel=firefox%5F%2D%5Fwindows;kvrepo%5Fdvosplt=windows%5F7;kvadtc%5Fdvosversion=NT%206%2E1;kvadtc%5Fcrmcc=UNKNOWN;kvadtc%5Fcrmnc=UNKNOWN;gdpr=0;](http://19.at.atwola.com/adlink/5113.1/395191/0/5/AdId=-3;BnId=0;itime=421506930;kvmn=93245558;kvadtc%5Fdvmktname=unknown;kvadtc%5Fdvosplt=windows%5F7;kvadtc%5Fdvbrand=mozilla;kvadtc%5Fdvtype=desktop;kvadtc%5Fdvmodel=firefox%5F%2D%5Fwindows;kvrepo%5Fdvosplt=windows%5F7;kvadtc%5Fdvosversion=NT%206%2E1;kvadtc%5Fcrmcc=UNKNOWN;kvadtc%5Fcrmnc=UNKNOWN;gdpr=0;)
5. Jika file kedua diinspect sebagai html akan mengarah ke [http://aka-cdn-ns.adtechus.com/images/327/Ad0St1Sz5Sq0V1Id763207.gif](http://aka-cdn-ns.adtechus.com/images/327/Ad0St1Sz5Sq0V1Id763207.gif)


### 1B.
1. Buka `soal1.pcap`
2. Gunakan display filter `ip.dst == 192.168.1.158` pada Wireshark
3. Export object as HTTP
4. Akan terdapat 2 file yang sama dengan 1A

## Soal 2
1. Buka `soal2.pcap`
2. Tanpa display filter, export object as IMF, akan terdapat 2 file yaitu `lunch next week.eml` dan `rendezvous.eml` (Jawaban No. 2)
3. Buka kedua file pada online eml viewer seperti [https://www.encryptomatic.com/viewer/](https://www.encryptomatic.com/viewer/) atau kirimkan kedua file EML melalui gmail.
5. Setelah isi kedua file dilihat, ditemukan user-user email (Jawaban No. 1)
6. Jika menggunakan online viewer (atau gmail), akan ditemukan attachment .docx `secretrendezvous.docx` (Jawaban No. 3)
7. Untuk mendapatkan isi `secretrendezvous.docx` kita perlu menggunakan gmail karena isi `secretrendezvous.docx` akan muncul dan dapat dilihat/download secara otomatis
9. Dari file tersebut, didapatkan lokasi meeting adalah **Air mancur dekat Playa del Carmen, Meksiko** (Jawaban No. 4)

### Informasi yang didapat:
1. Email
* Email Ann: sneakyg33k@aol.com
* Email pacar Ann: mistersecretx@aol.com
* Email orang yang ditolak makan siang Ann: sec558@gmail.com
2. Tanggal Email: Keduanya 10 Oktober 2009
3. Tempat Pertemuan: Air mancur dekat Playa del Carmen, Meksiko
4. (Bonus) Source soal: [Puzzle #2: Ann Skips Bail](https://blog.system32.kr/13) dari google dengan keyword `ann dercover ctf wireshark`

## Soal 3
**Display filter:** `tcp.port == 21`**
1. Buka Wireshark
2. Capture paket melalui **Adapter for loopback traffic capture**
3. Terdapat error pada PC saya akibat kurang memori sehingga ketika paket dicapture Wireshark akan not responding, tetapi hasil akan tetap tersimpan pada `C:\Users\USER\AppData\Local\Temp`
4. Gunakan `tcp.port == 21` pada display filter
5. Secara default port 21 akan terblokir, sehingga tidak ada hasil yang ditampilkan ketika display filter
6. Agar bisa mendapat hasil dari port 21, dapat digunakan FTP Server. FileZilla server distart dari XAMPP lalu tambahkan **User** dan **Shared Folder** lewat **Admin**, kemudian gunakan FileZilla sebagai client. Isi **Host** sesuai server (127.0.0.1), **Username** dan **Password** sesuai user pada server, dan **Port** 21 yaitu port default untuk FTP. Selanjutnya mulai capture lagi menggunakan Wireshark lalu tes dengan transfer data dari **Remote site** ke **Local site**
7. Stop capture paket pada Wireshark lalu cari file .pcapng yang terbuat (format wireshark_.....) kemudian gunakan `tcp.port == 21` kembali pada display filter
8. Akan ada paket yang tertangkap
