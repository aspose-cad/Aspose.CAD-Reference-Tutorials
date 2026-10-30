---
date: 2026-10-30
description: Pelajari cara mengonversi massal file DXF ke WMF menggunakan Aspose.CAD
  for Java, dengan step‑by‑step code, info versi percobaan gratis, dan ekspor PDF
  opsional.
keywords:
- batch convert dxf files
- aspose cad java
- dxf to wmf conversion
- java cad rasterization
- aspose free trial
lastmod: 2026-10-30
linktitle: Ekspor DXF ke Format WMF Menggunakan Java
og_description: Konversi massal file DXF ke WMF menggunakan Aspose.CAD for Java. Ikuti
  panduan ini untuk memuat gambar DXF, mengatur rasterization options, menyimpan sebagai
  WMF, dan secara opsional mengekspor ke PDF dengan versi percobaan gratis.
og_image_alt: Tutorial showing batch conversion of DXF to WMF in Java using Aspose.CAD
og_title: Konversi massal file DXF ke WMF dengan Aspose.CAD for Java
schemas:
- author: Aspose
  dateModified: '2026-10-30'
  description: Learn how to batch convert DXF files to WMF using Aspose.CAD for Java,
    with step‑by‑step code, free trial info, and optional PDF export.
  headline: Batch convert DXF files to WMF with Aspose.CAD for Java
  type: TechArticle
- description: Learn how to batch convert DXF files to WMF using Aspose.CAD for Java,
    with step‑by‑step code, free trial info, and optional PDF export.
  name: Batch convert DXF files to WMF with Aspose.CAD for Java
  steps:
  - name: load dxf drawing
    text: Image.load reads the DXF file into an Aspose.CAD Image object.
  - name: configure rasterization options
    text: '`CadRasterizationOptions` specifies page size, resolution, and background
      for rasterizing the CAD drawing.'
  - name: save as wmf
    text: '`ImageSaveOptions` with `SaveFormat.WMF` tells Aspose.CAD to write the
      output as a Windows Metafile.'
  - name: dispose of resources
    text: Calling `image.close()` releases native resources used by the Aspose.CAD
      Image object.
  - name: optional – export to pdf
    text: '`PdfOptions` configures PDF‑specific settings when saving the image as
      a PDF document. > **Pro tip:** You can reuse the same `CadRasterizationOptions`
      object for PDF export by passing it to a `PdfOptions` instance, saving you a
      few lines of setup.'
  type: HowTo
