---
date: 2025-12-19
description: Pelajari cara mengekspor PDF AutoCAD menggunakan Aspose.CAD untuk Java.
  Panduan langkah demi langkah ini menunjukkan cara mengonversi DWG ke PDF, menyimpan
  CAD sebagai PDF, dan menangani lisensi.
linktitle: Export AutoCAD Images to PDF
second_title: Aspose.CAD Java API
title: Ekspor PDF AutoCAD - Ekspor Gambar AutoCAD ke PDF dengan Tutorial Aspose.CAD
  untuk Java
url: /id/java/cad-export-options/export-autocad-images-to-pdf/
weight: 10
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Ekspor PDF AutoCAD - Ekspor Gambar AutoCAD ke PDF dengan Aspose.CAD untuk Java

## Introduction

Apakah Anda ingin dengan mudah **mengekspor PDF AutoCAD** menggunakan Java? Tidak perlu mencari lagi! Dalam tutorial ini kami akan memandu Anda melalui proses mengonversi gambar AutoCAD ke PDF dengan Aspose.CAD untuk Java, sebuah pustaka kuat yang membuat proses **mengonversi DWG ke PDF** menjadi mudah. Pada akhir tutorial Anda akan memahami cara **menyimpan CAD sebagai PDF**, menerapkan pengaturan rasterisasi khusus, dan menggunakan lisensi Aspose.CAD untuk penggunaan produksi.

## Quick Answers
- **Apakah saya dapat mengonversi DWG ke PDF dengan Java?** Ya, Aspose.CAD untuk Java menangani DWG, DXF, dan banyak format lainnya.  
- **Apakah saya memerlukan lisensi?** Sebuah **lisensi Aspose CAD** diperlukan untuk penggunaan tak terbatas; lisensi sementara tersedia untuk evaluasi.  
- **Versi Java apa yang didukung?** Java 8+ (pustaka ini kompatibel dengan semua JDK modern).  
- **Bisakah saya menyesuaikan ukuran halaman PDF?** Tentu – sesuaikan `pageWidth` dan `pageHeight` dalam opsi rasterisasi.  
- **Apakah rasterisasi 3‑D memungkinkan?** Ya, aktifkan `TypeOfEntities.Entities3D` untuk rendering 3‑D penuh.

## What is **export autocad pdf**?
Apa itu **export autocad pdf**?  
Mengekspor PDF AutoCAD berarti mengonversi gambar CAD berbasis vektor (DWG, DXF, DWF, dll.) menjadi dokumen PDF yang dapat dibawa ke mana saja sambil mempertahankan lapisan, ketebalan garis, dan secara opsional geometri 3‑D. Hal ini berguna untuk berbagi desain dengan klien, mengarsipkan, atau mencetak tanpa memerlukan perangkat lunak CAD.

## Why use Aspose.CAD for Java to **export autocad pdf**?
- **Dukungan format lengkap** – bekerja dengan DWG, DXF, DWF, dan banyak lagi.  
- **Tanpa ketergantungan eksternal** – pustaka murni Java, tanpa DLL native.  
- **Rasterisasi berkualitas tinggi** – kontrol atas DPI, ukuran halaman, dan tata letak.  
- **Fleksibilitas lisensi** – mulai dengan percobaan gratis, kemudian tingkatkan ke **lisensi Aspose CAD** permanen.  

## Prerequisites

Sebelum memulai, pastikan Anda memiliki:

