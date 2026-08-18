---
date: 2026-02-28
description: Pelajari cara mengonversi DWG ke PDF dengan Aspose.CAD untuk Java, membuat
  file yang mematuhi PDF/A1a dan PDF/A1b dengan cepat dan akurat.
linktitle: DWG to Compliance PDF
second_title: Aspose.CAD Java API
title: Konversi DWG ke PDF (PDF/A1a & A1b) menggunakan Aspose.CAD untuk Java
url: /id/java/cad-to-pdf-and-svg-export-options/dwg-to-compliance-pdf/
weight: 11
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Mengonversi DWG ke PDF (PDF/A1a & A1b) menggunakan Aspose.CAD untuk Java

## Pendahuluan

Dalam alur kerja rekayasa dan desain modern, **convert DWG to PDF** adalah kebutuhan harian untuk berbagi, mengarsipkan, dan mematuhi format dokumen standar industri. PDF/A‑1a dan PDF/A‑1b adalah standar arsip yang paling banyak diterima, menjamin bahwa gambar Anda akan ditampilkan dengan cara yang sama pada sistem apa pun. Aspose.CAD untuk Java membuat konversi ini menjadi sederhana, dapat diandalkan, dan sepenuhnya dapat diprogram. Pada tutorial ini Anda akan belajar cara mengonversi file DWG ke PDF yang mematuhi PDF/A hanya dengan beberapa baris kode Java.

## Jawaban Cepat
- **Perpustakaan apa yang menangani konversi?** Aspose.CAD untuk Java  
- **Standar PDF/A mana yang didukung?** PDF/A‑1a dan PDF/A‑1b  
- **Apakah saya memerlukan lisensi untuk pengujian?** Ya – lisensi sementara tersedia dari Aspose.  
- **Versi Java minimum apa?** Java 8 atau lebih tinggi disarankan.  
- **Bisakah saya memproses batch banyak file DWG?** Tentu – ulangi langkah untuk setiap file atau lakukan loop melalui folder.

## Apa itu “convert DWG to PDF” dan mengapa penting?
Mengonversi gambar DWG ke PDF menghasilkan dokumen yang dapat dilihat secara universal sambil mempertahankan kesetiaan vektor. Ketika Anda memilih kepatuhan PDF/A‑1a atau PDF/A‑1b, file juga menyertakan profil warna, font, dan metadata yang diperlukan untuk arsip jangka panjang, yang penting untuk pengajuan regulasi, dokumentasi konstruksi, dan deliverable klien.

## Mengapa menggunakan Aspose.CAD untuk Java?
- **Dukungan penuh versi DWG** – dari R12 lama hingga rilis terbaru.  
- **Tanpa ketergantungan eksternal** – perpustakaan berfungsi langsung, tidak memerlukan perangkat lunak CAD.  
- **Kontrol detail** – Anda dapat mengatur opsi rasterisasi, DPI, ukuran halaman, dan kepatuhan PDF/A.  
- **Kinerja tinggi** – cocok untuk pemrosesan batch ribuan gambar.

## Prasyarat

Sebelum memulai, pastikan Anda memiliki:

- Lingkungan pengembangan Java (JDK 8 atau lebih baru) dengan IDE pilihan Anda.  
- Perpustakaan Aspose.CAD untuk Java – unduh dari [download link](https://releases.aspose.com/cad/java/).  
- Folder yang berisi gambar DWG yang ingin Anda konversi.

## Import Namespaces

Pertama, impor kelas yang diperlukan. Menempatkan import di bagian atas file membuat kode lebih mudah dibaca dan dipelihara.

```java
import com.aspose.cad.Image;

import com.aspose.cad.imageoptions.CadRasterizationOptions;
import com.aspose.cad.imageoptions.PdfCompliance;
import com.aspose.cad.imageoptions.PdfDocumentOptions;
import com.aspose.cad.imageoptions.PdfOptions;
```

## Langkah 1: Atur Direktori Sumber Daya

Tentukan jalur tempat file DWG Anda berada. Sesuaikan string untuk menunjuk ke direktori Anda yang sebenarnya.

```java
String dataDir = "Your Document Directory" + "DWGDrawings/";
```

## Langkah 2: Muat File DWG

Gunakan `Image.load` untuk membaca file DWG ke memori. Objek ini nanti akan disimpan sebagai PDF.

```java
String srcFile = dataDir + "Bottom_plate.dwg";
Image objImage = Image.load(srcFile);
```

## Langkah 3: Buat Opsi PDF

Buat instance `PdfOptions` dan lampirkan objek `CadRasterizationOptions`. Opsi rasterisasi memungkinkan Anda mengontrol bagaimana data vektor dirender di dalam PDF.

```java
PdfOptions pdfOptions = new PdfOptions();
pdfOptions.setVectorRasterizationOptions(new CadRasterizationOptions());
```

## Langkah 4: Atur Opsi PDF Inti (Kepatuhan)

Di sini Anda memberi tahu Aspose.CAD level kepatuhan PDF/A yang Anda butuhkan. Contoh dimulai dengan PDF/A‑1a.

```java
pdfOptions.setCorePdfOptions(new PdfDocumentOptions());
pdfOptions.getCorePdfOptions().setCompliance(PdfCompliance.PdfA1a);
```

## Langkah 5: Simpan PDF dengan Kepatuhan PDF/A‑1a

Sekarang tulis file PDF ke disk. File output akan mematuhi PDF/A‑1a, siap untuk arsip.

```java
objImage.save(dataDir + "Saved1.pdf", pdfOptions);
```

## Langkah 6: Ubah Kepatuhan ke PDF/A‑1b dan Simpan Lagi

Jika Anda memerlukan PDF/A‑1b, cukup ubah flag kepatuhan dan simpan file kedua.

```java
pdfOptions.getCorePdfOptions().setCompliance(PdfCompliance.PdfA1b);
objImage.save(dataDir + "Saved.pdf", pdfOptions);
```

> **Pro tip:** Bungkus logika konversi dalam metode yang dapat digunakan kembali sehingga Anda dapat memanggilnya untuk setiap DWG dalam folder, mengurangi boilerplate dan meningkatkan maintainability.

## Kasus Penggunaan Umum

| Skenario | Mengapa PDF/A? |
|----------|----------------|
| **Pengajuan regulasi** | Menjamin keterbacaan jangka panjang dan keabsahan hukum. |
| **Deliverable klien** | Klien dapat membuka file tanpa perangkat lunak CAD apa pun. |
| **Sistem manajemen dokumen** | File PDF/A dapat diindeks dan dicari di sebagian besar platform DMS. |

## Masalah Umum dan Solusinya

- **Font atau simbol yang hilang** – Pastikan file DWG menyertakan semua font yang diperlukan, atau atur `CadRasterizationOptions.setEmbedFonts(true)`.  
- **Ukuran file besar** – Kurangi DPI pada opsi rasterisasi atau aktifkan kompresi via `PdfDocumentOptions.setCompress(true)`.  
- **Lisensi tidak ditemukan** – Terapkan lisensi sementara atau permanen sebelum konversi; jika tidak, Anda akan mendapatkan watermark.

## Pertanyaan yang Sering Diajukan

**T: Apakah Aspose.CAD kompatibel dengan semua versi file DWG?**  
J: Aspose.CAD mendukung berbagai versi DWG, termasuk rilis terbaru. Lihat [documentation](https://reference.aspose.com/cad/java/) untuk daftar kompatibilitas lengkap.

**T: Bisakah saya menyesuaikan pengaturan output PDF?**  
J: Tentu! Opsi seperti ukuran halaman, DPI, rasterisasi vektor, dan kepatuhan PDF/A semuanya dapat dikonfigurasi melalui `PdfOptions` dan `CadRasterizationOptions`.

**T: Apakah lisensi sementara tersedia untuk pengujian?**  
J: Ya, Anda dapat memperoleh lisensi sementara untuk evaluasi dari [tautan ini](https://purchase.aspose.com/temporary-license/).

**T: Di mana saya dapat mendapatkan dukungan komunitas?**  
J: Forum [Aspose.CAD](https://forum.aspose.com/c/cad/19) adalah tempat yang bagus untuk mengajukan pertanyaan dan berbagi pengalaman.

**T: Bisakah saya mencoba Aspose.CAD secara gratis sebelum membeli?**  
J: Tentu! Unduh versi trial gratis dari [sini](https://releases.aspose.com/) untuk menjelajahi seluruh fitur.

---

**Terakhir Diperbarui:** 2026-02-28  
**Diuji Dengan:** Aspose.CAD untuk Java 24.11 (terbaru pada saat penulisan)  
**Penulis:** Aspose  

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}