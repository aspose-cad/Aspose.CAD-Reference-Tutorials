---
date: 2026-01-10
description: Pelajari cara membaca file DWG dan membuat entitas multileader DWG menggunakan
  Aspose.CAD untuk Java dalam tutorial langkah demi langkah ini.
linktitle: Support MLeader Entity for DWG Format with Java
second_title: Aspose.CAD Java API
title: Cara Membaca DWG dan Mendukung MLeader dengan Aspose.CAD untuk Java
url: /id/java/cad-text-and-formatting/support-mleader-entity/
weight: 12
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Cara Membaca DWG dan Mendukung MLeader dengan Aspose.CAD untuk Java

## Introduction

Jika Anda perlu **membaca file DWG** dan bekerja dengan **multileader DWG** dalam aplikasi Java, Anda berada di tempat yang tepat. Aspose.CAD untuk Java memberikan cara yang bersih dan programatis untuk membuka gambar DWG, memeriksa objek MLeader, dan memvalidasi properti mereka—semua tanpa memerlukan workstation CAD lengkap. Dalam tutorial ini kami akan membahas setiap langkah, mulai dari memuat file DWG hingga memastikan data multileader sesuai dengan gaya yang diharapkan.

## Quick Answers
- **Apa yang dimaksud dengan “cara membaca dwg”?** Memuat DWG dengan `Image.load()` dan melakukan casting ke `CadImage`.
- **Apakah saya dapat membuat entitas dwg multileader?** Ya – Anda dapat menambah, mengedit, dan memvalidasi objek MLeader menggunakan API CadMLeader.
- **Versi perpustakaan mana yang diperlukan?** Semua rilis Aspose.CAD untuk Java terbaru (API yang ditunjukkan bekerja dengan build 2024+).
- **Apakah saya memerlukan lisensi untuk pengembangan?** Lisensi sementara cukup untuk pengujian; lisensi penuh diperlukan untuk produksi.
- **Apakah kode ini lintas‑platform?** Tentu – Java berjalan di Windows, Linux, dan macOS.

## What is “how to read dwg” with Aspose.CAD?

Membaca file DWG berarti mengonversi gambar biner menjadi objek `CadImage` di memori. Setelah Anda memiliki objek tersebut, Anda dapat mengenumerasi entitasnya (garis, lingkaran, teks, objek **MLeader**, dll.) dan memeriksa propertinya.

## Why support MLeader entities?

Objek MLeader (multileader) menggabungkan garis pemimpin dengan teks atau blok yang terlampir, menjadikannya penting untuk anotasi dalam gambar teknik. Mendukungnya memungkinkan Anda:

- Memverifikasi bahwa anotasi sesuai dengan standar perusahaan.
- Mengekstrak teks untuk pemrosesan lanjutan (mis., pembuatan BOM).
- Memodifikasi gaya pemimpin secara programatis atau mengganti konten blok.

## Prerequisites

Sebelum kita mulai, pastikan Anda memiliki:

1. **Lingkungan Pengembangan Java** – JDK 11+ dan IDE favorit Anda (IntelliJ, Eclipse, VS Code).  
2. **Aspose.CAD untuk Java** – Unduh JAR terbaru dari [tautan unduhan](https://releases.aspose.com/cad/java/).  

## Import Namespaces

Tambahkan impor berikut ke kelas Java Anda sehingga Anda dapat bekerja dengan entitas DWG dan opsi rasterisasi:

```java
import com.aspose.cad.Image;

import com.aspose.cad.fileformats.cad.CadImage;
import com.aspose.cad.fileformats.cad.cadobjects.CadMLeader;
import com.aspose.cad.fileformats.cad.cadobjects.CadMLeaderContextData;
import com.aspose.cad.fileformats.cad.cadobjects.CadMLeaderLine;
import com.aspose.cad.fileformats.cad.cadobjects.CadMLeaderNode;
import com.aspose.cad.imageoptions.CadRasterizationOptions;
import com.aspose.cad.imageoptions.PdfOptions;
```

## How to Read DWG Files Using Aspose.CAD for Java

### Langkah 1: Muat file DWG dan dapatkan `CadImage`

```java
String dataDir = "Your Document Directory" + "DWGDrawings/";
String file = dataDir + "Multileaders.dwg";
Image image = Image.load(file);
CadImage cadImage = (CadImage) image;
```

### Langkah 2: Validasi bahwa gambar berisi entitas MLeader

```java
Assert.areNotEqual(cadImage.getEntities().length, 0);
CadMLeader cadMLeader = (CadMLeader) cadImage.getEntities()[2];
```

### Langkah 3: Verifikasi gaya MLeader dan atribut dasar

```java
Assert.areEqual(cadMLeader.getStyleDescription(), "Standard");
Assert.areEqual(cadMLeader.getLeaderStyleId(), "12E");
Assert.areEqual(cadMLeader.getArrowHeadId1(), "639");
Assert.areEqual(cadMLeader.getLeaderLineTypeID(), "14");
```

### Langkah 4: Akses data konteks MLeader (inti dari multileader)

```java
CadMLeaderContextData context = cadMLeader.getContextData();
```

### Langkah 5: Validasi atribut tingkat konteks

```java
Assert.areEqual(context.getArrowHeadSize(), 30.0, 0.1);
Assert.areEqual(context.getBasePoint().getX(), 481, 1);
Assert.areEqual(context.getContentScale(), 1.0, 0.01);
Assert.areEqual(context.getDefaultText().getValue(),
    "This is multileader with huge text\\P{\\H1.5x;6666666666666666666666666666\\P}bbbbbbbbbbbbbbbbbbbbbbbbbbbbbbbbbbb");
Assert.areEqual(context.hasMText(), true);
```

### Langkah 6: Bekerja dengan node MLeader dan garis pemimpinnya

```java
CadMLeaderNode mleaderNode = context.getLeaderNode();
Assert.areEqual(mleaderNode.getLastLeaderLinePoint().getX(), 473, 1);

CadMLeaderLine leaderLine = mleaderNode.getLeaderLine();
Assert.areEqual(leaderLine.getBreakEndPoint().toString(), null);
Assert.areEqual(Integer.toString(leaderLine.getBreakPointIndex().getValue()), Integer.toString(0));
Assert.areEqual(leaderLine.getBreakStartPoint().toString(), null);
Assert.areEqual(Integer.toString(leaderLine.getLeaderLineIndex().getValue()), Integer.toString(0));
Assert.areEqual(Integer.toString(leaderLine.getLeaderPoints().size()), Integer.toString(4));
```

### Langkah 7: Validasi atribut tambahan node MLeader

```java
Assert.areEqual(Integer.toString(mleaderNode.getBranchIndex()), Integer.toString(0));
Assert.areEqual(mleaderNode.getDogLegLength(), 8.0, 0.1);
Assert.areEqual(context.hasMText(), true);
```

### Langkah 8: Periksa properti terkait teks

```java
Assert.areEqual(context.getTextAttachmentType().getValue(), (short) 1);
Assert.areEqual(context.getTextBackgroundColor().getValue(), 18);
Assert.areEqual(context.getTextHeight(), 20.0, 0.1);
Assert.areEqual(context.getTextStyleID().getValue(), "11");
Assert.areEqual(context.getTextRotation().getValue(), 0.0, 0.01);
```

### Langkah 9: Tinjau atribut MLeader lainnya untuk kelengkapan

```java
Assert.areEqual(cadMLeader.getArrowHeadId1(), "639");
Assert.areEqual(cadMLeader.getLeaderType(), 1);
Assert.areEqual(cadMLeader.getBlockContentColor(), 0);
Assert.areEqual(cadMLeader.getLeaderLineColor(), 0);
Assert.areEqual(cadMLeader.getTextHeight(), 1.0, 0.01);
```

## Common Issues and Solutions

| Masalah | Mengapa Terjadi | Solusi |
|---------|----------------|--------|
| `ClassCastException` saat casting entitas | Indeks yang dipilih bukan objek MLeader. | Verifikasi `cadImage.getEntities()[i] instanceof CadMLeader` sebelum melakukan casting. |
| `null` values untuk titik garis pemimpin | Gambar menggunakan gaya pemimpin khusus yang tidak sepenuhnya didukung. | Gunakan versi Aspose.CAD terbaru atau kembali ke gaya default untuk pengujian. |
| Kegagalan asersi pada nilai numerik | Perbedaan pembulatan kecil antara versi CAD. | Sesuaikan toleransi dalam `Assert.areEqual(..., delta)` seperti yang ditunjukkan pada contoh. |

## Frequently Asked Questions

**T: Apakah saya dapat menggunakan Aspose.CAD untuk Java dengan format CAD lain?**  
J: Ya, Aspose.CAD mendukung DXF, DWF, DGN, dan beberapa format raster selain DWG.

**T: Di mana saya dapat menemukan dokumentasi terperinci untuk Aspose.CAD untuk Java?**  
J: Lihat [dokumentasi](https://reference.aspose.com/cad/java/) resmi untuk detail API dan contoh kode.

**T: Apakah tersedia percobaan gratis?**  
J: Tentu – Anda dapat mengunduh percobaan dari halaman [free trial](https://releases.aspose.com/).

**T: Bagaimana cara mendapatkan lisensi sementara untuk pengujian?**  
J: Dapatkan lisensi sementara melalui [tautan lisensi sementara](https://purchase.aspose.com/temporary-license/).

**T: Di mana saya dapat menanyakan bantuan kepada komunitas?**  
J: [Forum Aspose.CAD](https://forum.aspose.com/c/cad/19) adalah tempat terbaik untuk berbagi pertanyaan dan solusi.

## Conclusion

Anda sekarang memiliki panduan lengkap end‑to‑end untuk **cara membaca DWG** dan **membuat entitas DWG multileader** menggunakan Aspose.CAD untuk Java. Dengan mengikuti langkah‑langkah di atas, Anda dapat memvalidasi gaya MLeader, mengekstrak data anotasi, dan mengintegrasikan pemrosesan DWG ke dalam alur kerja berbasis Java apa pun.

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}

---

**Terakhir Diperbarui:** 2026-01-10  
**Diuji Dengan:** Aspose.CAD 24.11 untuk Java  
**Penulis:** Aspose