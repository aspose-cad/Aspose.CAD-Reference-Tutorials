---
date: 2026-02-12
description: Pelajari cara mengatur ukuran halaman PDF saat mengonversi CAD ke PDF
  menggunakan Aspose.CAD untuk Java. Ikuti panduan langkah demi langkah ini untuk
  mengaktifkan pelacakan, mengonversi CAD ke PDF, dan menyimpan CAD sebagai PDF secara
  efisien.
linktitle: Set PDF Page Size – Enable Tracking for CAD Rendering
second_title: Aspose.CAD Java API
title: Cara Mengatur Ukuran Halaman PDF dan Mengaktifkan Pelacakan untuk Proses Rendering
  CAD
url: /id/java/advanced-cad-features/enable-tracking-for-cad-rendering-process/
weight: 10
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Aktifkan Pelacakan untuk Proses Rendering CAD

## Pendahuluan

Dalam tutorial ini Anda akan belajar cara **mengatur ukuran halaman PDF** saat **mengonversi CAD ke PDF** menggunakan **Aspose.CAD for Java**. Dengan mengaktifkan pelacakan Anda mendapatkan visibilitas penuh atas pipeline rendering, sehingga lebih mudah untuk men-debug dan mengoptimalkan konversi dari file CAD (seperti DXF) ke PDF. Baik Anda perlu **menyimpan CAD sebagai PDF**, menghasilkan PDF dari DXF, atau sekadar mengontrol dimensi output, langkah‑langkah di bawah ini akan memandu Anda melalui seluruh proses.

## Jawaban Cepat
- **Apa yang dilakukan “set PDF page size”?** Ini mendefinisikan lebar dan tinggi halaman PDF yang dihasilkan selama rendering CAD.  
- **Mengapa mengaktifkan pelacakan?** Pelacakan mencatat setiap tahap konversi, membantu Anda menemukan bottleneck kinerja atau kesalahan.  
- **Apakah saya memerlukan lisensi?** Trial gratis cukup untuk evaluasi; lisensi komersial diperlukan untuk produksi.  
- **Format CAD apa yang didukung?** DWG, DXF, DGN, dan banyak lainnya – lihat dokumentasi Aspose.CAD untuk daftar lengkap.  
- **Bisakah saya mengubah dimensi halaman secara dinamis?** Ya – cukup sesuaikan nilai `PageWidth` dan `PageHeight` di `CadRasterizationOptions`.

## Apa itu “set PDF page size” dalam rendering CAD?

Mengatur ukuran halaman PDF memberi tahu rasterizer seberapa besar kanvas yang harus dibuat ketika data CAD vektor dirasterkan menjadi halaman PDF. Ini penting untuk mempertahankan fidelitas visual, terutama saat menangani gambar teknik yang detail.

## Mengapa mengaktifkan pelacakan untuk rendering CAD?

Mengaktifkan pelacakan menyediakan log terperinci dari setiap langkah—dari memuat file sumber hingga menulis output PDF. Ini membantu Anda:

- Mendiagnosa mengapa gambar tertentu mungkin dirender secara tidak tepat.  
- Mengukur waktu yang dibutuhkan untuk setiap tahap, berguna untuk penyetelan kinerja.  
- Memverifikasi bahwa ukuran halaman yang Anda konfigurasikan memang diterapkan.

## Prasyarat

Sebelum masuk ke pengaturan pelacakan, pastikan Anda memiliki prasyarat berikut:

1. **Lingkungan Pengembangan Java** – Java 8 atau lebih baru terpasang di mesin Anda.  
2. **Pustaka Aspose.CAD** – Unduh dan integrasikan pustaka Aspose.CAD ke dalam proyek Java Anda. Anda dapat menemukan tautan unduhan [di sini](https://releases.aspose.com/cad/java/).  
3. **Direktori Dokumen** – Siapkan sebuah direktori untuk menyimpan file CAD Anda serta PDF yang dihasilkan.

## Impor Namespace

Di proyek Java Anda, impor namespace yang diperlukan untuk memanfaatkan fungsionalitas Aspose.CAD. Tambahkan baris berikut di awal kode Anda:

```java
import java.io.FileNotFoundException;
import java.io.FileOutputStream;
import java.io.OutputStream;

import com.aspose.cad.Image;

import com.aspose.cad.imageoptions.CadRasterizationOptions;
import com.aspose.cad.imageoptions.PdfOptions;
```

## Atur Jalur Direktori Sumber Daya

```java
String dataDir = "Your Document Directory" + "CADConversion/";
```

Ganti `"Your Document Directory"` dengan jalur sebenarnya ke direktori dokumen Anda.

## Muat File CAD

```java
String srcFile = dataDir + "conic_pyramid.dxf";
Image image = Image.load(srcFile);
```

Tentukan jalur ke file CAD Anda, pastikan berada dalam direktori dokumen yang telah ditetapkan.

## Atur Opsi Output PDF

```java
OutputStream stream = new FileOutputStream(dataDir + "conic_pyramid.pdf");
PdfOptions pdfOptions = new PdfOptions();
```

Buat aliran output dan atur opsi PDF untuk konversi.

## Konfigurasikan CadRasterizationOptions (Set PDF Page Size)

```java
CadRasterizationOptions cadRasterizationOptions = new CadRasterizationOptions();
pdfOptions.setVectorRasterizationOptions(cadRasterizationOptions);
cadRasterizationOptions.setPageWidth(800);
cadRasterizationOptions.setPageHeight(600);
```

Di sini kami **mengatur ukuran halaman PDF** dengan mendefinisikan `PageWidth` dan `PageHeight`. Sesuaikan nilai‑nilai ini agar cocok dengan dimensi yang dibutuhkan untuk gambar teknik Anda. Ini adalah langkah inti yang menjawab **bagaimana mengatur ukuran PDF** ketika Anda **java cad to pdf**.

## Simpan File PDF

```java
image.save(stream, pdfOptions);
```

Simpan file PDF yang telah dirender dengan opsi yang telah ditentukan.

## Verifikasi Pengaktifan Pelacakan

```java
System.out.println("Tracking enabled successfully for CAD rendering process.");
```

Pastikan pelacakan berhasil diaktifkan untuk proses rendering CAD.

## Masalah Umum & Pemecahan Masalah

| Gejala | Penyebab Kemungkinan | Solusi |
|---------|----------------------|--------|
| Halaman PDF muncul kosong | `PageWidth`/`PageHeight` diatur ke 0 | Pastikan dimensi tidak nol diberikan. |
| File output rusak | Aliran output tidak ditutup | Panggil `stream.close()` setelah `image.save(...)`. |
| Lapisan hilang di PDF | File CAD menggunakan entitas yang tidak didukung | Verifikasi bahwa format file sepenuhnya didukung oleh Aspose.CAD. |

## Pertanyaan yang Sering Diajukan

### Q1: Apakah Aspose.CAD kompatibel dengan semua format file CAD?

A1: Aspose.CAD mendukung beragam format CAD, termasuk DWG, DXF, DGN, dan lainnya. Lihat [dokumentasi](https://reference.aspose.com/cad/java/) untuk daftar lengkap.

### Q2: Bisakah saya menyesuaikan dimensi output file PDF?

A2: Tentu saja! Sesuaikan parameter `PageWidth` dan `PageHeight` dalam `CadRasterizationOptions` untuk menyesuaikan dimensi output.

### Q3: Apakah tersedia trial gratis untuk Aspose.CAD for Java?

A3: Ya, Anda dapat menjelajahi kemampuan Aspose.CAD dengan memperoleh trial gratis [di sini](https://releases.aspose.com/).

### Q4: Bagaimana saya dapat mendapatkan dukungan komunitas untuk pertanyaan terkait Aspose.CAD?

A4: Kunjungi [forum Aspose.CAD](https://forum.aspose.com/c/cad/19) untuk berinteraksi dengan komunitas dan meminta bantuan.

### Q5: Apakah lisensi sementara tersedia untuk Aspose.CAD?

A5: Ya, jika Anda memerlukan lisensi sementara, Anda dapat memperolehnya [di sini](https://purchase.aspose.com/temporary-license/).

## Kesimpulan

Selamat! Anda kini telah mempelajari cara **mengatur ukuran halaman PDF** dan mengaktifkan pelacakan untuk rendering CAD menggunakan **Aspose.CAD for Java**. Panduan ini memberi Anda kemampuan untuk **mengonversi CAD ke PDF**, **menyimpan CAD sebagai PDF**, dan menghasilkan PDF dari DXF dengan kontrol penuh atas dimensi halaman serta log eksekusi yang terperinci. Silakan bereksperimen dengan berbagai ukuran halaman dan jelajahi opsi rasterisasi tambahan untuk menyesuaikan alur kerja teknik Anda.

---

**Last Updated:** 2026-02-12  
**Tested With:** Aspose.CAD for Java 24.12 (latest at time of writing)  
**Author:** Aspose  

---

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}