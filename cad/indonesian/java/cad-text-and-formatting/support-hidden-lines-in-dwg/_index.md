---
date: 2026-01-02
description: Pelajari cara mengekspor DWG menjadi PDF, mengaktifkan garis tersembunyi,
  dan mengonversi DWG ke PDF dengan Aspose.CAD untuk Java dalam tutorial langkah demi
  langkah ini.
linktitle: Export DWG as PDF with Hidden Lines Using Java
second_title: Aspose.CAD Java API
title: Ekspor DWG sebagai PDF dengan Garis Tersembunyi – Aspose.CAD untuk Java
url: /id/java/cad-text-and-formatting/support-hidden-lines-in-dwg/
weight: 11
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Ekspor DWG ke PDF dengan Garis Tersembunyi – Aspose.CAD untuk Java

## Pendahuluan

Dalam tutorial ini Anda akan belajar cara **mengekspor DWG ke PDF** sambil mempertahankan garis tersembunyi menggunakan Aspose.CAD untuk Java. Apakah Anda perlu **mengonversi DWG ke PDF**, membuat panduan bergaya **tutorial dwg ke pdf**, atau sekadar **menyimpan DWG sebagai PDF** dengan dukungan garis tersembunyi, kami akan memandu Anda melalui setiap langkah. Pada akhir tutorial, Anda akan memiliki solusi siap pakai yang dapat Anda integrasikan ke dalam proyek Java mana pun.

## Jawaban Cepat
- **Apa yang dibahas dalam tutorial ini?** Mengaktifkan rendering garis tersembunyi saat mengekspor DWG ke PDF dengan Aspose.CAD untuk Java.  
- **Operasi utama apa yang dilakukan?** `export dwg as pdf`.  
- **Apakah saya memerlukan lisensi?** Versi percobaan gratis dapat digunakan untuk pengujian; lisensi komersial diperlukan untuk produksi.  
- **Apa saja prasyaratnya?** Lingkungan pengembangan Java, pustaka Aspose.CAD untuk Java, dan file DWG.  
- **Berapa lama waktu implementasinya?** Sekitar 10‑15 menit untuk pengaturan dasar.

## Apa itu “export dwg as pdf”?
Mengekspor file DWG ke PDF mengubah gambar CAD berbasis vektor menjadi format dokumen portabel sambil mempertahankan lapisan, tipe garis, dan rendering garis tersembunyi opsional. Hal ini memudahkan berbagi desain CAD dengan pemangku kepentingan yang mungkin tidak memiliki perangkat lunak CAD.

## Mengapa mengaktifkan garis tersembunyi saat mengekspor?
Garis tersembunyi memberikan representasi visual yang lebih jelas dari model 3D yang kompleks pada halaman 2‑D, memastikan hanya tepi yang terlihat yang ditekankan. Ini meningkatkan keterbacaan dan sering diperlukan untuk dokumentasi teknik.

## Prasyarat

