# README - Jobsheet 2 Pengolahan Citra

## Identitas
- Nama: Alif Rahman Maulana
- NIM: 33423201
- Mata Kuliah: Pengolahan Citra

## Penjelasan Kode

### Praktik 1 - Deteksi Tepi Sobel pada Citra Grayscale
Kode menggunakan gambar grayscale dari `skimage` (data `coins`) lalu menerapkan operator Sobel untuk:
- Arah horizontal (`sobel_h`)
- Arah vertikal (`sobel_v`)
- Gabungan kedua arah (`sobel`)

Hasil divisualisasikan dalam 4 tampilan: gambar asli, gradien X, gradien Y, dan hasil tepi Sobel.

### Praktik 2 - Deteksi Tepi Sobel pada Citra Berwarna per Kanal RGB
Kode menggunakan citra berwarna (`astronaut`) dan memisahkan kanal merah, hijau, dan biru.
Masing-masing kanal diproses dengan Sobel, lalu digabungkan kembali menjadi citra RGB tepi.
Visualisasi menampilkan:
- Gambar asli
- Tepi kanal merah
- Tepi kanal hijau
- Tepi kanal biru
- Tepi gabungan RGB

### Praktik 3 - Deteksi Tepi Roberts pada Grayscale dan Berwarna
Kode menerapkan operator Roberts pada:
- Citra grayscale (`coins`)
- Citra berwarna (`astronaut`) per kanal RGB

Untuk citra berwarna, tiap kanal diproses lalu digabungkan kembali agar terlihat kontribusi tepi dari masing-masing kanal.

### Praktik 4 - Perbandingan Operator pada Citra Grayscale
Kode membandingkan beberapa operator deteksi tepi pada citra grayscale:
- Sobel
- Roberts
- Prewitt
- Kirsch (melalui gradient morfologi)
- Canny

Hasil ditampilkan dalam grid agar mudah membandingkan kualitas tepi dari setiap operator pada gambar yang sama.

### Praktik 5 - Perbandingan Operator pada Grayscale dan Berwarna
Kode membandingkan operator yang sama pada dua jenis citra:
- Grayscale
- Berwarna

Untuk citra berwarna, dibuat fungsi `apply_edge_detection()` agar operator dijalankan per kanal RGB kemudian digabungkan kembali.
Sedangkan Canny diterapkan pada citra berwarna yang terlebih dahulu dikonversi ke grayscale.

### Praktik 6 - Upload Foto Sendiri dan Bandingkan Hasil Operator
Kode meminta pengguna mengunggah gambar dari handphone/komputer, mengubah gambar ke grayscale, lalu menerapkan:
- Sobel
- Roberts
- Prewitt
- Scharr
- Canny

Setiap hasil ditampilkan berdampingan agar perbedaan karakter tiap operator mudah dianalisis.

## Keterangan Praktik Terakhir
Praktik terakhir adalah program untuk melakukan perbandingan deteksi tepi dari beberapa operator menggunakan gambar yang didapat dari handphone masing-masing.

## Kesimpulan
1. Setiap operator deteksi tepi memiliki karakter hasil yang berbeda.
2. Sobel dan Prewitt cocok untuk deteksi tepi umum, Roberts cenderung menghasilkan tepi yang lebih tipis.
3. Canny umumnya menghasilkan tepi paling bersih karena melalui proses penyaringan dan thresholding.
4. Pada citra berwarna, pemrosesan per kanal RGB dapat menampilkan detail tepi yang berbeda di tiap kanal.
5. Pengujian dengan foto sendiri (praktik terakhir) penting karena kondisi nyata seperti pencahayaan, tekstur, dan noise memengaruhi hasil deteksi tepi.
