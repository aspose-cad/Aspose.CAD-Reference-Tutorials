---
title: Mendukung Entitas MLeader untuk Format DWG dengan Aspose.CAD untuk Java
linktitle: Mendukung Entitas MLeader untuk Format DWG dengan Java
second_title: Aspose.CAD Java API
description: Buka kekuatan Aspose.CAD untuk Java dengan tutorial langkah demi langkah kami tentang mendukung entitas MLeader dalam format DWG.
weight: 12
url: /id/java/cad-text-and-formatting/support-mleader-entity/
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Mendukung Entitas MLeader untuk Format DWG dengan Aspose.CAD untuk Java

## Perkenalan

Di bidang desain berbantuan komputer (CAD) dengan Java, memahami dan menerapkan dukungan untuk entitas MLeader dalam format DWG adalah keterampilan yang berharga. Aspose.CAD untuk Java memberikan solusi tangguh untuk tugas-tugas tersebut, menawarkan serangkaian alat dan fungsi canggih. Tutorial ini akan memandu Anda melalui proses mendukung entitas MLeader dalam file DWG menggunakan Java dengan Aspose.CAD.

## Prasyarat

Sebelum kita mempelajari tutorialnya, pastikan Anda memiliki prasyarat berikut:

1. Lingkungan Pengembangan Java: Pastikan Anda telah menyiapkan lingkungan pengembangan Java di sistem Anda.

2.  Perpustakaan Aspose.CAD: Unduh dan instal perpustakaan Aspose.CAD untuk Java dari[tautan unduhan](https://releases.aspose.com/cad/java/).

## Impor Namespace

Dalam proyek Java Anda, impor namespace yang diperlukan untuk memanfaatkan kemampuan Aspose.CAD secara efektif. Sertakan baris berikut dalam kode Anda:

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

Sekarang, mari kita pecahkan kodenya menjadi panduan langkah demi langkah untuk mendukung entitas MLeader untuk format DWG menggunakan Java dengan Aspose.CAD.

## 1. Muat File DWG dan Akses CadImage

```java
String dataDir = "Your Document Directory" + "DWGDrawings/";
String file = dataDir + "Multileaders.dwg";
Image image = Image.load(file);
CadImage cadImage = (CadImage) image;
```

## 2. Validasi Entitas MLeader

```java
Assert.areNotEqual(cadImage.getEntities().length, 0);
CadMLeader cadMLeader = (CadMLeader) cadImage.getEntities()[2];
```

### 3. Verifikasi Gaya dan Atribut MLeader

```java
Assert.areEqual(cadMLeader.getStyleDescription(), "Standard");
Assert.areEqual(cadMLeader.getLeaderStyleId(), "12E");
Assert.areEqual(cadMLeader.getArrowHeadId1(), "639");
Assert.areEqual(cadMLeader.getLeaderLineTypeID(), "14");
```

## 4. Akses Data Konteks MLeader

```java
CadMLeaderContextData context = cadMLeader.getContextData();
```

## 5. Validasi Atribut Konteks

```java
Assert.areEqual(context.getArrowHeadSize(), 30.0, 0.1);
Assert.areEqual(context.getBasePoint().getX(), 481, 1);
Assert.areEqual(context.getContentScale(), 1.0, 0.01);
Assert.areEqual(context.getDefaultText().getValue(), "This is multileader with huge text\\P{\\H1.5x;6666666666666666666666666666\\P}bbbbbbbbbbbbbbbbbbbbbbbbbbbbbbbbbbb");
Assert.areEqual(context.hasMText(), true);
```

## 6. Akses Node MLeader dan Garis Pemimpin

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

## 7. Validasi Atribut MLeader Tambahan

```java
Assert.areEqual(Integer.toString(mleaderNode.getBranchIndex()), Integer.toString(0));
Assert.areEqual(mleaderNode.getDogLegLength(), 8.0, 0.1);
Assert.areEqual(context.hasMText(), true);
```

## 8. Validasi Atribut Teks

```java
Assert.areEqual(context.getTextAttachmentType().getValue(), (short) 1);
Assert.areEqual(context.getTextBackgroundColor().getValue(), 18);
Assert.areEqual(context.getTextHeight(), 20.0, 0.1);
Assert.areEqual(context.getTextStyleID().getValue(), "11");
Assert.areEqual(context.getTextRotation().getValue(), 0.0, 0.01);
```

## 9. Atribut MLeader Tambahan

```java
Assert.areEqual(cadMLeader.getArrowHeadId1(), "639");
Assert.areEqual(cadMLeader.getLeaderType(), 1);
Assert.areEqual(cadMLeader.getBlockContentColor(), 0);
Assert.areEqual(cadMLeader.getLeaderLineColor(), 0);
Assert.areEqual(cadMLeader.getTextHeight(), 1.0, 0.01);
```

## Kesimpulan

Selamat! Anda telah berhasil menavigasi panduan komprehensif tentang mendukung entitas MLeader untuk format DWG menggunakan Java dan Aspose.CAD. Kemampuan ini membuka pintu bagi manipulasi CAD tingkat lanjut dan menyempurnakan perangkat pengembangan Java Anda.

## FAQ

### Q1: Dapatkah saya menggunakan Aspose.CAD untuk Java dengan format CAD lainnya?

A1: Ya, Aspose.CAD mendukung berbagai format CAD selain DWG, memberikan fleksibilitas dalam proyek Anda.

### Q2: Di mana saya dapat menemukan dokumentasi terperinci untuk Aspose.CAD untuk Java?

 A2: Lihat[dokumentasi](https://reference.aspose.com/cad/java/) untuk wawasan mendalam tentang kemampuan Aspose.CAD.

### Q3: Apakah tersedia uji coba gratis?

 A3: Ya, jelajahi fungsinya secara langsung dengan[uji coba gratis](https://releases.aspose.com/).

### Q4: Bagaimana saya bisa mendapatkan lisensi sementara untuk Aspose.CAD?

A4: Dapatkan lisensi sementara melalui[Link ini](https://purchase.aspose.com/temporary-license/).

### Q5: Di mana saya dapat mencari dukungan dan bantuan komunitas?

A5: Kunjungi[Forum Aspose.CAD](https://forum.aspose.com/c/cad/19) untuk terhubung dengan komunitas dan mendapatkan bantuan.
{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}