1. **Aspose.CAD untuk Java** – unduh pustaka dari situs resmi [di sini](https://releases.aspose.com/cad/java/).  
2. **File DWG** – pastikan gambar DWG sumber disimpan di direktori yang diketahui.  
3. **Lingkungan pengembangan Java** – JDK 8+ dan IDE pilihan Anda (Eclipse, IntelliJ, dll.).  

Setelah semuanya siap, mari kita selami kode.

## Impor Namespace

Mulailah dengan mengimpor kelas yang diperlukan agar Anda dapat bekerja dengan gambar CAD dan opsi PDF.

```java
import com.aspose.cad.Image;

import com.aspose.cad.fileformats.cad.CadImage;
import com.aspose.cad.imageoptions.CadRasterizationOptions;
import com.aspose.cad.imageoptions.PdfOptions;
import java.util.Arrays;
import java.util.List;
```

## Langkah 1: Siapkan Proyek Anda

Buat proyek Java dan tambahkan JAR Aspose.CAD ke jalur build Anda. Kemudian tentukan direktori yang berisi file DWG Anda.

```java
String dataDir = "Your Document Directory" + "DWGDrawings/";
```

> **Tip Pro:** Gunakan path absolut atau konfigurasikan path relatif berdasarkan folder sumber daya proyek Anda.

## Langkah 2: Muat File DWG

Muat file DWG sumber ke dalam objek `CadImage` sehingga Anda dapat memanipulasinya.

```java
String sourceFilePath = dataDir + "Bottom_plate.dwg";
String outPath = dataDir + "Bottom_plate.pdf";
CadImage cadImage = (CadImage)Image.load(sourceFilePath);
```

## Langkah 3: Konfigurasikan Opsi Rasterisasi

Pilih lapisan yang ingin Anda sertakan dan atur ukuran halaman agar sesuai dengan gambar asli. Di sinilah kami mengaktifkan rendering garis tersembunyi dengan menentukan tata letak.

```java
List<String> list = Arrays.asList("Print","L1_RegMark","L2_RegMark");
CadRasterizationOptions rasterizationOptions = new CadRasterizationOptions();
rasterizationOptions.setPageHeight(cadImage.getHeight());
rasterizationOptions.setPageWidth(cadImage.getWidth()) ;
rasterizationOptions.setLayers(list);
```

## Langkah 4: Atur Opsi PDF

Beritahu Aspose.CAD untuk meraster data vektor menjadi PDF, menggunakan tata letak “Model” untuk menjaga garis tersembunyi tetap tersembunyi.

```java
PdfOptions pdfOptions = new PdfOptions();
rasterizationOptions.setLayouts(new String[] { "Model" });
pdfOptions.setVectorRasterizationOptions(rasterizationOptions);
```

## Langkah 5: Simpan Hasilnya

Akhirnya, ekspor DWG sebagai file PDF. Garis tersembunyi akan dipertahankan sesuai dengan tata letak yang Anda tetapkan.

```java
cadImage.save(outPath, pdfOptions);
System.out.println("\nThe DWG file exported successfully to PDF.\nFile saved at " + dataDir);
```

> **Kesalahan Umum:** Lupa mengatur tata letak ke `"Model"` akan menyebabkan semua garis (termasuk yang tersembunyi) muncul solid dalam PDF.

## Kesimpulan

Anda kini memiliki metode lengkap yang siap produksi untuk **mengekspor DWG ke PDF** dengan dukungan garis tersembunyi menggunakan Aspose.CAD untuk Java. Pendekatan ini dapat diintegrasikan ke dalam alat pemrosesan batch, layanan web, atau aplikasi desktop untuk mengotomatiskan konversi CAD‑ke‑PDF.

## Pertanyaan yang Sering Diajukan

### T1: Bisakah saya menggunakan Aspose.CAD untuk Java dengan format file CAD lainnya?
A1: Ya, Aspose.CAD mendukung berbagai format CAD seperti DWG, DXF, DWF, dan lainnya.

### T2: Apakah ada versi percobaan gratis untuk Aspose.CAD untuk Java?
A2: Ya, Anda dapat menemukan versi percobaan gratis [di sini](https://releases.aspose.com/).

### T3: Bagaimana cara mendapatkan dukungan untuk Aspose.CAD untuk Java?
A3: Kunjungi forum Aspose.CAD [di sini](https://forum.aspose.com/c/cad/19) untuk dukungan komunitas.

### T4: Di mana saya dapat menemukan dokumentasi terperinci untuk Aspose.CAD untuk Java?
A4: Lihat dokumentasi [di sini](https://reference.aspose.com/cad/java/).

### T5: Bisakah saya membeli lisensi sementara untuk Aspose.CAD untuk Java?
A5: Ya, Anda dapat memperoleh lisensi sementara [di sini](https://purchase.aspose.com/temporary-license/).

### T6: Apakah metode ini juga bekerja untuk mengonversi DWG ke PDF di lingkungan server tanpa antarmuka?
A6: Tentu saja. Karena kode hanya menggunakan API Aspose.CAD, ia berjalan tanpa ketergantungan UI apa pun, menjadikannya ideal untuk otomatisasi sisi server.

---

**Terakhir Diperbarui:** 2026-01-02  
**Diuji Dengan:** Aspose.CAD untuk Java 24.12  
**Penulis:** Aspose  

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}