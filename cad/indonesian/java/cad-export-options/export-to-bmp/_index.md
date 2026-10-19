---
date: 2026-10-19
description: Pelajari cara mengonversi DWG ke BMP dan mengekspor CAD ke BMP secara
  efisien menggunakan Aspose.CAD for Java. Ikuti panduan langkah demi langkah kami
  untuk konversi yang tepat.
keywords:
- convert dwg to bmp
- how to convert dwg
- export cad to bmp
lastmod: 2026-10-19
linktitle: Ekspor ke BMP
og_description: Konversi DWG ke BMP menggunakan Aspose.CAD for Java. Panduan ini menunjukkan
  cara mengekspor CAD ke BMP dengan rasterization control, batch processing tips,
  dan performance benchmarks.
og_image_alt: Screenshot of Java code converting DWG to BMP with Aspose.CAD
og_title: Konversi DWG ke BMP dengan Aspose.CAD for Java – Ekspor Cepat dan Berkualitas
  Tinggi
schemas:
- author: Aspose
  dateModified: '2026-10-19'
  description: Learn how to convert DWG to BMP and export CAD to BMP efficiently using
    Aspose.CAD for Java. Follow our step‑by‑step guide for precise conversions.
  headline: Convert DWG to BMP with Aspose.CAD for Java
  type: TechArticle
