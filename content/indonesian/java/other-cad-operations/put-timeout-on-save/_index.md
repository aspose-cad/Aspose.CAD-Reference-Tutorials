---
title: Batas waktu Simpan untuk CAD dengan Aspose.CAD
linktitle: Letakkan Batas Waktu pada Simpan
second_title: Aspose.CAD Java API
description: Pelajari cara meningkatkan kinerja aplikasi Java Anda dengan Aspose.CAD. Beri batas waktu untuk menyimpan gambar CAD. Ikuti panduan langkah demi langkah kami.
type: docs
weight: 15
url: /id/java/other-cad-operations/put-timeout-on-save/
---
## Perkenalan

Selamat datang di tutorial tentang memberi batas waktu penyimpanan menggunakan Aspose.CAD untuk Java. Dalam panduan ini, kami akan memandu Anda melalui proses pengaturan waktu tunggu untuk menyimpan gambar CAD guna meningkatkan kinerja aplikasi Anda. Aspose.CAD untuk Java adalah perpustakaan canggih yang memungkinkan Anda bekerja dengan file CAD di aplikasi Java Anda dengan lancar.

## Prasyarat

Sebelum masuk ke tutorial, pastikan Anda memiliki prasyarat berikut:
-  Aspose.CAD untuk Perpustakaan Java: Pastikan Anda memiliki perpustakaan Aspose.CAD untuk Java yang terintegrasi ke dalam proyek Anda. Anda dapat mengunduh perpustakaan dari[situs web](https://releases.aspose.com/cad/java/).
- Lingkungan Pengembangan: Siapkan lingkungan pengembangan Java Anda dengan semua alat dan dependensi yang diperlukan.

## Paket Impor

Untuk memulai, impor paket yang diperlukan ke proyek Java Anda. Tambahkan baris berikut di awal file Java Anda:

```java
import com.aspose.cad.Image;
import com.aspose.cad.InterruptionTokenSource;
import com.aspose.cad.fileformats.cad.CadImage;
import com.aspose.cad.imageoptions.CadRasterizationOptions;
import com.aspose.cad.imageoptions.PdfOptions;
import java.util.concurrent.TimeUnit;
```

Sekarang, mari kita pecahkan kode contoh menjadi petunjuk langkah demi langkah:

## Langkah 1: Tetapkan Direktori Sumber dan Output

```java
final String SourceDir = Utils.getDataDir_DWGDrawings();
final String OutputDir = Utils.getDataDir_Output();
```

Pastikan Anda memiliki direktori sumber dan keluaran yang benar untuk gambar CAD Anda.

## Langkah 2: Buat Sumber Token Interupsi

```java
final InterruptionTokenSource source = new com.aspose.cad.InterruptionTokenSource();
```

Inisialisasi sumber token interupsi untuk mengelola interupsi selama operasi penyimpanan.

## Langkah 3: Muat Gambar CAD

```java
final CadImage cadImageBig = (CadImage)Image.load(SourceDir + "Drawing11.dwg");
```

 Muat gambar CAD ke dalam a`CadImage` obyek.

## Langkah 4: Konfigurasikan Opsi Rasterisasi

```java
CadRasterizationOptions rasterizationOptionsBig = new CadRasterizationOptions();
rasterizationOptionsBig.setPageWidth(cadImageBig.getSize().getWidth() / 2);
rasterizationOptionsBig.setPageHeight(cadImageBig.getSize().getHeight() / 2);
```

Konfigurasikan opsi rasterisasi untuk gambar CAD.

## Langkah 5: Konfigurasikan Opsi PDF

```java
final PdfOptions CADfBig = new PdfOptions();
CADfBig.setVectorRasterizationOptions(rasterizationOptionsBig);
CADfBig.setInterruptionToken(source.getToken());
```

Siapkan opsi PDF dengan opsi rasterisasi vektor dan token interupsi.

## Langkah 6: Simpan Gambar dengan Timeout

```java
cadImageBig.save(OutputDir + "PutTimeoutOnSave_out.pdf", CADfBig);
```

Simpan gambar CAD ke file PDF dengan batas waktu yang ditentukan.

## Langkah 7: Tangani Interupsi

```java
java.lang.Thread thread = new java.lang.Thread(new Runnable() {
    @Override
    public void run() {
        try {
            cadImageBig.save(OutputDir + "PutTimeoutOnSave_out.pdf", CADfBig);
        } catch (Throwable th) {
            System.out.println("interrupted !!!");
        }
    }
});
thread.start();
TimeUnit.SECONDS.sleep(3);
source.interrupt();
thread.join();
```

Buat thread untuk menangani operasi penyimpanan dan hentikan setelah batas waktu yang ditentukan.

## Kesimpulan

Selamat! Anda telah berhasil mempelajari cara memberi batas waktu penyimpanan menggunakan Aspose.CAD untuk Java. Fitur ini dapat meningkatkan efisiensi aplikasi Anda yang berhubungan dengan CAD.

## FAQ

### Q1: Bagaimana cara mengunduh Aspose.CAD untuk Java?

 A1: Anda dapat mengunduhnya dari[halaman rilis](https://releases.aspose.com/cad/java/).

### Q2: Di mana saya dapat menemukan dokumentasi Aspose.CAD untuk Java?

 A2: Lihat[dokumentasi](https://reference.aspose.com/cad/java/) untuk informasi yang komprehensif.

### Q3: Apakah tersedia uji coba gratis?

A3: Ya, Anda bisa mendapatkan uji coba gratis[Link ini](https://releases.aspose.com/).

### Q4: Bagaimana cara mendapatkan lisensi sementara?

 A4: Kunjungi[Di Sini](https://purchase.aspose.com/temporary-license/) untuk rincian lisensi sementara.

### Q5: Butuh bantuan atau punya pertanyaan?

 A5: Pergilah ke[Forum Aspose.CAD](https://forum.aspose.com/c/cad/19) untuk dukungan masyarakat.