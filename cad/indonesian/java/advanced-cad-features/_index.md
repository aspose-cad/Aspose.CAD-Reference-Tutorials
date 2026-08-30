---
date: 2026-06-24
description: Pelajari cara mengonversi CAD ke PDF, mengatur ukuran kanvas, mengekstrak
  atribut blok, mengatur warna latar belakang CAD, dan menerapkan skala tata letak
  otomatis menggunakan Aspose.CAD untuk Java.
keywords:
- convert cad to pdf
- set canvas size java
- set cad background color
linktitle: Atur Ukuran Kanvas – Fitur CAD Lanjutan
schemas:
- author: Aspose
  dateModified: '2026-06-24'
  description: Learn how to convert CAD to PDF, set canvas size, extract block attributes,
    set CAD background color, and apply auto layout scaling using Aspose.CAD for Java.
  headline: Convert CAD to PDF – Set Canvas Size and Advanced Features with Aspose.CAD
    for Java
  type: TechArticle
- questions:
  - answer: Yes. Loop through your collection of CAD files, configure the canvas size
      on each `ImageOptions` instance, and save the output programmatically.
    question: Can I set a custom canvas size for every file in a batch process?
  - answer: The quality is determined by the DPI setting in the rendering options.
      You can increase DPI while keeping the canvas dimensions to get higher‑resolution
      PDFs.
    question: Does setting the canvas size affect the quality of the exported PDF?
  - answer: Use the `ExternalReference` collection to resolve the reference, then
      iterate over its `BlockReference` objects to read attribute values.
    question: How do I extract block attribute values from a DWG that contains external
      references?
  - answer: Yes. The scaling logic works for both raster (PNG, TIFF) and vector (PDF,
      SVG) outputs, ensuring the drawing fits the canvas.
    question: Is auto layout scaling compatible with vector output formats like PDF?
  - answer: A paid Aspose.CAD license is required for production deployments. A free
      evaluation license can be used for development and testing.
    question: What licensing is required for commercial use?
  type: FAQPage
second_title: Aspose.CAD Java API
title: Konversi CAD ke PDF – Atur Ukuran Kanvas dan Fitur Lanjutan dengan Aspose.CAD
  untuk Java
url: /id/java/advanced-cad-features/
weight: 24
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Konversi CAD ke PDF – Atur Ukuran Kanvas dan Fitur Lanjutan dengan Aspose.CAD untuk Java

## Pendahuluan

Jika Anda ingin **mengonversi CAD ke PDF** sekaligus **mengatur ukuran kanvas** di Java, Anda berada di tempat yang tepat. Aspose.CAD untuk Java tidak hanya memungkinkan Anda mengontrol dimensi kanvas tetapi juga menawarkan serangkaian kemampuan lanjutan seperti **mengekstrak nilai atribut blok**, **mengatur warna latar belakang CAD**, dan menerapkan **skala tata letak otomatis**. Dalam panduan ini kami akan membahas topik utama, menjelaskan mengapa hal tersebut penting, dan mengarahkan Anda ke tutorial terperinci yang menyelami setiap fitur.

## Jawaban Cepat
- **Apa yang dilakukan “set canvas size”?** Ini menentukan lebar dan tinggi tepat dari gambar atau PDF output, memberi Anda kontrol presisi atas area render akhir.  
- **Apakah saya dapat mengonversi CAD ke PDF setelah mengatur ukuran kanvas?** Ya—Aspose.CAD memungkinkan Anda mengonversi file CAD ke PDF sambil mempertahankan dimensi kanvas yang Anda tentukan.  
- **Apakah ekstraksi nilai atribut blok didukung?** Tentu saja; API menyediakan metode untuk membaca nilai atribut dari referensi eksternal.  
- **Bagaimana cara mengubah warna latar belakang render CAD?** Gunakan opsi `setBackgroundColor` untuk menerapkan latar belakang khusus sebelum ekspor.  
- **Apa itu auto layout scaling?** Ini secara otomatis menyesuaikan gambar agar sesuai dengan kanvas, memastikan tampilan optimal tanpa perhitungan manual.

