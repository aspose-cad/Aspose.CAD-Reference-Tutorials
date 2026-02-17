---
date: 2026-02-17
description: Pelajari cara menyimpan DWG sebagai JPEG di Java menggunakan Aspose.CAD,
  menambahkan beberapa lapisan, dan menyesuaikan dimensi CAD untuk konversi gambar
  yang presisi.
linktitle: Support of Layers in CAD
second_title: Aspose.CAD Java API
title: Simpan DWG sebagai JPEG dengan Dukungan Lapisan di Java
url: /id/java/advanced-cad-features/support-of-layers-in-cad/
weight: 18
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Simpan DWG sebagai JPEG dengan Dukungan Layer di Java

## Pendahuluan

Dalam tutorial ini Anda akan menemukan cara **menyimpan DWG sebagai JPEG** sambil memanfaatkan dukungan layer secara penuh di Aspose.CAD untuk Java. Layer memungkinkan Anda mengisolasi bagian tertentu dari gambar, sehingga mudah mengekspor hanya apa yang Anda butuhkan. Kami akan membimbing Anda melalui setiap langkah, mulai dari menyiapkan lingkungan hingga mengekspor JPEG yang hanya mencakup layer yang Anda pilih.

## Jawaban Cepat
- **Apa arti “save DWG as JPEG”?** Itu mengonversi gambar DWG (atau CAD lainnya) menjadi gambar raster JPEG.  
- **Bisakah saya menyertakan hanya layer yang dipilih?** Ya – gunakan metode `setLayers` untuk menentukan layer mana yang akan dirender.  
- **Bagaimana cara mengubah ukuran gambar?** Sesuaikan `setPageWidth` dan `setPageHeight` dalam `CadRasterizationOptions`.  
- **Apakah ini solusi khusus Java?** Contoh ini menggunakan Aspose.CAD untuk Java, tetapi konsep yang sama berlaku untuk bahasa lain.  
- **Apakah saya memerlukan lisensi?** Versi percobaan gratis dapat digunakan untuk pengujian; lisensi komersial diperlukan untuk produksi.

## Apa itu “save DWG as JPEG”?
Menyimpan DWG sebagai JPEG berarti merasterkan file CAD berbasis vektor (DWG, DWF, DXF, dll.) menjadi bitmap JPEG standar. Ini berguna ketika Anda perlu menyematkan gambar CAD dalam halaman web, email, atau laporan yang hanya mendukung gambar raster.

## Mengapa menggunakan konversi JPEG yang mendukung layer?
- **Fokus pada data yang relevan:** Ekspor hanya layer yang Anda butuhkan, mengurangi ukuran file dan kekacauan visual.  
- **Mempertahankan maksud desain:** Layer mempertahankan pengelompokan logis objek, sehingga Anda dapat menggunakan kembali file sumber yang sama untuk output yang berbeda.  
- **Kontrol penuh atas dimensi:** Dengan menyesuaikan opsi rasterisasi, Anda dapat menghasilkan gambar resolusi tinggi yang sesuai dengan kebutuhan penerbitan Anda.

## Prasyarat

Sebelum memulai, pastikan Anda memiliki hal berikut:

