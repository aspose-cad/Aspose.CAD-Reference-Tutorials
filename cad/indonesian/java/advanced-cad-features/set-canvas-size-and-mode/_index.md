---
date: 2026-08-29
description: Pelajari cara mengatur ukuran halaman pdf dan mengonversi CAD ke PDF
  menggunakan Aspose.CAD untuk Java, dengan penskalaan tata letak otomatis dan ekspor
  TIFF.
keywords:
- set pdf page size
- convert cad to pdf
- canvas size java
- high resolution tiff
- change pdf dimensions
lastmod: 2026-08-29
linktitle: Atur ukuran halaman pdf – konversi cad ke pdf
og_description: Pelajari cara mengatur ukuran halaman pdf saat mengonversi gambar
  CAD ke PDF di Java menggunakan Aspose.CAD. Panduan ini mencakup dimensi kanvas,
  penskalaan tata letak otomatis, dan mengekspor ke TIFF resolusi tinggi.
og_image_alt: Tutorial showing how to set pdf page size and convert CAD to PDF in
  Java
og_title: Atur ukuran halaman pdf – konversi CAD ke PDF dengan Aspose di Java
schemas:
- author: Aspose
  dateModified: '2026-08-29'
  description: Learn how to set pdf page size and convert CAD to PDF using Aspose.CAD
    for Java, with automatic layout scaling and TIFF export.
  headline: Set pdf page size – convert cad to pdf (Java)
  type: TechArticle
- questions:
  - answer: No. Canvas size controls page dimensions; vector data remains resolution‑independent,
      ensuring crisp rendering at any zoom level.
    question: does the canvas size affect vector quality in the PDF?
  - answer: Yes. Adjust `rasterizationOptions.setResolution(dpiValue)` before creating
      `TiffOptions`.
    question: can I set a different DPI for the TIFF output?
  - answer: Use Aspose.PDF to load the generated PDF and call `pdf.getPages().setPageSize(PageSize.A4)`
      or a custom size.
    question: how can I change PDF dimensions for an existing PDF without re‑rendering
      the CAD?
  - answer: Keep `setAutomaticLayoutsScaling(true)` and avoid `setNoScaling(true)`;
      this retains layer visibility and layout fidelity.
    question: what is the best way to convert dxf to pdf while preserving layers?
  type: FAQPage
second_title: Aspose.CAD Java API
tags:
- set pdf page size
- convert cad
- Aspose.CAD
- Java
- high resolution tiff
title: Atur ukuran halaman pdf – konversi cad ke pdf (Java)
url: /id/java/advanced-cad-features/set-canvas-size-and-mode/
weight: 16
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Set ukuran halaman PDF – konversi CAD ke PDF (Java)

## Pendahuluan

Jika Anda perlu **set pdf page size** saat mengonversi gambar CAD ke PDF, Anda berada di tempat yang tepat. Dalam tutorial ini kami akan menunjukkan cara menggunakan Aspose.CAD untuk Java untuk menentukan dimensi kanvas yang tepat, mengaktifkan automatic layout scaling, dan kemudian mengekspor hasilnya ke PDF dan TIFF. Baik Anda menyiapkan skema teknik untuk dicetak atau menghasilkan thumbnail untuk galeri web, mengontrol ukuran halaman dan resolusi output sangat penting.

## Jawaban Cepat

- **Apa arti “convert CAD to PDF”?** Mengubah gambar CAD (mis., DXF, DWG) menjadi dokumen PDF yang dapat dilihat di platform apa pun.  
- **Apakah saya juga dapat mengekspor ke TIFF?** Ya—gunakan `TiffOptions` untuk membuat gambar raster beresolusi tinggi.  
- **Opsi mana yang mengontrol ukuran kanvas di Java?** `CadRasterizationOptions.setPageWidth/Height`.  
- **Apa itu automatic layout scaling?** Sebuah flag (`setAutomaticLayoutsScaling(true)`) yang mempertahankan proporsi tata letak asli ketika ukuran kanvas berubah.  
- **Apakah saya memerlukan lisensi untuk Aspose.CAD?** Lisensi sementara atau permanen diperlukan untuk penggunaan produksi.

## Cara mengatur pdf page size saat mengonversi CAD ke PDF di Java

Muat file CAD Anda, konfigurasikan `CadRasterizationOptions` dengan lebar dan tinggi yang diinginkan, aktifkan automatic layout scaling, dan kemudian simpan hasilnya sebagai PDF. Pendekatan dua langkah ini memungkinkan Anda mengontrol dimensi tepat halaman output tanpa mengorbankan kualitas vektor.

## Apa itu convert CAD ke PDF?

