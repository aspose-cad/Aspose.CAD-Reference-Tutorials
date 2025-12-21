---
date: 2025-12-21
description: Pelajari cara mengonversi DWG ke PDF dengan mengekspor tata letak DWG
  tertentu ke PDF menggunakan Aspose.CAD untuk Java. Ikuti tutorial dwg ke pdf langkah
  demi langkah ini untuk mempermudah alur kerja CAD Anda.
linktitle: Export Specific DWG Layout to PDF
second_title: Aspose.CAD Java API
title: Konversi DWG ke PDF – Ekspor Tata Letak dengan Aspose.CAD untuk Java
url: /id/java/cad-drawing-conversion/export-specific-dwg-layout-to-pdf/
weight: 14
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Konversi DWG ke PDF – Ekspor Tata Letak Spesifik Menggunakan Aspose.CAD untuk Java

## Introduction

Di dunia Computer‑Aided Design (CAD) yang dinamis, **convert DWG to PDF** merupakan kebutuhan yang sering muncul saat berbagi gambar dengan klien, kontraktor, atau pemangku kepentingan non‑teknis. Aspose.CAD untuk Java membuat konversi ini menjadi mudah, bahkan memungkinkan Anda memilih satu tata letak dari file DWG multi‑layout. Pada tutorial ini kami akan membahas **cara mengekspor tata letak spesifik DWG** ke PDF, sehingga Anda dapat memberikan hasil yang tepat sesuai kebutuhan proyek tanpa halaman tambahan atau pemotongan manual.

## Quick Answers
- **Apa arti “convert DWG to PDF”?** Ini mengubah gambar DWG menjadi dokumen PDF, mempertahankan data vektor dan kesetiaan tata letak.  
- **Perpustakaan mana yang menangani konversi?** Aspose.CAD untuk Java menyediakan API siap pakai.  
- **Apakah saya memerlukan lisensi untuk produksi?** Ya, lisensi komersial diperlukan; versi percobaan gratis dapat digunakan untuk evaluasi.  
- **Bisakah saya memilih satu tata letak?** Tentu – atur properti `Layouts` ke nama tata letak yang diinginkan.  
- **Versi Java apa yang didukung?** Java 8 dan yang lebih baru sepenuhnya kompatibel.

## Prerequisites

Sebelum memulai, pastikan Anda memiliki:

- **Java Development Environment** – JDK 8+ dan IDE pilihan Anda.  
- **Aspose.CAD Library** – Unduh JAR terbaru dari situs resmi **[here](https://releases.aspose.com/cad/java/)**.  
- **DWG File** – Gambar yang berisi setidaknya satu tata letak (misalnya *visualization_-_conference_room.dwg*).  

## Why Export a Specific DWG Layout to PDF?

Banyak file DWG berisi beberapa ruang kertas (layout). Mengekspor seluruh file dapat menghasilkan PDF yang besar dengan halaman yang tidak diinginkan. Memilih satu tata letak:

- Mengurangi ukuran file.  
- Memfokuskan perhatian pemirsa pada lembar gambar yang relevan.  
- Menyesuaikan standar dokumentasi proyek.  

## Step‑by‑Step Guide

### Step 1: Set Up the Project Environment

Buat proyek Java baru (Maven, Gradle, atau IDE biasa) dan tambahkan JAR Aspose.CAD ke classpath Anda. Anda dapat mengunduhnya **[here](https://releases.aspose.com/cad/java/)**.

### Step 2: Import Necessary Packages

Tambahkan namespace Aspose.CAD yang diperlukan ke kelas Java Anda.

```java
import com.aspose.cad.Image;
import com.aspose.cad.imageoptions.CadRasterizationOptions;
import com.aspose.cad.imageoptions.PdfOptions;
```

### Step 3: Load the DWG File

Tunjuk ke file DWG yang ingin Anda konversi dan muat ke objek `Image`.

```java
String srcFile = dataDir + "visualization_-_conference_room.dwg";
Image image = Image.load(srcFile);
```

### Step 4: Configure Rasterization Options

Tentukan ukuran halaman dan, yang paling penting, tata letak yang ingin Anda ekspor.

```java
CadRasterizationOptions rasterizationOptions = new CadRasterizationOptions();
rasterizationOptions.setPageWidth(1600);
rasterizationOptions.setPageHeight(1600);
// Specify desired layout name
rasterizationOptions.setLayouts(new String[] {"Layout1"});
```

### Step 5: Set PDF Export Options

Hubungkan pengaturan rasterisasi dengan pengekspor PDF.

```java
PdfOptions pdfOptions = new PdfOptions();
pdfOptions.setVectorRasterizationOptions(rasterizationOptions);
```

### Step 6: Export DWG to PDF

Simpan hasilnya sebagai file PDF. Output akan berisi hanya **Layout1**, menghasilkan operasi **convert DWG to PDF** yang bersih.

```java
image.save(dataDir + "ExportSpecificLayoutToPDF_out_.pdf", pdfOptions);
```

## Common Issues and Solutions

| Masalah | Mengapa Terjadi | Solusi |
|-------|----------------|-----|
| **Layout not found** | Nama tata letak salah ketik atau tidak ada dalam DWG. | Gunakan `image.getLayoutNames()` untuk menampilkan tata letak yang tersedia, lalu pilih yang benar. |
| **Low resolution PDF** | `PageWidth`/`PageHeight` terlalu kecil. | Tingkatkan dimensi (mis., 2000 × 2000) atau setel `rasterizationOptions.setResolution(300);`. |
| **License exception** | Menjalankan tanpa lisensi yang valid di lingkungan non‑trial. | Terapkan lisensi Aspose.CAD Anda sebelum memuat gambar: `License license = new License(); license.setLicense("Aspose.CAD.lic");`. |

## Frequently Asked Questions

**Q1: Bisakah saya menggunakan Aspose.CAD untuk Java bersama perpustakaan CAD berbasis Java lainnya?**  
A: Aspose.CAD untuk Java adalah perpustakaan mandiri tetapi dapat diintegrasikan dengan perpustakaan berbasis Java lainnya untuk fungsionalitas tambahan.

**Q2: Apakah ada opsi lisensi untuk Aspose.CAD?**  
A: Ya, Anda dapat menjelajahi opsi lisensi dan detail pembelian **[here](https://purchase.aspose.com/buy)**.

**Q3: Bagaimana cara mendapatkan lisensi sementara untuk Aspose.CAD?**  
A: Kunjungi **[this link](https://purchase.aspose.com/temporary-license/)** untuk meminta lisensi sementara.

**Q4: Di mana saya dapat menemukan dukungan untuk Aspose.CAD?**  
A: Untuk pertanyaan atau bantuan, kunjungi **[Aspose.CAD forum](https://forum.aspose.com/c/cad/19)**.

**Q5: Apakah ada versi percobaan gratis untuk Aspose.CAD?**  
A: Ya, Anda dapat mengakses versi percobaan gratis **[here](https://releases.aspose.com/)**.

## Conclusion

Dengan mengikuti **dwg to pdf tutorial** ini, Anda kini memiliki cara andal untuk **convert DWG to PDF** sambil menargetkan satu tata letak. Pendekatan ini menghemat ruang penyimpanan, mempercepat berbagi dokumen, dan menjaga alur kerja CAD Anda tetap rapi. Jangan ragu untuk bereksperimen dengan pengaturan rasterisasi yang berbeda atau menggabungkan beberapa tata letak menjadi satu PDF seiring perkembangan proyek Anda.

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}

---

**Terakhir Diperbarui:** 2025-12-21  
**Diuji Dengan:** Aspose.CAD for Java 24.12  
**Penulis:** Aspose