---
date: 2026-11-18
description: Pelajari cara mengekspor DWG ke PDF, mengaktifkan pelacakan, dan menggunakan
  kelas penanganan kesalahan khusus Java dengan Aspose.CAD untuk Java. Termasuk konversi
  DXF‑ke‑PDF.
keywords:
- export dwg to pdf
- custom error handler java
- dwg to pdf java
lastmod: 2026-11-18
linktitle: Aktifkan Pelacakan pada File DWG Menggunakan Java
og_description: Ekspor DWG ke PDF dan aktifkan pelacakan penuh di Java dengan Aspose.CAD.
  Pelajari cara menggunakan penanganan kesalahan khusus, mengonversi DXF ke PDF, dan
  mencatat peringatan render.
og_image_alt: Guide showing DWG to PDF conversion and tracking in Java with Aspose.CAD
og_title: Ekspor DWG ke PDF dengan pelacakan menggunakan Aspose.CAD untuk Java
schemas:
- author: Aspose
  dateModified: '2026-11-18'
  description: Learn how to export DWG to PDF, enable tracking, and use a custom error
    handler Java class with Aspose.CAD for Java. Includes DXF‑to‑PDF conversion.
  headline: Export DWG to PDF and Enable Tracking with Aspose.CAD Java
  type: TechArticle