## Apa itu “set canvas size” dalam Aspose.CAD untuk Java?

Mengatur ukuran kanvas memberi tahu mesin render dimensi piksel tepat (atau ukuran fisik) untuk file output. Ini penting ketika Anda membutuhkan tata letak halaman yang konsisten, mengintegrasikan gambar CAD ke dalam laporan, atau menghasilkan thumbnail dengan dimensi yang dapat diprediksi secara akurat.

## Mengapa menggunakan fitur lanjutan Aspose.CAD?

Aspose.CAD mendukung **lebih dari 50 format input dan output**—termasuk DWG, DXF, DWF, PDF, PNG, TIFF, dan SVG—dan dapat memproses gambar dengan ratusan halaman tanpa memuat seluruh file ke memori. Perpustakaan ini menyediakan **rendering berfidelity tinggi hingga 600 DPI**, menjamin bahwa PDF yang dikonversi mempertahankan ketebalan garis, lapisan, dan warna persis seperti yang muncul dalam file CAD sumber.

## Prasyarat
- Java Development Kit (JDK) 8 atau yang lebih tinggi.  
- Perpustakaan Aspose.CAD untuk Java (unduh versi terbaru dari situs web Aspose).  
- Lisensi Aspose.CAD yang valid untuk penggunaan produksi (versi percobaan gratis dapat digunakan untuk evaluasi).

## Ikhtisar Langkah‑per‑Langkah dari Topik Lanjutan

### Cara mengatur ukuran kanvas dalam Aspose.CAD untuk Java?

Saat Anda membuat instance `CadImage`, Anda dapat menentukan lebar dan tinggi kanvas melalui objek `ImageOptions` sebelum menyimpan. Ini memastikan file yang diekspor sesuai dengan dimensi yang Anda butuhkan.

**Jawaban langsung:**  
Buat objek `CadImage`, konfigurasikan instance `ImageOptions` dengan `setWidth` dan `setHeight`, lalu panggil `save`—output akan dirender pada ukuran kanvas tepat yang Anda definisikan.

**Penjelasan istilah:**  
`CadImage` adalah kelas inti Aspose.CAD yang mewakili gambar CAD yang dimuat dalam memori.  

`ImageOptions` adalah objek konfigurasi yang mengontrol parameter rasterisasi seperti ukuran kanvas, DPI, dan warna latar belakang.

### Cara mengonversi CAD ke PDF sambil mempertahankan ukuran kanvas?

Gunakan kelas `PdfOptions` bersama dengan pengaturan kanvas. Proses konversi menghormati dimensi kanvas, menghasilkan PDF yang tampak persis seperti render di layar.

**Jawaban langsung:**  
Buat instance `PdfOptions`, atur `setVectorRasterizationOptions`-nya ke objek `ImageOptions` yang berisi lebar dan tinggi kanvas Anda, lalu panggil `save` pada `CadImage` dengan format PDF. PDF yang dihasilkan akan mempertahankan ukuran kanvas yang Anda tentukan.

**Penjelasan istilah:**  
`PdfOptions` adalah kelas Aspose.CAD yang mendefinisikan pengaturan ekspor khusus PDF, termasuk opsi vektor‑rasterisasi untuk kontrol tata letak yang presisi.

### Cara mengekstrak nilai atribut blok dari referensi eksternal?

API menyediakan koleksi `BlockReference`. Dengan mengiterasi koleksi ini Anda dapat membaca nilai atribut seperti nama lapisan, warna, atau data khusus yang tertanam dalam file DWG/DXF.

**Jawaban langsung:**  
Akses metode `getBlockReferences()` pada `CadImage`, iterasi setiap `BlockReference`, dan panggil `getAttributes()` untuk mengambil pasangan kunci‑nilai yang mewakili atribut blok. Ini berfungsi untuk referensi internal maupun eksternal.

**Penjelasan istilah:**  
`BlockReference` mewakili sebuah instance definisi blok dalam gambar CAD, menampilkan properti seperti posisi, rotasi, dan atribut yang terlampir.

