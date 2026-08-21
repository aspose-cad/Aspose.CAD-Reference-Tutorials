---
date: 2026-04-13
description: Pelajari cara merasterkan lapisan CAD dengan Java menggunakan Aspose.CAD
  untuk Java. Panduan langkah demi langkah ini menunjukkan konversi tingkat lapisan
  ke gambar raster.
keywords:
- java rasterize cad layer
- Aspose CAD Java
- convert CAD layer to raster
linktitle: Ubah Lapisan CAD ke Format Gambar Raster
second_title: Aspose.CAD Java API
title: Java Rasterisasi Lapisan CAD – Tutorial Aspose CAD
url: /id/java/cad-drawing-conversion/convert-cad-layer-to-raster-image/
weight: 11
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Tutorial Aspose CAD Java: Mengonversi Lapisan CAD ke Format Gambar Raster

## Pendahuluan

Jika Anda perlu **java rasterize cad layer** file untuk memudahkan berbagi, mencetak, atau pemrosesan gambar lanjutan, Anda berada di tempat yang tepat. Dalam tutorial ini kami akan menjelaskan bagaimana Aspose.CAD untuk Java memungkinkan Anda memilih lapisan individual dari gambar CAD dan mengekspornya sebagai gambar raster berkualitas tinggi seperti JPEG, PNG, atau BMP. Pada akhir tutorial Anda akan memahami mengapa rasterisasi selektif penting, cara mengonfigurasi opsi rasterisasi, dan cara menyimpan hasilnya dengan hanya beberapa baris kode.

## Jawaban Cepat
- **Apa yang dibahas dalam tutorial ini?** Mengonversi lapisan CAD terpilih menjadi gambar raster menggunakan Aspose.CAD untuk Java.  
- **Format apa yang didukung?** Semua format raster yang didukung oleh Aspose (JPEG, PNG, BMP, dll.).  
- **Apakah saya memerlukan lisensi?** Versi percobaan gratis dapat digunakan untuk pengembangan; lisensi diperlukan untuk produksi.  
- **Apa prasyaratnya?** Lingkungan pengembangan Java dan pustaka Aspose.CAD Java.  
- **Berapa lama implementasinya?** Sekitar 10–15 menit untuk konversi dasar.

## Apa itu “java rasterize cad layer”?

Rasterisasi lapisan CAD berarti mengonversi data vektor dari lapisan tertentu tersebut menjadi gambar berbasis piksel. Proses ini mempertahankan tampilan visual lapisan sambil membuatnya kompatibel dengan sistem apa pun yang dapat menampilkan format gambar standar.

## Mengapa menggunakan pendekatan ini?

- **Selective Export** – Hanya lapisan yang Anda butuhkan yang dirender, mengurangi ukuran file dan waktu pemrosesan.  
- **Format Flexibility** – Ganti `JpegOptions` dengan `PngOptions`, `BmpOptions`, dll., tanpa mengubah logika inti.  
- **High‑Quality Rendering** – Aspose.CAD mempertahankan ketebalan garis, warna, dan teks persis seperti pada file CAD asli.

## Prasyarat

Sebelum menyelam ke kode, pastikan Anda memiliki hal berikut:

- **Java Development Environment** – JDK 8 atau yang lebih tinggi terpasang dan terkonfigurasi.  
- **Aspose.CAD Library** – Unduh dan instal pustaka Aspose.CAD untuk Java dari [download link](https://releases.aspose.com/cad/java/).

## Impor Namespace

Pada langkah ini, kita akan mengimpor kelas yang diperlukan untuk mulai bekerja dengan file CAD.

### Impor Kelas Aspose.CAD

In your Java source file, include the required Aspose.CAD imports:

```java
import com.aspose.cad.Image;


import com.aspose.cad.imageoptions.CadRasterizationOptions;
import com.aspose.cad.imageoptions.JpegOptions;
import java.util.ArrayList;
import java.util.Arrays;
import java.util.List;
```

## Mengonversi Lapisan CAD ke Format Gambar Raster

Berikut adalah proses lengkap langkah demi langkah. Setiap langkah dijelaskan dengan bahasa sederhana sebelum blok kode, sehingga Anda tahu persis apa yang terjadi.

### Langkah 1: Siapkan File CAD

Pertama, arahkan ke file CAD Anda dan muat ke dalam objek `Image`.

```java
// The path to the resource directory.
String dataDir = "Your Document Directory" + "CADConversion/";
String srcFile = dataDir + "conic_pyramid.dxf";
Image image = Image.load(srcFile);
```

### Langkah 2: Konfigurasikan Opsi Rasterisasi

Buat instance `CadRasterizationOptions` untuk menentukan ukuran dan kualitas gambar output.

```java
CadRasterizationOptions rasterizationOptions = new CadRasterizationOptions();
rasterizationOptions.setPageWidth(500);
rasterizationOptions.setPageHeight(500);
```

### Langkah 3: Tentukan Lapisan CAD

Tambahkan nama lapisan yang ingin Anda rasterisasi. Pada contoh ini kami mengekspor lapisan default `"0"`.

```java
List<String> stringList = new ArrayList<>(Arrays.asList("0"));
rasterizationOptions.setLayers(stringList);
```

### Langkah 4: Siapkan Opsi JPEG

Buat objek `JpegOptions` (atau opsi gambar raster lainnya) dan hubungkan dengan pengaturan rasterisasi.

```java
JpegOptions options = new JpegOptions();
options.setVectorRasterizationOptions(rasterizationOptions);
```

### Langkah 5: Ekspor ke JPEG

Terakhir, simpan lapisan yang telah dirasterisasi sebagai file JPEG.

```java
image.save(dataDir + "CADLayersToRasterImageFormats_out_.jpg", options);
```

Ulangi langkah-langkah di atas untuk lapisan tambahan atau sesuaikan parameter rasterisasi (resolusi, warna latar belakang, dll.) untuk memenuhi kebutuhan spesifik Anda.

## Masalah Umum & Pemecahan Masalah

| Gejala | Penyebab Kemungkinan | Perbaikan |
|---------|----------------------|-----------|
| Output gambar kosong | Tidak ada lapisan yang ditentukan atau nama lapisan salah | Verifikasi bahwa nama lapisan ada dalam file CAD; gunakan `image.getLayers()` untuk menampilkannya. |
| Resolusi rendah | DPI default rendah | Setel `rasterizationOptions.setResolution(300);` (atau lebih tinggi) sebelum menyimpan. |
| Format CAD tidak didukung | Menggunakan versi Aspose.CAD yang lebih lama | Perbarui ke rilis Aspose.CAD untuk Java terbaru. |

## Pertanyaan yang Sering Diajukan

**Q: Bisakah saya menggunakan Aspose.CAD untuk Java dengan bahasa pemrograman lain?**  
A: Aspose.CAD terutama mendukung Java, tetapi ada versi untuk .NET, C++, dan bahasa lain yang tersedia.

**Q: Di mana saya dapat menemukan dukungan atau bantuan tambahan?**  
A: Untuk pertanyaan atau bantuan, kunjungi [forum Aspose.CAD](https://forum.aspose.com/c/cad/19).

**Q: Apakah tersedia versi percobaan gratis?**  
A: Ya, Anda dapat menjelajahi Aspose.CAD dengan memperoleh versi percobaan gratis dari [sini](https://releases.aspose.com/).

**Q: Bagaimana cara mendapatkan lisensi sementara untuk Aspose.CAD?**  
A: Dapatkan lisensi sementara dari [tautan ini](https://purchase.aspose.com/temporary-license/).

**Q: Apakah ada persyaratan sistem khusus untuk Aspose.CAD untuk Java?**  
A: Pastikan Anda memiliki lingkungan pengembangan Java yang kompatibel; lihat dokumentasi untuk persyaratan detail.

---

**Terakhir Diperbarui:** 2026-04-13  
**Diuji Dengan:** Aspose.CAD for Java 24.12 (latest at time of writing)  
**Penulis:** Aspose

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}