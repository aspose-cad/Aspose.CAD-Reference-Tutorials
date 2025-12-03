---
date: 2025-12-03
description: Pelajari cara mengatur ukuran halaman PDF saat mengonversi DWG ke PDF
  dan mengaktifkan pelacakan dalam file DWG menggunakan Aspose.CAD untuk Java – panduan
  lengkap untuk mengekspor PDF gambar CAD dengan presisi.
language: id
linktitle: Set PDF Page Size and Enable Tracking in DWG Files Using Java
second_title: Aspose.CAD Java API
title: Atur Ukuran Halaman PDF dan Aktifkan Pelacakan pada File DWG Menggunakan Aspose.CAD
  di Java
url: /java/additional-features/enable-tracking/
weight: 12
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Atur Ukuran Halaman PDF dan Aktifkan Pelacakan pada File DWG Menggunakan Aspose.CAD di Java

## Pendahuluan

Jika Anda perlu **mengatur ukuran halaman PDF** saat *mengonversi DWG ke PDF* dan juga melacak masalah rendering apa pun, Aspose.CAD untuk Java memberikan cara yang bersih dan programatik untuk melakukan keduanya. Dalam tutorial ini kami akan menjelaskan langkah‑langkah tepat untuk mengonfigurasi dimensi halaman, mengaktifkan pelacakan, dan mengekspor PDF gambar CAD—semua dari Java. Pada akhir tutorial Anda akan memahami mengapa mengatur ukuran halaman yang tepat penting untuk gambar CAD dan bagaimana menangkap informasi pelacakan terperinci selama proses ekspor.

## Jawaban Cepat
- **Apa yang dipengaruhi oleh “set PDF page size”?** Ini menentukan lebar dan tinggi kanvas PDF yang dihasilkan, memastikan gambar Anda pas dengan sempurna.  
- **Apakah saya memerlukan lisensi untuk menggunakan fitur ini?** Versi percobaan dapat digunakan untuk pengujian; lisensi komersial diperlukan untuk produksi.  
- **Versi Aspose.CAD mana yang diperlukan?** Versi terbaru yang mendukung `CadRasterizationOptions`.  
- **Bisakah saya menggunakan ini dengan format CAD lain?** Contoh menunjukkan DWG/DXF, tetapi pendekatan yang sama berlaku untuk sebagian besar format yang didukung.  
- **Berapa lama proses konversi?** Biasanya kurang dari satu detik untuk file sederhana; gambar yang lebih besar mungkin memerlukan waktu lebih lama.

## Apa itu “set PDF page size” dalam konteks ekspor CAD?
Mengatur ukuran halaman PDF memberi tahu renderer dimensi tepat (dalam piksel atau poin) dari kanvas output. Ini sangat penting untuk gambar teknis di mana skala dan tata letak harus dipertahankan. Tanpa pengaturan ukuran halaman secara eksplisit, PDF mungkin menggunakan ukuran default yang memotong atau mendistorsi gambar.

## Mengapa mengatur ukuran halaman PDF saat mengekspor gambar CAD?
- **Mempertahankan skala** – Insinyur mengandalkan cetakan yang sesuai skala.  
- **Pas ke kertas** – Pilih A4, Letter, atau ukuran khusus yang sesuai dengan spesifikasi proyek.  
- **Meningkatkan keterbacaan** – Halaman yang lebih besar dapat menampilkan detail halus tanpa harus memperbesar.  
- **Output konsisten** – Pipeline otomatis menghasilkan PDF dengan dimensi identik setiap kali dijalankan.

## Cara mengatur ukuran halaman PDF saat mengonversi DWG ke PDF?
Di bawah ini kami akan mengonfigurasi `CadRasterizationOptions` dengan nilai lebar dan tinggi khusus sebelum mengekspor. Langkah ini secara langsung menangani kata kunci utama **set PDF page size**.

## Prasyarat

