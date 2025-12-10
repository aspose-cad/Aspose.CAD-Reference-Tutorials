---
date: 2025-12-10
description: Pelajari cara membuat PDF dari CAD menggunakan Aspose.CAD untuk Java
  dengan penyesuaian pena. Panduan langkah demi langkah ini menunjukkan cara mengekspor
  CAD ke PDF secara efisien.
linktitle: Pen Support in Export
second_title: Aspose.CAD Java API
title: Cara Membuat PDF dari CAD dengan Dukungan Pena saat Mengekspor
url: /id/java/advanced-cad-features/pen-support-in-export/
weight: 13
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Dukungan Pena dalam Ekspor

## Pendahuluan

Dalam dunia konversi CAD yang bergerak cepat, pengembang sering perlu **membuat PDF dari CAD** file sambil mempertahankan kesetiaan visual. Aspose.CAD untuk Java mempermudah hal ini, menawarkan opsi kaya seperti penyesuaian pena yang memungkinkan Anda menyesuaikan gaya garis selama proses ekspor. Dalam panduan ini kami akan membahas contoh lengkap, langkah‑demi‑langkah yang menunjukkan cara **mengekspor CAD ke PDF** dengan pengaturan pena khusus, sehingga Anda dapat menghasilkan PDF yang halus langsung dari gambar DXF.

## Jawaban Cepat
- **Apa arti “create PDF from CAD”?** Mengonversi gambar CAD (misalnya DXF) menjadi dokumen PDF sambil mempertahankan kualitas vektor.  
- **Perpustakaan mana yang menangani penyesuaian pena?** Kelas `PenOptions` milik Aspose.CAD untuk Java.  
- **Bisakah saya menggunakan ini untuk format lain?** Ya – pengaturan pena yang sama berlaku untuk PNG, BMP, TIFF, dll.  
- **Apakah saya memerlukan lisensi?** Lisensi Aspose.CAD yang valid diperlukan untuk penggunaan produksi.  
- **Versi Java minimum apa?** Java 8 atau lebih tinggi.

## Apa itu “create PDF from CAD”?
Membuat PDF dari CAD berarti meraster atau merender gambar CAD menjadi file PDF. Hal ini memudahkan berbagi, mencetak, dan mengarsipkan desain teknik tanpa memerlukan perangkat lunak CAD di sisi penerima.

## Mengapa menggunakan dukungan pena saat mengekspor CAD ke PDF?
Dukungan pena memungkinkan Anda mengontrol ujung garis, sambungan, dan ketebalan, memberi kemampuan untuk menyesuaikan standar merek perusahaan atau standar gambar teknik. Ini sangat berguna ketika rendering garis default tidak memenuhi kebutuhan visual Anda.

## Prasyarat

