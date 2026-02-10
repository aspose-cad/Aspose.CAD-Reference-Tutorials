---
date: 2025-12-28
description: Pelajari cara membuat PDF dari CAD dengan mengonversi DWG ke PDF menggunakan
  Aspose.CAD untuk Java. Ikuti langkah‑demi‑langkah untuk mengekspor tata letak DWG
  ke PDF dan menghasilkan gambar.
linktitle: Render DWG Document to Image with Java
second_title: Aspose.CAD Java API
title: 'Buat PDF dari CAD - DWG ke Gambar dengan Aspose.CAD untuk Java'
url: /id/java/cad-meta-data-and-rendering/render-dwg-to-image/
weight: 11
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Render Dokumen DWG ke Gambar dengan Aspose.CAD untuk Java

## Pendahuluan

Di dunia pengembangan Java yang dinamis, Aspose.CAD menonjol sebagai alat yang kuat untuk menangani file Computer‑Aided Design (CAD). **Tutorial ini menunjukkan cara membuat PDF dari CAD** dengan merender dokumen DWG ke gambar dan kemudian mengekspornya ke PDF. Baik Anda seorang pengembang berpengalaman maupun baru memulai perjalanan coding, panduan langkah‑demi‑langkah ini akan memandu Anda melalui proses dengan jelas dan mudah.

## Jawaban Cepat
- **Perpustakaan apa yang saya perlukan?** Aspose.CAD untuk Java.
- **Apakah saya dapat mengonversi DWG ke PDF?** Ya – contoh ini mendemonstrasikan konversi layout DWG ke PDF.
- **Apakah saya memerlukan lisensi untuk produksi?** Lisensi Aspose.CAD yang valid diperlukan untuk penggunaan non‑evaluasi.
- **IDE mana yang didukung?** Eclipse, IntelliJ IDEA, NetBeans, dan IDE apa pun yang mendukung Java.
- **Format output apa yang tersedia?** PDF, PNG, JPEG, BMP, dan format raster lainnya.

## Apa itu membuat pdf dari cad?
Membuat PDF dari CAD berarti mengambil gambar berbasis vektor (seperti file DWG) dan meraster atau memvektorisasinya menjadi dokumen PDF. Ini memungkinkan berbagi, pencetakan, dan pengarsipan gambar teknis dengan mudah tanpa memerlukan aplikasi CAD asli.

## Mengapa menggunakan Aspose.CAD untuk Java?
- **Tanpa dependensi eksternal** – perpustakaan berfungsi langsung setelah dipasang.
- **Rendering berpresisi tinggi** – mempertahankan ketebalan garis, lapisan, dan layout.
- **Pemrosesan batch** – Anda dapat mengonversi banyak gambar dalam satu kali jalankan.
- **Lintas‑platform** – bekerja di Windows, Linux, dan macOS.

## Prasyarat

- **Lingkungan Pengembangan Java** – JDK 8 atau lebih tinggi terpasang.
- **Perpustakaan Aspose.CAD untuk Java** – unduh dari [tautan unduhan](https://releases.aspose.com/cad/java/).
- **Dokumen DWG** – file DWG yang ingin Anda render (contoh atau milik Anda sendiri).

## Impor Namespace

Di kode Java Anda, impor kelas yang diperlukan untuk memanfaatkan fungsionalitas Aspose.CAD:

```java
import com.aspose.cad.Image;

import com.aspose.cad.imageoptions.CadRasterizationOptions;
import com.aspose.cad.imageoptions.PdfOptions;
```

Sekarang, mari kita uraikan kode contoh menjadi beberapa langkah untuk pemahaman yang komprehensif:

## Langkah 1: Tentukan Direktori Sumber Daya

```java
// The path to the resource directory.
String dataDir = "Your Document Directory" + "DWGDrawings/";
```

Ganti `"Your Document Directory"` dengan jalur sebenarnya tempat file DWG Anda disimpan.

## Langkah 2: Muat Dokumen DWG

```java
String srcFile = dataDir + "visualization_-_conference_room.dwg";
Image image = Image.load(srcFile);
```

Ini memuat file DWG ke dalam objek `Image` yang dapat diproses oleh Aspose.CAD.

## Langkah 3: Atur Opsi Rasterisasi

```java
CadRasterizationOptions rasterizationOptions = new CadRasterizationOptions();
rasterizationOptions.setPageWidth(1600);
rasterizationOptions.setPageHeight(1600);
rasterizationOptions.setLayouts(new String[] {"Layout1"});
```

Di sini kita mendefinisikan bagaimana gambar harus dirasterisasi: ukuran halaman dan layout spesifik yang akan dirender. Ini adalah langkah kunci untuk **render dwg to image** dan untuk **export dwg layout pdf**.

## Langkah 4: Buat Opsi PDF

```java
PdfOptions pdfOptions = new PdfOptions();
pdfOptions.setVectorRasterizationOptions(rasterizationOptions);
```

`PdfOptions` mengaitkan pengaturan rasterisasi dengan format output PDF.

## Langkah 5: Ekspor ke PDF

```java
image.save(dataDir + "ExportSpecificLayoutToPDF_out_.pdf", pdfOptions);
```

Metode `save` menulis gambar yang telah dirender ke file PDF, secara efektif **convert dwg to pdf**.

## Masalah Umum dan Solusinya
| Masalah | Solusi |
|-------|----------|
| **File tidak ditemukan** | Pastikan `dataDir` mengarah ke folder yang benar dan nama file DWG sudah tepat. |
| **Output PDF kosong** | Pastikan nama layout (`"Layout1"`) ada dalam file DWG; gunakan `image.getAvailableLayouts()` untuk menampilkannya. |
| **Kualitas gambar rendah** | Tingkatkan `PageWidth` dan `PageHeight` atau setel `rasterizationOptions.setResolution(300);`. |

## Pertanyaan yang Sering Diajukan

### Q1: Bisakah saya merender beberapa layout dari satu file DWG?

A1: Ya, Anda dapat. Cukup ubah nama layout dalam array `setLayouts` sesuai kebutuhan.

### Q2: Apakah Aspose.CAD kompatibel dengan berbagai IDE Java?

A2: Ya, Aspose.CAD kompatibel dengan IDE Java populer seperti Eclipse, IntelliJ IDEA, dan lainnya.

### Q3: Di mana saya dapat menemukan bantuan dan dukungan tambahan?

A3: Kunjungi [forum Aspose.CAD](https://forum.aspose.com/c/cad/19) untuk dukungan komunitas dan diskusi.

### Q4: Bagaimana cara mendapatkan lisensi sementara untuk Aspose.CAD?

A4: Anda dapat memperoleh lisensi sementara dari [sini](https://purchase.aspose.com/temporary-license/).

### Q5: Apakah ada lebih banyak opsi rendering yang tersedia di Aspose.CAD?

A5: Tentu, jelajahi [dokumentasi](https://reference.aspose.com/cad/java/) yang luas untuk informasi detail.

---

**Terakhir Diperbarui:** 2025-12-28  
**Diuji Dengan:** Aspose.CAD untuk Java 24.11  
**Penulis:** Aspose  

---

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}