- **Lingkungan Pengembangan Java** – JDK 8 atau yang lebih baru terpasang.  
- **Pustaka Aspose.CAD untuk Java** – unduh dari [download link](https://releases.aspose.com/cad/java/).  
- **Direktori Dokumen** – sebuah folder di mesin Anda tempat file CAD sumber dan PDF yang dihasilkan akan disimpan.

## Import Namespaces

Dalam proyek Java Anda, impor kelas yang diperlukan untuk bekerja dengan Aspose.CAD:

```java
import com.aspose.cad.Image;

import com.aspose.cad.imageoptions.CadRasterizationOptions;
import com.aspose.cad.imageoptions.PdfOptions;
//import com.aspose.cad.imageoptions.TypeOfEntities;
```

Sekarang mari kita bahas kode langkah demi langkah.

## Step‑by‑Step Guide

### Step 1: Set the Resource Directory Path

```java
String dataDir = "Your Document Directory" + "ExportingCAD/";
```

> **Pro tip:** Ganti `"Your Document Directory"` dengan path absolut ke folder yang Anda buat pada prasyarat.

### Step 2: Load the CAD Image

```java
String srcFile = dataDir + "conic_pyramid.dxf";
Image cadImage = Image.load(srcFile);
```

> **Why this matters:** Memuat file CAD ke dalam objek `Image` memberi Anda akses penuh ke mesin rasterisasi Aspose.CAD.

### Step 3: Set Rasterization Options

```java
CadRasterizationOptions rasterizationOptions = new CadRasterizationOptions();
rasterizationOptions.setPageWidth(500);
rasterizationOptions.setPageHeight(500);
// rasterizationOptions.setTypeOfEntities(TypeOfEntities.Entities3D);

rasterizationOptions.setLayouts(new String[] {"Model"});
```

- Sesuaikan `pageWidth` dan `pageHeight` untuk mengubah ukuran PDF keluaran.  
- Hapus komentar pada baris `setTypeOfEntities` jika Anda memerlukan **java convert cad pdf** untuk entitas 3‑D.  
- Pemanggilan `setLayouts` memilih tata letak (Model, Layout1, dll.) yang akan dirender.

### Step 4: Configure PDF Options

```java
PdfOptions pdfOptions = new PdfOptions();
pdfOptions.setVectorRasterizationOptions(rasterizationOptions);
```

Ini menghubungkan pengaturan rasterisasi dengan output PDF, memastikan data vektor dikonversi dengan benar.

### Step 5: Save the PDF

```java
cadImage.save(dataDir + "Export3DImagestoPDF_out_.pdf", pdfOptions);
```

File yang dihasilkan, `Export3DImagestoPDF_out_.pdf`, merupakan representasi **save cad as pdf** dari gambar AutoCAD asli Anda.

## Common Issues & Solutions

| Gejala | Penyebab Kemungkinan | Solusi |
|---------|----------------------|--------|
| PDF kosong | Opsi rasterisasi tidak diatur atau tata letak tidak cocok | Verifikasi bahwa `setLayouts` sesuai dengan nama tata letak dalam file CAD Anda. |
| Gambar beresolusi rendah | `pageWidth`/`pageHeight` terlalu kecil | Tingkatkan dimensi atau tetapkan DPI yang lebih tinggi melalui `rasterizationOptions.setResolution(...)`. |
| Pengecualian lisensi | Tidak ada lisensi yang valid diterapkan | Terapkan **lisensi Aspose CAD** atau gunakan lisensi sementara untuk pengujian. |

## Frequently Asked Questions

### Q1: Bisakah saya menggunakan Aspose.CAD untuk Java dengan format file CAD lainnya?
A1: Ya, Aspose.CAD mendukung berbagai format termasuk DWG, DWF, DGN, dan lainnya, memberi Anda fleksibilitas dalam proyek.

### Q2: Bagaimana cara mendapatkan lisensi sementara untuk Aspose.CAD untuk Java?
A2: Kunjungi [di sini](https://purchase.aspose.com/temporary-license/) untuk memperoleh lisensi sementara untuk evaluasi.

### Q3: Apakah ada opsi tata letak untuk rasterisasi?
A3: Ya, Anda dapat menyesuaikan tata letak (misalnya `"Model"`, `"Layout1"`) melalui metode `setLayouts` untuk mengontrol tampilan mana yang dirender.

### Q4: Bisakah saya menyesuaikan ukuran file PDF keluaran?
A4: Tentu! Sesuaikan parameter `pageWidth` dan `pageHeight` dalam opsi rasterisasi agar sesuai dengan dimensi yang diinginkan.

### Q5: Di mana saya dapat mencari bantuan atau berdiskusi tentang masalah terkait Aspose.CAD untuk Java?
A5: Kunjungi [forum Aspose.CAD](https://forum.aspose.com/c/cad/19) untuk dukungan khusus dan diskusi komunitas.

---

**Terakhir Diperbarui:** 2025-12-19  
**Diuji Dengan:** Aspose.CAD untuk Java 24.10  
**Penulis:** Aspose  

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}