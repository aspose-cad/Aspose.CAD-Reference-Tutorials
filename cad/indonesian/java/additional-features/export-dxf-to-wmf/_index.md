---
date: 2026-06-09
description: Pelajari cara mengonversi DXF ke WMF dengan Aspose.CAD untuk Java, termasuk
  percobaan gratis, dukungan Java 8+, dan ekspor PDF opsional. Panduan langkah demi
  langkah dengan contoh kode.
keywords:
- convert dxf to wmf
- aspose cad java
- aspose free trial
- aspose cad conversion
- export dxf pdf
linktitle: Ekspor DXF ke Format WMF Menggunakan Java
schemas:
- author: Aspose
  dateModified: '2026-06-09'
  description: Learn how to convert DXF to WMF with Aspose.CAD for Java, including
    a free trial, Java 8+ support, and optional PDF export. Step‑by‑step guide with
    code examples.
  headline: Convert DXF to WMF Using Aspose.CAD in Java
  type: TechArticle
- description: Learn how to convert DXF to WMF with Aspose.CAD for Java, including
    a free trial, Java 8+ support, and optional PDF export. Step‑by‑step guide with
    code examples.
  name: Convert DXF to WMF Using Aspose.CAD in Java
  steps:
  - name: Load DXF Drawing
    text: Image.load reads the DXF file into an Aspose.CAD Image object.
  - name: Configure Rasterization Options
    text: CadRasterizationOptions specifies page size, resolution, and background
      for rasterizing the CAD drawing.
  - name: Save as WMF
    text: ImageSaveOptions with SaveFormat.WMF tells Aspose.CAD to write the output
      as a Windows Metafile.
  - name: Dispose of Resources
    text: Calling image.close() releases native resources used by the Aspose.CAD Image
      object.
  - name: Optional – Export to PDF
    text: PdfOptions configures PDF‑specific settings when saving the image as a PDF
      document. > **Pro tip:** You can reuse the same `CadRasterizationOptions` object
      for PDF export by passing it to a `PdfOptions` instance, saving you a few lines
      of setup.
  type: HowTo
- questions:
  - answer: Yes. Load the file in a try‑with‑resources block and dispose of the `Image`
      object promptly. Adjust `CadRasterizationOptions.setPageWidth/Height` to a reasonable
      size to keep memory usage low.
    question: Can I convert large DXF files (hundreds of MB) without running out of
      memory?
  - answer: WMF is a flat vector format, so layer hierarchy is flattened, but line
      styles, colors, and hatch patterns are preserved.
    question: Does the WMF output retain layer information?
  - answer: Use `rasterizationOptions.setResolution(300);` to define DPI before saving.
    question: Is it possible to set a custom DPI for the WMF?
  - answer: Absolutely. Loop through a directory, load each file, and apply the same
      rasterization and save logic.
    question: Can I batch‑convert multiple DXF files in one run?
  - answer: Aspose.CAD for Java supports Java 8 and later, including Java 11, 17,
      and newer LTS releases.
    question: What versions of Java are supported?
  type: FAQPage
second_title: Aspose.CAD Java API
title: Konversi DXF ke WMF Menggunakan Aspose.CAD di Java
url: /id/java/additional-features/export-dxf-to-wmf/
weight: 14
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Mengonversi DXF ke WMF Menggunakan Aspose.CAD di Java

## Pendahuluan

Dalam tutorial ini Anda akan mempelajari cara **mengonversi DXF ke WMF** dengan Aspose.CAD untuk Java. Baik Anda perlu menyematkan gambar CAD dalam laporan berbasis Windows, menghasilkan grafik vektor ringan untuk dokumen Office, atau mengotomatiskan konversi batch, mengonversi DXF ke WMF adalah kebutuhan yang sering muncul dalam alur kerja rekayasa dan pelaporan. Kami akan memandu Anda melalui proses memuat gambar DXF, mengonfigurasi opsi rasterisasi, menyimpan hasil sebagai WMF, dan secara opsional mengekspor gambar yang sama ke PDF.

## Jawaban Cepat
- **Apakah saya dapat mengonversi DXF ke WMF dengan percobaan gratis?** Ya – Aspose menawarkan percobaan penuh selama 30‑hari.  
- **Versi Java apa yang diperlukan?** Java 8 atau lebih baru.  
- **Apakah saya memerlukan lisensi untuk menjalankan kode?** Lisensi diperlukan untuk produksi; percobaan dapat digunakan untuk pengembangan dan pengujian.  
- **Apakah konversi tanpa kehilangan?** Data vektor dipertahankan; opsi rasterisasi memungkinkan Anda mengontrol resolusi.  
- **Apakah saya juga dapat mengekspor gambar yang sama ke PDF?** Tentu – lihat langkah “Export to PDF” di bawah.

## Apa itu “convert DXF to WMF”?

