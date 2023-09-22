# Jarkom-Modul-1-E08-2023
Laporan Resmi Praktimum 1 JARKOM

**Anggota Kelompok ``E08``** 
| No | Nama | NRP |
| --- | --- | --- |
| 1 | Samuel Berkat Hulu | 5025201055 |
| 2 | Hanafi Satriyo Utomo Setiawan | 5025211195 |

## Soal 1
User melakukan berbagai aktivitas dengan menggunakan protokol FTP. Salah satunya adalah mengunggah suatu file.
1. Berapakah sequence number (raw) pada packet yang menunjukkan aktivitas tersebut?
2. Berapakah acknowledge number (raw) pada packet yang menunjukkan aktivitas tersebut?
3. Berapakah sequence number (raw) pada packet yang menunjukkan response dari aktivitas tersebut?
4. Berapakah acknowledge number (raw) pada packet yang menunjukkan response dari aktivitas tersebut?

## Penyelesaian Soal 1
- Gunakan filter `ftp`
- Untuk soal A dan B cari packet yang berisi `Request : STOR (namafile)`
- <img width="1511" alt="image" src="https://github.com/tiostwn/Jarkom-Modul-1-E08-2023/assets/53292102/c7c02c4d-92b0-4e22-9703-82b70f601183">
Sehingga, dapat kita ketahui bahwa:
- Sequence number (raw) : `258040667`
- Acknowledge number (raw) : `104486103925`
_______________________
- Untuk soal C dan D cai paket yang berisi `Response : 150` (ada di bawah paket STOR)
- <img width="1511" alt="image" src="https://github.com/tiostwn/Jarkom-Modul-1-E08-2023/assets/53292102/e47339f9-ee1c-4721-8670-3b3212eabf3f">
Sehingga, dapat kita ketahui bahwa:
- Sequence number (raw) : `258040667`
- Acknowledge number (raw) : `104486103925`


  
## Soal 2
Sebutkan web server yang digunakan pada portal praktikum Jaringan Komputer!

## Penyelesaian Soal 2
- Filter menggunakan `http contains "10.21.78.111"`
- Pilih salah satu paket
- Klik kanan pada paket tersebut
- Pilih follow -> TCP STREAM
- Pilih follow -> TCP STREAM
- <img width="1512" alt="image" src="https://github.com/tiostwn/Jarkom-Modul-1-E08-2023/assets/53292102/9d58f338-1dda-4ad0-9a7b-e093d84cf712">


## Soal 3
Dapin sedang belajar analisis jaringan. Bantulah Dapin untuk mengerjakan soal berikut:
1. Berapa banyak paket yang tercapture dengan IP source maupun destination address adalah 239.255.255.250 dengan port 3702?
2. Protokol layer transport apa yang digunakan?

## Penyelesaian Soal 3
- Filter menggunakan
```R
ip.addr == 239.255.255.250 && udp.port == 3702
```

- Bisa dilihat ada sebanyak 21 paket
<img width="1512" alt="image" src="https://github.com/tiostwn/Jarkom-Modul-1-E08-2023/assets/53292102/d3223e04-7391-4fdb-950f-4084ae922f4d">



## Soal 4
Berapa nilai checksum yang didapat dari header pada paket nomor 130?

## Penyelesaian Soal 4
<img width="1512" alt="image" src="https://github.com/tiostwn/Jarkom-Modul-1-E08-2023/assets/53292102/afe08da9-f7ac-4af6-8cef-6e3868a61d02">



## Soal 5
Elshe menemukan suatu file packet capture yang menarik. Bantulah Elshe untuk menganalisis file packet capture tersebut.
Berapa banyak packet yang berhasil di capture dari file pcap tersebut?
Port berapakah pada server yang digunakan untuk service SMTP?
Dari semua alamat IP yang tercapture, IP berapakah yang merupakan public IP?
## Penyelesaian Soal 5



