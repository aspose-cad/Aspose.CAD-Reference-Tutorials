---
date: 2026-04-09
description: Pelajari cara mengekspor lapisan DWG, mengonversi gambar DWG, dan menyimpan
  JPEG DWG menggunakan C# dengan Aspose.CAD untuk .NET. Panduan langkah demi langkah
  untuk manipulasi file CAD yang efisien.
keywords:
- export dwg layers
- convert dwg image
- dwg layer visibility
- save dwg jpeg
linktitle: Menangani Lapisan dalam File DWG dengan C#
second_title: Aspose.CAD .NET - CAD and BIM File Format
title: Ekspor Lapisan DWG dengan C# – Tutorial Aspose.CAD
url: /id/net/dwg-file-manipulation/support-of-layers/
weight: 11
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Ekspor Lapisan DWG dengan C# – Tutorial Aspose.CAD

## Pendahuluan

Dalam panduan komprehensif ini Anda akan belajar **cara mengekspor lapisan DWG** menggunakan C# dan perpustakaan Aspose.CAD. Baik Anda perlu **mengonversi gambar DWG**, mengontrol **visibilitas lapisan DWG**, atau sekadar **menyimpan file DWG JPEG**, langkah‑langkah di bawah ini akan menunjukkan cara melakukannya secara efisien. Pada akhir tutorial Anda akan memiliki potongan kode siap‑jalankan yang mengisolasi lapisan tertentu dan merendernya sebagai JPEG berkualitas tinggi.

## Jawaban Cepat
- **Apa arti “export dwg layers”?** Itu berarti merasterisasi lapisan terpilih dari file DWG menjadi format gambar seperti JPEG atau PNG.  
- **Perpustakaan mana yang terbaik untuk tugas ini?** Aspose.CAD untuk .NET menyediakan dukungan lengkap tanpa memerlukan AutoCAD.  
- **Bisakah saya mengekspor beberapa lapisan sekaligus?** Ya – berikan array nama lapisan ke opsi rasterisasi.  
- **Apakah saya memerlukan lisensi untuk penggunaan produksi?** Lisensi komersial diperlukan; versi percobaan gratis tersedia untuk evaluasi.  
- **Format output apa yang didukung?** JPEG, PNG, BMP, TIFF, dan beberapa lainnya melalui kelas ImageOptions.

## Apa itu ekspor lapisan dwg?
Mengekspor lapisan DWG berarti mengambil data vektor yang berada pada satu atau lebih lapisan dalam gambar DWG dan merasterisasikannya menjadi gambar bitmap. Ini berguna ketika Anda ingin membagikan tampilan bagian tertentu dari gambar tanpa mengungkapkan seluruh file CAD.

## Mengapa mengontrol visibilitas lapisan DWG?
Mengontrol visibilitas lapisan memungkinkan Anda:

- Membuat aset visual bersih untuk presentasi atau dokumentasi.  
- Mengurangi ukuran file dengan mengekspor hanya geometri yang diperlukan.  
- Melindungi detail desain proprietari dengan menyembunyikan lapisan rahasia.  

## Prasyarat

Sebelum kita mulai, pastikan Anda memiliki:

- Pengetahuan dasar tentang bahasa pemrograman C#.  
- Visual Studio terpasang di komputer Anda.  
- Perpustakaan Aspose.CAD untuk .NET, yang dapat Anda unduh dari [situs Aspose.CAD](https://releases.aspose.com/cad/net/).

## Impor Namespace

Untuk memulai, impor namespace yang memberi Anda akses ke fitur rasterisasi dan ekspor gambar.

```csharp
using Aspose.CAD.ImageOptions;
using System;
using System.Collections.Generic;
using System.IO;
using System.Linq;
using System.Text;
```

## Langkah 1: Muat File DWG

Muat file DWG (atau DWF) sumber ke dalam objek `Image`. Objek ini mewakili seluruh gambar dalam memori.

```csharp
string MyDir = "Your Document Directory";
string sourceFilePath = MyDir + "for_layers_test.dwf";

using (Aspose.CAD.Image image = Aspose.CAD.Image.Load(sourceFilePath))
{
    // Your code for subsequent steps goes here
}
```

*Mengapa ini penting:* Memuat file sekali memungkinkan Anda menggunakan kembali instance `image` yang sama untuk sejumlah ekspor spesifik lapisan, meningkatkan kinerja.

## Langkah 2: Konfigurasikan Opsi Rasterisasi

Buat instance `CadRasterizationOptions` untuk memberi tahu Aspose.CAD cara merender gambar. Di sini kami menetapkan resolusi tinggi (1600 × 1600) untuk memastikan JPEG yang diekspor tajam.

```csharp
Aspose.CAD.ImageOptions.CadRasterizationOptions rasterizationOptions = new Aspose.CAD.ImageOptions.CadRasterizationOptions();
rasterizationOptions.PageWidth = 1600;
rasterizationOptions.PageHeight = 1600;
```

Anda juga dapat menyesuaikan warna latar belakang, skala ketebalan garis, atau pengaturan anti‑aliasing jika diperlukan.

## Langkah 3: Tentukan Lapisan (Visibilitas Lapisan DWG)

Tambahkan lapisan yang ingin Anda **ekspor lapisan dwg**. Pada contoh ini kami mengekspor hanya “LayerA”. Untuk mengekspor beberapa lapisan, cukup daftarkan mereka dalam array.

```csharp
rasterizationOptions.Layers = new string[] { "LayerA" };
```

*Tip pro:* Gunakan nama lapisan yang persis seperti yang muncul dalam gambar; nama lapisan sensitif terhadap huruf besar/kecil.

## Langkah 4: Konfigurasikan Opsi Ekspor Gambar

Pilih format gambar yang ingin Anda buat. Kami akan menggunakan `JpegOptions` karena JPEG menawarkan keseimbangan yang baik antara kualitas dan ukuran file, yang ideal ketika Anda perlu **menyimpan dwg jpeg** untuk pratinjau web.

```csharp
JpegOptions jpegOptions = new JpegOptions();
jpegOptions.VectorRasterizationOptions = rasterizationOptions;
```

Jika Anda perlu **mengonversi gambar dwg** ke PNG atau TIFF, ganti `JpegOptions` dengan kelas opsi yang sesuai.

## Langkah 5: Simpan Gambar yang Diekspor

Tentukan jalur file output dan panggil `Save`. Mesin rasterisasi menghormati daftar lapisan yang Anda berikan, sehingga hanya “LayerA” yang muncul dalam JPEG akhir.

```csharp
MyDir = MyDir + "for_layers_test.jpg";
image.Save(MyDir, jpegOptions);
```

Setelah baris ini dijalankan, Anda akan menemukan `for_layers_test.jpg` di direktori dokumen Anda, yang berisi hanya lapisan yang dipilih.

## Masalah Umum dan Solusinya

| Masalah | Solusi |
|-------|------------|
| **Nama lapisan tidak ditemukan** | Verifikasi ejaan dan huruf besar/kecil yang tepat dari lapisan dalam DWG asli. Gunakan penampil CAD untuk melihat daftar nama lapisan. |
| **Gambar output kosong** | Pastikan opsi rasterisasi memiliki latar belakang yang tidak transparan dan bahwa lapisan yang dipilih memang berisi geometri. |
| **Output beresolusi rendah** | Tingkatkan `PageWidth` dan `PageHeight` atau atur `Resolution` dalam `CadRasterizationOptions`. |
| **Versi DWG tidak didukung** | Perbarui ke versi Aspose.CAD terbaru; versi tersebut menambahkan dukungan untuk rilis AutoCAD yang lebih baru. |

## Pertanyaan yang Sering Diajukan

### Q1: Bisakah saya menangani beberapa lapisan secara bersamaan?
A1: Ya, Anda bisa. Cukup tambahkan nama lapisan ke array `rasterizationOptions.Layers`.

### Q2: Apakah versi percobaan Aspose.CAD tersedia?
A2: Ya, Anda dapat memperoleh versi percobaan gratis dari [sini](https://releases.aspose.com/).

### Q3: Di mana saya dapat menemukan dokumentasi?
A3: Dokumentasi tersedia [di sini](https://reference.aspose.com/cad/net/).

### Q4: Bagaimana cara mendapatkan dukungan untuk Aspose.CAD?
A4: Anda dapat mencari dukungan di [forum Aspose.CAD](https://forum.aspose.com/c/cad/19).

### Q5: Apa saja opsi lisensi untuk Aspose.CAD?
A5: Anda dapat menjelajahi opsi lisensi dan detail pembelian [di sini](https://purchase.aspose.com/buy).

**Pertanyaan Tambahan**

**Q: Bisakah saya mengekspor gambar ke PNG alih-alih JPEG?**  
A: Tentu saja. Ganti `JpegOptions` dengan `PngOptions` dan sesuaikan ekstensi file sesuai.

**Q: Apakah perpustakaan ini mempertahankan gaya garis dan warna?**  
A: Ya. Semua properti vektor dirender dengan setia selama rasterisasi.

---

**Terakhir Diperbarui:** 2026-04-09  
**Diuji Dengan:** Aspose.CAD untuk .NET (rilis terbaru)  
**Penulis:** Aspose  

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}