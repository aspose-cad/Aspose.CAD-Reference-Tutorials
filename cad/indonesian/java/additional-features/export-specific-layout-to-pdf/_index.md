---
date: 2025-12-04
description: Pelajari cara mengekspor file DXF ke PDF dengan Aspose.CAD untuk Java,
  membuat PDF dari DXF, dan mengatur ukuran halaman Java untuk konversi CAD yang akurat.
language: id
linktitle: Export Specific DXF Layout to PDF with Java
second_title: Aspose.CAD Java API
title: Cara Mengekspor Tata Letak DXF ke PDF dengan Aspose.CAD untuk Java
url: /java/additional-features/export-specific-layout-to-pdf/
weight: 17
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Cara Mengekspor Tata Letak DXF ke PDF dengan Aspose.CAD untuk Java

## Introduction

Jika Anda seorang pengembang Java yang bekerja dengan gambar CAD, Anda tahu bahwa **cara mengekspor dxf** secara akurat dapat menentukan keberhasilan sebuah proyek. Baik Anda menghasilkan laporan teknik, berbagi desain dengan klien, atau mengotomatiskan konversi batch, sebuah perpustakaan konversi PDF Java yang handal sangat penting. Dalam tutorial ini kami akan memandu Anda mengekspor tata letak DXF tertentu ke PDF menggunakan **Aspose.CAD for Java**, menunjukkan cara **membuat pdf dari dxf**, mengontrol dimensi halaman, dan menjaga kualitas vektor tetap utuh.

## Quick Answers
- **Apa perpustakaan utama?** Aspose.CAD for Java, sebuah perpustakaan konversi pdf Java khusus untuk CAD.
- **Apakah saya dapat memilih tata letak tertentu?** Ya – gunakan `CadRasterizationOptions.setLayouts()` untuk menargetkan nama tata letak.
- **Bagaimana cara mengatur ukuran halaman?** Sesuaikan `setPageWidth()` dan `setPageHeight()` dalam opsi rasterisasi (mis., 1600 × 1600).
- **Apakah saya memerlukan lisensi untuk produksi?** Lisensi komersial diperlukan untuk penggunaan produksi; versi percobaan gratis tersedia.
- **Versi Java apa yang didukung?** Java 8 ke atas (JDK 1.8+).

## What is “how to export dxf” in Java?

Mengekspor file DXF berarti mengonversi data vektornya ke format lain—biasanya PDF—sementara mempertahankan lapisan, ketebalan garis, dan informasi tata letak. Aspose.CAD menangani pekerjaan berat, memungkinkan Anda fokus pada logika bisnis daripada parsing file tingkat rendah.

## Why use Aspose.CAD for Java?

- **Dukungan CAD lengkap** – Menangani DWG, DXF, DWF, dan lainnya.
- **Tanpa dependensi eksternal** – Pure Java, tanpa DLL native.
- **Rasterisasi presisi** – Pilih output vektor atau raster, atur DPI, ukuran halaman, dan tata letak.
- **Kinerja tinggi** – Dioptimalkan untuk pemrosesan batch dan skenario sisi server.

## Prerequisites

Sebelum Anda memulai, pastikan Anda memiliki:

