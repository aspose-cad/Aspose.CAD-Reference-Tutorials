---
date: 2026-10-19
description: Pelajari cara membuat file thumbnail PNG IFC dengan Aspose.CAD for Java
  hanya dalam beberapa baris kode.
keywords:
- create png thumbnail ifc
- ifc to png conversion
- aspose cad java
- java image processing
- bIM visualization
lastmod: 2026-10-19
linktitle: Ekspor IFC ke PNG
og_description: Buat file thumbnail PNG IFC dengan mudah menggunakan Aspose.CAD for
  Java. Panduan langkah demi langkah ini menunjukkan cara memuat, meraster, dan menyimpan
  model IFC sebagai gambar PNG berkualitas tinggi.
og_image_alt: Developer guide showing Java code that converts IFC files to PNG thumbnails
  using Aspose.CAD
og_title: Buat thumbnail PNG IFC dengan Aspose.CAD for Java
schemas:
- author: Aspose
  dateModified: '2026-10-19'
  description: Learn how to create PNG thumbnail IFC files with Aspose.CAD for Java
    in just a few lines of code.
  headline: How to create PNG thumbnail IFC with Aspose.CAD for Java
  type: TechArticle
- description: Learn how to create PNG thumbnail IFC files with Aspose.CAD for Java
    in just a few lines of code.
  name: How to create PNG thumbnail IFC with Aspose.CAD for Java
  steps:
  - name: load the IFC file
    text: First, point to the folder where your IFC file lives and load it with `CadImage.load`.
      `CadImage.load` reads a CAD file and returns an image object that can be rasterized.
      > **Why this matters:** Loading the file as a `CadImage` gives you access to
      vector‑raster conversion options that control resol
  - name: set rasterization options
    text: Define the output dimensions and any other vector‑related settings through
      `VectorRasterizationOptions`. `VectorRasterizationOptions` lets you specify
      output size, background color, and other rasterization parameters. > Adjust
      `PageWidth` and `PageHeight` to control the final PNG resolution, which i
  - name: configure PNG options
    text: Link the rasterization options to the PNG exporter by creating a `PngOptions`
      instance.
  - name: save the image as PNG
    text: Finally, write the rasterized image to disk using the `save` method. `save`
      writes the rasterized image to the specified file path in the chosen format.
      > After this step you have successfully **created a PNG thumbnail IFC** and
      can use the resulting `example.png` anywhere you need a raster image.
  type: HowTo
- questions:
  - answer: Yes, Aspose.CAD supports many formats (DWG, DXF, DGN, etc.). Simply change
      the file extension and load the appropriate image class.
    question: Can I use this approach to convert other CAD formats to PNG?
  - answer: DPI is controlled indirectly via `PageWidth`/`PageHeight`. Adjust these
      values relative to the desired physical size to achieve the required DPI.
    question: Does the library let me set a custom DPI?
  - answer: PNG is a lossless format, so the rasterized image retains the full visual
      fidelity of the original vector data.
    question: Is the PNG output loss‑less?
  type: FAQPage
second_title: Aspose.CAD Java API
tags:
- ifc conversion
- png thumbnail
- aspose.cad
- java image processing
- bim visualization
title: Cara membuat thumbnail PNG IFC dengan Aspose.CAD for Java
url: /id/java/cad-export-options/export-ifc-to-png/
weight: 18
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Ekspor IFC ke PNG dengan Aspose.CAD untuk Java

## Pendahuluan

Dalam tutorial ini Anda akan belajar cara **create PNG thumbnail IFC** file dengan Aspose.CAD untuk Java. Apakah Anda membutuhkan preview cepat untuk portal BIM, menghasilkan thumbnail untuk sistem manajemen dokumen, atau mengotomatisasi konversi batch, langkah-langkah di bawah ini memungkinkan Anda merasterisasi model IFC 3‑D menjadi gambar PNG 2‑D yang tajam hanya dengan beberapa baris kode Java.

## Jawaban Cepat
- **Library apa yang diperlukan?** Aspose.CAD for Java.  
- **Bisakah saya membuat PNG thumbnail IFC dalam beberapa baris kode?** Ya – seluruh alur kerja muat dalam kurang dari 20 baris.  
- **Apakah saya memerlukan lisensi untuk produksi?** Lisensi sementara berfungsi untuk pengujian; lisensi penuh diperlukan untuk penyebaran komersial.  
- **Apakah output dapat diskalakan?** Anda dapat mengatur dimensi piksel apa pun, sehingga PNG dapat diskalakan ke ukuran apa pun yang Anda butuhkan.  
- **Versi Java apa yang didukung?** Java 8 atau lebih tinggi.

