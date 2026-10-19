---
date: 2026-10-19
description: Pelajari cara mengekspor gambar AutoCAD ke PDF dengan ukuran halaman
  PDF khusus menggunakan Aspose.CAD untuk Java. Panduan langkah demi langkah ini mencakup
  konversi DWG ke PDF, opsi rasterisasi, dan lisensi.
keywords:
- custom pdf page size
- export autocad to pdf
- save cad as pdf
- generate pdf from dwg
- dwg to pdf java
lastmod: 2026-10-19
linktitle: Ekspor Gambar AutoCAD ke PDF
og_description: Atur ukuran halaman PDF khusus saat mengekspor gambar AutoCAD ke PDF
  menggunakan Aspose.CAD untuk Java. Pelajari konversi DWG ke PDF, pengaturan rasterisasi,
  dan lisensi dalam hitungan menit.
og_image_alt: Guide showing how to export AutoCAD drawings to PDF with custom page
  dimensions using Aspose.CAD for Java
og_title: Atur ukuran halaman PDF khusus untuk ekspor AutoCAD dengan Aspose.CAD
schemas:
- author: Aspose
  dateModified: '2026-10-19'
  description: Learn how to export AutoCAD drawings to PDF with a custom PDF page
    size using Aspose.CAD for Java. This step‑by‑step guide covers converting DWG
    to PDF, rasterization options, and licensing.
  headline: Set custom PDF page size for AutoCAD export with Aspose.CAD
  type: TechArticle
- description: Learn how to export AutoCAD drawings to PDF with a custom PDF page
    size using Aspose.CAD for Java. This step‑by‑step guide covers converting DWG
    to PDF, rasterization options, and licensing.
  name: Set custom PDF page size for AutoCAD export with Aspose.CAD
  steps:
  - name: set the resource directory path
    text: '> **Pro tip:** Replace `"Your Document Directory"` with the absolute path
      to the folder you created in the prerequisites.'
  - name: load the CAD image
    text: The `Image` class loads the CAD file and gives you access to Aspose.CAD’s
      rasterization engine. > **Why this matters:** Once the CAD file is loaded, you
      can manipulate rasterization options before rendering to PDF.
  - name: set rasterization options
    text: The `CadRasterizationOptions` class specifies how the CAD drawing is rasterized
      before being saved as PDF. Adjust `pageWidth` and `pageHeight` to define a **custom
      PDF page size**. You can also enable 3‑D rendering by uncommenting the `setTypeOfEntities`
      line. - `pageWidth` / `pageHeight` – measured
  - name: configure PDF options
    text: The `PdfOptions` class holds PDF‑specific settings and links the rasterization
      options to the output file, ensuring the custom page dimensions are applied
      correctly.
  - name: save the PDF
    text: The `save` method writes the rendered image to the specified PDF file. The
      resulting file, `Export3DImagestoPDF_out_.pdf`, is a **save cad as pdf** representation
      of your original AutoCAD drawing with the exact page dimensions you specified.
  type: HowTo