- description: Learn how to convert DWG to BMP and export CAD to BMP efficiently using
    Aspose.CAD for Java. Follow our step‑by‑step guide for precise conversions.
  name: Convert DWG to BMP with Aspose.CAD for Java
  steps:
  - name: set the resource directory path
    text: Define the absolute path that points to the folder containing your source
      DWG file. > **Pro tip:** Use `System.getProperty("user.dir")` to build an absolute
      path that works across environments.
  - name: load the CAD file
    text: Load the CAD file into an Aspose.CAD `Image` object. The `Image` class reads
      the CAD file once, allowing you to reuse the same instance for multiple export
      formats (BMP, PNG, JPEG) without re‑reading the file from disk. > **Why this
      matters:** Loading the file once lets you reuse the `Image` instanc
  - name: configure BMP export options
    text: Create and configure BMP export options, including rasterization settings.
      `BmpOptions` tells Aspose.CAD to produce a BMP image and gives you access to
      the nested `RasterizationOptions` object where you set resolution, page dimensions,
      and layout. > **Tip:** You can also set `bmpOptions.setBitsPerPi
  - name: set rasterization parameters
    text: Define parameters such as page height, page width, and layout for rasterization.
      Specifying the layout (e.g., `"Model"` or `"Layout1"`) ensures the correct drawing
      view is rendered; omitting it may produce a blank bitmap for multi‑layout drawings.
      > **Common pitfall:** Forgetting to specify the layo
  - name: export to BMP
    text: 'Specify the output path and save the BMP file. Calling `image.save(outputPath,
      bmpOptions);` writes the rasterized bitmap to the target folder. The resulting
      `site.bmp` file can be embedded directly in HTML `<img>` tags, inserted into
      PDF reports, or processed further with standard image‑processing '
  type: HowTo
- questions:
  - answer: Yes. Change the file extension in `fileName` to `.dxf`, `.dwf`, etc.,
      and Aspose.CAD automatically selects the appropriate parser.
    question: Can I convert other CAD formats (e.g., DXF) to BMP with the same code?
  - answer: BMP does not support alpha transparency; for transparent output, export
      to PNG instead.
    question: Is it possible to set a transparent background for the BMP?
  - answer: Use a PDF library such as iText or Aspose.PDF, load the BMP as an image
      object, and add it to the PDF page with `document.add(image)`.
    question: How do I embed the generated BMP into a PDF report?
  - answer: Yes. Increase `rasterizationOptions.setResolution(600);` or higher to
      produce print‑ready BMP files without quality loss.
    question: Does the library support high‑resolution printing?
  - answer: Aspose offers perpetual, subscription, and temporary licenses. Contact
      sales for a custom quote that matches your deployment scale.
    question: What licensing options are available for commercial use?
  type: FAQPage
second_title: Aspose.CAD Java API
tags:
- convert dwg
- Aspose.CAD
- Java CAD conversion
title: Konversi DWG ke BMP dengan Aspose.CAD for Java
url: /id/java/cad-export-options/export-to-bmp/
weight: 12
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Mengonversi DWG ke BMP dengan Aspose.CAD untuk Java

## Pendahuluan

Dalam alur kerja rekayasa modern, kemampuan untuk **mengonversi DWG ke BMP** dengan cepat dan dapat diandalkan sangat penting untuk membuat thumbnail, dokumentasi, atau mengintegrasikan visual CAD ke dalam aplikasi web. Aspose.CAD untuk Java menyediakan API murni‑Java yang memungkinkan Anda **mengekspor CAD ke BMP** dengan kontrol penuh atas pengaturan rasterisasi, tanpa memerlukan DLL native apa pun. Pada tutorial ini Anda akan mempelajari cara menyiapkan pustaka, mengonfigurasi opsi ekspor, dan menangani jebakan umum sehingga Anda dapat menambahkan konversi DWG‑ke‑BMP ke proyek Java mana pun dengan percaya diri.

## Jawaban Cepat
- **Perpustakaan apa yang saya butuhkan?** Aspose.CAD untuk Java (versi percobaan gratis tersedia di [halaman percobaan gratis Aspose](https://releases.aspose.com/)).  
- **Format file apa yang didukung untuk konversi?** DWG, DWF, DXF, dan banyak format CAD lainnya dapat dikonversi ke BMP.  
- **Apakah saya memerlukan lisensi untuk pengembangan?** Lisensi sementara atau evaluasi cukup untuk pengujian; lisensi penuh diperlukan untuk produksi. Beli lisensi sementara dari [halaman pembelian lisensi sementara](https://purchase.aspose.com/temporary-license/).  
- **Berapa lama proses konversi?** Biasanya kurang dari satu detik untuk gambar berukuran standar pada perangkat keras modern.  
- **Bisakah saya memproses banyak file sekaligus?** Ya—cukup lakukan loop pada kode konversi untuk setiap file.  

Untuk dukungan komunitas, kunjungi [forum Aspose.CAD](https://forum.aspose.com/c/cad/19).

## Apa itu mengonversi DWG ke BMP?

Mengonversi DWG ke BMP mengubah gambar DWG berbasis vektor menjadi gambar BMP raster, memungkinkan tampilan di peramban, dokumen, atau alat pengeditan gambar. Konversi ini mempertahankan ketebalan garis, warna, dan lapisan sambil merender gambar pada resolusi yang ditentukan, menjadikannya ideal untuk thumbnail, laporan, atau skenario apa pun yang memerlukan representasi bitmap.

## Mengapa mengekspor CAD ke BMP dengan Aspose.CAD?

Mengekspor CAD ke BMP dengan Aspose.CAD memberikan **rasterisasi berfidelity tinggi** untuk lebih dari 50 + format input dan output, dan dapat memproses gambar beratus‑ratus halaman tanpa memuat seluruh file ke memori. Pustaka ini berjalan pada **semua runtime Java utama** (Java 8‑17) dan menghilangkan ketergantungan eksternal, yang mengurangi kompleksitas penyebaran hingga 80 %. Mesin rasterisasinya mendukung resolusi dari 72 DPI hingga 1200 DPI, memberi Anda kontrol presisi atas kualitas gambar untuk penggunaan web maupun cetak.

## Prasyarat

Sebelum masuk ke tutorial, pastikan Anda memiliki hal‑hal berikut:

- **Pustaka Aspose.CAD untuk Java** – unduh dari [halaman unduhan resmi Aspose.CAD untuk Java](https://releases.aspose.com/cad/java/).  
- **Lingkungan pengembangan Java** – JDK 8 atau lebih baru, dengan IDE pilihan Anda (IntelliJ, Eclipse, dll.).  
- **Pengetahuan dasar Java** – familiaritas dengan Maven/Gradle untuk manajemen dependensi akan mempercepat penyiapan.

## Impor namespace

Di file sumber Java Anda, impor kelas‑kelas yang menyediakan penanganan CAD dan kemampuan ekspor BMP:

Kelas `Image` adalah objek inti Aspose.CAD yang mewakili file CAD apa pun yang didukung dalam memori.  
`BmpOptions` menentukan format output dan pengaturan rasterisasi untuk file BMP.  
`RasterizationOptions` memungkinkan Anda menentukan ukuran halaman, resolusi, dan tata letak sebelum rendering.

```java
import com.aspose.cad.Image;
import com.aspose.cad.InterpolationMode;
import com.aspose.cad.SmoothingMode;
import com.aspose.cad.TextRenderingHint;

