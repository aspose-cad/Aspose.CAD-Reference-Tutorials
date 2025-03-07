---
title: Ekspor DGN ke Gambar Raster di Aspose.CAD untuk .NET
linktitle: Ekspor DGN ke Gambar Raster
second_title: Aspose.CAD .NET - Format File CAD dan BIM
description: Konversikan DGN ke gambar raster dengan mudah menggunakan Aspose.CAD untuk .NET. Jelajahi panduan langkah demi langkah dan manfaatkan kekuatan .NET dalam manipulasi file CAD.
weight: 13
url: /id/net/cad-export-formats/export-dgn-to-raster-image/
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Ekspor DGN ke Gambar Raster di Aspose.CAD untuk .NET

## Perkenalan

Dalam ranah dinamis pengembangan .NET, Aspose.CAD muncul sebagai alat yang ampuh untuk menangani file Computer-Aided Design (CAD). Tutorial ini mendalami proses mengekspor file DGN ke gambar raster menggunakan Aspose.CAD untuk .NET. Jika Anda ingin mengubah file DGN menjadi gambar raster yang menarik secara visual dengan mulus, Anda berada di tempat yang tepat.

## Prasyarat

Sebelum kita memulai perjalanan ini, pastikan Anda memiliki prasyarat berikut:

-  Aspose.CAD untuk .NET: Pastikan Anda telah menginstal perpustakaan Aspose.CAD di proyek .NET Anda. Anda dapat menemukan perpustakaan dan dokumentasi yang relevan di[situs web](https://reference.aspose.com/cad/net/).

- Contoh File DGN: Siapkan file DGN untuk dikonversi. Dalam contoh kita, kita akan menggunakan "Nikon_D90_Camera.dgn."

Sekarang, mari selami panduan langkah demi langkah.

## Impor Namespace

Di proyek .NET Anda, mulailah dengan mengimpor namespace yang diperlukan untuk Aspose.CAD. Langkah ini memungkinkan Anda mengakses kelas dan metode yang diperlukan DGN untuk mengonversi gambar raster.

```csharp
using System;
using System.Collections.Generic;
using System.Linq;
using System.Text;
using System.Threading.Tasks;
using Aspose.CAD;
```

## Langkah 1: Muat File DGN

 Mulailah dengan memuat file DGN ke a`CadImage` obyek. Ini memberikan landasan untuk operasi selanjutnya.

```csharp
string MyDir = "Your Document Directory";
string sourceFilePath = MyDir + "Nikon_D90_Camera.dgn";

using (CadImage cadImage = (CadImage)Image.Load(sourceFilePath))
{
    // Kode Anda untuk diproses lebih lanjut ada di sini
}
```

## Langkah 2: Tentukan Opsi Rasterisasi

 Membuat`CadRasterizationOptions` objek dan atur berbagai properti untuk menyesuaikan proses rasterisasi sesuai dengan kebutuhan Anda.

```csharp
CadRasterizationOptions rasterizationOptions = new CadRasterizationOptions();
rasterizationOptions.PageWidth = 600;
rasterizationOptions.PageHeight = 300;
rasterizationOptions.NoScaling = true;
rasterizationOptions.AutomaticLayoutsScaling = false;
```

## Langkah 3: Buat Objek JpegOptions

 Karena kami bertujuan untuk mengonversi file DGN ke JPEG, buatlah a`JpegOptions` objek dan menetapkan yang telah ditentukan sebelumnya`CadRasterizationOptions` untuk itu.

```csharp
ImageOptionsBase options = new JpegOptions();
options.VectorRasterizationOptions = rasterizationOptions;
```

## Langkah 4: Simpan Gambar Raster

 Memanfaatkan`Save` metode`CadImage` kelas untuk mengekspor file DGN ke gambar raster dalam format yang diinginkan, dalam hal ini JPEG.

```csharp
cadImage.Save(MyDir + "ExportDGNToRasterImage_out.jpg", options);
```

## Kesimpulan

Selamat! Anda telah berhasil menavigasi langkah-langkah untuk mengekspor file DGN ke gambar raster menggunakan Aspose.CAD untuk .NET. Tutorial ini telah membekali Anda dengan pengetahuan penting untuk mengintegrasikan fungsi ini ke dalam proyek .NET Anda dengan mudah.

## FAQ

### Q1: Bisakah saya mengekspor file DGN ke format selain JPEG?

A1: Ya, Aspose.CAD untuk .NET mendukung berbagai format output. Anda dapat mengubah opsi yang sesuai pada Langkah 3.

### Q2 Bagaimana cara menangani pengecualian selama proses konversi?

A2: Pastikan Anda memiliki penanganan pengecualian yang tepat, seperti yang ditunjukkan dalam kode yang disediakan, untuk mengatasi potensi masalah.

### Q3: Apakah ada versi uji coba yang tersedia untuk Aspose.CAD untuk .NET?

 A3: Ya, Anda dapat menjelajahi produk dengan uji coba gratis. Mengunjungi[Di Sini](https://releases.aspose.com/) untuk informasi lebih lanjut.

### Q4: Di mana saya dapat mencari bantuan atau mendiskusikan masalah terkait Aspose.CAD untuk .NET?

 A4: Pergilah ke[Forum Aspose.CAD](https://forum.aspose.com/c/cad/19) untuk dukungan dan diskusi komunitas.

### Q5: Bagaimana cara mendapatkan lisensi sementara Aspose.CAD untuk .NET?

 A5: Kunjungi[Link ini](https://purchase.aspose.com/temporary-license/)untuk memperoleh lisensi sementara untuk kebutuhan pengembangan Anda.
{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}
