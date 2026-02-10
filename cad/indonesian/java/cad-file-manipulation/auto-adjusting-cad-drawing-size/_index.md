---
date: 2025-12-22
description: Pelajari cara mengekspor gambar CAD dan mengonversi DWG ke BMP dalam
  Java dengan Aspose.CAD. Ikuti panduan langkah demi langkah ini untuk manipulasi
  file CAD yang efisien.
linktitle: Auto Adjusting CAD Drawing Size
second_title: Aspose.CAD Java API
title: Cara Mengekspor Gambar CAD ke BMP Menggunakan Aspose.CAD untuk Java
url: /id/java/cad-file-manipulation/auto-adjusting-cad-drawing-size/
weight: 13
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Cara Mengekspor Gambar CAD ke BMP Menggunakan Aspise.CAD untuk Java

## Perkenalan

Jika Anda mencari cara yang jelas dan dapat diandalkan untuk **cara mengekspor file cad** dari Java, Anda berada di tempat yang tepat. Dengan Aspose.CAD untuk Java Anda tidak hanya dapat menyesuaikan ukuran gambar secara otomatis tetapi juga **mengonversi DWG ke BMP** dalam beberapa baris kode. Tutorial ini memandu Anda melalui seluruh proses, mulai dari menyiapkan lingkungan hingga menghasilkan gambar BMP yang mempertahankan tata letak CAD asli.

## Jawaban Cepat
- **Apa yang dimaksud dengan “cara mengekspor cad”?** Ini merujuk pada mengkonversi file CAD (DWG, DXF, dll.) ke format lain seperti BMP, PNG, atau PDF.
- **Perpustakaan mana yang menangani konversi?** Aspose.CAD for Java menyediakan API sederhana untuk tugas ini.
- **Apakah saya memerlukan lisensi?** Lisensi sementara cukup untuk pengujian; lisensi penuh diperlukan untuk produksi.
- **Dapatkah saya mengekspor beberapa tata letak sekaligus?** Ya – dengan mengatur properti `Layouts` Anda dapat menentukan tata letak mana yang akan dirender.
- **Apakah BMP satu-satunya format keluaran?** Tidak – Anda juga dapat mengekspor ke PNG, JPEG, TIFF, dan lainnya.

## Apa itu “cara mengekspor cad” dengan Aspose.CAD?
Mengekspor CAD berarti mengambil gambar CAD asli (misalnya file DWG) dan merendernya menjadi gambar raster atau format vektor lain. Aspose.CAD menangani semua proses berat: mem-parsing struktur CAD, merasterisasi entitas vektor, dan menulis hasil ke format gambar pilihan Anda.

## Mengapa menggunakan Aspose.CAD untuk Java untuk **mengonversi DWG ke BMP**?
- **Tidak ada ketergantungan eksternal** – murni Java, tanpa DLL asli.
- **Dukungan penuh untuk DWG, DXF, DGN, dan format lainnya**.
- **Kontrol halus** atas opsi rasterisasi seperti pemilihan tata letak, skala, dan warna latar belakang.
- **Kinerja tinggi** cocok untuk pengiriman batch di server.

## Prasyarat

Sebelum Anda mulai, pastikan Anda memiliki hal berikut:

1. **Java Development Kit** – unduh di [di sini](https://www.java.com/en/download/).
2. **Aspose.CAD untuk perpustakaan Java** – dapatkan JAR terbaru dari [di sini](https://releases.aspose.com/cad/java/).
3. **Sample CAD file** – file DWG (misalnya `sample.dwg`) yang ditempatkan di direktori dokumen proyek Anda.

## Impor Namespace

Di aplikasi Java Anda, sertakan namespace yang diperlukan untuk memanfaatkan fungsionalitas Aspose.CAD. Berikut contohnya:

```java

import com.aspose.cad.Image;
import com.aspose.cad.ImageOptionsBase;

import com.aspose.cad.imageoptions.CadRasterizationOptions;
import com.aspose.cad.imageoptions.PngOptions;
```

Sekarang, mari kita uraikan proses **how to export cad** menjadi langkah‑langkah yang dapat dikelola.

## Panduan Langkah demi Langkah

### Langkah 1: Muat Gambar CAD

```java
String dataDir = "Your Document Directory" + "CADConversion/";
String sourceFilePath = dataDir + "sample.dwg";
Image objImage = Image.load(sourceFilePath);
```

Kami memuat file DWG sumber ke dalam objek `Image`, yang berfungsi sebagai titik masuk untuk semua operasi selanjutnya.

### Langkah 2: Buat `BmpOptions`

```java
BmpOptions bmpOptions = new BmpOptions();
```

`BmpOptions` akan menyimpan pengaturan rasterisasi khusus untuk output BMP.

### Langkah 3: Konfigurasi Pengaturan Rasterisasi

```java
CadRasterizationOptions cadRasterizationOptions = new CadRasterizationOptions();
bmpOptions.setVectorRasterizationOptions(cadRasterizationOptions);
```

Di sini kami menghubungkan opsi rasterisasi ke opsi BMP, memungkinkan kontrol atas cara entitas CAD dirender.

### Step 4: Set the Layout(s) to Export

```java
cadRasterizationOptions.setLayouts(new String[]{"Model"});
```

Properti `Layouts` memberi tahu Aspose.CAD layout gambar mana yang akan disertakan. Dalam kebanyakan kasus, `"Model"` adalah layout utama yang ingin Anda konvers.

### Langkah 5: Ekspor ke Format BMP

```java
String outPath = sourceFilePath + ".bmp";
objImage.save(outPath, bmpOptions);
```

Memanggil `save` dengan `BmpOptions` yang telah dikonfigurasi akan menulis file BMP ke disk. Ini menyelesaikan alur kerja **convert DWG to BMP**.

## Masalah Umum dan Solusinya

| Edisi | Alasan | Perbaiki |
|-------|--------|-----|
| Gambar keluaran kosong | Nama layout salah atau layout tidak ada | Verifikasi nama layout cocok dengan file CAD (mis., `"Model"`). |
| Resolusi rendah | DPI default terlalu rendah | Setel `cadRasterizationOptions.setResolution(300);` sebelum menyimpan. |
| Kesalahan kehabisan memori untuk file besar | Gambar besar memerlukan lebih banyak heap | Tingkatkan ukuran heap JVM (`-Xmx2g`) atau proses halaman secara terpisah. |

## Pertanyaan yang Sering Diajukan

**T: Apakah Aspose.CAD kompatibel dengan format file CAD yang berbeda?**
J: Ya, Aspose.CAD mendukung DWG, DXF, DGN, dan banyak format lainnya.

**T: Bisakah saya menggunakan Aspose.CAD untuk proyek komersial?**
J: Tentu saja. Beli lisensi [di sini](https://purchase.aspose.com/buy) untuk penggunaan produksi.

**T: Bagaimana cara mendapatkan lisensi sementara untuk pengujian?**
J: Anda bisa mendapatkan lisensi sementara [di sini](https://purchase.aspose.com/temporary-license/).

**T: Di mana saya dapat menemukan dukungan komunitas?**
J: Bergabunglah dengan forum komunitas Aspose.CAD di [forum](https://forum.aspose.com/c/cad/19).

**T: Apakah ada uji coba gratis yang tersedia untuk Aspose.CAD untuk Java?**
J: Ya, unduh uji coba gratis [di sini](https://releases.aspose.com/).

## Kesimpulan

Dalam panduan ini kami menunjukkan **cara mengekspor file CAD** dari Java dan **mengonversi DWG ke BMP** menggunakan Aspose.CAD. Dengan mengikuti lima langkah di atas, Anda dapat mengintegrasikan konversi CAD‑ke‑gambar ke dalam aplikasi Java apa pun, baik itu alat desktop, layanan web, atau pipeline pemrosesan batch. Menjelajahi format output lain (PNG, JPEG, PDF) dengan mengganti kelas opsi, dan memanfaatkan set fitur lengkap Aspose.CAD untuk memenuhi semua kebutuhan manipulasi CAD Anda.

---

**Terakhir Diperbarui:** 22-12-2025
**Diuji Dengan:** Aspose.CAD untuk Java 24.12
**Penulis:** Beranggapan  

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}