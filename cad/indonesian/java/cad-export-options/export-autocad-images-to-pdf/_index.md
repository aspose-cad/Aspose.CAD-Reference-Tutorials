---
date: 2026-10-19
description: Pelajari cara mengonversi DWG ke PDF di Java dengan Aspose.CAD. Panduan
  langkah demi langkah ini menunjukkan cara mengekspor PDF AutoCAD, menyimpan CAD
  sebagai PDF, dan menerapkan lisensi.
keywords:
- dwg to pdf java
- export autocad pdf
- java pdf export library
- aspose cad license
- save cad pdf
- customize pdf page size
lastmod: 2026-10-19
linktitle: Ekspor Gambar AutoCAD ke PDF
og_description: Pelajari cara mengonversi DWG ke PDF di Java dengan Aspose.CAD. Panduan
  ini memandu Anda melalui proses mengekspor PDF AutoCAD, menyimpan CAD sebagai PDF,
  dan lisensi.
og_image_alt: 'Tutorial: convert DWG to PDF in Java with Aspose.CAD'
og_title: Mengonversi DWG ke PDF di Java menggunakan Aspose.CAD
schemas:
- author: Aspose
  dateModified: '2026-10-19'
  description: Learn how to convert DWG to PDF in Java with Aspose.CAD. This step‑by‑step
    guide shows you how to export AutoCAD PDF, save CAD as PDF, and apply a license.
  headline: Convert DWG to PDF in Java using Aspose.CAD
  type: TechArticle
- description: Learn how to convert DWG to PDF in Java with Aspose.CAD. This step‑by‑step
    guide shows you how to export AutoCAD PDF, save CAD as PDF, and apply a license.
  name: Convert DWG to PDF in Java using Aspose.CAD
  steps:
  - name: set the resource directory path
    text: Replace `"Your Document Directory"` with the absolute path to the folder
      you created in the prerequisites. > **Pro tip:** Use `Paths.get(...).toAbsolutePath()`
      to avoid path‑related errors on different operating systems.
  - name: load the CAD image
    text: Loading the CAD file into an `Image` object gives you full access to Aspose.CAD’s
      rasterization engine. The `Image` class loads the DWG file and prepares it for
      conversion. > **Why this matters:** Once the drawing is in memory, you can query
      its layouts, layers, and metadata before rasterizing.
  - name: set rasterization options
    text: Adjust `pageWidth` and `pageHeight` to **customize PDF page size**. Enabling
      `setTypeOfEntities(TypeOfEntities.Entities3D)` allows full 3‑D rendering when
      needed. The `RasterizationOptions` object controls DPI, page dimensions, and
      entity types for the output. - `pageWidth` / `pageHeight` are measur
  - name: configure PDF options
    text: Tie the rasterization settings to the PDF output, ensuring the vector data
      is correctly transformed. The `PdfOptions` class links the rasterization configuration
      with the final PDF file.
  - name: save the PDF
    text: The resulting file, `Export3DImagestoPDF_out_.pdf`, is a **save cad as pdf**
      representation of your original AutoCAD drawing. The `save` method writes the
      rasterized image to a PDF file on disk.
  type: HowTo
