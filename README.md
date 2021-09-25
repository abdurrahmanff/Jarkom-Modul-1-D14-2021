# Jarkom-Modul-1-D14-2021
Lapres Modul 1 Jarkom

### Nama Anggota Kelompok
1. A. Zidan Abdillah Majid (05111940000070)
2. Cliffton Delias Perangin Angin (05111940000181)
3. Abdurrahman Fauzan Firmansyah (05111940000231)

### Soal

**1.  Sebutkan webserver yang digunakan pada "ichimarumaru.tech"!**

Filter dengan: ```http.host contains "ichimarumaru.tech"```

![image](https://user-images.githubusercontent.com/72073667/134759201-09cc7eb1-80b2-43e1-a499-8ae4448b3169.png)

Klik kanan paket dan follow tcp stream

![image](https://user-images.githubusercontent.com/72073667/134759241-229be894-1f01-4cfe-9ea2-d6407bd00b80.png)

Bisa dilihat webserver yang digunakan adalah ```nginx/1.18.0 (Ubuntu)```

**2. Temukan paket dari web-web yang menggunakan basic authentication method!**

Filter dengan: ```http.authbasic```, dan kita menemukan 3 paket yang menggunakan basic authentication

![image](https://user-images.githubusercontent.com/72073667/134759408-bc258915-effc-45c1-bd10-015b3ab8a005.png)

**3. Ikuti perintah di basic.ichimarumaru.tech! Username dan password bisa didapatkan
dari file .pcapng!**

Filter menggunakan: ```http.host contains "basic.ichimarumaru.tech"```

![image](https://user-images.githubusercontent.com/72073667/134759422-5425ceee-3883-4185-a4b7-620d3137e548.png)

Pada paket 2 bisa dilihat credentialsnya yang merupakan ```[username]:[password]```

Setelah login pada basic.ichimarumaru.tech, tinggal mengisi sesuai yang diminta

![image](https://user-images.githubusercontent.com/72073667/134759446-0b008475-d5d8-4560-8d55-737525dc2e1a.png)

**4. Temukan paket mysql yang mengandung perintah query select!**

Filter menggunakan: ```mysql.query contains "select" or mysql.query contains "SELECT"``` untuk mendapatkan semua paket yang memiliki query select baik semua huruf kapital maupun tidak. Ditemukan 3 paket.

![image](https://user-images.githubusercontent.com/72073667/134759459-1c3352ed-3e5c-4f69-b6a1-c6eda36d37f0.png)

**5. Login ke portal.ichimarumaru.tech kemudian ikuti perintahnya! Username dan
password bisa didapat dari query insert pada table users dari file .pcap!**

Filter menggunakan ```mysql.query contains "INSERT"```

Didapatkan satu paket yang menggunakan query insert, pada Statement, bisa dilihat username dan passwordnya

![image](https://user-images.githubusercontent.com/72073667/134759481-9cac46c5-294a-4c61-acf5-63c2e51c74b5.png)

Setelah login ke portal.ichimarumaru.tech, tinggal isi sesuai perintah

![image](https://user-images.githubusercontent.com/72073667/134759490-9f894e41-3d6e-4845-815e-13223a19cc36.png)

**6. Cari username dan password ketika melakukan login ke FTP Server!**

Mengisi display filter dengan : ```ftp contains user```

![image](https://user-images.githubusercontent.com/55623766/134754850-ff8cf795-c8ae-4d26-9ac8-1a9973f3a4f4.png)

Klik kanan lalu klik follow dan pilih TCP-Stream.

![image](https://user-images.githubusercontent.com/55623766/134754871-91cd0f2a-7a56-4d87-a5fb-f1c1ff05ca42.png)

Password dan Username sudah terlihat. User = secretuser. Password = aku.pengen.pw.aja

![image](https://user-images.githubusercontent.com/55623766/134754875-8d5e7528-eff6-477f-9d37-f0237534dc5d.png)

**7. Ada 500 file zip yang disimpan ke FTP Server dengan nama 0.zip, 1.zip, 2.zip, ..., 499.zip. Simpan dan Buka file pdf tersebut. (Hint = nama pdf-nya "Real.pdf")!**

Mengisi display filter dengan : ```frame contains "Real.pdf"```

![image](https://user-images.githubusercontent.com/55623766/134754975-abda5fdc-9493-408e-acb0-67a7b01f315d.png)

Klik kanan lalu klik follow dan pilih TCP Stream.

![image](https://user-images.githubusercontent.com/55623766/134755003-0411e4f6-7839-4be7-b9d1-f0c46260beeb.png)

Ubah data dari ASCII ke Raw. 

![image](https://user-images.githubusercontent.com/55623766/134755051-71b394b2-40fd-40f0-805d-7d6832cc90b4.png)

Save as dalam format file pdf dengan nama "Real.zip".

![image](https://user-images.githubusercontent.com/55623766/134755072-43d3985c-6473-4a4c-8267-691fcf608e12.png)

Extract file zip tersebut dan buka file Real.pdf.

![image](https://user-images.githubusercontent.com/55623766/134755118-26dfa764-92bf-4d76-9505-aa07f9d03d71.png)

**9. Dari paket-paket yang menuju FTP terdapat inidkasi penyimpanan beberapa file. Salah satunya adalah sebuah file berisi data rahasia dengan nama "secret.zip". Simpan dan buka file tersebut!**

Cari file menggunakan filter ```ftp-data.command contains "secret.zip"```

![image](https://user-images.githubusercontent.com/55623766/134755214-e2792d2e-ad2d-4f59-88af-e33df64f054a.png)

Setelah itu klik kanan pada salah satu paket dan follow TCP Stream, ubah ASCII menjadi Raw, lalu save as dengan nama "secret.zip"

![image](https://user-images.githubusercontent.com/55623766/134755266-6196332c-e133-442c-808b-f13cd4b5d34d.png)

Setelah kita buka, isinya adalah sebuah file dengan nama "Wanted.pdf"

![image](https://user-images.githubusercontent.com/55623766/134755283-44dda1b7-640f-4dc1-8a57-c109526c02ce.png)

**10. Selain itu terdapat "history.txt" yang kemungkinan berisi history bash server tersebut! Gunakan isi dari "history.txt" untuk menemukan password untuk membuka file rahasia yang ada di "secret.zip"!**

Cari file menggunakan filter ```ftp-data.command contains "history.txt"```

![image](https://user-images.githubusercontent.com/55623766/134755376-2e77fa54-25da-44a0-97f4-848ebb933ccf.png)

Setelah itu klik kanan salah satu paket dan follow TCP Stream

![image](https://user-images.githubusercontent.com/55623766/134755398-e2da936a-b359-403e-871e-2314f7403c32.png)

Passwordnya berada pada file "bukanapaapa.txt". Untuk mencarinya bisa menggunakan filter ```ftp-data.command contains "bukanapaapa.txt"```

![image](https://user-images.githubusercontent.com/55623766/134755429-8f732c95-fe54-4c07-822f-42eceb1c005a.png)

Saat di-follow TCP Stream, bisa kita lihat passwordnya yaitu ```d1b1langbukanapaapajugagapercaya```

![image](https://user-images.githubusercontent.com/55623766/134755444-df741347-88bf-4307-80ef-96732b90e6c6.png)

Tinggal kita extract zip tadi dan kita mendapat isi file dari "Wanted.zip" seperti ini

![image](https://user-images.githubusercontent.com/55623766/134755471-143fef3c-22db-4d2b-86e8-5e93fc0c6900.png)

**11. Filter sehingga wireshark hanya mengambil paket yang berasal dari port 80!**

Mengisi capture filter dengan : ```src port 80```

![11 1](https://user-images.githubusercontent.com/90588333/134758943-a4a2f549-ccf0-49fb-bdef-a7eb12178eb3.png)

![11 2](https://user-images.githubusercontent.com/90588333/134758978-3f71fa1e-a4b7-44a5-b6f2-8a01c71e90b2.png)

**12. Filter sehingga wireshark hanya mengambil paket yang mengandung port 21!**

Mengisi capture filter dengan : ```port 21```

![12 1](https://user-images.githubusercontent.com/90588333/134759005-7cf00022-6454-48ee-bf9e-e8f916140d1f.png)

![12 2](https://user-images.githubusercontent.com/90588333/134759006-1f193785-d1c9-4cb6-8089-18465551609e.png)

**13. Filter sehingga wireshark hanya menampilkan paket yang menuju port 443!**

Mengisi capture filter dengan : ```tcp.dstport == 443```

![13 1](https://user-images.githubusercontent.com/90588333/134759474-b1b1d142-84bf-491d-9650-f944594c5e84.png)

**14. Filter sehingga wireshark hanya mengambil paket yang tujuannya ke kemenag.go.id!**

Mengisi capture filter dengan : ```dst host kemenag.go.id```

![14 1](https://user-images.githubusercontent.com/90588333/134759031-64223d76-e706-40b2-b3c0-774efcabb911.png)

![14 2](https://user-images.githubusercontent.com/90588333/134759033-d9b8e163-cb1f-40e3-845a-74aa1c1b2022.png)

**15. Filter sehingga wireshark hanya mengambil paket yang berasal dari ip kalian!**

Mengisi capture filter dengan : ```src host 192.168.1.30```

![15 1](https://user-images.githubusercontent.com/90588333/134759050-696f35dd-67d3-43d2-9e9a-87fc04cbcd38.png)

![15 2](https://user-images.githubusercontent.com/90588333/134759052-c0a2d327-026c-445b-8567-6b46efdecc24.png)