Converting CAD to PDF berarti mengambil gambar teknik berbasis vektor dan merendernya sebagai halaman PDF, mempertahankan garis, lapisan, dan geometri sambil membuat file dapat diakses secara universal. Proses ini meraster gambar sesuai opsi yang ditentukan, menghasilkan PDF yang dapat dibuka di perangkat apa pun tanpa memerlukan perangkat lunak CAD, dan mempertahankan kesetiaan visual desain asli.

## Mengapa mengatur ukuran kanvas java?

Mengatur ukuran kanvas di Java memungkinkan Anda menentukan resolusi output dan dimensi halaman, memastikan bahwa PDF atau TIFF yang dihasilkan sesuai dengan kebutuhan pencetakan atau tampilan Anda. Ini juga memberi Anda kontrol atas perilaku skala, yang penting untuk gambar berformat besar.

## Prasyarat

Sebelum menyelam ke tutorial, pastikan Anda memiliki prasyarat berikut:

- Aspose.CAD for Java: Pastikan Anda memiliki perpustakaan Aspose.CAD yang terpasang di lingkungan Java Anda. Anda dapat mengunduh perpustakaan Aspose.CAD untuk Java [here](https://releases.aspose.com/cad/java/).
- Direktori dokumen: Siapkan direktori dokumen untuk menyimpan file CAD Anda. Direktori ini akan dirujuk dalam langkah‑langkah tutorial.

Sekarang, mari kita mulai dengan panduan langkah demi langkah.

## Impor namespace

Dalam langkah ini, kami akan mengimpor namespace yang diperlukan untuk memulai proyek Aspose.CAD Anda.

`Image` adalah kelas utama yang digunakan untuk memuat file CAD.

```java
import java.awt.Image;

import com.aspose.cad.fileformats.tiff.enums.TiffExpectedFormat;
import com.aspose.cad.imageoptions.CadRasterizationOptions;
import com.aspose.cad.imageoptions.PdfOptions;
import com.aspose.cad.imageoptions.TiffOptions;
```

## Langkah 1: impor kelas Aspose.CAD

Kelas `Image` menyediakan metode untuk memuat dan menyimpan gambar CAD.

```java
// The path to the resource directory.
String dataDir = "Your Document Directory" + "CADConversion/";

String srcFile = dataDir + "conic_pyramid.dxf";
com.aspose.cad.Image objImage = com.aspose.cad.Image.load(srcFile);
```

Dalam potongan kode ini, kami menyiapkan jalur ke direktori sumber daya dan memuat file DXF menggunakan kelas `Image` milik Aspose.CAD.

## Langkah 2: atur properti CadRasterizationOptions (set canvas size java)

`CadRasterizationOptions` menentukan pengaturan rasterisasi seperti ukuran halaman dan skala untuk konversi CAD‑to‑raster.

```java
// Create an instance of CadRasterizationOptions and set its various properties
CadRasterizationOptions rasterizationOptions = new CadRasterizationOptions();
rasterizationOptions.setPageWidth(1600);
rasterizationOptions.setPageHeight(1600);

rasterizationOptions.setAutomaticLayoutsScaling(true);
rasterizationOptions.setNoScaling(true);
```

Di sini, kami membuat instance `CadRasterizationOptions` dan mengonfigurasi properti seperti lebar halaman, tinggi halaman, dan **automatic layout scaling**. Ini adalah inti dari **configure canvas mode** untuk konversi Anda.

## Langkah 3: buat PdfOptions dan atur vectorRasterizationOptions

`PdfOptions` mendefinisikan pengaturan output PDF untuk konversi.

```java
// Create an instance of PdfOptions
PdfOptions pdfOptions = new PdfOptions();

// Set the VectorRasterizationOptions property
pdfOptions.setVectorRasterizationOptions(rasterizationOptions);
```

Sekarang, kami membuat instance `PdfOptions` dan mengatur properti `VectorRasterizationOptions`‑nya ke `CadRasterizationOptions` yang telah dikonfigurasi sebelumnya.

## Langkah 4: ekspor ke PDF (convert CAD to PDF)

```java
// Export CAD to PDF
objImage.save(dataDir + "result_out_.pdf", pdfOptions);
```

Akhirnya, kami menyimpan gambar CAD ke file PDF menggunakan opsi yang ditentukan, menyelesaikan proses **convert CAD to PDF**.

## Langkah 5: buat TiffOptions dan atur vectorRasterizationOptions (export CAD to TIFF)

`TiffOptions` mengonfigurasi parameter output TIFF seperti kompresi dan resolusi.

```java
// Create an instance of TiffOptions
TiffOptions tiffOptions = new TiffOptions(TiffExpectedFormat.Default);

// Set the VectorRasterizationOptions property
tiffOptions.setVectorRasterizationOptions(rasterizationOptions);
```

## Langkah 6: ekspor ke TIFF

```java
// Export CAD to TIFF
objImage.save(dataDir + "result_out_.tiff", tiffOptions);
```

Akhirnya, kami menyimpan gambar CAD ke file TIFF menggunakan opsi yang ditentukan, menunjukkan cara **export CAD to TIFF** setelah mengonfigurasi ukuran kanvas.

## Masalah umum dan solusi

| Masalah | Penyebab | Solusi |
|-------|-------|-----|
| Output PDF kosong | `setNoScaling(true)` menonaktifkan rendering untuk beberapa gambar | Hapus `setNoScaling(true)` atau setel ke `false`. |
| Resolusi TIFF terlihat rendah | Lebar/tinggi halaman terlalu kecil | Tingkatkan nilai `setPageWidth` / `setPageHeight`. |
| Tata letak terlihat terdistorsi | Automatic layout scaling dinonaktifkan | Pastikan `setAutomaticLayoutsScaling(true)` diaktifkan. |

## Mengapa menyesuaikan ukuran kanvas dan DPI?

Mengubah ukuran kanvas secara langsung memengaruhi resolusi rasterisasi output. Jika Anda perlu **increase TIFF resolution**, cukup naikkan nilai `setPageWidth` / `setPageHeight` atau panggil `rasterizationOptions.setResolution(300)` sebelum membuat `TiffOptions`. Ini memberi Anda gambar raster berkualitas tinggi yang cocok untuk pencetakan atau inspeksi detail.

## Pertanyaan yang sering diajukan

**Q1: dapatkah saya menggunakan Aspose.CAD untuk Java dengan kerangka kerja Java lainnya?**  
A: Ya, Aspose.CAD dirancang untuk terintegrasi secara mulus dengan berbagai kerangka kerja Java.

**Q2: apakah lisensi sementara tersedia untuk Aspose.CAD?**  
A: Ya, Anda dapat memperoleh halaman lisensi sementara [here](https://purchase.aspose.com/temporary-license/).

**Q3: di mana saya dapat mendapatkan dukungan komunitas untuk Aspose.CAD?**  
A: Kunjungi forum Aspose.CAD [Aspose.CAD forum](https://forum.aspose.com/c/cad/19) untuk dukungan komunitas dan diskusi.

**Q4: dapatkah saya mencoba Aspose.CAD secara gratis?**  
A: Tentu! Dapatkan halaman unduhan percobaan gratis [here](https://releases.aspose.com/).

**Q5: bagaimana cara membeli Aspose.CAD untuk Java?**  
A: Beli Aspose.CAD untuk Java [here](https://purchase.aspose.com/buy).

**Q: apakah ukuran kanvas memengaruhi kualitas vektor dalam PDF?**  
A: Tidak. Ukuran kanvas mengontrol dimensi halaman; data vektor tetap independen resolusi, memastikan render yang tajam pada tingkat zoom apa pun.

**Q: dapatkah saya mengatur DPI yang berbeda untuk output TIFF?**  
A: Ya. Sesuaikan `rasterizationOptions.setResolution(dpiValue)` sebelum membuat `TiffOptions`.

**Q: bagaimana saya dapat mengubah dimensi PDF untuk PDF yang ada tanpa merender ulang CAD?**  
A: Gunakan Aspose.PDF untuk memuat PDF yang dihasilkan dan panggil `pdf.getPages().setPageSize(PageSize.A4)` atau ukuran khusus.

**Q: apa cara terbaik untuk mengonversi dxf ke pdf sambil mempertahankan lapisan?**  
A: Pertahankan `setAutomaticLayoutsScaling(true)` dan hindari `setNoScaling(true)`; ini menjaga visibilitas lapisan dan kesetiaan tata letak.

## Kesimpulan

Selamat! Anda telah berhasil **convert CAD to PDF** dan **export CAD to TIFF** sambil **set canvas size java**, mengaktifkan **automatic layout scaling**, serta mempelajari cara **configure canvas mode** untuk output berkualitas tinggi. Tutorial ini memberikan fondasi yang kuat untuk proyek konversi CAD Anda. Jelajahi lebih banyak fitur dan kemungkinan di [Aspose.CAD documentation](https://reference.aspose.com/cad/java/).

---

**Last Updated:** 2026-08-29  
**Tested with:** Aspose.CAD for Java 24.12  
**Author:** Aspose

## Tutorial Terkait

- [Set Canvas Size – Fitur CAD Lanjutan dengan Aspose.CAD untuk Java](/cad/java/advanced-cad-features/)
- [Ekspor DWG ke PDF di Java – Set PDF Page Size dengan Aspose.CAD](/cad/java/cad-export-options/export-to-pdf/)
- [Set Custom Page Size – PDF dari CAD dengan Auto Layout Scaling](/cad/java/advanced-cad-features/setting-auto-layout-scaling/)

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}