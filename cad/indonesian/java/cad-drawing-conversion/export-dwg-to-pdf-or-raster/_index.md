---
date: 2026-10-14
description: Pelajari cara perpustakaan CAD Java Aspose.CAD untuk Java dapat mengekspor
  DWG ke PDF atau gambar raster dengan cepat dan akurat.
keywords:
- export dwg pdf
- high quality pdf
- dwg to pdf tutorial
- aspose cad java
- java cad library
lastmod: 2026-10-14
linktitle: Ekspor DWG PDF dan gambar raster
og_description: Ekspor DWG PDF dengan cepat menggunakan Aspose.CAD untuk Java. Pelajari
  konversi PDF berkualitas tinggi, opsi raster, dan lisensi dalam panduan langkah
  demi langkah ini.
og_image_alt: Tutorial showing Java code to convert DWG drawings to PDF and raster
  formats with Aspose.CAD
og_title: Ekspor DWG PDF dan gambar raster menggunakan perpustakaan CAD Java Aspose.CAD
schemas:
- author: Aspose
  dateModified: '2026-10-14'
  description: Learn how the Java CAD library Aspose.CAD for Java can export DWG to
    PDF or raster images quickly and accurately.
  headline: Export DWG PDF and raster images using Java CAD library Aspose.CAD
  type: TechArticle
- description: Learn how the Java CAD library Aspose.CAD for Java can export DWG to
    PDF or raster images quickly and accurately.
  name: Export DWG PDF and raster images using Java CAD library Aspose.CAD
  steps:
  - name: Load the DWG file
    text: First, load your DWG drawing using the `Image` class. This creates an in‑memory
      representation that Aspose.CAD can work with.
  - name: Determine unit type
    text: Understanding whether the drawing uses metric or imperial units is essential
      for correct scaling. The helper method `IsMetric` (implementation omitted for
      brevity) returns a boolean flag.
  - name: Set rasterization options
    text: The `CadRasterizationOptions` class defines rasterization parameters such
      as DPI, page size, and unit conversion. Based on the unit system, configure
      page size, scaling, and the target unit type. These options drive how the DWG
      is rasterized before being wrapped into a PDF.
  - name: Configure PDF options (pdf options cad)
    text: The `PdfOptions` class specifies PDF‑specific settings, including compression
      and metadata. Create a `PdfOptions` instance and attach the rasterization settings.
      This tells Aspose.CAD how to embed the rasterized content into the final PDF.
  - name: Save as PDF
    text: The `save` method writes the image to the given file path using the supplied
      options. Finally, export the drawing to a PDF file. The `save` method takes
      the output path and the configured `PdfOptions`. When the code finishes, you’ll
      find **Saved.pdf** in your `DWGDrawings` folder, ready for distribu
  type: HowTo
