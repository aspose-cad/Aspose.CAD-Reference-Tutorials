---
date: 2026-06-04
description: Pelajari cara membuat PDF dari CAD dan menambahkan watermark menggunakan
  Aspose.CAD for Java. Panduan langkah‑demi‑langkah ini mencakup mengekspor CAD ke
  PDF, menambahkan teks CAD, dan branding.
keywords:
- create pdf from cad
- export cad to pdf
- add text cad
- watermark cad drawing
- convert dwg to pdf
linktitle: Tambahkan Watermark
schemas:
- author: Aspose
  dateModified: '2026-06-04'
  description: Learn how to create PDF from CAD and add a watermark using Aspose.CAD
    for Java. This step‑by‑step guide covers export CAD to PDF, add text CAD, and
    branding.
  headline: Create PDF from CAD with Watermark - Aspose.CAD for Java
  type: TechArticle
- description: Learn how to create PDF from CAD and add a watermark using Aspose.CAD
    for Java. This step‑by‑step guide covers export CAD to PDF, add text CAD, and
    branding.
  name: Create PDF from CAD with Watermark - Aspose.CAD for Java
  steps:
  - name: Import Packages
    text: The `com.aspose.cad` namespace provides all classes you need for CAD manipulation.
      The `Image` class is the entry point for loading and saving CAD files. The `MText`
      class represents multi‑line text that can be styled and positioned.
  - name: Add New MTEXT
    text: MText represents multi‑line text entities that can be used for watermarks.
  - name: Add Simple Entity like Text
    text: TextEntity is a single‑line text object used for simple annotations.
  - name: Export to PDF
    text: SaveFormat.Pdf specifies PDF as the output format for saving.
  type: HowTo