## Apa itu “convert IFC to PNG”?
Mengonversi IFC (Industry Foundation Classes) ke PNG berarti merasterisasi model bangunan 3‑D menjadi gambar bitmap 2‑D. Proses ini membuat thumbnail visual yang dapat ditampilkan di peramban, laporan, atau aplikasi seluler tanpa memerlukan penampil CAD lengkap.

## Mengapa menggunakan Aspose.CAD untuk Java?
Aspose.CAD mendukung **30+ format CAD dan BIM**, termasuk IFC, DWG, DXF, dan DGN, dan dapat memproses file hingga **2 GB** tanpa memuat seluruh dokumen ke memori. Library ini murni Java, memiliki **nol ketergantungan eksternal**, dan berjalan di Windows, Linux, serta macOS, menjadikannya ideal untuk pembuatan gambar sisi‑server.  
Ia menyediakan rasterisasi berperforma tinggi, dukungan format yang luas, dan integrasi mudah ke dalam aplikasi Java.

## Prasyarat

- **Aspose.CAD Library** – unduh JAR terbaru dari [download link](https://releases.aspose.com/cad/java/).  
- **Java Development Kit** – JDK 8 atau lebih baru terpasang di mesin Anda.  
- **IFC source file** – letakkan file di folder yang dapat Anda referensikan dari kode Anda.

## Impor namespace

Paket `com.aspose.cad` menyediakan semua kelas yang Anda perlukan. `CadImage` adalah titik masuk untuk memuat file CAD, sementara `PngOptions` mengonfigurasi pengaturan rasterisasi.

```java
import com.aspose.cad.Image;

import com.aspose.cad.fileformats.ifc.IfcImage;
import com.aspose.cad.imageoptions.CadRasterizationOptions;
import com.aspose.cad.imageoptions.PngOptions;
```

## Cara membuat PNG thumbnail IFC di Java?

Muat file IFC, tentukan opsi rasterisasi, dan simpan hasilnya sebagai gambar PNG – itulah alur kerja konversi lengkap. Bagian-bagian berikut memecah setiap langkah, sehingga Anda dapat menyalin‑tempel potongan kode ke dalam proyek Anda dan menjalankannya segera.

### Langkah 1: muat file IFC
Pertama, arahkan ke folder tempat file IFC Anda berada dan muat dengan `CadImage.load`.  
`CadImage.load` membaca file CAD dan mengembalikan objek gambar yang dapat dirasterisasi.

```java
String dataDir = "Your Document Directory" + "ExportingIFC/";
String fileName = dataDir + "example.ifc";
IfcImage cadImage = (IfcImage)Image.load(fileName);
```

> **Mengapa ini penting:** Memuat file sebagai `CadImage` memberi Anda akses ke opsi konversi vektor‑raster yang mengontrol resolusi, warna latar belakang, dan ketebalan garis.

### Langkah 2: atur opsi rasterisasi
Tentukan dimensi output dan pengaturan terkait vektor lainnya melalui `VectorRasterizationOptions`.  
`VectorRasterizationOptions` memungkinkan Anda menentukan ukuran output, warna latar belakang, dan parameter rasterisasi lainnya.

```java
CadRasterizationOptions vectorOptions = new CadRasterizationOptions();
vectorOptions.setPageWidth(1500);
vectorOptions.setPageHeight(1500);
```

> Sesuaikan `PageWidth` dan `PageHeight` untuk mengontrol resolusi PNG akhir, yang penting ketika Anda **save PNG java** file untuk cetakan berkualitas tinggi atau thumbnail web.

### Langkah 3: konfigurasikan opsi PNG
Hubungkan opsi rasterisasi ke pengekspor PNG dengan membuat instance `PngOptions`.

```java
PngOptions pngOptions = new PngOptions();
pngOptions.setVectorRasterizationOptions(vectorOptions);
```

### Langkah 4: simpan gambar sebagai PNG
Akhirnya, tulis gambar yang dirasterisasi ke disk menggunakan metode `save`.  
`save` menulis gambar yang dirasterisasi ke jalur file yang ditentukan dalam format yang dipilih.

```java
String outPath = dataDir + "example.png";
cadImage.save(outPath, pngOptions);
```

> Setelah langkah ini Anda telah berhasil **created a PNG thumbnail IFC** dan dapat menggunakan `example.png` yang dihasilkan di mana saja Anda membutuhkan gambar raster.

## Kasus penggunaan umum
- **Membuat thumbnail** untuk model BIM di portal web.  
- **Menyematkan snapshot denah lantai** ke dalam laporan PDF atau Word.  
- **Konversi batch otomatis** perpustakaan IFC besar untuk proyek arsip atau migrasi.

## Pemecahan Masalah & Tips
- **Masalah memori:** Untuk file IFC yang sangat besar, tingkatkan heap JVM (`-Xmx2g` atau lebih tinggi).  
- **Tekstur hilang:** Pastikan sumber daya eksternal file IFC dapat dijangkau dari `dataDir`.  
- **Tips pro:** Gunakan `vectorOptions.setBackgroundColor(Color.getWhite())` jika Anda lebih suka latar belakang putih daripada PNG transparan default.

## FAQ

### Q1: Apakah Aspose.CAD kompatibel dengan semua versi file IFC?
A1: Aspose.CAD mendukung berbagai versi IFC. Lihat [documentation](https://reference.aspose.com/cad/java/) untuk informasi kompatibilitas detail.

### Q2: Bisakah saya menyesuaikan opsi rasterisasi lebih lanjut?
A2: Tentu saja! Jelajahi [documentation](https://reference.aspose.com/cad/java/) untuk pengaturan lanjutan seperti kontrol DPI, anti‑aliasing, dan ketebalan garis.

### Q3: Apakah ada versi percobaan yang tersedia?
A3: Ya, Anda dapat mengunduh percobaan gratis dari [Aspose.CAD free trial](https://releases.aspose.com/).

### Q4: Bagaimana saya dapat memperoleh lisensi sementara untuk pengujian?
A4: Dapatkan lisensi sementara dari [Aspose.CAD temporary license page](https://purchase.aspose.com/temporary-license/).

### Q5: Di mana saya dapat mengajukan pertanyaan atau melaporkan masalah?
A5: Bergabunglah dengan komunitas di [Aspose.CAD forum](https://forum.aspose.com/c/cad/19) untuk dukungan dari insinyur Aspose dan sesama pengembang.

## Pertanyaan yang Sering Diajukan

**Q: Bisakah saya menggunakan pendekatan ini untuk mengonversi format CAD lain ke PNG?**  
A: Ya, Aspose.CAD mendukung banyak format (DWG, DXF, DGN, dll.). Cukup ubah ekstensi file dan muat kelas gambar yang sesuai.

**Q: Apakah library memungkinkan saya mengatur DPI khusus?**  
A: DPI dikontrol secara tidak langsung melalui `PageWidth`/`PageHeight`. Sesuaikan nilai ini relatif terhadap ukuran fisik yang diinginkan untuk mencapai DPI yang diperlukan.

**Q: Apakah output PNG loss‑less?**  
A: PNG adalah format lossless, sehingga gambar yang dirasterisasi mempertahankan fidelitas visual penuh dari data vektor asli.

## Kesimpulan

Anda kini memiliki metode lengkap, siap produksi untuk **create PNG thumbnail IFC** file menggunakan Aspose.CAD untuk Java. Integrasikan langkah-langkah ini ke dalam alat desktop, layanan sisi‑server, atau fungsi cloud untuk mengotomatisasi pipeline visualisasi BIM dan menyajikan thumbnail berkualitas tinggi dengan cepat kepada pengguna akhir.

---

**Terakhir Diperbarui:** 2026-10-19  
**Diuji Dengan:** Aspose.CAD for Java 24.11  
**Penulis:** Aspose

## Tutorial Terkait

- [Cara Mengonversi STL ke PNG dengan Aspose.CAD untuk Java](/cad/java/cad-export-options/export-stl-to-png/)
- [Konversi DWG ke PNG – Simpan CAD sebagai PNG Menggunakan Aspose.CAD untuk Java](/cad/java/cad-drawing-conversion/convert-cad-drawing-to-raster-image/)
- [Ekspor DWG ke PDF di Java – Atur Ukuran Halaman PDF dengan Aspose.CAD](/cad/java/cad-export-options/export-to-pdf/)

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}