- questions:
  - answer: Yes, Aspose.CAD for Java seamlessly integrates with popular Java frameworks
      such as Spring, Jakarta EE, and Android.
    question: Can I use Aspose.CAD for Java with other Java frameworks?
  - answer: Yes, you can obtain a temporary license **[obtain a temporary license](https://purchase.aspose.com/temporary-license/)**.
    question: Is a temporary license available for Aspose.CAD for Java?
  - answer: Visit the **[Aspose.CAD forum](https://forum.aspose.com/c/cad/19)** for
      assistance from the community and Aspose engineers.
    question: Where can I find support for Aspose.CAD for Java?
  - answer: You can purchase a license **[purchase a license](https://purchase.aspose.com/buy)**.
    question: How can I purchase a license for Aspose.CAD for Java?
  - answer: Aspose.CAD for Java supports both metric and imperial units, automatically
      detecting the drawing’s unit system.
    question: What units does Aspose.CAD for Java support?
  type: FAQPage
second_title: Aspose.CAD Java API
tags:
- export dwg
- aspose.cad
- java cad conversion
title: Ekspor DWG PDF dan gambar raster menggunakan perpustakaan CAD Java Aspose.CAD
url: /id/java/cad-drawing-conversion/export-dwg-to-pdf-or-raster/
weight: 13
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Ekspor DWG PDF dan gambar raster menggunakan perpustakaan CAD Java Aspose.CAD

## Pendahuluan

Mengekspor DWG ke PDF adalah kebutuhan yang sering muncul bagi insinyur, arsitek, dan siapa saja yang perlu berbagi gambar CAD tanpa mengungkapkan format file asli. Dengan **Aspose.CAD for Java**, Anda dapat **export dwg pdf** — atau gambar raster — hanya dengan beberapa baris kode Java, menjaga kesetiaan vektor dan presisi tata letak. Tutorial ini memandu Anda melalui proses memuat file DWG, mengonfigurasi rasterisasi, dan menyimpan hasilnya sebagai PDF atau gambar berkualitas tinggi. Anda juga akan melihat mengapa Aspose.CAD menjadi perpustakaan CAD Java pilihan utama untuk konversi yang andal dan lintas‑platform.

Untuk panduan khusus hanya konversi PDF, lihat [Tutorial Ekspor DWG ke PDF](/java/cad-drawing-conversion/export-dwg-to-pdf/).

## Jawaban Cepat
- **Apa yang dibahas dalam tutorial ini?** Mengekspor file DWG ke PDF atau gambar raster menggunakan Aspose.CAD for Java.  
- **Apakah saya memerlukan lisensi?** Lisensi sementara gratis tersedia untuk evaluasi; lisensi penuh diperlukan untuk produksi.  
- **Versi Java mana yang didukung?** Semua runtime Java 8+ dapat bekerja dengan API Aspose.CAD Java terbaru.  
- **Bisakah saya mengonversi DWG ke format gambar lain?** Ya – opsi rasterisasi yang sama memungkinkan Anda menghasilkan PNG, JPEG, BMP, dll.  
- **Berapa lama proses konversi berlangsung?** Biasanya kurang dari satu detik untuk gambar standar; file yang lebih besar mungkin memerlukan beberapa detik.

## Mengapa perpustakaan CAD Java adalah pilihan terbaik untuk konversi DWG?

Aspose.CAD for Java adalah pilihan terbaik karena menyediakan implementasi murni‑Java yang tidak memerlukan DLL native, secara otomatis mendeteksi satuan metrik atau imperial, menghasilkan output raster hingga 1200 DPI, dan menghasilkan PDF yang mempertahankan vektor tanpa ketergantungan eksternal. Perpustakaan ini juga menawarkan model lisensi fleksibel yang memungkinkan Anda memulai dengan lisensi sementara dan meningkatkan ke penggunaan perusahaan.

## Apa itu “export dwg to pdf”?

`Export dwg pdf` adalah proses mengubah file gambar DWG asli menjadi dokumen PDF sambil mempertahankan data vektor, lapisan, dan skala. Konversi ini menghasilkan file yang tidak bergantung pada perangkat sehingga dapat dilihat di platform apa pun tanpa memerlukan AutoCAD. Karena PDF menyimpan informasi vektor, teks tetap dapat dicari dan grafik tetap tajam pada semua tingkat zoom, menjadikannya ideal untuk dokumentasi, tinjauan klien, dan penyimpanan arsip.

## Mengapa menggunakan Aspose.CAD Java untuk konversi ini?

Anda sebaiknya menggunakan Aspose.CAD Java karena perpustakaan ini menangani konversi satuan, rasterisasi, dan penyematan PDF secara internal, menghilangkan kebutuhan akan alat pihak ketiga atau pipeline baris perintah yang rumit. API‑nya dirancang untuk pengembang: satu objek `Image` mewakili gambar, dan beberapa objek konfigurasi memungkinkan Anda menyesuaikan DPI, ukuran halaman, dan kompresi. Hasilnya adalah output yang konsisten dan dapat diulang di lingkungan Windows, Linux, dan macOS.

## Prasyarat

Sebelum masuk ke kode, pastikan Anda memiliki:

- Pengetahuan dasar tentang pemrograman Java.  
- Perpustakaan Aspose.CAD for Java terpasang. Jika Anda belum mengunduhnya, dapatkan **[unduh Aspose.CAD for Java](https://releases.aspose.com/cad/java/)**.  
- File DWG untuk pengujian – contoh **Bottom_plate.dwg** digunakan dalam panduan ini.  

## Impor namespace

Di proyek Java Anda, impor kelas yang diperlukan untuk memulai konversi:

```java
import com.aspose.cad.Image;

import com.aspose.cad.imageoptions.CadRasterizationOptions;
import com.aspose.cad.imageoptions.PdfOptions;
import com.aspose.cad.imageoptions.UnitType;
```

## Panduan langkah demi langkah

### Langkah 1: Muat file DWG

Pertama, muat gambar DWG Anda menggunakan kelas `Image`. Ini membuat representasi dalam memori yang dapat diproses oleh Aspose.CAD.

```java
String dataDir = "Your Document Directory" + "DWGDrawings/";
String srcFile = dataDir + "Bottom_plate.dwg";
Image objImage = Image.load(srcFile);
```

### Langkah 2: Tentukan jenis unit

Memahami apakah gambar menggunakan satuan metrik atau imperial sangat penting untuk skala yang tepat. Metode bantu `IsMetric` (implementasi dihilangkan untuk singkat) mengembalikan nilai boolean.

```java
Boolean currentUnitIsMetric = IsMetric(objImage.getUnitType());
int currentUnitCoefficient = objImage.getUnitType();
```

### Langkah 3: Atur opsi rasterisasi

Kelas `CadRasterizationOptions` mendefinisikan parameter rasterisasi seperti DPI, ukuran halaman, dan konversi satuan. Berdasarkan sistem satuan, konfigurasikan ukuran halaman, skala, dan tipe satuan target. Opsi‑opsi ini menentukan bagaimana DWG dirasterisasi sebelum dibungkus ke dalam PDF.

```java
CadRasterizationOptions rasterizationOptions = new CadRasterizationOptions();

if (currentUnitIsMetric) {
    // Metric units
    double metersCoeff = 1 / 1000.0;
    double scaleFactor = metersCoeff / currentUnitCoefficient;
    rasterizationOptions.setPageWidth((float)(210 * scaleFactor));
    rasterizationOptions.setPageHeight((float)(297 * scaleFactor));
    rasterizationOptions.setUnitType(UnitType.Millimeter);
} else {
    // Imperial units
    rasterizationOptions.setPageWidth((float)(8.27f / currentUnitCoefficient));
    rasterizationOptions.setPageHeight((float)(11.69f / currentUnitCoefficient));
    rasterizationOptions.setUnitType(UnitType.Inch);
}
```

### Langkah 4: Konfigurasikan opsi PDF (pdf options cad)

Kelas `PdfOptions` menentukan pengaturan khusus PDF, termasuk kompresi dan metadata. Buat instance `PdfOptions` dan lampirkan pengaturan rasterisasi. Ini memberi tahu Aspose.CAD cara menyematkan konten raster ke PDF akhir.

```java
PdfOptions pdfOptions = new PdfOptions();
pdfOptions.setVectorRasterizationOptions(new CadRasterizationOptions());
```

### Langkah 5: Simpan sebagai PDF

Metode `save` menulis gambar ke jalur file yang diberikan menggunakan opsi yang disediakan. Akhirnya, ekspor gambar ke file PDF. Metode `save` menerima jalur output dan `PdfOptions` yang telah dikonfigurasi.

```java
objImage.save(dataDir + "Saved.pdf", pdfOptions);
```

Setelah kode selesai, Anda akan menemukan **Saved.pdf** di folder `DWGDrawings` Anda, siap untuk distribusi atau pengarsipan.

## Bagaimana cara mengonversi gambar raster DWG dengan perpustakaan CAD Java?

Anda dapat mengonversi DWG ke format raster dengan mengganti `PdfOptions` dengan kelas opsi khusus raster seperti `PngOptions` atau `JpegOptions`. Gunakan kembali instance `CadRasterizationOptions` yang sama, sesuaikan format output, dan panggil metode `save` dengan objek opsi baru. Pendekatan ini memungkinkan Anda menghasilkan PNG, JPEG, BMP, atau TIFF dengan satu perubahan baris, menjaga alur kerja tetap konsisten.

## Bagaimana cara menghasilkan PDF DWG menggunakan opsi PDF CAD?

Contoh di atas sudah **menghasilkan pdf dwg**. Untuk menyempurnakan ukuran PDF, aktifkan kompresi dengan memanggil `pdfOptions.setCompress(true)`. Anda juga dapat menyematkan metadata khusus, mengatur versi PDF, atau menambahkan perlindungan kata sandi melalui properti tambahan `PdfOptions`. Penyesuaian ini memberi Anda kontrol penuh atas PDF akhir tanpa meninggalkan basis kode Java.

## Masalah umum & tips

- **Ukuran halaman tidak tepat** – Periksa kembali logika konversi satuan; koefisien yang tidak cocok dapat menghasilkan halaman terlalu besar.  
- **Font atau lineweight hilang** – Pastikan DWG merujuk ke semua sumber eksternal sebelum konversi.  
- **Kinerja pada gambar besar** – Tingkatkan pengaturan `DPI` di `CadRasterizationOptions` hanya ketika kualitas lebih tinggi diperlukan; DPI lebih rendah mempercepat pemrosesan.  
- **Masalah lisensi** – Untuk evaluasi Anda dapat menggunakan **lisensi sementara Aspose**; lisensi penuh diperlukan untuk penerapan produksi.

## Pertanyaan yang sering diajukan

**Q: Bisakah saya menggunakan Aspose.CAD for Java dengan kerangka kerja Java lain?**  
A: Ya, Aspose.CAD for Java terintegrasi mulus dengan kerangka kerja Java populer seperti Spring, Jakarta EE, dan Android.

**Q: Apakah lisensi sementara tersedia untuk Aspose.CAD for Java?**  
A: Ya, Anda dapat memperoleh lisensi sementara **[peroleh lisensi sementara](https://purchase.aspose.com/temporary-license/)**.

**Q: Di mana saya dapat menemukan dukungan untuk Aspose.CAD for Java?**  
A: Kunjungi **[forum Aspose.CAD](https://forum.aspose.com/c/cad/19)** untuk bantuan dari komunitas dan insinyur Aspose.

**Q: Bagaimana cara membeli lisensi untuk Aspose.CAD for Java?**  
A: Anda dapat membeli lisensi **[beli lisensi](https://purchase.aspose.com/buy)**.

**Q: Satuan apa yang didukung oleh Aspose.CAD for Java?**  
A: Aspose.CAD for Java mendukung satuan metrik dan imperial, secara otomatis mendeteksi sistem satuan gambar.

**Q: Bisakah saya mengonversi DWG ke format gambar lain (mis., PNG, JPEG) menggunakan API yang sama?**  
A: Tentu saja. Ganti `PdfOptions` dengan opsi gambar raster yang sesuai (mis., `PngOptions`) dan gunakan kembali `CadRasterizationOptions` yang sama.

## Kesimpulan

Tutorial ini menunjukkan cara **export dwg pdf** dan gambar raster menggunakan **perpustakaan cad java** Aspose.CAD for Java. Dengan mengikuti panduan langkah demi langkah, Anda dapat mengintegrasikan konversi CAD yang andal ke dalam aplikasi Java apa pun, baik Anda memerlukan PDF untuk dokumentasi atau gambar raster untuk tampilan web. Sifat murni‑Java perpustakaan, output berkualitas tinggi, dan lisensi yang fleksibel menjadikannya pilihan solid untuk utilitas kecil maupun pipeline perusahaan berskala besar.

---

**Last Updated:** 2026-10-14  
**Tested With:** Aspose.CAD for Java 24.10  
**Author:** Aspose

## Tutorial Terkait

- [Ekspor DWG ke PDF: Tata Letak Spesifik Menggunakan Aspose.CAD for Java](/cad/java/cad-drawing-conversion/export-specific-dwg-layout-to-pdf/)
- [Ekspor DWG ke PDF di Java – Atur Ukuran Halaman PDF dengan Aspose.CAD](/cad/java/cad-export-options/export-to-pdf/)
- [Ekspor DWG ke PDF dengan Garis Tersembunyi – Aspose.CAD for Java](/cad/java/cad-text-and-formatting/support-hidden-lines-in-dwg/)


{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}