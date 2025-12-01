---
date: 2025-12-01
description: Pelajari cara mengatur ukuran halaman PDF, mengonversi DWG ke PDF, dan
  mengaktifkan pelacakan perubahan DWG menggunakan Aspose.CAD untuk Java.
language: id
linktitle: Set PDF Page Size and Track DWG with Java
second_title: Aspose.CAD Java API
title: Atur Ukuran Halaman PDF dan Lacak DWG dengan Aspose.CAD Java
url: /java/additional-features/enable-tracking/
weight: 12
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Atur Ukuran Halaman PDF dan Lacak DWG dengan Aspose.CAD Java

## Pendahuluan

Saat berkolaborasi pada proyek CAD, Anda sering perlu **mengatur ukuran halaman PDF** untuk tata letak yang konsisten, **mengonversi DWG ke PDF**, dan melacak setiap perubahan yang dibuat pada gambar. Aspose.CAD untuk Java memungkinkan semua ini dalam satu alur kerja yang terintegrasi. Pada tutorial ini kami akan menjelaskan langkah‑langkah tepat untuk **mengatur ukuran halaman PDF**, mengaktifkan **pelacakan perubahan DWG**, dan mengekspor gambar sebagai PDF—semua menggunakan Java.

## Jawaban Cepat
- **Bagaimana cara mengatur ukuran halaman PDF?** Gunakan `CadRasterizationOptions.setPageWidth()` dan `setPageHeight()` sebelum mengekspor.  
- **Apakah saya dapat melacak perubahan saat mengekspor?** Ya – terapkan `CadRenderHandler` khusus untuk menangkap hasil pelacakan.  
- **Metode apa yang mengonversi DWG ke PDF?** Panggil `image.save(stream, pdfOptions)` setelah mengonfigurasi opsi.  
- **Apa saja prasyarat utama?** JDK, Aspose.CAD untuk Java, dan folder berisi file DWG/DXF.  
- **Apakah lisensi diperlukan untuk produksi?** Ya, lisensi Aspose.CAD yang valid diperlukan untuk penyebaran non‑trial.

## Apa itu “mengatur ukuran halaman PDF” dalam konteks ekspor DWG?

Mengatur ukuran halaman PDF menentukan dimensi kanvas PDF yang dihasilkan (lebar × tinggi dalam piksel). Ini penting ketika Anda ingin gambar yang diekspor sesuai dengan ukuran kertas atau tata letak layar tertentu, memastikan semua elemen muncul tepat di tempat yang diharapkan.

## Mengapa mengaktifkan pelacakan saat mengekspor file DWG?

Pelacakan (atau change‑tracking) mencatat setiap masalah rendering, font yang hilang, atau entitas yang tidak didukung yang terjadi selama konversi. Dengan menangkap informasi ini Anda dapat:

- Dengan cepat mengidentifikasi masalah yang perlu diperbaiki sebelum pengiriman akhir.  
- Memberikan umpan balik yang jelas kepada anggota tim tentang apa yang diubah atau dihilangkan.  
- Mempertahankan jejak audit untuk industri dengan kepatuhan yang ketat.

## Prasyarat

