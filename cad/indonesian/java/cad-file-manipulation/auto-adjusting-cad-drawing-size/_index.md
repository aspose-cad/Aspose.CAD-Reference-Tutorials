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

## Introduction

Jika Anda mencari cara yang jelas dan dapat diandalkan untuk **how to export cad** file dari Java, Anda berada di tempat yang tepat. Dengan Aspose.CAD for Java Anda tidak hanya dapat menyesuaikan ukuran gambar secara otomatis tetapi juga **convert DWG to BMP** dalam beberapa baris kode. Tutorial ini memandu Anda melalui seluruh proses, mulai dari menyiapkan lingkungan hingga menghasilkan gambar BMP yang mempertahankan tata letak CAD asli.

## Quick Answers
- **What does “how to export cad” mean?** Ini merujuk pada mengonversi file CAD (DWG, DXF, dll.) ke format lain seperti BMP, PNG, atau PDF.  
- **Which library handles the conversion?** Aspose.CAD for Java menyediakan API sederhana untuk tugas ini.  
- **Do I need a license?** Lisensi sementara cukup untuk pengujian; lisensi penuh diperlukan untuk produksi.  
- **Can I export multiple layouts at once?** Ya – dengan mengatur properti `Layouts` Anda dapat menentukan layout mana yang akan dirender.  
- **Is BMP the only output format?** Tidak – Anda juga dapat mengekspor ke PNG, JPEG, TIFF, dan lainnya.

## What is “how to export cad” with Aspose.CAD?
Mengekspor CAD berarti mengambil gambar CAD asli (misalnya file DWG) dan merendernya menjadi gambar raster atau format vektor lain. Aspose.CAD menangani semua proses berat: mem-parsing struktur CAD, merasterisasi entitas vektor, dan menulis hasil ke format gambar pilihan Anda.

## Why use Aspose.CAD for Java to **convert DWG to BMP**?
- **No external dependencies** – murni Java, tanpa DLL native.  
- **Full support for DWG, DXF, DGN, dan format lainnya**.  
- **Fine‑grained control** atas opsi rasterisasi seperti pemilihan layout, skala, dan warna latar belakang.  
- **High performance** cocok untuk pemrosesan batch di server.

## Prerequisites

Sebelum Anda mulai, pastikan Anda memiliki hal berikut:

1. **Java Development Kit** – unduh di [here](https://www.java.com/en/download/).  
2. **Aspose.CAD for Java library** – dapatkan JAR terbaru dari [here](https://releases.aspose.com/cad/java/).  
3. **Sample CAD file** – file DWG (misalnya `sample.dwg`) yang ditempatkan di direktori dokumen proyek Anda.

## Import Namespaces

Di aplikasi Java Anda, sertakan namespace yang diperlukan untuk memanfaatkan fungsionalitas Aspose.CAD. Berikut contoh:

```java

import com.aspose.cad.Image;
import com.aspose.cad.ImageOptionsBase;

import com.aspose.cad.imageoptions.CadRasterizationOptions;
import com.aspose.cad.imageoptions.PngOptions;
```

Sekarang, mari kita uraikan proses **how to export cad** menjadi langkah‑langkah yang dapat dikelola.

## Step‑by‑Step Guide

### Step 1: Load the CAD Drawing

```java
String dataDir = "Your Document Directory" + "CADConversion/";
String sourceFilePath = dataDir + "sample.dwg";
Image objImage = Image.load(sourceFilePath);
```

Kami memuat file DWG sumber ke dalam objek `Image`, yang berfungsi sebagai titik masuk untuk semua operasi selanjutnya.

### Step 2: Create `BmpOptions`

```java
BmpOptions bmpOptions = new BmpOptions();
```

`BmpOptions` akan menyimpan pengaturan rasterisasi khusus untuk output BMP.

### Step 3: Configure Rasterization Settings

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

### Step 5: Export to BMP Format

```java
String outPath = sourceFilePath + ".bmp";
objImage.save(outPath, bmpOptions);
```

Memanggil `save` dengan `BmpOptions` yang telah dikonfigurasi akan menulis file BMP ke disk. Ini menyelesaikan alur kerja **convert DWG to BMP**.

## Common Issues and Solutions

| Issue | Reason | Fix |
|-------|--------|-----|
| Output image is blank | Nama layout salah atau layout tidak ada | Verifikasi nama layout cocok dengan file CAD (mis., `"Model"`). |
| Low resolution | DPI default terlalu rendah | Set `cadRasterizationOptions.setResolution(300);` sebelum menyimpan. |
| Out‑of‑memory error for large files | Gambar besar memerlukan lebih banyak heap | Tingkatkan ukuran heap JVM (`-Xmx2g`) atau proses halaman secara terpisah. |

## Frequently Asked Questions

**Q: Is Aspose.CAD compatible with different CAD file formats?**  
A: Yes, Aspose.CAD supports DWG, DXF, DGN, and many other formats.

**Q: Can I use Aspose.CAD for commercial projects?**  
A: Absolutely. Purchase a license [here](https://purchase.aspose.com/buy) for production use.

**Q: How do I obtain a temporary license for testing?**  
A: You can get a temporary license [here](https://purchase.aspose.com/temporary-license/).

**Q: Where can I find community support?**  
A: Join the Aspose.CAD community forum at [forum](https://forum.aspose.com/c/cad/19).

**Q: Is there a free trial available for Aspose.CAD for Java?**  
A: Yes, download the free trial [here](https://releases.aspose.com/).

## Conclusion

Dalam panduan ini kami menunjukkan **how to export cad** file dari Java dan **convert DWG to BMP** menggunakan Aspose.CAD. Dengan mengikuti lima langkah di atas, Anda dapat mengintegrasikan konversi CAD‑ke‑gambar ke dalam aplikasi Java apa pun, baik itu alat desktop, layanan web, atau pipeline pemrosesan batch. Jelajahi format output lain (PNG, JPEG, PDF) dengan mengganti kelas opsi, dan manfaatkan set fitur lengkap Aspose.CAD untuk memenuhi semua kebutuhan manipulasi CAD Anda.

---

**Last Updated:** 2025-12-22  
**Tested With:** Aspose.CAD for Java 24.12  
**Author:** Aspose  

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}