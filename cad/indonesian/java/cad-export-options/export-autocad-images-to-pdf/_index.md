---
date: 2026-02-20
description: Pelajari cara mengekspor PDF AutoCAD menggunakan Aspose.CAD untuk Java.
  Panduan langkah demi langkah ini menunjukkan cara **mengonversi DWG ke PDF**, **menyimpan
  CAD sebagai PDF**, dan menangani lisensi.
linktitle: Export AutoCAD Images to PDF
second_title: Aspose.CAD Java API
title: Konversi DWG ke PDF - Ekspor Gambar AutoCAD ke PDF dengan Aspose.CAD untuk
  Java
url: /id/java/cad-export-options/export-autocad-images-to-pdf/
weight: 10
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Ekspor PDF AutoCAD - Ekspor Gambar AutoCAD ke PDF dengan Aspose.CAD untuk Java

## Pendahuluan

Apakah Anda ingin **mengonversi DWG ke PDF** menggunakan Java? Tidak perlu mencari lagi! Pada tutorial ini kami akan memandu Anda mengonversi gambar AutoCAD ke PDF dengan Aspose.CAD untuk Java, sebuah pustaka kuat yang membuat proses **convert DWG to PDF** menjadi mudah. Pada akhir tutorial Anda akan memahami cara **save CAD as PDF**, menerapkan pengaturan rasterisasi khusus, dan bekerja dengan lisensi Aspose.CAD untuk penggunaan produksi.

## Jawaban Cepat
- **Apakah saya dapat mengonversi DWG ke PDF dengan Java?** Ya, Aspose.CAD untuk Java menangani DWG, DXF, dan banyak format lainnya.  
- **Apakah saya memerlukan lisensi?** **Aspose CAD license** diperlukan untuk penggunaan tak terbatas; lisensi sementara tersedia untuk evaluasi.  
- **Versi Java apa yang didukung?** Java 8+ (pustaka kompatibel dengan semua JDK modern).  
- **Bisakah saya menyesuaikan ukuran halaman PDF?** Tentu – sesuaikan `pageWidth` dan `pageHeight` dalam opsi rasterisasi.  
- **Apakah rasterisasi 3‑D memungkinkan?** Ya, aktifkan `TypeOfEntities.Entities3D` untuk rendering 3‑D penuh.

## Apa itu **export autocad pdf**?
Mengekspor PDF AutoCAD berarti mengonversi gambar CAD berbasis vektor (DWG, DXF, DWF, dll.) menjadi dokumen PDF portabel sambil mempertahankan lapisan, ketebalan garis, dan secara opsional geometri 3‑D. Ini berguna untuk berbagi desain dengan klien, mengarsipkan, atau mencetak tanpa memerlukan perangkat lunak CAD.

## Mengapa Mengonversi DWG ke PDF dengan Aspose.CAD untuk Java?
- **Dukungan format lengkap** – bekerja dengan DWG, DXF, DWF, dan banyak lagi.  
- **Tanpa ketergantungan eksternal** – pustaka Java murni, tanpa DLL native.  
- **Rasterisasi berkualitas tinggi** – kontrol atas DPI, ukuran halaman, dan tata letak, sehingga Anda dapat **customize PDF page size** sesuai kebutuhan proyek.  
- **Fleksibilitas lisensi** – mulai dengan percobaan gratis, kemudian tingkatkan ke **Aspose CAD license** permanen.  

## Prasyarat

Sebelum memulai, pastikan Anda memiliki:

- **Lingkungan Pengembangan Java** – JDK 8 atau lebih baru terpasang.  
- **Aspose.CAD untuk Java Library** – unduh dari [download link](https://releases.aspose.com/cad/java/).  
- **Direktori Dokumen** – sebuah folder di mesin Anda tempat file CAD sumber dan PDF yang dihasilkan akan disimpan.

## Impor Namespace

Di proyek Java Anda, impor kelas yang diperlukan untuk bekerja dengan Aspose.CAD:

```java
import com.aspose.cad.Image;

import com.aspose.cad.imageoptions.CadRasterizationOptions;
import com.aspose.cad.imageoptions.PdfOptions;
//import com.aspose.cad.imageoptions.TypeOfEntities;
```

Sekarang mari kita bahas kode langkah demi langkah.

## Cara mengonversi DWG ke PDF dengan Aspose.CAD untuk Java

### Langkah 1: Atur Jalur Direktori Sumber Daya

```java
String dataDir = "Your Document Directory" + "ExportingCAD/";
```

> **Tip profesional:** Ganti `"Your Document Directory"` dengan jalur absolut ke folder yang Anda buat pada bagian prasyarat.

### Langkah 2: Muat Gambar CAD

```java
String srcFile = dataDir + "conic_pyramid.dxf";
Image cadImage = Image.load(srcFile);
```

> **Mengapa ini penting:** Memuat file CAD ke dalam objek `Image` memberi Anda akses penuh ke mesin rasterisasi Aspose.CAD.

### Langkah 3: Atur Opsi Rasterisasi

```java
CadRasterizationOptions rasterizationOptions = new CadRasterizationOptions();
rasterizationOptions.setPageWidth(500);
rasterizationOptions.setPageHeight(500);
// rasterizationOptions.setTypeOfEntities(TypeOfEntities.Entities3D);

rasterizationOptions.setLayouts(new String[] {"Model"});
```

- Sesuaikan `pageWidth` dan `pageHeight` untuk **customize PDF page size**.  
- Hapus komentar pada baris `setTypeOfEntities` jika Anda memerlukan **java convert cad pdf** untuk entitas 3‑D.  
- Pemanggilan `setLayouts` memilih layout (Model, Layout1, dll.) yang akan dirender.

### Langkah 4: Konfigurasikan Opsi PDF

```java
PdfOptions pdfOptions = new PdfOptions();
pdfOptions.setVectorRasterizationOptions(rasterizationOptions);
```

Ini mengaitkan pengaturan rasterisasi dengan output PDF, memastikan data vektor dikonversi dengan benar.

### Langkah 5: Simpan PDF

```java
cadImage.save(dataDir + "Export3DImagestoPDF_out_.pdf", pdfOptions);
```

File yang dihasilkan, `Export3DImagestoPDF_out_.pdf`, merupakan representasi **save cad as pdf** dari gambar AutoCAD asli Anda.

## Masalah Umum & Solusi

| Gejala | Penyebab Kemungkinan | Solusi |
|--------|----------------------|--------|
| PDF kosong | Opsi rasterisasi tidak diatur atau layout tidak cocok | Verifikasi `setLayouts` sesuai dengan nama layout di file CAD Anda. |
| Gambar beresolusi rendah | `pageWidth`/`pageHeight` terlalu kecil | Tingkatkan dimensi atau set DPI lebih tinggi lewat `rasterizationOptions.setResolution(...)`. |
| Pengecualian lisensi | Tidak ada lisensi yang valid diterapkan | Terapkan **Aspose CAD license** atau gunakan lisensi sementara untuk pengujian. |

## Pertanyaan yang Sering Diajukan

### Q1: Bisakah saya menggunakan Aspose.CAD untuk Java dengan format file CAD lain?
A1: Ya, Aspose.CAD mendukung berbagai format termasuk DWG, DWF, DGN, dan lainnya, memberi Anda fleksibilitas dalam proyek.

### Q2: Bagaimana cara mendapatkan lisensi sementara untuk Aspose.CAD untuk Java?
A2: Kunjungi [di sini](https://purchase.aspose.com/temporary-license/) untuk memperoleh lisensi sementara untuk evaluasi.

### Q3: Apakah ada opsi layout untuk rasterisasi?
A3: Ya, Anda dapat menyesuaikan layout (misalnya `"Model"`, `"Layout1"`) melalui metode `setLayouts` untuk mengontrol tampilan yang dirender.

### Q4: Bisakah saya menyesuaikan ukuran file PDF output?
A4: Tentu! Sesuaikan parameter `pageWidth` dan `pageHeight` dalam opsi rasterisasi agar sesuai dengan dimensi yang diinginkan.

### Q5: Di mana saya dapat mencari bantuan atau berdiskusi mengenai masalah Aspose.CAD untuk Java?
A5: Kunjungi [forum Aspose.CAD](https://forum.aspose.com/c/cad/19) untuk dukungan khusus dan diskusi komunitas.

---

**Terakhir Diperbarui:** 2026-02-20  
**Diuji Dengan:** Aspose.CAD untuk Java 24.10  
**Penulis:** Aspose  

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}