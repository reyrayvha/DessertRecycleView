# DessertRecycleView

Proyek aplikasi Android sederhana untuk menampilkan daftar *dessert* menggunakan komponen **RecyclerView** pada Kotlin. Aplikasi ini dibuat sebagai materi praktikum/tugas mata kuliah Pengembangan Aplikasi Mobile (PAM).

## Gambaran Aplikasi

Aplikasi menampilkan daftar makanan penutup (Donut, Ice Cream Sandwich, dan Froyo) dalam tampilan daftar vertikal. Setiap item memiliki gambar, deskripsi singkat, dan warna latar belakang lingkaran yang diatur secara dinamis melalui kode program.

### Fitur Utama
- **RecyclerView & Custom Adapter**: Pengelolaan daftar item menggunakan `DessertAdapter` dan `ViewHolder` agar rendering memori efisien.
- **Dynamic Circle Background**: Latar belakang lingkaran pada ikon gambar dibuat secara programatik menggunakan `GradientDrawable` berbasis warna HEX dari data class `Dessert`.
- **Edge-to-Edge Layout**: Mendukung penanganan *WindowInsets* untuk tampilan serasi dengan sistem Android modern.

## Struktur Proyek

```
app/src/main/
├── java/lat/pam/dessertrecycleview/
│   ├── Dessert.kt          # Data class (description, imageRes, colorHex)
│   ├── DessertAdapter.kt   # Adapter RecyclerView & pembuatan background lingkaran
│   └── MainActivity.kt     # Activity utama penyedia data & inisialisasi list
└── res/
    ├── layout/
    │   ├── activity_main.xml # Layout utama penampung RecyclerView
    │   └── itemdesert.xml    # Layout kustom untuk tiap item dessert
    └── drawable/             # Asset gambar dessert (donut, icecream, froyo)
```

## Spesifikasi Teknis

- **Bahasa**: Kotlin
- **Min SDK**: API 27 (Android 8.1 Oreo)
- **Target SDK**: API 37
- **UI Framework**: Android Views (ConstraintLayout, RecyclerView, Material Components)

## Cara Menjalankan

1. Buka proyek ini di **Android Studio**.
2. Sync Gradle hingga selesai.
3. Jalankan aplikasi pada emulator atau perangkat fisik Android (Minimum API 27).
