# Dokumen Teknis Modul 1 — Lingkungan Pengembangan, Git, dan Lalu Lintas HTTP 

Nama/NIM   : Erlangga Aditya Permana/105224038  
Repositori : [https://github.com/xvasgit/PemWeb26.git](https://github.com/xvasgit/PemWeb26.git)

## 1\. Lingkungan Pengembangan

| No | Tool/OS | Version |
| :---- | :---- | :---- |
| 1 | Windows 11 | 25H2 |
| 2 | Node.js | 24.13.0 |
| 3 | npm | 11.6.2 |
| 4 | Git | 2.53.0.windows.1 |
| 5 | Visual Studio Code | 1.139.0 |

## 2\. Alur Kerja Git  
Keluaran git log \--oneline \--graph  
<img width="855" height="40" alt="image" src="https://github.com/user-attachments/assets/e88b6b7e-9051-4eec-b017-2d34e20acbdb" />

 
[Tautan pull request yang telah digabungkan ](https://github.com/xvasgit/PemWeb26/pull/1) 

Konflik yang terjadi pada commit kedua  
<img width="468" height="107" alt="image" src="https://github.com/user-attachments/assets/1e67072b-29c6-4353-98a0-db2afd922dfb" />


Cara penyelesaian konflik  
Penyelesaian konflik dapat dilakukan di GitHub langsung atau di IDE repositori lokal yang terhubung dengan repository GitHubnya. Jika pada GitHub langsung, cara menyelesaikan konfliknya adalah dengan membuat Pull Request lalu akan ada opsi “Resolve Conflict” yang muncul jika PR terdeteksi tidak bisa langsung di-merge. Dalam laman Resolve Conflict, diberikan opsi untuk meng-accept antara edit dari branch asal saja, edit dari branch tujuan saja, atau gabungan edit dari kedua branch. Pada kasus saya, saya memilih untuk memilih accept kedua perubahan sebagai uji coba. Hasilnya, edit dari branch tujuan yang sudah ada ikut masuk ke Pull Request baru yang dapat otomatis di-merge karena sudah di Resolve Conflict.  
<img width="464" height="212" alt="image" src="https://github.com/user-attachments/assets/4f5e4d97-d25a-4284-ab30-2efb4a60f10f" />


## 3\. Pengamatan Lalu Lintas HTTP

| No | URL | Metode | Kode Status | Content Type | Header Lain yang Diamati |
| :---- | :---- | :---- | :---- | :---- | :---- |
| 1 | http://localhost:3000/ | GET | 200 OK | text/html; charset=utf-8 | no-cache (Cache-Control) |
| 2 | http://localhost:3000/ halaman-tidak-ada | GET | 404 Not Found | text/html; charset=utf-8 | no-cache (Cache-Control) |
| 3 | Satu berkas CSS atau JS dari localhost :  chrome-extension://efaidnbmnnnibpcajpcglclefindmkaj/dist/[FloatingActionButton.js](http://FloatingActionButton.js)  | GET | 200 OK  | text/javascript | Tue, 15 Sep 2026 03:13:56 GMT (last-modified) |
| 4 | http://github.com (curl) | HEAD | 301 Moved Permanently | \- | [https://github.com/](https://github.com/) (Location) |
| 5 | https:// developer.mozilla.org (dengan cache) | GET | 302 Found (from disk cache) | text/html; charset=utf-8 | max-age=3600,public (Cache-Control) |

## 4\. Kendala dan Penyelesaian  
Saat ini tidak ada kendala. Pengerjaan dari mulai cek version tools, memahami dasar alur kerja Git, dan pengamatan lalu lintas HTTP masih bisa dimengerti dengan baik.

## 5\. Catatan Pemanfaatan AI  
Tidak menggunakan AI