- questions:
  - answer: Yes – the library supports DWG, DXF, DWF, DGN, and over 30 additional
      formats, giving you flexibility across projects.
    question: Can I use Aspose.CAD for Java with other CAD file formats?
  - answer: Visit the [temporary license page](https://purchase.aspose.com/temporary-license/)
      to request a time‑limited license for evaluation.
    question: How do I obtain a temporary license for Aspose.CAD for Java?
  - answer: Absolutely. Use `setLayouts("Model")`, `setLayouts("Layout1")`, etc.,
      to choose which view is rendered into the PDF.
    question: Are there layout options for rasterization?
  - answer: Yes – modify `pageWidth` and `pageHeight` in the rasterization options
      to match any required page dimensions.
    question: Can I change the size of the output PDF file?
  - answer: The dedicated community is available at the [Aspose.CAD forum](https://forum.aspose.com/c/cad/19)
      where you can ask questions and share solutions.
    question: Where can I get help if I run into problems?
  type: FAQPage
second_title: Aspose.CAD Java API
tags:
- dwg to pdf
- aspose.cad
- java cad conversion
- export autocad pdf
title: Mengonversi DWG ke PDF di Java menggunakan Aspose.CAD
url: /id/java/cad-export-options/export-autocad-images-to-pdf/
weight: 10
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Ekspor PDF AutoCAD – mengekspor gambar AutoCAD ke PDF dengan Aspose.CAD untuk Java

## Pendahuluan

Jika Anda perlu **mengonversi DWG ke PDF dalam Java**, Anda berada di tempat yang tepat. Tutorial ini menunjukkan cara mengekspor gambar AutoCAD ke PDF menggunakan Aspose.CAD untuk Java, sebuah pustaka murni‑Java yang menangani DWG, DXF, DWF, dan banyak format CAD lainnya tanpa ketergantungan native. Pada akhir tutorial Anda akan dapat **menyimpan CAD sebagai PDF**, menyesuaikan opsi rasterisasi seperti ukuran halaman, dan menerapkan **lisensi Aspose CAD** dengan benar untuk penggunaan produksi.

## Jawaban Cepat
- **Apakah saya dapat mengonversi DWG ke PDF dengan Java?** Ya – Aspose.CAD untuk Java secara native mendukung DWG, DXF, dan puluhan format CAD lainnya.  
- **Apakah saya memerlukan lisensi?** Lisensi **Aspose CAD** permanen menghapus semua batasan evaluasi; lisensi sementara tersedia untuk pengujian.  
- **Versi Java mana yang didukung?** Java 8 dan yang lebih tinggi didukung sepenuhnya.  
- **Bisakah saya mengontrol dimensi halaman PDF?** Tentu – atur `pageWidth` dan `pageHeight` dalam opsi rasterisasi.  
- **Apakah rendering 3‑D memungkinkan?** Ya – aktifkan `TypeOfEntities.Entities3D` untuk merasterisasi entitas 3‑D.

## Apa itu ekspor PDF AutoCAD?
Mengekspor PDF AutoCAD adalah proses mengubah gambar CAD vektor menjadi dokumen PDF portabel. Proses ini mempertahankan lapisan, ketebalan garis, warna, dan secara opsional geometri 3‑D, sehingga mudah berbagi desain dengan klien atau mengarsipkannya tanpa memerlukan perangkat lunak CAD.

## Mengapa mengonversi DWG ke PDF dengan Aspose.CAD untuk Java?
Aspose.CAD mendukung **lebih dari 50 format input dan output**, memproses gambar ber‑ratus halaman tanpa memuat seluruh file ke memori, dan berjalan di platform apa pun yang mendukung Java 8+. Pustaka ini memberi Anda kontrol penuh atas DPI, ukuran halaman, dan tata letak, sehingga Anda dapat **menyesuaikan ukuran halaman PDF** agar sesuai dengan spesifikasi proyek yang tepat, semuanya tanpa menginstal DLL native.

## Prasyarat

- **Java Development Kit** – JDK 8 atau yang lebih baru terpasang di workstation Anda.  
- **Aspose.CAD untuk Java** – unduh JAR terbaru dari [tautan unduhan](https://releases.aspose.com/cad/java/).  
- **Direktori kerja** – folder tempat file DWG sumber Anda dan PDF yang dihasilkan akan disimpan.

## Impor namespace

Kelas `Image` mewakili gambar CAD yang dapat dirasterisasi, sementara `RasterizationOptions` dan `PdfOptions` memungkinkan Anda menyetel detail konversi.

Kelas `Image` adalah objek tingkat‑atas Aspose.CAD yang menyimpan gambar CAD dalam memori.  
Kelas `RasterizationOptions` menentukan bagaimana data vektor dirasterisasi sebelum ditulis ke PDF.  
Kelas `PdfOptions` menggabungkan pengaturan rasterisasi dengan parameter keluaran khusus PDF.

```java
import com.aspose.cad.Image;

import com.aspose.cad.imageoptions.CadRasterizationOptions;
import com.aspose.cad.imageoptions.PdfOptions;
//import com.aspose.cad.imageoptions.TypeOfEntities;
```

Sekarang mari kita tinjau kode langkah demi langkah.

## Cara mengonversi DWG ke PDF dengan Aspose.CAD untuk Java?

Untuk mengonversi file DWG ke PDF dengan Aspose.CAD untuk Java, muat gambar menggunakan kelas Image, konfigurasikan CadRasterizationOptions (seperti DPI, ukuran halaman, dan tipe entitas), bungkus opsi tersebut dalam PdfOptions, lalu panggil metode save dengan menentukan nama file .pdf. Urutan ini memastikan data vektor dirasterisasi dengan benar dan PDF yang dihasilkan sesuai dengan kebutuhan tata letak Anda.

### Langkah 1: atur jalur direktori sumber daya

Ganti `"Your Document Directory"` dengan jalur absolut ke folder yang Anda buat pada bagian prasyarat.

```java
String dataDir = "Your Document Directory" + "ExportingCAD/";
```

> **Pro tip:** Gunakan `Paths.get(...).toAbsolutePath()` untuk menghindari kesalahan terkait jalur pada sistem operasi yang berbeda.

### Langkah 2: muat gambar CAD

Memuat file CAD ke dalam objek `Image` memberi Anda akses penuh ke mesin rasterisasi Aspose.CAD.

Kelas `Image` memuat file DWG dan menyiapkannya untuk konversi.

```java
String srcFile = dataDir + "conic_pyramid.dxf";
Image cadImage = Image.load(srcFile);
```

> **Mengapa ini penting:** Setelah gambar berada di memori, Anda dapat menanyakan tata letak, lapisan, dan metadata sebelum merasterisasi.

### Langkah 3: atur opsi rasterisasi

Sesuaikan `pageWidth` dan `pageHeight` untuk **menyesuaikan ukuran halaman PDF**. Mengaktifkan `setTypeOfEntities(TypeOfEntities.Entities3D)` memungkinkan rendering 3‑D penuh bila diperlukan.

Objek `RasterizationOptions` mengontrol DPI, dimensi halaman, dan tipe entitas untuk output.

```java
CadRasterizationOptions rasterizationOptions = new CadRasterizationOptions();
rasterizationOptions.setPageWidth(500);
rasterizationOptions.setPageHeight(500);
// rasterizationOptions.setTypeOfEntities(TypeOfEntities.Entities3D);

rasterizationOptions.setLayouts(new String[] {"Model"});
```

- `pageWidth` / `pageHeight` diukur dalam poin (1 pt = 1/72 in).  
- Hapus komentar pada baris `setTypeOfEntities` untuk rasterisasi 3‑D.  
- `setLayouts` memilih tata letak mana (Model, Layout1, dll.) yang akan dirender.

### Langkah 4: konfigurasikan opsi PDF

Hubungkan pengaturan rasterisasi dengan output PDF, memastikan data vektor ditransformasikan dengan benar.

Kelas `PdfOptions` mengaitkan konfigurasi rasterisasi dengan file PDF akhir.

```java
PdfOptions pdfOptions = new PdfOptions();
pdfOptions.setVectorRasterizationOptions(rasterizationOptions);
```

### Langkah 5: simpan PDF

File yang dihasilkan, `Export3DImagestoPDF_out_.pdf`, merupakan representasi **menyimpan CAD sebagai PDF** dari gambar AutoCAD asli Anda.

Metode `save` menulis gambar yang dirasterisasi ke file PDF di disk.

```java
cadImage.save(dataDir + "Export3DImagestoPDF_out_.pdf", pdfOptions);
```

## Masalah Umum & Solusi

| Gejala | Penyebab Kemungkinan | Solusi |
|--------|----------------------|--------|
| PDF kosong | Opsi rasterisasi tidak disetel atau tata letak tidak cocok | Verifikasi bahwa `setLayouts` sesuai dengan nama tata letak dalam file CAD Anda. |
| Gambar ber‑resolusi rendah | `pageWidth`/`pageHeight` terlalu kecil | Tingkatkan dimensi atau atur DPI lebih tinggi melalui `rasterizationOptions.setResolution(...)`. |
| Pengecualian lisensi | Lisensi yang berlaku tidak diterapkan | Terapkan **lisensi Aspose CAD** atau gunakan lisensi sementara untuk pengujian. |

## Pertanyaan yang Sering Diajukan

**Q:** Apakah saya dapat menggunakan Aspose.CAD untuk Java dengan format file CAD lainnya?  
**A:** Ya – pustaka ini mendukung DWG, DXF, DWF, DGN, dan lebih dari 30 format tambahan, memberi Anda fleksibilitas lintas proyek.

**Q:** Bagaimana cara mendapatkan lisensi sementara untuk Aspose.CAD untuk Java?  
**A:** Kunjungi [halaman lisensi sementara](https://purchase.aspose.com/temporary-license/) untuk meminta lisensi berjangka waktu untuk evaluasi.

**Q:** Apakah ada opsi tata letak untuk rasterisasi?  
**A:** Tentu. Gunakan `setLayouts("Model")`, `setLayouts("Layout1")`, dll., untuk memilih tampilan mana yang dirender ke PDF.

**Q:** Bisakah saya mengubah ukuran file PDF yang dihasilkan?  
**A:** Ya – modifikasi `pageWidth` dan `pageHeight` dalam opsi rasterisasi agar sesuai dengan dimensi halaman yang diperlukan.

**Q:** Di mana saya dapat mendapatkan bantuan jika mengalami masalah?  
**A:** Komunitas khusus tersedia di [forum Aspose.CAD](https://forum.aspose.com/c/cad/19) tempat Anda dapat mengajukan pertanyaan dan berbagi solusi.

---

**Terakhir Diperbarui:** 2026-10-19  
**Diuji Dengan:** Aspose.CAD untuk Java 24.10  
**Penulis:** Aspose

## Tutorial Terkait

- [Ekspor DWG ke PDF dalam Java – Atur Ukuran Halaman PDF dengan Aspose.CAD](/cad/java/cad-export-options/export-to-pdf/)
- [Ekspor DWG ke PDF: Tata Letak Spesifik Menggunakan Aspose.CAD untuk Java](/cad/java/cad-drawing-conversion/export-specific-dwg-layout-to-pdf/)
- [Ekspor DWG ke PDF dan Aktifkan Pelacakan dengan Aspose.CAD Java](/cad/java/additional-features/enable-tracking/)


{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}