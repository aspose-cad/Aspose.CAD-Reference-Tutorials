---
date: 2025-12-10
description: Pelajari cara mengonversi CAD ke PDF menggunakan Aspose.CAD untuk Java
  sambil mengatur ukuran kanvas, skala tata letak otomatis, dan mengekspor ke TIFF.
linktitle: Convert CAD to PDF – Set Canvas Size & Mode
second_title: Aspose.CAD Java API
title: Konversi CAD ke PDF – Atur Ukuran Kanvas & Mode (Java)
url: /id/java/advanced-cad-features/set-canvas-size-and-mode/
weight: 16
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Atur Ukuran Kanvas dan Mode

## Pendahuluan

Apakah Anda ingin **convert CAD to PDF** sambil memiliki kontrol penuh atas ukuran kanvas dan mode rendering? Panduan komprehensif ini memandu Anda melalui langkah‑langkah tepat untuk mengatur ukuran kanvas di Java, mengaktifkan **automatic layout scaling**, dan kemudian mengekspor hasilnya ke format PDF dan TIFF menggunakan Aspose.CAD. Baik Anda sedang menyempurnakan pipeline produksi atau bereksperimen dengan prototipe, Anda akan menemukan instruksi yang jelas dan dapat ditindaklanjuti di sini.

## Jawaban Cepat
- **What does “convert CAD to PDF” mean?** Mengubah gambar CAD (misalnya DXF, DWG) menjadi dokumen PDF yang dapat dilihat di platform apa pun.  
- **Can I also export to TIFF?** Ya—gunakan `TiffOptions` untuk membuat gambar raster resolusi tinggi.  
- **Which option controls canvas size in Java?** `CadRasterizationOptions.setPageWidth/Height`.  
- **What is automatic layout scaling?** Sebuah flag (`setAutomaticLayoutsScaling(true)`) yang mempertahankan proporsi tata letak asli ketika ukuran kanvas berubah.  
- **Do I need a license for Aspose.CAD?** Lisensi sementara atau permanen diperlukan untuk penggunaan produksi.

## Apa itu **convert CAD to PDF**?

Mengonversi CAD ke PDF berarti mengambil gambar teknik berbasis vektor dan merendernya sebagai halaman PDF, mempertahankan garis, lapisan, dan geometri sambil membuat file dapat diakses secara universal.

## Mengapa mengatur ukuran kanvas **java**?

Mengatur ukuran kanvas di Java memungkinkan Anda menentukan resolusi output dan dimensi halaman, memastikan bahwa PDF atau TIFF yang dihasilkan sesuai dengan kebutuhan pencetakan atau tampilan Anda. Ini juga memberi Anda kontrol atas perilaku skala, yang penting untuk gambar berformat besar.

## Prasyarat

Sebelum memulai tutorial, pastikan Anda memiliki prasyarat berikut:

