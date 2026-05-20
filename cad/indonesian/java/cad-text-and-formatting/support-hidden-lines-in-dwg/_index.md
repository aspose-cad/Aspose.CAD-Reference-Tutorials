---
date: 2026-03-05
description: Pelajari cara mengekspor DWG ke PDF, mengaktifkan garis tersembunyi,
  dan mengonversi DWG ke PDF dengan Aspose.CAD untuk Java dalam tutorial langkah demi
  langkah ini.
linktitle: Export DWG as PDF Using Java
second_title: Aspose.CAD Java API
title: Ekspor DWG ke PDF dengan Garis Tersembunyi – Aspose.CAD untuk Java
url: /id/java/cad-text-and-formatting/support-hidden-lines-in-dwg/
weight: 11
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Ekspor DWG ke PDF dengan Garis Tersembunyi – Aspose.CAD untuk Java

## Pendahuluan

Dalam tutorial ini Anda akan belajar cara **export dwg to pdf** sambil mempertahankan garis tersembunyi menggunakan Aspose.CAD untuk Java. Baik Anda perlu **convert DWG to PDF**, membuat panduan bergaya **dwg to pdf tutorial**, atau sekadar **save DWG as PDF** dengan dukungan garis tersembunyi, kami akan memandu Anda melalui setiap langkah. Pada akhir tutorial, Anda akan memiliki solusi siap pakai yang dapat Anda masukkan ke dalam proyek Java apa pun.

## Jawaban Cepat
- **Apa yang dibahas dalam tutorial ini?** Mengaktifkan rendering garis tersembunyi saat mengekspor DWG ke PDF dengan Aspose.CAD untuk Java.  
- **Operasi utama apa yang dilakukan?** `export dwg to pdf`.  
- **Apakah saya memerlukan lisensi?** Versi percobaan gratis cukup untuk pengujian; lisensi komersial diperlukan untuk produksi.  
- **Apa saja prasyaratnya?** Lingkungan pengembangan Java, pustaka Aspose.CAD untuk Java, dan file DWG.  
- **Berapa lama implementasinya?** Sekitar 10‑15 menit untuk pengaturan dasar.

## Apa itu “export dwg to pdf”?
Mengekspor file DWG ke PDF mengubah gambar CAD berbasis vektor menjadi format dokumen portabel sambil mempertahankan lapisan, tipe garis, dan opsi rendering garis tersembunyi. Hal ini memudahkan berbagi desain CAD dengan pemangku kepentingan yang mungkin tidak memiliki perangkat lunak CAD.

## Cara Mengaktifkan Garis Tersembunyi Saat Mengekspor DWG ke PDF
Garis tersembunyi dikontrol melalui pengaturan layout dalam opsi rasterisasi. Dengan memilih layout **Model**, Aspose.CAD memberi tahu renderer untuk memperlakukan tepi tersembunyi sebagai tidak terlihat, menghasilkan representasi 2‑D bersih dari model 3‑D.

## Mengapa mengaktifkan garis tersembunyi saat mengekspor?
Garis tersembunyi memberikan representasi visual yang lebih jelas dari model 3‑D yang kompleks pada halaman 2‑D, memastikan hanya tepi yang terlihat yang ditekankan. Ini meningkatkan keterbacaan dan sering diperlukan untuk dokumentasi teknik.

## Prasyarat

