---
date: 2025-12-19
description: Pelajari cara menyimpan CAD sebagai PNG menggunakan Aspose.CAD untuk
  Java, mengonversi file DWG, DXF, dan file CAD lainnya menjadi gambar raster secara
  efisien.
linktitle: Convert CAD Drawing to Raster Image Format
second_title: Aspose.CAD Java API
title: Simpan CAD sebagai PNG – Konversi Gambar CAD ke Format Gambar Raster Menggunakan
  Aspose.CAD untuk Java
url: /id/java/cad-drawing-conversion/convert-cad-drawing-to-raster-image/
weight: 10
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Simpan CAD menjadi PNG – Konversi Gambar CAD ke Format Gambar Raster Menggunakan Aspose.CAD untuk Java

## Perkenalan

Dalam tutorial ini, Anda akan belajar cara **menyimpan CAD sebagai PNG** menggunakan Aspose.CAD untuk Java. Mengonversi gambar CAD ke format gambar raster seperti PNG merupakan kebutuhan yang sering muncul untuk pemasaran web, dokumentasi, dan pelaporan. Aspose.CAD menyediakan cara yang andal dan berperforma tinggi untuk melakukan **konversi cad ke png** untuk DWG, DXF, DWF, dan banyak tipe file CAD lainnya.

## Jawaban Cepat
- **Perpustakaan apa yang menangani konversi?** Aspose.CAD untuk Java.
- **Apakah saya dapat mengonversi DWG ke PNG?** Ya – API yang sama berfungsi untuk DWG, DXF, dan format lainnya.
- **Apakah saya memerlukan lisensi untuk produksi?** Lisensi komersial diperlukan untuk penggunaan non‑evaluasi.
- **Apakah ukuran raster dapat dikonfigurasi?** Tentu – Anda dapat mengatur lebar halaman, tinggi, dan DPI melalui opsi rasterisasi.
- **Berapa lama proses konversi?** Biasanya kurang dari satu detik untuk gambar standar; file yang lebih besar mungkin memerlukan waktu lebih lama.

## Apa itu “simpan CAD sebagai PNG”?
Menyimpan CAD sebagai PNG berarti merasterkan data CAD berbasis vektor menjadi gambar berbasis piksel (PNG). Proses ini, yang sering disebut **konversi cad ke raster**, mempertahankan kesetiaan visual sambil menghasilkan format yang mudah disisipkan ke halaman web, email, atau laporan.

## Mengapa menggunakan Aspose.CAD untuk Java?
- **Format Dukungan luas** – bekerja dengan DWG, DXF, DWF, dan lainnya.
- **Tanpa ketergantungan eksternal** – murni Java, tanpa DLL native.
- **Kontrol detail** – sesuaikan resolusi, warna latar belakang, dan kualitas rendering.
- **Kinerja skalabel** – cocok untuk transmisi batch atau konversi on‑the‑fly.

## Prasyarat

Sebelum memulai tutorial, pastikan Anda telah menyiapkan prasyarat berikut:

