---
date: 2025-12-21
description: Pelajari cara mengonversi DWG ke BMP dan mengekspor CAD ke BMP menggunakan
  Aspose.CAD untuk Java dengan panduan langkah demi langkah ini.
linktitle: Export to BMP
second_title: Aspose.CAD Java API
title: Cara Mengonversi DWG ke BMP dengan Aspose.CAD untuk Java
url: /id/java/cad-export-options/export-to-bmp/
weight: 12
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Mengonversi DWG ke BMP dengan Aspose.CAD untuk Java

## Pendahuluan

Dalam alur kerja desain digital modern, kemampuan untuk **mengonversi DWG ke BMP** dengan cepat dan andal sangat penting. Baik Anda membangun layanan pemrosesan batch maupun membutuhkan konversi satu berkas, Aspose.CAD untuk Java menyediakan API yang kuat untuk **mengekspor CAD ke BMP** dengan kontrol penuh atas pengaturan rasterisasi. Pada tutorial ini Anda akan melewati setiap langkah—dari memuat berkas DWG hingga menyimpan gambar BMP akhir—sehingga Anda dapat mengintegrasikan konversi ke dalam aplikasi Java Anda dengan percaya diri.

## Jawaban Cepat
- **Perpustakaan apa yang dibutuhkan?** Aspose.CAD untuk Java.  
- **Bisakah saya mengonversi DWG ke BMP dalam satu baris kode?** Tidak, Anda harus memuat berkas, mengatur opsi rasterisasi, lalu menyimpan.  
- **Apakah lisensi diperlukan untuk produksi?** Ya, lisensi komersial diperlukan; tersedia versi percobaan gratis.  
- **Apakah API mendukung konversi batch?** Tentu—lakukan perulangan pada berkas-berkas dan gunakan kembali opsi yang sama.  
- **Versi Java apa yang didukung?** Java 8 dan yang lebih baru.

## Apa itu “mengonversi DWG ke BMP”?

Mengonversi berkas DWG (gambar AutoCAD) ke BMP (bitmap) meraster data vektor menjadi format berbasis piksel. Ini berguna ketika Anda memerlukan gambar yang dapat dilihat secara universal untuk laporan, thumbnail, atau pratinjau web tanpa memerlukan perangkat lunak CAD.

## Mengapa menggunakan Aspose.CAD untuk Java untuk mengekspor CAD ke BMP?

- **Tanpa dependensi eksternal** – murni Java, tanpa DLL native.  
- **Rasterisasi halus** – kontrol ukuran halaman, tata letak, anti‑aliasing.  
- **Fidelity tinggi** – mempertahankan ketebalan garis, warna, dan lapisan.  
- **Skalabel** – bekerja untuk berkas tunggal maupun pekerjaan batch besar.

## Prasyarat

Sebelum masuk ke kode, pastikan Anda memiliki:

- **Perpustakaan Aspose.CAD untuk Java** – unduh dari [sini](https://releases.aspose.com/cad/java/).  
- **Lingkungan Pengembangan Java** – JDK 8+ dan IDE pilihan Anda.  
- **Pengetahuan Dasar Java** – familiar dengan kelas, metode, dan I/O berkas.

## Impor Namespace

Di proyek Java Anda, impor namespace yang diperlukan untuk mengakses fungsionalitas Aspose.CAD:

```java
import com.aspose.cad.Image;
import com.aspose.cad.InterpolationMode;
import com.aspose.cad.SmoothingMode;
import com.aspose.cad.TextRenderingHint;

import com.aspose.cad.imageoptions.BmpOptions;
import com.aspose.cad.imageoptions.CadRasterizationOptions;
import com.aspose.cad.imageoptions.PdfOptions;
//import com.aspose.cad.imageoptions.TypeOfEntities;
```

## Langkah 1: Tetapkan Jalur Direktori Sumber Daya

Definisikan folder yang berisi berkas DWG (atau CAD lainnya) yang ingin Anda konversi.

```java
String dataDir = "Your Document Directory" + "ExportingCAD/";
```

## Langkah 2: Muat Berkas CAD

Buat objek `Image` dengan memuat berkas DWG sumber.

```java
String fileName = (dataDir + "site.dwf");
Image image = Image.load(fileName);
```

## Langkah 3: Konfigurasikan Opsi Ekspor BMP

Instansiasi `BmpOptions` dan lampirkan objek `CadRasterizationOptions` yang mengontrol cara data vektor dirasterisasi.

```java
BmpOptions bmpOptions = new BmpOptions();
CadRasterizationOptions rasterizationOptions = new CadRasterizationOptions();
bmpOptions.setVectorRasterizationOptions(rasterizationOptions);
```

## Langkah 4: Atur Parameter Rasterisasi

Sesuaikan dimensi halaman dan tentukan tata letak mana yang akan dirender. Pengaturan ini secara langsung memengaruhi kualitas dan ukuran BMP yang dihasilkan.

```java
rasterizationOptions.setPageHeight(500);
rasterizationOptions.setPageWidth(500);
rasterizationOptions.setLayouts(new String[] { "Model" });
```

## Langkah 5: Ekspor ke BMP

Berikan jalur output dan panggil `save` untuk menulis berkas BMP.

```java
String outPath = dataDir + "site.bmp";
image.save(outPath, bmpOptions);
```

Ulangi langkah-langkah di atas untuk setiap berkas CAD yang ingin Anda **konversi DWG ke BMP** menggunakan Aspose.CAD untuk Java.

## Masalah Umum & Tips

- **Nama tata letak tidak tepat** – Pastikan string tata letak cocok dengan salah satu tata letak yang didefinisikan dalam berkas DWG Anda (misalnya, `"Model"` atau `"Layout1"`).  
- **Output beresolusi rendah** – Tingkatkan `PageWidth` dan `PageHeight` untuk hasil DPI yang lebih tinggi.  
- **Konsumsi memori** – Untuk gambar yang sangat besar, pertimbangkan memproses berkas satu per satu dan membuang objek `Image` setelah setiap penyimpanan.

## FAQ's

### Q1: Apakah Aspose.CAD untuk Java cocok untuk pemrosesan batch?

A1: Tentu! Aspose.CAD untuk Java mendukung pemrosesan batch, memungkinkan Anda menangani banyak berkas CAD secara bersamaan dengan efisien.

### Q2: Bisakah saya menyesuaikan opsi rasterisasi untuk tata letak yang berbeda?

A2: Ya, Anda dapat menyesuaikan opsi rasterisasi seperti dimensi halaman dan tata letak sesuai kebutuhan spesifik Anda.

### Q3: Di mana saya dapat menemukan dukungan tambahan untuk Aspose.CAD untuk Java?

A3: Kunjungi [forum Aspose.CAD](https://forum.aspose.com/c/cad/19) untuk dukungan komunitas dan diskusi.

### Q4: Apakah tersedia versi percobaan gratis?

A4: Ya, Anda dapat menjelajahi versi percobaan gratis Aspose.CAD untuk Java [di sini](https://releases.aspose.com/).

### Q5: Bagaimana cara memperoleh lisensi sementara?

A5: Dapatkan lisensi sementara untuk Aspose.CAD untuk Java [di sini](https://purchase.aspose.com/temporary-license/).

## Pertanyaan yang Sering Diajukan

**T: Bisakah saya mengonversi format CAD lain (mis., DXF, DGN) ke BMP?**  
J: Ya, API yang sama bekerja dengan DXF, DGN, DWF, dan format lain yang didukung.

**T: Apakah konversi mempertahankan visibilitas lapisan?**  
J: Secara default semua lapisan yang terlihat dirasterisasi; Anda dapat menyembunyikan lapisan melalui `CadRasterizationOptions` bila diperlukan.

**T: Apakah dapat mengatur warna latar belakang untuk BMP?**  
J: Ya, gunakan `rasterizationOptions.setBackgroundColor(Color.getWhite());` sebelum menyimpan.

**T: Bagaimana menangani berkas CAD yang dilindungi kata sandi?**  
J: Muat berkas dengan `Image.load(fileName, loadOptions)` dimana `loadOptions` mencakup kata sandi.

**T: Apa cara terbaik meningkatkan kinerja untuk batch besar?**  
J: Gunakan satu instance `BmpOptions` dan hanya ubah jalur berkas input untuk setiap iterasi.

## Kesimpulan

Dengan mengikuti panduan ini, Anda kini memiliki dasar yang kuat untuk **mengonversi DWG ke BMP** dan **mengekspor CAD ke BMP** menggunakan Aspose.CAD untuk Java. Integrasikan langkah-langkah ini ke dalam aplikasi Anda untuk mengotomatisasi pembuatan gambar, membuat thumbnail, atau menyiapkan aset untuk pemrosesan lanjutan.

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}

---

**Terakhir Diperbarui:** 2025-12-21  
**Diuji Dengan:** Aspose.CAD untuk Java 24.11  
**Penulis:** Aspose  

---