1. **Aspose.CAD untuk Java** – unduh pustaka dari situs resmi [di sini](https://releases.aspose.com/cad/java/).  
2. **File DWG** – miliki gambar DWG sumber yang disimpan di direktori yang diketahui.  
3. **Lingkungan pengembangan Java** – JDK 8+ dan IDE pilihan Anda (Eclipse, IntelliJ, dll.).  

Setelah semuanya siap, mari kita masuk ke kode.

## Import Namespaces

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

> **Pro tip:** Gunakan path absolut atau konfigurasikan path relatif berdasarkan folder sumber daya proyek Anda.

## Langkah 2: Muat File DWG

Muat file DWG sumber ke dalam objek `CadImage` sehingga Anda dapat memanipulasinya.

```java
String sourceFilePath = dataDir + "Bottom_plate.dwg";
String outPath = dataDir + "Bottom_plate.pdf";
CadImage cadImage = (CadImage)Image.load(sourceFilePath);
```

## Langkah 3: Konfigurasikan Opsi Rasterisasi

Pilih lapisan yang ingin Anda sertakan dan atur ukuran halaman agar sesuai dengan gambar asli. Di sinilah kita mengaktifkan rendering garis tersembunyi dengan menentukan layout.

```java
List<String> list = Arrays.asList("Print","L1_RegMark","L2_RegMark");
CadRasterizationOptions rasterizationOptions = new CadRasterizationOptions();
rasterizationOptions.setPageHeight(cadImage.getHeight());
rasterizationOptions.setPageWidth(cadImage.getWidth()) ;
rasterizationOptions.setLayers(list);
```

## Langkah 4: Atur Opsi PDF

Beritahu Aspose.CAD untuk meraster data vektor menjadi PDF, menggunakan layout “Model” agar garis tersembunyi tetap tersembunyi.

```java
PdfOptions pdfOptions = new PdfOptions();
rasterizationOptions.setLayouts(new String[] { "Model" });
pdfOptions.setVectorRasterizationOptions(rasterizationOptions);
```

## Langkah 5: Simpan Hasilnya

Akhirnya, ekspor DWG sebagai file PDF. Garis tersembunyi akan dihormati sesuai dengan layout yang Anda tetapkan.

```java
cadImage.save(outPath, pdfOptions);
System.out.println("\nThe DWG file exported successfully to PDF.\nFile saved at " + dataDir);
```

> **Common Pitfall:** Lupa mengatur layout ke `"Model"` akan menyebabkan semua garis (termasuk yang tersembunyi) muncul solid dalam PDF.

## Masalah Umum dan Solusinya

| Masalah | Mengapa Terjadi | Cara Memperbaiki |
|---------|-----------------|------------------|
| PDF menampilkan semua garis solid | Layout tidak diatur ke **Model** | Pastikan `rasterizationOptions.setLayouts(new String[] { "Model" });` dipanggil sebelum menyimpan. |
| Lapisan hilang dalam output | Nama lapisan tidak tepat | Verifikasi nama lapisan dalam file DWG dan cocokkan secara persis dalam `list`. |
| Kesalahan out‑of‑memory pada file besar | Ukuran rasterisasi terlalu besar | Kurangi dimensi halaman atau proses gambar secara bertahap jika memungkinkan. |

## Pertanyaan yang Sering Diajukan

### Q1: Bisakah saya menggunakan Aspose.CAD untuk Java dengan format file CAD lain?
A1: Ya, Aspose.CAD mendukung berbagai format CAD seperti DWG, DXF, DWF, dan lainnya.

### Q2: Apakah ada versi percobaan gratis untuk Aspose.CAD untuk Java?
A2: Ya, Anda dapat menemukan versi percobaan gratis [di sini](https://releases.aspose.com/).

### Q3: Bagaimana cara mendapatkan dukungan untuk Aspose.CAD untuk Java?
A3: Kunjungi forum Aspose.CAD [di sini](https://forum.aspose.com/c/cad/19) untuk dukungan komunitas.

### Q4: Di mana saya dapat menemukan dokumentasi detail untuk Aspose.CAD untuk Java?
A4: Lihat dokumentasi [di sini](https://reference.aspose.com/cad/java/).

### Q5: Bisakah saya membeli lisensi sementara untuk Aspose.CAD untuk Java?
A5: Ya, Anda dapat memperoleh lisensi sementara [di sini](https://purchase.aspose.com/temporary-license/).

### Q6: Apakah metode ini juga bekerja untuk mengonversi DWG ke PDF di lingkungan server tanpa antarmuka (headless)?
A6: Tentu saja. Karena kode hanya menggunakan API Aspose.CAD, ia berjalan tanpa ketergantungan UI, menjadikannya ideal untuk otomasi sisi server.

## Kesimpulan

Anda kini memiliki metode lengkap dan siap produksi untuk **export dwg to pdf** dengan dukungan garis tersembunyi menggunakan Aspose.CAD untuk Java. Pendekatan ini dapat diintegrasikan ke dalam alat pemrosesan batch, layanan web, atau aplikasi desktop untuk mengotomatisasi konversi CAD‑ke‑PDF.

---

**Terakhir Diperbarui:** 2026-03-05  
**Diuji Dengan:** Aspose.CAD untuk Java 24.12  
**Penulis:** Aspose  

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}