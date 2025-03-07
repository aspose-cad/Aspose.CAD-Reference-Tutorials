---
title: Konversi STL ke PNG Menjadi Mudah dengan Aspose.CAD untuk .NET
linktitle: Mengekspor File STL ke PNG
second_title: Aspose.CAD .NET - Format File CAD dan BIM
description: Konversi file STL ke PNG dengan mudah menggunakan Aspose.CAD untuk .NET. Ikuti panduan langkah demi langkah kami untuk integrasi yang lancar. Unduh sekarang!
weight: 10
url: /id/net/stl-file-export/exporting-stl-files-to-png/
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Konversi STL ke PNG Menjadi Mudah dengan Aspose.CAD untuk .NET

## Perkenalan
Dalam dunia desain berbantuan komputer (CAD) yang dinamis, konversi file yang efisien sangatlah penting. Aspose.CAD untuk .NET adalah toolkit canggih yang menyederhanakan proses mengekspor file STL ke PNG, memberikan fleksibilitas dan fungsionalitas yang dibutuhkan pengembang. Tutorial ini akan memandu Anda melalui proses langkah demi langkah, memastikan transisi yang lancar dari STL ke PNG menggunakan Aspose.CAD.
## Prasyarat
Sebelum kita masuk ke tutorialnya, pastikan Anda memiliki yang berikut ini:
1.  Aspose.CAD untuk .NET: Unduh dan instal perpustakaan Aspose.CAD. Kamu bisa menemukannya[Di Sini](https://releases.aspose.com/cad/net/).
2. Lingkungan Pengembangan: Siapkan lingkungan pengembangan .NET pilihan Anda.
3. File STL: Siapkan file STL untuk dikonversi. Untuk tutorial ini, kita akan menggunakan contoh file bernama "galeon.stl."
## Impor Namespace
Untuk memulai prosesnya, impor namespace yang diperlukan di aplikasi .NET Anda. Ini memastikan bahwa Anda memiliki akses ke kelas dan metode yang diperlukan untuk konversi STL ke PNG.
```csharp
using Aspose.CAD.FileFormats.Cad;
using Aspose.CAD.ImageOptions;
using System;
using System.Collections.Generic;
using System.Linq;
using System.Text;
```
## Langkah 1: Tentukan Direktori dan Jalur File Sumber
```csharp
string MyDir = "Your Document Directory";
string sourceFilePath = MyDir + "galeon.stl";
```
Pastikan Anda mengganti "Direktori Dokumen Anda" dengan jalur direktori sebenarnya tempat file STL Anda berada.
## Langkah 2: Muat Gambar CAD
```csharp
using (var cadImage = (CadImage)Image.Load(sourceFilePath))
{
    // Langkah selanjutnya akan dieksekusi dalam blok ini
}
```
Langkah ini memuat file STL sebagai gambar CAD, memungkinkan Anda memanipulasi dan mengekspornya.
## Langkah 3: Tetapkan Opsi Rasterisasi
```csharp
var rasterizationOptions = new CadRasterizationOptions();
rasterizationOptions.PageWidth = 100;
rasterizationOptions.PageHeight = 100;
```
Sesuaikan lebar dan tinggi halaman sesuai dengan preferensi dan kebutuhan Anda. Pengaturan ini menentukan dimensi PNG yang diekspor.
## Langkah 4: Konfigurasikan Opsi PNG
```csharp
PngOptions pngOptions = new PngOptions();
pngOptions.VectorRasterizationOptions = rasterizationOptions;
```
Buat opsi PNG, dengan menggabungkan pengaturan rasterisasi yang ditentukan pada langkah sebelumnya.
## Langkah 5: Simpan File PNG
```csharp
string outPath = sourceFilePath + ".png";
cadImage.Save(outPath, pngOptions);
```
Tentukan jalur keluaran untuk file PNG dan simpan gambar CAD dalam format PNG menggunakan opsi yang disediakan.
Ulangi langkah-langkah ini sesuai kebutuhan untuk kasus penggunaan spesifik Anda, dan Anda akan berhasil mengekspor file STL ke PNG dengan Aspose.CAD untuk .NET.
## Kesimpulan
Aspose.CAD untuk .NET menyederhanakan tugas rumit dalam mengonversi file STL ke PNG, memberdayakan pengembang dengan perangkat yang andal. Dengan mengikuti panduan langkah demi langkah ini, Anda dapat mengintegrasikan fungsi ini ke dalam aplikasi Anda dengan lancar.
## FAQ
### T: Dapatkah saya menyesuaikan dimensi PNG yang diekspor?
 Sangat! Pada Langkah 3, sesuaikan`PageWidth` Dan`PageHeight` nilai untuk memenuhi kebutuhan spesifik Anda.
### T: Apakah lisensi sementara tersedia untuk tujuan pengujian?
 Ya, Anda bisa mendapatkan lisensi sementara[Di Sini](https://purchase.aspose.com/temporary-license/) untuk pengujian dan evaluasi.
### T: Di mana saya bisa mendapatkan dukungan tambahan atau diskusi komunitas?
 Mengunjungi[Forum Aspose.CAD](https://forum.aspose.com/c/cad/19) untuk dukungan dan diskusi kolaboratif.
### T: Apakah ada format file lain yang didukung untuk konversi?
 Ya, Aspose.CAD mendukung berbagai format CAD selain STL. Mengacu kepada[dokumentasi](https://reference.aspose.com/cad/net/) untuk daftar lengkap.
### T: Bisakah saya memproses beberapa file STL secara batch?
Tentu! Terapkan loop berdasarkan langkah-langkah yang disediakan untuk memproses banyak file STL secara batch.
{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}
