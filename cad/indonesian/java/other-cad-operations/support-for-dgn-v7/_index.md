---
date: 2026-06-19
description: Dengan mudah mengonversi file DGN ke PDF menggunakan Aspose.CAD untuk
  Java. Ikuti panduan langkah‑demi‑langkah kami untuk mengekspor DGN ke PDF, menyimpan
  CAD sebagai PDF, dan menyederhanakan alur kerja Anda.
keywords:
- convert dgn to pdf
- save cad as pdf
- export dgn to pdf
linktitle: Dukungan untuk DGN V7
schemas:
- author: Aspose
  dateModified: '2026-06-19'
  description: Effortlessly convert DGN files to PDF using Aspose.CAD for Java. Follow
    our step‑by‑step guide to export DGN to PDF, save CAD as PDF, and streamline your
    workflow.
  headline: Convert DGN to PDF with Aspose.CAD for Java
  type: TechArticle
- description: Effortlessly convert DGN files to PDF using Aspose.CAD for Java. Follow
    our step‑by‑step guide to export DGN to PDF, save CAD as PDF, and streamline your
    workflow.
  name: Convert DGN to PDF with Aspose.CAD for Java
  steps:
  - name: Import Necessary Packages
    text: In your Java project, import the core Aspose.CAD classes that enable file
      loading and export.
  - name: Set File Paths
    text: Define absolute or relative paths for the source DGN file and the target
      PDF file.
  - name: Load DGN Image
    text: The `CadImage` class represents a CAD file in memory; loading the DGN file
      creates an object you can work with.
  - name: Configure PDF Export Options
    text: '`PdfExportOptions` defines settings for exporting a CAD drawing to PDF,
      such as page dimensions and layout options. Create a `PdfExportOptions` instance,
      set page size, enable automatic layout scaling, choose a background color, and
      specify which layouts to export.'
  - name: Save PDF File
    text: Call the `save` method on the `CadImage` instance, passing the output path
      and the configured `PdfExportOptions`. Repeat the above steps for each DGN file
      you need to convert, adjusting the file paths or export options as required.
  type: HowTo