- questions:
  - answer: It activates Aspose.CAD’s render callbacks so you can see warnings and
      errors during export.
    question: What does “enable dwg tracking java” do?
  - answer: A trial works for testing; a commercial license is required for production
      use.
    question: Do I need a license?
  - answer: Yes – the same `PdfOptions` object used for DWG works for DXF, covering
      the *java convert dxf pdf* scenario.
    question: Can I also convert DXF to PDF?
  - answer: Java 8 or higher.
    question: Which JDK version is required?
  - answer: See the [Aspose.CAD Java Documentation](https://reference.aspose.com/cad/java/)
      linked below.
    question: Where can I find more examples?
  type: FAQPage
second_title: Aspose.CAD Java API
tags:
- export dwg to pdf
- aspose.cad java
- custom error handler
- dxf to pdf
- java cad conversion
title: Ekspor DWG ke PDF dan Aktifkan Pelacakan dengan Aspose.CAD Java
url: /id/java/additional-features/enable-tracking/
weight: 12
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Ekspor DWG ke PDF dan aktifkan pelacakan dengan Aspose.CAD Java

## Pendahuluan

Mengekspor DWG ke PDF sambil mempertahankan visibilitas penuh terhadap proses konversi sangat penting bagi tim yang berfokus pada CAD modern. Dalam panduan ini Anda akan menemukan **cara mengaktifkan pelacakan** dalam alur kerja DWG, mengonversi DXF ke PDF dalam pipeline yang sama, dan menangkap setiap peringatan rendering dengan kelas **custom error handler Java**. Pada akhirnya Anda akan memiliki potongan kode siap produksi yang tidak hanya menghasilkan PDF berkualitas tinggi tetapi juga mencatat informasi diagnostik untuk audit dan pemecahan masalah.

## Jawaban Cepat
- **Apa yang dilakukan “enable dwg tracking java”?** Itu mengaktifkan callback render Aspose.CAD sehingga Anda dapat melihat peringatan dan kesalahan selama ekspor.  
- **Apakah saya memerlukan lisensi?** Versi percobaan dapat digunakan untuk pengujian; lisensi komersial diperlukan untuk penggunaan produksi.  
- **Bisakah saya juga mengonversi DXF ke PDF?** Ya – objek `PdfOptions` yang sama digunakan untuk DWG juga berfungsi untuk DXF, mencakup skenario *java convert dxf pdf*.  
- **Versi JDK mana yang diperlukan?** Java 8 atau lebih tinggi.  
- **Di mana saya dapat menemukan contoh lebih banyak?** Lihat [Dokumentasi Aspose.CAD Java](https://reference.aspose.com/cad/java/) yang terhubung di bawah.  

## Apa itu ekspor dwg ke pdf?

Export DWG to PDF adalah proses mengonversi gambar AutoCAD asli (DWG) menjadi dokumen PDF portabel sambil mempertahankan fidelitas vektor, lapisan, dan anotasi. **Aspose.CAD mengonversi DWG ke PDF dalam Java murni, sehingga Anda tidak pernah memerlukan instalasi AutoCAD berlisensi.** Konversi ini mempertahankan ketebalan garis yang tepat, gaya teks, dan geometri tata letak, menjadikan PDF cocok untuk peninjauan klien, arsip, atau pemrosesan lanjutan.

## Mengapa menggunakan Aspose.CAD untuk Java?

Aspose.CAD untuk Java menyediakan solusi Java murni yang komprehensif untuk konversi CAD, mendukung lebih dari 50 format, menawarkan kinerja tinggi, dan menyediakan pelacakan bawaan melalui callback render. Tidak memerlukan dependensi eksternal dan dapat diintegrasikan ke dalam pipeline sisi server. Perpustakaan ini juga mencakup pemrosesan efisien memori, memungkinkan konversi file hingga 500 halaman tanpa harus memuat seluruh dokumen ke RAM.

## Prasyarat

- **Java Development Kit (JDK)** 8 atau yang lebih baru terpasang di mesin Anda.  
- **Aspose.CAD untuk Java** diunduh dari [tautan unduhan](https://releases.aspose.com/cad/java/) resmi.  
- **Aspose.CAD Free Trial** dapat diperoleh dari halaman [Aspose.CAD Free Trial](https://releases.aspose.com/) jika Anda memerlukan evaluasi cepat.  
- Folder yang berisi file DWG/DXF yang ingin Anda konversi.  

## Cara mengekspor DWG ke PDF?

Muat file sumber Anda, konfigurasikan `PdfOptions`, lampirkan `CadRenderHandler` khusus, dan panggil `save`. Alur end‑to‑end ini mengonversi DWG (atau DXF) ke PDF sambil menghasilkan informasi pelacakan untuk setiap langkah rendering, memastikan bahwa semua peringatan atau kesalahan ditangkap dan dapat ditindaklanjuti oleh pengembang atau proses otomatis.

## Impor namespace

Antarmuka `CadRenderHandler` menerima diagnostik rendering seperti peringatan dan kesalahan selama konversi.  
```java
import com.aspose.cad.Image;

import com.aspose.cad.imageoptions.CadRasterizationOptions;
import com.aspose.cad.imageoptions.CadRenderResult;
import com.aspose.cad.imageoptions.PdfOptions;
import com.aspose.cad.imageoptions.RenderResult;
import java.io.FileNotFoundException;
import java.io.FileOutputStream;
import java.io.OutputStream;
```

## Langkah 1: muat file dwg/dxf  

`CadImage` mewakili gambar CAD yang dimuat ke memori dan menyediakan akses ke halaman serta lapisannya.  
```java
String dataDir = "Your Document Directory" + "DXFDrawings/";
Image image = Image.load(dataDir + "conic_pyramid.dxf");
```

## Langkah 2: konfigurasikan opsi ekspor pdf (cara mengonversi dxf ke pdf)

`PdfOptions` mendefinisikan pengaturan output PDF, sementara `VectorRasterizationOptions` mengontrol parameter rasterisasi seperti DPI dan warna latar belakang.  
```java
OutputStream stream = new FileOutputStream(dataDir + "output_conic_pyramid.pdf");
PdfOptions pdfOptions = new PdfOptions();
CadRasterizationOptions cadRasterizationOptions = new CadRasterizationOptions();
pdfOptions.setVectorRasterizationOptions(cadRasterizationOptions);
cadRasterizationOptions.setPageWidth(800);
cadRasterizationOptions.setPageHeight(600);
```

## Langkah 3: implementasikan pelacakan (custom error handler java)

`ErrorHandler` memperluas `CadRenderHandler` untuk menangkap dan mencatat pesan render yang dihasilkan selama proses konversi.  
```java
cadRasterizationOptions.RenderResult = new ErrorHandler();
```

## Langkah 4: ekspor ke pdf  

Memanggil metode `save` pada instance `CadImage` menulis PDF yang dirender ke jalur output yang ditentukan.  
```java
System.out.println("Exporting to pdf format");
image.save(stream, pdfOptions);
```

## Langkah 5: kelas cadrenderhandler  

`CadRenderHandler` adalah kelas callback dasar yang menerima `RenderResult` berisi pesan terperinci setelah rendering selesai.  
```java
public static class ErrorHandler extends CadRasterizationOptions.CadRenderHandler {
    @Override
    public void invoke(CadRenderResult result) {
        System.out.println("Tracking results of exporting");

        if (result.isRenderComplete())
            return;

        System.out.println("Have some problems:");

        int idxError = 1;
        for (RenderResult rr : result.getFailures()) {
            System.out.printf("{0}. {1}, {2}", idxError, rr.getRenderCode(), rr.getMessage());
            idxError++;
        }
    }
}
```

## Mengapa ini penting

Mengaktifkan pelacakan menciptakan jejak audit yang memenuhi persyaratan kepatuhan di sektor yang diatur seperti arsitektur, teknik, dan konstruksi. Custom error handler juga memungkinkan Anda mengintegrasikan pemeriksaan kesehatan konversi CAD ke dalam pipeline CI/CD, secara otomatis menandai file yang memerlukan peninjauan manual.

## Masalah umum dan solusi

- **`NullPointerException` pada `RenderResult`** – Pastikan Anda menggunakan Aspose.CAD 23.10 atau yang lebih baru; rilis sebelumnya tidak memiliki API `RenderResult`.  
- **File tidak ditemukan** – Periksa kembali bahwa `dataDir` mengarah ke folder yang tepat dan nama file cocok dengan sensitivitas huruf.  
- **Output pelacakan hilang** – Pastikan instance `ErrorHandler` Anda telah ditetapkan dengan benar ke `cadRasterizationOptions.setRenderHandler(new ErrorHandler())`.  

## Pertanyaan yang sering diajukan

**Q:** Bisakah saya mengaktifkan pelacakan untuk format file CAD lain menggunakan Aspose.CAD untuk Java?  
**A:** Pelacakan terutama tersedia untuk DWG dan DXF. Untuk format lain, konsultasikan dokumentasi resmi untuk melihat API mana yang menyediakan callback render.

**Q:** Bagaimana saya dapat menyesuaikan opsi ekspor tambahan, seperti mengatur metadata PDF?  
**A:** `PdfOptions` menyediakan properti seperti `setTitle`, `setAuthor`, dan `setSubject`. Atur ini sebelum memanggil `save` untuk menyematkan metadata dalam PDF yang dihasilkan.

**Q:** Apakah versi percobaan cukup untuk mengevaluasi fitur pelacakan?  
**A:** Ya, versi percobaan gratis mencakup akses penuh ke API, memungkinkan Anda menguji `CadRenderHandler` dan ekspor PDF tanpa batasan.

**Q:** Di mana saya dapat mendapatkan dukungan komunitas untuk Aspose.CAD untuk Java?  
**A:** Kunjungi [forum Aspose.CAD](https://forum.aspose.com/c/cad/19) untuk mengajukan pertanyaan dan berbagi pengalaman dengan pengembang lain.

**Q:** Bagaimana cara mendapatkan lisensi sementara untuk lingkungan pengujian otomatis?  
**A:** Ikuti langkah-langkah di [Lisensi Sementara](https://purchase.aspose.com/temporary-license/) untuk menghasilkan file lisensi dengan batas waktu.

## Kesimpulan

Dengan mengikuti tutorial ini Anda kini mengetahui cara **mengekspor DWG ke PDF**, mengaktifkan pelacakan full‑stack, dan menangani konversi DXF‑ke‑PDF dengan kelas **custom error handler Java**. Gabungkan potongan kode ini ke dalam pipeline build Anda untuk memperoleh visibilitas, meningkatkan keandalan, dan memenuhi kepatuhan tingkat industri untuk pemrosesan dokumen CAD.

---

**Last Updated:** 2026-11-18  
**Tested With:** Aspose.CAD for Java 24.12  
**Author:** Aspose  

## Tutorial terkait

- [Ekspor DWG ke PDF dan Konversi Gambar CAD – Tutorial Aspose.CAD Java](/cad/java/cad-drawing-conversion/)
- [Ekspor DWG ke PDF atau Raster Menggunakan Aspose.CAD untuk Java](/cad/java/cad-drawing-conversion/export-dwg-to-pdf-or-raster/)
- [Ekspor Layout DWG Spesifik ke PDF Menggunakan Aspose.CAD untuk Java](/cad/java/cad-drawing-conversion/export-specific-dwg-layout-to-pdf/)

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}