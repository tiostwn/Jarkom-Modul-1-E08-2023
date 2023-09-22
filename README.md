# Jarkom-Modul-1-E08-2023
Laporan Resmi Praktimum 1 JARKOM

**Anggota Kelompok**
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
