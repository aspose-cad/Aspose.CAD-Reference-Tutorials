---
date: 2025-12-28
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

Jika Anda perlu **membuat PDF dari file DWG** sekaligus menyisipkan teks khusus, Anda berada di tempat yang tepat. Pada tutorial ini kami akan membahas seluruh proses—memuat gambar DWG, menambahkan anotasi teks, dan akhirnya menyimpan hasilnya sebagai PDF menggunakan Aspose.CAD untuk Java. Pada akhir tutorial Anda akan memahami cara **menyimpan DWG sebagai PDF**, menyesuaikan tinggi teks, dan bahkan menambahkan anotasi dasar.

## Jawaban Cepat
- **Apakah saya dapat mengonversi DWG ke PDF di Java?** Ya, Aspose.CAD untuk Java menyediakan API yang sederhana.  
- **Apakah saya memerlukan lisensi untuk penggunaan produksi?** Lisensi komersial diperlukan; versi percobaan gratis tersedia.  
- **Metode mana yang menambahkan teks ke DWG?** Gunakan objek `CadText` dan tambahkan ke model space.  
- **Bisakah saya mengatur tinggi teks?** Tentu—gunakan `setTextHeight()` pada instance `CadText`.  
- **Apakah output berbasis vektor?** Ketika opsi rasterisasi diatur ke `UseObjectColor`, PDF mempertahankan data vektor berkualitas tinggi.

## Prasyarat

Sebelum memulai tutorial, pastikan Anda telah menyiapkan prasyarat berikut:

- **Pustaka Aspose.CAD untuk Java:** Unduh dan instal pustaka dari [halaman Aspose.CAD untuk Java](https://releases.aspose.com/cad/java/).

- **Java Development Kit (JDK):** Pastikan Anda memiliki JDK terbaru yang terpasang di sistem Anda.

- **Gambar DWG:** Siapkan file gambar DWG tempat Anda ingin menambahkan teks.

## Impor Namespace

Di dalam kode Java Anda, impor namespace yang diperlukan untuk Aspose.CAD:

```java
import com.aspose.cad.Image;


import com.aspose.cad.fileformats.cad.CadDrawTypeMode;
import com.aspose.cad.fileformats.cad.CadImage;
import com.aspose.cad.fileformats.cad.cadobjects.CadText;
import com.aspose.cad.imageoptions.CadRasterizationOptions;
import com.aspose.cad.imageoptions.PdfOptions;
```

Sekarang, mari kita uraikan potongan kode yang diberikan menjadi beberapa langkah:

## Langkah 1: Siapkan Direktori Dokumen dan Jalur File DWG

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

## Langkah 5: Siapkan Opsi PDF (Persiapkan pembuatan PDF dari DWG)

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

## Langkah 7: Simpan DWG yang Dimodifikasi sebagai PDF (dwg to pdf java)

```java
image.save(dataDir + "SimpleEntites_generated.dwg.pdf", pdfOptions);
```

Dengan mengikuti langkah‑langkah ini, Anda akan dapat **membuat PDF dari DWG**, menambahkan teks khusus, dan mengontrol tinggi teks—semua dengan hanya beberapa baris kode Java.

## Mengapa Menambahkan Teks ke DWG dan Mengonversi ke PDF?

Menambahkan teks langsung ke file DWG berguna untuk:

- **Memberi catatan pada desain** dengan keterangan atau nomor bagian.
- **Membuat dokumentasi yang dapat dicetak** di mana PDF berfungsi sebagai format baca‑saja yang didukung secara luas.
- **Mengotomatiskan pemrosesan batch** pada perpustakaan CAD besar tanpa penyuntingan manual.

## Masalah Umum & Tips

- **Teks tidak muncul?** Pastikan koordinat X/Y berada dalam batas gambar dan layer terlihat.
- **Tinggi teks tidak tepat?** Sesuaikan `setTextHeight()`; nilai tersebut berada dalam sistem satuan gambar.
- **PDF terlihat raster?** Pastikan `CadDrawTypeMode.UseObjectColor` diatur untuk mempertahankan informasi vektor.
- **Kinerja pada file besar?** Tingkatkan `pageHeight`/`pageWidth` hanya bila diperlukan; nilai yang lebih besar akan mengonsumsi lebih banyak memori.

## Pertanyaan yang Sering Diajukan

**T: Apakah Aspose.CAD kompatibel dengan semua versi file DWG?**  
J: Aspose.CAD mendukung berbagai versi file DWG, memastikan kompatibilitas dengan beragam perangkat lunak CAD.

**T: Bisakah saya menyesuaikan font dan format teks yang ditambahkan?**  
J: Ya, Anda dapat menyesuaikan font, gaya, dan opsi format lainnya untuk teks yang ditambahkan ke file DWG menggunakan Aspose.CAD.

**T: Apakah ada versi percobaan gratis untuk Aspose.CAD untuk Java?**  
J: Ya, Anda dapat menjelajahi fitur Aspose.CAD dengan memperoleh versi percobaan gratis [di sini](https://releases.aspose.com/).

**T: Di mana saya dapat menemukan dokumentasi detail untuk Aspose.CAD untuk Java?**  
J: Lihat dokumentasi [di sini](https://reference.aspose.com/cad/java/) untuk informasi mendalam dan contoh.

**T: Bagaimana cara mendapatkan dukungan atau bantuan terkait Aspose.CAD?**  
J: Kunjungi [forum Aspose.CAD](https://forum.aspose.com/c/cad/19) untuk mendapatkan bantuan dan terhubung dengan komunitas.

---

**Terakhir Diperbarui:** 2025-12-28  
**Diuji Dengan:** Aspose.CAD untuk Java 24.12  
**Penulis:** Aspose  

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}