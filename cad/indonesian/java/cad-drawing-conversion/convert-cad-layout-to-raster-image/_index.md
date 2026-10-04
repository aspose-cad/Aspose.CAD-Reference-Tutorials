---
date: 2026-10-04
description: Pelajari cara cepat mengonversi DWG ke PNG dan mengekspor CAD sebagai
  PNG atau format raster lainnya menggunakan Aspose.CAD for Java. Dapatkan hasil berkualitas
  tinggi dengan cepat.
keywords:
- convert dwg to png
- dwg to raster image
- convert cad to pdf
- export cad as png
- convert dwg to jpeg
lastmod: 2026-10-04
linktitle: Konversi Tata Letak CAD ke Format Gambar Raster
og_description: Konversi DWG ke PNG dengan cepat menggunakan Aspose.CAD for Java.
  Pelajari langkah demi langkah cara mengekspor CAD sebagai PNG, JPEG, TIFF, dan lainnya.
og_image_alt: 'Developer guide: Convert DWG to PNG and other raster formats using
  Aspose.CAD for Java'
og_title: Konversi DWG ke PNG dan format raster lainnya menggunakan Aspose.CAD for
  Java
schemas:
- author: Aspose
  dateModified: '2026-10-04'
  description: Learn how to quickly convert dwg to png and export cad as png or other
    raster formats using Aspose.CAD for Java. Get high‑quality results fast.
  headline: Convert DWG to PNG and other raster formats using Aspose.CAD for Java
  type: TechArticle
- description: Learn how to quickly convert dwg to png and export cad as png or other
    raster formats using Aspose.CAD for Java. Get high‑quality results fast.
  name: Convert DWG to PNG and other raster formats using Aspose.CAD for Java
  steps:
  - name: set up the resource directory
    text: Replace `"Your Document Directory"` with the absolute path where your CAD
      files reside. This directory will be used for both input and output files.
  - name: load the CAD file
    text: '`Image.load` parses the source file and creates an in‑memory representation
      that you can rasterize. You can load any supported format (DWG, DXF, DGN, etc.)
      – this is the **how to convert cad** part.'
  - name: configure rasterization options
    text: '`CadRasterizationOptions` defines how the vector data is turned into pixels.
      `setPageWidth` and `setPageHeight` control output resolution (larger values
      = higher DPI). `setLayouts` lets you **convert CAD to raster** for specific
      layouts; omit it to rasterize the whole drawing.'
  - name: set image options
    text: '`TiffOptions` (or `PngOptions` for PNG) tells Aspose which raster format
      to generate and lets you fine‑tune compression, color depth, and other format‑specific
      settings. Choose the options class that matches your desired output.'
  - name: save the resultant image
    text: Call `save` on the `Image` instance, passing the output file name and the
      options object. Change the file extension to `.png` (and use `PngOptions`) to
      **save CAD as PNG**. The same pattern works for JPEG, BMP, or PDF. > **Common
      pitfall:** Forgetting to match the file extension with the options cla
  type: HowTo
