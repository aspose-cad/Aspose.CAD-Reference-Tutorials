---
date: 2026-03-24
description: Pelajari cara mengonversi DGN ke PDF (dan PNG) dengan dukungan 3D untuk
  DGN V7 menggunakan Aspose.CAD untuk .NET – panduan langkah demi langkah.
linktitle: 3D Support for DGN V7
second_title: Aspose.CAD .NET - CAD and BIM File Format
title: Konversi DGN ke PDF (Dukungan 3D) dengan Aspose.CAD untuk .NET
url: /id/net/cad-features-and-support/3d-support-for-dgn-v7/
weight: 10
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Mengonversi DGN ke PDF (Dukungan 3D) dengan Aspose.CAD untuk .NET

## Pendahuluan

Dalam alur kerja CAD modern, kemampuan untuk **convert DGN to PDF** dengan cepat dan mempertahankan geometri 3‑D sangat penting. Baik Anda membuat dokumentasi, membagikan desain kepada pemangku kepentingan non‑CAD, atau mengarsipkan proyek, Aspose.CAD untuk .NET memberikan cara yang andal untuk mengubah file DGN V7 menjadi output PDF berkualitas tinggi (dan bahkan PNG). Pada tutorial ini kami akan memandu Anda melalui langkah‑langkah tepat untuk mengaktifkan dukungan 3D dan menghasilkan PDF dari file DGN.

## Jawaban Cepat
- **Apa yang dibahas dalam tutorial ini?** Mengaktifkan dukungan 3D dan mengonversi DGN V7 ke PDF menggunakan Aspose.CAD untuk .NET.  
- **Format utama apa yang dihasilkan?** PDF (dengan ekspor PNG opsional).  
- **Apakah saya memerlukan lisensi?** Versi percobaan gratis cukup untuk pengujian; lisensi komersial diperlukan untuk produksi.  
- **Versi .NET yang didukung?** .NET Framework 4.5+, .NET Core 3.1+, .NET 5/6+.  
- **Berapa lama implementasinya?** Sekitar 10‑15 menit untuk konversi dasar.

## Apa itu “convert DGN to PDF”?

Mengonversi DGN ke PDF berarti merender data vektor yang disimpan dalam file MicroStation DGN ke dalam format dokumen portabel yang dapat dilihat di perangkat apa pun tanpa perangkat lunak CAD khusus. Dengan mesin rasterisasi 3‑D Aspose.CAD, konversi ini mempertahankan tata letak, warna, dan petunjuk kedalaman, menghasilkan representasi visual yang setia.

## Mengapa menggunakan Aspose.CAD untuk konversi ini?

- **Rasterisasi 3‑D penuh** – mempertahankan informasi kedalaman dan tata letak.  
- **Tanpa ketergantungan eksternal** – perpustakaan .NET murni, tidak memerlukan MicroStation.  
- **Berbagai format output** – PDF, PNG, JPEG, TIFF, dll. (kata kunci sekunder *convert dgn to png* didukung langsung).  
- **Lintas‑platform** – berfungsi di Windows, Linux, dan macOS.

## Prasyarat

Sebelum memulai, pastikan Anda memiliki hal‑hal berikut:

- Aspose.CAD untuk .NET terpasang. Anda dapat mengunduhnya dari [Aspose.CAD for .NET download page](https://releases.aspose.com/cad/net/).  
- File DGN V7 yang valid yang ingin Anda proses.  
- Lingkungan pengembangan .NET (Visual Studio, VS Code, atau CLI). Instruksi instalasi tersedia di [.NET documentation](https://docs.microsoft.com/en-us/dotnet/core/install/).

## Impor Namespace

```csharp
using System;
using System.Collections.Generic;
using System.Linq;
using System.Text;
using System.Threading.Tasks;
using Aspose.CAD;
```

Namespace ini memberi Anda akses ke kelas inti Aspose.CAD dan utilitas standar .NET.

## Langkah 1: Siapkan Lingkungan

Tentukan di mana file DGN sumber Anda berada dan ke mana PDF output harus disimpan.

```csharp
string MyDir = "Your Document Directory";
string sourceFilePath = MyDir + "Nikon_D90_Camera.dgn";
```

> **Pro tip:** Gunakan `Path.Combine` untuk konstruksi path yang independen platform.

## Langkah 2: Muat File DGN

Buat instance `DgnImage` dengan memuat file menggunakan `Image.Load`. Langkah ini menyiapkan data CAD untuk rasterisasi.

```csharp
using (DgnImage dgnImage = (DgnImage)Image.Load(sourceFilePath))
{
    // Code snippet continues...
}
```

## Langkah 3: Konfigurasikan Opsi Ekspor

Siapkan `PdfOptions` bersama dengan `CadRasterizationOptions`. Di sini Anda mengontrol ukuran halaman, latar belakang, dan layout (view) mana yang akan diekspor.

```csharp
var options = new PdfOptions
{
    VectorRasterizationOptions = new CadRasterizationOptions
    {
        PageWidth = 1500,
        PageHeight = 1500,
        CenterDrawing = true,
        AutomaticLayoutsScaling = true,
        BackgroundColor = Color.Black,
        Layouts = new string[] { "1", "2", "3", "9" } // Export specific views
    }
};
```

Jika Anda perlu **convert DGN to PNG** sebagai gantinya, cukup ganti `PdfOptions` dengan `PngOptions` sambil mempertahankan pengaturan rasterisasi yang sama.

## Langkah 4: Simpan Hasil

Akhirnya, tulis output yang telah dirender ke lokasi yang diinginkan.

```csharp
string outFile = "Your Output Directory"; // Specify the output directory
dgnImage.Save(outFile, options);
```

Setelah dijalankan, Anda akan menemukan file PDF (atau PNG jika Anda mengubah opsi) yang secara akurat merepresentasikan gambar DGN 3‑D asli.

## Masalah Umum & Tips

- **Layout yang hilang:** Pastikan nama layout di `Layouts` cocok dengan yang ada di file DGN; jika tidak, mereka akan diabaikan.  
- **File besar:** Tingkatkan `PageWidth`/`PageHeight` secara bertahap untuk menghindari konsumsi memori yang tinggi.  
- **Akurasi warna:** Jika latar belakang tampak gelap, pastikan `BackgroundColor` diatur ke nilai yang diinginkan (misalnya, `Color.White`).

## Kesimpulan

Anda kini telah menguasai cara **convert DGN to PDF** dengan dukungan 3‑D penuh menggunakan Aspose.CAD untuk .NET. Alur kerja ini dapat diintegrasikan ke dalam pipeline otomatis, utilitas desktop, atau layanan web untuk menyajikan visualisasi CAD kepada siapa saja.

## FAQ

### Q1: Dapatkah saya memproses beberapa file DGN secara bersamaan menggunakan pendekatan ini?

A1: Ya, Anda dapat memodifikasi kode untuk menangani banyak file dalam sebuah loop atau sebagai bagian dari sistem pemrosesan batch.

### Q2: Format ekspor lain apa saja yang didukung oleh Aspose.CAD untuk .NET?

A2: Aspose.CAD untuk .NET mendukung berbagai format ekspor, termasuk PDF, PNG, JPG, dan lainnya. Lihat [documentation](https://reference.aspose.com/cad/net/) untuk detailnya.

### Q3: Apakah Aspose.CAD untuk .NET kompatibel dengan versi .NET Core terbaru?

A3: Ya, Aspose.CAD untuk .NET dirancang agar kompatibel dengan versi .NET Core terbaru. Pastikan Anda memiliki versi yang sesuai terpasang di lingkungan Anda.

### Q4: Dapatkah saya menyesuaikan pengaturan ekspor lebih lanjut untuk kebutuhan spesifik saya?

A4: Tentu saja! Kode yang disediakan merupakan titik awal. Anda dapat menjelajahi opsi dan konfigurasi tambahan di [Aspose.CAD documentation](https://reference.aspose.com/cad/net/).

### Q5: Di mana saya dapat mencari bantuan atau berbagi pengalaman dengan Aspose.CAD untuk .NET?

A5: Bergabunglah dengan komunitas Aspose.CAD di [forum](https://forum.aspose.com/c/cad/19) untuk berinteraksi dengan pengembang lain dan mendapatkan bantuan.

---

**Terakhir Diperbarui:** 2026-03-24  
**Diuji dengan:** Aspose.CAD 24.11 untuk .NET  
**Penulis:** Aspose  

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}