### Cara mengatur warna latar belakang CAD untuk tampilan yang lebih halus?

Properti `BackgroundColor` dari opsi rendering memungkinkan Anda memilih warna RGB apa pun. Ini sangat berguna ketika latar belakang putih default bertentangan dengan merek atau tema UI Anda.

**Jawaban langsung:**  
Setel `ImageOptions.setBackgroundColor(Color.getRGB(255, 255, 255))` (atau nilai RGB yang diinginkan) sebelum menyimpan gambar atau PDF; warna yang dipilih akan mengisi latar belakang kanvas di belakang semua entitas gambar.

**Penjelasan istilah:**  
`BackgroundColor` adalah properti `ImageOptions` yang menentukan warna isi yang diterapkan ke seluruh kanvas sebelum entitas CAD apa pun digambar.

### Cara menerapkan auto layout scaling untuk penyesuaian kanvas dinamis?

Aktifkan flag `AutoLayoutScaling` dalam opsi rendering. Mesin akan secara otomatis menyesuaikan skala gambar agar sesuai dengan kanvas sambil mempertahankan rasio aspek, menghemat Anda dari perhitungan manual.

**Jawaban langsung:**  
Panggil `ImageOptions.setAutoLayoutScaling(true)`; renderer akan menghitung faktor skala optimal sehingga seluruh gambar muat dalam dimensi kanvas yang ditentukan tanpa distorsi.

**Penjelasan istilah:**  
`AutoLayoutScaling` adalah flag Boolean dalam `ImageOptions` yang, ketika diaktifkan, memberi instruksi pada mesin rendering untuk secara otomatis menyesuaikan gambar agar mengisi kanvas.

## Tutorial Terperinci untuk Setiap Fitur

Berikut adalah tutorial khusus yang membimbing Anda melalui setiap kemampuan lanjutan langkah demi langkah. Klik tautan mana pun untuk menyelami lebih dalam.

### [Aktifkan Pelacakan untuk Proses Rendering CAD](./enable-tracking-for-cad-rendering-process/)
Tingkatkan rendering CAD Anda dengan Aspose.CAD untuk Java. Ikuti panduan langkah demi langkah kami untuk mengaktifkan pelacakan dan meningkatkan pengalaman konversi PDF Anda.

### [Integrasikan Format IGES](./integrate-iges-format/)
Jelajahi integrasi format IGES secara mulus dengan Aspose.CAD untuk Java. Ikuti panduan langkah demi langkah kami, memanfaatkan kekuatan Aspose.CAD untuk meningkatkan pengalaman pengembangan CAD Anda.

### [Dukungan Mesh dengan Aspose.CAD untuk Java](./mesh-support-in-cad/)
Jelajahi dukungan mesh dalam aplikasi Java dengan Aspose.CAD. Konversi file CAD ke PDF dengan mudah. 

### [Dukungan Pen dalam Ekspor](./pen-support-in-export/)
Kuasai kustomisasi pen dalam ekspor CAD dengan Aspose.CAD untuk Java. Ikuti panduan langkah demi langkah kami untuk integrasi yang mulus.

### [Membaca File DWT](./reading-dwt-files/)
Kuasai membaca file DWT di Java dengan Aspose.CAD. Ikuti panduan langkah demi langkah kami untuk integrasi yang mulus.

### [Mengatur Latar Belakang dan Warna Gambar Menggunakan Aspose.CAD untuk Java](./setting-background-and-drawing-color/)
Konversi file CAD ke PDF dan TIFF dengan mudah menggunakan Aspose.CAD untuk Java. Atur latar belakang dan warna gambar khusus untuk hasil visual yang menakjubkan.

### [Atur Ukuran Kanvas dan Mode](./set-canvas-size-and-mode/)
Jelajahi kekuatan Aspose.CAD untuk Java dengan panduan langkah demi langkah kami tentang **setting canvas size** dan mode. Konversi file CAD ke format PDF dan TIFF dengan mudah.

