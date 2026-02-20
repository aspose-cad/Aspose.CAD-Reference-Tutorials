---
date: 2026-02-20
description: Pelajari cara mengonversi STL ke PNG menggunakan Aspose.CAD untuk Java.
  Panduan langkah demi langkah ini menunjukkan cara mengekspor file STL secara efisien.
linktitle: Export STL to PNG
second_title: Aspose.CAD Java API
title: Cara Mengonversi STL ke PNG dengan Aspose.CAD untuk Java
url: /id/java/cad-export-options/export-stl-to-png/
weight: 20
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Mengonversi STL ke PNG dengan Aspose.CAD untuk Java

## Pendahuluan

Jika Anda perlu **mengonversi STL ke PNG** dalam aplikasi Java, Aspose.CAD untuk Java membuat pekerjaan ini cepat dan dapat diandalkan. Dalam tutorial ini kami akan membahas seluruh proses—dari menyiapkan proyek Anda hingga menyimpan gambar PNG akhir—sehingga Anda dapat mengintegrasikan konversi STL ke dalam alur kerja Anda dengan percaya diri.

## Jawaban Cepat
- **Apa yang dilakukan perpustakaan ini?** Ia mengonversi format CAD (termasuk STL) menjadi gambar raster seperti PNG.  
- **Bahasa apa yang digunakan?** Java, dengan API Aspose.CAD.  
- **Apakah saya memerlukan lisensi?** Lisensi sementara atau penuh diperlukan untuk penggunaan produksi.  
- **Berapa lama implementasinya?** Sekitar 10‑15 menit untuk konversi dasar.  
- **Bisakah saya menyesuaikan ukuran gambar?** Ya, melalui `CadRasterizationOptions`.

## Apa itu mengonversi STL ke PNG?

Mengonversi STL ke PNG mengubah file mesh 3‑D (STL) menjadi gambar raster 2‑D (PNG). Ini berguna ketika Anda memerlukan pratinjau visual cepat, menghasilkan thumbnail, atau menyematkan model dalam halaman web tanpa memerlukan penampil 3‑D.

## Mengapa menggunakan Aspose.CAD untuk Java?

- **API lengkap** – Menangani banyak format CAD, tidak hanya STL.  
- **Tanpa dependensi eksternal** – Murni Java, mudah ditambahkan ke proyek Maven/Gradle apa pun.  
- **Output raster berkualitas tinggi** – Kontrol atas resolusi, latar belakang, dan anti‑aliasing.  
- **Mendukung skenario “cara mengekspor STL”** – Ideal untuk pemrosesan batch atau konversi secara langsung.

## Prasyarat

Sebelum memulai, pastikan Anda memiliki:

- Java Development Kit (JDK) terpasang di mesin Anda.  
- Perpustakaan Aspose.CAD untuk Java diunduh. Anda dapat mendapatkannya [di sini](https://releases.aspose.com/cad/java/).  
- Lisensi yang valid atau lisensi sementara dari [di sini](https://purchase.aspose.com/temporary-license/).

## Impor Namespace

Dalam proyek Java Anda, impor kelas yang diperlukan:

```java
import com.aspose.cad.Image;

import com.aspose.cad.fileformats.dgn.DgnImage;
import com.aspose.cad.imageoptions.CadRasterizationOptions;
import com.aspose.cad.fileformats.cad.CadImage;
import com.aspose.cad.imageoptions.CadRasterizationOptions;
import com.aspose.cad.imageoptions.PngOptions;
```

Sekarang, mari kita uraikan contoh ini menjadi beberapa langkah.

## Langkah 1: Siapkan Proyek Anda

Buat proyek Java baru dan tambahkan perpustakaan Aspose.CAD untuk Java ke dependensi proyek Anda (Maven, Gradle, atau penyertaan JAR manual).

## Langkah 2: Tentukan File STL Anda

Tentukan jalur ke file STL yang ingin Anda konversi:

```java
String dataDir = "Your Document Directory" + "ExportingSTL/";
String fileName = dataDir + "example.stl";
```

## Langkah 3: Muat File STL

Muat file STL menggunakan metode `Image.load`. Ini membuat objek **gambar CAD** yang dapat Anda rasterisasi:

```java
CadImage cadImage = (CadImage)Image.load(fileName);
```

## Langkah 4: Konfigurasikan Opsi Rasterisasi

Siapkan opsi rasterisasi untuk mengontrol ukuran dan kualitas PNG output. Opsi-opsi ini merupakan bagian dari proses konversi **cad image to png**:

```java
CadRasterizationOptions vectorOptions = new CadRasterizationOptions();
vectorOptions.setPageWidth(1500);
vectorOptions.setPageHeight(1500);
```

## Langkah 5: Konfigurasikan Opsi PNG

Buat instance `PngOptions`. Jika Anda ingin menerapkan pengaturan rasterisasi, hapus komentar pada baris di bawah ini:

```java
PngOptions pngOptions = new PngOptions();
// Uncomment the line below if you want to set vector rasterization options
// pngOptions.setVectorRasterizationOptions(vectorOptions);
```

## Langkah 6: Simpan sebagai PNG

Akhirnya, ekspor gambar CAD ke file PNG—ini adalah langkah **save PNG Java**:

```java
String outPath = dataDir + "galeon.stl.png";
cadImage.save(outPath, pngOptions);
```

> **Tip pro:** Sesuaikan `PageWidth` dan `PageHeight` agar sesuai dengan dimensi thumbnail yang diinginkan untuk pemrosesan lebih cepat.

Selamat! Anda telah berhasil **mengonversi file STL ke PNG** menggunakan Aspose.CAD untuk Java.

## Masalah Umum dan Solusinya

| Masalah | Alasan | Solusi |
|-------|--------|----------|
| Output PNG kosong | Opsi rasterisasi tidak diatur | Hapus komentar `pngOptions.setVectorRasterizationOptions(vectorOptions);` atau tentukan warna latar belakang |
| OutOfMemoryError pada file STL besar | Memori heap tidak cukup | Tingkatkan heap JVM (`-Xmx2g`) atau proses file secara bertahap |
| LicenseException | Tidak ada lisensi yang valid | Terapkan lisensi sementara atau yang dibeli sebelum memuat gambar |

## Pertanyaan yang Sering Diajukan

### Q1: Apakah Aspose.CAD untuk Java kompatibel dengan semua versi file STL?
A1: Aspose.CAD untuk Java mendukung berbagai versi file STL, memastikan kompatibilitas dengan sebagian besar format umum.

### Q2: Bisakah saya menggunakan Aspose.CAD untuk Java dalam proyek komersial?
A2: Ya, Anda dapat. Cukup dapatkan lisensi yang valid dari [di sini](https://purchase.aspose.com/buy).

### Q3: Apakah saya memerlukan lisensi sementara untuk percobaan gratis?
A3: Tidak, lisensi sementara tidak diperlukan untuk percobaan gratis. Anda dapat memulai langsung dengan versi percobaan [di sini](https://releases.aspose.com/).

### Q4: Di mana saya dapat menemukan dukungan tambahan atau mengajukan pertanyaan?
A4: Kunjungi forum Aspose.CAD [di sini](https://forum.aspose.com/c/cad/19) untuk dukungan atau pertanyaan apa pun.

### Q5: Apakah ada dokumentasi komprehensif yang tersedia?
A5: Ya, dokumentasi dapat ditemukan [di sini](https://reference.aspose.com/cad/java/).

## Kesimpulan

Dalam panduan ini kami menunjukkan cara **mengonversi STL ke PNG** secara efisien menggunakan Aspose.CAD untuk Java. Dengan mengikuti langkah-langkah di atas, Anda dapat mengintegrasikan konversi STL‑to‑PNG ke dalam pipeline berbasis Java apa pun, baik Anda membangun utilitas desktop, layanan web, atau alat pelaporan otomatis.

---

**Terakhir Diperbarui:** 2026-02-20  
**Diuji Dengan:** Aspose.CAD untuk Java 24.12 (terbaru pada saat penulisan)  
**Penulis:** Aspose  

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}