---
title: Konversikan Tata Letak ke Gambar Raster di Aspose.CAD untuk .NET
linktitle: Konversi Tata Letak ke Gambar Raster
second_title: Aspose.CAD .NET - Format File CAD dan BIM
description: Konversi tata letak CAD ke gambar raster dengan mudah menggunakan Aspose.CAD untuk .NET. Tingkatkan pengembangan Anda dengan kemampuan manipulasi CAD yang kuat.
weight: 12
url: /id/net/cad-drawing-manipulation/convert-layouts-to-raster-image/
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Konversikan Tata Letak ke Gambar Raster di Aspose.CAD untuk .NET

## Perkenalan

Apakah Anda ingin dengan mudah mengonversi tata letak menjadi gambar raster di aplikasi .NET Anda? Tidak perlu mencari lagi! Panduan langkah demi langkah ini akan memandu Anda melalui proses menggunakan Aspose.CAD untuk .NET, perpustakaan canggih yang menyederhanakan tugas Computer-Aided Design (CAD).

## Prasyarat

Sebelum masuk ke tutorial, pastikan Anda memiliki prasyarat berikut:

- Aspose.CAD untuk .NET Library: Unduh dan instal perpustakaan dari[Halaman unduhan Aspose.CAD untuk .NET](https://releases.aspose.com/cad/net/).

- Lingkungan Pengembangan: Pastikan Anda memiliki lingkungan pengembangan .NET yang berfungsi di mesin Anda.

- Dokumen untuk Dikonversi: Siapkan dokumen CAD yang berisi tata letak yang ingin Anda ubah menjadi gambar raster.

- Direktori Dokumen Anda: Ganti placeholder "Direktori Dokumen Anda" dalam kode dengan jalur ke direktori dokumen Anda.

## Impor Namespace

Pertama, mari impor namespace yang diperlukan agar fungsionalitas Aspose.CAD dapat diakses dalam kode Anda.

```csharp
using System;
using System.Collections.Generic;
using System.Linq;
using System.Text;
using System.Threading.Tasks;
using Aspose.CAD;
```

## Langkah 1: Muat Dokumen CAD

Mulailah dengan memuat dokumen CAD menggunakan perpustakaan Aspose.CAD.

```csharp
string sourceFilePath = MyDir + "conic_pyramid.dxf";
using (Image image = Image.Load(sourceFilePath))
{
    //Kode Anda untuk langkah selanjutnya akan ditempatkan di sini
}
```

## Langkah 2: Konfigurasikan Opsi Rasterisasi

 Buat sebuah contoh dari`CadRasterizationOptions` untuk mengatur lebar halaman, tinggi, dan menentukan tata letak yang ingin Anda konversi.

```csharp
CadRasterizationOptions rasterizationOptions = new CadRasterizationOptions();
rasterizationOptions.PageWidth = 1200;
rasterizationOptions.PageHeight = 1200;
rasterizationOptions.Layouts = new string[] { "Model", "Layout1" };
```

## Langkah 3: Siapkan TiffOptions untuk Gambar yang Dihasilkan

 Buat sebuah contoh dari`TiffOptions`untuk menentukan format gambar yang dihasilkan.

```csharp
ImageOptionsBase options = new TiffOptions(TiffExpectedFormat.Default);
options.VectorRasterizationOptions = rasterizationOptions;
```

## Langkah 4: Simpan Gambar yang Dihasilkan

Tentukan jalur keluaran dan simpan gambar yang dikonversi.

```csharp
string outputFilePath = MyDir + "conic_pyramid_layoutstorasterimage_out.tiff";
image.Save(outputFilePath, options);
```

## Kesimpulan

Selamat! Anda telah berhasil mengonversi tata letak CAD ke format gambar raster menggunakan Aspose.CAD untuk .NET. Kemungkinannya sangat besar, dan panduan ini berfungsi sebagai titik awal untuk upaya Anda yang berhubungan dengan CAD.

## FAQ

### Q1: Apakah Aspose.CAD kompatibel dengan semua format CAD?

 A1: Aspose.CAD mendukung berbagai format CAD, termasuk DWG, DXF, DWF, STL, dan banyak lagi. Periksalah[dokumentasi](https://reference.aspose.com/cad/net/) untuk daftar lengkap.

### Q2: Bagaimana cara mendapatkan lisensi sementara untuk Aspose.CAD?

 A2: Kunjungi[halaman lisensi sementara](https://purchase.aspose.com/temporary-license/) untuk memperoleh izin sementara untuk tujuan pengujian dan evaluasi.

### Q3: Di mana saya dapat menemukan dukungan untuk Aspose.CAD?

 A3: Forum adalah tempat yang tepat untuk mencari bantuan. Mengunjungi[Forum Aspose.CAD](https://forum.aspose.com/c/cad/19) untuk terhubung dengan komunitas dan mendapatkan bantuan.

### Q4: Dapatkah saya mencoba Aspose.CAD secara gratis?

 A4: Tentu saja! Ambil milikmu[uji coba gratis](https://releases.aspose.com/) untuk menjelajahi fitur dan kemampuan Aspose.CAD.

### Q5: Di mana saya bisa membeli lisensi untuk Aspose.CAD?

 A5: Navigasikan ke[halaman pembelian](https://purchase.aspose.com/buy) untuk membeli lisensi dan membuka potensi penuh Aspose.CAD.
{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}
