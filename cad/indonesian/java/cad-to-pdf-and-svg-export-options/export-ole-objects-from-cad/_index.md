---
date: 2026-01-04
description: Pelajari cara **menyimpan CAD sebagai PNG** dan dengan mudah mengekspor
  objek OLE dari file CAD menggunakan Aspose.CAD untuk Java. Penyiapan cepat, contoh
  kode lengkap, dan tips praktik terbaik.
linktitle: Export OLE Objects from CAD
second_title: Aspose.CAD Java API
title: Simpan CAD sebagai PNG dan Ekspor Objek OLE dengan Aspose.CAD untuk Java
url: /id/java/cad-to-pdf-and-svg-export-options/export-ole-objects-from-cad/
weight: 10
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Simpan CAD sebagai PNG dan Ekspor OLE Objects dengan Aspose.CAD untuk Java

## Pendahuluan

Dalam dunia Computer‑Aided Design (CAD) yang bergerak cepat, kemampuan untuk **save CAD as PNG** sambil mengekstrak objek OLE (Object Linking and Embedding) yang tertanam dapat secara dramatis menyederhanakan alur kerja Anda. Apakah Anda sedang membangun alat konversi batch, menghasilkan thumbnail untuk portal web, atau sekadar perlu mengarsipkan konten OLE, Aspose.CAD untuk Java memberikan cara yang bersih dan programatis untuk melakukannya. Dalam tutorial ini kami akan memandu Anda melalui seluruh proses, mulai dari menyiapkan proyek hingga mengekspor setiap objek OLE sebagai gambar PNG.

## Jawaban Cepat
- **Apakah saya dapat mengekspor objek OLE langsung ke PNG?** Ya – Aspose.CAD memuat file CAD dan memungkinkan Anda meraster setiap layout ke PNG.  
- **Versi Java apa yang diperlukan?** Java 8 atau lebih baru.  
- **Apakah saya memerlukan lisensi untuk fitur ini?** Versi percobaan gratis dapat digunakan untuk evaluasi; lisensi diperlukan untuk produksi.  
- **Apakah data vektor akan dipertahankan?** Rasterisasi PNG mempertahankan kesetiaan visual, tetapi outputnya berupa raster, bukan vektor.  
- **Apakah pemrosesan batch didukung?** Tentu – iterasi melalui array file seperti yang ditunjukkan dalam contoh kode.

## Prasyarat

Sebelum memulai, pastikan Anda memiliki hal berikut:

- **Java Development Kit (JDK)** – Java 8+ terpasang dan dikonfigurasi.  
- **Aspose.CAD for Java** – Unduh pustaka terbaru dari [download link](https://releases.aspose.com/cad/java/).  
- **CAD source files** – File DWG/DXF/DGN apa pun yang berisi objek OLE yang ingin Anda ekspor.

## Impor Namespace

Untuk bekerja dengan file CAD Anda perlu mengimpor kelas inti Aspose.CAD. Pertahankan blok impor persis seperti yang ditunjukkan – blok tersebut menyediakan kelas yang akan digunakan nanti dalam tutorial.

```java
import com.aspose.cad.Image;

import com.aspose.cad.fileformats.cad.CadImage;
import com.aspose.cad.imageoptions.CadRasterizationOptions;
import com.aspose.cad.imageoptions.PngOptions;
```

## Cara Menyimpan CAD sebagai PNG

Berikut adalah panduan singkat langkah‑demi‑langkah yang menunjukkan **cara mengekspor objek OLE dan menyimpan CAD sebagai PNG**. Setiap langkah mencakup penjelasan singkat diikuti oleh kode tepat yang perlu Anda salin ke dalam proyek Anda.

### Langkah 1: Tetapkan Direktori Dokumen Anda

Tentukan folder yang berisi gambar CAD Anda. Ganti placeholder dengan jalur sebenarnya di mesin Anda.

```java
String dataDir = "Your Document Directory" + "DWGDrawings/";
```

### Langkah 2: Tentukan Nama File CAD

Daftar semua file CAD yang ingin Anda proses. Anda dapat menambahkan sebanyak yang diperlukan.

```java
String[] files = new String[] { "D ZD junior D10m H2m.dwg", "ZD - Senior D6m H2m45.dwg" };
```

### Langkah 3: Atur Opsi Ekspor PNG

Konfigurasikan pengaturan rasterisasi. Di sini kami menargetkan layout tertentu (`Layout1`) dan menggunakan opsi PNG default.

```java
PngOptions pngOptions = new PngOptions();
CadRasterizationOptions rasterizationOptions = new CadRasterizationOptions();
pngOptions.setVectorRasterizationOptions(rasterizationOptions);
rasterizationOptions.setLayouts(new String[] { "Layout1" });
```

### Langkah 4: Iterasi Melalui File CAD dan Simpan sebagai PNG

Muat setiap file CAD, rasterisasi objek OLE, dan tulis file PNG output. Akhiran `_out.png` membantu Anda mengidentifikasi gambar yang dihasilkan.

```java
for(String file : files)
{
    CadImage cadImage = (CadImage)Image.load(dataDir + file);
    cadImage.save(dataDir + file + "_out.png", pngOptions);
}
```

## Masalah Umum dan Solusinya

| Masalah | Mengapa Terjadi | Solusi |
|---------|----------------|--------|
| **`Image.load` throws `FileNotFoundException`** | Path `dataDir` tidak benar atau nama file memiliki typo. | Periksa kembali string direktori dan pastikan nama file cocok persis, termasuk spasi. |
| **Output PNG is blank** | Nama layout tidak ada dalam file CAD sumber. | Gunakan `cadImage.getLayouts()` untuk menampilkan layout yang tersedia, lalu perbarui `rasterizationOptions.setLayouts(...)`. |
| **Large CAD files cause OutOfMemoryError** | Rasterisasi gambar beresolusi tinggi mengonsumsi banyak memori heap. | Tingkatkan heap JVM (`-Xmx2g`) atau turunkan resolusi rasterisasi melalui `rasterizationOptions.setResolution(...)`. |

## FAQ

### Q1: Apakah Aspose.CAD kompatibel dengan semua format file CAD?

A1: Aspose.CAD mendukung berbagai format CAD, termasuk DWG, DXF, dan DGN. Lihat [documentation](https://reference.aspose.com/cad/java/) untuk daftar lengkap.

### Q2: Apakah saya dapat menyesuaikan pengaturan ekspor untuk objek OLE?

A2: Ya, Aspose.CAD menyediakan banyak opsi untuk menyesuaikan pengaturan ekspor, memungkinkan Anda menyesuaikan output sesuai kebutuhan spesifik Anda.

### Q3: Apakah tersedia versi percobaan gratis untuk Aspose.CAD?

A3: Ya, Anda dapat menjelajahi kemampuan Aspose.CAD dengan mendapatkan versi percobaan gratis dari [here](https://releases.aspose.com/).

### Q4: Di mana saya dapat mendapatkan dukungan komunitas untuk Aspose.CAD?

A4: Bergabunglah dengan komunitas Aspose.CAD di [forum](https://forum.aspose.com/c/cad/19) untuk meminta bantuan dan berbagi pengalaman Anda.

### Q5: Bagaimana cara membeli lisensi untuk Aspose.CAD?

A5: Kunjungi [purchase page](https://purchase.aspose.com/buy) untuk memperoleh lisensi yang sesuai dengan kebutuhan pengembangan Anda.

## Kesimpulan

Dengan mengikuti lima langkah sederhana ini, Anda dapat **save CAD as PNG** dan mengekstrak setiap objek OLE yang tertanam hanya dengan beberapa baris kode Java. Pendekatan ini ideal untuk konversi batch, pelaporan otomatis, atau skenario apa pun di mana Anda memerlukan gambar raster konten CAD tanpa ekspor manual. Jangan ragu untuk bereksperimen dengan opsi rasterisasi yang berbeda untuk menyesuaikan kebutuhan kualitas dan kinerja Anda.

---

**Terakhir Diperbarui:** 2026-01-04  
**Diuji Dengan:** Aspose.CAD for Java 24.12 (latest at time of writing)  
**Penulis:** Aspose  

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}