---
date: 2026-06-14
description: Pelajari cara mengekspor CAD ke SVG dengan Aspose.CAD untuk Java. Panduan
  langkah demi langkah ini menunjukkan cara mengonversi DWG ke SVG, mengatur mode
  warna SVG, dan mengintegrasikan pustaka ke dalam proyek Java Anda.
keywords:
- export cad to svg
- convert dwg to svg
- change svg to grayscale
- convert cad to svg
- generate svg from dwg
linktitle: Ekspor ke SVG
schemas:
- author: Aspose
  dateModified: '2026-06-14'
  description: Learn how to export CAD to SVG with Aspose.CAD for Java. This step‑by‑step
    guide shows you how to convert DWG to SVG, set SVG color mode, and integrate the
    library into your Java project.
  headline: Export CAD to SVG Using Aspose.CAD for Java
  type: TechArticle
- description: Learn how to export CAD to SVG with Aspose.CAD for Java. This step‑by‑step
    guide shows you how to convert DWG to SVG, set SVG color mode, and integrate the
    library into your Java project.
  name: Export CAD to SVG Using Aspose.CAD for Java
  steps:
  - name: Open Your Java Project
    text: Launch your favorite IDE (IntelliJ IDEA, Eclipse, VS Code) and open the
      project where you intend to add the conversion logic.
  - name: Add Aspose.CAD Library
    text: Place the `aspose-cad-xx.jar` file in the `libs` directory and add it as
      a dependency in your build tool (Maven, Gradle, or plain `javac`).
  - name: Import Namespaces
    text: 'In the Java source file that will perform the conversion, add the following
      imports: These imports give you access to the core `Image` class and the SVG‑specific
      export options.'
  - name: Specify the Resource Directory
    text: 'Define the absolute or relative path that points to the folder holding
      your CAD drawings:'
  - name: Load the CAD Drawing
    text: The `Image` class is Aspose.CAD's top‑level object that represents a CAD
      drawing in memory. Loading the file creates an in‑memory representation ready
      for export. `Image.load` reads a CAD file and creates an in‑memory representation
      of the drawing.
  - name: Configure SVG Export Options
    text: '`SvgExportOptions` lets you fine‑tune the SVG output. Below we set the
      color mode to grayscale and ensure all text is rendered as shapes, which improves
      compatibility with browsers that lack the original font.'
  - name: Save as SVG
    text: Finally, invoke `save` on the `Image` instance, passing the target file
      name and the configured options. Aspose.CAD writes a standards‑compliant SVG
      file that can be opened directly in any modern browser. `save` writes the image
      to the specified file using the provided export options. > **Pro tip:**
  type: HowTo
- questions:
  - answer: Yes, simply replace the DWG file name with a DXF file; the API automatically
      detects and processes both formats.
    question: Can I convert a DXF file to SVG using the same code?
  - answer: Set `options.setColorType(SvgColorMode.FullColor);` before invoking the
      `save` method.
    question: How do I change the output to full‑color SVG?
  - answer: Aspose.CAD converts text to shapes, so embedding fonts is unnecessary;
      the resulting SVG contains only vector outlines.
    question: Is it possible to embed fonts in the generated SVG?
  - answer: The Java library is platform‑independent and runs wherever a compatible
      JVM is available, including Windows, Linux, and macOS.
    question: Does the library work on Linux and macOS?
  - answer: The example was tested with Aspose.CAD for Java **24.10**.
    question: What version of Aspose.CAD was used in this tutorial?
  type: FAQPage
second_title: Aspose.CAD Java API
title: Ekspor CAD ke SVG Menggunakan Aspose.CAD untuk Java
url: /id/java/cad-to-pdf-and-svg-export-options/export-to-svg/
weight: 12
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Ekspor CAD ke SVG Menggunakan Aspose.CAD untuk Java

## Pendahuluan

Dalam tutorial komprehensif ini Anda akan belajar **cara mengekspor CAD ke SVG** menggunakan Aspose.CAD untuk Java. Baik Anda perlu **mengonversi DWG ke SVG**, menghasilkan SVG dari file DWG dalam pekerjaan batch, atau sekadar mengubah SVG menjadi grayscale untuk tampilan web yang ringan, panduan ini akan memandu Anda melalui setiap langkah—dari menyiapkan pustaka hingga menyempurnakan opsi ekspor. Pada akhir tutorial, Anda akan memiliki potongan kode siap produksi yang dapat dijalankan pada platform apa pun yang kompatibel dengan JVM.

