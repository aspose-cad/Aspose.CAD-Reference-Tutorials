---
date: 2026-06-29
description: Pelajari cara membuat PDF dari DWG dan menyesuaikan tata letak PDF menggunakan
  Aspose.CAD for Java. Integrasi mudah untuk pengembang Java.
keywords:
- create pdf from dwg
- convert cad to pdf
- pdf different page sizes
- export dwg to pdf
- customize pdf layout
linktitle: PDF Tunggal dengan Tata Letak Berbeda
schemas:
- author: Aspose
  dateModified: '2026-06-29'
  description: Learn how to create PDF from DWG and customize PDF layout using Aspose.CAD
    for Java. Easy integration for Java developers.
  headline: Create PDF from DWG with Aspose.CAD for Java
  type: TechArticle
- questions:
  - answer: Yes, Aspose.CAD for Java integrates seamlessly with libraries such as
      Apache POI, Jackson, or Spring Boot.
    question: Can I use Aspose.CAD for Java with other Java libraries?
  - answer: Absolutely! You can access a free trial version [here](https://releases.aspose.com/).
    question: Is there a trial version available?
  - answer: Visit the [Aspose.CAD forum](https://forum.aspose.com/c/cad/19) for community
      support and discussions.
    question: Where can I find additional support?
  - answer: You can obtain a temporary license [here](https://purchase.aspose.com/temporary-license/).
    question: How do I obtain a temporary license?
  - answer: Purchase the full version of Aspose.CAD for Java [here](https://purchase.aspose.com/buy).
    question: Where can I purchase the full version?
  type: FAQPage
second_title: Aspose.CAD Java API
title: Buat PDF dari DWG dengan Aspose.CAD for Java
url: /id/java/other-cad-operations/single-pdf-different-layouts/
weight: 16
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Buat PDF dari DWG dengan Aspose.CAD untuk Java

## Pendahuluan

Dalam tutorial ini Anda akan **create PDF from DWG** file dan menerapkan beberapa tata letak ukuran halaman menggunakan Aspose.CAD untuk Java. Apakah Anda perlu menghasilkan cetak biru konstruksi, skema teknik, atau PDF siap pemasaran, langkah‑langkah di bawah ini menunjukkan cara mengonversi gambar CAD ke PDF, menyesuaikan dimensi setiap tata letak, dan menghasilkan satu dokumen multi‑halaman — semuanya tanpa meninggalkan lingkungan Java Anda.

## Jawaban Cepat
- **Apa yang dibahas dalam tutorial?** Mengonversi gambar DWG menjadi satu PDF dengan beberapa ukuran halaman.  
- **Perpustakaan apa yang diperlukan?** Aspose.CAD untuk Java (versi terbaru).  
- **Apakah saya memerlukan lisensi?** Versi percobaan gratis dapat digunakan untuk pengembangan; lisensi komersial diperlukan untuk produksi.  
- **Bisakah saya mengekspor format lain?** Ya – API juga mendukung ekspor ke PNG, JPEG, dan SVG.  
- **Apakah Java 8 cukup?** Perpustakaan ini bekerja dengan Java 8 dan runtime yang lebih baru.

## Apa itu “create pdf from dwg”?

**Create PDF from DWG** berarti mengonversi file AutoCAD DWG asli menjadi dokumen PDF sambil mempertahankan kesetiaan vektor, lapisan, dan ketebalan garis, serta memungkinkan penyesuaian tata letak. Aspose.CAD melakukan konversi ini sepenuhnya di memori, sehingga tidak memerlukan perangkat lunak CAD eksternal, dan PDF yang dihasilkan dapat diedit atau dicetak secara langsung.

## Mengapa menyesuaikan tata letak PDF dari DWG?

Aspose.CAD mendukung **30+ format CAD** dan dapat menghasilkan PDF hingga **500 MB** tanpa memuat seluruh file ke memori. Dengan mendefinisikan ukuran halaman individual untuk setiap tata letak, Anda dapat menghasilkan lembar cetak yang sesuai dengan dimensi ISO, ANSI, atau kustom – manfaat terukur yang menghemat waktu dan menghilangkan proses manual pasca‑pemrosesan.

## Prasyarat

Sebelum memulai, pastikan Anda telah menyiapkan hal‑hal berikut:
- **Lingkungan Java:** Pastikan Anda telah menginstal Java di mesin Anda.  
- **Perpustakaan Aspose.CAD:** Unduh dan instal perpustakaan Aspose.CAD untuk Java dari [tautan unduhan](https://releases.aspose.com/cad/java/).  
- **Direktori Dokumen:** Siapkan direktori untuk gambar DWG Anda.

## Impor Paket

Kelas `CadImage` adalah objek inti Aspose.CAD yang mewakili gambar CAD dalam memori. Impor namespace yang diperlukan sebelum Anda mulai:

```java
import com.aspose.cad.Image;
import com.aspose.cad.SizeF;
import com.aspose.cad.fileformats.cad.CadImage;
import com.aspose.cad.imageoptions.CadRasterizationOptions;
import com.aspose.cad.imageoptions.PdfOptions;
import com.aspose.cad.imageoptions.VectorRasterizationOptions;
```

## Langkah 1: Muat Gambar CAD

`CadImage` memuat file DWG dan memberikan akses ke data vektornya. Mulailah dengan memuat gambar CAD Anda ke dalam objek `CadImage`:

```java
String dataDir = "Your Document Directory" + "DWGDrawings/";
CadImage cadImage = (CadImage)Image.load(dataDir + "City skyway map.dwg");
```

## Langkah 2: Konfigurasikan Opsi Rasterisasi

`RasterizationOptions` menentukan bagaimana vektor CAD dirasterisasi sebelum ditempatkan ke dalam PDF. Siapkan opsi rasterisasi untuk gambar CAD:

```java
CadRasterizationOptions rasterizationOptions = new CadRasterizationOptions();
rasterizationOptions.setPageWidth(1000);
rasterizationOptions.setPageHeight(1000);
```

## Langkah 3: Sesuaikan Ukuran Halaman Tata Letak

`PdfOptions` memungkinkan Anda menetapkan dimensi halaman yang berbeda untuk setiap tata letak di dalam DWG. Definisikan ukuran kustom untuk beberapa tata letak dalam gambar CAD:

```java
rasterizationOptions.getLayoutPageSizes().addItem("ANSI C Plot", new SizeF(500, 1000));
rasterizationOptions.getLayoutPageSizes().addItem("8.5 x 11 Plot", new SizeF(1000, 100));
```

## Langkah 4: Atur Opsi PDF

`PdfOptions` adalah wadah yang menggabungkan pengaturan rasterisasi dan definisi tata letak. Konfigurasikan opsi PDF, termasuk pengaturan rasterisasi:

```java
PdfOptions pdfOptions = new PdfOptions();
pdfOptions.setVectorRasterizationOptions(rasterizationOptions);
```

## Langkah 5: Simpan sebagai PDF

`PdfSaveOptions` menyelesaikan konversi dan menulis file output. Simpan gambar CAD yang telah diproses sebagai PDF:

```java
cadImage.save(dataDir + "singlePDF_out.pdf", pdfOptions);
```

Selamat! Anda telah berhasil **create pdf from dwg** dengan ukuran halaman yang berbeda menggunakan Aspose.CAD untuk Java.

## Masalah Umum dan Solusinya

- **Halaman kosong dalam PDF output** – Pastikan nilai `PageSize` cocok dengan dimensi tata letak sebenarnya dalam file DWG.  
- **Kesalahan memori pada gambar besar** – Gunakan `CadImage.load(..., LoadOptions)` dengan `LoadOptions.setLoadMode(LoadMode.Memory)` untuk men-stream file alih‑alih memuatnya sepenuhnya.  
- **Skala tidak tepat** – Sesuaikan `RasterizationOptions.setPageWidth` dan `setPageHeight` agar sesuai dengan DPI (dots per inch) yang diinginkan.

## Pertanyaan yang Sering Diajukan

**Q: Bisakah saya menggunakan Aspose.CAD untuk Java dengan perpustakaan Java lain?**  
A: Ya, Aspose.CAD untuk Java terintegrasi mulus dengan perpustakaan seperti Apache POI, Jackson, atau Spring Boot.

**Q: Apakah ada versi percobaan yang tersedia?**  
A: Tentu saja! Anda dapat mengakses versi percobaan gratis [di sini](https://releases.aspose.com/).

**Q: Di mana saya dapat menemukan dukungan tambahan?**  
A: Kunjungi [forum Aspose.CAD](https://forum.aspose.com/c/cad/19) untuk dukungan komunitas dan diskusi.

**Q: Bagaimana cara mendapatkan lisensi sementara?**  
A: Anda dapat memperoleh lisensi sementara [di sini](https://purchase.aspose.com/temporary-license/).

**Q: Di mana saya dapat membeli versi lengkap?**  
A: Beli versi lengkap Aspose.CAD untuk Java [di sini](https://purchase.aspose.com/buy).

---

**Terakhir Diperbarui:** 2026-06-29  
**Diuji dengan:** Aspose.CAD untuk Java 24.10  
**Penulis:** Aspose

## Tutorial Terkait

- [Ekspor DWG ke PDF atau Raster Menggunakan Aspose.CAD untuk Java](/cad/java/cad-drawing-conversion/export-dwg-to-pdf-or-raster/)
- [Ekspor Tata Letak CAD ke PDF dengan Aspose.CAD untuk Java](/cad/java/cad-export-options/export-cad-layouts-to-pdf/)
- [Ekspor Tata Letak DWG Spesifik ke PDF Menggunakan Aspose.CAD untuk Java](/cad/java/cad-drawing-conversion/export-specific-dwg-layout-to-pdf/)


{{< /blocks/products/pf/tutorial-page-section >}}
{{< /blocks/products/pf/main-container >}}
{{< blocks/products/products-backtop-button >}}
{{< /blocks/products/pf/main-wrap-class >}}