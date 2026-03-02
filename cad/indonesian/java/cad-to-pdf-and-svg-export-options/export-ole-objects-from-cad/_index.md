---
date: 2026-03-02
description: Buka potensi Aspose.CAD untuk Java. Dengan mudah ekspor objek OLE dan
  **simpan CAD sebagai PNG**. Unduh sekarang untuk manajemen data CAD yang mulus.
linktitle: Export OLE Objects from CAD
second_title: Aspose.CAD Java API
title: Simpan CAD sebagai PNG – Ekspor Objek OLE Menggunakan Aspose.CAD untuk Java
url: /id/java/cad-to-pdf-and-svg-export-options/export-ole-objects-from-cad/
weight: 10
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Simpan CAD sebagai PNG – Ekspor OLE Objects Menggunakan Aspose.CAD untuk Java

## Pendahuluan

Di dunia dinamis Computer-Aided Design (CAD), mengelola dan mengekstrak objek OLE (Object Linking and Embedding) secara efisien—serta dapat **menyimpan CAD sebagai PNG**—sangat penting untuk alur kerja hilir seperti pelaporan, pratinjau web, atau arsip. Aspose.CAD untuk Java menyediakan solusi code‑first yang kuat yang memungkinkan Anda mengekspor objek OLE dan mengonversi gambar CAD ke gambar PNG berkualitas tinggi hanya dengan beberapa baris kode.

## Jawaban Cepat
- **Apa yang dilakukan Aspose.CAD?** Membaca, memanipulasi, dan mengonversi file CAD (DWG, DXF, DGN, dll.) tanpa memerlukan perangkat lunak CAD asli.  
- **Apakah saya dapat menyimpan CAD sebagai PNG?** Ya—gunakan `PngOptions` bersama dengan `CadRasterizationOptions` untuk merasterisasi layout apa pun.  
- **Bagaimana cara mengekspor objek OLE?** Muat file CAD dengan `Image.load` dan simpan setiap layout yang berisi OLE sebagai PNG.  
- **Apakah saya memerlukan lisensi?** Versi percobaan gratis tersedia; lisensi komersial menghapus batasan evaluasi.  
- **Versi Java apa yang diperlukan?** Java 8 atau yang lebih tinggi didukung sepenuhnya.

## Apa itu **simpan CAD sebagai PNG**?
Menyimpan CAD sebagai PNG berarti merasterisasi gambar CAD berbasis vektor menjadi gambar PNG berbasis piksel. Konversi ini berguna ketika Anda membutuhkan format ringan yang dapat dilihat secara universal untuk halaman web, aplikasi seluler, atau dokumentasi.

## Mengapa menggunakan Aspose.CAD untuk Java untuk **mengonversi CAD ke PNG**?
- **Tidak memerlukan instalasi CAD** – perpustakaan ini bekerja sepenuhnya di Java.  
- **Mempertahankan kesetiaan tata letak** – Anda dapat memilih layout tertentu, mengontrol DPI, dan mempertahankan kualitas garis.  
- **Pemrosesan batch** – iterasi atas banyak file dengan loop sederhana.  
- **Ekspor objek OLE** – konten OLE yang disematkan dalam file DWG/DXF secara otomatis dirender ke output PNG.

## Prasyarat

Sebelum memulai tutorial, pastikan Anda memiliki prasyarat berikut:

- **Lingkungan Java** – Pastikan Anda memiliki lingkungan pengembangan Java yang terpasang di mesin Anda.  
- **Aspose.CAD untuk Java** – Unduh dan instal perpustakaan Aspose.CAD untuk Java. Anda dapat menemukan perpustakaan tersebut di [tautan unduhan](https://releases.aspose.com/cad/java/).  
- **File CAD** – Siapkan file CAD yang berisi objek OLE yang ingin Anda ekspor.

## Impor Namespace

Untuk memulai, impor namespace yang diperlukan ke dalam proyek Java Anda. Namespace ini menyediakan kelas dan fungsionalitas penting untuk bekerja dengan file CAD menggunakan Aspose.CAD.

```java
import com.aspose.cad.Image;

import com.aspose.cad.fileformats.cad.CadImage;
import com.aspose.cad.imageoptions.CadRasterizationOptions;
import com.aspose.cad.imageoptions.PngOptions;
```

Sekarang, mari kita uraikan proses mengekspor objek OLE dari CAD menjadi beberapa langkah:

## Cara **menyimpan CAD sebagai PNG** dan mengekspor objek OLE

### Langkah 1: Atur Direktori Dokumen Anda

```java
String dataDir = "Your Document Directory" + "DWGDrawings/";
```

Pastikan mengganti `"Your Document Directory"` dengan jalur ke direktori yang berisi file CAD Anda.

### Langkah 2: Definisikan Nama File CAD

```java
String[] files = new String[] { "D ZD junior D10m H2m.dwg", "ZD - Senior D6m H2m45.dwg" };
```

Tentukan nama-nama file CAD yang ingin Anda proses dalam array `files`.

### Langkah 3: Atur Opsi Ekspor PNG

```java
PngOptions pngOptions = new PngOptions();
CadRasterizationOptions rasterizationOptions = new CadRasterizationOptions();
pngOptions.setVectorRasterizationOptions(rasterizationOptions);
rasterizationOptions.setLayouts(new String[] { "Layout1" });
```

Konfigurasikan opsi ekspor PNG, termasuk rasterisasi vektor dan pengaturan layout. Opsi‑opsi ini memungkinkan Anda **mengonversi CAD ke PNG** dengan kualitas yang diinginkan.

### Langkah 4: Iterasi Melalui File CAD

```java
for(String file : files)
{
    CadImage cadImage = (CadImage)Image.load(dataDir + file);
    cadImage.save(dataDir + file + "_out.png", pngOptions);
}
```

Iterasi melalui setiap file CAD yang ditentukan, muat menggunakan Aspose.CAD, dan simpan objek OLE sebagai gambar PNG. Loop ini menunjukkan cara sederhana untuk **mengonversi DWG ke PNG** secara massal.

## Masalah Umum dan Solusinya

| Masalah | Penyebab | Solusi |
|-------|-------|----------|
| **Output PNG kosong** | Nama layout tidak cocok | Verifikasi bahwa nama layout (`"Layout1"`) ada di DWG sumber. |
| **Grafik OLE tidak muncul** | Objek OLE disimpan di layout yang berbeda | Sertakan semua layout yang relevan dalam `rasterizationOptions.setLayouts(...)`. |
| **Kesalahan out‑of‑memory pada file besar** | Pengaturan DPI tinggi | Kurangi DPI melalui `rasterizationOptions.setResolution(...)` atau proses file satu per satu. |

## Pertanyaan yang Sering Diajukan

**T: Apakah Aspose.CAD kompatibel dengan semua format file CAD?**  
J: Aspose.CAD mendukung berbagai format CAD, termasuk DWG, DXF, dan DGN. Lihat [dokumentasi](https://reference.aspose.com/cad/java/) untuk daftar lengkap.

**T: Bisakah saya menyesuaikan pengaturan ekspor untuk objek OLE?**  
J: Ya, Aspose.CAD menyediakan opsi yang luas untuk menyesuaikan pengaturan ekspor, memungkinkan Anda menyesuaikan output sesuai kebutuhan spesifik.

**T: Apakah tersedia versi percobaan gratis untuk Aspose.CAD?**  
J: Ya, Anda dapat menjelajahi kemampuan Aspose.CAD dengan mendapatkan versi percobaan gratis dari [sini](https://releases.aspose.com/).

**T: Di mana saya dapat mendapatkan dukungan komunitas untuk Aspose.CAD?**  
J: Bergabunglah dengan komunitas Aspose.CAD di [forum](https://forum.aspose.com/c/cad/19) untuk meminta bantuan dan berbagi pengalaman.

**T: Bagaimana cara membeli lisensi untuk Aspose.CAD?**  
J: Kunjungi [halaman pembelian](https://purchase.aspose.com/buy) untuk memperoleh lisensi yang sesuai dengan kebutuhan pengembangan Anda.

## Kesimpulan

Dengan langkah‑langkah sederhana namun kuat ini, Anda dapat dengan mulus **menyimpan CAD sebagai PNG** sambil mengekspor objek OLE dari file CAD menggunakan Aspose.CAD untuk Java. Alat serbaguna ini memberdayakan pengembang untuk mengelola data CAD secara efisien, membuka peluang baru dalam pengembangan aplikasi CAD dan alur kerja berbasis gambar hilir.

---

**Terakhir Diperbarui:** 2026-03-02  
**Diuji Dengan:** Aspose.CAD untuk Java 24.12  
**Penulis:** Aspose  

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}