---
date: 2026-10-25
description: Pelajari cara mengonversi DWG ke PDF, mengekspor tata letak CAD, file
  BMP, IFC, dan STL menggunakan Aspose.CAD for Java. Termasuk catatan lisensi, tips
  kinerja, dan contoh penggunaan dunia nyata.
keywords:
- convert dwg to pdf
- cad layout pdf export
- generate pdf from dwg
- java convert cad pdf
- export stl to png
lastmod: 2026-10-25
linktitle: Opsi Ekspor CAD
og_description: Konversi DWG ke PDF, BMP, IFC, dan STL dengan Aspose.CAD for Java.
  Pelajari langkah demi langkah, lihat angka kinerja, dan dapatkan panduan lisensi
  dalam panduan 2026 ini.
og_image_alt: Screenshot of Aspose.CAD Java API converting DWG to PDF
og_title: Konversi DWG ke PDF dan opsi ekspor CAD lainnya di Java
schemas:
- author: Aspose
  dateModified: '2026-10-25'
  description: Learn how to convert DWG to PDF, export CAD layouts, BMP, IFC, and
    STL files using Aspose.CAD for Java. Includes licensing notes, performance tips,
    and real‑world use cases.
  headline: How to convert DWG to PDF and other CAD export options in Java
  type: TechArticle
- questions:
  - answer: Load the IFC file with `Image.load("model.ifc")` and call `save("model.png",
      new PngOptions())`.
    question: How do I convert IFC to PNG using Aspose.CAD?
  - answer: Yes—Aspose.CAD treats layouts as images internally, so `save("layout.pdf",
      new PdfOptions())` handles it automatically.
    question: Can I export a CAD layout directly to PDF without converting to an image
      first?
  - answer: Exporting an AutoCAD drawing converts the entire drawing, while exporting
      a layout targets a specific paper‑space view, preserving its page settings.
    question: What is the difference between exporting AutoCAD to PDF and exporting
      a CAD layout to PDF?
  - answer: No inherent limit; each layout becomes a separate page in the resulting
      PDF.
    question: Is there a limit on the number of pages when exporting a multi‑sheet
      DWG to PDF?
  - answer: A single Aspose.CAD license covers all supported formats (PDF, PNG, BMP,
      etc.).
    question: Do I need a separate license for each export format?
  type: FAQPage
second_title: Aspose.CAD Java API
tags:
- convert dwg to pdf
- Aspose.CAD
- Java CAD conversion
- CAD export tutorials
title: Cara mengonversi DWG ke PDF dan opsi ekspor CAD lainnya di Java
url: /id/java/cad-export-options/
weight: 30
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Opsi ekspor CAD

## Pendahuluan

Jika Anda seorang pengembang Java yang perlu **mengonversi DWG ke PDF** dengan cepat dan dapat diandalkan, Anda berada di tempat yang tepat. Panduan ini membahas skenario ekspor paling umum Aspose.CAD untuk Java—termasuk gambar AutoCAD, tata letak CAD, BMP, PDF, IFC, dan file STL. Anda akan melihat mengapa fitur-fitur ini penting dalam proyek dunia nyata, mempelajari tips praktik terbaik, dan mendapatkan potongan kode siap salin untuk aplikasi Anda.

## Jawaban cepat
- **Apa cara termudah untuk mengekspor AutoCAD ke PDF?** Gunakan `Image.save("output.pdf", new PdfOptions())` dari Aspose.CAD.  
- **Format apa saja yang dapat saya konversi dari file IFC?** PNG didukung sepenuhnya; cukup muat file IFC dan simpan sebagai PNG.  
- **Bisakah saya mengekspor file STL langsung ke PNG?** Ya—muat model STL dan panggil `save("image.png")`.  
- **Apakah saya memerlukan lisensi untuk penggunaan produksi?** Lisensi komersial diperlukan untuk penerapan non‑trial.  
- **Versi Java apa yang diperlukan?** Java 8 atau lebih tinggi disarankan.

## Apa itu ekspor AutoCAD ke PDF?

Mengekspor gambar AutoCAD ke PDF berarti mengonversi file DWG/DXF berbasis vektor menjadi format halaman yang diterima secara luas. PDF mempertahankan lapisan, ketebalan garis, dan warna, menjadikannya ideal untuk berbagi desain dengan klien, peninjau, atau sistem hilir yang tidak memahami file CAD asli.

## Mengapa menggunakan Aspose.CAD untuk Java?

Aspose.CAD untuk Java adalah perpustakaan **pure‑Java**—tidak memerlukan DLL native atau interop COM. Ia mereproduksi geometri, teks, dan data raster dengan **ketelitian tinggi**, mendukung **pemrosesan batch** ribuan file, dan menangani **lebih dari 60 format input dan output** (termasuk DWG, DXF, IFC, STL, BMP, PNG, dan PDF). Pipeline yang efisien dalam penggunaan memori memungkinkan Anda memproses gambar beratus‑ratus halaman tanpa memuat seluruh file ke RAM.

