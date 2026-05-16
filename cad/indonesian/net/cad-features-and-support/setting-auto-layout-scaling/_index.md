---
date: 2026-03-26
description: Pelajari cara membuat PDF dari CAD dan mengonversi DXF ke PDF menggunakan
  Aspose.CAD untuk .NET dengan Auto Layout Scaling untuk rendering yang tepat dan
  dapat disesuaikan.
linktitle: Setting Auto Layout Scaling
second_title: Aspose.CAD .NET - CAD and BIM File Format
title: 'Buat PDF dari CAD: Skala Tata Letak Otomatis – Aspose.CAD'
url: /id/net/cad-features-and-support/setting-auto-layout-scaling/
weight: 14
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Buat PDF dari CAD: Skala Tata Letak Otomatis – Aspose.CAD

Dalam aplikasi .NET modern, mengubah gambar CAD menjadi PDF berkualitas tinggi merupakan kebutuhan umum—baik Anda perlu **create PDF from CAD** untuk pelaporan, berbagi, atau pengarsipan. Tutorial ini memandu Anda menggunakan Aspose.CAD untuk .NET untuk mengaktifkan Auto Layout Scaling, memberikan hasil pixel‑perfect sekaligus menunjukkan cara **convert DXF to PDF** dan **export CAD to PDF** dengan kode minimal.

## Jawaban Cepat
- **Apa yang dilakukan Auto Layout Scaling?** It automatically adjusts the layout to fit the page size, preserving geometry fidelity.  
- **Format apa yang didukung?** Any format Aspose.CAD reads (DXF, DWG, DGN, etc.) can be exported to PDF.  
- **Apakah saya memerlukan lisensi?** A free trial works for development; a commercial license is required for production.  
- **Bisakah saya mengubah ukuran halaman?** Yes—set `PageWidth` and `PageHeight` in `CadRasterizationOptions`.  
- **Apakah kompatibel dengan .NET Core?** Absolutely, works with .NET Framework and .NET Core/5/6+.

## Apa itu “create PDF from CAD”?
Membuat PDF dari file CAD berarti merasterkan data gambar vektor ke dalam format dokumen portabel. Konversi ini mempertahankan lapisan, ketebalan garis, dan warna sambil membuat file dapat dilihat di perangkat apa pun tanpa perangkat lunak CAD.

## Mengapa menggunakan Auto Layout Scaling?
Auto Layout Scaling memastikan seluruh gambar muat rapi pada halaman output, menghilangkan perhitungan manual untuk faktor skala. Ini sangat berguna saat menangani gambar dengan dimensi beragam, seperti rencana arsitektur atau skematik mekanik.

## Prasyarat
Sebelum Anda mulai, pastikan Anda memiliki:

1. **Aspose.CAD for .NET** – unduh perpustakaan terbaru dari [halaman unduhan](https://releases.aspose.com/cad/net/).  
2. **Lingkungan pengembangan .NET** – Visual Studio, Rider, atau editor apa pun yang mendukung C#.  
3. **File DXF contoh** – misalnya `conic_pyramid.dxf`, atau file CAD apa pun yang ingin Anda konversi.

## Impor Namespace
Tambahkan namespace yang diperlukan agar Anda dapat mengakses kelas Aspose.CAD.

```csharp
using System;
using System.Collections.Generic;
using System.Linq;
using System.Text;
using System.Threading.Tasks;
using Aspose.CAD;
```

## Langkah 1: Muat File CAD
Muat gambar sumber ke dalam objek `Image`. Ini adalah titik masuk untuk semua pemrosesan selanjutnya.

```csharp
string MyDir = "Your Document Directory";
string sourceFilePath = MyDir + "conic_pyramid.dxf";

using (Image image = Image.Load(sourceFilePath))
{
    // Your code here
}
```

## Langkah 2: Konfigurasikan Opsi Rasterisasi
Tentukan dimensi halaman output. Sesuaikan nilai-nilai ini agar cocok dengan ukuran PDF yang diinginkan.

```csharp
CadRasterizationOptions rasterizationOptions = new CadRasterizationOptions();
rasterizationOptions.PageWidth = 1600;
rasterizationOptions.PageHeight = 1600;
```

## Langkah 3: Aktifkan Auto Layout Scaling
Aktifkan skala otomatis sehingga gambar muat pada halaman tanpa terpotong.

```csharp
rasterizationOptions.AutomaticLayoutsScaling = true;
```

## Langkah 4: Buat Opsi PDF
Hubungkan pengaturan rasterisasi ke pengekspor PDF.

```csharp
PdfOptions pdfOptions = new PdfOptions();
pdfOptions.VectorRasterizationOptions = rasterizationOptions;
```

## Langkah 5: Simpan Hasil – create PDF from CAD
Tentukan jalur output dan simpan gambar sebagai PDF. Langkah ini **creates PDF from CAD** dengan skala yang Anda konfigurasikan.

```csharp
MyDir = MyDir + "result_out.pdf";
image.Save(MyDir, pdfOptions);
```

## Masalah Umum & Tips
- **Font atau gaya garis yang hilang?** Ensure the CAD file references are embedded or available on the server.  
- **File besar menyebabkan tekanan memori?** Process the drawing in chunks or increase the application’s memory limit.  
- **Output terlihat buram?** Increase `PageWidth`/`PageHeight` for higher DPI, or set `Resolution` in `CadRasterizationOptions`.

## Pertanyaan yang Sering Diajukan

**Q: Bisakah saya menerapkan Auto Layout Scaling ke format file lain selain DXF?**  
A: Ya, Aspose.CAD mendukung DWG, DGN, dan banyak format CAD lainnya untuk skala otomatis.

**Q: Bagaimana saya dapat menangani kesalahan selama proses rendering?**  
A: Bungkus kode konversi dalam blok `try‑catch` dan tangkap `Aspose.CAD.CadException` untuk informasi kesalahan yang detail.

**Q: Apakah ada batas ukuran file yang dapat ditangani oleh Aspose.CAD?**  
A: Perpustakaan ini dirancang untuk file besar, tetapi kinerja tergantung pada RAM dan CPU yang tersedia. Pertimbangkan memproses gambar yang sangat besar di server dengan sumber daya yang memadai.

**Q: Bisakah saya menyesuaikan PDF output lebih lanjut (misalnya, menambahkan watermark atau metadata)?**  
A: Tentu saja. Setelah menyimpan, Anda dapat menggunakan Aspose.PDF untuk memodifikasi PDF—menambahkan watermark, mengatur properti dokumen, atau menggabungkan halaman.

**Q: Di mana saya dapat menemukan sumber daya tambahan dan dukungan untuk Aspose.CAD?**  
A: Jelajahi [forum Aspose.CAD](https://forum.aspose.com/c/cad/19) untuk bantuan komunitas, dan lihat [dokumentasi](https://reference.aspose.com/cad/net/) untuk detail API yang lebih mendalam.

## Kesimpulan
Anda kini telah mempelajari cara **create PDF from CAD**, mengaktifkan **Auto Layout Scaling**, dan secara efektif **convert DXF to PDF** menggunakan Aspose.CAD untuk .NET. Pendekatan ini memberi Anda kontrol penuh atas kualitas rendering sambil menjaga implementasi tetap sederhana.

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}

---

**Terakhir Diperbarui:** 2026-03-26  
**Diuji Dengan:** Aspose.CAD for .NET 24.12 (latest)  
**Penulis:** Aspose  

---