- **Java Development Kit (JDK)** – Java 8 atau yang lebih baru terpasang di mesin Anda.  
- **Aspose.CAD untuk Java** – Unduh dari [halaman unduhan Aspose CAD resmi](https://releases.aspose.com/cad/java/).  
- **Direktori Dokumen** – Folder yang berisi file DWG/DXF yang ingin Anda proses.

## Impor Namespace

Pertama, impor kelas yang diperlukan. Blok kode tidak diubah dari tutorial asli.

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

## Langkah 1: Muat File DWG/DXF

Muat gambar sumber Anda. Sesuaikan jalur agar mengarah ke file Anda sendiri.

```java
String dataDir = "Your Document Directory" + "DXFDrawings/";
Image image = Image.load(dataDir + "conic_pyramid.dxf");
```

## Langkah 2: Konfigurasi Opsi Ekspor PDF (termasuk ukuran halaman)

Di sini kami mengatur lebar dan tinggi halaman—ini adalah tempat kami **set PDF page size**. Nilainya dalam piksel; Anda dapat mengonversi dari inci atau milimeter sesuai kebutuhan.

```java
OutputStream stream = new FileOutputStream(dataDir + "output_conic_pyramid.pdf");
PdfOptions pdfOptions = new PdfOptions();
CadRasterizationOptions cadRasterizationOptions = new CadRasterizationOptions();
pdfOptions.setVectorRasterizationOptions(cadRasterizationOptions);
cadRasterizationOptions.setPageWidth(800);   // <-- custom width
cadRasterizationOptions.setPageHeight(600);  // <-- custom height
```

> **Tip:** Jika Anda lebih suka ukuran kertas standar, gunakan konversi `1 inch = 72 points`. Untuk halaman A4 (8,27 × 11,69 in), atur `pageWidth = 595` dan `pageHeight = 842`.

## Langkah 3: Implementasikan Pelacakan

Pelacakan menangkap masalah rendering apa pun. Kami menambahkan handler khusus yang akan dipanggil setelah proses ekspor.

```java
cadRasterizationOptions.RenderResult = new ErrorHandler();
```

## Langkah 4: Ekspor ke PDF

Sekarang lakukan konversi. PDF akan dibuat dengan dimensi yang Anda tentukan, dan informasi pelacakan akan dicetak ke konsol.

```java
System.out.println("Exporting to pdf format");
image.save(stream, pdfOptions);
```

## Langkah 5: Kelas CadRenderHandler

Handler mencetak semua kegagalan yang terjadi selama rendering. Ini membantu Anda men-debug masalah saat **mengekspor PDF gambar CAD**.

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

## Masalah Umum dan Solusinya

| Masalah | Penyebab | Solusi |
|-------|-------|-----|
| **PDF Kosong** | Ukuran halaman diatur 0 atau terlalu kecil | Pastikan `setPageWidth` dan `setPageHeight` memiliki nilai positif. |
| **Geometri Hilang** | Kesalahan rendering yang ditangkap oleh handler | Tinjau output konsol dari `ErrorHandler` dan selesaikan `RenderCode` yang spesifik. |
| **File tidak ditemukan** | Jalur `dataDir` salah | Gunakan jalur absolut atau pastikan direktori tersebut ada. |
| **Pengecualian lisensi** | Menggunakan versi percobaan tanpa lisensi yang valid untuk file besar | Terapkan lisensi Aspose.CAD Anda sebelum memuat gambar. |

## Pertanyaan yang Sering Diajukan

**T: Bisakah saya mengaktifkan pelacakan untuk format file CAD lain menggunakan Aspose.CAD untuk Java?**  
J: Aspose.CAD terutama mendukung DWG/DXF untuk pelacakan. Untuk format lain, lihat dokumentasi resmi.

**T: Bagaimana cara menangani opsi ekspor tambahan di Aspose.CAD untuk Java?**  
J: Perpustakaan menawarkan banyak opsi seperti DPI, warna latar belakang, dan rasterisasi vektor. Lihat [Dokumentasi Aspose.CAD Java](https://reference.aspose.com/cad/java/) untuk detailnya.

**T: Apakah tersedia versi percobaan untuk Aspose.CAD untuk Java?**  
J: Ya, Anda dapat mengunduh percobaan gratis dari [Aspose.CAD Free Trial](https://releases.aspose.com/).

**T: Di mana saya dapat mencari bantuan atau berdiskusi tentang masalah terkait Aspose.CAD untuk Java?**  
J: Kunjungi [forum Aspose.CAD](https://forum.aspose.com/c/cad/19) untuk dukungan komunitas dan jawaban resmi.

**T: Bagaimana cara mendapatkan lisensi sementara untuk Aspose.CAD untuk Java?**  
J: Ikuti langkah‑langkah yang dijelaskan pada halaman [Lisensi Sementara](https://purchase.aspose.com/temporary-license/).

---

**Terakhir Diperbarui:** 2025-12-03  
**Diuji Dengan:** Aspose.CAD untuk Java 24.11 (terbaru pada saat penulisan)  
**Penulis:** Aspose  

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}