- **Lingkungan Pengembangan Java** – JDK yang berfungsi (8 atau lebih baru) serta IDE atau alat build pilihan Anda.  
- **Perpustakaan Aspose.CAD** – unduh JAR terbaru dari situs resmi [di sini](https://releases.aspose.com/cad/java/).  
- **File DXF contoh** – untuk tutorial ini kami akan menggunakan `conic_pyramid.dxf`.

Setelah semua persiapan selesai, mari kita selami kode.

## Impor Namespace

```java
import com.aspose.cad.Image;

import com.aspose.cad.fileformats.cad.CadImage;
import com.aspose.cad.imageoptions.CadRasterizationOptions;
import com.aspose.cad.imageoptions.PdfOptions;
import com.aspose.cad.imageoptions.PenOptions;
import com.aspose.cad.internal.imaging.LineCap;
```

## Langkah 1: Tentukan Direktori Dokumen Anda

```java
String dataDir = "Your Document Directory" + "CADConversion/";
```

> **Tip Pro:** Ganti `"Your Document Directory"` dengan jalur absolut tempat file DXF Anda berada.

## Langkah 2: Muat File CAD

```java
String srcFile = dataDir + "conic_pyramid.dxf";
CadImage cadImage = (CadImage) Image.load(srcFile);
```

Metode `Image.load` membaca file DXF dan membuat objek `CadImage` yang dapat kita manipulasi.

## Langkah 3: Konfigurasikan Opsi Rasterisasi

```java
CadRasterizationOptions rasterizationOptions = new CadRasterizationOptions();
rasterizationOptions.setPageWidth(cadImage.getWidth() * 100);
rasterizationOptions.setPageHeight(cadImage.getHeight() * 100);
```

Sesuaikan dimensi halaman untuk mengontrol resolusi PDF yang dihasilkan. Mengalikan dengan 100 memberikan output beresolusi tinggi yang cocok untuk pencetakan.

## Langkah 4: Sesuaikan Opsi Pena

```java
PenOptions penOts = new PenOptions();
penOts.setStartCap(LineCap.Flat);
penOts.setEndCap(LineCap.Flat);
```

Di sini kami mengatur kedua ujung pena, mulai dan akhir, menjadi `Flat`. Anda dapat bereksperimen dengan nilai `LineCap` lain (misalnya `Round`, `Square`) untuk menghasilkan efek visual yang berbeda.

## Langkah 5: Konfigurasikan Opsi Ekspor PDF

```java
PdfOptions pdfOptions = new PdfOptions();
pdfOptions.setVectorRasterizationOptions(rasterizationOptions);
```

Objek `PdfOptions` menghubungkan pengaturan rasterisasi dengan proses ekspor PDF.

## Langkah 6: Simpan PDF yang Diekspor

```java
cadImage.save((dataDir + "9LHATT-A56_generated.pdf"), pdfOptions);
```

Menjalankan baris ini menulis file PDF bernama `9LHATT-A56_generated.pdf` ke folder `dataDir` Anda, lengkap dengan gaya pena khusus yang telah Anda tentukan.

## Kasus Penggunaan Umum

- **Dokumentasi teknis** – menyisipkan gambar teknik yang tepat dalam manual PDF.  
- **Pelaporan otomatis** – menghasilkan PDF dari data CAD secara langsung dalam layanan web.  
- **Kontrol kualitas** – menerapkan ujung garis khusus untuk menyoroti garis pengukuran atau toleransi.

## Pemecahan Masalah & Tips

- **Path file tidak benar** – pastikan `dataDir` diakhiri dengan pemisah file (`/` atau `\\`).  
- **Lisensi hilang** – tanpa lisensi yang valid, perpustakaan berjalan dalam mode evaluasi, yang dapat menambahkan watermark.  
- **Gaya garis tak terduga** – periksa kembali bahwa `PenOptions` telah diatur sebelum memanggil `save`; jika tidak, nilai default yang akan digunakan.

## Pertanyaan yang Sering Diajukan

### Q1: Bisakah saya menyesuaikan opsi pena untuk format selain PDF?

A1: Ya, penyesuaian pena yang ditunjukkan dalam tutorial ini berlaku untuk berbagai format gambar, termasuk PDF, PNG, BMP, GIF, JPEG2000, JPEG, PSD, TIFF, dan WMF.

### Q2: Bagaimana cara menangani ujung mulai dan akhir yang berbeda untuk pena?

A2: Gunakan kelas `PenOptions` untuk mengatur ujung mulai dan akhir yang diinginkan, memberikan fleksibilitas dalam mendefinisikan tampilan garis.

### Q3: Bagaimana jika saya tidak menentukan opsi pena?

A3: Jika opsi pena tidak secara eksplisit diatur, sistem akan menggunakan pena defaultnya, yang dapat berbeda dalam konteks yang berbeda.

### Q4: Apakah ada pertimbangan khusus untuk opsi rasterisasi?

A4: Sesuaikan lebar dan tinggi halaman dalam opsi rasterisasi untuk mengontrol dimensi gambar yang diekspor.

### Q5: Di mana saya dapat menemukan dukungan tambahan atau diskusi komunitas?

A5: Jelajahi forum komunitas Aspose.CAD di [sini](https://forum.aspose.com/c/cad/19) untuk dukungan dan diskusi.

---

**Terakhir Diperbarui:** 2025-12-10  
**Diuji Dengan:** Aspose.CAD 24.11 untuk Java  
**Penulis:** Aspose  

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}