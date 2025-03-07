---
title: Ekspor ke PDF dengan Aspose.CAD untuk Java
linktitle: Ekspor ke PDF
second_title: Aspose.CAD Java API
description: Pelajari cara mengekspor file CAD ke PDF dengan mudah menggunakan Aspose.CAD untuk Java. Ikuti panduan langkah demi langkah kami untuk integrasi yang lancar.
weight: 13
url: /id/java/cad-export-options/export-to-pdf/
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Ekspor ke PDF dengan Aspose.CAD untuk Java

## Perkenalan

Selamat datang di tutorial komprehensif tentang mengekspor file CAD ke PDF menggunakan Aspose.CAD untuk Java. Jika Anda ingin mengonversi gambar CAD Anda ke format PDF yang didukung secara luas dengan lancar, Anda berada di tempat yang tepat. Dalam panduan langkah demi langkah ini, kami akan menguraikan prosesnya, memastikan Anda memahami setiap langkah untuk mencapai ekspor PDF yang sukses.

## Prasyarat

Sebelum masuk ke tutorial, pastikan Anda memiliki prasyarat berikut:

-  Aspose.CAD untuk Java: Pastikan Anda telah menginstal perpustakaan Aspose.CAD di lingkungan Java Anda. Anda dapat mengunduhnya[Di Sini](https://releases.aspose.com/cad/java/).

- Direktori Sumber Daya: Siapkan direktori tempat file CAD Anda disimpan. Ganti "Direktori Dokumen Anda" di cuplikan kode yang disediakan dengan jalur sebenarnya.

Sekarang, mari kita beralih ke langkah utama.

## Impor Namespace

Dalam proyek Java Anda, mulailah dengan mengimpor namespace yang diperlukan untuk mengaktifkan penggunaan fungsionalitas Aspose.CAD.

```java
import com.aspose.cad.Image;
import com.aspose.cad.InterpolationMode;
import com.aspose.cad.SmoothingMode;
import com.aspose.cad.TextRenderingHint;

import com.aspose.cad.imageoptions.CadRasterizationOptions;
import com.aspose.cad.imageoptions.PdfOptions;
//impor com.aspose.cad.imageoptions.TypeOfEntities;
```

## Langkah 1: Muat File CAD

Muat file CAD Anda ke objek Gambar Aspose.CAD. Ganti "site.dwf" dengan nama file CAD Anda yang sebenarnya.

```java
String fileName = (dataDir + "site.dwf");
Image image = Image.load(fileName);
```

## Langkah 2: Konfigurasikan Opsi PDF

Siapkan opsi ekspor PDF, termasuk opsi rasterisasi vektor seperti tinggi halaman, lebar, dan tata letak.

```java
PdfOptions pdfOptions = new PdfOptions();
CadRasterizationOptions rasterizationOptions = new CadRasterizationOptions();
pdfOptions.setVectorRasterizationOptions(rasterizationOptions);

rasterizationOptions.setPageHeight(500);
rasterizationOptions.setPageWidth(500);
rasterizationOptions.setLayouts(new String[] { "Model" });
```

## Langkah 3: Ekspor ke PDF

Tentukan jalur keluaran untuk file PDF yang dihasilkan dan simpan gambar dengan opsi PDF yang dikonfigurasi.

```java
String outPath = dataDir + "site.pdf";
image.save(outPath, pdfOptions);
```

Selamat! Anda telah berhasil mengekspor file CAD Anda ke PDF menggunakan Aspose.CAD untuk Java.

## Kesimpulan

Dalam tutorial ini, kita menjelajahi proses langkah demi langkah mengekspor file CAD ke PDF menggunakan Aspose.CAD untuk Java. Dengan mengikuti langkah-langkah sederhana namun efektif ini, Anda dapat mengintegrasikan fungsi ini dengan lancar ke dalam aplikasi Java Anda.

## FAQ

### Q1: Apakah Aspose.CAD kompatibel dengan semua format file CAD?

A1: Ya, Aspose.CAD mendukung berbagai format CAD, memastikan kompatibilitas dengan berbagai perangkat lunak desain.

### Q2: Dapatkah saya menyesuaikan pengaturan keluaran PDF?

A2: Tentu saja. Tutorial ini memberikan sekilas opsi penyesuaian, namun Anda dapat menjelajahi lebih jauh untuk menyesuaikan keluaran sesuai kebutuhan Anda.

### Q3: Di mana saya dapat menemukan dukungan tambahan untuk Aspose.CAD?

 A3: Untuk pertanyaan atau masalah apa pun, kunjungi[Forum Aspose.CAD](https://forum.aspose.com/c/cad/19) untuk mencari bantuan dari masyarakat.

### Q4: Apakah tersedia uji coba gratis?

 A4: Ya, Anda dapat mengakses uji coba gratis Aspose.CAD[Di Sini](https://releases.aspose.com/).

### Q5: Bagaimana cara mendapatkan lisensi sementara untuk Aspose.CAD?

 A5: Untuk perizinan sementara, kunjungi[Link ini](https://purchase.aspose.com/temporary-license/).
{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}