- questions:
  - answer: Yes, it supports over 30 CAD and raster formats, including DWG, DXF, DGN,
      and SVG.
    question: Is Aspose.CAD compatible with different CAD file formats?
  - answer: Absolutely. Adjust `setPageWidth`, `setPageHeight`, or `setResolution`
      in `CadRasterizationOptions` to achieve the desired DPI.
    question: Can I customize the resolution of the output raster image?
  - answer: Provide an array with all layout names to `setLayouts`, e.g., `new String[]{"Model","Layout1","Layout2"}`.
    question: How can I convert multiple CAD layouts in a single run?
  - answer: Yes—PNG, JPEG, BMP, PDF, and more are available via their respective `*Options`
      classes.
    question: Are there output formats besides TIFF supported?
  - answer: Visit the [Aspose.CAD forum](https://forum.aspose.com/c/cad/19) for community
      support and official assistance.
    question: Where can I get help or share my experience with Aspose.CAD?
  type: FAQPage
second_title: Aspose.CAD Java API
tags:
- convert dwg
- Aspose.CAD
- Java raster conversion
- CAD image processing
title: Konversi DWG ke PNG dan format raster lainnya menggunakan Aspose.CAD for Java
url: /id/java/cad-drawing-conversion/convert-cad-layout-to-raster-image/
weight: 12
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Mengonversi DWG ke PNG dan format raster lainnya menggunakan Aspose.CAD untuk Java

## Pendahuluan

`Aspose.CAD for Java` adalah perpustakaan yang memungkinkan konversi programatik file CAD ke gambar raster seperti PNG, JPEG, dan TIFF. Mengonversi DWG ke PNG (atau format gambar raster lainnya) adalah kebutuhan umum ketika Anda perlu membagikan gambar CAD dengan rekan tim yang tidak memiliki penampil CAD, menyematkan desain dalam dokumentasi, atau menghasilkan thumbnail untuk galeri web. Dalam panduan ini Anda akan belajar cara mengonversi dwg ke png dengan cepat dan andal, baik Anda bekerja dengan file gambar lengkap maupun hanya tata letak tertentu. Anda juga mungkin perlu **convert CAD to raster** untuk pratinjau web, alat pelaporan, atau aplikasi seluler.

## Jawaban Cepat
- **Library apa yang menangani DWG ke PNG?** Aspose.CAD for Java menyediakan mesin konversi.  
- **Format raster apa yang dapat saya ekspor?** PNG, JPEG, TIFF, PDF, BMP, dan lebih dari 30 format tambahan.  
- **Apakah saya memerlukan lisensi untuk pengujian?** Versi percobaan gratis dapat digunakan untuk pengembangan; lisensi komersial diperlukan untuk produksi.  
- **Bisakah saya memilih tata letak tertentu?** Ya – gunakan `setLayouts` untuk menargetkan “Model”, “Layout1”, dll.  
- **Apakah output beresolusi tinggi memungkinkan?** Tentu – sesuaikan `setPageWidth` dan `setPageHeight` (atau `setResolution`) untuk mengontrol DPI.

## Apa itu “convert dwg to png”?

Convert dwg to png berarti mengubah gambar vektor DWG menjadi gambar PNG berbasis piksel yang dapat ditampilkan oleh penampil gambar standar apa pun. Proses ini merasterkan entitas vektor, mempertahankan ketebalan garis, warna, dan lapisan sambil menerjemahkannya ke dalam bitmap beresolusi tetap. Hasilnya ideal untuk disematkan dalam PDF, dokumen Word, atau halaman web di mana dukungan vektor terbatas.

## Mengapa mengekspor CAD sebagai PNG (atau format raster lainnya)?

Mengekspor CAD sebagai PNG memberi Anda kompatibilitas universal, pemuatan cepat, dan penyematan mudah di semua platform utama. Gambar raster dimuat secara instan dibandingkan membuka file DWG yang berat, dan kompresi loss‑less PNG memastikan fidelitas visual. Dengan mengontrol resolusi, warna latar belakang, dan tata letak, Anda menjamin setiap pemangku kepentingan melihat tampilan yang sama, baik file dilihat di desktop, perangkat seluler, atau dalam browser.

## Kasus penggunaan umum

| Skenario | Mengapa output raster membantu |
|----------|-------------------------------|
| **Dokumentasi proyek** | Menyematkan PNG dalam PDF atau dokumen Word menghindari kebutuhan perangkat lunak CAD bagi peninjau. |
| **Portal web** | Thumbnail yang dihasilkan dari file DWG dimuat secara instan dan meningkatkan pengalaman pengguna. |
| **Aplikasi seluler** | Gambar raster ditampilkan dengan benar pada perangkat yang tidak memiliki penampil CAD. |
| **Pelaporan otomatis** | Konversi batch beberapa tata letak ke PNG/JPEG untuk dimasukkan ke dalam grafik atau dasbor. |

## Prasyarat

1. **Lingkungan pengembangan Java** – JDK 8 atau yang lebih baru terpasang dan dikonfigurasi.  
2. **Aspose.CAD for Java** – Unduh JAR terbaru dari [Aspose.CAD for Java documentation](https://reference.aspose.com/cad/java/).  

## Impor namespace

`com.aspose.cad.Image` adalah kelas inti yang mewakili setiap file CAD dalam memori. `com.aspose.cad.imageoptions.*` menyediakan objek opsi untuk setiap format raster. Impor kelas yang Anda perlukan untuk memuat gambar, mengonfigurasi rasterisasi, dan menyimpan output.

> **Pro tip:** Jika Anda berencana untuk **export CAD as PNG** alih-alih TIFF, ganti `TiffOptions` dengan `PngOptions` (ditemukan di `com.aspose.cad.imageoptions.PngOptions`).

## Panduan langkah‑demi‑langkah

### Langkah 1: siapkan direktori sumber daya

Ganti `"Your Document Directory"` dengan jalur absolut tempat file CAD Anda berada. Direktori ini akan digunakan untuk file input dan output.

```java
import com.aspose.cad.Image;
import com.aspose.cad.ImageOptionsBase;

import com.aspose.cad.fileformats.tiff.enums.TiffExpectedFormat;
import com.aspose.cad.imageoptions.CadRasterizationOptions;
import com.aspose.cad.imageoptions.TiffOptions;
```

### Langkah 2: muat file CAD

`Image.load` mengurai file sumber dan membuat representasi dalam memori yang dapat Anda rasterisasi. Anda dapat memuat format apa pun yang didukung (DWG, DXF, DGN, dll.) – ini adalah bagian **how to convert cad**.

```java
// The path to the resource directory.
String dataDir = "Your Document Directory" + "CADConversion/";
```

### Langkah 3: konfigurasikan opsi rasterisasi

`CadRasterizationOptions` menentukan bagaimana data vektor diubah menjadi piksel. `setPageWidth` dan `setPageHeight` mengontrol resolusi output (nilai lebih besar = DPI lebih tinggi). `setLayouts` memungkinkan Anda **convert CAD to raster** untuk tata letak tertentu; hapus jika ingin meraster seluruh gambar.

```java
String srcFile = dataDir + "conic_pyramid.dxf";
Image image = Image.load(srcFile);
```

### Langkah 4: atur opsi gambar

`TiffOptions` (atau `PngOptions` untuk PNG) memberi tahu Aspose format raster yang akan dihasilkan dan memungkinkan Anda menyesuaikan kompresi, kedalaman warna, dan pengaturan spesifik format lainnya. Pilih kelas opsi yang sesuai dengan output yang diinginkan.

```java
CadRasterizationOptions rasterizationOptions = new CadRasterizationOptions();
rasterizationOptions.setPageWidth(1200);
rasterizationOptions.setPageHeight(1200);
rasterizationOptions.setLayouts(new String[] {"Model", "Layout1"});
```

### Langkah 5: simpan gambar hasil

Panggil `save` pada instance `Image`, berikan nama file output dan objek opsi. Ubah ekstensi file menjadi `.png` (dan gunakan `PngOptions`) untuk **save CAD as PNG**. Pola yang sama berlaku untuk JPEG, BMP, atau PDF.

```java
ImageOptionsBase options = new TiffOptions(TiffExpectedFormat.Default);
options.setVectorRasterizationOptions(rasterizationOptions);
```

> **Common pitfall:** Lupa mencocokkan ekstensi file dengan kelas opsi akan menyebabkan `UnsupportedFormatException`. Selalu pastikan keduanya sinkron.

## Masalah umum dan solusi

| Masalah | Solusi |
|---------|--------|
| **Gambar output kosong** | Verifikasi bahwa nama tata letak dalam `setLayouts` persis sama dengan yang ada di file CAD sumber. |
| **PNG beresolusi rendah** | Tingkatkan `setPageWidth` / `setPageHeight` atau setel `setResolution` pada opsi rasterisasi. |
| **Versi DWG tidak didukung** | Pastikan Anda menggunakan versi Aspose.CAD terbaru; rilis lama mungkin tidak mendukung versi DWG yang lebih baru. |
| **Kesalahan memori pada file besar** | Proses halaman satu per satu atau tingkatkan heap JVM (`-Xmx2g`). |

## Pertanyaan yang sering diajukan

**Q: Apakah Aspose.CAD kompatibel dengan berbagai format file CAD?**  
A: Ya, mendukung lebih dari 30 format CAD dan raster, termasuk DWG, DXF, DGN, dan SVG.

**Q: Bagaimana saya dapat menyesuaikan resolusi gambar raster output?**  
A: Tentu. Sesuaikan `setPageWidth`, `setPageHeight`, atau `setResolution` dalam `CadRasterizationOptions` untuk mencapai DPI yang diinginkan.

**Q: Bagaimana saya dapat mengonversi beberapa tata letak CAD dalam satu kali jalankan?**  
A: Berikan array dengan semua nama tata letak ke `setLayouts`, misalnya `new String[]{"Model","Layout1","Layout2"}`.

**Q: Apakah ada format output selain TIFF yang didukung?**  
A: Ya—PNG, JPEG, BMP, PDF, dan lainnya tersedia melalui kelas `*Options` masing‑masing.

**Q: Di mana saya dapat mendapatkan bantuan atau berbagi pengalaman dengan Aspose.CAD?**  
A: Kunjungi [Aspose.CAD forum](https://forum.aspose.com/c/cad/19) untuk dukungan komunitas dan bantuan resmi.

## Kesimpulan

Dengan mengikuti langkah‑langkah ini Anda dapat **convert DWG to PNG**, **export CAD as PNG**, **save CAD as JPEG**, atau menghasilkan format raster lain yang Anda perlukan. Aspose.CAD for Java menangani pekerjaan berat, memungkinkan Anda fokus pada integrasi gambar berkualitas tinggi ke dalam aplikasi, dokumentasi, atau portal web Anda. Dukungan perpustakaan untuk lebih dari 30 format dan kemampuannya merender gambar ber‑ratus halaman tanpa memuat seluruh file ke memori menjadikannya pilihan kuat untuk rasterisasi CAD tingkat perusahaan.

---

**Last Updated:** 2026-10-04  
**Tested With:** Aspose.CAD for Java 24.12  
**Author:** Aspose  







```java
image.save(dataDir + "conic_pyramid_layoutstorasterimage_out_.tiff", options);
```

```bash
java -jar aspose-cad.jar -i input.dwg -o output.png -w 1200 -h 1200
```

## Tutorial Terkait

- [Ekspor DWG ke PDF atau Raster dengan Cepat Menggunakan pustaka java cad Aspose.CAD untuk Java](/cad/java/cad-drawing-conversion/export-dwg-to-pdf-or-raster/)
- [Konversi DWG ke BMP dengan Aspose.CAD untuk Java](/cad/java/cad-export-options/export-to-bmp/)
- [Ekspor DWG ke PDF: Tata Letak Spesifik Menggunakan Aspose.CAD untuk Java](/cad/java/cad-drawing-conversion/export-specific-dwg-layout-to-pdf/)


{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}