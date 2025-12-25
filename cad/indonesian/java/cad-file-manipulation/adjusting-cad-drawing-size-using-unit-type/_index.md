---
date: 2025-12-25
description: Pelajari cara mengekspor DWG ke BMP menggunakan Aspose.CAD untuk Java.
  Panduan langkah demi langkah ini menunjukkan cara menyesuaikan ukuran gambar CAD
  dan mengonversi CAD ke BMP secara efisien.
linktitle: Adjusting CAD Drawing Size Using Unit Type
second_title: Aspose.CAD Java API
title: Ekspor DWG ke BMP – Sesuaikan Ukuran CAD Menggunakan Tipe Unit (Java)
url: /id/java/cad-file-manipulation/adjusting-cad-drawing-size-using-unit-type/
weight: 14
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Ekspor DWG ke BMP – Menyesuaikan Ukuran Gambar CAD Menggunakan Unit Type dengan Aspose.CAD untuk Java

## Pendahuluan

Saat Anda perlu **mengekspor DWG ke BMP**, mengontrol ukuran output dan satuan pengukuran sangat penting untuk proses lanjutan atau pencetakan. Pada tutorial ini Anda akan belajar cara menyesuaikan ukuran gambar CAD dan mengonversi CAD ke BMP dengan Aspose.CAD untuk Java, menggunakan properti `UnitType` untuk menentukan satuan pengukuran. Langkah‑langkah dijelaskan dengan bahasa yang mudah dipahami, sehingga Anda dapat mengikutinya meskipun baru mengenal pustaka ini.

## Jawaban Cepat
- **Apa arti “ekspor DWG ke BMP”?** Mengonversi gambar DWG menjadi gambar raster BMP.  
- **Properti mana yang mengontrol ukuran output?** `CadRasterizationOptions.setUnitType()` menetapkan satuan (misalnya sentimeter).  
- **Apakah saya memerlukan lisensi untuk menjalankan kode?** Versi percobaan gratis dapat digunakan untuk evaluasi; lisensi diperlukan untuk produksi.  
- **Bisakah saya memilih layout lain?** Ya, gunakan `setLayouts()` untuk menentukan layout model atau paper space.  
- **Format output apa yang didukung?** Selain BMP, Anda dapat mengekspor ke PNG, JPEG, TIFF, dll., dengan mengubah kelas opsi.

## Apa itu **ekspor DWG ke BMP**?

Mengekspor DWG ke BMP berarti merasterkan file DWG berbasis vektor menjadi gambar bitmap (BMP). Ini berguna ketika Anda memerlukan representasi pixel‑perfect untuk sistem lama, pipeline pemrosesan gambar, atau skenario tampilan sederhana.

## Mengapa menyesuaikan ukuran gambar CAD dengan **Unit Type**?

Menetapkan unit type memungkinkan Anda mengontrol dimensi fisik gambar yang diekspor tanpa harus menghitung faktor skala secara manual. Hal ini memastikan bitmap sesuai dengan ukuran dunia nyata (misalnya sentimeter), yang penting untuk gambar teknik dan dokumentasi cetak.

## Prasyarat

Sebelum memulai tutorial, pastikan Anda telah menyiapkan prasyarat berikut:

- **Lingkungan Pengembangan Java** – JDK yang berfungsi (versi 8 atau lebih baru) serta IDE atau alat build (Maven/Gradle).  
- **Pustaka Aspose.CAD untuk Java** – Unduh dan integrasikan pustaka Aspose.CAD ke dalam proyek Java Anda. Anda dapat memperoleh pustaka tersebut [di sini](https://releases.aspose.com/cad/java/).

## Impor Namespace

Di dalam kode Java Anda, sertakan namespace yang diperlukan untuk mengakses fungsionalitas Aspose.CAD. Tambahkan impor berikut:

```java
import com.aspose.cad.Image;
import com.aspose.cad.ImageOptionsBase;

import com.aspose.cad.imageoptions.CadRasterizationOptions;
import com.aspose.cad.imageoptions.PngOptions;
```

Sekarang, mari kita uraikan proses menyesuaikan ukuran gambar CAD menggunakan unit type menjadi langkah‑langkah yang mudah dikelola:

## Langkah 1: Definisikan Direktori Data

```java
String dataDir = "Your Document Directory" + "CADConversion/";
```

Tetapkan jalur ke direktori tempat file CAD Anda berada.

## Langkah 2: Muat Gambar CAD

```java
String sourceFilePath = dataDir + "sample.dwg";
Image image = Image.load(sourceFilePath);
```

Muat gambar CAD menggunakan kelas `Image` dari Aspose.CAD.

## Langkah 3: Buat Opsi BMP

```java
BmpOptions bmpOptions = new BmpOptions();
```

Instansiasi kelas `BmpOptions` untuk mengekspor layout CAD ke format BMP.

## Langkah 4: Konfigurasikan Opsi Rasterisasi

```java
CadRasterizationOptions cadRasterizationOptions = new CadRasterizationOptions();
bmpOptions.setVectorRasterizationOptions(cadRasterizationOptions);
```

Buat instance `CadRasterizationOptions` dan hubungkan dengan `BmpOptions` untuk rasterisasi vektor.

## Langkah 5: Atur Unit Type

```java
cadRasterizationOptions.setUnitType(UnitType.Centimeter);
```

Tentukan unit type yang diinginkan untuk gambar CAD. Pada contoh ini, kami menetapkannya ke **Centimeter**, yang secara langsung memengaruhi ukuran gambar yang diekspor ketika Anda **menyesuaikan ukuran gambar CAD**.

## Langkah 6: Atur Layouts

```java
cadRasterizationOptions.setLayouts(new String[] { "Model" });
```

Definisikan layout yang akan dipertimbangkan selama proses ekspor. Pada kasus ini, kami memilih layout **"Model"**, namun Anda dapat beralih ke layout paper space bila diperlukan.

## Langkah 7: Ekspor ke BMP

```java
String outPath = sourceFilePath + ".bmp";
image.save(outPath, bmpOptions);
```

Akhirnya, simpan gambar CAD yang telah dimodifikasi dalam format BMP. Langkah ini menyelesaikan alur kerja **ekspor DWG ke BMP** sambil mempertahankan penyesuaian ukuran yang telah Anda konfigurasi.

## Masalah Umum dan Solusinya

| Masalah | Penyebab | Solusi |
|-------|--------|-----|
| **Gambar output terlalu kecil** | Unit type tidak diatur atau default (pixel) yang digunakan | Panggil `setUnitType()` dengan satuan yang diinginkan (misalnya `UnitType.Centimeter`). |
| **Layout yang diekspor salah** | Nama layout typo | Verifikasi nama layout dengan penampil CAD; gunakan string yang tepat pada `setLayouts()`. |
| **Exception lisensi** | Menjalankan tanpa lisensi yang valid di produksi | Terapkan lisensi sementara atau permanen seperti yang dijelaskan di FAQ. |

## Pertanyaan yang Sering Diajukan (Lanjutan)

**T: Bisakah saya menggunakan Aspose.CAD untuk Java dengan bahasa pemrograman lain?**  
J: Aspose.CAD terutama mendukung Java, namun tersedia versi untuk bahasa lain seperti .NET.

**T: Apakah ada opsi lisensi untuk Aspose.CAD?**  
J: Ya, Anda dapat menjelajahi opsi lisensi dan membeli Aspose.CAD [di sini](https://purchase.aspose.com/buy).

**T: Apakah tersedia trial gratis untuk Aspose.CAD?**  
J: Tentu, Anda dapat mengakses trial gratis [di sini](https://releases.aspose.com/).

**T: Bagaimana cara mendapatkan dukungan untuk Aspose.CAD untuk Java?**  
J: Kunjungi forum Aspose.CAD [di sini](https://forum.aspose.com/c/cad/19) untuk dukungan lengkap.

**T: Bisakah saya memperoleh lisensi sementara untuk Aspose.CAD?**  
J: Ya, Anda dapat memperoleh lisensi sementara [di sini](https://purchase.aspose.com/temporary-license/).

---

**Terakhir Diperbarui:** 2025-12-25  
**Diuji Dengan:** Aspose.CAD untuk Java 24.10  
**Penulis:** Aspose  

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}