## Soal 6
Seorang anak bernama Udin Berteman dengan SlameT yang merupakan seorang penggemar film detektif. sebagai teman yang baik, Ia selalu mengajak slamet untuk bermain valoranT bersama. suatu malam, terjadi sebuah hal yang tak terdUga. ketika udin mereka membuka game tersebut, laptop udin menunjukkan sebuah field text dan Sebuah kode Invalid bertuliskan "server SOURCE ADDRESS 7812 is invalid". ketika ditelusuri di google, hasil pencarian hanya menampilkan a1 e5 u21. jiwa detektif slamet pun bergejolak. bantulah udin dan slamet untuk menemukan solusi kode error tersebut.
## Penyelesaian Soal 6
** BELUM SELESAI **



## Soal 7
Berapa jumlah packet yang menuju IP 184.87.193.88?
## Penyelesaian Soal 7
- Pada layar Display Filter ketikan ``ip.dst == 184.87.193.88`` dan Enter.
- kemudian muncul packet-packet yang berasal dari alamat ``184.87.193.88``.
- ![Screenshot 2023-09-18 200041](https://github.com/tiostwn/Jarkom-Modul-1-E08-2023/assets/100474007/b67c9834-f14d-49f7-a144-ee2f638e8e40)
- Dari hasil display filter yang dilakukan terdapat ``6 packet`` yang menuju ``184.87.193.88``.




## Saol 8
Berikan kueri filter sehingga wireshark hanya mengambil semua protokol paket yang menuju port 80! (Jika terdapat lebih dari 1 port, maka urutkan sesuai dengan abjad)
## Penyelesaian Soal 8
- Filter menggunakan
  ```R
   tcp.dstport == 80 || udp.dstport == 80
  ```


## Soal 9
Berikan kueri filter sehingga wireshark hanya mengambil paket yang berasal dari alamat 10.51.40.1 tetapi tidak menuju ke alamat 10.39.55.34!
## Penyelesaian Soal 9
- Pada layar Display Filter ketikan dan Enter.
```R
  ip.src == 10.51.40.1 && ip.dst != 10.39.55.34
```
- Filter diatas hanya mengambil paket dari alamat ``10.51.40.11`` dan tidak menuju ke alamat ``10.39.55.34``
- ![no 9](https://github.com/tiostwn/Jarkom-Modul-1-E08-2023/assets/100474007/7b4d1dcb-e0a1-46ad-9b25-474a3b085d27)



## Soal 10
Sebutkan kredensial yang benar ketika user mencoba login menggunakan Telnet
## Penyelesaian Soal 10
- Pada layar Display Filter ketikan ``telnet`` dan Enter, untuk filter packet - paket yang menuju telnet.
- ![Screenshot 2023-09-22 173125](https://github.com/tiostwn/Jarkom-Modul-1-E08-2023/assets/100474007/61bfbe5b-ab47-4176-8781-d12d5389dca3)
- Kemudian temukan packet ``no 236`` yang berisikan Telnet ``Data : Login:``.
- ![Screenshot 2023-09-22 175038](https://github.com/tiostwn/Jarkom-Modul-1-E08-2023/assets/100474007/5ad7e38f-db10-4cc2-9af0-447b277e4073)
- Klik kanan pada packet ``no 236`` pilih ``Follow`` ---> ``TCP Stream``.
- ![Screenshot 2023-09-22 174256](https://github.com/tiostwn/Jarkom-Modul-1-E08-2023/assets/100474007/17a7059a-65db-49cc-9f59-ac4f5472d15d)
- ``TCP Stream`` untuk melihat isi dari packet. Kemudain akan muncul Login & Password yang di cari.
- ![Screenshot 2023-09-22 174334](https://github.com/tiostwn/Jarkom-Modul-1-E08-2023/assets/100474007/036a59b2-3d06-4097-8824-d390ca6c19bc)
- Dari gambar diatas kita tahu bahwa kredensial yang bernar untuk login adalah ``dhafin:kesayangank0k0``.