import com.aspose.cad.imageoptions.BmpOptions;
import com.aspose.cad.imageoptions.CadRasterizationOptions;
import com.aspose.cad.imageoptions.PdfOptions;
//import com.aspose.cad.imageoptions.TypeOfEntities;
```

## Cara mengonversi DWG ke BMP menggunakan Aspose.CAD untuk Java

Proses ini meliputi memuat file DWG sumber, mengonfigurasi opsi ekspor BMP—termasuk resolusi, ukuran halaman, dan tata letak—dan akhirnya menyimpan gambar yang telah dirasterisasi. Dengan mengikuti langkah‑langkah ini Anda dapat menghasilkan file BMP berkualitas tinggi secara andal untuk gambar tunggal atau batch besar, sambil menjaga penggunaan memori tetap rendah dan menghindari pembacaan file berulang.

### Langkah 1: atur jalur direktori sumber daya

Tentukan jalur absolut yang mengarah ke folder berisi file DWG sumber Anda.

```java
String dataDir = "Your Document Directory" + "ExportingCAD/";
```

> **Tip pro:** Gunakan `System.getProperty("user.dir")` untuk membangun jalur absolut yang berfungsi di semua lingkungan.

### Langkah 2: muat file CAD

Muat file CAD ke dalam objek `Image` Aspose.CAD.

Kelas `Image` membaca file CAD sekali, memungkinkan Anda menggunakan kembali instance yang sama untuk beberapa format ekspor (BMP, PNG, JPEG) tanpa harus membaca ulang file dari disk.

```java
String fileName = (dataDir + "site.dwf");
Image image = Image.load(fileName);
```

> **Mengapa ini penting:** Memuat file sekali memungkinkan Anda menggunakan kembali instance `Image` untuk berbagai format ekspor jika diperlukan.

### Langkah 3: konfigurasikan opsi ekspor BMP

Buat dan konfigurasikan opsi ekspor BMP, termasuk pengaturan rasterisasi.

`BmpOptions` memberi tahu Aspose.CAD untuk menghasilkan gambar BMP dan memberi Anda akses ke objek `RasterizationOptions` yang bersarang, tempat Anda mengatur resolusi, dimensi halaman, dan tata letak.

```java
BmpOptions bmpOptions = new BmpOptions();
CadRasterizationOptions rasterizationOptions = new CadRasterizationOptions();
bmpOptions.setVectorRasterizationOptions(rasterizationOptions);
```

> **Tip:** Anda juga dapat menetapkan `bmpOptions.setBitsPerPixel(24);` untuk mengontrol kedalaman warna.

### Langkah 4: atur parameter rasterisasi

Tentukan parameter seperti tinggi halaman, lebar halaman, dan tata letak untuk rasterisasi.

Menentukan tata letak (misalnya, `"Model"` atau `"Layout1"`) memastikan tampilan gambar yang tepat dirender; mengabaikannya dapat menghasilkan bitmap kosong untuk gambar dengan banyak tata letak.

```java
rasterizationOptions.setPageHeight(500);
rasterizationOptions.setPageWidth(500);
rasterizationOptions.setLayouts(new String[] { "Model" });
```

> **Jebakan umum:** Lupa menyebutkan tata letak dapat menghasilkan gambar kosong pada gambar dengan banyak tata letak.

### Langkah 5: ekspor ke BMP

Tentukan jalur output dan simpan file BMP.

Memanggil `image.save(outputPath, bmpOptions);` menulis bitmap yang telah dirasterisasi ke folder target. File `site.bmp` yang dihasilkan dapat disisipkan langsung dalam tag HTML `<img>`, dimasukkan ke dalam laporan PDF, atau diproses lebih lanjut dengan pustaka pemrosesan gambar standar.

```java
String outPath = dataDir + "site.bmp";
image.save(outPath, bmpOptions);
```

> **Hasil:** File `site.bmp` akan muncul di folder `ExportingCAD` Anda, siap digunakan dalam laporan, halaman web, atau pemrosesan gambar lanjutan.

Ulangi langkah‑langkah ini untuk setiap file CAD yang ingin Anda ekspor ke BMP menggunakan Aspose.CAD untuk Java.

## Masalah umum dan solusi

| Masalah | Penyebab | Solusi |
|-------|-------|----------|
| BMP kosong | Nama tata letak salah atau tata letak tidak disertakan | Pastikan nama tata letak cocok dengan file CAD sumber (misalnya, `"Model"`). |
| Gambar beresolusi rendah | DPI rasterisasi default terlalu rendah | Tetapkan `rasterizationOptions.setResolution(300);` untuk kualitas lebih tinggi. |
| OutOfMemoryError pada file besar | Heap JVM tidak cukup | Tingkatkan heap JVM (`-Xmx2g`) atau proses file dalam batch lebih kecil. |
| Banding warna | Menggunakan BMP 8‑bit alih‑alih 24‑bit | Tetapkan `bmpOptions.setBitsPerPixel(24);` untuk output true‑color. |
| Konversi batch lambat | Memuat pustaka untuk setiap file | Muat `Image` sekali per file dan gunakan kembali instance `BmpOptions` yang sama dalam batch. |

## Pertanyaan yang sering diajukan

**T: Bisakah saya mengonversi format CAD lain (misalnya DXF) ke BMP dengan kode yang sama?**  
J: Ya. Ubah ekstensi file pada `fileName` menjadi `.dxf`, `.dwf`, dll., dan Aspose.CAD secara otomatis memilih parser yang tepat.

**T: Apakah mungkin menetapkan latar belakang transparan untuk BMP?**  
J: BMP tidak mendukung transparansi alfa; untuk output transparan, ekspor ke PNG saja.

**T: Bagaimana cara menyisipkan BMP yang dihasilkan ke dalam laporan PDF?**  
J: Gunakan pustaka PDF seperti iText atau Aspose.PDF, muat BMP sebagai objek gambar, dan tambahkan ke halaman PDF dengan `document.add(image)`.

**T: Apakah pustaka ini mendukung pencetakan beresolusi tinggi?**  
J: Ya. Tingkatkan `rasterizationOptions.setResolution(600);` atau lebih tinggi untuk menghasilkan file BMP siap cetak tanpa kehilangan kualitas.

**T: Opsi lisensi apa yang tersedia untuk penggunaan komersial?**  
J: Aspose menawarkan lisensi perpetual, berlangganan, dan sementara. Hubungi tim penjualan untuk penawaran khusus yang sesuai dengan skala penyebaran Anda.

## Tips tambahan dan praktik terbaik

- **Pemrosesan batch:** Bungkus langkah konversi dalam loop `for` yang mengiterasi direktori berisi file DWG. Gunakan kembali satu instance `BmpOptions` untuk meminimalkan overhead pembuatan objek.  
- **Manajemen memori:** Panggil `image.dispose();` setelah setiap penyimpanan untuk membebaskan sumber daya native secara cepat, terutama saat memproses batch besar.  
- **Optimasi kinerja:** Untuk gambar dengan banyak lapisan, nonaktifkan lapisan yang tidak diperlukan melalui `rasterizationOptions.getLayers().clear();` lalu tambahkan hanya lapisan yang Anda butuhkan. Ini dapat mengurangi waktu pemrosesan hingga 40 %.  
- **Konvensi penamaan file:** Tambahkan resolusi ke nama file output (misalnya, `drawing_300dpi.bmp`) agar lebih mudah melacak kualitas aset dalam alur kerja downstream.

## Kesimpulan

Mengekspor file CAD ke format BMP sangat sederhana dengan Aspose.CAD untuk Java. Dengan mengikuti panduan langkah‑demi‑langkah ini, Anda dapat dengan mulus mengintegrasikan fungsi **mengonversi DWG ke BMP** ke dalam aplikasi Java Anda, memastikan output raster yang efisien dan berkualitas tinggi untuk setiap alur kerja rekayasa. Jelajahi opsi ekspor lain dari pustaka ini—seperti PNG, JPEG, dan TIFF—untuk membangun pipeline konversi CAD‑ke‑gambar yang lengkap.

---

**Terakhir Diperbarui:** 2026-10-19  
**Diuji Dengan:** Aspose.CAD untuk Java 24.11 (terbaru pada saat penulisan)  
**Penulis:** Aspose

## Tutorial Terkait

- [Ekspor DWG ke BMP dan Sesuaikan Ukuran CAD Menggunakan Tipe Unit dengan Aspose.CAD untuk Java](/cad/java/cad-file-manipulation/adjusting-cad-drawing-size-using-unit-type/)
- [Sesuaikan Ukuran Gambar CAD Secara Otomatis dan Konversi DWG ke BMP dengan Aspose.CAD untuk Java](/cad/java/cad-file-manipulation/auto-adjusting-cad-drawing-size/)
- [Konversi DWG ke PNG – Simpan CAD sebagai PNG Menggunakan Aspose.CAD untuk Java](/cad/java/cad-drawing-conversion/convert-cad-drawing-to-raster-image/)


{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}