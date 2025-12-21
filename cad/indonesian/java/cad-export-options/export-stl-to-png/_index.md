---
date: 2025-12-21
description: Pelajari cara mengekspor STL ke PNG menggunakan Aspose.CAD untuk Java
  – panduan langkah demi langkah yang mempermudah konversi file STL ke PNG dalam proyek
  Java Anda.
linktitle: Export STL to PNG
second_title: Aspose.CAD Java API
title: Ekspor STL ke PNG dengan Aspose.CAD untuk Java
url: /id/java/cad-export-options/export-stl-to-png/
weight: 20
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Ekspor STL ke PNG dengan Aspose.CAD untuk Java

## Pendahuluan

Jika Anda perlu **export stl to png** dengan cepat dan andal di lingkungan Java, Aspose.CAD untuk Java adalah alat yang sempurna. Dalam tutorial ini kami akan membahas semua yang Anda butuhkan—dari menyiapkan proyek hingga menyimpan gambar PNG berkualitas tinggi—sehingga Anda dapat mengintegrasikan aset visual 3‑D ke dalam aplikasi Anda dengan percaya diri.

## Jawaban Cepat
- **Apa arti “export stl to png”?** Itu mengonversi model STL 3‑D menjadi gambar raster PNG 2‑D.  
- **Library mana yang menangani konversi?** Aspose.CAD untuk Java menyediakan dukungan native untuk format STL dan PNG.  
- **Apakah saya memerlukan lisensi?** Lisensi Aspose.CAD sementara atau permanen diperlukan untuk penggunaan produksi.  
- **Berapa lama implementasinya?** Sekitar 10‑15 menit untuk skrip konversi dasar.  
- **Bisakah saya menyesuaikan ukuran gambar?** Ya – opsi rasterisasi memungkinkan Anda mengatur lebar dan tinggi khusus.

## Apa itu export stl to png?

Mengekspor STL ke PNG berarti mengambil mesh 3‑D (STL) dan merendernya sebagai gambar datar (PNG). Ini berguna ketika Anda ingin menampilkan pratinjau, menghasilkan thumbnail, atau menyematkan model dalam laporan tanpa memerlukan penampil 3‑D.

## Mengapa mengonversi STL ke PNG di Java?

- **Kompatibilitas lintas‑platform** – PNG bekerja di peramban, aplikasi seluler, dan antarmuka desktop.  
- **Kinerja** – Merender gambar statis jauh lebih cepat daripada memuat model 3‑D lengkap.  
- **Kesederhanaan** – Aspose.CAD menyederhanakan proses rasterisasi yang kompleks, memungkinkan Anda fokus pada logika bisnis.  

## Prasyarat

Sebelum Anda memulai, pastikan Anda memiliki:

