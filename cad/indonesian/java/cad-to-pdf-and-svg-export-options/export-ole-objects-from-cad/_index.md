---
title: Ekspor Objek OLE dari CAD Menggunakan Aspose.CAD untuk Java
linktitle: Ekspor Objek OLE dari CAD
second_title: Aspose.CAD Java API
description: Buka potensi Aspose.CAD untuk Java. Ekspor objek OLE dari file CAD dengan mudah. Unduh sekarang untuk pengelolaan data CAD yang lancar.
weight: 10
url: /id/java/cad-to-pdf-and-svg-export-options/export-ole-objects-from-cad/
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Ekspor Objek OLE dari CAD Menggunakan Aspose.CAD untuk Java

## Perkenalan

Dalam dunia Computer-Aided Design (CAD) yang dinamis, mengelola dan mengekstraksi objek OLE (Object Linking and Embedding) secara efisien sangatlah penting. Aspose.CAD untuk Java memberikan solusi ampuh untuk mengekspor objek OLE dari file CAD. Panduan langkah demi langkah ini akan memandu Anda melalui prosesnya, memastikan Anda memanfaatkan potensi penuh dari alat ini.

## Prasyarat

Sebelum masuk ke tutorial, pastikan Anda memiliki prasyarat berikut:

- Lingkungan Java: Pastikan Anda telah menyiapkan lingkungan pengembangan Java di mesin Anda.
-  Aspose.CAD untuk Java: Unduh dan instal perpustakaan Aspose.CAD untuk Java. Anda dapat menemukan perpustakaan di[tautan unduhan](https://releases.aspose.com/cad/java/).
- File CAD: Siapkan file CAD yang berisi objek OLE yang ingin Anda ekspor.

## Impor Namespace

Untuk memulai, impor namespace yang diperlukan ke dalam proyek Java Anda. Namespace ini menyediakan kelas dan fungsi penting yang diperlukan untuk bekerja dengan file CAD menggunakan Aspose.CAD.

```java
import com.aspose.cad.Image;

import com.aspose.cad.fileformats.cad.CadImage;
import com.aspose.cad.imageoptions.CadRasterizationOptions;
import com.aspose.cad.imageoptions.PngOptions;
```

Sekarang, mari kita uraikan proses mengekspor objek OLE dari CAD menjadi beberapa langkah:

## Langkah 1: Atur Direktori Dokumen Anda

```java
String dataDir = "Your Document Directory" + "DWGDrawings/";
```

Pastikan untuk mengganti "Direktori Dokumen Anda" dengan jalur ke direktori yang berisi file CAD Anda.

## Langkah 2: Tentukan Nama File CAD

```java
String[] files = new String[] { "D ZD junior D10m H2m.dwg", "ZD - Senior D6m H2m45.dwg" };
```

 Tentukan nama file CAD yang ingin Anda proses di`files` Himpunan.

## Langkah 3: Tetapkan Opsi Ekspor PNG

```java
PngOptions pngOptions = new PngOptions();
CadRasterizationOptions rasterizationOptions = new CadRasterizationOptions();
pngOptions.setVectorRasterizationOptions(rasterizationOptions);
rasterizationOptions.setLayouts(new String[] { "Layout1" });
```

Konfigurasikan opsi ekspor PNG, termasuk rasterisasi vektor dan pengaturan tata letak.

## Langkah 4: Iterasi Melalui File CAD

```java
for(String file : files)
{
    CadImage cadImage = (CadImage)Image.load(dataDir + file);
    cadImage.save(dataDir + file + "_out.png", pngOptions);
}
```

Ulangi setiap file CAD yang ditentukan, muat menggunakan Aspose.CAD, dan simpan objek OLE sebagai gambar PNG.

## Kesimpulan

Dengan langkah sederhana namun ampuh ini, Anda dapat mengekspor objek OLE dari file CAD dengan lancar menggunakan Aspose.CAD untuk Java. Alat serbaguna ini memberdayakan pengembang untuk mengelola data CAD secara efisien, membuka kemungkinan baru dalam pengembangan aplikasi CAD.

## FAQ

### Q1: Apakah Aspose.CAD kompatibel dengan semua format file CAD?

 A1: Aspose.CAD mendukung berbagai format CAD, termasuk DWG, DXF, dan DGN. Mengacu kepada[dokumentasi](https://reference.aspose.com/cad/java/) untuk daftar lengkapnya.

### Q2: Dapatkah saya menyesuaikan pengaturan ekspor untuk objek OLE?

A2: Ya, Aspose.CAD menyediakan opsi ekstensif untuk menyesuaikan pengaturan ekspor, memungkinkan Anda menyesuaikan output dengan kebutuhan spesifik Anda.

### Q3: Apakah ada uji coba gratis yang tersedia untuk Aspose.CAD?

 A3: Ya, Anda dapat mengeksplorasi kemampuan Aspose.CAD dengan mendapatkan uji coba gratis dari[Di Sini](https://releases.aspose.com/).

### Q4: Di mana saya bisa mendapatkan dukungan komunitas untuk Aspose.CAD?

 A4: Bergabunglah dengan komunitas Aspose.CAD di[forum](https://forum.aspose.com/c/cad/19) untuk mencari bantuan dan berbagi pengalaman Anda.

### Q5: Bagaimana cara membeli lisensi untuk Aspose.CAD?

A5: Kunjungi[halaman pembelian](https://purchase.aspose.com/buy) untuk mendapatkan lisensi yang sesuai dengan kebutuhan pengembangan Anda.
{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}
