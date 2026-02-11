---
date: 2026-01-10
description: Pelajari cara mengekspor DGN ke DWG dan mengonversi MicroStation DGN
  ke AutoCAD DWG menggunakan Aspose.CAD untuk Java. Panduan langkah demi langkah.
linktitle: Export DGN as Part of DWG
second_title: Aspose.CAD Java API
title: Ekspor DGN ke DWG dengan Aspose.CAD untuk Java
url: /id/java/dgn-export-options/export-dgn-as-part-of-dwg/
weight: 10
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Ekspor DGN ke DWG dengan Aspose.CAD untuk Java

## Pendahuluan

Dalam tutorial ini, Anda akan belajar cara **export dgn to dwg** dan menyematkan desain MicroStation DGN ke dalam file AutoCAD DWG menggunakan pustaka Aspose.CAD untuk Java. Baik Anda memigrasikan gambar MicroStation lama atau perlu menggabungkan underlay DGN dengan layout DWG, panduan ini akan memandu Anda melalui setiap langkah—dari menyiapkan lingkungan hingga menghasilkan pratinjau PDF dari DWG akhir.

## Jawaban Cepat
- **Apa yang dicapai dengan “export dgn to dwg”?** Itu menyematkan underlay DGN ke dalam DWG, memungkinkan tampilan yang mulus di AutoCAD.
- **Format apa yang dapat saya ekspor untuk pratinjau cepat?** Anda dapat **export cad file to pdf** menggunakan `PdfOptions`.
- **Apakah saya memerlukan lisensi untuk menjalankan kode?** Lisensi Aspose.CAD sementara atau berbayar diperlukan untuk penggunaan produksi.
- **Versi Java apa yang didukung?** Java 8 atau yang lebih baru bekerja dengan rilis terbaru Aspose.CAD untuk Java.
- **Apakah tersedia percobaan gratis?** Ya – unduh percobaan dari situs web Aspose.

## Apakah “export dgn to dwg”?

Mengekspor DGN ke DWG berarti mengonversi atau menyematkan desain MicroStation DGN sebagai underlay di dalam gambar AutoCAD DWG. Hal ini memungkinkan profesional CAD memanfaatkan aset DGN yang ada tanpa harus membuat ulang geometri dari awal.

## Kenapa mengonversi MicroStation DGN ke AutoCAD DWG?
- **Kolaborasi:** Tim yang menggunakan AutoCAD dapat melihat dan mengedit konten DGN secara langsung.
- **Standarisasi:** DWG adalah format de‑facto untuk banyak alur kerja hilir (mis., pembuatan PDF, rendering 3D).
- **Preservasi:** Menjaga referensi DGN asli tetap utuh, mengurangi kehilangan data.

## Prasyarat

Sebelum kita masuk ke tutorial, pastikan Anda memiliki prasyarat berikut:

1. **Pustaka Aspose.CAD:** Unduh dan instal pustaka Aspose.CAD untuk Java. Anda dapat menemukan pustaka tersebut [di sini](https://releases.aspose.com/cad/java/).
2. **Java Development Kit (JDK):** Pastikan Anda telah menginstal Java di sistem Anda.
3. **Integrated Development Environment (IDE):** Pilih IDE Java seperti Eclipse atau IntelliJ untuk pengalaman pengembangan yang lebih lancar.

## Impor Paket

Dalam proyek Java Anda, impor paket Aspose.CAD yang diperlukan untuk memungkinkan manipulasi file CAD. Berikut contoh:

```java
import com.aspose.cad;
import com.aspose.cad.imageoptions;
import com.aspose.cad.fileformats.cad.cadconsts;
import com.aspose.cad.fileformats.cad;
import com.aspose.cad.fileformats.cad.cadobjects;
```

## Langkah 1: Atur Jalur File

Tentukan jalur file input dan output untuk file DWG. Perbarui variabel `dataDir`, `fileName`, dan `outPath` sesuai kebutuhan.

```java
String dataDir = "Your Document Directory" + "ExportingDGN/";
String fileName = dataDir + "BlockRefDgn.dwg";
String outPath = dataDir + "BlockRefDgn.dwg.pdf";
```

## Langkah 2: Buat Instance PdfOptions

Buat instance kelas `PdfOptions`, karena kami **mengekspor file CAD ke PDF** untuk verifikasi cepat.

```java
PdfOptions exportOptions = new PdfOptions();
```

## Langkah 3: Muat File DWG

Muat file DWG yang ada sebagai gambar dan konversi ke tipe `CadImage`.

```java
CadImage cadImage = (CadImage) Image.load(fileName);
```

## Langkah 4: Iterasi Melalui Entitas

Lakukan iterasi pada setiap entitas di dalam file DWG dan periksa apakah itu merupakan definisi gambar. Jika ya, ambil referensi eksternal ke objek tersebut.

```java
for (CadBaseEntity baseEntity : cadImage.getEntities()) {
    if (baseEntity.getTypeName() == CadEntityTypeName.DGNUNDERLAY) {
        CadDgnUnderlay dgnFile = (CadDgnUnderlay)baseEntity;
        System.out.println(dgnFile.getUnderlayPath());
    }
}
```

## Langkah 5: Definisikan Opsi Rasterisasi

Definisikan pengaturan untuk objek `CadRasterizationOptions`, termasuk lebar halaman, tinggi, layout, dan warna latar belakang.

```java
CadRasterizationOptions vectorRasterizationOptions = new CadRasterizationOptions();
vectorRasterizationOptions.setPageWidth(1600);
vectorRasterizationOptions.setPageHeight(1600);
vectorRasterizationOptions.setLayouts(new String[] { "Model" });
vectorRasterizationOptions.setAutomaticLayoutsScaling(false);
vectorRasterizationOptions.setNoScaling(true);
vectorRasterizationOptions.setBackgroundColor(Color.getBlack());
vectorRasterizationOptions.setDrawType(CadDrawTypeMode.UseObjectColor);
```

## Langkah 6: Atur Opsi Rasterisasi Vektor

Atur opsi rasterisasi vektor untuk ekspor.

```java
exportOptions.setVectorRasterizationOptions(vectorRasterizationOptions);
```

## Langkah 7: Ekspor DWG ke PDF

Akhirnya, ekspor DWG ke PDF dengan memanggil metode `save`.

```java
cadImage.save(outPath, exportOptions);
```

## Masalah Umum dan Solusinya

| Masalah | Penyebab | Solusi |
|-------|-------|----------|
| **No DGN underlay appears** | The DWG does not contain a `DGNUNDERLAY` entity. | Verify that the source DWG includes a DGN reference. |
| **PDF is blank** | Rasterization options set to zero size or wrong layout. | Ensure `setPageWidth`/`setPageHeight` are positive and `setLayouts` matches the DWG layout name. |
| **License exception** | Running without a valid Aspose.CAD license. | Apply a temporary or purchased license before calling any API methods. |

## Pertanyaan yang Sering Diajukan

### Q1: Di mana saya dapat menemukan dokumentasi untuk Aspose.CAD untuk Java?

A1: Dokumentasi dapat ditemukan [di sini](https://reference.aspose.com/cad/java/).

### Q2: Bagaimana cara mengunduh pustaka Aspose.CAD untuk Java?

A2: Anda dapat mengunduh pustaka tersebut dari [tautan ini](https://releases.aspose.com/cad/java/).

### Q3: Apakah tersedia percobaan gratis untuk Aspose.CAD untuk Java?

A3: Ya, Anda dapat menemukan percobaan gratis [di sini](https://releases.aspose.com/).

### Q4: Di mana saya dapat memperoleh lisensi sementara untuk Aspose.CAD untuk Java?

A4: Dapatkan lisensi sementara [di sini](https://purchase.aspose.com/temporary-license/).

### Q5: Butuh bantuan atau memiliki pertanyaan?

A5: Kunjungi forum dukungan komunitas Aspose.CAD [di sini](https://forum.aspose.com/c/cad/19).

### Q6: Bisakah saya mengonversi PDF yang dihasilkan kembali ke DWG?

A6: PDF adalah pratinjau raster; konversi kembali ke DWG memerlukan alat reverse‑engineering terpisah.

### Q7: Apakah pendekatan ini bekerja dengan format CAD lain seperti DWF atau DXF?

A7: Ya, Aspose.CAD mendukung banyak format; Anda hanya perlu menyesuaikan ekstensi file dan pengaturan rasterisasi sesuai.

---

**Terakhir Diperbarui:** 2026-01-10  
**Diuji Dengan:** Aspose.CAD for Java 24.11  
**Penulis:** Aspose  

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}