---
date: 2026-05-25
description: Pelajari cara mengekspor file dgn ke gambar JPEG dengan Aspose.CAD for
  Java. Panduan langkah demi langkah ini menunjukkan cara mengonversi dgn ke jpeg
  secara efisien.
keywords:
- how to export dgn
- convert dgn to jpeg
- java convert cad to image
linktitle: Mengekspor DGN dalam Format AutoCAD ke Format Gambar Raster
schemas:
- author: Aspose
  dateModified: '2026-05-25'
  description: Learn how to export dgn files to JPEG images with Aspose.CAD for Java.
    This step‑by‑step guide shows you how to convert dgn to jpeg efficiently.
  headline: How to Export DGN to JPEG with Aspose.CAD for Java
  type: TechArticle
- description: Learn how to export dgn files to JPEG images with Aspose.CAD for Java.
    This step‑by‑step guide shows you how to convert dgn to jpeg efficiently.
  name: How to Export DGN to JPEG with Aspose.CAD for Java
  steps:
  - name: '**Aspose.CAD Library** – download the latest JAR from the official site [here](https://releases.aspose.com/cad/java/).
      You can also explore other product releases [here](https://releases.aspose.com/).'
    text: '**Aspose.CAD Library** – download the latest JAR from the official site [here](https://releases.aspose.com/cad/java/).
      You can also explore other product releases [here](https://releases.aspose.com/).'
  - name: '**Java Development Kit (JDK)** – Java 8 or newer installed on your machine.'
    text: '**Java Development Kit (JDK)** – Java 8 or newer installed on your machine.'
  - name: '**IDE** – IntelliJ IDEA, Eclipse, or any Java‑compatible editor you prefer.'
    text: '**IDE** – IntelliJ IDEA, Eclipse, or any Java‑compatible editor you prefer.'
  type: HowTo
- questions:
  - answer: Yes, Aspose.CAD supports over 30 vector formats, including DWG, DXF, DWF,
      and SVG, enabling a single API for many conversion scenarios.
    question: Can I use Aspose.CAD for Java with other CAD file formats?
  - answer: Yes, you can access a free trial [here](https://releases.aspose.com/).
    question: Is there a free trial available for Aspose.CAD for Java?
  - answer: Refer to the official docs [here](https://reference.aspose.com/cad/java/).
    question: Where can I find documentation for Aspose.CAD for Java?
  - answer: Visit the support forum [here](https://forum.aspose.com/c/cad/19).
    question: How can I get support for Aspose.CAD for Java?
  - answer: You can buy a license [here](https://purchase.aspose.com/buy).
    question: Where can I purchase a license for Aspose.CAD for Java?
  type: FAQPage
second_title: Aspose.CAD Java API
title: Cara Mengekspor DGN ke JPEG dengan Aspose.CAD for Java
url: /id/java/dgn-export-options/exporting-dgn-to-raster-image/
weight: 13
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Tutorial Konversi Java DGN ke JPEG dengan Aspose.CAD

## Pendahuluan

Pada panduan komprehensif ini Anda akan menemukan **how to export dgn** file ke gambar JPEG menggunakan Aspose.CAD untuk Java. Baik Anda membangun layanan pemrosesan batch atau menambahkan pembuatan pratinjau secara langsung ke penampil CAD, tutorial ini memandu Anda melalui setiap langkah, mulai dari memuat file sumber hingga menyimpan output raster. Anda juga akan melihat tip praktis yang membuat kode Anda bersih dan berkinerja baik.

## Jawaban Cepat
- **Perpustakaan apa yang saya butuhkan?** Aspose.CAD for Java (download [here](https://releases.aspose.com/cad/java/)).
- **Bisakah saya mengonversi DGN ke JPEG dalam satu baris?** Ya – muat dengan `CadImage.load` dan panggil `save` dengan `JpegOptions`.
- **Apakah lisensi diperlukan untuk produksi?** Ya, lisensi komersial menghilangkan watermark evaluasi.
- **Versi Java apa yang didukung?** Java 8 sampai 17 didukung sepenuhnya.
- **Seberapa besar DGN yang dapat saya proses?** File hingga 2 GB dapat ditangani tanpa memuat seluruh file ke memori.

## Apa itu “how to export dgn”?
*“How to export dgn”* merujuk pada proses mengonversi file desain MicroStation DGN ke format lain, biasanya gambar raster seperti JPEG, untuk memudahkan penampilan atau berbagi. Konversi ini memungkinkan pemangku kepentingan yang tidak memiliki perangkat lunak CAD untuk memeriksa desain, menyisipkan gambar dalam dokumen, atau menghasilkan thumbnail untuk galeri web, meningkatkan aksesibilitas dan kolaborasi antar tim.

## Mengapa menggunakan Aspose.CAD untuk Java?
Aspose.CAD mendukung **lebih dari 30 format CAD** (termasuk DGN, DWG, DXF) dan dapat merender file **hingga 2 GB** tanpa memerlukan aplikasi CAD asli. Mesin rasternya memproses gambar multi‑halaman dengan **> 50 fps** pada perangkat keras server standar, menghasilkan output JPEG berkualitas tinggi dengan satu panggilan API.

## Prasyarat

Sebelum memulai, pastikan Anda memiliki:

1. **Aspose.CAD Library** – unduh JAR terbaru dari situs resmi [here](https://releases.aspose.com/cad/java/). Anda juga dapat menjelajahi rilis produk lainnya [here](https://releases.aspose.com/).  
2. **Java Development Kit (JDK)** – Java 8 atau yang lebih baru terpasang di mesin Anda.  
3. **IDE** – IntelliJ IDEA, Eclipse, atau editor kompatibel Java apa pun yang Anda sukai.

## Impor Paket

Dalam proyek Java Anda, impor kelas Aspose.CAD yang diperlukan:

```java
import java.io.FileNotFoundException;
import java.io.FileOutputStream;
import java.io.OutputStream;
import com.aspose.cad.Image;
import com.aspose.cad.ImageOptionsBase;
import com.aspose.cad.fileformats.dgn.DgnImage;
import com.aspose.cad.imageoptions.CadRasterizationOptions;
import com.aspose.cad.imageoptions.JpegOptions;
```

## Cara mengekspor dgn ke JPEG menggunakan Aspose.CAD di Java?

Kelas `CadImage` mewakili dokumen CAD yang dimuat ke memori, menyediakan metode untuk merender dan menyimpan.

Muat file DGN Anda dengan `CadImage.load("source.dgn")`, konfigurasikan `JpegOptions` (termasuk kualitas dan resolusi), tetapkan `RasterizationOptions` yang sesuai seperti dimensi halaman dan warna latar belakang, dan akhirnya panggil `image.save("output.jpg", jpegOptions)`. Alur tiga langkah ini menangani konversi vektor‑ke‑raster, mempertahankan ketebalan garis, dan menulis file JPEG berkualitas tinggi dalam kurang dari satu detik untuk gambar standar.

## Langkah 1: Muat File DGN

Kelas `CadImage` mewakili dokumen CAD yang dimuat ke memori.

```java
String dataDir = "Your Document Directory" + "ExportingDGN/";
DgnImage dgnImage = (DgnImage) Image.load(dataDir + "Nikon_D90_Camera.dgn");
```

## Langkah 2: Buat Objek JpegOptions

`JpegOptions` mendefinisikan pengaturan khusus untuk output JPEG, seperti kualitas kompresi dan resolusi.

```java
ImageOptionsBase options = new JpegOptions();
```

## Langkah 3: Tetapkan Opsi Rasterisasi

`RasterizationOptions` menentukan cara grafik vektor di‑rasterisasi, termasuk ukuran halaman, DPI, warna latar belakang, dan anti‑aliasing.

```java
CadRasterizationOptions vectorOptions = new CadRasterizationOptions();
vectorOptions.setPageWidth(600);
vectorOptions.setPageHeight(400);
vectorOptions.setNoScaling(true);
vectorOptions.setAutomaticLayoutsScaling(false);
options.setVectorRasterizationOptions(vectorOptions);
```

## Langkah 4: Simpan Gambar yang Dikonversi

Memanggil `save` menulis gambar raster ke disk menggunakan opsi yang Anda berikan.

```java
OutputStream outStream = new FileOutputStream(dataDir + "ExportDGNToRasterImage_Out.jpg");
dgnImage.save(outStream, options);
```

### Kasus Penggunaan Umum

- **Pembuatan pratinjau web** – Konversi gambar teknik ke thumbnail JPEG ringan untuk tampilan cepat di browser.  
- **Arsip batch** – Otomatiskan konversi ribuan file DGN ke JPEG untuk penyimpanan jangka panjang tanpa memerlukan MicroStation.  
- **Pelaporan** – Sisipkan snapshot CAD ke dalam laporan PDF atau HTML langsung dari kode Java.

### Masalah Umum dan Solusinya

| Masalah | Solusi |
|-------|----------|
| **Gambar muncul kosong** | Pastikan `RasterizationOptions.setPageWidth/Height` sesuai dengan ekstensi gambar, dan atur latar belakang yang tidak transparan. |
| **Output kualitas rendah** | Tingkatkan `JpegOptions.setQuality(100)` dan atur DPI yang lebih tinggi (mis., `RasterizationOptions.setResolution(300)`). |
| **Kesalahan out‑of‑memory** | Gunakan `CadImage.load` dengan `loadOptions.setLoadMode(LoadMode.Memory)` untuk streaming file besar. |

## Pertanyaan yang Sering Diajukan

**T: Bisakah saya menggunakan Aspose.CAD untuk Java dengan format file CAD lainnya?**  
J: Ya, Aspose.CAD mendukung lebih dari 30 format vektor, termasuk DWG, DXF, DWF, dan SVG, memungkinkan satu API untuk banyak skenario konversi.

**T: Apakah ada percobaan gratis untuk Aspose.CAD untuk Java?**  
J: Ya, Anda dapat mengakses percobaan gratis [here](https://releases.aspose.com/).

**T: Di mana saya dapat menemukan dokumentasi untuk Aspose.CAD untuk Java?**  
J: Lihat dokumentasi resmi [here](https://reference.aspose.com/cad/java/).

**T: Bagaimana cara mendapatkan dukungan untuk Aspose.CAD untuk Java?**  
J: Kunjungi forum dukungan [here](https://forum.aspose.com/c/cad/19).

**T: Di mana saya dapat membeli lisensi untuk Aspose.CAD untuk Java?**  
J: Anda dapat membeli lisensi [here](https://purchase.aspose.com/buy).

**Terakhir Diperbarui:** 2026-05-25  
**Diuji Dengan:** Aspose.CAD 24.11 untuk Java  
**Penulis:** Aspose

## Tutorial Terkait

- [Ekspor DGN ke PDF AutoCAD dengan Mudah menggunakan Aspose.CAD untuk Java](/cad/java/dgn-export-options/exporting-dgn-to-pdf/)
- [Ekspor DGN ke DWG dengan Aspose.CAD untuk Java – Tutorial](/cad/java/dgn-export-options/)
- [Simpan CAD sebagai PNG – Konversi Gambar CAD ke Format Gambar Raster Menggunakan Aspose.CAD untuk Java](/cad/java/cad-drawing-conversion/convert-cad-drawing-to-raster-image/)


{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}