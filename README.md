# Jarkom-Modul-1-D14-2021
Lapres Modul 1 Jarkom

### Nama Anggota Kelompok
1. A. Zidan Abdillah Majid (05111940000070)
2. Cliffton Delias Perangin Angin (05111940000181)
3. Abdurrahman Fauzan Firmansyah (05111940000231)

### Soal

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

Tinggal kita extract zip tadi dan kita mendapat isi file dari "Wanted.zip" seperti di ini

![image](https://user-images.githubusercontent.com/55623766/134755471-143fef3c-22db-4d2b-86e8-5e93fc0c6900.png)


