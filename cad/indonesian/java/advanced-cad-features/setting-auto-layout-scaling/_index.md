---
date: 2026-08-29
description: Pelajari cara mengatur ukuran halaman pdf khusus dan membuat PDF dari
  CAD menggunakan Aspose.CAD untuk Java. Panduan langkah‑demi‑langkah ini mencakup
  ekspor CAD ke PDF dengan Auto Layout Scaling.
keywords:
- custom pdf page size
- create pdf from cad
- dwg to pdf java
- custom page size pdf
- java convert cad pdf
lastmod: 2026-08-29
linktitle: Mengatur Auto Layout Scaling
og_description: Atur ukuran halaman pdf khusus saat mengonversi file CAD ke PDF dengan
  Aspose.CAD untuk Java. Ikuti panduan langkah‑demi‑langkah untuk menggunakan Auto
  Layout Scaling dan mencapai hasil tata letak yang sempurna.
og_image_alt: 'Tutorial: set custom pdf page size for CAD to PDF conversion using
  Aspose.CAD Java'
og_title: Atur ukuran halaman pdf khusus untuk ekspor PDF CAD – Aspose.CAD Java
schemas:
- author: Aspose
  dateModified: '2026-08-29'
  description: Learn how to set a custom pdf page size and create PDF from CAD using
    Aspose.CAD for Java. This step‑by‑step guide covers export CAD to PDF with Auto
    Layout Scaling.
  headline: How to set custom pdf page size for CAD PDF export
  type: TechArticle
- description: Learn how to set a custom pdf page size and create PDF from CAD using
    Aspose.CAD for Java. This step‑by‑step guide covers export CAD to PDF with Auto
    Layout Scaling.
  name: How to set custom pdf page size for CAD PDF export
  steps:
  - name: load the CAD file
    text: Loading the source file is the first step in **how to export CAD** to a
      PDF document.
  - name: create rasterization options
    text: The `CadRasterizationOptions` class defines how the CAD drawing is rasterized
      and which page dimensions to use. It also lets you control DPI, background color,
      and other rendering details.
  - name: set auto layout scaling
    text: Enable the automatic scaling feature. This is the core of **how to set scaling**
      for a CAD‑to‑PDF conversion.
  - name: create PDF options
    text: Link the rasterization settings to the PDF export options.
  - name: export to PDF
    text: Finally, save the rendered image as a PDF file. This step completes the
      **convert dxf to pdf** workflow. Repeat the steps above for any additional CAD
      files you need to process, whether they are **DWG**, **DWF**, or other supported
      formats.
  type: HowTo