### [Mengatur Auto Layout Scaling dengan Aspose.CAD untuk Java](./setting-auto-layout-scaling/)
Tingkatkan alur kerja CAD Anda dengan Aspose.CAD untuk Java. Panduan langkah demi langkah ini memperkenalkan Auto Layout Scaling, memastikan tampilan optimal dan efisiensi. Unduh perpustakaan, ikuti tutorial, dan revolusionerkan proyek CAD Anda.

### [Dukungan Lapisan dengan Aspose.CAD di Java](./support-of-layers-in-cad/)
Kuasai dukungan lapisan dalam pengembangan CAD Java dengan Aspose.CAD. Atur dan ekspor gambar dengan mudah.

### [Ekstrak Nilai Atribut Blok dari Referensi Eksternal Menggunakan Aspose.CAD di Java](./extract-block-attribute-value/)
Jelajahi tutorial kami tentang mengekstrak nilai atribut blok dari referensi eksternal DWG di Java menggunakan Aspose.CAD. Tingkatkan alur kerja pengembangan CAD Anda dengan mudah.

## Masalah Umum & Pemecahan Masalah
- **Ukuran kanvas tidak diterapkan:** Pastikan Anda mengatur ukuran pada objek `ImageOptions` yang tepat sebelum memanggil `save()`.  
- **Warna latar belakang tidak berubah:** Verifikasi bahwa mode rendering mendukung warna latar belakang (misalnya, PNG, TIFF).  
- **Atribut blok mengembalikan null:** Periksa bahwa file DWG memang berisi definisi atribut dan Anda mengakses referensi blok yang tepat.  
- **Auto layout scaling terlihat terdistorsi:** Pastikan flag aspect‑ratio diaktifkan; jika tidak, mesin dapat meregangkan gambar.

## Pertanyaan yang Sering Diajukan

**Q: Bisakah saya mengatur ukuran kanvas khusus untuk setiap file dalam proses batch?**  
A: Ya. Loop melalui koleksi file CAD Anda, konfigurasikan ukuran kanvas pada setiap instance `ImageOptions`, dan simpan output secara programatis.

**Q: Apakah mengatur ukuran kanvas memengaruhi kualitas PDF yang diekspor?**  
A: Kualitas ditentukan oleh pengaturan DPI dalam opsi rendering. Anda dapat meningkatkan DPI sambil mempertahankan dimensi kanvas untuk mendapatkan PDF dengan resolusi lebih tinggi.

**Q: Bagaimana cara mengekstrak nilai atribut blok dari DWG yang berisi referensi eksternal?**  
A: Gunakan koleksi `ExternalReference` untuk menyelesaikan referensi, lalu iterasi objek `BlockReference`-nya untuk membaca nilai atribut.

**Q: Apakah auto layout scaling kompatibel dengan format output vektor seperti PDF?**  
A: Ya. Logika scaling bekerja untuk output raster (PNG, TIFF) dan vektor (PDF, SVG), memastikan gambar sesuai dengan kanvas.

**Q: Lisensi apa yang diperlukan untuk penggunaan komersial?**  
A: Lisensi Aspose.CAD berbayar diperlukan untuk penyebaran produksi. Lisensi evaluasi gratis dapat digunakan untuk pengembangan dan pengujian.

---
**Terakhir Diperbarui:** 2026-06-24  
**Diuji Dengan:** Aspose.CAD untuk Java 24.12 (terbaru)  
**Penulis:** Aspose  

{{< blocks/products/products-backtop-button >}}

## Tutorial Terkait

- [Buat PDF dari CAD – Auto Layout Scaling dengan Aspose.CAD Java](/cad/java/advanced-cad-features/setting-auto-layout-scaling/)
- [Cara Mengonversi DXF ke PDF dengan Aspose.CAD untuk Java](/cad/java/additional-features/)
- [Ekspor DWG ke PDF dan Konversi Gambar CAD – Tutorial Aspose.CAD Java](/cad/java/cad-drawing-conversion/)


{{< /blocks/products/pf/tutorial-page-section >}}
{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}