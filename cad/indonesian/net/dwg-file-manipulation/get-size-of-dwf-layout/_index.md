---
date: 2026-04-06
description: Pelajari cara mengonversi DWF ke JPG dalam C# menggunakan Aspose.CAD
  dan temukan cara mengekstrak ukuran tata letak DWF dari file DWG.
keywords:
- convert dwf to jpg
- how to extract dwf
- convert dwg to jpg
linktitle: Bekerja dengan File DWG di C# - Dapatkan Ukuran Tata Letak DWF
second_title: Aspose.CAD .NET - CAD and BIM File Format
title: Mengonversi DWF ke JPG dalam C# – Dapatkan Ukuran Layout DWF dari DWG
url: /id/net/dwg-file-manipulation/get-size-of-dwf-layout/
weight: 10
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Mengonversi DWF ke JPG di C# – Dapatkan Ukuran Tata Letak DWF dari DWG

## Pendahuluan

Jika Anda perlu **mengonversi DWF ke JPG** sambil juga mengetahui dimensi tata letak yang tepat, Anda berada di tempat yang tepat. Dalam tutorial ini kami akan membahas contoh lengkap, end‑to‑end yang menggunakan Aspose.CAD untuk .NET untuk membuka file DWF yang dihasilkan dari DWG, membaca ukuran setiap tata letak, dan menyimpan tata letak sebagai gambar JPG berkualitas tinggi. Pada akhir tutorial Anda tidak hanya akan mengetahui cara mengekstrak informasi tata letak DWF tetapi juga memiliki potongan kode yang dapat digunakan kembali dalam proyek C# mana pun.

## Jawaban Cepat
- **Apa arti “convert DWF to JPG”?** Artinya merasterisasi tata letak DWF vektor menjadi gambar bitmap JPEG.  
- **Mengapa membaca ukuran tata letak terlebih dahulu?** Mengetahui batas tepat memungkinkan Anda mengatur dimensi halaman yang benar, menghindari output yang terdistorsi atau terpotong.  
- **Perpustakaan mana yang menangani ini?** Aspose.CAD untuk .NET menyediakan dukungan penuh untuk DWG, DWF, dan konversi gambar raster.  
- **Apakah saya memerlukan lisensi?** Lisensi sementara dapat digunakan untuk evaluasi; lisensi penuh diperlukan untuk produksi.  
- **Versi .NET apa yang didukung?** .NET Framework 4.5+, .NET Core 3.1+, .NET 5/6/7.

## Apa itu “convert DWF to JPG” dan mengapa penting?

Mengonversi file DWF (Design Web Format) ke JPG menghasilkan gambar portabel yang dapat ditampilkan di peramban, disisipkan dalam laporan, atau dibagikan kepada pemangku kepentingan yang tidak memiliki perangkat lunak CAD. Konversi ini juga memberi Anda fleksibilitas untuk memanipulasi gambar (mengubah ukuran, mengompres, menambahkan watermark) menggunakan alat pemrosesan gambar standar.

## Mengapa mengekstrak ukuran tata letak DWF?

File DWF dapat berisi beberapa tata letak, masing‑masing dengan sistem koordinat dan satuan sendiri (inci, milimeter, dll.). Mengekstrak ukuran tata letak memungkinkan Anda:

1. Mempertahankan rasio aspek asli saat merasterisasi.  
2. Memilih DPI yang tepat untuk output beresolusi tinggi.  
3. Mengotomatiskan pemrosesan batch banyak tata letak tanpa penyesuaian manual.

## Prasyarat

Untuk mengikuti tutorial ini dengan lancar, pastikan Anda memiliki prasyarat berikut:

