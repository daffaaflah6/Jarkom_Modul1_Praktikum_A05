# Jarkom_Modul1_Praktikum_A05

MUHAMMMAD DAFFA’ AFLAH SYARIF    05111840000030 || PUTU PUTRI NATIH DEVAYANTI       05111840000163

# A. Display Filter
- Sebutkan webserver yang digunakan pada "testing.mekanis.me"!

Langkah :

Pada dislay filter, tulis `http.host  == "testing.mekanis.me"`
![1 1](https://user-images.githubusercontent.com/52326074/96357974-725f1800-112c-11eb-8bfe-91b6392ed75d.jpg)
Kemudian klik kanan di salah satu port, pilih Follow -> TCP Stream. Maka akan terlihat `Server: nginx/1.14.0 (Ubuntu)`
![1 2](https://user-images.githubusercontent.com/52326074/96357975-74c17200-112c-11eb-9959-38bb57da8ea1.jpg)

- Simpan gambar "Tim_Kunjungan_Kerja_BAKN_DPR_RI_ke_Sukabumi141436.jpg"!

Langkah :

Pada dislay filter, tulis `http contains "Tim_Kunjungan_Kerja_BAKN_DPR_RI_ke_Sukabumi141436.jpg"`
![2 1](https://user-images.githubusercontent.com/52326074/96357982-902c7d00-112c-11eb-8aeb-03c9093314e3.jpg)
Kemudian pilih File -> Expert ObjectS -> HTTP. Lalu pada text filter illih file `Tim_Kunjungan_Kerja_BAKN_DPR_RI_ke_Sukabumi141436.jpg` kemudian save
![2 2](https://user-images.githubusercontent.com/52326074/96357984-91f64080-112c-11eb-8652-2e1267277235.jpg)
Hasil download gambar sebagai berikut.
![Tim_Kunjungan_Kerja_BAKN_DPR_RI_ke_Sukabumi141436](https://user-images.githubusercontent.com/52326074/96357986-93c00400-112c-11eb-9b6a-0227d1af1358.jpg)

- Cari username dan password ketika login di "ppid.dpr.go.id"!

Langkah :

Pada display filter tulis `http.request.method == POST && http.host contains ppid.dpr.go.id`
Kemudian lihat pada HTML for UML Encoded maka akan terlihat username : `10pemuda` dan password : `guncangdunia`
![3](https://user-images.githubusercontent.com/52326074/96357988-a5a1a700-112c-11eb-8509-6f9885f31f6d.jpg)

- Temukan paket dari web-web yang menggunakan basic authentication method!

Langkah:

Pada display filter tulis `http.authbasic`. Maka akan terlihat paket dari web-web yang menggunakan basic authentication method
![4](https://user-images.githubusercontent.com/52326074/96357995-af2b0f00-112c-11eb-956f-94f57b1397e7.jpg)

- Ikuti perintah di aku.pengen.pw! Username dan password bisa didapatkan dari file .pcapng!

Langkah :

Pada display filter tulis `http.host contains "aku.pengen.pw"`. Kemudian lihat pada Hypertext Transfer Control -> Authorization -> Credentials maka akan terlihat `kakakgamtenk:hartatahtabermuda` menunjukkan username dan password untuk mengakses link `aku.pengen.pw`
![5 1](https://user-images.githubusercontent.com/52326074/96358004-c0741b80-112c-11eb-9223-a607b26a8076.jpg)
Kemudian akses link `aku.pengen.pw` dan masukkan username dan passwordnya -> `kakakgamtenk:hartatahtabermuda`
![5 2](https://user-images.githubusercontent.com/52326074/96358006-c23ddf00-112c-11eb-8507-be59d48645ba.jpg)
Lalu akan terbuka websitenya dan diminta untuk menjawab pertanyaan dan mengisinya pada kolom tertera. Pertanyaannya yaitu `Sebutkan urutan konfigurasi pengkabelan T568B` dan jawabannya
```
Urutan T56B :
Urutan 1 : Putih Orange RD+ (data terima+)
Urutan 2 : Orange RD- (data terima-)
Urutan 3 : Putih Hijau TD+ (data kirim+)
Urutan 4 : Biru NC (tidak dipakai)
Urutan 5 : Putih Biru NC (tidak dipakai)
Urutan 6 : Hijau TD- (data kirim-)
Urutan 7 : Putih Coklat NC (tidak dipakai)
Urutan 8 : Coklat NC (tidak dipakai)
```
![5 3](https://user-images.githubusercontent.com/52326074/96358007-c36f0c00-112c-11eb-8060-42cf094bf4f4.jpg)

- Seseorang menyimpan file zip melalui FTP dengan nama "Answer.zip". Simpan dan Buka file "Open This.pdf" di Answer.zip. Untuk mendapatkan password zipnya, temukan dalam file zipkey.txt (passwordnya adalah isi dari file txt tersebut).

Langkah : 

Mencari file `Answer.zip` terlebih dahulu dengan melakukan penyaringan pada display filter, `ftp-data contains “Answer.zip”`

![no 6 answer zip](https://user-images.githubusercontent.com/56763600/96361332-62a8f900-1157-11eb-851a-df98655116d2.png)

Kemudian klik kanan di salah satu port, pilih Follow -> TCP Stream. Kemudian pilih `raw` dan save as dalam bentuk .zip. 

Lalu buka file Answer.zip pada tempat penyimpanan komputer kita. Dan akan menemukan file Open This.pdf. 

![no 6 openthis pdf](https://user-images.githubusercontent.com/56763600/96361339-6e94bb00-1157-11eb-95fc-da9e46104e7f.png)

Saat dibuka, akan dimintai password. Untuk mendapatkan password, kita harus mencari file zipkey.txt dengan melakukan penyaringan pada wireshark `ftp-data contains "zipkey.txt"`

![no 6 nyari zipkey](https://user-images.githubusercontent.com/56763600/96361360-9421c480-1157-11eb-9040-2398fa4920fd.png)

Kemudian kita follow TCP Stream. Lalu hasilnya akan tampak seperti ini. 

![no 6 zipkey](https://user-images.githubusercontent.com/56763600/96361346-76545f80-1157-11eb-8b63-0091c71f36d4.png)

Password akan digunakan untuk membuka pdf tadi. Maka akan tampak hasil pdf seperti dibawah ini. 

![no 6 openthis pdf udah kebuka](https://user-images.githubusercontent.com/56763600/96361365-a0a61d00-1157-11eb-9c4e-8124ac0dbf5c.png)

- Ada 500 file zip yang disimpan ke FTP Server dengan nama 1.zip, 2.zip, ..., 500.zip. Salah satunya berisi pdf yang berisi puisi. Simpan dan Buka file pdf tersebut.
- Cari objek apa saja yang didownload (RETR) dari koneksi FTP dengan Microsoft FTP Service!
- Cari username dan password ketika login FTP pada localhost!
- Cari file .pdf di wireshark lalu download dan buka file tersebut! clue: "25 50 44 46"

# B. Capture Filter
- Filter sehingga wireshark hanya mengambil paket yang mengandung port 21!
- Filter sehingga wireshark hanya mengambil paket yang berasal dari port 80!
- Filter sehingga wireshark hanya menampilkan paket yang menuju port 443!
- Filter sehingga wireshark hanya mengambil paket yang berasal dari ip kalian!
- Filter sehingga wireshark hanya mengambil paket yang tujuannya ke monta.if.its.ac.id!