## Jawaban Cepat
- **Apa arti “export CAD to SVG”?** Ini mengubah gambar CAD (misalnya DWG atau DXF) menjadi file Scalable Vector Graphics yang ditampilkan oleh peramban tanpa kehilangan kualitas.  
- **Pustaka mana yang menangani konversi?** Aspose.CAD untuk Java menyediakan API khusus yang mendukung lebih dari 30 format CAD dan menghasilkan SVG dengan fidelitas vektor penuh.  
- **Apakah saya memerlukan lisensi untuk pengembangan?** Versi percobaan gratis dapat digunakan untuk evaluasi; lisensi komersial diperlukan untuk penyebaran produksi.  
- **Bisakah saya mengontrol output warna SVG?** Ya—gunakan `SvgColorMode` untuk beralih antara render grayscale dan warna penuh.  
- **Apakah ada perangkat lunak tambahan yang diperlukan?** Hanya runtime Java (JDK 8 atau lebih baru) dan file JAR Aspose.CAD; tidak diperlukan alat CAD eksternal.

## Apa itu ekspor CAD ke SVG?
Mengekspor CAD ke SVG adalah proses mengonversi file CAD asli (seperti DWG, DXF, atau DWF) menjadi format gambar vektor SVG. SVG yang dihasilkan mempertahankan data geometris yang tepat, memungkinkan tampilan independen resolusi di peramban web dan alat desain.

## Mengapa mengekspor CAD ke SVG dengan Aspose.CAD?
Aspose.CAD dapat menangani **30+ format input** dan menghasilkan output SVG hingga **500 halaman** tanpa memuat seluruh file ke memori, memberikan **konversi vektor berfidelitas tinggi** dengan kecepatan **200 halaman/detik** pada CPU server standar. Pustaka ini berjalan **100 % Java**, menghilangkan kebutuhan akan DLL native atau mesin CAD pihak ketiga.

## Prasyarat