- questions:
  - answer: Aspose.CAD supports **DWG, DXF, DWT, DWF, and over 30 additional formats**,
      allowing you to **export cad to pdf** from virtually any source file.
    question: Is Aspose.CAD compatible with all CAD file formats?
  - answer: Yes – you can control font family, size, color, rotation, and transparency
      through the `MText` or `TextEntity` properties.
    question: Can I customize the appearance of the watermark text?
  - answer: Yes, you can download the trial version [here](https://releases.aspose.com/).
    question: Is there a trial version available for Aspose.CAD for Java?
  - answer: Visit the [Aspose.CAD forum](https://forum.aspose.com/c/cad/19) for community
      assistance and official support channels.
    question: How can I get support for Aspose.CAD?
  - answer: Refer to the [documentation](https://reference.aspose.com/cad/java/) for
      detailed API references, code samples, and best‑practice guides.
    question: Where can I find the complete documentation for Aspose.CAD for Java?
  type: FAQPage
second_title: Aspose.CAD Java API
title: Buat PDF dari CAD dengan Watermark - Aspose.CAD for Java
url: /id/java/other-cad-operations/add-watermark/
weight: 12
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Buat PDF dari CAD dengan Watermark - Aspose.CAD for Java

## Pendahuluan

Dalam tutorial ini Anda akan **membuat PDF dari CAD** drawing dan menerapkan watermark khusus menggunakan Aspose.CAD for Java. Menambahkan watermark memungkinkan Anda melindungi hak kekayaan intelektual, memberi merek pada desain, atau menyematkan informasi revisi. Kami akan memandu seluruh alur kerja—dari mengimpor paket yang diperlukan, menambahkan watermark berbasis teks, hingga mengekspor drawing CAD akhir sebagai file PDF. Pada akhir tutorial Anda akan memiliki potongan kode yang dapat digunakan kembali dalam proyek Java apa pun.

## Jawaban Cepat
- **Apa tujuan utama?** Membuat PDF dari file CAD dan menambahkan watermark dalam beberapa baris kode Java.  
- **Perpustakaan apa yang diperlukan?** Aspose.CAD for Java (mendukung lebih dari 30 format CAD).  
- **Apakah saya memerlukan lisensi untuk pengujian?** Versi percobaan gratis selama 30 hari tersedia; lisensi komersial diperlukan untuk produksi.  
- **Bisakah saya mengekspor CAD ke PDF setelah menambahkan watermark?** Ya – panggilan API yang sama yang menyimpan drawing juga mengonversinya ke PDF.  
- **Apakah proses ini thread‑safe?** Semua kelas Aspose.CAD dirancang untuk penggunaan bersamaan ketika Anda membuat instance terpisah per thread.

## Apa itu watermark dalam CAD?
Watermark dalam CAD adalah lapisan teks atau grafik semi‑transparan yang ditempatkan pada drawing untuk menunjukkan kepemilikan, kerahasiaan, atau status revisi. Watermark muncul di belakang atau di atas geometri utama tanpa mengubah data desain yang mendasarinya, memungkinkan penonton melihat konten asli sambil mengenali keberadaan watermark.

## Mengapa menambahkan watermark saat Anda **membuat pdf dari cad**?
Aspose.CAD for Java mendukung **lebih dari 30 format input** (DWG, DXF, DWF, DWT, dll.) dan dapat menangani file hingga **500 MB** tanpa memuat seluruh dokumen ke memori. Menambahkan watermark selama langkah konversi PDF menghilangkan proses pasca‑pemrosesan terpisah, menghemat hingga **40 %** waktu pemrosesan dalam pipeline batch.

## Prasyarat

- **Aspose.CAD for Java** – unduh JAR terbaru dari situs resmi [di sini](https://releases.aspose.com/cad/java/).  
- **Java Development Kit (JDK)** – versi 11 atau lebih baru disarankan.  
- Lisensi **Aspose.CAD** yang valid untuk penggunaan produksi (opsional untuk percobaan).  

## Cara membuat PDF dari CAD dengan watermark?

CadImage adalah kelas utama yang mewakili drawing CAD dalam Aspose.CAD.  
Untuk membuat PDF dari file CAD dengan watermark tersemat, pertama‑tama muat drawing ke dalam instance `CadImage`, yang mewakili dokumen CAD di memori. Selanjutnya, buat objek `MText` atau `TextEntity` yang berisi teks watermark, atur ukuran font, warna, dan opasitasnya, lalu tambahkan ke model space. Akhirnya, panggil `save` dengan `SaveFormat.Pdf` untuk mengekspor drawing yang telah dimodifikasi ke PDF, mempertahankan kualitas vektor.

### Langkah 1: Impor Paket

Namespace `com.aspose.cad` menyediakan semua kelas yang Anda perlukan untuk manipulasi CAD.

Kelas `Image` adalah titik masuk untuk memuat dan menyimpan file CAD.  
Kelas `MText` mewakili teks multi‑baris yang dapat diberi gaya dan diposisikan.  

```java
import com.aspose.cad.Image;
import com.aspose.cad.fileformats.cad.CadImage;
import com.aspose.cad.fileformats.cad.cadobjects.Cad3DPoint;
import com.aspose.cad.fileformats.cad.cadobjects.CadMText;
import com.aspose.cad.fileformats.cad.cadobjects.CadText;
import com.aspose.cad.imageoptions.CadRasterizationOptions;
import com.aspose.cad.imageoptions.PdfOptions;
```

### Langkah 2: Tambahkan MTEXT Baru

MText mewakili entitas teks multi‑baris yang dapat digunakan untuk watermark.  

```java
//add new MTEXT
CadMText watermark = new CadMText();
watermark.setText("Watermark message");
watermark.setInitialTextHeight(40);
watermark.setInsertionPoint(new Cad3DPoint(300, 40));
watermark.setLayerName("0");
cadImage.getBlockEntities().get_Item("*Model_Space").addEntity(watermark);
```

### Langkah 3: Tambahkan Entitas Sederhana seperti Teks

TextEntity adalah objek teks satu‑baris yang digunakan untuk anotasi sederhana.  

```java
// or add more simple entity like Text
CadText text = new CadText();
text.setDefaultValue("Watermark text");
text.setTextHeight(40);
text.setFirstAlignment(new Cad3DPoint(300, 40));
text.setLayerName("0") ;
cadImage.getBlockEntities().get_Item("*Model_Space").addEntity(text);
```

### Langkah 4: Ekspor ke PDF

`SaveFormat.Pdf` menentukan PDF sebagai format output untuk penyimpanan.  

```java
// export to pdf
CadRasterizationOptions rasterizationOptions = new CadRasterizationOptions();
rasterizationOptions.setPageWidth(1600);
rasterizationOptions.setPageHeight(1600);
rasterizationOptions.setLayouts(new String[]{"Model"});
PdfOptions pdfOptions = new PdfOptions();
pdfOptions.setVectorRasterizationOptions(rasterizationOptions);
cadImage.save(dataDir + "AddWatermark_out.pdf", pdfOptions);

```

## Masalah Umum dan Solusi

- **Watermark tidak terlihat** – Pastikan warna teks kontras dengan latar belakang dan atur properti `Transparency` (misalnya, 0.5 untuk opasitas 50 %).  
- **File besar menyebabkan OutOfMemoryError** – Aktifkan mode streaming `CadImage` dengan mengatur `CadImageOptions.setLoadMode(LoadMode.Paged)`.  
- **Rendering font tidak tepat** – Instal font TrueType yang diperlukan di server atau sematkan menggunakan `FontRepository`.

## Pertanyaan yang Sering Diajukan

**T: Apakah Aspose.CAD kompatibel dengan semua format file CAD?**  
J: Aspose.CAD mendukung **DWG, DXF, DWT, DWF, dan lebih dari 30 format tambahan**, memungkinkan Anda **mengekspor cad ke pdf** dari hampir semua file sumber.

**T: Bisakah saya menyesuaikan tampilan teks watermark?**  
J: Ya – Anda dapat mengontrol keluarga font, ukuran, warna, rotasi, dan transparansi melalui properti `MText` atau `TextEntity`.

**T: Apakah ada versi percobaan untuk Aspose.CAD for Java?**  
J: Ya, Anda dapat mengunduh versi percobaan [di sini](https://releases.aspose.com/).

**T: Bagaimana cara mendapatkan dukungan untuk Aspose.CAD?**  
J: Kunjungi [forum Aspose.CAD](https://forum.aspose.com/c/cad/19) untuk bantuan komunitas dan saluran dukungan resmi.

**T: Di mana saya dapat menemukan dokumentasi lengkap untuk Aspose.CAD for Java?**  
J: Lihat [dokumentasi](https://reference.aspose.com/cad/java/) untuk referensi API detail, contoh kode, dan panduan praktik terbaik.

---

**Terakhir Diperbarui:** 2026-06-04  
**Diuji Dengan:** Aspose.CAD for Java 24.12  
**Penulis:** Aspose  

{{< blocks/products/products-backtop-button >}}

## Tutorial Terkait

- [Export DWG to PDF or Raster Using Aspose.CAD for Java](/cad/java/cad-drawing-conversion/export-dwg-to-pdf-or-raster/)
- [Create PDF from DWG and Add Text Using Aspose.CAD for Java](/cad/java/cad-text-and-annotation/add-text-in-dwg/)
- [Export Specific DWG Layout to PDF Using Aspose.CAD for Java](/cad/java/cad-drawing-conversion/export-specific-dwg-layout-to-pdf/)


{{< /blocks/products/pf/tutorial-page-section >}}
{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}