1. **Lingkungan Pengembangan Java:** Pastikan Anda memiliki lingkungan pengembangan Java yang berfungsi di mesin Anda.
2. **Perpustakaan Aspose.CAD:** Unduh dan integrasikan perpustakaan Aspose.CAD untuk Java ke dalam proyek Anda. Anda dapat menemukan perpustakaan tersebut [di sini](https://releases.aspose.com/cad/java/).

## Impor Namespace

Dalam kode Java Anda, impor namespace yang diperlukan untuk memanfaatkan fungsionalitas Aspose.CAD untuk Java secara efektif. Langkah ini penting untuk mengakses kelas dan metode yang dibutuhkan.

```java
import com.aspose.cad.Image;
import com.aspose.cad.ImageOptionsBase;

import com.aspose.cad.imageoptions.CadRasterizationOptions;
import com.aspose.cad.imageoptions.PngOptions;
```

Sekarang, mari kita uraikan proses mengonversi gambar CAD menjadi gambar raster dalam langkah‑langkah terperinci:

## Langkah 1: Muat Gambar CAD

```java
String dataDir = "Your Document Directory" + "CADConversion/";
String srcFile = dataDir + "conic_pyramid.dxf";
Image image = Image.load(srcFile);
```

Pada langkah ini, kita memuat gambar CAD dari jalur file yang ditentukan menggunakan metode `Image.load()`.

## Langkah 2: Atur Opsi Rasterisasi

```java
CadRasterizationOptions rasterizationOptions = new CadRasterizationOptions();
rasterizationOptions.setPageWidth(1200);
rasterizationOptions.setPageHeight(1200);
```

Buat instance `CadRasterizationOptions` dan atur lebar serta tinggi halaman untuk gambar raster.

## Langkah 3: Buat Opsi Gambar

```java
ImageOptionsBase options = new PngOptions();
options.setVectorRasterizationOptions(rasterizationOptions);
```

Buat instance `PngOptions` untuk gambar hasil dan tetapkan opsi rasterisasi vektor.

## Langkah 4: Simpan Gambar Raster

```java
image.save(dataDir + "conic_pyramid_raster_image_out.png", options);
```

Simpan gambar raster yang dihasilkan ke direktori yang ditentukan menggunakan metode `image.save()`.

Ulangi langkah‑langkah ini untuk file CAD spesifik Anda, dan Anda akan berhasil **mengonversi gambar gambar CAD** ke PNG.

## Kasus & Tip Penggunaan Umum

- **Pembuatan tayangan web** – Konversi file DWG besar menjadi thumbnail PNG ringan untuk tampilan cepat di browser.
- **Penyisipan dalam laporan** – Gunakan output PNG dalam laporan PDF atau Word di mana file vektor CAD tidak didukung.
- **Konversi batch** – Loop melalui folder berisi file CAD dan menerapkan pengaturan rasterisasi yang sama untuk output yang konsisten.
- **Tips pro:** Sesuaikan `rasterizationOptions.setResolution()` untuk meningkatkan DPI demi cetakan beresolusi tinggi.

## Kesimpulan

Kesimpulannya, mengubah gambar CAD menjadi gambar raster menggunakan Aspose.CAD untuk Java adalah proses yang sederhana. Dengan mengikuti langkah‑langkah yang dijabarkan dalam tutorial ini, Anda dapat dengan efisien mengintegrasikan fungsionalitas ini ke dalam aplikasi Java Anda dan melakukan **konversi dwg ke png**, **ekspor cad sebagai png**, atau **konversi cad ke png** lainnya yang Anda perlukan.

## Pertanyaan yang Sering Diajukan

**Q: Bagaimana cara mengubah file DWG ke PNG dengan warna latar belakang khusus?**
A: Atur properti `backgroundColor` pada `CadRasterizationOptions` sebelum membuat instance `PngOptions`.

**Q: Apakah memungkinkan mengonversi beberapa file CAD dalam satu batch operasi?**
A: Ya—bungkus langkah pemuatan, rasterisasi, dan penyimpanan di dalam loop yang mengiterasi koleksi file Anda.

**Q: Kualitas gambar apa yang dapat saya harapkan dari pengaturan default?**
A: DPI default (96) menghasilkan kualitas layar PNG; tingkatkan DPI untuk hasil kualitas cetak.

**Q: Apakah Aspose.CAD mendukung latar belakang transparan pada keluaran PNG?**
J: Tentu. Secara default, PNG disimpan dengan saluran alfa; Anda juga dapat menentukan latar belakang transparan dalam opsi rasterisasi.

**Q: Bisakah saya mengonversi file CAD ke format raster lain seperti JPEG atau BMP?**
A: Ya—ganti `PngOptions` dengan `JpegOptions` atau `BmpOptions` sambil mempertahankan pengaturan rasterisasi yang sama.

---

**Terakhir Diperbarui:** 19-12-2025
**Diuji Dengan:** Aspose.CAD untuk Java 24.12 (terbaru)
**Penulis:** Beranggapan  

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}