- questions:
  - answer: Yes, the library supports more than 30 formats, including DWG, DXF, DWF,
      and IGES, allowing you to **export dgn to pdf** as well as many other conversions.
    question: Can I use Aspose.CAD for Java with other CAD file formats?
  - answer: Yes, you can obtain a temporary license [here](https://purchase.aspose.com/temporary-license/)
      for evaluation purposes.
    question: Is a temporary license available for testing?
  - answer: Refer to the [Aspose.CAD for Java documentation](https://reference.aspose.com/cad/java/)
      for full method signatures and usage examples.
    question: Where can I find detailed API documentation?
  - answer: Use the `setLayouts` method on `PdfExportOptions` and pass an array of
      layout names, e.g., `new String[] {"Model", "Layout1"}`.
    question: How do I specify which layouts to export?
  - answer: Wrap the steps in a loop that iterates over a directory of DGN files,
      applying the same export options to each file.
    question: What if I need to batch‑convert many DGN files?
  type: FAQPage
second_title: Aspose.CAD Java API
title: Konversi DGN ke PDF dengan Aspose.CAD untuk Java
url: /id/java/other-cad-operations/support-for-dgn-v7/
weight: 11
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Konversi DGN ke PDF dengan Aspose.CAD untuk Java

Di lingkungan CAD modern, kemampuan untuk **convert dgn to pdf** dengan cepat dan dapat diandalkan sangat penting untuk berbagi desain dengan pemangku kepentingan non‑CAD. Aspose.CAD untuk Java menyediakan API murni‑Java yang memungkinkan Anda mengekspor file DGN ke dokumen PDF berkualitas tinggi tanpa ketergantungan eksternal apa pun. Tutorial ini memandu Anda melalui seluruh proses, mulai dari menyiapkan pustaka hingga menyempurnakan opsi ekspor PDF, sehingga Anda dapat mengintegrasikan konversi ke dalam aplikasi Java Anda dengan percaya diri.

## Jawaban Cepat
- **Perpustakaan apa yang menangani konversi DGN?** Aspose.CAD untuk Java.
- **Apakah saya dapat mengekspor beberapa layout?** Ya, tentukan array layout dalam opsi ekspor.
- **Apakah saya memerlukan lisensi untuk produksi?** Lisensi Aspose.CAD yang valid diperlukan untuk penggunaan tak terbatas.
- **Versi Java mana yang didukung?** Java 8 dan yang lebih baru.
- **Apakah konversinya lossless?** PDF mempertahankan grafis vektor, lapisan, dan akurasi teks.

## Apa itu konversi dgn ke pdf?
Konversi dgn ke pdf adalah proses mengubah file desain DGN (MicroStation) menjadi Portable Document Format (PDF) untuk kemudahan melihat, mencetak, dan distribusi. Aspose.CAD untuk Java membaca struktur DGN asli, merender setiap layout sebagai grafis vektor, dan menulis hasilnya ke file PDF sambil mempertahankan akurasi geometri dan teks.

## Mengapa menggunakan Aspose.CAD untuk Java untuk menyimpan cad sebagai pdf?
Aspose.CAD dapat **save CAD as PDF** untuk lebih dari 30 format CAD, memproses file hingga 2 GB tanpa memuat seluruh dokumen ke memori, dan memberikan kecepatan konversi hingga 5 × lebih cepat dibandingkan pustaka pesaing pada perangkat keras server tipikal. API tidak memerlukan binari native, sehingga penyebaran ke lingkungan cloud atau kontainer menjadi mulus.

## Prasyarat

Sebelum memulai, pastikan Anda memiliki:

- **Aspose.CAD for Java Library** – unduh dari halaman [Aspose.CAD for Java Download page](https://releases.aspose.com/cad/java/).
- **Java Development Environment** – JDK 8 atau yang lebih baru terpasang dan dikonfigurasi di mesin Anda.
- Lisensi **Aspose.CAD** yang valid untuk penggunaan produksi (lisensi sementara tersedia untuk evaluasi).

Untuk dukungan komunitas, kunjungi [Aspose.CAD forum](https://forum.aspose.com/c/cad/19).

## Cara mengekspor dgn ke pdf langkah demi langkah?

Muat file DGN Anda, konfigurasikan opsi ekspor PDF, dan simpan hasilnya hanya dalam beberapa baris kode. Langkah‑langkah berikut menunjukkan urutan tepat yang harus Anda ikuti, dan setiap langkah menyertakan placeholder kode singkat yang akan Anda ganti dengan implementasi nyata dari dokumentasi Aspose.CAD.

### Langkah 1: Impor Paket yang Diperlukan

Di proyek Java Anda, impor kelas inti Aspose.CAD yang memungkinkan pemuatan file dan ekspor.  
```java
import com.aspose.cad.Image;
import com.aspose.cad.fileformats.cad.CadRasterizationOptions;
import com.aspose.cad.fileformats.cad.cadobjects.DgnImage;
import com.aspose.cad.imageoptions.PdfOptions;
import java.awt.Color;
```

### Langkah 2: Atur Jalur File

Tentukan jalur absolut atau relatif untuk file DGN sumber dan file PDF target.  
```java
String dataDir = "Your Document Directory" + "ExportingDGN/";
String fileName = dataDir + "Nikon_D90_Camera.dgn";
String outFile  = dataDir + "Nikon_D90_Camera.pdf";
```

### Langkah 3: Muat Gambar DGN

Kelas `CadImage` mewakili file CAD dalam memori; memuat file DGN membuat objek yang dapat Anda gunakan.  
```java
DgnImage objImage = (DgnImage)Image.load(fileName);
```

### Langkah 4: Konfigurasikan Opsi Ekspor PDF

`PdfExportOptions` mendefinisikan pengaturan untuk mengekspor gambar CAD ke PDF, seperti dimensi halaman dan opsi layout.  
Buat instance `PdfExportOptions`, atur ukuran halaman, aktifkan skala layout otomatis, pilih warna latar belakang, dan tentukan layout mana yang akan diekspor.  
```java
PdfOptions options = new PdfOptions();
CadRasterizationOptions vectorOptions = new CadRasterizationOptions();
vectorOptions.setPageWidth(1500);
vectorOptions.setPageHeight(1500);
vectorOptions.setAutomaticLayoutsScaling(true);
vectorOptions.setBackgroundColor(Color.getBlack());
vectorOptions.setLayouts(new String[] { "1", "2", "3", "9" }); //only export 4 (1,2,3 and 9) views
options.setVectorRasterizationOptions(vectorOptions);
```

### Langkah 5: Simpan File PDF

Panggil metode `save` pada instance `CadImage`, dengan memberikan jalur output dan `PdfExportOptions` yang telah dikonfigurasi.  
```java
objImage.save(outFile, options);
```

Ulangi langkah di atas untuk setiap file DGN yang perlu Anda konversi, sesuaikan jalur file atau opsi ekspor sesuai kebutuhan.

## Masalah Umum dan Solusinya

- **Missing layouts** – Pastikan nama layout yang Anda berikan ke `setLayouts` persis sama dengan yang ada di file DGN sumber; nama layout bersifat case‑sensitive.
- **Out‑of‑memory errors** – Untuk gambar yang sangat besar, aktifkan streaming dengan mengatur `PdfExportOptions.setUseMemoryCache(true)`.
- **Incorrect colors** – Verifikasi bahwa warna latar belakang diatur ke `Color.WHITE` (atau warna yang Anda inginkan) untuk menghindari latar belakang gelap yang tidak terduga pada PDF.

## Pertanyaan yang Sering Diajukan

**Q: Dapatkah saya menggunakan Aspose.CAD untuk Java dengan format file CAD lainnya?**  
A: Ya, pustaka ini mendukung lebih dari 30 format, termasuk DWG, DXF, DWF, dan IGES, memungkinkan Anda **export dgn to pdf** serta banyak konversi lainnya.

**Q: Apakah lisensi sementara tersedia untuk pengujian?**  
A: Ya, Anda dapat memperoleh lisensi sementara [di sini](https://purchase.aspose.com/temporary-license/) untuk tujuan evaluasi.

**Q: Di mana saya dapat menemukan dokumentasi API yang detail?**  
A: Lihat [Aspose.CAD for Java documentation](https://reference.aspose.com/cad/java/) untuk tanda tangan metode lengkap dan contoh penggunaan.

**Q: Bagaimana cara menentukan layout mana yang akan diekspor?**  
A: Gunakan metode `setLayouts` pada `PdfExportOptions` dan berikan array nama layout, misalnya `new String[] {"Model", "Layout1"}`.

**Q: Bagaimana jika saya perlu batch‑convert banyak file DGN?**  
A: Bungkus langkah‑langkah tersebut dalam loop yang mengiterasi direktori berisi file DGN, menerapkan opsi ekspor yang sama pada setiap file.

---

**Last Updated:** 2026-06-19  
**Tested With:** Aspose.CAD untuk Java 24.10  
**Author:** Aspose  

{{< blocks/products/products-backtop-button >}}

## Tutorial Terkait

- [Ekspor DWG ke PDF dan Konversi Gambar CAD – Tutorial Aspose.CAD Java](/cad/java/cad-drawing-conversion/)
- [dwg ke pdf java – Ekspor CAD ke PDF dengan Aspose.CAD](/cad/java/cad-export-options/export-to-pdf/)
- [Ekspor Layout CAD ke PDF dengan Aspose.CAD untuk Java](/cad/java/cad-export-options/export-cad-layouts-to-pdf/)


{{< /blocks/products/pf/tutorial-page-section >}}
{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}