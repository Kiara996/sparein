# Mockup SVG halaman

Mockup halaman-halaman Sparein buat dibuka di Figma, dibikin dari spesifikasi di [`UI-Specs.md`](../../UI-Specs.md) dan kerangka di `UI-Base-Build.md`. Ini referensi tampilan, bukan sumber kebenaran. Kalau beda sama dokumen spesifikasi, dokumennya yang menang.

Semua frame pakai header, footer, dan lebar isi yang sama (kerangka base): desktop 1440 dan mobile 390.

## Isi

| Folder | Modul | Halaman | Jumlah file |
|---|---|---|---|
| `devices/` | M1 Perangkat | Katalog (P10), detail (P11), form (P12), konfirmasi hapus | 11 |
| `diagnostics/` | M2 Diagnosa | Pilih perangkat dan hasil (P20), detail gejala (P21), form gejala (P22) | 8 |
| `guides/` | M3 Panduan | Daftar (P30), detail (P31), form (P32), tersimpan (P33) | 10 |
| `parts/` | M4 Suku Cadang | Direktori (P40), detail (P41), form (P42) | 8 |
| `journal/` | M5 Jurnal | Jurnal saya (P50), detail catatan (P51), form catatan (P52) | 8 |
| `core/` | core | Profil saya (P03) | 3 |

Total 48 file. Beranda (P00) belum dibikin, sengaja ditunda.

## Penamaan

`<kode halaman>-<nama>-<ukuran>[-<varian>].svg`, contoh `p31-detail-panduan-desktop-visitor.svg`.

Varian yang ada:

| Akhiran | Artinya |
|---|---|
| `-visitor`, `-member`, `-admin`, `-contributor` | Tampilan buat role itu (header dan isi ikut beda) |
| `-kosong` | State kosong |
| `-error` | State error di form |
| `-belum-berhasil` | Catatan jurnal yang statusnya belum berhasil |
| `-pilih-perangkat`, `-hasil` | Dua tahap halaman diagnosa |

## Yang perlu kamu tahu

- **Halaman modul 1 (`devices/`) mengikuti kode yang sudah ada**, bukan desain ideal di `UI-Specs.md`. Filter masih satu baris (cari, kategori, merek) dan kartu cuma menampilkan gambar, nama, dan merek, karena API perangkat belum ngirim nama kategori dan skor (lihat Q20 dan Q21 di `UI-Specs.md`). Halaman modul lain mengikuti desain di `UI-Specs.md`.
- **Kartu dengan gambar** pakai kotak placeholder biru muda dan ikon. Ganti dengan foto asli di Figma.
- **Beberapa elemen di `UI-Specs.md` sengaja ngga digambar** biar tetap sederhana: pagination, tombol melayang di mobile, dan bar ringkasan hasil diagnosa di mobile.
- **Isi halaman modul 2 sampai 5 adalah usulan.** Pemilik modulnya yang berhak setuju atau ubah.

## Cara import ke Figma

1. Install font **Inter** dulu di komputermu, biar teks ngga ganti font.
2. Drag file `.svg` ke kanvas Figma. Hasilnya satu frame berisi vektor dan layer teks.
3. Nama layer udah dirapihin (`Kartu`, `Form/Field ...`, `Button/primary`, `Empty State`, dan seterusnya).

Auto layout, komponen beserta variannya, Color Style, Text Style, dan prototype ngga ikut ke-import. Bagian itu tetap dibangun manual di Figma, dengan SVG ini sebagai patokan visual. Efek **Background blur** di header juga ngga ikut, tambahin manual: fill `white` 80% plus Background blur 20.

## Catatan teknis

- Teks ditulis per baris (ngga ada auto wrap), jadi kalau fontnya beda, lebar teks bisa sedikit geser.
- Ikon dari Lucide (lisensi ISC).
