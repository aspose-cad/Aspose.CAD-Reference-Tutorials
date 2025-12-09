---
date: 2025-12-09
description: Pelajari cara membuat PDF dari file DWG menggunakan Aspose.CAD untuk
  Java. Konversi DWG ke PDF dengan mudah menggunakan dukungan mesh.
linktitle: Mesh Support in CAD
second_title: Aspose.CAD Java API
title: Buat PDF dari DWG dengan Aspose.CAD untuk Java
url: /id/java/advanced-cad-features/mesh-support-in-cad/
weight: 12
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Buat PDF dari DWG dengan Aspose.CAD untuk Java

## Pendahuluan

Dalam tutorial ini Anda akan belajar **cara membuat PDF dari DWG** menggunakan Aspose.CAD untuk Java. Dukungan mesh pada perpustakaan memungkinkan Anda mengonversi gambar CAD yang kompleks—termasuk yang berisi mesh 3‑D—langsung ke PDF tanpa kehilangan detail. Baik Anda perlu **mengonversi DWG ke PDF** untuk pelaporan, pengarsipan, atau pemrosesan lanjutan, langkah‑langkah di bawah ini akan memandu Anda melalui solusi yang andal dan siap produksi.

## Jawaban Cepat
- **Apa yang dibahas dalam tutorial ini?** Mengonversi file DWG yang berisi mesh menjadi PDF menggunakan Aspose.CAD untuk Java.  
- **Apakah saya memerlukan lisensi?** Lisensi sementara dapat digunakan untuk pengujian; lisensi penuh diperlukan untuk penggunaan komersial.  
- **Versi Java mana yang didukung?** Java 8 atau yang lebih baru.  
- **Apakah saya dapat mengekspor format lain?** Ya – Aspose.CAD juga mendukung PNG, JPEG, BMP, dan lainnya.  
- **Berapa lama proses konversi?** Biasanya kurang dari satu detik untuk gambar berukuran standar.

## Cara membuat PDF dari DWG?

Di bawah ini Anda akan menemukan panduan singkat langkah‑demi‑langkah yang membawa Anda melalui seluruh proses—dari menyiapkan proyek hingga menyimpan PDF akhir.

## Prasyarat