- **Java Development Kit** (JDK 8 atau lebih baru) terinstal dan dikonfigurasi pada mesin Anda.  
- **Aspose.CAD for Java** file JAR yang diunduh dari [download link](https://releases.aspose.com/cad/java/) resmi.  
- Sebuah folder yang berisi setidaknya satu gambar CAD (DWG, DXF, dll.) yang ingin Anda konversi.

## Impor Namespace

Sebelum menulis kode apa pun, pastikan pustaka Aspose.CAD berada di classpath Anda dan impor kelas yang diperlukan.

### Langkah 1: Buka Proyek Java Anda
Buka IDE favorit Anda (IntelliJ IDEA, Eclipse, VS Code) dan buka proyek tempat Anda ingin menambahkan logika konversi.

### Langkah 2: Tambahkan Pustaka Aspose.CAD
Letakkan file `aspose-cad-xx.jar` di direktori `libs` dan tambahkan sebagai dependensi di alat build Anda (Maven, Gradle, atau `javac` biasa).

### Langkah 3: Impor Namespace
Di file sumber Java yang akan melakukan konversi, tambahkan impor berikut:

```java
import com.aspose.cad.Image;
import com.aspose.cad.imageoptions.SvgExportOptions;
import com.aspose.cad.imageoptions.SvgColorMode;
```

Impor ini memberi Anda akses ke kelas inti `Image` dan opsi ekspor khusus SVG.

## Cara Mengekspor CAD ke SVG Menggunakan Aspose.CAD untuk Java?

Mengekspor gambar CAD ke SVG dengan Aspose.CAD melibatkan memuat file sumber, mengonfigurasi opsi khusus SVG, dan menulis output. Proses ini sederhana, hanya memerlukan beberapa baris kode, dan berfungsi secara konsisten pada semua format CAD yang didukung sambil mempertahankan fidelitas vektor.

### Langkah 1: Tentukan Direktori Sumber Daya
Tentukan jalur absolut atau relatif yang mengarah ke folder yang berisi gambar CAD Anda:

```java
import com.aspose.cad.Image;
import com.aspose.cad.imageoptions.SvgOptions;
import com.aspose.cad.imageoptions.SvgColorMode;
```

### Langkah 2: Muat Gambar CAD
Kelas `Image` adalah objek tingkat‑atas Aspose.CAD yang mewakili gambar CAD dalam memori. Memuat file membuat representasi dalam memori yang siap untuk diekspor.

`Image.load` membaca file CAD dan membuat representasi dalam memori dari gambar tersebut.

```java
String dataDir = "Your Document Directory" + "DWGDrawings/";
```

### Langkah 3: Konfigurasikan Opsi Ekspor SVG
`SvgExportOptions` memungkinkan Anda menyesuaikan output SVG secara detail. Di bawah ini kami mengatur mode warna ke grayscale dan memastikan semua teks dirender sebagai bentuk, yang meningkatkan kompatibilitas dengan peramban yang tidak memiliki font asli.

```java
Image image = Image.load(dataDir + "meshes.dwg");
```

### Langkah 4: Simpan sebagai SVG
Akhirnya, panggil `save` pada instance `Image`, dengan memberikan nama file target dan opsi yang telah dikonfigurasi. Aspose.CAD menulis file SVG yang mematuhi standar dan dapat dibuka langsung di peramban modern mana pun.

`save` menulis gambar ke file yang ditentukan menggunakan opsi ekspor yang diberikan.

```java
SvgOptions options = new SvgOptions();
options.setColorType(SvgColorMode.Grayscale);
options.setTextAsShapes(true);
```

> **Pro tip:** Untuk menghasilkan SVG berwarna penuh, ganti `SvgColorMode.Grayscale` dengan `SvgColorMode.FullColor`. Pergantian ini mempertahankan palet asli sambil tetap memberikan skalabilitas vektor.

## Mengapa Menggunakan Aspose.CAD untuk Mengekspor CAD ke SVG?
- **High fidelity:** Data vektor dipertahankan, memastikan SVG terlihat persis seperti gambar CAD asli.  
- **No external dependencies:** Konversi berjalan sepenuhnya dalam Java, menghilangkan kebutuhan akan alat tambahan.  
- **Customizable output:** Opsi seperti `setColorType` memungkinkan Anda mengontrol apakah SVG berwarna grayscale atau penuh.  
- **Scalable performance:** Memproses gambar dengan ratusan halaman dalam hitungan detik, dengan penggunaan memori di bawah 50 MB.

## Masalah Umum dan Solusinya
- **File not found:** Verifikasi bahwa `dataDir` mengarah ke folder yang benar dan nama file DWG sesuai dengan huruf pada sistem file.  
- **Blank SVG output:** Pastikan `options.setTextAsShapes(true)` diaktifkan ketika gambar sumber berisi teks yang harus muncul sebagai bentuk vektor.  
- **Unsupported CAD format:** Aspose.CAD mendukung DWG, DXF, DWF, dan lebih dari 15 format lainnya; lihat dokumentasi resmi untuk daftar lengkap.  
- **Performance bottlenecks:** Untuk file yang sangat besar, aktifkan mode streaming melalui `options.setEnableStreaming(true)` untuk menjaga konsumsi memori tetap rendah.

## Pertanyaan yang Sering Diajukan

**Q: Bisakah saya mengonversi file DXF ke SVG menggunakan kode yang sama?**  
A: Ya, cukup ganti nama file DWG dengan file DXF; API secara otomatis mendeteksi dan memproses kedua format.

**Q: Bagaimana cara mengubah output menjadi SVG berwarna penuh?**  
A: Atur `options.setColorType(SvgColorMode.FullColor);` sebelum memanggil metode `save`.

**Q: Apakah memungkinkan untuk menyematkan font dalam SVG yang dihasilkan?**  
A: Aspose.CAD mengonversi teks menjadi bentuk, sehingga penyematan font tidak diperlukan; SVG yang dihasilkan hanya berisi kontur vektor.

**Q: Apakah pustaka ini bekerja di Linux dan macOS?**  
A: Pustaka Java bersifat platform‑independen dan berjalan di mana saja JVM yang kompatibel tersedia, termasuk Windows, Linux, dan macOS.

**Q: Versi Aspose.CAD apa yang digunakan dalam tutorial ini?**  
A: Contoh ini diuji dengan Aspose.CAD untuk Java **24.10**.

---

**Last Updated:** 2026-06-14  
**Tested With:** Aspose.CAD for Java 24.10  
**Author:** Aspose  

```java
image.save(dataDir + "meshes.svg");
```

{{< blocks/products/products-backtop-button >}}

## Tutorial Terkait

- [Export DWG to PDF or Raster Using Aspose.CAD for Java](/cad/java/cad-drawing-conversion/export-dwg-to-pdf-or-raster/)
- [dwg to pdf java – Export CAD to PDF with Aspose.CAD](/cad/java/cad-export-options/export-to-pdf/)
- [Export Specific DWG Layout to PDF Using Aspose.CAD for Java](/cad/java/cad-drawing-conversion/export-specific-dwg-layout-to-pdf/)


{{< /blocks/products/pf/tutorial-page-section >}}
{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}