- Aspose.CAD for Java: Pastikan Anda telah menginstal library Aspose.CAD di lingkungan Java Anda. Anda dapat mengunduhnya [di sini](https://releases.aspose.com/cad/java/).
- Document Directory: Siapkan direktori dokumen untuk menyimpan file CAD Anda. Direktori ini akan direferensikan dalam langkah‑langkah tutorial.

Sekarang, mari kita mulai dengan panduan langkah‑demi‑langkah.

## Impor Namespace

Pada langkah ini, kita akan mengimpor namespace yang diperlukan untuk memulai proyek Aspose.CAD Anda.

```java
import java.awt.Image;

import com.aspose.cad.fileformats.tiff.enums.TiffExpectedFormat;
import com.aspose.cad.imageoptions.CadRasterizationOptions;
import com.aspose.cad.imageoptions.PdfOptions;
import com.aspose.cad.imageoptions.TiffOptions;
```

## Langkah 1: Impor Kelas Aspose.CAD

```java
// The path to the resource directory.
String dataDir = "Your Document Directory" + "CADConversion/";

String srcFile = dataDir + "conic_pyramid.dxf";
com.aspose.cad.Image objImage = com.aspose.cad.Image.load(srcFile);
```

Dalam potongan kode ini, kami menyiapkan path ke direktori sumber daya dan memuat file DXF menggunakan kelas `Image` Aspose.CAD.

## Langkah 2: Atur Properti **CadRasterizationOptions** (set canvas size java)

```java
// Create an instance of CadRasterizationOptions and set its various properties
CadRasterizationOptions rasterizationOptions = new CadRasterizationOptions();
rasterizationOptions.setPageWidth(1600);
rasterizationOptions.setPageHeight(1600);

rasterizationOptions.setAutomaticLayoutsScaling(true);
rasterizationOptions.setNoScaling(true);
```

Di sini, kami membuat instance `CadRasterizationOptions` dan mengonfigurasi properti seperti lebar halaman, tinggi halaman, dan **automatic layout scaling**. Ini merupakan inti dari **configure canvas mode** untuk konversi Anda.

## Langkah 3: Buat PdfOptions dan Atur VectorRasterizationOptions

```java
// Create an instance of PdfOptions
PdfOptions pdfOptions = new PdfOptions();

// Set the VectorRasterizationOptions property
pdfOptions.setVectorRasterizationOptions(rasterizationOptions);
```

Sekarang, kami membuat instance `PdfOptions` dan mengatur properti `VectorRasterizationOptions`‑nya ke `CadRasterizationOptions` yang telah dikonfigurasi sebelumnya.

## Langkah 4: Ekspor ke PDF (convert cad to pdf)

```java
// Export CAD to PDF
objImage.save(dataDir + "result_out_.pdf", pdfOptions);
```

Akhirnya, kami menyimpan gambar CAD ke file PDF menggunakan opsi yang ditentukan, menyelesaikan proses **convert CAD to PDF**.

## Langkah 5: Buat TiffOptions dan Atur VectorRasterizationOptions (export cad to tiff)

```java
// Create an instance of TiffOptions
TiffOptions tiffOptions = new TiffOptions(TiffExpectedFormat.Default);

// Set the VectorRasterizationOptions property
tiffOptions.setVectorRasterizationOptions(rasterizationOptions);
```

Pada langkah ini, kami menyiapkan instance `TiffOptions` dan mengonfigurasi properti `VectorRasterizationOptions`‑nya.

## Langkah 6: Ekspor ke TIFF

```java
// Export CAD to TIFF
objImage.save(dataDir + "result_out_.tiff", tiffOptions);
```

Akhirnya, kami menyimpan gambar CAD ke file TIFF menggunakan opsi yang ditentukan, menunjukkan cara **export CAD to TIFF** setelah mengatur ukuran kanvas.

## Masalah Umum dan Solusinya

| Masalah | Penyebab | Solusi |
|---------|----------|--------|
| PDF output kosong | `setNoScaling(true)` menonaktifkan rendering untuk beberapa gambar | Hapus `setNoScaling(true)` atau setel ke `false`. |
| Resolusi TIFF terlihat rendah | Lebar/tinggi halaman terlalu kecil | Tingkatkan nilai `setPageWidth` / `setPageHeight`. |
| Tata letak terlihat terdistorsi | Automatic layout scaling dinonaktifkan | Pastikan `setAutomaticLayoutsScaling(true)` diaktifkan. |

## Kesimpulan

Selamat! Anda telah berhasil **convert CAD to PDF** dan **export CAD to TIFF** sambil **set canvas size java**, mengaktifkan **automatic layout scaling**, dan mempelajari cara **configure canvas mode** untuk output berkualitas tinggi. Tutorial ini memberikan dasar yang kuat untuk proyek konversi CAD Anda. Jelajahi lebih banyak fitur dan kemungkinan di [dokumentasi Aspose.CAD](https://reference.aspose.com/cad/java/).

## FAQ

### Q1: Bisakah saya menggunakan Aspose.CAD untuk Java dengan kerangka kerja Java lainnya?

A1: Ya, Aspose.CAD dirancang untuk terintegrasi secara mulus dengan berbagai kerangka kerja Java.

### Q2: Apakah lisensi sementara tersedia untuk Aspose.CAD?

A2: Ya, Anda dapat memperoleh lisensi sementara [di sini](https://purchase.aspose.com/temporary-license/).

### Q3: Di mana saya dapat mendapatkan dukungan komunitas untuk Aspose.CAD?

A3: Kunjungi [forum Aspose.CAD](https://forum.aspose.com/c/cad/19) untuk dukungan komunitas dan diskusi.

### Q4: Bisakah saya mencoba Aspose.CAD secara gratis?

A4: Tentu saja! Dapatkan percobaan gratis [di sini](https://releases.aspose.com/).

### Q5: Bagaimana cara membeli Aspose.CAD untuk Java?

A5: Beli produk tersebut [di sini](https://purchase.aspose.com/buy).

**Q: Apakah ukuran kanvas memengaruhi kualitas vektor dalam PDF?**  
A: Tidak. Ukuran kanvas mengontrol dimensi halaman; data vektor tetap independen resolusi, memastikan render yang tajam pada tingkat zoom apa pun.

**Q: Bisakah saya mengatur DPI yang berbeda untuk output TIFF?**  
A: Ya. Sesuaikan `rasterizationOptions.setResolution(dpiValue)` sebelum membuat `TiffOptions`.

---

**Last:** 2025-12-10  
**Tested With:** Aspose.CAD for Java 24.12  
**Author:** Aspose  

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}