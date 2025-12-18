---
date: 2025-12-18
description: Pelajari cara mengonversi DWG ke PNG dan format gambar raster lainnya
  dengan Aspose.CAD untuk Java. Ekspor CAD sebagai PNG dengan hasil berkualitas tinggi.
linktitle: Convert CAD Layout to Raster Image Format
second_title: Aspose.CAD Java API
title: Konversi DWG ke PNG dan Format Raster Lain Menggunakan Aspose.CAD untuk Java
url: /id/java/cad-drawing-conversion/convert-cad-layout-to-raster-image/
weight: 12
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Mengonversi DWG ke PNG dan Format Raster Lainnya Menggunakan Aspose.CAD untuk Java

## Pendahuluan

Mengonversi DWG ke PNG (atau format gambar raster lainnya) adalah kebutuhan umum ketika Anda perlu membagikan gambar CAD kepada rekan tim yang tidak memiliki penampil CAD, menyisipkan desain dalam dokumentasi, atau menghasilkan thumbnail untuk galeri web. Aspose.CAD untuk Java membuat konversi ini menjadi sederhana, baik Anda bekerja dengan file gambar lengkap maupun hanya tata letak tertentu. Dalam tutorial ini kami akan memandu Anda melalui langkah‑langkah tepat untuk **mengonversi tata letak CAD ke gambar raster**—teknik yang sama dapat Anda gunakan untuk menghasilkan output PNG, JPEG, TIFF, atau PDF.

## Jawaban Cepat
- **Perpustakaan apa yang menangani DWG ke PNG?** Aspose.CAD untuk Java  
- **Format apa yang dapat diekspor?** PNG, JPEG, TIFF, PDF, BMP, dan lainnya  
- **Apakah saya memerlukan lisensi untuk pengujian?** Versi percobaan gratis dapat digunakan untuk pengembangan; lisensi diperlukan untuk produksi  
- **Bisakah saya memilih tata letak tertentu?** Ya, gunakan `setLayouts` untuk menargetkan “Model”, “Layout1”, dll.  
- **Apakah output beresolusi tinggi memungkinkan?** Tentu—sesuaikan `setPageWidth` dan `setPageHeight` untuk mengontrol DPI  

## Apa itu “convert dwg to png”?

Istilah “convert dwg to png” menggambarkan proses mengambil file DWG berbasis vektor (format asli untuk banyak aplikasi CAD) dan merasternya menjadi gambar PNG berbasis piksel. Gambar raster ideal untuk tampilan web, berbagi lewat email, dan integrasi ke dalam perangkat lunak non‑CAD.

## Mengapa mengekspor CAD sebagai PNG (atau format raster lainnya)?

- **Kompatibilitas Universal:** PNG dan JPEG didukung oleh hampir semua penampil gambar dan peramban.  
- **Pemuatan Cepat:** Gambar raster dimuat seketika dibandingkan membuka file DWG yang berat.  
- **Mudah Disisipkan:** Sisipkan PNG langsung ke Word, PowerPoint, atau HTML tanpa plugin tambahan.  
- **Penampilan Konsisten:** Anda mengontrol resolusi, latar belakang, dan tata letak, memastikan setiap pemangku kepentingan melihat visual yang sama.  

## Prasyarat

Sebelum memulai, pastikan Anda memiliki:

1. **Lingkungan Pengembangan Java** – JDK 8 atau yang lebih baru terpasang dan terkonfigurasi.  
2. **Aspose.CAD untuk Java** – Unduh JAR terbaru dari [dokumentasi Aspose.CAD untuk Java](https://reference.aspose.com/cad/java/).  

## Impor Namespace

Pertama, impor kelas‑kelas yang diperlukan. Impor ini memberi Anda akses ke pemuatan gambar, opsi rasterisasi, dan pengaturan output TIFF/PNG.

```java
import com.aspose.cad.Image;
import com.aspose.cad.ImageOptionsBase;

import com.aspose.cad.fileformats.tiff.enums.TiffExpectedFormat;
import com.aspose.cad.imageoptions.CadRasterizationOptions;
import com.aspose.cad.imageoptions.TiffOptions;
```

> **Pro tip:** Jika Anda berencana mengekspor ke PNG alih‑alih TIFF, ganti `TiffOptions` dengan `PngOptions` (ditemukan di `com.aspose.cad.imageoptions.PngOptions`).

## Panduan Langkah‑demi‑Langkah

### Langkah 1: Siapkan Direktori Sumber Daya

```java
// The path to the resource directory.
String dataDir = "Your Document Directory" + "CADConversion/";
```

Ganti `"Your Document Directory"` dengan jalur absolut tempat file CAD Anda berada.

### Langkah 2: Muat File CAD

```java
String srcFile = dataDir + "conic_pyramid.dxf";
Image image = Image.load(srcFile);
```

Anda dapat memuat format apa pun yang didukung (DWG, DXF, DGN, dll.). Ini adalah bagian **cara mengonversi cad**—cukup arahkan ke file dan biarkan Aspose menangani parsing.

### Langkah 3: Konfigurasikan Opsi Rasterisasi

```java
CadRasterizationOptions rasterizationOptions = new CadRasterizationOptions();
rasterizationOptions.setPageWidth(1200);
rasterizationOptions.setPageHeight(1200);
rasterizationOptions.setLayouts(new String[] {"Model", "Layout1"});
```

- `setPageWidth` / `setPageHeight` mengontrol resolusi output (nilai lebih besar = DPI lebih tinggi).  
- `setLayouts` memungkinkan Anda **mengonversi cad ke raster** untuk tata letak tertentu; hapus jika ingin meraster seluruh gambar.

### Langkah 4: Atur Opsi Gambar

```java
ImageOptionsBase options = new TiffOptions(TiffExpectedFormat.Default);
options.setVectorRasterizationOptions(rasterizationOptions);
```

Jika Anda menginginkan PNG, buat instance `PngOptions` alih‑alih `TiffOptions`. Di sinilah Anda **mengekspor cad sebagai png**.

### Langkah 5: Simpan Gambar Hasil

```java
image.save(dataDir + "conic_pyramid_layoutstorasterimage_out_.tiff", options);
```

Ubah ekstensi file menjadi `.png` (dan objek opsi menjadi `PngOptions`) untuk **menyimpan CAD sebagai JPEG/PNG**.

> **Kesalahan Umum:** Lupa mencocokkan ekstensi file dengan kelas opsi akan menyebabkan `UnsupportedFormatException`. Selalu pastikan keduanya sinkron.

## Masalah Umum dan Solusinya

| Masalah | Solusi |
|-------|----------|
| **Gambar output kosong** | Pastikan nama tata letak di `setLayouts` persis sama dengan yang ada di file CAD sumber. |
| **PNG beresolusi rendah** | Tingkatkan `setPageWidth` / `setPageHeight` atau atur `setResolution` pada opsi rasterisasi. |
| **Versi DWG tidak didukung** | Pastikan Anda menggunakan versi Aspose.CAD terbaru; versi lama mungkin tidak mendukung rilis DWG yang lebih baru. |
| **Kesalahan memori pada file besar** | Proses halaman satu per satu atau tingkatkan heap JVM (`-Xmx2g`). |

## Pertanyaan yang Sering Diajukan

**T: Apakah Aspose.CAD kompatibel dengan berbagai format file CAD?**  
J: Ya, mendukung DWG, DXF, DGN, dan banyak lainnya.

**T: Bisakah saya menyesuaikan resolusi gambar raster output?**  
J: Tentu. Sesuaikan `setPageWidth`, `setPageHeight`, atau `setResolution` dalam `CadRasterizationOptions`.

**T: Bagaimana cara mengonversi beberapa tata letak CAD dalam satu kali proses?**  
J: Berikan array berisi semua nama tata letak ke `setLayouts`, misalnya `new String[]{"Model","Layout1","Layout2"}`.

**T: Apakah ada format output selain TIFF yang didukung?**  
J: Ya—PNG, JPEG, BMP, PDF, dan lainnya tersedia melalui kelas `*Options` masing‑masing.

**T: Di mana saya dapat mendapatkan bantuan atau berbagi pengalaman dengan Aspose.CAD?**  
J: Kunjungi [forum Aspose.CAD](https://forum.aspose.com/c/cad/19) untuk dukungan komunitas dan bantuan resmi.

## Kesimpulan

Dengan mengikuti langkah‑langkah ini Anda dapat **mengonversi DWG ke PNG**, **mengekspor CAD sebagai PNG**, **menyimpan CAD sebagai JPEG**, atau menghasilkan format raster lain yang Anda butuhkan. Aspose.CAD untuk Java menangani proses berat, memungkinkan Anda fokus pada integrasi gambar berkualitas tinggi ke dalam aplikasi, dokumentasi, atau portal web Anda.

---

**Last Updated:** 2025-12-18  
**Tested With:** Aspose.CAD for Java 24.12  
**Author:** Aspose  

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}