- Aspose.CAD untuk .NET: Pastikan Anda telah menginstal Aspose.CAD untuk .NET. Anda dapat mengunduhnya dari [halaman unduhan Aspose.CAD untuk .NET](https://releases.aspose.com/cad/net/).

Dengan pustaka yang siap, Anda dapat fokus pada kode daripada mencari ketergantungan.

## Impor Namespace

Sebelum kita mulai menulis kode, impor namespace yang diperlukan. Ini menyediakan kelas‑kelas yang akan kita gunakan untuk bekerja dengan file CAD, opsi rasterisasi, dan I/O file.

```csharp
using Aspose.CAD.FileFormats.Cad;
using Aspose.CAD.FileFormats.Dwf;
using Aspose.CAD.ImageOptions;
using System;
using System.Collections.Generic;
using System.IO;
using System.Linq;
using System.Text;
```

## Langkah 1: Siapkan Lingkungan Anda

Buat proyek konsol C# atau pustaka kelas baru, tambahkan referensi ke **Aspose.CAD.dll**, dan pastikan proyek menargetkan versi .NET yang kompatibel.

## Langkah 2: Tentukan Jalur File (cara mengekstrak DWF)

Tentukan di mana file DWF sumber Anda berada dan ke mana file JPG yang dihasilkan harus ditulis.

```csharp
string MyDir = "Your Document Directory";
string sourceFilePath = MyDir + "blocks_and_tables.dwf";
```

> **Tips Pro:** Use `Path.Combine(MyDir, "blocks_and_tables.dwf")` for safer path handling on different OSes.

## Langkah 3: Muat Gambar DWF

Muat file DWF ke dalam objek `Aspose.CAD.Image`. Kami melakukan cast ke `DwfImage` karena kami memerlukan akses ke properti spesifik halaman.

```csharp
using (DwfImage image = (DwfImage)Aspose.CAD.Image.Load(sourceFilePath))
{
    // Code for further steps will go here
}
```

## Langkah 4: Iterasi Melalui Halaman

Sebuah DWF dapat berisi beberapa halaman (tata letak). Lakukan loop melalui masing‑masing sehingga kita dapat memprosesnya secara individual.

```csharp
foreach (var page in image.Pages)
{
    // Code for further steps will go here
}
```

## Langkah 5: Dapatkan Informasi Tata Letak

Di dalam loop, ambil nama tata letak. Nama ini akan digunakan baik untuk pencatatan maupun untuk penamaan file JPG output.

```csharp
var layout = page.Name;
System.Console.WriteLine("Layout= " + layout);
```

## Langkah 6: Siapkan Opsi JPG

Buat instance `JpegOptions` dan konfigurasikan opsi rasterisasi. Properti `Layouts` memberi tahu Aspose.CAD tata letak mana yang akan dirender.

```csharp
using (FileStream fs = new FileStream(MyDir + "layout_" + layout + ".jpg", FileMode.Create))
{
    JpegOptions jpegOptions = new JpegOptions();
    CadRasterizationOptions options = new CadRasterizationOptions();
    options.Layouts = new string[] { layout };
    // Code for further steps will go here
}
```

## Langkah 7: Tentukan Ukuran Halaman (konversi dwg ke jpg)

Hitung lebar dan tinggi tata letak dalam satuan aslinya. Informasi ini penting untuk mengatur ukuran halaman raster dengan benar.

```csharp
double sizeExtX = page.MaxPoint.X - page.MinPoint.X;
double sizeExtY = page.MaxPoint.Y - page.MinPoint.Y;
// Code for further steps will go here
```

## Langkah 8: Siapkan Dimensi Halaman

Konversi satuan asli (inci atau milimeter) ke piksel menggunakan metode bantu yang disediakan oleh Aspose.CAD. Jika tipe satuan bukan keduanya, kami kembali menggunakan nilai mentah.

```csharp
if (page.UnitType == UnitType.Inch)
{
    options.PageHeight = CommonHelper.INtoPixels(sizeExtY, CommonHelper.DPI);
    options.PageWidth = CommonHelper.INtoPixels(sizeExtX, CommonHelper.DPI);
}
else if (page.UnitType == UnitType.Millimeter)
{
    options.PageHeight = CommonHelper.MMtoPixels(sizeExtY, CommonHelper.DPI);
    options.PageWidth = CommonHelper.MMtoPixels(sizeExtX, CommonHelper.DPI);
}
else
{
    options.PageHeight = (float)sizeExtY;
    options.PageWidth = (float)sizeExtX;
}
```

## Langkah 9: Simpan File JPG

Akhirnya, hubungkan opsi rasterisasi ke opsi JPEG dan simpan gambar ke disk.

```csharp
jpegOptions.VectorRasterizationOptions = options;
image.Save(fs, jpegOptions);
}
```

Setelah loop selesai, Anda akan memiliki file JPG untuk setiap tata letak, masing‑masing berukuran tepat sesuai dimensi DWF asli.

## Masalah Umum dan Solusinya

| Gejala | Penyebab Kemungkinan | Solusi |
|---------|----------------------|--------|
| Output JPG kosong | `options.Layouts` tidak diatur dengan benar | Verifikasi nama tata letak cocok dengan `page.Name`. |
| Gambar terdistorsi | Konversi DPI salah | Gunakan `CommonHelper.DPI = 300` (atau DPI target Anda) sebelum konversi. |
| File tidak ditemukan | Path `MyDir` tidak tepat | Gunakan path absolut atau `Path.Combine`. |
| Pengecualian lisensi | Tidak ada lisensi yang diterapkan | Muat lisensi sementara atau permanen sebelum memanggil `Image.Load`. |

## Pertanyaan yang Sering Diajukan

### Q1: Apakah Aspose.CAD kompatibel dengan format file DWG terbaru?

A1: Aspose.CAD mendukung berbagai format file DWG, termasuk versi terbaru. Lihat [dokumentasi](https://reference.aspose.com/cad/net/) untuk detail kompatibilitas spesifik.

### Q2: Bisakah saya menggunakan Aspose.CAD untuk proyek komersial dan pribadi?

A2: Ya, Aspose.CAD menawarkan opsi lisensi fleksibel untuk penggunaan komersial maupun pribadi. Kunjungi [halaman pembelian](https://purchase.aspose.com/buy) untuk detail lebih lanjut.

### Q3: Bagaimana saya dapat memperoleh lisensi sementara untuk Aspose.CAD?

A3: Anda dapat memperoleh lisensi sementara dari [sini](https://purchase.aspose.com/temporary-license/) untuk tujuan evaluasi.

### Q4: Di mana saya dapat menemukan dukungan untuk Aspose.CAD?

A4: Untuk pertanyaan atau bantuan, kunjungi [forum Aspose.CAD](https://forum.aspose.com/c/cad/19).

### Q5: Apakah ada percobaan gratis untuk Aspose.CAD?

A5: Ya, Anda dapat mengakses versi percobaan gratis Aspose.CAD [di sini](https://releases.aspose.com/).

### Q6: Bagaimana cara mengonversi file DWG langsung ke JPG tanpa mengekstrak DWF terlebih dahulu?

A6: Anda dapat memuat file DWG dengan `Aspose.CAD.Image.Load` dan menggunakan alur kerja rasterisasi yang sama; cukup atur `options.Layouts` ke nama tata letak yang diinginkan dari DWG.

### Q7: Apakah konversi mempertahankan kualitas vektor?

A7: Setelah dirasterisasi ke JPG, gambar menjadi berbasis bitmap, sehingga skalabilitas vektor hilang. Untuk skala tanpa kehilangan kualitas, pertimbangkan mengekspor ke PNG atau SVG.

---

**Terakhir Diperbarui:** 2026-04-06  
**Diuji Dengan:** Aspose.CAD 24.11 for .NET  
**Penulis:** Aspose  

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}