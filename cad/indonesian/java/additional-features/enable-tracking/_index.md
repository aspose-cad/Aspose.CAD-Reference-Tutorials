---
date: 2026-02-10
description: Panduan langkah demi langkah tentang cara mengaktifkan pelacakan pada
  file DWG menggunakan Aspose.CAD untuk Java dan cara mengonversi DXF ke PDF dengan
  penanganan kesalahan khusus.
linktitle: Enable Tracking in DWG Files Using Java
second_title: Aspose.CAD Java API
title: Cara Mengaktifkan Pelacakan pada File DWG Menggunakan Aspose.CAD di Java
url: /id/java/additional-features/enable-tracking/
weight: 12
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Cara Mengaktifkan Pelacakan pada File DWG Menggunakan Aspose.CAD di Java

## Pendahuluan

Jika Anda bekerja pada proyek CAD kolaboratif, mengetahui **cara mengaktifkan pelacakan** dalam alur kerja DWG Anda merupakan perubahan besar. Ini memberi Anda wawasan waktu nyata tentang masalah rendering, memungkinkan Anda menangkap gangguan konversi lebih awal, dan menjaga semua pemangku kepentingan tetap terinformasi. Dalam tutorial ini kami akan memandu Anda langkah demi langkah untuk mengaktifkan pelacakan dengan Aspose.CAD untuk Java, dan kami juga akan menunjukkan **cara mengonversi DXF ke PDF** sebagai bagian dari pipeline yang sama. Pada akhir tutorial Anda akan memiliki potongan kode lengkap yang siap produksi yang melaporkan error melalui kelas **custom error handler Java** saat mengekspor gambar Anda.

## Jawaban Cepat
- **Apa yang dilakukan “enable dwg tracking java”?** Itu mengaktifkan callback penanganan error Aspose.CAD sehingga Anda dapat melihat masalah rendering selama ekspor.  
- **Apakah saya memerlukan lisensi?** Versi trial dapat digunakan untuk pengujian; lisensi komersial diperlukan untuk produksi.  
- **Bisakah saya juga mengonversi DXF ke PDF?** Ya – `PdfOptions` yang sama digunakan untuk DWG juga berfungsi untuk DXF, memenuhi skenario *java convert dxf pdf*.  
- **Versi JDK mana yang diperlukan?** Java 8 atau lebih tinggi.  
- **Di mana saya dapat menemukan contoh lainnya?** Lihat Dokumentasi Aspose.CAD Java yang ditautkan di bawah.

## Cara Mengaktifkan Pelacakan pada File DWG Menggunakan Aspose.CAD

Mengaktifkan pelacakan DWG dalam aplikasi Java berarti melampirkan handler render khusus yang menangkap peringatan, error, dan informasi diagnostik lainnya saat file CAD dirasterisasi atau diekspor. Visibilitas ini membantu pengembang men-debug pipeline konversi dan memastikan hasil yang lebih berkualitas.

## Mengapa Menggunakan Aspose.CAD untuk Java?

- **Dukungan CAD lengkap** – DWG, DXF, DGN, dan lainnya.  
- **Tanpa dependensi eksternal** – perpustakaan Java murni, ideal untuk otomatisasi sisi server.  
- **Pelacakan bawaan** – hasil render detail melalui `CadRenderHandler`.  
- **Ekspor PDF mudah** – konversi satu baris sambil mempertahankan data vektor.  

## Prasyarat

Sebelum kita masuk ke implementasi, pastikan Anda telah menyiapkan prasyarat berikut:

- Java Development Kit (JDK): Pastikan Java terpasang di sistem Anda.  
- Aspose.CAD for Java: Unduh dan instal Aspose.CAD for Java dari [download link](https://releases.aspose.com/cad/java/).  
- Direktori Dokumen: Siapkan direktori tempat file DWG Anda berada.

## Impor Namespace

Dalam proyek Java Anda, mulailah dengan mengimpor namespace yang diperlukan untuk memanfaatkan fungsionalitas Aspose.CAD:

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

## Langkah 2: Konfigurasikan Opsi Ekspor PDF (Cara Mengonversi DXF ke PDF)

Atur opsi ekspor PDF, menentukan opsi rasterisasi vektor untuk CAD. Ini juga memperlihatkan kemampuan *java convert dxf pdf*:

```java
OutputStream stream = new FileOutputStream(dataDir + "output_conic_pyramid.pdf");
PdfOptions pdfOptions = new PdfOptions();
CadRasterizationOptions cadRasterizationOptions = new CadRasterizationOptions();
pdfOptions.setVectorRasterizationOptions(cadRasterizationOptions);
cadRasterizationOptions.setPageWidth(800);
cadRasterizationOptions.setPageHeight(600);
```

## Langkah 3: Implementasikan Pelacakan (Custom Error Handler Java)

Implementasikan pelacakan menggunakan kelas error handler khusus. Kelas ini akan menangkap masalah rendering dan menampilkannya di konsol:

```java
cadRasterizationOptions.RenderResult = new ErrorHandler();
```

## Langkah 4: Ekspor ke PDF

Mulailah proses ekspor untuk mengonversi file DWG/DXF menjadi PDF dengan pelacakan diaktifkan:

```java
System.out.println("Exporting to pdf format");
image.save(stream, pdfOptions);
```

## Langkah 5: Kelas CadRenderHandler

Definisikan kelas `ErrorHandler` (yang memperluas `CadRenderHandler`) untuk memproses hasil rendering dan mengeluarkan informasi pelacakan:

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

## Mengapa Ini Penting

Dengan mengaktifkan pelacakan Anda memperoleh jejak audit yang jelas dari setiap langkah konversi. Hal ini sangat berharga di industri yang diatur (arsitektur, teknik, konstruksi) dimana bukti rendering yang akurat diperlukan untuk audit kepatuhan. Error handler khusus juga memberi Anda titik kait untuk mencatat masalah ke sistem pemantauan atau memicu percobaan ulang otomatis.

## Masalah Umum dan Solusinya

- **`NullPointerException` pada `RenderResult`** – Pastikan Anda menggunakan Aspose.CAD versi 23.10 atau lebih baru; rilis lama tidak memiliki API `RenderResult`.  
- **File tidak ditemukan** – Verifikasi bahwa `dataDir` mengarah ke folder yang tepat dan nama file cocok persis, termasuk huruf besar/kecil.  
- **Output pelacakan tidak muncul** – Pastikan `ErrorHandler` kustom telah ditetapkan dengan benar ke `cadRasterizationOptions.RenderResult`.

## Pertanyaan yang Sering Diajukan

**Q:** Apakah saya dapat mengaktifkan pelacakan untuk format file CAD lain menggunakan Aspose.CAD untuk Java?  
A: Aspose.CAD terutama mendukung pelacakan DWG. Untuk format lain, lihat dokumentasi resmi.

**Q:** Bagaimana saya dapat menangani opsi ekspor tambahan di Aspose.CAD untuk Java?  
A: Jelajahi dokumentasi lengkap di [Aspose.CAD Java Documentation](https://reference.aspose.com/cad/java/).

**Q:** Apakah tersedia versi trial untuk Aspose.CAD untuk Java?  
A: Ya, Anda dapat mengakses versi trial di [Aspose.CAD Free Trial](https://releases.aspose.com/).

**Q:** Di mana saya dapat mencari bantuan atau mendiskusikan masalah terkait Aspose.CAD untuk Java?  
A: Kunjungi [Aspose.CAD forum](https://forum.aspose.com/c/cad/19) untuk dukungan komunitas.

**Q:** Bagaimana cara mendapatkan lisensi sementara untuk Aspose.CAD untuk Java?  
A: Ikuti proses yang dijelaskan di [Temporary License](https://purchase.aspose.com/temporary-license/).

## Kesimpulan

Mengaktifkan pelacakan DWG di Java dengan Aspose.CAD tidak hanya memberi Anda visibilitas terhadap masalah konversi tetapi juga menyederhanakan alur kerja desain kolaboratif. Dengan mengikuti langkah‑langkah di atas Anda dapat **cara mengaktifkan pelacakan**, mengonversi DXF ke PDF, dan menangani setiap masalah rendering dengan elegan.

---

**Last Updated:** 2026-02-10  
**Tested With:** Aspose.CAD for Java 24.12  
**Author:** Aspose  

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}