1. **Aspose.CAD for Java Library** – unduh dari [website](https://releases.aspose.com/cad/java/). Ikuti panduan instalasi untuk menambahkan file JAR ke classpath proyek Anda.  
2. **Java Development Environment** – JDK terbaru (8 atau lebih baru) terpasang di mesin Anda.

Setelah semuanya siap, mari jelajahi kode yang diperlukan untuk **menyimpan DWG sebagai JPEG** dengan rendering layer selektif.

## Impor Namespace

Mulailah dengan mengimpor kelas Aspose.CAD yang diperlukan dan utilitas Java standar:

```java
import com.aspose.cad.Image;

import com.aspose.cad.imageoptions.CadRasterizationOptions;
import com.aspose.cad.imageoptions.JpegOptions;
import java.util.ArrayList;
import java.util.Arrays;
import java.util.List;
```

## Panduan Langkah‑per‑Langkah

### Langkah 1: Menyiapkan Jalur File

Tentukan di mana file DWF sumber berada dan di mana JPEG output akan ditulis.

```java
String dataDir = "Your Document Directory" + "DWFDrawings/";
String srcFile = dataDir + "for_layers_test.dwf";
String outFile = dataDir + "for_layers_test.jpg";
```

### Langkah 2: Memuat Gambar DWF

Gunakan metode `Image.load` dari Aspose.CAD untuk membaca gambar CAD.

```java
Image image = Image.load(srcFile);
```

### Langkah 3: Mengonfigurasi Opsi Rasterisasi (Sesuaikan Dimensi CAD)

Buat instance `CadRasterizationOptions` dan atur ukuran output yang diinginkan. Mengubah nilai-nilai ini memungkinkan Anda **menyesuaikan dimensi CAD** untuk JPEG akhir.

```java
CadRasterizationOptions rasterizationOptions = new CadRasterizationOptions();
rasterizationOptions.setPageWidth(1600);
rasterizationOptions.setPageHeight(1600);
```

### Langkah 4: Menentukan Layer (Tambahkan Beberapa Layer)

Jika Anda ingin merender lebih dari satu layer, cukup tambahkan nama-namanya ke dalam daftar. Di sini kami memulai dengan satu layer bernama “LayerA”.

```java
List<String> stringList = new ArrayList<>(Arrays.asList("LayerA"));
rasterizationOptions.setLayers(stringList);
```

*Pro tip:* Untuk **menambahkan beberapa layer**, perluas pemanggilan `Arrays.asList`, misalnya `Arrays.asList("LayerA", "LayerB", "LayerC")`. Ini memungkinkan Anda **memilih layer CAD tertentu** untuk konversi.

### Langkah 5: Mengonfigurasi Opsi JPEG (Java Convert CAD Image)

Hubungkan pengaturan rasterisasi dengan format output JPEG.

```java
JpegOptions jpegOptions = new JpegOptions();
jpegOptions.setVectorRasterizationOptions(rasterizationOptions);
```

### Langkah 6: Mengekspor ke JPG (Simpan DWG sebagai JPEG)

Akhirnya, tulis gambar ke disk. Langkah ini **menyimpan gambar CAD sebagai file JPEG** yang hanya berisi layer yang dipilih.

```java
image.save(outFile, jpegOptions);
```

Dengan mengikuti langkah-langkah ini Anda telah berhasil **menyimpan DWG sebagai JPEG** sambil mengontrol layer yang muncul dan menyesuaikan dimensi gambar.

## Cara Mengonversi DWF ke JPEG dengan Pemilihan Layer

Meskipun contoh ini menggunakan sumber DWF, pipeline rasterisasi yang sama bekerja untuk format CAD yang didukung apa pun (DWG, DXF, DGN, dll.). Cukup ubah ekstensi file di `srcFile` dan perpustakaan akan menangani operasi **convert DWF to JPEG** (atau format lain) secara otomatis.

## Masalah Umum dan Solusinya

| Masalah | Solusi |
|-------|----------|
| **Layers not appearing** | Verifikasi bahwa nama layer persis sama dengan yang disimpan dalam file DWF (case‑sensitive). |
| **Output image is blank** | Pastikan `setPageWidth` dan `setPageHeight` cukup besar untuk menampung ekstensi gambar. |
| **License exception** | Gunakan lisensi percobaan untuk pengujian; dapatkan lisensi penuh untuk lingkungan produksi. |

## Pertanyaan yang Sering Diajukan

**T: Bisakah saya menambahkan beberapa layer ke opsi rasterisasi?**  
J: Tentu saja. Perluas `stringList` dengan nama layer tambahan, misalnya `Arrays.asList("LayerA", "LayerB")`.

**T: Apakah Aspose.CAD kompatibel dengan format CAD lain?**  
J: Ya, ia mendukung DWG, DXF, DWF, dan banyak format lainnya.

**T: Bagaimana saya dapat mengubah dimensi gambar output?**  
J: Modifikasi `setPageWidth` dan `setPageHeight` dalam instance `CadRasterizationOptions`.

**T: Di mana saya dapat membeli lisensi untuk Aspose.CAD?**  
J: Anda dapat menjelajahi opsi lisensi [di sini](https://purchase.aspose.com/buy).

**T: Di mana saya dapat mendapatkan dukungan komunitas?**  
J: Bergabunglah dengan komunitas Aspose.CAD di [forum](https://forum.aspose.com/c/cad/19) untuk bantuan dan diskusi.

---

**Terakhir Diperbarui:** 2026-02-17  
**Diuji Dengan:** Aspose.CAD for Java 24.11  
**Penulis:** Aspose  

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}