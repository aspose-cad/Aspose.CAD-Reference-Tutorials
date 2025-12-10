---
date: 2025-12-09
description: Pelajari cara mengaktifkan pelacakan DWG dengan Java dan juga lihat cara
  mengonversi DXF ke PDF menggunakan Aspose.CAD. Panduan langkah demi langkah ini
  menunjukkan alur kerja lengkap untuk proyek CAD kolaboratif.
linktitle: Enable Tracking in DWG Files Using Java
second_title: Aspose.CAD Java API
title: Aktifkan Pelacakan pada File DWG Menggunakan Aspose.CAD di Java
url: /id/java/additional-features/enable-tracking/
weight: 12
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Aktifkan Pelacakan pada File DWG Menggunakan Aspose.CAD di Java

## Pendahuluan

Dalam alur kerja CAD modern, kemampuan untuk **enable dwg tracking java** sangat penting bagi tim yang perlu memantau perubahan, menangkap kesalahan lebih awal, dan memastikan semua pemangku kepentingan berada pada halaman yang sama. Tutorial ini akan memandu Anda melalui langkah‑langkah tepat untuk mengaktifkan pelacakan pada file DWG menggunakan Aspose.CAD untuk Java, dan di sepanjang proses Anda juga akan melihat cara **java convert dxf pdf** sebagai bagian dari proses ekspor. Pada akhir tutorial, Anda akan memiliki potongan kode siap‑jalankan yang tidak hanya melakukan konversi tetapi juga melaporkan masalah rendering apa pun.

## Jawaban Cepat
- **Apa yang dilakukan “enable dwg tracking java”?** Itu mengaktifkan callback penanganan error Aspose.CAD sehingga Anda dapat melihat masalah rendering selama proses ekspor.  
- **Apakah saya memerlukan lisensi?** Versi percobaan dapat digunakan untuk pengujian; lisensi komersial diperlukan untuk produksi.  
- **Apakah saya juga dapat mengonversi DXF ke PDF?** Ya – `PdfOptions` yang sama digunakan untuk DWG juga berfungsi untuk DXF, memenuhi skenario *java convert dxf pdf*.  
- **Versi JDK mana yang diperlukan?** Java 8 atau lebih tinggi.  
- **Di mana saya dapat menemukan contoh lain?** Lihat Dokumentasi Aspose.CAD Java yang ditautkan di bawah.

## Apa itu enable dwg tracking java?
Mengaktifkan pelacakan DWG dalam aplikasi Java berarti menambahkan handler render kustom yang menangkap peringatan, error, dan informasi diagnostik lainnya saat file CAD dirasterisasi atau diekspor. Visibilitas ini membantu pengembang men-debug pipeline konversi dan memastikan hasil yang lebih berkualitas.

## Mengapa menggunakan Aspose.CAD untuk Java?
- **Dukungan CAD lengkap** – DWG, DXF, DGN, dan lainnya.  
- **Tanpa dependensi eksternal** – pustaka Java murni, ideal untuk otomatisasi sisi server.  
- **Pelacakan bawaan** – hasil render detail melalui `CadRenderHandler`.  
- **Ekspor PDF mudah** – konversi satu baris sambil mempertahankan data vektor.

## Prasyarat

Sebelum kita masuk ke implementasi, pastikan Anda telah menyiapkan hal‑hal berikut:

- Java Development Kit (JDK): Pastikan Java telah terpasang di sistem Anda.  
- Aspose.CAD untuk Java: Unduh dan instal Aspose.CAD untuk Java dari [download link](https://releases.aspose.com/cad/java/).  
- Direktori Dokumen: Siapkan direktori tempat file DWG Anda berada.

## Impor Namespace

Dalam proyek Java Anda, mulai dengan mengimpor namespace yang diperlukan untuk memanfaatkan fungsionalitas Aspose.CAD:

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

## Langkah 1: Muat File DWG

Mulailah dengan memuat file DWG (atau DXF) ke dalam aplikasi Java Anda. Sesuaikan jalur file sesuai kebutuhan:

```java
String dataDir = "Your Document Directory" + "DXFDrawings/";
Image image = Image.load(dataDir + "conic_pyramid.dxf");
```

## Langkah 2: Konfigurasikan Opsi Ekspor PDF

Siapkan opsi ekspor PDF, menentukan opsi rasterisasi vektor untuk CAD. Ini juga memperlihatkan kemampuan *java convert dxf pdf*:

```java
OutputStream stream = new FileOutputStream(dataDir + "output_conic_pyramid.pdf");
PdfOptions pdfOptions = new PdfOptions();
CadRasterizationOptions cadRasterizationOptions = new CadRasterizationOptions();
pdfOptions.setVectorRasterizationOptions(cadRasterizationOptions);
cadRasterizationOptions.setPageWidth(800);
cadRasterizationOptions.setPageHeight(600);
```

## Langkah 3: Implementasikan Pelacakan

Implementasikan pelacakan menggunakan kelas penanganan error kustom. Kelas ini akan menangkap masalah rendering dan menampilkannya di konsol:

```java
cadRasterizationOptions.RenderResult = new ErrorHandler();
```

## Langkah 4: Ekspor ke PDF

Mulailah proses ekspor untuk mengonversi file DWG/DXF ke PDF dengan pelacakan diaktifkan:

```java
System.out.println("Exporting to pdf format");
image.save(stream, pdfOptions);
```

## Langkah 5: Kelas CadRenderHandler

Definisikan kelas `ErrorHandler` (yang memperluas `CadRenderHandler`) untuk memproses hasil render dan mengeluarkan informasi pelacakan:

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

- **`NullPointerException` pada `RenderResult`** – Pastikan Anda menggunakan Aspose.CAD versi 23.10 atau lebih baru; rilis lama tidak memiliki API `RenderResult`.  
- **File tidak ditemukan** – Verifikasi bahwa `dataDir` mengarah ke folder yang benar dan nama file cocok persis, termasuk huruf besar/kecil.  
- **Output pelacakan tidak muncul** – Pastikan `ErrorHandler` kustom telah ditetapkan dengan benar ke `cadRasterizationOptions.RenderResult`.

## Pertanyaan yang Sering Diajukan

**T:** Apakah saya dapat mengaktifkan pelacakan untuk format file CAD lain menggunakan Aspose.CAD untuk Java?  
**J:** Aspose.CAD terutama mendukung pelacakan DWG. Untuk format lain, lihat dokumentasi resmi.

**T:** Bagaimana cara menangani opsi ekspor tambahan di Aspose.CAD untuk Java?  
**J:** Jelajahi dokumentasi lengkap di [Aspose.CAD Java Documentation](https://reference.aspose.com/cad/java/).

**T:** Apakah ada versi percobaan yang tersedia untuk Aspose.CAD untuk Java?  
**J:** Ya, Anda dapat mengakses versi percobaan di [Aspose.CAD Free Trial](https://releases.aspose.com/).

**T:** Di mana saya dapat mencari bantuan atau berdiskusi mengenai masalah terkait Aspose.CAD untuk Java?  
**J:** Kunjungi [Aspose.CAD forum](https://forum.aspose.com/c/cad/19) untuk dukungan komunitas.

**T:** Bagaimana cara mendapatkan lisensi sementara untuk Aspose.CAD untuk Java?  
**J:** Ikuti proses yang dijelaskan di [Temporary License](https://purchase.aspose.com/temporary-license/).

## Kesimpulan

Mengaktifkan pelacakan DWG di Java dengan Aspose.CAD tidak hanya memberi Anda visibilitas terhadap masalah konversi tetapi juga memperlancar alur kerja desain kolaboratif. Dengan mengikuti langkah‑langkah di atas, Anda dapat **enable dwg tracking java**, mengonversi DXF ke PDF, dan menangani setiap masalah rendering dengan elegan.

---

**Last Updated:** 2025-12-09  
**Tested With:** Aspose.CAD for Java 24.12  
**Author:** Aspose  

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}