## Mengapa ini penting

Kemampuan **mengonversi DWG ke PDF** secara langsung memungkinkan Anda mengotomatisasi pembuatan laporan, membuat deliverable siap klien, dan menyematkan data CAD ke portal web tanpa mengekspos file DWG mentah. API yang sama juga menghasilkan ekspor berbasis gambar (BMP, PNG) untuk thumbnail, pemeriksaan visual cepat, dan pratinjau ringan.

## Prasyarat
- Java 8 atau lebih baru terpasang.  
- Perpustakaan Aspose.CAD untuk Java ditambahkan ke proyek Anda (Maven, Gradle, atau JAR manual).  
- Lisensi Aspose yang valid untuk penggunaan produksi (versi percobaan gratis tersedia untuk evaluasi).

## Cara mengonversi DWG ke PDF dalam Java

`Image` adalah kelas inti Aspose.CAD yang mewakili dokumen CAD dalam memori.  
`PdfOptions` mengonfigurasi pengaturan output khusus PDF seperti resolusi dan kompresi.

Muat DWG (atau format CAD lain yang didukung) dengan `Image.load`, lalu panggil `save` menggunakan instance `PdfOptions`. Pola dua langkah ini menangani konversi vektor‑ke‑PDF, mempertahankan lapisan, dan memungkinkan Anda menyesuaikan DPI atau pengaturan kompresi.

Kelas `Image` mewakili dokumen CAD apa pun yang didukung dalam memori, sementara `PdfOptions` mengonfigurasi PDF output. Tidak diperlukan alat konversi tambahan atau utilitas eksternal.

### Langkah 1: muat file DWG
```java
// Load a DWG file – the Image class is the entry point for all Aspose.CAD operations
com.aspose.cad.Image cadImage = com.aspose.cad.Image.load("sample.dwg");
```

### Langkah 2: konfigurasikan opsi PDF (opsional)
```java
// Create PDF options – you can set vector rasterization DPI, compression, etc.
com.aspose.cad.imageoptions.PdfOptions pdfOptions = new com.aspose.cad.imageoptions.PdfOptions();
pdfOptions.setVectorRasterizationOptions(
    new com.aspose.cad.imageoptions.VectorRasterizationOptions()
        .setPageWidth(2100)   // width in pixels (A4 at 300 DPI)
        .setPageHeight(2970)  // height in pixels
        .setResolution(300)   // 300 DPI for high‑quality output
);
```

### Langkah 3: simpan sebagai PDF
```java
// Save the loaded DWG as a PDF file
cadImage.save("output.pdf", pdfOptions);

// Release resources – important when processing many files in a loop
cadImage.dispose();
```

Ketiga baris di atas membentuk alur kerja **konversi DWG ke PDF** lengkap. Anda dapat menempatkannya dalam loop untuk memproses batch direktori gambar.

## Ekspor tata letak CAD ke PDF

Mengekspor tata letak tertentu (view paper‑space) bekerja dengan cara yang sama karena Aspose.CAD memperlakukan setiap tata letak sebagai gambar secara internal. Cukup muat DWG, pilih tata letak berdasarkan nama jika diperlukan, dan panggil `save` dengan `PdfOptions`. Tidak ada langkah konversi tambahan yang diperlukan.

## Ekspor ke BMP

`BmpOptions` menentukan parameter output format BMP seperti kedalaman bit dan resolusi. Ketika Anda memerlukan thumbnail raster atau aset bitmap, gunakan `BmpOptions` alih‑alih `PdfOptions`. Objek `Image` yang sama dapat disimpan ke BMP dengan satu panggilan, memungkinkan Anda menghasilkan pratinjau resolusi tinggi untuk katalog atau thumbnail UI.

## Ekspor ke PDF (file CAD umum)

Selain DWG, perpustakaan dapat mengonversi DXF, DWF, dan format CAD lain ke PDF dengan kode yang identik. Cukup ubah ekstensi file pada `Image.load`. Mesin konversi di bawahnya secara otomatis mendeteksi format sumber.

## Ekspor IFC ke PNG

`PngOptions` mendefinisikan pengaturan format PNG seperti tingkat kompresi. File IFC (Industry Foundation Classes) umum dalam alur kerja BIM. Muat IFC dengan `Image.load` dan simpan sebagai PNG menggunakan `PngOptions`. Ini menghasilkan gambar raster yang dapat disematkan dalam dasbor web atau dokumentasi.

## Ekspor STL ke PNG

`PngOptions` mendefinisikan pengaturan format PNG seperti tingkat kompresi. File STL mendeskripsikan mesh 3‑D. Aspose.CAD merendernya menjadi gambar 2‑D, yang dapat Anda ekspor sebagai PNG untuk pemeriksaan visual cepat atau daftar produk. Pola yang sama `Image.save("model.png", new PngOptions())` berlaku.