- **Java Development Kit (JDK)** – versi terbaru (8+).  
- **Aspose.CAD untuk Java** – unduh dari halaman resmi [Aspose CAD download page](https://releases.aspose.com/cad/java/).  
- **Direktori Dokumen** – folder yang berisi file DWG/DXF yang ingin Anda proses.

## Impor Namespace

Mulailah dengan mengimpor kelas Aspose.CAD yang diperlukan serta kelas I/O standar Java.

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

## Langkah 1: Muat File DWG (atau DXF)

Muat gambar sumber Anda ke dalam objek `Image`. Sesuaikan jalur agar mengarah ke direktori Anda sendiri.

```java
String dataDir = "Your Document Directory" + "DXFDrawings/";
Image image = Image.load(dataDir + "conic_pyramid.dxf");
```

## Langkah 2: Konfigurasikan Opsi Ekspor PDF (termasuk ukuran halaman)

Di sini kami mengatur opsi PDF dan secara eksplisit **mengatur ukuran halaman PDF** menjadi 800 × 600 piksel. Ini adalah tempat kata kunci utama diterapkan.

```java
OutputStream stream = new FileOutputStream(dataDir + "output_conic_pyramid.pdf");
PdfOptions pdfOptions = new PdfOptions();
CadRasterizationOptions cadRasterizationOptions = new CadRasterizationOptions();
pdfOptions.setVectorRasterizationOptions(cadRasterizationOptions);
cadRasterizationOptions.setPageWidth(800);   // set PDF page width
cadRasterizationOptions.setPageHeight(600);  // set PDF page height
```

## Langkah 3: Implementasikan Pelacakan

Buat penangkap kesalahan khusus yang akan menerima informasi pelacakan selama proses konversi.

```java
cadRasterizationOptions.RenderResult = new ErrorHandler();
```

## Langkah 4: Ekspor ke PDF

Dengan opsi dan penangkap pelacakan yang sudah disiapkan, ekspor gambar. Langkah ini **mengonversi DWG ke PDF** (atau DXF ke PDF dalam contoh kami).

```java
System.out.println("Exporting to pdf format");
image.save(stream, pdfOptions);
```

## Langkah 5: Kelas CadRenderHandler – Menangkap Hasil Pelacakan

Kelas `ErrorHandler` memperluas `CadRenderHandler` dan mencetak setiap masalah rendering yang terjadi saat **melacak perubahan DWG**.

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

## Masalah Umum & Cara Mengatasinya

| Masalah | Mengapa Terjadi | Solusi |
|-------|----------------|-----|
| **Font yang hilang** | File CAD merujuk pada font yang tidak terpasang di server. | Instal font yang diperlukan atau sematkan dalam gambar sumber. |
| **Entitas tidak didukung** | Beberapa entitas DWG belum didukung oleh Aspose.CAD. | Gunakan output pelacakan untuk mengidentifikasinya dan sederhanakan gambar. |
| **Ukuran halaman tidak tepat** | `setPageWidth/Height` tidak dipanggil sebelum ekspor. | Pastikan ukuran halaman diatur dalam `CadRasterizationOptions` seperti contoh di atas. |

## Pertanyaan yang Sering Diajukan

### Q1: Bisakah saya mengaktifkan pelacakan untuk format file CAD lain menggunakan Aspose.CAD untuk Java?

A1: Aspose.CAD terutama mendukung pelacakan untuk file DWG/DXF. Untuk format lain, lihat dokumentasi resmi untuk mengetahui fitur yang tersedia.

### Q2: Bagaimana cara menangani opsi ekspor tambahan di Aspose.CAD untuk Java?

A2: Perpustakaan ini menawarkan banyak opsi seperti DPI, warna latar belakang, dan rasterisasi vektor. Jelajahi di [Aspose.CAD Java Documentation](https://reference.aspose.com/cad/java/).

### Q3: Apakah ada versi percobaan yang tersedia untuk Aspose.CAD untuk Java?

A3: Ya, Anda dapat mengunduh percobaan gratis dari [Aspose.CAD Free Trial](https://releases.aspose.com/).

### Q4: Di mana saya dapat mencari bantuan atau berdiskusi tentang masalah terkait Aspose.CAD untuk Java?

A4: Forum komunitas di [Aspose.CAD forum](https://forum.aspose.com/c/cad/19) adalah tempat yang bagus untuk mengajukan pertanyaan dan berbagi pengalaman.

### Q5: Bagaimana cara memperoleh lisensi sementara untuk Aspose.CAD untuk Java?

A5: Ikuti langkah‑langkah yang dijelaskan pada halaman [Temporary License](https://purchase.aspose.com/temporary-license/) untuk meminta lisensi berjangka waktu untuk evaluasi.

### Q6: Bisakah saya **mengonversi DWG ke PDF** sambil mempertahankan lapisan?

A6: Ya. Dengan mengonfigurasi `CadRasterizationOptions` Anda dapat mempertahankan informasi lapisan dalam PDF yang dihasilkan.

### Q7: Apa cara terbaik untuk **mengekspor DWG sebagai PDF** dengan dimensi halaman khusus?

A7: Atur lebar dan tinggi yang diinginkan menggunakan `setPageWidth` dan `setPageHeight` sebelum memanggil `image.save()` – persis seperti yang ditunjukkan pada Langkah 2.

## Kesimpulan

Dengan mengikuti langkah‑langkah di atas Anda dapat **mengatur ukuran halaman PDF**, **mengonversi DWG ke PDF**, dan **melacak perubahan pada file DWG** menggunakan Aspose.CAD untuk Java. Alur kerja ini memberi Anda kontrol penuh atas tata letak output sekaligus menyediakan diagnostik berharga yang menjaga kolaborasi CAD Anda tetap lancar dan bebas error. Jangan ragu untuk menjelajahi opsi rendering tambahan dan mengintegrasikan kode ini ke dalam pipeline otomatisasi yang lebih besar.

---

**Terakhir Diperbarui:** 2025-12-01  
**Diuji Dengan:** Aspose.CAD untuk Java 24.12 (terbaru pada saat penulisan)  
**Penulis:** Aspose  

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}