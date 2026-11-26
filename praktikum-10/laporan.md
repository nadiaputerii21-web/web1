# Laporan Praktikum Pertemuan 10 — Pemrograman Web 1
Nama : Nadia Puteri
NIM : 2510010335
Kelas : 3B REG TI BJB

## Percobaan 1-Navbar
## 2.3 Tabel Pengamatan
| No | Eksperimen | Pengamatan |
|---|---|---|
| 1 | Class #menuLab dan nilai aria-expanded saat menu terbuka | Saat menu dibuka, class `show` ditambahkan pada `#menuLab` dan nilai `aria-expanded` berubah menjadi `true` |
| 2 | Hamburger di 1000 px dengan navbar-expand-lg | Pada lebar 1000 px, tombol hamburger tidak muncul karena menu sudah ditampilkan secara horizontal |
| 3 | Perilaku di 800 px:-md / tanpa fungsi / tanpa class expand | `navbar-expand-md` menampilkan menu secara horizontal. `navbar-expand` membuat menu selalu terbuka, sedangkan tanpa class expand menu tetap menggunakan tampilan collapse |
| 4 | data-bs-target salah ketik | Menu tidak bisa dibuka karena `data-bs-target` mengarah ke ID yang salah, yaitu `#menu`, bukan `#menuLab` |
| 5 | Tanpa JS bundle | Tanpa JavaScript bundle, tombol hamburger dan dropdown Layanan tidak dapat digunakan |
| 6 | bg-dark tanpa dan dengan data-bs-theme="dark" | Dengan `bg-dark`, latar navbar berubah menjadi gelap, tetapi teks masih gelap. Setelah ditambahkan `data-bs-theme="dark"`, teks dan ikon hamburger berubah menjadi terang |
| 7 | sticky-top vs fixed-top | `sticky-top` membuat navbar tetap menempel di atas saat halaman digulir. Sementara itu, `fixed-top` membuat navbar selalu berada di atas dan dapat menutupi sebagian judul Konten halaman |

## Percobaan 2-tombol
## 3.3 Tabel Pengamatan
| No | Eksperimen | Pengamatan |
|---|---|---|
| 1 | Kelompok Batal–Simpan di 375 px dan 1000 px | Pada 375 px, tombol Batal dan Simpan tersusun vertikal dengan lebar penuh. Pada 1000 px, kedua tombol tersusun horizontal dan berada di sebelah kanan |
| 2 | Elemen nonaktif yang masih bisa difokus dengan Tab | Tombol dengan atribut `disabled` dilewati saat menekan Tab. Tautan yang hanya menggunakan class `disabled` masih bisa difokus dan diaktifkan dengan Enter. Tautan tanpa `href` dan menggunakan `aria-disabled="true"` tidak menerima fokus |
| 3 | Kontras text-bg-warning vs bg-warning | `text-bg-warning` menghasilkan teks gelap dengan latar kuning sehingga lebih mudah dibaca. Sementara itu, `bg-warning` menghasilkan teks putih dengan latar kuning sehingga kontrasnya rendah |
| 4 | Nama tombol Notifikasi dengan dan tanpa visually-hidden | Dengan `visually-hidden`, nama tombol terbaca "Notifikasi 3 notifikasi belum dibaca". Setelah dihapus, nama tombol hanya terbaca "Notifikasi 3" |

## Percobaan 3-tipografi
## 4.3 Tabel Pengamatan
| Class lama | Utilitas pengganti (isi) | Tampilan sama? (ya/tidak) |
|---|---|---|
| `.judul-besar` | display-5 text-center | Ya |
| `.pembuka` | lead text-body-secondary text-center | Ya |
| `.label` | text-uppercase fw-bold small | Tidak sepenuhnya, karena jarak antarhuruf berbeda. |
| `.catatan` | small fst-italic | Ya |
| `.nim` | font-monospace | Ya |
| Temuan Lighthouse untuk `<h4>` | Urutan heading tidak berurutan karena dari `<h1>` langsung ke `<h4>` | Tidak |

## Hasil Tangkapan Layar
![Sebelum](p3-tipografi/sebelum.png) ![Sesudah](p3-tipografi/sesudah.png)

## Percobaan 4 — Dashboard
![Mobile, menu terbuka](p4-dashboard/mobile-menu-terbuka(1).png)![Mobile, menu terbuka](p4-dashboard/mobile-menu-terbuka(2).png)![Mobile, menu terbuka](p4-dashboard/mobile-menu-terbuka(3).png)
![Desktop](p4-dashboard/desktop2.png)

Skor Lighthouse Accessibility: 95

## Jawaban Pertanyaan Analisis
1. Saat hamburger diklik, JavaScript Bootstrap mengubah class pada bagian menu navbar. Menu yang awalnya tersembunyi akan terbuka, dan jika diklik lagi akan tertutup. Hal ini sama seperti materi manipulasi DOM, yaitu JavaScript bisa mengubah bagian HTML tanpa harus memuat ulang halaman
2. Karena CSS Bootstrap masih berjalan sehingga tampilan navbar tetap muncul. Namun, JavaScript Bootstrap tidak dimuat, sehingga tombol hamburger dan dropdown tidak bisa digunakan
3. Karena walaupun tampilannya terlihat tidak aktif, tautan tersebut masih bisa dibuka karena masih memiliki href. Jadi, sebaiknya href dihapus agar tautan benar-benar tidak bisa digunakan
4. a. Karena <h2 class="h5"> lebih sesuai untuk judul panel yang berada di bawah judul utama
b. Agar susunan judul lebih rapi dan mudah dipahami oleh pembaca maupun screen reader
5. Skor Lighthouse Accessibility dashboard adalah **95/100**. Yang perlu diperbaiki adalah masalah kontras warna tulisan dengan latar belakang. Saya memperbaikinya dengan menggunakan warna teks yang lebih gelap agar tulisan lebih mudah dibaca

## Kesimpulan
Berdasarkan praktikum yang telah dilakukan, saya memahami cara menggunakan Bootstrap untuk membuat tampilan website yang lebih. Saya juga mempelajari penggunaan navbar, dropdown, tombol, serta pengaturan teks menggunakan class Bootstrap. Selain itu, saya belajar bahwa JavaScript Bootstrap berfungsi untuk menjalankan fitur interaktif pada website. Melalui pengujian Lighthouse, dashboard saya mendapatkan skor Accessibility 95/100 dan saya mengetahui pentingnya memperhatikan kontras warna agar website lebih mudah dibaca