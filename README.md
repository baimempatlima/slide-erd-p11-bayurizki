# Entity Relationship Diagram

Presentasi web pertemuan ke-11 mata kuliah **Analisis dan Desain Sistem Informasi Perpustakaan** (IPP330030, 3 SKS).

Bayu Rizki, M.Kom
Jurusan Ilmu Perpustakaan, Fakultas Adab dan Humaniora, UIN Alauddin Makassar

97 slide. Dari ERD konseptual notasi Chen ke ERD logis crow's foot, selalu bersanding dengan DFD.

---

## Menjalankan

Buka `index.html` di peramban. Tidak perlu server, tidak perlu sambungan internet. Semua fon, gambar, dan skrip ada di dalam folder ini.

## Mengunggah ke GitHub Pages

1. Buat repositori baru, lalu unggah **seluruh isi folder ini** ke akar repositori, bukan foldernya.
2. Buka `Settings` lalu `Pages`.
3. Pada `Source` pilih **Deploy from a branch**, branch `main`, folder `/ (root)`.
4. Tunggu sampai tab `Actions` menyelesaikan proses, biasanya satu sampai dua menit.
5. Bila halaman masih 404, muat ulang dengan `Ctrl` `Shift` `R`.

Berkas `.nojekyll` sudah disertakan supaya GitHub tidak memproses ulang folder dan berkas yang diawali garis bawah.

## Tombol

| Tombol | Fungsi |
| --- | --- |
| `←` `→` `spasi` | pindah slide |
| angka lalu tunggu sebentar | lompat ke nomor slide |
| `O` | ikhtisar semua slide |
| `M` | menu lompat per bagian |
| `F` | layar penuh |
| `H` atau `?` | tampilkan atau sembunyikan catatan tombol |
| `Esc` | tutup ikhtisar, menu, atau gambar yang diperbesar |

Klik di sepertiga kanan layar untuk maju, di seperlima kiri untuk mundur. Di layar sentuh, geser ke kiri atau ke kanan. Klik gambar mana pun untuk memperbesarnya.

Alamat di bilah peramban ikut berubah, misalnya `#s31`, sehingga satu slide bisa ditautkan langsung.

## Bagian yang bisa diklik

| Slide | Yang terjadi |
| --- | --- |
| 1, pembuka | Klik kotak ANGGOTA, PEMINJAMAN, atau EKSEMPLAR untuk membaca kalimat relasinya |
| 2 dan 3, kata penting | Ketik di kotak saring untuk menyaring 20 istilah |
| 30, dua notasi | Sakelar Notasi Chen dan Crow's foot |
| 33, lima langkah | Klik kotak untuk membaca garis dari arah itu; lambang di ujung seberang ikut menyala |
| semua gambar | Klik untuk memperbesar |

---

## Menyembunyikan slide

Semua slide ada di dalam **`index.html`**, satu di bawah yang lain, masing-masing diawali komentar penanda:

```html
<!-- ===== SLIDE 33 | BAGIAN H | Lima langkah membaca satu garis crow's foot ===== -->
<section class="slide" data-sec="BAGIAN H" data-title="...">
```

Ada dua cara menyembunyikannya. Keduanya membuat nomor halaman, bilah kemajuan, ikhtisar, dan menu bagian **menghitung ulang dengan sendirinya**, jadi tidak ada nomor yang bolong.

**Cara 1, tambahkan `data-hide`.** Paling rapi, karena slidenya tetap utuh dan mudah dikembalikan.

```html
<section class="slide" data-hide data-sec="BAGIAN H" data-title="...">
```

**Cara 2, tambahkan kelas `hide`.**

```html
<section class="slide hide" data-sec="BAGIAN H" data-title="...">
```

Untuk mengembalikannya, hapus `data-hide` atau kata `hide` itu saja.

Mengomentari seluruh blok `<section>` dengan `<!-- ... -->` juga berhasil, tetapi hati-hati: isi slide sudah mengandung komentar penanda, dan komentar HTML tidak boleh bersarang.

## Mengubah isi

| Yang diubah | Berkas |
| --- | --- |
| teks, susunan, dan urutan slide | `index.html` |
| warna, ukuran huruf, tata letak | `deck.css` |
| gambar ERD | `img/s*.png`, nomornya mengikuti nomor slide pada berkas sumber |

Ukuran huruf utama ada di bagian atas `deck.css` dan pada aturan `h1`, `.kick`, `.ent p`, `.item p`, `tbody td`, serta `thead th`.

## Warna

Diambil dari diagram ERD dan logo institusi.

| Nama | Nilai | Dipakai untuk |
| --- | --- | --- |
| biru | `#17567E` | kepala kotak entitas, judul bagian, tabel |
| biru muda | `#2F86C0` | aksen dan bilah kemajuan |
| kuning tua | `#B87A08` | hal yang belum diwawancarai, kunci asing, sorotan |
| hijau | `#1F7A52` | hal yang sudah tersedia atau benar |
| merah | `#AE3A31` | hal yang keliru |
