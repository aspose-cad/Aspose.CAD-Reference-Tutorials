---
date: 2026-04-23
description: Pelajari cara mengonversi DWG ke PNG dan menyimpan CAD sebagai PNG menggunakan
  Aspose.CAD untuk Java, mengonversi file DWG, DXF, dan file CAD lainnya menjadi gambar
  raster secara efisien.
keywords:
- convert dwg to png
- save cad as png
- cad to png conversion
linktitle: Ubah Gambar CAD ke Format Gambar Raster
second_title: Aspose.CAD Java API
title: Ubah DWG ke PNG – Simpan CAD sebagai PNG Menggunakan Aspose.CAD untuk Java
url: /id/java/cad-drawing-conversion/convert-cad-drawing-to-raster-image/
weight: 10
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Mengonversi DWG ke PNG – Simpan CAD sebagai PNG Menggunakan Aspose.CAD untuk Java

## Pendahuluan

Dalam tutorial ini, Anda akan belajar cara **mengonversi DWG ke PNG** menggunakan Aspose.CAD untuk Java. Mengonversi gambar CAD ke format gambar raster seperti PNG adalah kebutuhan yang sering muncul untuk pratinjau web, dokumentasi, dan pelaporan. Aspose.CAD menyediakan cara yang andal dan berkinerja tinggi untuk melakukan **konversi cad ke png** untuk DWG, DXF, DWF, dan banyak tipe file CAD lainnya.

## Jawaban Cepat
- **Perpustakaan apa yang menangani konversi?** Aspose.CAD untuk Java.  
- **Apakah saya dapat mengonversi DWG ke PNG?** Ya – API yang sama bekerja untuk DWG, DXF, dan format lainnya.  
- **Apakah saya memerlukan lisensi untuk produksi?** Lisensi komersial diperlukan untuk penggunaan non‑evaluasi.  
- **Apakah ukuran raster dapat dikonfigurasi?** Tentu – Anda dapat mengatur lebar halaman, tinggi, dan DPI melalui opsi rasterisasi.  
- **Berapa lama proses konversi?** Biasanya kurang dari satu detik untuk gambar standar; file yang lebih besar mungkin memerlukan waktu lebih lama.

## Cara Mengonversi DWG ke PNG Menggunakan Aspose.CAD

Menyimpan CAD sebagai PNG berarti merasterkan data CAD berbasis vektor menjadi gambar berbasis piksel (PNG). Proses ini, yang sering disebut **convert dwg to raster**, mempertahankan kesetiaan visual sambil menghasilkan format yang mudah disisipkan ke halaman web, email, atau laporan.

## Mengapa Menggunakan Aspose.CAD untuk Java?

- **Dukungan format yang luas** – bekerja dengan DWG, DXF, DWF, dan lainnya.  
- **Tanpa dependensi eksternal** – Java murni, tanpa DLL native.  
- **Kontrol halus** – sesuaikan resolusi, warna latar belakang, dan kualitas rendering.  
- **Kinerja skalabel** – cocok untuk pemrosesan batch atau konversi on‑the‑fly.  
- **Cara menyimpan CAD** – API memungkinkan Anda **menyimpan CAD sebagai PNG** hanya dengan beberapa baris kode.

## Prasyarat

Sebelum memulai tutorial, pastikan Anda telah menyiapkan prasyarat berikut:

1. **Lingkungan Pengembangan Java** – JDK yang berfungsi (8 atau lebih baru) serta IDE atau alat build pilihan Anda.  
2. **Perpustakaan Aspose.CAD** – unduh dan integrasikan perpustakaan Aspose.CAD untuk Java ke dalam proyek Anda. Anda dapat menemukan perpustakaan tersebut [di sini](https://releases.aspose.com/cad/java/).

## Impor Namespace

Dalam kode Java Anda, impor namespace yang diperlukan untuk memanfaatkan fungsionalitas Aspose.CAD untuk Java secara efektif. Langkah ini penting untuk mengakses kelas dan metode yang dibutuhkan.

```java
import com.aspose.cad.Image;
import com.aspose.cad.ImageOptionsBase;

import com.aspose.cad.imageoptions.CadRasterizationOptions;
import com.aspose.cad.imageoptions.PngOptions;
```

Sekarang, mari kita uraikan proses mengonversi gambar CAD menjadi gambar raster ke dalam langkah‑langkah terperinci:

## Langkah 1: Muat Gambar CAD

```java
String dataDir = "Your Document Directory" + "CADConversion/";
String srcFile = dataDir + "conic_pyramid.dxf";
Image image = Image.load(srcFile);
```

Pada langkah ini, kami memuat gambar CAD dari jalur file yang ditentukan menggunakan metode `Image.load()`.

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

## Kasus Penggunaan Umum & Tips

- **Pembuatan pratinjau web** – Konversi file DWG besar menjadi thumbnail PNG ringan untuk tampilan cepat di browser.  
- **Penyisipan dalam laporan** – Gunakan output PNG dalam laporan PDF atau Word di mana file CAD vektor tidak didukung.  
- **Konversi batch** – Loop melalui folder berisi file CAD dan terapkan pengaturan rasterisasi yang sama untuk output yang konsisten.  
- **Tip pro:** Sesuaikan `rasterizationOptions.setResolution()` untuk meningkatkan DPI bagi cetakan resolusi tinggi.  
- **Cara mengonversi DWG** – Anda juga dapat mengubah format output dengan mengganti `PngOptions` dengan opsi gambar lain (misalnya, `JpegOptions`) sambil mempertahankan pengaturan rasterisasi yang sama.

## Kesimpulan

Dengan mengikuti langkah‑langkah di atas, Anda dapat dengan mudah **mengonversi DWG ke PNG**, **menyimpan CAD sebagai PNG**, atau melakukan **konversi cad ke png** apa pun yang Anda perlukan. API Aspose.CAD untuk Java membuat proses ini sederhana, memberi Anda kontrol penuh atas resolusi, warna latar belakang, dan format output—sempurna untuk pratinjau web, dokumentasi, atau pipeline pemrosesan batch.

## Pertanyaan yang Sering Diajukan

**T: Bagaimana cara mengonversi file DWG ke PNG dengan warna latar belakang khusus?**  
J: Atur properti `backgroundColor` pada `CadRasterizationOptions` sebelum membuat instance `PngOptions`.

**T: Apakah memungkinkan mengonversi beberapa file CAD dalam satu operasi batch?**  
J: Ya—bungkus langkah pemuatan, rasterisasi, dan penyimpanan di dalam loop yang mengiterasi koleksi file Anda.

**T: Kualitas gambar apa yang dapat saya harapkan dari pengaturan default?**  
J: DPI default (96) menghasilkan PNG kualitas layar; tingkatkan DPI untuk hasil kualitas cetak.

**T: Apakah Aspose.CAD mendukung latar belakang transparan pada output PNG?**  
J: Tentu. Secara default, PNG disimpan dengan saluran alfa; Anda juga dapat menentukan latar belakang transparan dalam opsi rasterisasi.

**T: Dapatkah saya mengonversi file CAD ke format raster lain seperti JPEG atau BMP?**  
J: Ya—ganti `PngOptions` dengan `JpegOptions` atau `BmpOptions` sambil mempertahankan pengaturan rasterisasi yang sama.

---

**Terakhir Diperbarui:** 2026-04-23  
**Diuji Dengan:** Aspose.CAD untuk Java 24.12 (terbaru)  
**Penulis:** Aspose  

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}