- **Lingkungan Pengembangan Java:** JDK 8 atau yang lebih baru terpasang di mesin Anda.  
- **Pustaka Aspose.CAD untuk Java:** Unduh JAR terbaru dari [tautan unduhan](https://releases.aspose.com/cad/java/).  
- **Dokumen dengan Mesh:** File DWG yang berisi data mesh (mis., `meshes.dwg`).  

## Impor Namespace

In your Java source file, include the required Aspose.CAD classes:

```java
import com.aspose.cad.Image;

import com.aspose.cad.fileformats.cad.CadImage;
import com.aspose.cad.imageoptions.CadRasterizationOptions;
import com.aspose.cad.imageoptions.PdfOptions;
```

## Langkah 1: Siapkan Proyek

Buat proyek Java baru (atau tambahkan ke proyek yang sudah ada) dan tambahkan JAR Aspose.CAD ke classpath proyek. Tentukan direktori dasar yang akan menyimpan DWG sumber Anda dan PDF yang dihasilkan.

## Langkah 2: Tentukan Jalur File

Specify where the input DWG lives and where the output PDF should be written.

```java
String dataDir = "Your Document Directory" + "CADConversion/";
String sourceFilePath = dataDir + "meshes.dwg";
String outPath = dataDir + "meshes.pdf";
```

## Langkah 3: Muat Gambar CAD

Load the DWG file into a `CadImage` object so that Aspose.CAD can work with its internal structure.

```java
CadImage cadImage = (CadImage)Image.load(sourceFilePath);
```

## Langkah 4: Konfigurasikan Opsi Rasterisasi

Set the rasterization options that control the size and layout of the generated PDF pages. The `Layouts` array tells Aspose.CAD to render the **Model** space, which includes mesh entities.

```java
CadRasterizationOptions rasterizationOptions = new CadRasterizationOptions();
rasterizationOptions.setPageWidth(1600);
rasterizationOptions.setPageHeight(1600);
rasterizationOptions.setLayouts(new String[] { "Model" });
```

## Langkah 5: Atur Opsi PDF

Attach the rasterization settings to a `PdfOptions` instance. This tells the library to use the previously defined options when producing the PDF.

```java
PdfOptions pdfOptions = new PdfOptions();
pdfOptions.setVectorRasterizationOptions(rasterizationOptions);
```

## Langkah 6: Simpan PDF

Finally, save the loaded CAD image as a PDF file. The resulting document will contain a faithful representation of the original DWG, including any mesh geometry.

```java
cadImage.save(outPath, pdfOptions);
```

### Mengapa ini berhasil untuk **mengonversi CAD ke PDF**

Aspose.CAD melakukan rasterisasi berbasis vektor, mempertahankan ketebalan garis, warna, dan detail mesh 3‑D. Dengan mengonfigurasi opsi rasterisasi, Anda mengendalikan resolusi dan tata letak, memastikan bahwa **ekspor gambar CAD** terlihat persis seperti yang diharapkan dalam PDF.

## Kasus Penggunaan Umum

- **Pelaporan otomatis:** Menghasilkan laporan PDF dari gambar teknik secara langsung.  
- **Pengarsipan dokumen:** Menyimpan gambar CAD sebagai PDF untuk preservasi jangka panjang  
- **Layanan web:** Menyediakan API yang menerima unggahan DWG dan mengembalikan PDF, berguna untuk platform SaaS.  

## Tips Pemecahan Masalah

- **Mesh tidak muncul di output:** Pastikan properti `Layouts` mencakup `"Model"`; mesh biasanya disimpan di ruang model.  
- **Skala tidak tepat:** Sesuaikan `PageWidth` dan `PageHeight` agar cocok dengan satuan asli gambar.  
- **Kesalahan lisensi:** Pastikan Anda telah memanggil `License.setLicense()` dengan file lisensi yang valid sebelum memuat gambar.  

## Kesimpulan

Dengan mengikuti langkah‑langkah ini Anda dapat dengan andal **mengonversi DWG ke PDF** dan memanfaatkan sepenuhnya dukungan mesh Aspose.CAD. Kemampuan ini menyederhanakan alur kerja yang memerlukan ekspor PDF berkualitas tinggi dari gambar CAD yang kompleks, baik untuk penggunaan internal maupun dokumentasi yang ditujukan kepada klien.

## FAQ

### Q1: Apakah Aspose.CAD untuk Java cocok untuk penggunaan komersial?

A1: Ya, Aspose.CAD untuk Java dirancang untuk penggunaan pribadi maupun komersial. Anda dapat menemukan detail lisensi di [halaman pembelian](https://purchase.aspose.com/buy).

### Q2: Bagaimana saya dapat memperoleh lisensi sementara untuk tujuan pengujian?

A2: Dapatkan lisensi sementara dari [sini](https://purchase.aspose.com/temporary-license/) untuk pengujian dan evaluasi.

### Q3: Di mana saya dapat menemukan dukungan komunitas untuk Aspose.CAD untuk Java?

A3: Kunjungi forum khusus Aspose.CAD di [https://forum.aspose.com/c/cad/19](https://forum.aspose.com/c/cad/19) untuk dukungan komunitas.

### Q4: Apakah ada format output lain yang didukung selain PDF?

A4: Ya, Aspose.CAD untuk Java mendukung berbagai format output, termasuk PNG, JPEG, BMP, dan lainnya. Lihat dokumentasi untuk detail.

### Q5: Bisakah saya mencoba Aspose.CAD untuk Java secara gratis?

A5: Ya, Anda dapat menjelajahi versi percobaan gratis Aspose.CAD untuk Java [di sini](https://releases.aspose.com/).

---

**Last Updated:** 2025-12-09  
**Tested With:** Aspose.CAD for Java 24.11  
**Author:** Aspose  

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}