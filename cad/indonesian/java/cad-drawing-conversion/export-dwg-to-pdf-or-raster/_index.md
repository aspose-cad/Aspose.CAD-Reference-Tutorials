---
date: 2026-02-17
description: Pelajari bagaimana perpustakaan CAD Java Aspose.CAD for Java dapat mengekspor
  DWG ke PDF atau gambar raster dengan cepat dan akurat.
linktitle: Export DWG to PDF or Raster
second_title: Aspose.CAD Java API
title: Ekspor DWG ke PDF atau Raster Menggunakan perpustakaan CAD Java Aspose.CAD
  untuk Java
url: /id/java/cad-drawing-conversion/export-dwg-to-pdf-or-raster/
weight: 13
---

versi gambar raster dwg dengan pustaka java cad"

Paragraph.

How to generate pdf dwg using pdf options cad => "Cara menghasilkan pdf dwg menggunakan pdf options cad"

Paragraph.

Common Issues & Tips => "Masalah Umum & Tips"

Bullet points translate.

Frequently Asked Questions heading.

Each Q/A translate.

Conclusion paragraph.

Footer lines.

Make sure to keep code block placeholders unchanged.

Also keep shortcodes unchanged.

Let's craft final output.{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Ekspor DWG ke PDF atau Raster Menggunakan pustaka java cad Aspose.CAD untuk Java

## Introduction

Di dunia desain berbantuan komputer (CAD) yang dinamis, penanganan gambar secara efisien sangat penting. Dengan **java cad library** **Aspose.CAD for Java** Anda dapat **export dwg to pdf** — atau gambar raster — hanya dengan beberapa baris kode. Tutorial ini memandu Anda melalui seluruh proses, mulai dari memuat file DWG hingga menghasilkan PDF berkualitas tinggi, sambil menyoroti mengapa Aspose.CAD Java menjadi pustaka pilihan utama untuk tugas konversi CAD.

## Quick Answers
- **Apa yang dibahas dalam tutorial ini?** Mengekspor file DWG ke PDF atau gambar raster menggunakan Aspose.CAD for Java.  
- **Apakah saya memerlukan lisensi?** Lisensi sementara gratis tersedia untuk evaluasi; lisensi penuh diperlukan untuk produksi.  
- **Versi Java mana yang didukung?** Semua runtime Java 8+ dapat bekerja dengan API Aspose.CAD Java terbaru.  
- **Apakah saya dapat mengonversi DWG ke format gambar lain?** Ya – opsi rasterisasi yang sama memungkinkan Anda menghasilkan PNG, JPEG, BMP, dll.  
- **Berapa lama proses konversi berlangsung?** Biasanya kurang dari satu detik untuk gambar standar; file yang lebih besar mungkin memerlukan beberapa detik.

## Mengapa pustaka java cad adalah pilihan terbaik untuk konversi DWG?

- **Implementasi murni Java** – tanpa DLL native atau alat eksternal.  
- **Penanganan satuan yang akurat** – satuan metrik dan imperial terdeteksi secara otomatis.  
- **Output raster berkualitas tinggi** – DPI dan kontrol ukuran halaman yang disetel halus.  
- **Dukungan PDF penuh** – pembuatan PDF yang mempertahankan vektor tanpa ketergantungan tambahan.  
- **Lisensi fleksibel** – mulai dengan **temporary license aspose** untuk pengujian, kemudian tingkatkan saat produksi.

## Apa itu “export dwg to pdf”?

Mengekspor DWG ke PDF berarti mengonversi gambar AutoCAD asli menjadi dokumen PDF yang portabel dan independen dari perangkat. PDF yang dihasilkan mempertahankan data vektor, lapisan, dan skala, menjadikannya ideal untuk berbagi, mencetak, atau mengarsipkan.

## Mengapa menggunakan Aspose.CAD Java untuk konversi ini?

Karena **java cad library** menangani semua hal mulai dari konversi satuan hingga rasterisasi secara internal, Anda menghindari kerumitan alat pihak ketiga dan mendapatkan hasil yang konsisten di semua platform.

## Prerequisites

Sebelum masuk ke kode, pastikan Anda memiliki:

- Pengetahuan dasar pemrograman Java.  
- Pustaka Aspose.CAD for Java terpasang. Jika belum mengunduhnya, dapatkan **[di sini](https://releases.aspose.com/cad/java/)**.  
- File DWG untuk pengujian – contoh **Bottom_plate.dwg** digunakan dalam panduan ini.

## Import Namespaces

Di proyek Java Anda, impor kelas yang diperlukan untuk memulai konversi:

```java
import com.aspose.cad.Image;

import com.aspose.cad.imageoptions.CadRasterizationOptions;
import com.aspose.cad.imageoptions.PdfOptions;
import com.aspose.cad.imageoptions.UnitType;
```

## Step‑by‑Step Guide

### Step 1: Load the DWG File

Langkah pertama, muat gambar DWG Anda menggunakan kelas `Image`. Ini membuat representasi dalam memori yang dapat diproses oleh Aspose.CAD.

```java
String dataDir = "Your Document Directory" + "DWGDrawings/";
String srcFile = dataDir + "Bottom_plate.dwg";
Image objImage = Image.load(srcFile);
```

### Step 2: Determine Unit Type

Memahami apakah gambar menggunakan satuan metrik atau imperial penting untuk skala yang tepat. Metode bantu `IsMetric` (implementasi dihilangkan untuk singkat) mengembalikan nilai boolean.

```java
Boolean currentUnitIsMetric = IsMetric(objImage.getUnitType());
int currentUnitCoefficient = objImage.getUnitType();
```

### Step 3: Set Rasterization Options

Berdasarkan sistem satuan, konfigurasikan ukuran halaman, skala, dan jenis satuan target. Opsi‑opsi ini menentukan bagaimana DWG dirasterisasi sebelum dibungkus ke dalam PDF.

```java
CadRasterizationOptions rasterizationOptions = new CadRasterizationOptions();

if (currentUnitIsMetric) {
    // Metric units
    double metersCoeff = 1 / 1000.0;
    double scaleFactor = metersCoeff / currentUnitCoefficient;
    rasterizationOptions.setPageWidth((float)(210 * scaleFactor));
    rasterizationOptions.setPageHeight((float)(297 * scaleFactor));
    rasterizationOptions.setUnitType(UnitType.Millimeter);
} else {
    // Imperial units
    rasterizationOptions.setPageWidth((float)(8.27f / currentUnitCoefficient));
    rasterizationOptions.setPageHeight((float)(11.69f / currentUnitCoefficient));
    rasterizationOptions.setUnitType(UnitType.Inch);
}
```

### Step 4: Configure PDF Options (pdf options cad)

Buat instance `PdfOptions` dan lampirkan pengaturan rasterisasi. Ini memberi tahu Aspose.CAD cara menyematkan konten raster ke PDF akhir.

```java
PdfOptions pdfOptions = new PdfOptions();
pdfOptions.setVectorRasterizationOptions(new CadRasterizationOptions());
```

### Step 5: Save as PDF

Akhirnya, ekspor gambar ke file PDF. Metode `save` menerima jalur output dan `PdfOptions` yang telah dikonfigurasi.

```java
objImage.save(dataDir + "Saved.pdf", pdfOptions);
```

Setelah kode selesai dijalankan, Anda akan menemukan **Saved.pdf** di folder `DWGDrawings` Anda, siap untuk distribusi atau pengarsipan.

## Cara mengonversi gambar raster dwg dengan pustaka java cad

Jika Anda memerlukan gambar raster alih‑alih PDF, cukup ganti `PdfOptions` dengan opsi gambar raster yang sesuai (misalnya, `PngOptions`, `JpegOptions`). Instance `CadRasterizationOptions` yang sama dapat dipakai kembali, memungkinkan Anda **convert dwg raster** dengan perubahan kode yang minimal.

## Cara menghasilkan pdf dwg menggunakan pdf options cad

Contoh di atas sudah **generates pdf dwg**. Dengan menyesuaikan `pdfOptions`—misalnya, menetapkan `pdfOptions.setCompress(true)`—Anda dapat mengontrol ukuran dan kualitas PDF. Ini menunjukkan fleksibilitas API **pdf options cad**.

## Masalah Umum & Tips

- **Ukuran halaman tidak tepat** – Periksa kembali logika konversi satuan; koefisien yang tidak cocok dapat menghasilkan halaman terlalu besar.  
- **Font atau lineweight hilang** – Pastikan DWG merujuk ke semua sumber eksternal sebelum konversi.  
- **Kinerja pada gambar besar** – Tingkatkan pengaturan `DPI` di `CadRasterizationOptions` hanya bila kualitas lebih tinggi diperlukan; DPI lebih rendah mempercepat proses.  
- **Masalah lisensi** – Untuk evaluasi Anda dapat menggunakan **temporary license aspose**; lisensi penuh diperlukan untuk penggunaan produksi.

## Frequently Asked Questions

**T: Apakah saya dapat menggunakan Aspose.CAD untuk Java dengan kerangka kerja Java lainnya?**  
J: Ya, Aspose.CAD untuk Java dapat terintegrasi mulus dengan kerangka kerja populer seperti Spring, Jakarta EE, dan Android.

**T: Apakah lisensi sementara tersedia untuk Aspose.CAD untuk Java?**  
J: Ya, Anda dapat memperoleh lisensi sementara **[di sini](https://purchase.aspose.com/temporary-license/)**.

**T: Di mana saya dapat menemukan dukungan untuk Aspose.CAD untuk Java?**  
J: Kunjungi **[forum Aspose.CAD](https://forum.aspose.com/c/cad/19)** untuk bantuan dari komunitas dan insinyur Aspose.

**T: Bagaimana cara membeli lisensi untuk Aspose.CAD untuk Java?**  
J: Anda dapat membeli lisensi **[di sini](https://purchase.aspose.com/buy)**.

**T: Unit apa saja yang didukung oleh Aspose.CAD untuk Java?**  
J: Aspose.CAD untuk Java mendukung baik unit metrik maupun imperial, secara otomatis mendeteksi sistem satuan gambar.

**T: Bisakah saya mengonversi DWG ke format gambar lain (misalnya PNG, JPEG) menggunakan API yang sama?**  
J: Tentu saja. Ganti `PdfOptions` dengan opsi gambar raster yang sesuai (misalnya, `PngOptions`) dan gunakan kembali `CadRasterizationOptions` yang sama.

## Conclusion

Tutorial ini menunjukkan cara **export dwg to pdf** dan gambar raster menggunakan **java cad library** Aspose.CAD untuk Java. Dengan mengikuti panduan langkah‑demi‑langkah, Anda dapat mengintegrasikan konversi CAD yang handal ke dalam aplikasi Java apa pun, baik untuk PDF dokumentasi maupun gambar raster untuk tampilan web.

---

**Last Updated:** 2026-02-17  
**Tested With:** Aspose.CAD for Java 24.10  
**Author:** Aspose  

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}