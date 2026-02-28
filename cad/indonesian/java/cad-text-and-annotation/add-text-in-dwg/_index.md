---
date: 2026-02-28
description: Pelajari cara membuat PDF dari DWG, menyimpan DWG sebagai PDF, dan menambahkan
  teks ke gambar DWG dengan Aspose.CAD untuk Java—panduan langkah demi langkah.
linktitle: Add Text in DWG
second_title: Aspose.CAD Java API
title: Buat PDF dari DWG dan Tambahkan Teks Menggunakan Aspose.CAD untuk Java
url: /id/java/cad-text-and-annotation/add-text-in-dwg/
weight: 10
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Buat PDF dari DWG dan Tambahkan Teks Menggunakan Aspose.CAD untuk Java

## Pendahuluan

Jika Anda perlu **membuat PDF dari DWG** sambil juga menyisipkan teks khusus, Anda berada di tempat yang tepat. Dalam tutorial ini kami akan membahas seluruh proses—memuat gambar DWG, menambahkan anotasi teks, dan akhirnya menyimpan hasilnya sebagai PDF menggunakan Aspose.CAD untuk Java. Pada akhir tutorial Anda akan memahami cara **menyimpan DWG sebagai PDF**, menyesuaikan tinggi teks, dan bahkan menambahkan anotasi dasar.

## Jawaban Cepat
- **Apakah saya dapat mengonversi DWG ke PDF di Java?** Ya, Aspose.CAD untuk Java menyediakan API yang sederhana.  
- **Apakah saya memerlukan lisensi untuk penggunaan produksi?** Lisensi komersial diperlukan; versi percobaan gratis tersedia.  
- **Metode mana yang menambahkan teks ke DWG?** Gunakan objek `CadText` dan tambahkan ke model space.  
- **Bisakah saya mengatur tinggi teks?** Tentu—gunakan `setTextHeight()` pada instance `CadText`.  
- **Apakah output berbasis vektor?** Ketika opsi rasterisasi diatur ke `UseObjectColor`, PDF mempertahankan data vektor berkualitas tinggi.

## Apa itu “create PDF from DWG”?
Membuat PDF dari gambar DWG berarti mengonversi format CAD asli menjadi dokumen yang dapat dibaca secara luas dan hanya‑baca sambil mempertahankan geometri aslinya. Konversi ini penting ketika Anda perlu berbagi desain dengan pemangku kepentingan yang tidak memiliki perangkat lunak CAD.

## Mengapa menggunakan Aspose.CAD untuk Java untuk mengonversi DWG ke PDF?
Aspose.CAD menawarkan solusi murni‑Java yang tidak memerlukan instalasi CAD eksternal. Ia mendukung **convert DWG to PDF**, mempertahankan fidelitas vektor, dan memungkinkan Anda menambahkan anotasi secara programatis seperti teks, dimensi, atau grafik khusus sebelum konversi.

## Prasyarat

Sebelum memulai tutorial, pastikan Anda memiliki prasyarat berikut:

- Perpustakaan Aspose.CAD untuk Java: Unduh dan instal perpustakaan dari [halaman Aspose.CAD untuk Java](https://releases.aspose.com/cad/java/).

- Java Development Kit (JDK): Pastikan Anda memiliki JDK terbaru terinstal di sistem Anda.

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

Sekarang, mari uraikan potongan kode yang diberikan menjadi beberapa langkah:

## Langkah 1: Siapkan Direktori Dokumen dan Path File DWG

```java
String dataDir = "Your Document Directory" + "DWGDrawings/";
String dwgPathToFile = dataDir + "SimpleEntites.dwg";
```

## Langkah 2: Muat Gambar DWG

```java
Image image = Image.load(dwgPathToFile);
```

## Langkah 3: Buat Objek CadText (Tambahkan Teks ke DWG)

```java
CadText cadText = new CadText();
cadText.setStyleType("Standard");
cadText.setDefaultValue("Some custom text");
cadText.setColorId(256);
cadText.setLayerName("0");
cadText.getFirstAlignment().setX(47.9);
cadText.getFirstAlignment().setY(5.56);
cadText.setTextHeight(0.8);          // set text height in DWG units
cadText.setScaleX(0);
```

## Langkah 4: Tambahkan Teks ke CadImage (Sisipkan Anotasi)

```java
CadImage cadImage = ((CadImage)(image));
cadImage.getBlockEntities().get_Item("*Model_Space").addEntity(cadText);
```

## Langkah 5: Siapkan Opsi PDF (Persiapkan untuk membuat PDF dari DWG)

```java
PdfOptions pdfOptions = new PdfOptions();
```

## Langkah 6: Konfigurasikan CadRasterizationOptions (Kontrol Rendering PDF)

```java
CadRasterizationOptions cadRasterizationOptions = new CadRasterizationOptions();
pdfOptions.setVectorRasterizationOptions(cadRasterizationOptions);
cadRasterizationOptions.setDrawType(CadDrawTypeMode.UseObjectColor);
cadRasterizationOptions.setPageHeight(1600);
cadRasterizationOptions.setPageWidth(1600);
cadRasterizationOptions.setLayouts(new String[] {"Model"});
```

## Langkah 7: Simpan DWG yang Dimodifikasi sebagai PDF (dwg ke pdf java)

```java
image.save(dataDir + "SimpleEntites_generated.dwg.pdf", pdfOptions);
```

Dengan mengikuti langkah‑langkah ini, Anda akan dapat **membuat PDF dari DWG**, menambahkan teks khusus, dan mengontrol tinggi teks—semua dengan hanya beberapa baris kode Java.

## Bagaimana cara mengonversi DWG ke PDF di Java secara skala besar?
Jika Anda perlu **mengonversi batch file DWG ke PDF**, bungkus kode di atas dalam loop yang mengiterasi folder berisi gambar DWG. Sesuaikan `pageHeight`/`pageWidth` hanya bila diperlukan untuk menjaga penggunaan memori tetap rendah, dan gunakan kembali instance `PdfOptions` yang sama untuk setiap file guna meningkatkan kinerja.

## Masalah Umum & Tips

- **Teks tidak muncul?** Verifikasi koordinat X/Y berada dalam batas gambar dan lapisan terlihat.  
- **Tinggi teks tidak tepat?** Sesuaikan `setTextHeight()`; nilai berada dalam sistem satuan gambar.  
- **PDF terlihat raster?** Pastikan `CadDrawTypeMode.UseObjectColor` diatur untuk mempertahankan informasi vektor.  
- **Kinerja pada file besar?** Tingkatkan `pageHeight`/`pageWidth` hanya bila diperlukan; nilai lebih besar mengonsumsi lebih banyak memori.

## Pertanyaan yang Sering Diajukan

**Q: Apakah Aspose.CAD kompatibel dengan semua versi file DWG?**  
A: Aspose.CAD mendukung berbagai versi file DWG, memastikan kompatibilitas dengan beragam perangkat lunak CAD.

**Q: Bisakah saya menyesuaikan font dan format teks yang ditambahkan?**  
A: Ya, Anda dapat menyesuaikan font, gaya, dan opsi format lainnya untuk teks yang ditambahkan ke file DWG menggunakan Aspose.CAD.

**Q: Apakah ada versi percobaan gratis untuk Aspose.CAD untuk Java?**  
A: Ya, Anda dapat menjelajahi fitur Aspose.CAD dengan mendapatkan versi percobaan gratis dari [sini](https://releases.aspose.com/).

**Q: Di mana saya dapat menemukan dokumentasi terperinci untuk Aspose.CAD untuk Java?**  
A: Lihat dokumentasi [sini](https://reference.aspose.com/cad/java/) untuk informasi mendalam dan contoh.

**Q: Bagaimana saya dapat mendapatkan dukungan atau bantuan terkait Aspose.CAD?**  
A: Kunjungi [forum Aspose.CAD](https://forum.aspose.com/c/cad/19) untuk mendapatkan bantuan dan terhubung dengan komunitas.

---

**Terakhir Diperbarui:** 2026-02-28  
**Diuji Dengan:** Aspose.CAD untuk Java 24.12  
**Penulis:** Aspose  

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}