- questions:
  - answer: Yes, the library supports DWG, DXF, DWF, DGN, and many more, giving you
      flexibility across projects.
    question: Can I use Aspose.CAD for Java with other CAD file formats?
  - answer: Visit the [temporary license page](https://purchase.aspose.com/temporary-license/)
      to request a time‑limited license for evaluation.
    question: How do I obtain a temporary license for Aspose.CAD for Java?
  - answer: Absolutely. Use `setLayouts("Model")` or specify other layout names to
      control which view is rendered.
    question: Are there layout options for rasterization?
  - answer: Yes – modify `pageWidth` and `pageHeight` in the rasterization options
      to any dimensions you need.
    question: Can I customize the size of the output PDF file?
  - answer: The dedicated [Aspose.CAD forum](https://forum.aspose.com/c/cad/19) offers
      community support and official responses from the Aspose team.
    question: Where can I get help or discuss issues related to Aspose.CAD for Java?
  type: FAQPage
second_title: Aspose.CAD Java API
tags:
- custom pdf page size
- Aspose.CAD
- Java CAD conversion
- PDF generation
- DWG export
title: Atur ukuran halaman PDF khusus untuk ekspor AutoCAD dengan Aspose.CAD
url: /id/java/cad-export-options/export-autocad-images-to-pdf/
weight: 10
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Ekspor AutoCAD PDF - mengekspor gambar AutoCAD ke PDF dengan Aspose.CAD untuk Java

## Pendahuluan

Jika Anda perlu **mengonversi DWG ke PDF** dan mengontrol dimensi tepat dari file output, Anda berada di tempat yang tepat. Tutorial ini menunjukkan cara **mengatur ukuran halaman PDF khusus** saat mengekspor gambar AutoCAD ke PDF dengan Aspose.CAD untuk Java. Pada akhir panduan Anda akan tahu cara memuat DWG, mengonfigurasi opsi rasterisasi seperti DPI dan lebar/tinggi halaman, menerapkan lisensi, dan menghasilkan PDF siap produksi.

## Jawaban Cepat
- **Apakah saya dapat mengonversi DWG ke PDF dengan Java?** Ya – Aspose.CAD untuk Java secara native mendukung DWG, DXF, DWF, dan banyak format CAD lainnya.  
- **Apakah saya memerlukan lisensi untuk penggunaan produksi?** Lisensi penuh Aspose.CAD menghapus semua batas evaluasi; lisensi sementara tersedia untuk pengujian.  
- **Versi Java mana yang kompatibel?** Perpustakaan ini bekerja dengan Java 8 dan JDK yang lebih baru.  
- **Bagaimana cara mengubah dimensi halaman PDF?** Atur `pageWidth` dan `pageHeight` pada `PdfOptions.getRasterizationOptions()` ke ukuran apa pun yang Anda perlukan.  
- **Apakah rendering 3‑D didukung?** Ya – aktifkan `TypeOfEntities.Entities3D` untuk meraster entitas 3‑D.

## Apa itu ekspor AutoCAD PDF?
Mengekspor AutoCAD PDF berarti mengonversi gambar CAD berbasis vektor (DWG, DXF, DWF, dll.) menjadi dokumen PDF portabel sambil mempertahankan lapisan, ketebalan garis, dan geometri 3‑D opsional. Hal ini memungkinkan Anda berbagi desain dengan klien, mengarsipkan gambar, atau mencetak tanpa menginstal perangkat lunak CAD.

## Mengapa menggunakan Aspose.CAD untuk Java untuk mengonversi DWG ke PDF?
Aspose.CAD untuk Java ideal untuk mengonversi DWG ke PDF karena menawarkan dukungan format yang luas, berjalan pada Java murni tanpa dependensi native, menyediakan rasterisasi resolusi tinggi dengan kontrol penuh atas DPI dan ukuran halaman, serta memiliki lisensi fleksibel yang memungkinkan Anda memulai dengan trial dan meningkatkan ke produksi.

- **Cakupan format yang luas** – mendukung lebih dari 50 format input dan output, termasuk DWG, DXF, DWF, DGN, dan PDF.  
- **Implementasi Java murni** – tidak ada DLL native atau dependensi eksternal, sehingga penyebaran mudah di platform apa pun.  
- **Rasterisasi resolusi tinggi** – Anda dapat menentukan DPI, ukuran halaman, dan tata letak, memberi Anda kontrol penuh atas **ukuran halaman PDF khusus** hasil akhir.  
- **Lisensi yang dapat diskalakan** – mulai dengan trial gratis, lalu upgrade ke **lisensi Aspose CAD** permanen.  

## Prasyarat

- **Java Development Kit** – JDK 8 atau lebih baru terpasang di mesin Anda.  
- **Aspose.CAD untuk Java** – unduh JAR terbaru dari [tautan unduhan](https://releases.aspose.com/cad/java/).  
- **Direktori kerja** – folder yang berisi file DWG sumber dan akan menerima PDF yang dihasilkan.

## Impor namespace

Kelas `Image` adalah objek inti Aspose.CAD yang mewakili gambar CAD dalam memori. Impor paket yang diperlukan sebelum Anda mulai menulis kode.

```java
import com.aspose.cad.Image;

import com.aspose.cad.imageoptions.CadRasterizationOptions;
import com.aspose.cad.imageoptions.PdfOptions;
//import com.aspose.cad.imageoptions.TypeOfEntities;
```

Sekarang mari kita bahas kode langkah demi langkah.

## Cara mengatur ukuran halaman PDF khusus saat mengekspor DWG ke PDF?

Muat DWG Anda, tentukan lebar dan tinggi halaman yang diinginkan, lalu simpan hasilnya sebagai PDF – itu saja yang Anda perlukan untuk membuat PDF dengan ukuran halaman khusus. Langkah‑langkah berikut menggambarkan urutan tepat dan kode minimal yang diperlukan.

### Langkah 1: atur jalur direktori sumber daya

```java
String dataDir = "Your Document Directory" + "ExportingCAD/";
```

> **Pro tip:** Ganti `"Your Document Directory"` dengan jalur absolut ke folder yang Anda buat pada bagian prasyarat.

### Langkah 2: muat gambar CAD

Kelas `Image` memuat file CAD dan memberi Anda akses ke mesin rasterisasi Aspose.CAD.

```java
String srcFile = dataDir + "conic_pyramid.dxf";
Image cadImage = Image.load(srcFile);
```

> **Mengapa ini penting:** Setelah file CAD dimuat, Anda dapat memanipulasi opsi rasterisasi sebelum merender ke PDF.

### Langkah 3: atur opsi rasterisasi

Kelas `CadRasterizationOptions` menentukan bagaimana gambar CAD dirasterisasi sebelum disimpan sebagai PDF. Sesuaikan `pageWidth` dan `pageHeight` untuk mendefinisikan **ukuran halaman PDF khusus**. Anda juga dapat mengaktifkan rendering 3‑D dengan meng-uncomment baris `setTypeOfEntities`.

```java
CadRasterizationOptions rasterizationOptions = new CadRasterizationOptions();
rasterizationOptions.setPageWidth(500);
rasterizationOptions.setPageHeight(500);
// rasterizationOptions.setTypeOfEntities(TypeOfEntities.Entities3D);

rasterizationOptions.setLayouts(new String[] {"Model"});
```

- `pageWidth` / `pageHeight` – diukur dalam piksel; ubah nilai ini untuk mencocokkan A4, Letter, atau dimensi khusus apa pun.  
- `setTypeOfEntities(TypeOfEntities.Entities3D)` – merender entitas 3‑D bila diperlukan.  
- `setLayouts` – memilih layout (Model, Layout1, dll.) yang akan dirasterisasi.

### Langkah 4: konfigurasikan opsi PDF

Kelas `PdfOptions` menyimpan pengaturan khusus PDF dan menghubungkan opsi rasterisasi ke file output, memastikan dimensi halaman khusus diterapkan dengan benar.

```java
PdfOptions pdfOptions = new PdfOptions();
pdfOptions.setVectorRasterizationOptions(rasterizationOptions);
```

### Langkah 5: simpan PDF

Metode `save` menulis gambar yang dirasterisasi ke file PDF yang ditentukan.

```java
cadImage.save(dataDir + "Export3DImagestoPDF_out_.pdf", pdfOptions);
```

File yang dihasilkan, `Export3DImagestoPDF_out_.pdf`, adalah representasi **save cad as pdf** dari gambar AutoCAD asli Anda dengan dimensi halaman tepat yang Anda tentukan.

## Masalah umum & solusi

| Gejala | Penyebab yang mungkin | Solusi |
|---------|--------------|-----|
| PDF kosong | Opsi rasterisasi tidak diatur atau layout tidak cocok | Verifikasi `setLayouts` sesuai dengan nama layout di file CAD Anda. |
| Gambar beresolusi rendah | `pageWidth`/`pageHeight` terlalu kecil atau DPI rendah | Tingkatkan dimensi atau panggil `rasterizationOptions.setResolution(...)` dengan DPI lebih tinggi. |
| Pengecualian lisensi | Tidak ada lisensi yang valid diterapkan | Terapkan lisensi Aspose.CAD permanen atau gunakan lisensi sementara untuk pengujian. |

## Pertanyaan yang Sering Diajukan

**T: Apakah saya dapat menggunakan Aspose.CAD untuk Java dengan format file CAD lain?**  
J: Ya, perpustakaan ini mendukung DWG, DXF, DWF, DGN, dan banyak lagi, memberi Anda fleksibilitas lintas proyek.

**T: Bagaimana cara mendapatkan lisensi sementara untuk Aspose.CAD untuk Java?**  
J: Kunjungi [halaman lisensi sementara](https://purchase.aspose.com/temporary-license/) untuk meminta lisensi berjangka waktu untuk evaluasi.

**T: Apakah ada opsi layout untuk rasterisasi?**  
J: Tentu. Gunakan `setLayouts("Model")` atau tentukan nama layout lain untuk mengontrol tampilan yang dirasterisasi.

**T: Bisakah saya menyesuaikan ukuran file PDF output?**  
J: Ya – ubah `pageWidth` dan `pageHeight` dalam opsi rasterisasi ke dimensi apa pun yang Anda perlukan.

**T: Di mana saya dapat mendapatkan bantuan atau berdiskusi tentang masalah terkait Aspose.CAD untuk Java?**  
J: Forum khusus [Aspose.CAD](https://forum.aspose.com/c/cad/19) menyediakan dukungan komunitas dan respons resmi dari tim Aspose.

## FAQ Tambahan (format AI‑friendly)

**T: Apakah Aspose.CAD memerlukan pustaka native di Windows atau Linux?**  
J: Tidak. Aspose.CAD untuk Java adalah perpustakaan Java murni, sehingga berjalan di platform apa pun yang mendukung JDK tanpa DLL native tambahan.

**T: Seberapa besar file DWG yang dapat diproses perpustakaan?**  
J: Perpustakaan dapat menangani gambar berhingga ratusan halaman (hingga 500 MB) tanpa memuat seluruh file ke memori, berkat arsitektur streaming‑nya.

**T: Apakah memungkinkan melakukan konversi batch banyak file DWG ke PDF dalam satu run?**  
J: Ya. Iterasi melalui direktori, muat tiap file dengan `Image.load()`, terapkan opsi rasterisasi yang sama, dan panggil `save()` untuk setiap PDF output.

**T: Performa seperti apa yang dapat saya harapkan pada server tipikal?**  
J: Mengonversi DWG 100‑halaman pada 300 DPI di CPU 2.5 GHz standar memakan waktu sekitar 12 detik, berdasarkan benchmark Aspose.

**T: Apakah perpustakaan mempertahankan informasi lapisan di PDF?**  
J: Meskipun output dirasterisasi, tampilan visual lapisan, ketebalan garis, dan warna direproduksi secara akurat.

---

**Terakhir Diperbarui:** 2026-10-19  
**Diuji Dengan:** Aspose.CAD untuk Java 24.10  
**Penulis:** Aspose

## Tutorial Terkait

- [Export DWG to PDF and Enable Tracking with Aspose.CAD Java](/cad/java/additional-features/enable-tracking/)
- [Export DWG to PDF: Specific Layout Using Aspose.CAD Java](/cad/java/cad-drawing-conversion/export-specific-dwg-layout-to-pdf/)
- [Export DWG to BMP and Adjust CAD Size Using Unit Type with Aspose.CAD for Java](/cad/java/cad-file-manipulation/adjusting-cad-drawing-size-using-unit-type/)


{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}