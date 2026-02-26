---
date: 2026-01-10
description: Pelajari cara membuat JPEG dari file DGN menggunakan Aspose.CAD untuk
  Java. Tutorial langkah demi langkah ini menunjukkan cara mengonversi DGN ke JPEG
  secara efisien.
linktitle: Exporting DGN in AutoCAD Format to Raster Image Format
second_title: Aspose.CAD Java API
title: Cara membuat JPEG dari DGN menggunakan Aspose.CAD untuk Java
url: /id/java/dgn-export-options/exporting-dgn-to-raster-image/
weight: 13
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Buat JPEG dari DGN menggunakan Aspose.CAD untuk Java

## Pendahuluan

Dalam panduan komprehensif ini Anda akan **membuat JPEG dari DGN** dengan hanya beberapa baris kode Java. Baik Anda sedang membangun alat konversi batch atau perlu menampilkan gambar CAD sebagai gambar yang ramah web, mengonversi DGN ke JPEG adalah kebutuhan umum untuk banyak alur kerja teknik dan desain. Kami akan membahas setiap langkah—dari menyiapkan pustaka Aspose.CAD hingga menyimpan gambar raster akhir—sehingga Anda dapat mengintegrasikan solusi ini ke dalam aplikasi Anda segera.

## Jawaban Cepat
- **Perpustakaan apa yang dibutuhkan?** Aspose.CAD untuk Java  
- **Bisakah saya mengonversi format CAD lain ke JPEG?** Ya, Aspose.CAD mendukung banyak format (lihat kata kunci sekunder *convert cad to jpeg*)  
- **Apakah saya memerlukan lisensi untuk produksi?** Lisensi komersial diperlukan untuk penggunaan non‑trial  
- **Versi Java apa yang didukung?** Java 8 atau lebih baru  
- **Berapa lama konversi tipikal berlangsung?** Biasanya kurang dari satu detik untuk gambar berukuran standar  

## Apa itu “create JPEG from DGN”?
Membuat JPEG dari file DGN berarti meraster gambar vektor DGN menjadi gambar berbasis piksel (JPEG). Proses ini mempertahankan kesetiaan visual sambil menghasilkan file ringan yang dapat ditampilkan di peramban, email, atau laporan tanpa memerlukan perangkat lunak CAD.

## Mengapa mengonversi DGN ke JPEG?
- **Berbagi mudah:** JPEG dapat dilihat secara universal di perangkat apa pun.  
- **Kinerja:** Gambar raster memuat lebih cepat di halaman web dibandingkan file CAD vektor.  
- **Kompatibilitas:** Banyak alat hilir (mis., mesin pelaporan) hanya menerima format raster.  

## Prasyarat

Sebelum memulai, pastikan Anda memiliki hal‑hal berikut:

1. **Aspose.CAD Library** – Unduh dari situs resmi **[di sini](https://releases.aspose.com/cad/java/)**.  
2. **Java Development Kit (JDK)** – Java 8 atau lebih baru terpasang di mesin Anda.  
3. **IDE** – IDE yang kompatibel dengan Java seperti IntelliJ IDEA atau Eclipse.  

## Impor Paket

Tambahkan impor yang diperlukan ke kelas Java Anda:

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

## Panduan Langkah‑demi‑Langkah

### Langkah 1: Muat File DGN

```java
String dataDir = "Your Document Directory" + "ExportingDGN/";
DgnImage dgnImage = (DgnImage) Image.load(dataDir + "Nikon_D90_Camera.dgn");
```

*Penjelasan:* Metode `Image.load` membaca file DGN sumber dan mengembalikan objek `DgnImage` yang kemudian dapat kita rasterisasi.

### Langkah 2: Buat Objek JpegOptions

```java
ImageOptionsBase options = new JpegOptions();
```

*Penjelasan:* `JpegOptions` memberi tahu Aspose.CAD bahwa format keluaran harus JPEG. Ini juga memungkinkan kita melampirkan pengaturan rasterisasi.

### Langkah 3: Konfigurasikan Pengaturan Rasterisasi

```java
CadRasterizationOptions vectorOptions = new CadRasterizationOptions();
vectorOptions.setPageWidth(600);
vectorOptions.setPageHeight(400);
vectorOptions.setNoScaling(true);
vectorOptions.setAutomaticLayoutsScaling(false);
options.setVectorRasterizationOptions(vectorOptions);
```

*Penjelasan:* Opsi‑opsi ini menentukan ukuran gambar yang dihasilkan dan mengontrol perilaku skala. Sesuaikan `PageWidth` dan `PageHeight` sesuai resolusi target Anda.

### Langkah 4: Simpan Gambar yang Dikonversi

```java
OutputStream outStream = new FileOutputStream(dataDir + "ExportDGNToRasterImage_Out.jpg");
dgnImage.save(outStream, options);
```

*Penjelasan:* Metode `save` menulis JPEG yang telah diraster ke aliran output yang ditentukan. Setelah langkah ini, Anda akan memiliki file JPEG siap pakai.

> **Pro tip:** Bungkus kode konversi dalam blok `try‑with‑resources` untuk memastikan aliran ditutup secara otomatis.

## Kasus Penggunaan Umum

- **Membuat thumbnail** untuk penjelajah file CAD.  
- **Menyisipkan gambar** ke dalam laporan PDF atau halaman HTML.  
- **Pemrosesan batch otomatis** arsip desain.  

## Pemecahan Masalah & Jebakan Umum

| Masalah | Penyebab | Solusi |
|-------|-------|-----|
| Gambar output kosong atau putih | Opsi rasterisasi tidak tepat (mis., `NoScaling` diset true dengan ukuran halaman yang tidak cocok) | Sesuaikan `PageWidth`/`PageHeight` atau set `NoScaling` ke false |
| Kesalahan out‑of‑memory untuk file DGN besar | Memuat file yang sangat besar tanpa streaming | Tingkatkan heap JVM (`-Xmx`) atau proses file dalam potongan lebih kecil |
| Kualitas JPEG tidak cukup | Kualitas JPEG default rendah | Gunakan `((JpegOptions)options).setQuality(100);` sebelum menyimpan |

## Pertanyaan yang Sering Diajukan

### Q1: Bisakah saya menggunakan Aspose.CAD untuk Java dengan format file CAD lain?

A1: Ya, Aspose.CAD mendukung beragam format, memungkinkan Anda **mengonversi CAD ke JPEG** serta banyak output raster atau vektor lainnya.

### Q2: Apakah ada percobaan gratis untuk Aspose.CAD untuk Java?

A2: Ya, Anda dapat mengakses percobaan gratis **[di sini](https://releases.aspose.com/)**.

### Q3: Di mana saya dapat menemukan dokumentasi untuk Aspose.CAD untuk Java?

A3: Lihat dokumentasi **[di sini](https://reference.aspose.com/cad/java/)**.

### Q4: Bagaimana cara mendapatkan dukungan untuk Aspose.CAD untuk Java?

A4: Kunjungi forum dukungan **[di sini](https://forum.aspose.com/c/cad/19)**.

### Q5: Di mana saya dapat membeli lisensi untuk Aspose.CAD untuk Java?

A5: Anda dapat membeli lisensi **[di sini](https://purchase.aspose.com/buy)**.

## Kesimpulan

Anda kini telah mempelajari cara **membuat JPEG dari DGN** menggunakan Aspose.CAD untuk Java. Dengan mengikuti langkah‑langkah di atas, Anda dapat dengan mulus mengintegrasikan konversi DGN‑ke‑JPEG ke dalam aplikasi Java apa pun, baik untuk alat desktop, layanan web, atau pipeline otomatis.

---

**Terakhir Diperbarui:** 2026-01-10  
**Diuji Dengan:** Aspose.CAD untuk Java 24.11 (terbaru pada saat penulisan)  
**Penulis:** Aspose  

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}