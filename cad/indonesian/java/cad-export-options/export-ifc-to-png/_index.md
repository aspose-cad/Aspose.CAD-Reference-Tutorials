---
title: Ekspor IFC ke PNG dengan Aspose.CAD untuk Java
linktitle: Ekspor IFC ke PNG
second_title: Aspose.CAD Java API
description: Konversikan IFC ke PNG dengan mudah menggunakan Aspose.CAD untuk Java. Ikuti tutorial langkah demi langkah kami.
weight: 18
url: /id/java/cad-export-options/export-ifc-to-png/
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Ekspor IFC ke PNG dengan Aspose.CAD untuk Java

## Perkenalan

Selamat datang di tutorial langkah demi langkah tentang mengekspor IFC (Kelas Fondasi Industri) ke PNG menggunakan Aspose.CAD untuk Java. Aspose.CAD adalah perpustakaan Java yang kuat yang menyediakan kemampuan luas untuk bekerja dengan file CAD, termasuk format IFC. Dalam tutorial ini, kami akan memandu Anda melalui proses mengonversi file IFC menjadi gambar PNG dengan penjelasan mendetail di setiap langkah.

## Prasyarat

Sebelum kita mulai, pastikan Anda memiliki prasyarat berikut:

-  Perpustakaan Aspose.CAD: Unduh dan instal perpustakaan Aspose.CAD untuk Java dari[tautan unduhan](https://releases.aspose.com/cad/java/).

- Direktori Dokumen: Siapkan direktori di sistem Anda tempat file IFC Anda berada.

## Impor Namespace

Di proyek Java Anda, impor namespace yang diperlukan seperti yang ditunjukkan di bawah ini:

```java
import com.aspose.cad.Image;

import com.aspose.cad.fileformats.ifc.IfcImage;
import com.aspose.cad.imageoptions.CadRasterizationOptions;
import com.aspose.cad.imageoptions.PngOptions;
```

## Langkah 1: Muat File IFC

```java
String dataDir = "Your Document Directory" + "ExportingIFC/";
String fileName = dataDir + "example.ifc";
IfcImage cadImage = (IfcImage)Image.load(fileName);
```

Langkah ini melibatkan memuat file IFC menggunakan Aspose.CAD.

## Langkah 2: Atur Opsi Vektor

```java
CadRasterizationOptions vectorOptions = new CadRasterizationOptions();
vectorOptions.setPageWidth(1500);
vectorOptions.setPageHeight(1500);
```

Konfigurasikan opsi vektor untuk rasterisasi, tentukan lebar dan tinggi halaman.

## Langkah 3: Tetapkan Opsi PNG

```java
PngOptions pngOptions = new PngOptions();
pngOptions.setVectorRasterizationOptions(vectorOptions);
```

Atur opsi PNG, termasuk opsi rasterisasi vektor.

## Langkah 4: Simpan sebagai PNG

```java
String outPath = dataDir + "example.png";
cadImage.save(outPath, pngOptions);
```

Simpan gambar yang diproses dalam format PNG.

## Kesimpulan

Selamat! Anda telah berhasil mengonversi file IFC ke PNG menggunakan Aspose.CAD untuk Java. Tutorial ini memberikan panduan komprehensif, memastikan Anda dapat mengintegrasikan fungsi ini ke dalam proyek Anda dengan lancar.

## FAQ

### Q1: Apakah Aspose.CAD kompatibel dengan semua versi file IFC?

 A1: Aspose.CAD mendukung berbagai versi file IFC. Mengacu kepada[dokumentasi](https://reference.aspose.com/cad/java/) untuk detail kompatibilitas.

### Q2: Dapatkah saya menyesuaikan opsi rasterisasi lebih lanjut?

 A2: Tentu saja! Jelajahi[dokumentasi](https://reference.aspose.com/cad/java/) untuk opsi penyesuaian lanjutan.

### Q3: Apakah ada versi uji coba yang tersedia?

A3: Ya, Anda dapat mengakses versi uji coba gratis[Di Sini](https://releases.aspose.com/).

### Q4: Bagaimana saya bisa mendapatkan lisensi sementara untuk Aspose.CAD?

 A4: Dapatkan lisensi sementara dari[Link ini](https://purchase.aspose.com/temporary-license/).

### Q5: Di mana saya bisa mencari bantuan atau mendiskusikan masalah?

A5: Kunjungi[Forum Aspose.CAD](https://forum.aspose.com/c/cad/19) untuk dukungan masyarakat.

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}
