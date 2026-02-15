---
date: 2026-02-15
description: Pelajari cara mengatur ukuran halaman PDF dan mengonversi CAD ke PDF
  menggunakan Aspose.CAD untuk Java, dengan penskalaan tata letak otomatis dan ekspor
  TIFF.
linktitle: Set PDF Page Size – Convert CAD to PDF
second_title: Aspose.CAD Java API
title: Atur Ukuran Halaman PDF – Konversi CAD ke PDF (Java)
url: /id/java/advanced-cad-features/set-canvas-size-and-mode/
weight: 16
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Set Canvas Size and Mode

## Introduction

Jika Anda perlu **set PDF page size** saat mengonversi gambar CAD ke PDF, Anda berada di tempat yang tepat. Dalam tutorial ini kami akan menunjukkan cara menggunakan Aspose.CAD for Java untuk menentukan dimensi kanvas yang tepat, mengaktifkan automatic layout scaling, dan kemudian mengekspor hasilnya ke PDF dan TIFF. Baik Anda menyiapkan skematik teknik untuk cetak atau menghasilkan thumbnail untuk galeri web, mengendalikan ukuran halaman dan resolusi output sangat penting.

## Quick Answers
- **What does “convert CAD to PDF” mean?** Transformasi gambar CAD (misalnya DXF, DWG) menjadi dokumen PDF yang dapat dilihat di platform apa pun.  
- **Can I also export to TIFF?** Ya—gunakan `TiffOptions` untuk membuat gambar raster beresolusi tinggi.  
- **Which option controls canvas size in Java?** `CadRasterizationOptions.setPageWidth/Height`.  
- **What is automatic layout scaling?** Sebuah flag (`setAutomaticLayoutsScaling(true)`) yang mempertahankan proporsi tata letak asli ketika ukuran kanvas berubah.  
- **Do I need a license for Aspose.CAD?** Lisensi sementara atau permanen diperlukan untuk penggunaan produksi.

## How to Set PDF Page Size When Converting CAD to PDF (Java)

Menentukan ukuran halaman PDF (atau ukuran kanvas) memungkinkan Anda mengatur dimensi akhir dokumen, yang sangat berguna ketika Anda harus **change PDF dimensions** agar sesuai dengan standar pencetakan atau kebutuhan UI. Di bawah ini kami akan membahas setiap langkah, menjelaskan *mengapa* di balik setiap baris kode.

## What is **convert CAD to PDF**?

Mengonversi CAD ke PDF berarti mengambil gambar teknik berbasis vektor dan merendernya sebagai halaman PDF, mempertahankan garis, lapisan, dan geometri sekaligus membuat file dapat diakses secara universal.

## Why set canvas size **java**?

Menentukan ukuran kanvas di Java memungkinkan Anda mendefinisikan resolusi output dan dimensi halaman, memastikan PDF atau TIFF yang dihasilkan sesuai dengan kebutuhan pencetakan atau tampilan Anda. Ini juga memberi Anda kontrol atas perilaku skala, yang penting untuk gambar berformat besar.

## Prerequisites

Sebelum menyelam ke tutorial, pastikan Anda memiliki prasyarat berikut:

- Aspose.CAD for Java: Pastikan Anda telah menginstal pustaka Aspose.CAD di lingkungan Java Anda. Anda dapat mengunduhnya [here](https://releases.aspose.com/cad/java/).
- Document Directory: Siapkan direktori dokumen untuk menyimpan file CAD Anda. Direktori ini akan direferensikan dalam langkah‑langkah tutorial.

Sekarang, mari kita mulai dengan panduan langkah‑demi‑langkah.

## Import Namespaces

Dalam langkah ini, kami akan mengimpor namespace yang diperlukan untuk memulai proyek Aspose.CAD Anda.

```java
import java.awt.Image;

import com.aspose.cad.fileformats.tiff.enums.TiffExpectedFormat;
import com.aspose.cad.imageoptions.CadRasterizationOptions;
import com.aspose.cad.imageoptions.PdfOptions;
import com.aspose.cad.imageoptions.TiffOptions;
```

## Step 1: Import Aspose.CAD Classes

```java
// The path to the resource directory.
String dataDir = "Your Document Directory" + "CADConversion/";

String srcFile = dataDir + "conic_pyramid.dxf";
com.aspose.cad.Image objImage = com.aspose.cad.Image.load(srcFile);
```

Dalam potongan kode ini, kami menyiapkan jalur ke direktori sumber daya dan memuat file DXF menggunakan kelas `Image` milik Aspose.CAD.

## Step 2: Set **CadRasterizationOptions** Properties (set canvas size java)

```java
// Create an instance of CadRasterizationOptions and set its various properties
CadRasterizationOptions rasterizationOptions = new CadRasterizationOptions();
rasterizationOptions.setPageWidth(1600);
rasterizationOptions.setPageHeight(1600);

rasterizationOptions.setAutomaticLayoutsScaling(true);
rasterizationOptions.setNoScaling(true);
```

Di sini, kami membuat instance `CadRasterizationOptions` dan mengonfigurasi properti seperti page width, page height, dan **automatic layout scaling**. Ini adalah inti dari **configure canvas mode** untuk konversi Anda.

## Step 3: Create PdfOptions and Set VectorRasterizationOptions

```java
// Create an instance of PdfOptions
PdfOptions pdfOptions = new PdfOptions();

// Set the VectorRasterizationOptions property
pdfOptions.setVectorRasterizationOptions(rasterizationOptions);
```

Sekarang, kami membuat instance `PdfOptions` dan menetapkan properti `VectorRasterizationOptions`‑nya ke `CadRasterizationOptions` yang telah dikonfigurasi sebelumnya.

## Step 4: Export to PDF (convert cad to pdf)

```java
// Export CAD to PDF
objImage.save(dataDir + "result_out_.pdf", pdfOptions);
```

Akhirnya, kami menyimpan gambar CAD ke file PDF menggunakan opsi yang ditentukan, menyelesaikan proses **convert CAD to PDF**.

## Step 5: Create TiffOptions and Set VectorRasterizationOptions (export cad to tiff)

```java
// Create an instance of TiffOptions
TiffOptions tiffOptions = new TiffOptions(TiffExpectedFormat.Default);

// Set the VectorRasterizationOptions property
tiffOptions.setVectorRasterizationOptions(rasterizationOptions);
```

Dalam langkah ini, kami menyiapkan instance `TiffOptions` dan mengonfigurasi properti `VectorRasterizationOptions`‑nya.

## Step 6: Export to TIFF

```java
// Export CAD to TIFF
objImage.save(dataDir + "result_out_.tiff", tiffOptions);
```

Akhirnya, kami menyimpan gambar CAD ke file TIFF menggunakan opsi yang ditentukan, memperlihatkan cara **export CAD to TIFF** setelah mengonfigurasi ukuran kanvas.

## Common Issues and Solutions

| Issue | Cause | Fix |
|-------|-------|-----|
| Output PDF is blank | `setNoScaling(true)` disables rendering for some drawings | Remove `setNoScaling(true)` or set it to `false`. |
| TIFF resolution looks low | Page width/height too small | Increase `setPageWidth` / `setPageHeight` values. |
| Layout looks distorted | Automatic layout scaling disabled | Ensure `setAutomaticLayoutsScaling(true)` is enabled. |

## Why Adjust Canvas Size and DPI?

Mengubah ukuran kanvas secara langsung memengaruhi resolusi rasterisasi output. Jika Anda perlu **increase TIFF resolution**, cukup tingkatkan nilai `setPageWidth` / `setPageHeight` atau panggil `rasterizationOptions.setResolution(300)` sebelum membuat `TiffOptions`. Ini memberi Anda gambar raster berkualitas tinggi yang cocok untuk cetak atau inspeksi detail.

## Frequently Asked Questions

### Q1: Can I use Aspose.CAD for Java with other Java frameworks?

A1: Yes, Aspose.CAD is designed to seamlessly integrate with various Java frameworks.

### Q2: Is a temporary license available for Aspose.CAD?

A2: Yes, you can obtain a temporary license [here](https://purchase.aspose.com/temporary-license/).

### Q3: Where can I get community support for Aspose.CAD?

A3: Visit the [Aspose.CAD forum](https://forum.aspose.com/c/cad/19) for community support and discussions.

### Q4: Can I try Aspose.CAD for free?

A4: Absolutely! Get a free trial [here](https://releases.aspose.com/).

### Q5: How do you purchase Aspose.CAD for Java?

A5: Purchase the product [here](https://purchase.aspose.com/buy).

**Additional Q&A**

**Q: Does the canvas size affect vector quality in the PDF?**  
A: No. Canvas size controls page dimensions; vector data remains resolution‑independent, ensuring crisp rendering at any zoom level.

**Q: Can I set a different DPI for the TIFF output?**  
A: Yes. Adjust `rasterizationOptions.setResolution(dpiValue)` before creating `TiffOptions`.

**Q: How can I **change PDF dimensions** for an existing PDF without re‑rendering the CAD?**  
A: Use Aspose.PDF to load the generated PDF and call `pdf.getPages().setPageSize(PageSize.A4)` or a custom size.

**Q: What is the best way to **convert dxf to pdf** while preserving layers?**  
A: Keep `setAutomaticLayoutsScaling(true)` and avoid `setNoScaling(true)`; this retains layer visibility and layout fidelity.

## Conclusion

Congratulations! You've successfully **convert CAD to PDF** and **export CAD to TIFF** while **set canvas size java**, enabling **automatic layout scaling**, and learning how to **configure canvas mode** for high‑quality outputs. This tutorial provides a solid foundation for your CAD conversion projects. Explore more features and possibilities in the [Aspose.CAD documentation](https://reference.aspose.com/cad/java/).

---

**Last Updated:** 2026-02-15  
**Tested With:** Aspose.CAD for Java 24.12  
**Author:** Aspose  

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}