- questions:
  - answer: Aspose.CAD for Java supports a broad range of formats, including DWG,
      DXF, DWF, and more than 30 additional CAD types.
    question: Is Aspose.CAD for Java compatible with all CAD file formats?
  - answer: Yes, the `CadRasterizationOptions` class provides properties for fine‑tuning
      scaling, DPI, background color, and other rasterization settings.
    question: Can I customize the scaling options further?
  - answer: Refer to the [documentation](https://reference.aspose.com/cad/java/) for
      in‑depth information and examples.
    question: Where can I find additional documentation for Aspose.CAD for Java?
  - answer: Yes, you can explore a [free trial](https://releases.aspose.com/) to experience
      the capabilities of Aspose.CAD for Java.
    question: Is there a free trial available for Aspose.CAD for Java?
  - answer: Visit the [Aspose.CAD forum](https://forum.aspose.com/c/cad/19) to connect
      with the community and seek support.
    question: How can I seek assistance or engage in discussions about Aspose.CAD
      for Java?
  type: FAQPage
second_title: Aspose.CAD Java API
tags:
- custom pdf page size
- Aspose.CAD
- Java CAD conversion
title: Cara mengatur ukuran halaman pdf khusus untuk ekspor PDF CAD
url: /id/java/advanced-cad-features/setting-auto-layout-scaling/
weight: 17
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Set ukuran halaman pdf khusus – buat PDF dari CAD dengan skala tata letak otomatis

## Pendahuluan

Jika Anda perlu **mengatur ukuran halaman pdf khusus** saat Anda **membuat PDF dari CAD** dengan cepat dan dengan skala yang sempurna, Aspose.CAD for Java siap membantu. Auto Layout Scaling secara otomatis mengubah ukuran tata letak CAD untuk mengisi dimensi halaman target, memastikan PDF yang dihasilkan sesuai dengan ukuran lembar yang diinginkan terlepas dari gambar sumber. Dalam tutorial ini kami akan membahas proses lengkap—dari memuat file DXF hingga mengekspor PDF—sementara menyoroti kemampuan **export CAD to PDF** perpustakaan dan menunjukkan bagaimana Anda juga dapat **mengonversi DWG ke PDF** atau **meningkatkan resolusi PDF** bila diperlukan.

## Jawaban Cepat
- **Apa yang dilakukan Auto Layout Scaling?** Itu secara otomatis mengubah ukuran tata letak CAD agar sesuai dengan dimensi halaman target saat rasterisasi.  
- **Format CAD apa yang dapat saya konversi?** Format apa pun yang didukung oleh Aspose.CAD (mis., DXF, DWG, DWF) dapat dikonversi ke PDF.  
- **Apakah saya memerlukan lisensi untuk produksi?** Ya, lisensi komersial diperlukan untuk penggunaan selain evaluasi.  
- **Berapa lama konversi tipikal memakan waktu?** Pada perangkat keras modern, file standar dikonversi dalam kurang dari satu detik.  
- **Bisakah saya mengubah ukuran halaman?** Tentu – gunakan `CadRasterizationOptions` untuk mengatur dimensi halaman khusus.

## Apa itu “membuat PDF dari CAD”?

Membuat PDF dari CAD berarti mengambil gambar teknik berbasis vektor (DXF, DWG, dll.) dan merasternya menjadi dokumen PDF. PDF mempertahankan kesetiaan visual gambar asli sekaligus dapat dilihat secara luas di platform apa pun, dan dapat dibuka pada perangkat yang tidak mendukung format CAD asli.

## Mengapa menggunakan skala tata letak otomatis?

Auto Layout Scaling menjamin setiap tata letak sepenuhnya mengisi halaman PDF tanpa perhitungan manual, menghemat waktu Anda dan menghilangkan kesalahan skala. Ini juga memastikan ketebalan garis dan warna dipertahankan secara akurat pada berbagai ukuran output. Ini menghasilkan output yang konsisten dan berkualitas tinggi pada puluhan file CAD serta mendukung pemrosesan batch untuk proyek besar.

## Prasyarat

1. **Aspose.CAD for Java Library** – unduh versi terbaru dari [halaman unduhan](https://releases.aspose.com/cad/java/).  
2. **Direktori sumber daya** – buat folder di mesin Anda untuk menyimpan file CAD; ganti `"Your Document Directory"` dalam kode dengan path tersebut.  
3. **File CAD contoh** – untuk panduan ini kami akan menggunakan `conic_pyramid.dxf`, yang termasuk dalam set data contoh Aspose.

## Impor namespace

Pertama, impor kelas yang diperlukan. Ini memberi kami akses ke fitur pemuatan gambar, rasterisasi, dan ekspor PDF.

```java
import com.aspose.cad.Image;

import com.aspose.cad.imageoptions.CadRasterizationOptions;
import com.aspose.cad.imageoptions.PdfOptions;
```

## Cara mengatur ukuran halaman khusus untuk PDF dari CAD

Sebelum kita masuk ke kode langkah demi langkah, mari klarifikasi mengapa dimensi halaman khusus penting. Mengatur **ukuran halaman pdf khusus** memungkinkan Anda mencocokkan ukuran lembar standar industri (A4, A1, Letter) atau mendefinisikan kanvas khusus, yang penting untuk pengajuan regulasi, manual teknis, atau pekerjaan cetak resolusi tinggi.

### Langkah 1: muat file CAD

Memuat file sumber adalah langkah pertama dalam **cara mengekspor CAD** ke dokumen PDF.

```java
String srcFile = dataDir + "conic_pyramid.dxf";
Image image = Image.load(srcFile);
```

### Langkah 2: buat opsi rasterisasi

Kelas `CadRasterizationOptions` menentukan bagaimana gambar CAD dirasterisasi dan dimensi halaman mana yang digunakan. Ini juga memungkinkan Anda mengontrol DPI, warna latar belakang, dan detail rendering lainnya.

```java
CadRasterizationOptions rasterizationOptions = new CadRasterizationOptions();
rasterizationOptions.setPageWidth(1600);
rasterizationOptions.setPageHeight(1600);
```

### Langkah 3: atur skala tata letak otomatis

Aktifkan fitur skala otomatis. Ini adalah inti dari **cara mengatur skala** untuk konversi CAD‑ke‑PDF.

```java
rasterizationOptions.setAutomaticLayoutsScaling(true);
```

### Langkah 4: buat opsi PDF

Hubungkan pengaturan rasterisasi ke opsi ekspor PDF.

```java
PdfOptions pdfOptions = new PdfOptions();
pdfOptions.setVectorRasterizationOptions(rasterizationOptions);
```

### Langkah 5: ekspor ke PDF

Akhirnya, simpan gambar yang dirender sebagai file PDF. Langkah ini menyelesaikan alur kerja **convert dxf to pdf**.

```java
image.save(dataDir + "result_out_.pdf", pdfOptions);
```

Ulangi langkah-langkah di atas untuk file CAD tambahan yang perlu Anda proses, baik itu **DWG**, **DWF**, atau format lain yang didukung.

## Kasus penggunaan umum

| Skenario | Mengapa mengatur ukuran halaman khusus? |
|----------|----------------------------------------|
| **Pengajuan gambar konstruksi** | Menyelaraskan PDF dengan ukuran lembar standar A1/A2 yang diperlukan oleh badan regulasi. |
| **Menyisipkan dalam manual teknis** | Menjamin gambar sesuai dengan tata letak manual yang telah ditentukan tanpa skala tambahan. |
| **Pencetakan resolusi tinggi** | Memungkinkan Anda meningkatkan DPI (mis., `rasterizationOptions.setResolution(300)`) sambil menjaga dimensi halaman tetap konsisten. |

## Masalah umum & pemecahan masalah

| Gejala | Penyebab kemungkinan | Perbaikan |
|---------|----------------------|-----------|
| Output PDF kosong | Opsi rasterisasi tidak diatur atau path file salah | Verifikasi path `srcFile` dan pastikan `setPageWidth/Height` tidak nol |
| Skala terdistorsi | `setAutomaticLayoutsScaling` dibiarkan `false` | Aktifkan skala otomatis atau hitung faktor skala secara manual |
| Lapisan hilang | DXF sumber berisi entitas yang tidak didukung | Periksa catatan rilis Aspose.CAD untuk tipe entitas yang didukung |

Aspose.CAD mendukung konversi **30+ format CAD** dan dapat memproses file hingga **500 MB** tanpa memuat seluruh dokumen ke memori, memberikan konversi cepat dan efisien memori untuk beban kerja perusahaan.

## Pertanyaan yang sering diajukan

**Q: Apakah Aspose.CAD for Java kompatibel dengan semua format file CAD?**  
A: Aspose.CAD for Java mendukung berbagai format, termasuk DWG, DXF, DWF, dan lebih dari 30 tipe CAD tambahan.

**Q: Bisakah saya menyesuaikan opsi skala lebih lanjut?**  
A: Ya, kelas `CadRasterizationOptions` menyediakan properti untuk penyetelan halus skala, DPI, warna latar belakang, dan pengaturan rasterisasi lainnya.

**Q: Di mana saya dapat menemukan dokumentasi tambahan untuk Aspose.CAD for Java?**  
A: Lihat [dokumentasi](https://reference.aspose.com/cad/java/) untuk informasi mendalam dan contoh.

**Q: Apakah ada percobaan gratis untuk Aspose.CAD for Java?**  
A: Ya, Anda dapat mencoba [percobaan gratis](https://releases.aspose.com/) untuk merasakan kemampuan Aspose.CAD for Java.

**Q: Bagaimana saya dapat mencari bantuan atau berdiskusi tentang Aspose.CAD for Java?**  
A: Kunjungi [forum Aspose.CAD](https://forum.aspose.com/c/cad/19) untuk terhubung dengan komunitas dan mencari dukungan.

**Pertanyaan umum tambahan**

**Q: Bagaimana cara mengonversi file DWG ke PDF alih-alih DXF?**  
A: Kode yang sama berfungsi; cukup ubah ekstensi file di `srcFile` menjadi `.dwg`.

**Q: Bisakah saya mengatur DPI khusus untuk PDF resolusi tinggi?**  
A: Ya, gunakan `rasterizationOptions.setResolution(300);` (atau DPI apa pun yang Anda butuhkan).

**Q: Apakah memungkinkan untuk menyematkan font dalam PDF yang dihasilkan?**  
A: Aspose.CAD meraster gambar, sehingga font dirender sebagai vektor; tidak diperlukan penyematan font terpisah.

## Kesimpulan

Dengan mengikuti panduan ini, Anda kini tahu cara **mengatur ukuran halaman pdf khusus** dan **membuat PDF dari CAD** menggunakan Aspose.CAD for Java dengan Auto Layout Scaling. Proses ini menyederhanakan alur kerja **export CAD to PDF**, memastikan skala yang konsisten, dan menghemat waktu pengembangan yang berharga. Silakan bereksperimen dengan berbagai ukuran halaman, resolusi, dan format CAD untuk memenuhi kebutuhan proyek Anda, baik Anda **mengonversi DWG ke PDF**, **meningkatkan resolusi PDF**, atau membangun pemroses batch **java CAD to PDF**.

---

**Terakhir diperbarui:** 2026-08-29  
**Diuji dengan:** Aspose.CAD for Java 24.12 (latest)  
**Penulis:** Aspose

## Tutorial Terkait

- [Cara Mengatur Ukuran Halaman PDF dan Mengaktifkan Pelacakan untuk Proses Rendering CAD menggunakan Aspose.CAD for Java](/cad/java/advanced-cad-features/enable-tracking-for-cad-rendering-process/)
- [Atur Ukuran Halaman PDF – Konversi CAD ke PDF (Java)](/cad/java/advanced-cad-features/set-canvas-size-and-mode/)
- [Ekspor DWG ke PDF atau Raster dengan Cepat Menggunakan perpustakaan java cad Aspose.CAD for Java](/cad/java/cad-drawing-conversion/export-dwg-to-pdf-or-raster/)


{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}