1. **Java Development Kit (JDK)** – Java 8 atau lebih baru. Unduh dari [Oracle](https://www.oracle.com/java/technologies/javase-downloads.html).
2. **Aspose.CAD for Java** – Dapatkan JAR terbaru dari [halaman unduhan Aspose.CAD](https://releases.aspose.com/cad/java/).
3. IDE atau alat build (Maven/Gradle) untuk menambahkan JAR Aspose.CAD ke classpath proyek Anda.

## Import Namespaces

First, import the classes you’ll need. These imports give you access to image loading, rasterization options, and PDF output settings.

```java
import com.aspose.cad.Image;
import com.aspose.cad.imageoptions.CadRasterizationOptions;
import com.aspose.cad.imageoptions.PdfOptions;
```

### Step‑by‑Step Guide

### Step 1: Set the Resource Directory

Define the folder that contains your DXF files. Replace the placeholder with the actual path on your machine.

```java
String dataDir = "Your Document Directory" + "DXFDrawings/";
```

> **Pro tip:** Use `System.getProperty("user.dir")` to build a relative path that works across environments.

### Step 2: Load the DXF File

Load the source DXF using `Image.load()`. This method reads the CAD file into an Aspose.CAD `Image` object.

```java
String srcFile = dataDir + "conic_pyramid.dxf";
Image image = Image.load(srcFile); 
```

### Step 3: Configure Rasterization Options (Set Page Size Java)

Here we create `CadRasterizationOptions` and define the output page size. Adjust the width/height to match the desired PDF dimensions.

```java
CadRasterizationOptions rasterizationOptions = new CadRasterizationOptions();
rasterizationOptions.setPageWidth(1600);
rasterizationOptions.setPageHeight(1600);   
rasterizationOptions.setLayouts(new String[] {"Model"});
```

- `setPageWidth` / `setPageHeight` – mengontrol **set page size java** untuk PDF.
- `setLayouts` – menentukan tata letak mana yang akan dirender; `"Model"` adalah ruang model default di banyak file DXF.

### Step 4: Create PDF Options (Java Convert CAD PDF)

Link the rasterization settings to a `PdfOptions` instance. This tells Aspose.CAD to output a PDF rather than a raster image.

```java
PdfOptions pdfOptions = new PdfOptions();
pdfOptions.setVectorRasterizationOptions(rasterizationOptions);
```

### Step 5: Export DXF to PDF (Create PDF from DXF)

Finally, save the image as a PDF. The output file name ends with `_layout_out_.pdf` to indicate the layout‑specific conversion.

```java
image.save(dataDir + "conic_pyramid_layout_out_.pdf", pdfOptions);
```

After execution, you’ll find `conic_pyramid_layout_out_.pdf` in the same directory, containing only the **Model** layout rendered at the dimensions you set.

## Common Issues and Solutions

| Issue | Reason | Fix |
|-------|--------|-----|
| **PDF Kosong** | Nama tata letak tidak cocok | Verifikasi nama tata letak yang tepat di DXF (gunakan penampil CAD). |
| **Ukuran halaman tidak tepat** | `setPageWidth/Height` tidak diterapkan | Pastikan Anda mengatur opsi rasterisasi **sebelum** membuat `PdfOptions`. |
| **Kehabisan memori untuk file besar** | Memuat DXF besar ke memori | Gunakan streaming atau tingkatkan heap JVM (`-Xmx2g`). |
| **Font hilang** | Elemen teks menggunakan font yang tidak tersedia | Instal font yang diperlukan di server atau sematkan melalui `CadRasterizationOptions`. |

## Frequently Asked Questions

**T: Apakah Aspose.CAD for Java cocok untuk pemula maupun pengembang berpengalaman?**  
J: Tentu saja. API-nya mudah dipahami untuk pemula sekaligus menawarkan kustomisasi mendalam bagi pengguna tingkat lanjut.

**T: Bisakah saya menyesuaikan opsi rasterisasi untuk tata letak yang berbeda?**  
J: Ya. Sesuaikan `CadRasterizationOptions` (ukuran halaman, DPI, warna latar) per tata letak sesuai kebutuhan.

**T: Di mana saya dapat menemukan dokumentasi lengkap untuk Aspose.CAD for Java?**  
J: Dokumentasi detail tersedia [di sini](https://reference.aspose.com/cad/java/).

**T: Apakah tersedia versi percobaan gratis untuk Aspose.CAD for Java?**  
J: Ya, Anda dapat mengunduh versi percobaan [di sini](https://releases.aspose.com/).

**T: Bagaimana saya dapat mendapatkan dukungan untuk Aspose.CAD for Java?**  
J: Kunjungi forum dukungan [di sini](https://forum.aspose.com/c/cad/19) untuk bantuan komunitas dan staf.

## Conclusion

Dalam panduan ini kami menunjukkan **cara mengekspor dxf** tata letak ke PDF menggunakan Aspose.CAD for Java, mencakup semua hal mulai dari menyiapkan lingkungan hingga menyempurnakan dimensi halaman. Dengan memanfaatkan **perpustakaan konversi pdf java** ini, Anda dapat mengotomatisasi alur kerja CAD‑ke‑PDF, mempertahankan kesetiaan vektor, dan mengintegrasikan pembuatan PDF yang mulus ke dalam aplikasi Java Anda.

---

**Last Updated:** 2025-12-04  
**Tested With:** Aspose.CAD for Java 24.12 (latest at time of writing)  
**Author:** Aspose  

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}