Mengonversi DXF ke WMF berarti mengambil file Drawing Exchange Format (DXF) — format CAD yang banyak digunakan — dan mengubahnya menjadi Windows Metafile (WMF). WMF adalah format gambar vektor yang terintegrasi dengan mulus ke Microsoft Office, aplikasi Windows, dan banyak alat pelaporan.

## Mengapa menggunakan Aspose.CAD untuk Java?

Aspose.CAD untuk Java menyediakan mesin murni‑Java, tanpa DLL native, yang mengonversi file CAD dengan **lebih dari 99 % fidelitas vektor**, mempertahankan lapisan, warna, gaya garis, dan pola hatch. Ia mendukung **lebih dari 50 format input dan output** — termasuk DXF, DWG, DGN, PDF, PNG, SVG, dan WMF — sambil memungkinkan Anda menyesuaikan ukuran halaman, DPI, dan warna latar melalui opsi rasterisasi bawaan. API yang sama juga menangani ekspor ke PDF, PNG, dan SVG, menghilangkan kebutuhan akan banyak pustaka.

### Keunggulan Utama
- **Tidak ada dependensi eksternal** – Java murni, bekerja pada semua OS yang menjalankan Java.  
- **Rendering berfidelitas tinggi** – mempertahankan ketebalan garis, warna, dan detail hatch.  
- **Rasterisasi bawaan** – mengontrol dimensi halaman, resolusi, dan latar belakang.  
- **Konversi satu pintu** – kelas yang sama mengekspor ke WMF, PDF, PNG, SVG, dll.

## Prasyarat

Sebelum memulai, pastikan Anda memiliki:

- **Aspose.CAD for Java** terintegrasi ke dalam proyek Anda. Unduh dari situs resmi: [Aspose.CAD Java download](https://releases.aspose.com/cad/java/).  
- **Direktori dokumen** tempat file DXF Anda disimpan (misalnya `Your Document Directory/DXFDrawings/`).  

## Impor Namespace

Impor berikut membawa kelas Aspose.CAD yang diperlukan untuk memuat, meraster, dan menyimpan file CAD.  
```java
import com.aspose.cad.Image;
import com.aspose.cad.ImageSaveOptions;
import com.aspose.cad.fileformats.cad.CadRasterizationOptions;
import com.aspose.cad.fileformats.cad.CadImage;
import com.aspose.cad.fileformats.cad.CadImageInfo;
import com.aspose.cad.fileformats.cad.CadImageInfo;
import java.awt.Color;
```

## Panduan Langkah‑per‑Langkah

### Bagaimana cara mengonversi DXF ke WMF di Java?

Muat file DXF Anda dengan `Image.load("yourFile.dxf")`, konfigurasikan `CadRasterizationOptions` untuk ukuran halaman dan DPI yang diinginkan, lalu panggil `image.save("output.wmf", new ImageSaveOptions(SaveFormat.WMF))`. Pola tiga langkah ini melakukan konversi lengkap sambil mempertahankan kualitas vektor dan hanya memerlukan beberapa baris kode.

#### Langkah 1: Muat Gambar DXF

`Image.load` membaca file DXF ke dalam objek Aspose.CAD Image.  
```java
import com.aspose.cad.Color;
import com.aspose.cad.Image;

import com.aspose.cad.fileformats.ifc.IfcImage;
import com.aspose.cad.imageoptions.CadRasterizationOptions;
import com.aspose.cad.imageoptions.PdfOptions;
import com.aspose.cad.imageoptions.WmfOptions;
```

#### Langkah 2: Konfigurasikan Opsi Rasterisasi

`CadRasterizationOptions` menentukan ukuran halaman, resolusi, dan latar belakang untuk meraster gambar CAD.  
```java
// The path to the resource directory.
String dataDir = "Your Document Directory" + "DXFDrawings/";
String srcFile = dataDir + "conic_pyramid.dxf";
Image image = Image.load(srcFile);
```

#### Langkah 3: Simpan sebagai WMF

`ImageSaveOptions` dengan `SaveFormat.WMF` memberi tahu Aspose.CAD untuk menulis output sebagai Windows Metafile.  
```java
CadRasterizationOptions rasterizationOptions = new CadRasterizationOptions();
rasterizationOptions.setPageWidth(100);
rasterizationOptions.setPageHeight(100);
WmfOptions wmfOptions = new WmfOptions();
```

#### Langkah 4: Buang Sumber Daya

Memanggil `image.close()` melepaskan sumber daya native yang digunakan oleh objek Aspose.CAD Image.  
```java
cadImage.save(dataDir+" example.ifc.wmf", wmfOptions);
```

#### Langkah 5: Opsional – Ekspor ke PDF

`PdfOptions` mengonfigurasi pengaturan khusus PDF saat menyimpan gambar sebagai dokumen PDF.  
```java
finally
{
  cadImage.dispose();
}
```

> **Pro tip:** Anda dapat menggunakan kembali objek `CadRasterizationOptions` yang sama untuk ekspor PDF dengan memberikannya ke instance `PdfOptions`, menghemat beberapa baris pengaturan.

## Bagaimana cara mengekspor DXF ke PDF menggunakan Aspose CAD Java?

Ekspor ke PDF mengikuti langkah pemuatan dan rasterisasi yang sama; cukup ganti format penyimpanan WMF dengan PDF. Gunakan `new ImageSaveOptions(SaveFormat.Pdf)` dan secara opsional atur opsi khusus PDF seperti tingkat kompresi atau metadata penulis. Konversi satu baris ini menghasilkan PDF yang dapat dicari, akurat halaman, yang mencerminkan tata letak CAD asli.

## Masalah Umum dan Solusinya

| Masalah | Penyebab | Solusi |
|-------|-------|-----|
| **`NullPointerException` on `cadImage.save`** | Variabel `cadImage` tidak didefinisikan (seharusnya `image`). | Ganti `cadImage` dengan `image` atau ubah nama variabel secara konsisten. |
| **Output WMF is blank** | Ukuran halaman rasterisasi terlalu kecil atau warna latar diatur ke transparan. | Tingkatkan `PageWidth`/`PageHeight` atau setel warna latar melalui `rasterizationOptions.setBackgroundColor(Color.WHITE);`. |
| **License exception** | Menjalankan tanpa lisensi Aspose yang valid di produksi. | Terapkan file lisensi saat aplikasi dimulai: `License license = new License(); license.setLicense("Aspose.Total.Java.lic");`. |

## Kesimpulan

Anda kini memiliki alur kerja lengkap dan siap produksi untuk **mengonversi DXF ke WMF** menggunakan Aspose.CAD untuk Java, dengan langkah opsional untuk **mengekspor gambar yang sama ke PDF**. Pendekatan ini memberikan output vektor berkualitas tinggi yang terintegrasi mulus dengan alat pelaporan dan dokumentasi berbasis Windows, sambil menjaga basis kode Anda tetap sederhana dan bebas dependensi.

## FAQ

### Q1: Di mana saya dapat menemukan dokumentasi Aspose.CAD?

A1: Anda dapat mengakses dokumentasi [di sini](https://reference.aspose.com/cad/java/).

### Q2: Bagaimana cara mengunduh Aspose.CAD untuk Java?

A2: Unduh pustaka [di sini](https://releases.aspose.com/cad/java/).

### Q3: Apakah tersedia percobaan gratis?

A3: Ya, Anda dapat mendapatkan percobaan gratis [di sini](https://releases.aspose.com/).

### Q4: Membutuhkan opsi lisensi sementara?

A4: Jelajahi lisensi sementara [di sini](https://purchase.aspose.com/temporary-license/).

### Q5: Di mana saya dapat mendapatkan dukungan?

A5: Kunjungi forum dukungan Aspose.CAD [di sini](https://forum.aspose.com/c/cad/19).

## Pertanyaan yang Sering Diajukan

**Q: Apakah saya dapat mengonversi file DXF besar (ratusan MB) tanpa kehabisan memori?**  
A: Ya. Muat file dalam blok `try‑with‑resources` dan buang objek `Image` segera. Sesuaikan `CadRasterizationOptions.setPageWidth/Height` ke ukuran yang wajar untuk menjaga penggunaan memori tetap rendah.

**Q: Apakah output WMF mempertahankan informasi lapisan?**  
A: WMF adalah format vektor datar, sehingga hierarki lapisan diluruskan, namun gaya garis, warna, dan pola hatch tetap dipertahankan.

**Q: Apakah memungkinkan mengatur DPI khusus untuk WMF?**  
A: Gunakan `rasterizationOptions.setResolution(300);` untuk menentukan DPI sebelum menyimpan.

**Q: Dapatkah saya mengonversi batch banyak file DXF dalam satu kali jalan?**  
A: Tentu. Loop melalui sebuah direktori, muat tiap file, dan terapkan logika rasterisasi serta penyimpanan yang sama.

**Q: Versi Java apa yang didukung?**  
A: Aspose.CAD untuk Java mendukung Java 8 dan yang lebih baru, termasuk Java 11, 17, dan rilis LTS terbaru.

**Last Updated:** 2026-06-09  
**Tested With:** Aspose.CAD for Java 24.11  
**Author:** Aspose

```java
image.save(dataDir + "conic_pyramid_out_.pdf"); 
```

## Tutorial Terkait

- [Create PDF from CAD – Export DXF to PDF with Aspose.CAD for Java](/cad/java/additional-features/export-dxf-to-pdf/)
- [Create PDF from DXF: Export Layer with Aspose.CAD for Java](/cad/java/additional-features/export-specific-layer-to-pdf/)
- [How to Convert DXF Layout to JPEG Image with Aspose.CAD in Java](/cad/java/additional-features/export-specific-layout-to-image/)


{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}