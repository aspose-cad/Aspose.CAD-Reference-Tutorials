---
date: 2026-04-06
description: Pelajari cara mengonversi DWG ke PDF dan menambahkan teks khusus menggunakan
  C# dan Aspose.CAD. Panduan langkah demi langkah ini mencakup pembuatan PDF dari
  DWG, menyisipkan entitas teks, dan mengubah font teks DWG.
keywords:
- convert dwg to pdf
- generate pdf from dwg
- insert text entity
- change dwg text font
- aspose cad dwg pdf
linktitle: Menambahkan Teks ke File DWG dengan C#
second_title: Aspose.CAD .NET - CAD and BIM File Format
title: Mengonversi DWG ke PDF dan Menambahkan Teks di C# – Tutorial Aspose.CAD
url: /id/net/dwg-file-manipulation/adding-text-to-dwg/
weight: 14
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Konversi DWG ke PDF dan Tambahkan Teks di C# – Aspose.CAD Tutorial

## Pendahuluan

Di dunia CAD dan pengembangan .NET yang bergerak cepat, **mengonversi DWG ke PDF** sambil menyisipkan anotasi khusus adalah kebutuhan yang sering. Baik Anda perlu menghasilkan gambar yang dapat dicetak untuk klien atau menyematkan catatan dinamis langsung ke DWG, Aspose.CAD membuat pekerjaan ini mudah. Dalam tutorial ini Anda akan belajar cara **mengonversi DWG ke PDF**, **menambahkan entitas teks**, dan bahkan **mengubah font teks DWG** menggunakan C#.

## Jawaban Cepat
- **Library apa yang terbaik untuk konversi DWG‑to‑PDF?** Aspose.CAD for .NET  
- **Apakah saya dapat menambahkan teks khusus saat konversi?** Yes – create a `CadText` entity and add it before saving.  
- **Apakah saya memerlukan lisensi untuk penggunaan produksi?** A commercial license is required; a free trial is available.  
- **Versi .NET mana yang didukung?** .NET Framework 4.5+, .NET Core 3.1+, .NET 5/6+.  
- **Apakah memungkinkan mengubah font teks?** Yes, adjust the `CadText` properties such as `StyleType` dan `TextHeight`.

## Apa itu “convert dwg to pdf”?

Mengonversi file DWG ke PDF mengubah gambar CAD berbasis vektor menjadi dokumen yang dapat dibagikan secara luas dan independen dari perangkat. PDF mempertahankan geometri dan lapisan asli, sambil memungkinkan Anda menyematkan anotasi, teks, atau metadata lainnya. Aspose.CAD menangani rasterisasi dan rendering vektor secara otomatis, sehingga Anda tidak memerlukan perangkat lunak CAD pihak ketiga di server.

## Mengapa menambahkan teks ke DWG sebelum konversi?

Menyematkan teks langsung ke DWG memberi Anda kontrol penuh atas penempatan, gaya, dan penugasan lapisan. Ketika file kemudian dikonversi ke PDF, teks muncul tepat di tempat yang Anda tentukan, mempertahankan maksud desain dan menghilangkan kebutuhan pemrosesan lanjutan di editor PDF.

## Prasyarat

Sebelum kita mulai, pastikan Anda memiliki:

- **Aspose.CAD Library** – download it from the [download link](https://releases.aspose.com/cad/net/).  
- **Lingkungan .NET yang berfungsi** (Visual Studio 2022, .NET 6, atau versi kompatibel lainnya).  
- **Folder untuk file uji Anda** – kami akan menyebutnya `MyDir` sepanjang panduan.

Sekarang, mari kita jalani proses langkah demi langkah.

## Impor Namespace

Tambahkan pernyataan `using` yang diperlukan agar Anda dapat mengakses kelas Aspose.CAD.

```csharp
using System;
using System.Collections.Generic;
using System.Linq;
using System.Text;
using System.Threading.Tasks;
using Aspose.CAD;
using Aspose.CAD.FileFormats.Cad.CadObjects;
using Aspose.CAD.FileFormats.Cad.CadConsts;
using Aspose.CAD.FileFormats.Cad;
using Aspose.CAD.FileFormats.Cad.CadObjects.AttEntities;
using Aspose.CAD.ImageOptions;
```

## Langkah 1: Muat File DWG

Muat file DWG sumber Anda ke dalam objek `Image`. Objek ini memberi Anda akses ke entitas CAD yang mendasarinya.

```csharp
string dwgPathToFile = MyDir + "SimpleEntites.dwg";
using (Image image = Image.Load(dwgPathToFile))
{
    // Subsequent steps will be performed inside this block
}
```

## Langkah 2: Buat Objek CadText (Sisipkan Entitas Teks)

Kelas `CadText` mewakili satu baris teks dalam DWG. Di sini kami mengatur gaya, nilai, warna, lapisan, dan posisi. Sesuaikan `StyleType` atau `TextHeight` untuk **mengubah font teks DWG**.

```csharp
CadText cadText = new CadText();
cadText.StyleType = "Standard";          // Font/style – change to alter DWG text font
cadText.DefaultValue = "Some custom text";
cadText.ColorId = 256;                    // 256 = ByLayer (you can use a specific ACI color)
cadText.LayerName = "0";
cadText.FirstAlignment.X = 47.90;
cadText.FirstAlignment.Y = 5.56;
cadText.TextHeight = 0.8;                 // Height influences visual size
cadText.ScaleX = 0.0;
```

## Langkah 3: Tambahkan Entitas Teks ke Model Space

Model space DWG menyimpan sebagian besar entitas gambar. Dengan menambahkan `CadText` kami ke blok `*Model_Space`, teks menjadi bagian dari gambar.

```csharp
CadImage cadImage = (CadImage)image;
cadImage.BlockEntities["*Model_Space"].AddEntity(cadText);
```

## Langkah 4: Konfigurasikan Opsi PDF (Hasilkan PDF dari DWG)

Siapkan opsi rasterisasi yang mengontrol cara DWG dirender menjadi PDF. Anda dapat menyesuaikan ukuran halaman, jenis gambar, dan tata letak.

```csharp
PdfOptions pdfOptions = new PdfOptions();
CadRasterizationOptions cadRasterizationOptions = new CadRasterizationOptions();
pdfOptions.VectorRasterizationOptions = cadRasterizationOptions;
cadRasterizationOptions.DrawType = CadDrawTypeMode.UseObjectColor;
cadRasterizationOptions.PageHeight = 1600;
cadRasterizationOptions.PageWidth = 1600;
cadRasterizationOptions.Layouts = new string[] { "Model" };
```

## Langkah 5: Simpan DWG yang Dimodifikasi sebagai PDF

Terakhir, ekspor gambar yang telah dimodifikasi. PDF yang dihasilkan mencakup teks yang baru disisipkan.

```csharp
image.Save(MyDir + "SimpleEntites_generated.pdf", pdfOptions);
```

> **Tips pro:** Jika Anda memerlukan PDF dengan resolusi lebih tinggi, tingkatkan `PageHeight` dan `PageWidth` secara proporsional.

## Masalah Umum & Solusinya

| Masalah | Alasan | Solusi |
|-------|--------|-----|
| Teks tidak muncul di PDF | Lapisan atau ID warna salah | Pastikan `LayerName` ada dan `ColorId` diatur ke warna yang terlihat (mis., 7 untuk putih). |
| Teks berada di tempat yang salah | Koordinat perataan tidak tepat | Verifikasi nilai `FirstAlignment.X/Y` relatif terhadap satuan gambar. |
| PDF kosong | Opsi rasterisasi tidak diatur | Atur `DrawType` ke `UseObjectColor` atau `UseObjectLineWeight`. |

## Pertanyaan yang Sering Diajukan (Existing)

### Q1: Apakah Aspose.CAD kompatibel dengan semua versi file DWG?

A1: Aspose.CAD mendukung berbagai versi file DWG, memastikan kompatibilitas dengan berbagai perangkat lunak CAD.

### Q2: Bisakah saya menambahkan beberapa entitas teks ke satu file DWG menggunakan Aspose.CAD?

A2: Ya, Anda dapat menambahkan beberapa entitas teks ke file DWG dengan mengulangi proses yang dijelaskan dalam tutorial.

### Q3: Bagaimana saya dapat mengubah font dan gaya teks di Aspose.CAD?

A3: Untuk mengubah font dan gaya teks, sesuaikan properti objek `CadText` sebelum menambahkannya ke file DWG.

### Q4: Apakah ada pertimbangan lisensi untuk menggunakan Aspose.CAD dalam proyek komersial?

A5: Ya, pastikan kepatuhan dengan ketentuan lisensi Aspose.CAD. Lihat [Aspose.CAD Purchase](https://purchase.aspose.com/buy) untuk detail.

### Q5: Di mana saya dapat mencari bantuan atau berdiskusi tentang pertanyaan terkait Aspose.CAD?

A5: Kunjungi [forum Aspose.CAD](https://forum.aspose.com/c/cad/19) untuk terhubung dengan komunitas dan mendapatkan dukungan.

## FAQ Tambahan

**Q: Bagaimana cara menghasilkan PDF dari DWG tanpa menambahkan teks?**  
A: Lewati langkah pembuatan `CadText` dan langsung konfigurasikan `PdfOptions` sebelum memanggil `image.Save(...)`.

**Q: Bisakah saya mengubah warna teks secara programatis?**  
A: Ya, atur `cadText.ColorId` ke nomor warna ACI tertentu (mis., 1 untuk merah).

**Q: Apakah memungkinkan menyisipkan teks multiline?**  
A: Gunakan `CadMText` untuk blok teks multiline; pendekatannya mirip dengan `CadText`.

**Q: Apakah Aspose.CAD mendukung konversi batch beberapa file DWG?**  
A: Tentu – lakukan loop melalui direktori file DWG, terapkan langkah yang sama, dan simpan masing‑masing sebagai PDF.

## Kesimpulan

Anda kini memiliki alur kerja lengkap yang siap produksi untuk **mengonversi DWG ke PDF**, **menambahkan teks khusus**, dan **menyesuaikan tampilan teks** menggunakan C# dan Aspose.CAD. Teknik ini ideal untuk pembuatan gambar otomatis, pipeline pelaporan, atau skenario apa pun di mana Anda perlu memperkaya file CAD secara langsung.

---

**Terakhir Diperbarui:** 2026-04-06  
**Diuji Dengan:** Aspose.CAD 24.11 for .NET  
**Penulis:** Aspose  

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}