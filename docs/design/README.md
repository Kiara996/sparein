# Mockup SVG

Mockup visual buat dibuka di Figma, dibikin dari spesifikasi di [`UI-Specs.md`](../UI-Specs.md) dan [`UI-Auth-Build.md`](../UI-Auth-Build.md). File di sini cuma referensi tampilan jadi, bukan sumber kebenaran. Kalau beda sama dokumen spesifikasi, dokumennya yang menang.

## Isi

| Folder | Isi |
|---|---|
| `auth/` | Halaman Masuk (P01) dan Daftar (P02), desktop 1440 dan mobile 390, state default dan error. Total 8 file |

Penamaan file: `<kode halaman>-<nama>-<ukuran>-<state>.svg`, contoh `p01-masuk-desktop-default.svg`.

## Cara import ke Figma

1. Install font **Inter** dulu di komputermu, biar teks ngga ganti font.
2. Drag file `.svg` ke kanvas Figma. Hasilnya satu frame berisi vektor dan layer teks.
3. Nama layer udah dirapihin (`Panel Ilustrasi`, `Panel Form`, `Form Wrap`, `Heading Group`, dan seterusnya) supaya gampang disamain sama struktur di build sheet.

## Yang ngga ikut ke-import

Auto layout, komponen beserta variannya, Color Style, Text Style, dan sambungan prototype. SVG cuma bentuk statis. Bagian itu tetap dibangun manual di Figma ngikutin `UI-Auth-Build.md`, dengan SVG ini sebagai patokan visual.

## Catatan

- Teks di SVG ditulis per baris (ngga ada auto wrap), jadi kalau font berbeda, lebar teks bisa sedikit geser.
- Ilustrasi di dalam frame sama dengan `docs/brand/auth-illustration.svg` dan `auth-illustration-banner.svg`. Kalau ilustrasinya diganti, frame di sini perlu digenerate ulang.
- Ikon (mata, peringatan, panah) dari Lucide (lisensi ISC).