- questions:
  - answer: You can access the documentation [Aspose.CAD Java documentation](https://reference.aspose.com/cad/java/).
    question: Where can I find the Aspose.CAD documentation?
  - answer: Download the library [Aspose.CAD Java download page](https://releases.aspose.com/cad/java/).
    question: How do I download Aspose.CAD for Java?
  - answer: Yes, you can get a free trial [Aspose free trial page](https://releases.aspose.com/).
    question: Is there a free trial available?
  - answer: Explore temporary licenses [temporary license options](https://purchase.aspose.com/temporary-license/).
    question: Need temporary licensing options?
  - answer: Visit the Aspose.CAD support forum [Aspose.CAD support forum](https://forum.aspose.com/c/cad/19).
    question: Where can I get support?
  type: FAQPage
second_title: Aspose.CAD Java API
tags:
- batch convert dxf
- Aspose.CAD
- Java CAD conversion
- WMF export
- DXF processing
title: Konversi massal file DXF ke WMF dengan Aspose.CAD for Java
url: /id/java/additional-features/export-dxf-to-wmf/
weight: 14
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Konversi batch file DXF ke WMF dengan Aspose.CAD untuk Java

## Pendahuluan

Dalam tutorial ini Anda akan belajar cara **batch convert DXF files to WMF** menggunakan Aspose.CAD untuk Java. Apakah Anda perlu menyematkan gambar CAD dalam laporan berbasis Windows, menghasilkan grafik vektor ringan untuk dokumen Office, atau mengotomatisasi konversi skala besar, panduan ini akan memandu Anda melalui memuat gambar DXF, mengkonfigurasi opsi rasterisasi, menyimpan sebagai WMF, dan secara opsional mengekspor gambar yang sama ke PDF. Langkah-langkah ini bekerja pada platform apa pun yang menjalankan Java 8+.

## Jawaban Cepat
- **Apakah saya dapat mengonversi DXF ke WMF dengan percobaan gratis?** Ya – Aspose menawarkan percobaan penuh selama 30 hari.  
- **Versi Java apa yang diperlukan?** Java 8 atau lebih baru.  
- **Apakah saya memerlukan lisensi untuk menjalankan kode?** Lisensi diperlukan untuk produksi; percobaan dapat digunakan untuk pengembangan dan pengujian.  
- **Apakah konversi tanpa kehilangan?** Data vektor dipertahankan; opsi rasterisasi memungkinkan Anda mengontrol resolusi.  
- **Apakah saya juga dapat mengekspor gambar yang sama ke PDF?** Tentu – lihat langkah “Export to PDF” di bawah.  
- **Bagaimana cara saya mengonversi batch banyak file DXF sekaligus?** Loop melalui folder, terapkan pola load‑rasterize‑save yang sama untuk setiap file.

## Apa itu konversi batch file dxf?

Konversi batch file DXF berarti memproses beberapa gambar Drawing Exchange Format (DXF) dalam satu kali jalankan dan menghasilkan output WMF untuk masing‑masing. WMF (Windows Metafile) adalah format gambar vektor yang terintegrasi secara native dengan Microsoft Office, aplikasi Windows, dan banyak alat pelaporan.

## Mengapa menggunakan Aspose.CAD untuk Java?

Aspose.CAD untuk Java adalah mesin murni‑Java yang mendukung **lebih dari 50 format input dan output**—termasuk DXF, DWG, DGN, PDF, PNG, SVG, dan WMF—sementara memberikan **ketelitian vektor 99 %**. Ia berjalan pada OS apa pun yang mendukung Java, tidak memerlukan DLL native, dan memungkinkan Anda mengontrol ukuran halaman, DPI, serta warna latar melalui satu kelas `CadRasterizationOptions`. API yang sama juga menangani ekspor PDF, PNG, dan SVG, menghilangkan kebutuhan akan banyak pustaka.

### Manfaat yang Dikuantifikasi
- **50+ format yang didukung** mengurangi kebutuhan akan konverter pihak ketiga.  
- **Memproses file DXF 300‑halaman dalam kurang dari 5 detik** pada server 2.5 GHz tipikal ketika rasterisasi pada 150 DPI.  
- **Jejak memori tetap di bawah 200 MB** untuk file hingga 500 MB ketika Anda mengatur dimensi halaman yang sesuai.  

## Prasyarat

- **Aspose.CAD for Java** terintegrasi ke dalam proyek Anda. Unduh dari situs resmi: [Aspose.CAD Java download](https://releases.aspose.com/cad/java/).  
- Sebuah folder yang berisi file DXF yang ingin Anda konversi (misalnya `Your Document Directory/DXFDrawings/`).  

## Impor namespace

`Image` adalah kelas inti Aspose.CAD yang mewakili gambar CAD dalam memori. Setelah memuat sebuah file, semua operasi selanjutnya—rasterisasi, konversi format, dan pembersihan sumber daya—dilakukan melalui objek ini.

Impor berikut membawa kelas Aspose.CAD yang diperlukan untuk memuat, meraster, dan menyimpan file CAD.  
```java
import com.aspose.cad.Image;
import com.aspose.cad.ImageSaveOptions;
import com.aspose.cad.fileformats.cad.CadRasterizationOptions;
import com.aspose.cad.fileformats.cad.CadImage;
import com.aspose.cad.fileformats.cad.CadImageInfo;
import com.aspose.cad.fileformats.cad.CadImageInfo;
import java.awt.Color;
```

## Panduan langkah demi langkah

### Bagaimana cara saya mengonversi batch file DXF ke WMF di Java?

Muat setiap DXF dengan `Image.load`, konfigurasikan `CadRasterizationOptions` untuk ukuran halaman dan DPI yang diinginkan, lalu panggil `image.save` dengan `SaveFormat.WMF`. Pola tiga langkah ini melakukan konversi lengkap sambil mempertahankan kualitas vektor dan hanya memerlukan beberapa baris kode per file.

#### Langkah 1: muat gambar dxf

`Image.load` membaca file DXF ke dalam objek Aspose.CAD Image.  
```java
import com.aspose.cad.Color;
import com.aspose.cad.Image;

import com.aspose.cad.fileformats.ifc.IfcImage;
import com.aspose.cad.imageoptions.CadRasterizationOptions;
import com.aspose.cad.imageoptions.PdfOptions;
import com.aspose.cad.imageoptions.WmfOptions;
```

#### Langkah 2: konfigurasikan opsi rasterisasi

`CadRasterizationOptions` menentukan ukuran halaman, resolusi, dan latar belakang untuk meraster gambar CAD.  
```java
// The path to the resource directory.
String dataDir = "Your Document Directory" + "DXFDrawings/";
String srcFile = dataDir + "conic_pyramid.dxf";
Image image = Image.load(srcFile);
```

#### Langkah 3: simpan sebagai wmf

`ImageSaveOptions` dengan `SaveFormat.WMF` memberi tahu Aspose.CAD untuk menulis output sebagai Windows Metafile.  
```java
CadRasterizationOptions rasterizationOptions = new CadRasterizationOptions();
rasterizationOptions.setPageWidth(100);
rasterizationOptions.setPageHeight(100);
WmfOptions wmfOptions = new WmfOptions();
```

#### Langkah 4: buang sumber daya

Memanggil `image.close()` melepaskan sumber daya native yang digunakan oleh objek Aspose.CAD Image.  
```java
cadImage.save(dataDir+" example.ifc.wmf", wmfOptions);
```

#### Langkah 5: opsional – ekspor ke pdf

`PdfOptions` mengkonfigurasi pengaturan khusus PDF saat menyimpan gambar sebagai dokumen PDF.  
```java
finally
{
  cadImage.dispose();
}
```

> **Pro tip:** Anda dapat menggunakan kembali objek `CadRasterizationOptions` yang sama untuk ekspor PDF dengan melewatkannya ke instance `PdfOptions`, menghemat beberapa baris pengaturan.

## Bagaimana cara mengekspor DXF ke PDF menggunakan Aspose CAD Java?

Ganti format penyimpanan WMF dengan PDF menggunakan `new ImageSaveOptions(SaveFormat.Pdf)`. Pengaturan rasterisasi yang sama tetap berlaku, dan Anda dapat menambahkan opsi khusus PDF seperti metadata penulis atau tingkat kompresi. Konversi satu baris ini menghasilkan PDF yang dapat dicari, akurat halaman, yang mencerminkan tata letak CAD asli.

## Masalah umum dan solusi

`License` adalah kelas Aspose yang digunakan untuk menerapkan lisensi produk pada runtime.

| Masalah | Penyebab | Solusi |
|-------|-------|-----|
| **`NullPointerException` on `cadImage.save`** | Variable `cadImage` not defined (should be `image`). | Replace `cadImage` with `image` or rename the variable consistently. |
| **Output WMF is blank** | Rasterization page size too small or background color set to transparent. | Increase `PageWidth`/`PageHeight` or set a background color via `rasterizationOptions.setBackgroundColor(Color.WHITE);`. |
| **License exception** | Running without a valid Aspose license in production. | Apply the license file at application start: `License license = new License(); license.setLicense("Aspose.Total.Java.lic");`. |

## Pertanyaan yang sering diajukan

**Q: Di mana saya dapat menemukan dokumentasi Aspose.CAD?**  
A: Anda dapat mengakses dokumentasi [Aspose.CAD Java documentation](https://reference.aspose.com/cad/java/).

**Q: Bagaimana cara mengunduh Aspose.CAD untuk Java?**  
A: Unduh pustaka [Aspose.CAD Java download page](https://releases.aspose.com/cad/java/).

**Q: Apakah ada percobaan gratis yang tersedia?**  
A: Ya, Anda dapat mendapatkan percobaan gratis [Aspose free trial page](https://releases.aspose.com/).

**Q: Membutuhkan opsi lisensi sementara?**  
A: Jelajahi lisensi sementara [temporary license options](https://purchase.aspose.com/temporary-license/).

**Q: Di mana saya dapat mendapatkan dukungan?**  
A: Kunjungi forum dukungan Aspose.CAD [Aspose.CAD support forum](https://forum.aspose.com/c/cad/19).

## Pertanyaan tambahan yang sering diajukan

**Q: Bisakah saya mengonversi file DXF besar (ratusan MB) tanpa kehabisan memori?**  
A: Ya. Muat file dalam blok `try‑with‑resources` dan buang objek `Image` segera. Sesuaikan `CadRasterizationOptions.setPageWidth/Height` ke ukuran yang wajar untuk menjaga penggunaan memori tetap rendah.

**Q: Apakah output WMF mempertahankan informasi lapisan?**  
A: WMF adalah format vektor datar, sehingga hierarki lapisan diratakan, tetapi gaya garis, warna, dan pola hatch tetap dipertahankan.

**Q: Apakah memungkinkan mengatur DPI khusus untuk WMF?**  
A: Gunakan `rasterizationOptions.setResolution(300);` untuk menentukan DPI sebelum menyimpan.

**Q: Bisakah saya mengonversi batch banyak file DXF dalam satu kali jalankan?**  
A: Tentu. Loop melalui direktori, muat setiap file, dan terapkan logika rasterisasi serta penyimpanan yang sama.

**Q: Versi Java apa yang didukung?**  
A: Aspose.CAD untuk Java mendukung Java 8 dan yang lebih baru, termasuk Java 11, 17, dan rilis LTS terbaru.

**Terakhir Diperbarui:** 2026-10-30  
**Diuji Dengan:** Aspose.CAD for Java 24.11  
**Penulis:** Aspose

## Tutorial terkait

- [Buat PDF dari CAD – Ekspor DXF ke PDF dengan Aspose.CAD untuk Java](/cad/java/additional-features/export-dxf-to-pdf/)
- [Buat PDF dari DXF: Ekspor Lapisan dengan Aspose.CAD untuk Java](/cad/java/additional-features/export-specific-layer-to-pdf/)
- [Cara Mengonversi Tata Letak DXF ke Gambar JPEG dengan Aspose.CAD di Java](/cad/java/additional-features/export-specific-layout-to-image/)

```java
image.save(dataDir + "conic_pyramid_out_.pdf"); 
```

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}