## Tutorial ekspor CAD

### [Ekspor gambar AutoCAD ke PDF - tutorial Aspose.CAD untuk Java](./export-autocad-images-to-pdf/)
Ekspor gambar AutoCAD ke PDF dengan mudah menggunakan Aspose.CAD untuk Java. Ikuti panduan langkah‑demi‑langkah untuk integrasi mulus.

### [Ekspor tata letak CAD ke PDF dengan Aspose.CAD untuk Java](./export-cad-layouts-to-pdf/)
Jelajahi Aspose.CAD untuk Java untuk mengekspor tata letak CAD ke PDF dengan mudah. Efisien, dapat diandalkan, dan ramah pengembang.

### [Ekspor ke BMP dengan Aspose.CAD untuk Java](./export-to-bmp/)
Jelajahi konversi CAD ke BMP yang mulus dengan Aspose.CAD untuk Java. Ikuti panduan langkah‑demi‑langkah untuk ekspor yang efisien dan presisi.

### [Ekspor ke PDF dengan Aspose.CAD untuk Java](./export-to-pdf/)
Pelajari cara mengekspor file CAD ke PDF dengan mudah menggunakan Aspose.CAD untuk Java. Ikuti panduan langkah‑demi‑langkah untuk integrasi mulus.

### [Ekspor IFC ke PNG dengan Aspose.CAD untuk Java](./export-ifc-to-png/)
Konversi IFC ke PNG dengan mudah menggunakan Aspose.CAD untuk Java. Ikuti tutorial langkah‑demi‑langkah kami.

### [Ekspor STL ke PNG dengan Aspose.CAD untuk Java](./export-stl-to-png/)
Jelajahi proses mulus mengekspor file STL ke PNG dalam Java dengan Aspose.CAD. Sederhanakan alur kerja Anda dan tingkatkan proyek Java Anda dengan mudah.

## Kasus penggunaan umum
- **Deliverable klien** – Sediakan tinjauan desain dalam PDF tanpa mengekspos file DWG sumber.  
- **Pelaporan otomatis** – Hasilkan thumbnail PNG dari model IFC atau STL untuk dasbor.  
- **Pipeline konversi batch** – Proses arsip CAD besar semalaman menggunakan loop Java sederhana.

## Tips & trik
- **Tip pro:** Atur `PdfOptions.setVectorRasterizationOptions().setResolution(300)` untuk mengontrol DPI pada ekspor berbasis raster dan menjaga ukuran file tetap wajar.  
- **Hindari lonjakan memori:** Panggil `Image.dispose()` setelah setiap `save` saat memproses banyak file.  
- **Pemecahan masalah:** Jika lapisan menghilang, pastikan DWG sumber memiliki lapisan yang terlihat dan aktifkan kompresi dengan `PdfOptions.setCompress(true)`.

## Pertanyaan yang sering diajukan

**T: Bagaimana cara mengonversi IFC ke PNG menggunakan Aspose.CAD?**  
J: Muat file IFC dengan `Image.load("model.ifc")` dan panggil `save("model.png", new PngOptions())`.

**T: Bisakah saya mengekspor tata letak CAD langsung ke PDF tanpa mengonversinya ke gambar terlebih dahulu?**  
J: Ya—Aspose.CAD memperlakukan tata letak sebagai gambar secara internal, sehingga `save("layout.pdf", new PdfOptions())` menangani secara otomatis.

**T: Apa perbedaan antara mengekspor AutoCAD ke PDF dan mengekspor tata letak CAD ke PDF?**  
J: Mengekspor gambar AutoCAD mengonversi seluruh gambar, sedangkan mengekspor tata letak menargetkan view paper‑space tertentu, mempertahankan pengaturan halaman khususnya.

**T: Apakah ada batasan jumlah halaman saat mengekspor DWG multi‑sheet ke PDF?**  
J: Tidak ada batasan bawaan; setiap tata letak menjadi halaman terpisah dalam PDF yang dihasilkan.

**T: Apakah saya memerlukan lisensi terpisah untuk setiap format ekspor?**  
J: Satu lisensi Aspose.CAD mencakup semua format yang didukung (PDF, PNG, BMP, dll.).

---

**Terakhir diperbarui:** 2026-10-25  
**Diuji dengan:** Aspose.CAD untuk Java 24.12  
**Penulis:** Aspose

## Tutorial Terkait

- [Ekspor CAD ke PDF: Ekspor Tata Letak CAD ke PDF dengan Aspose.CAD untuk Java](/cad/java/cad-export-options/export-cad-layouts-to-pdf/)
- [Ekspor DWG ke PDF dalam Java – Atur Ukuran Halaman PDF dengan Aspose.CAD](/cad/java/cad-export-options/export-to-pdf/)


{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}