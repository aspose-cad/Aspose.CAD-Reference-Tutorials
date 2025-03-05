---
title: Tambahkan Teks di DWG Menggunakan Aspose.CAD untuk Java
linktitle: Tambahkan Teks di DWG
second_title: Aspose.CAD Java API
description: Sempurnakan gambar DWG Anda dengan mudah dengan Aspose.CAD untuk Java. Tambahkan teks secara lancar dengan panduan langkah demi langkah kami.
type: docs
weight: 10
url: /id/java/cad-text-and-annotation/add-text-in-dwg/
---
## Perkenalan

Di bidang desain berbantuan komputer (CAD), Aspose.CAD untuk Java menonjol sebagai alat yang ampuh untuk memanipulasi dan mengonversi gambar DWG. Salah satu fitur praktisnya adalah kemampuan untuk menambahkan teks ke file DWG dengan mulus. Dalam tutorial ini, kami akan memandu Anda melalui proses menambahkan teks ke gambar DWG Anda menggunakan Aspose.CAD untuk Java.

## Prasyarat

Sebelum masuk ke tutorial, pastikan Anda memiliki prasyarat berikut:

-  Aspose.CAD untuk Java Library: Unduh dan instal perpustakaan dari[Aspose.CAD untuk halaman Java](https://releases.aspose.com/cad/java/).

- Java Development Kit (JDK): Pastikan Anda telah menginstal JDK terbaru di sistem Anda.

- Gambar DWG: Siapkan file gambar DWG tempat Anda ingin menambahkan teks.

## Impor Namespace

Dalam kode Java Anda, impor namespace yang diperlukan untuk Aspose.CAD:

```java
import com.aspose.cad.Image;


import com.aspose.cad.fileformats.cad.CadDrawTypeMode;
import com.aspose.cad.fileformats.cad.CadImage;
import com.aspose.cad.fileformats.cad.cadobjects.CadText;
import com.aspose.cad.imageoptions.CadRasterizationOptions;
import com.aspose.cad.imageoptions.PdfOptions;
```

Sekarang, mari kita uraikan cuplikan kode yang disediakan menjadi beberapa langkah:

## Langkah 1: Siapkan Direktori Dokumen dan Jalur File DWG

```java
String dataDir = "Your Document Directory" + "DWGDrawings/";
String dwgPathToFile = dataDir + "SimpleEntites.dwg";
```

## Langkah 2: Muat Gambar DWG

```java
Image image = Image.load(dwgPathToFile);
```

## Langkah 3: Buat Objek CadText

```java
CadText cadText = new CadText();
cadText.setStyleType("Standard");
cadText.setDefaultValue("Some custom text");
cadText.setColorId(256);
cadText.setLayerName("0");
cadText.getFirstAlignment().setX(47.9);
cadText.getFirstAlignment().setY(5.56);
cadText.setTextHeight(0.8);
cadText.setScaleX(0);
```

## Langkah 4: Tambahkan Teks ke CadImage

```java
CadImage cadImage = ((CadImage)(image));
cadImage.getBlockEntities().get_Item("*Model_Space").addEntity(cadText);
```

## Langkah 5: Atur Opsi PDF

```java
PdfOptions pdfOptions = new PdfOptions();
```

## Langkah 6: Konfigurasikan CadRasterizationOptions

```java
CadRasterizationOptions cadRasterizationOptions = new CadRasterizationOptions();
pdfOptions.setVectorRasterizationOptions(cadRasterizationOptions);
cadRasterizationOptions.setDrawType(CadDrawTypeMode.UseObjectColor);
cadRasterizationOptions.setPageHeight(1600);
cadRasterizationOptions.setPageWidth(1600);
cadRasterizationOptions.setLayouts(new String[] {"Model"});
```

## Langkah 7: Simpan DWG yang Dimodifikasi sebagai PDF

```java
image.save(dataDir + "SimpleEntites_generated.dwg.pdf", pdfOptions);
```

Dengan mengikuti langkah-langkah ini, Anda akan dapat menambahkan teks ke gambar DWG Anda dengan lancar menggunakan Aspose.CAD untuk Java.

## Kesimpulan

Aspose.CAD untuk Java memberdayakan pengembang untuk menyempurnakan dan memodifikasi gambar DWG secara terprogram. Tutorial ini memberikan panduan langkah demi langkah yang jelas untuk menambahkan teks ke file DWG Anda, menampilkan kesederhanaan dan kekuatan Aspose.CAD.

## FAQ

### Q1: Apakah Aspose.CAD kompatibel dengan semua versi file DWG?

A1: Aspose.CAD mendukung berbagai versi file DWG, memastikan kompatibilitas dengan berbagai perangkat lunak CAD.

### Q2: Dapatkah saya menyesuaikan font dan format teks yang ditambahkan?

A2: Ya, Anda dapat menyesuaikan font, gaya, dan opsi pemformatan lainnya untuk teks yang ditambahkan ke file DWG menggunakan Aspose.CAD.

### Q3: Apakah tersedia uji coba gratis untuk Aspose.CAD untuk Java?

 A3: Ya, Anda dapat menjelajahi fitur Aspose.CAD dengan mendapatkan uji coba gratis dari[Di Sini](https://releases.aspose.com/).

### Q4: Di mana saya dapat menemukan dokumentasi terperinci untuk Aspose.CAD untuk Java?

 A4: Lihat dokumentasi[Di Sini](https://reference.aspose.com/cad/java/) untuk informasi mendalam dan contoh.

### Q5: Bagaimana saya bisa mendapatkan dukungan atau mencari bantuan dengan Aspose.CAD?

A5: Kunjungi[Forum Aspose.CAD](https://forum.aspose.com/c/cad/19) untuk mendapatkan bantuan dan berhubungan dengan masyarakat.