- Java Development Kit (JDK) terpasang di mesin Anda.  
- Perpustakaan Aspose.CAD untuk Java sudah diunduh. Anda dapat mendapatkannya [di sini](https://releases.aspose.com/cad/java/).  
- Lisensi yang valid atau lisensi sementara dari [di sini](https://purchase.aspose.com/temporary-license/).  

## Impor Namespace

Tambahkan kelas Aspose.CAD yang diperlukan ke file sumber Java Anda:

```java
import com.aspose.cad.Image;

import com.aspose.cad.fileformats.dgn.DgnImage;
import com.aspose.cad.imageoptions.CadRasterizationOptions;
import com.aspose.cad.fileformats.cad.CadImage;
import com.aspose.cad.imageoptions.CadRasterizationOptions;
import com.aspose.cad.imageoptions.PngOptions;
```

Impor ini memberi Anda akses ke pemuatan gambar, rasterisasi, dan opsi khusus PNG.

## Panduan Langkah‑per‑Langkah

### Langkah 1: Siapkan Proyek Anda

Buat proyek Java baru (IDE pilihan Anda) dan tambahkan file JAR Aspose.CAD ke classpath proyek.

### Langkah 2: Tentukan File STL Anda (cara memuat stl)

Define the folder that contains the STL model you want to convert:

```java
String dataDir = "Your Document Directory" + "ExportingSTL/";
String fileName = dataDir + "example.stl";
```

> **Tip pro:** Simpan file STL Anda di folder sumber daya khusus untuk menghindari masalah jalur.

### Langkah 3: Muat File STL (konversi stl ke png)

Use the `Image.load` method to read the STL file into a `CadImage` object:

```java
CadImage cadImage = (CadImage)Image.load(fileName);
```

Pada titik ini geometri 3‑D siap untuk rasterisasi.

### Langkah 4: Konfigurasikan Opsi Rasterisasi (konversi 3d stl png)

Set the output dimensions and other raster settings. Adjust the width/height to match the desired PNG resolution:

```java
CadRasterizationOptions vectorOptions = new CadRasterizationOptions();
vectorOptions.setPageWidth(1500);
vectorOptions.setPageHeight(1500);
```

Anda juga dapat menyesuaikan warna latar belakang, ketebalan garis, atau anti‑aliasing di sini.

### Langkah 5: Konfigurasikan Opsi PNG (java konversi stl png)

Create a `PngOptions` instance and (optionally) attach the rasterization options:

```java
PngOptions pngOptions = new PngOptions();
// Uncomment the line below if you want to set vector rasterization options
// pngOptions.setVectorRasterizationOptions(vectorOptions);
```

Meninggalkan baris tersebut dalam komentar menggunakan pengaturan raster default, yang cukup untuk kebanyakan kasus.

### Langkah 6: Simpan sebagai PNG

Finally, write the rendered image to disk:

```java
String outPath = dataDir + "galeon.stl.png";
cadImage.save(outPath, pngOptions);
```

Sekarang Anda memiliki representasi PNG dari model STL asli Anda yang siap digunakan dalam komponen UI, halaman web, atau dokumentasi.

## Masalah Umum dan Solusinya

| Masalah | Penyebab | Solusi |
|-------|-------|-----|
| **Output PNG kosong** | Opsi rasterisasi tidak diatur atau ukuran nol | Pastikan `setPageWidth` dan `setPageHeight` memiliki nilai positif. |
| **OutOfMemoryError** | File STL sangat besar | Tingkatkan ukuran heap JVM (`-Xmx`) atau kurangi dimensi gambar. |
| **Lisensi tidak ditemukan** | File lisensi hilang atau tidak tepat | Letakkan file lisensi di classpath dan muat sebelum panggilan Aspose apa pun. |

## Kesimpulan

Anda telah berhasil mempelajari cara **export stl to png** menggunakan Aspose.CAD untuk Java. Alur kerja ini memungkinkan Anda menghasilkan pratinjau PNG berkualitas tinggi dari model STL apa pun, mempermudah tugas visualisasi dalam aplikasi berbasis Java.

## FAQ

### Q1: Apakah Aspose.CAD untuk Java kompatibel dengan semua versi file STL?

A1: Aspose.CAD untuk Java mendukung berbagai versi file STL, memastikan kompatibilitas dengan sebagian besar format umum.

### Q2: Bisakah saya menggunakan Aspose.CAD untuk Java dalam proyek komersial?

A2: Ya, Anda dapat. Cukup dapatkan lisensi yang valid dari [di sini](https://purchase.aspose.com/buy).

### Q3: Apakah saya memerlukan lisensi sementara untuk percobaan gratis?

A3: Tidak, lisensi sementara tidak diperlukan untuk percobaan gratis. Anda dapat memulai langsung dengan versi percobaan [di sini](https://releases.aspose.com/).

### Q4: Di mana saya dapat menemukan dukungan tambahan atau mengajukan pertanyaan?

A4: Kunjungi forum Aspose.CAD [di sini](https://forum.aspose.com/c/cad/19) untuk dukungan atau pertanyaan apa pun.

### Q5: Apakah ada dokumentasi lengkap yang tersedia?

A5: Ya, dokumentasi dapat ditemukan [di sini](https://reference.aspose.com/cad/java/).

## Pertanyaan yang Sering Diajukan

**Q: Bagaimana cara mengontrol warna latar belakang PNG yang diekspor?**  
A: Gunakan `vectorOptions.setBackgroundColor(Color.getWhite())` sebelum menetapkan opsi ke `pngOptions`.

**Q: Bisakah saya mengekspor beberapa file STL dalam proses batch?**  
A: Tentu – letakkan logika konversi di dalam loop yang mengiterasi daftar jalur file.

**Q: Apakah PNG mempertahankan transparansi?**  
A: Ya, PNG mendukung saluran alfa; Anda dapat mengaktifkannya melalui `pngOptions.setTransparent(true)` jika diperlukan.

**Q: Apakah memungkinkan mengekspor ke format raster lain (mis., JPEG, BMP)?**  
A: Aspose.CAD mendukung banyak format raster; cukup gunakan `JpegOptions`, `BmpOptions`, dll., alih-alih `PngOptions`.

**Q: Versi Aspose.CAD apa yang diperlukan untuk dukungan STL?**  
A: Dukungan STL telah tersedia sejak Aspose.CAD 20.x; menggunakan versi terbaru memastikan kompatibilitas penuh.

---

**Terakhir Diperbarui:** 2025-12-21  
**Diuji Dengan:** Aspose.CAD for Java 24.12  
**Penulis:** Aspose  

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}