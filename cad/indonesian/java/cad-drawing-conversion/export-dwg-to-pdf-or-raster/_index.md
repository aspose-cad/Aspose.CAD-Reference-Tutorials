---
date: 2025-12-18
description: Jelajahi cara mengekspor DWG ke PDF atau gambar raster di Java menggunakan
  Aspose.CAD. Panduan langkah demi langkah ini memastikan presisi, efisiensi, dan
  konversi DWG yang mudah.
linktitle: Export DWG to PDF or Raster
second_title: Aspose.CAD Java API
title: Ekspor DWG ke PDF atau Raster Menggunakan Aspose.CAD untuk Java
url: /id/java/cad-drawing-conversion/export-dwg-to-pdf-or-raster/
weight: 13
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Ekspor DWG ke PDF atau Raster Menggunakan Aspose.CAD untuk Java

## Pendahuluan

Dalam dunia desain berbantuan komputer (CAD) yang dinamis, penanganan gambar yang efisien sangat penting. Dengan **Aspose.CAD for Java** Anda dapat **mengekspor dwg ke pdf** — atau gambar raster — hanya dengan beberapa baris kode. Tutorial ini memandu Anda melalui seluruh proses, mulai dari memuat file DWG hingga menghasilkan PDF berkualitas tinggi, sambil menyoroti mengapa Aspose.CAD Java adalah pustaka pilihan untuk tugas konversi CAD.

## Jawaban Cepat
- **Apa yang dibahas dalam tutorial ini?** Mengekspor file DWG ke PDF atau gambar raster menggunakan Aspose.CAD untuk Java.  
- **Apakah saya memerlukan lisensi?** Lisensi sementara gratis tersedia untuk evaluasi; lisensi penuh diperlukan untuk produksi.  
- **Versi Java mana yang didukung?** Runtime Java 8+ apa pun dapat bekerja dengan API Aspose.CAD Java terbaru.  
- **Bisakah saya mengonversi DWG ke format gambar lain?** Ya – opsi rasterisasi yang sama memungkinkan Anda menghasilkan PNG, JPEG, BMP, dll.  
- **Berapa lama proses konversi?** Biasanya kurang dari satu detik untuk gambar standar; file yang lebih besar mungkin memerlukan beberapa detik.

## Apa itu “export dwg to pdf”?

Mengekspor DWG ke PDF berarti mengonversi gambar AutoCAD asli menjadi dokumen PDF yang portabel dan independen dari perangkat. PDF yang dihasilkan mempertahankan data vektor, lapisan, dan skala, menjadikannya ideal untuk berbagi, mencetak, atau mengarsipkan.

## Mengapa menggunakan Aspose.CAD Java untuk konversi ini?

- **Tanpa ketergantungan eksternal** – Java murni, tanpa DLL native.  
- **Penanganan satuan yang akurat** – secara otomatis menghormati satuan metrik atau imperial.  
- **Output raster berkualitas tinggi** – kontrol DPI dan ukuran halaman yang disesuaikan.  
- **Dukungan PDF penuh** – pembuatan PDF yang mempertahankan vektor tanpa perpustakaan tambahan.

## Prasyarat

Sebelum menyelam ke dalam kode, pastikan Anda memiliki:

- Pengetahuan dasar pemrograman Java.  
- Pustaka Aspose.CAD untuk Java terinstal. Jika Anda belum mengunduhnya, dapatkan **[di sini](https://releases.aspose.com/cad/java/)**.  
- File DWG untuk pengujian – contoh **Bottom_plate.dwg** digunakan dalam panduan ini.

## Impor Namespace

Dalam proyek Java Anda, impor kelas yang diperlukan untuk memulai konversi:

```java
import com.aspose.cad.Image;

import com.aspose.cad.imageoptions.CadRasterizationOptions;
import com.aspose.cad.imageoptions.PdfOptions;
import com.aspose.cad.imageoptions.UnitType;
```

## Panduan Langkah‑per‑Langkah

### Langkah 1: Muat File DWG

Pertama, muat gambar DWG Anda menggunakan kelas `Image`. Ini membuat representasi dalam memori yang dapat diproses oleh Aspose.CAD.

```java
String dataDir = "Your Document Directory" + "DWGDrawings/";
String srcFile = dataDir + "Bottom_plate.dwg";
Image objImage = Image.load(srcFile);
```

### Langkah 2: Tentukan Tipe Unit

Memahami apakah gambar menggunakan satuan metrik atau imperial sangat penting untuk skala yang tepat. Metode bantuan `IsMetric` (implementasi dihilangkan untuk singkat) mengembalikan nilai boolean.

```java
Boolean currentUnitIsMetric = IsMetric(objImage.getUnitType());
int currentUnitCoefficient = objImage.getUnitType();
```

### Langkah 3: Atur Opsi Rasterisasi

Berdasarkan sistem satuan, konfigurasikan ukuran halaman, skala, dan tipe satuan target. Opsi-opsi ini menentukan bagaimana DWG dirasterisasi sebelum dibungkus menjadi PDF.

```java
CadRasterizationOptions rasterizationOptions = new CadRasterizationOptions();

if (currentUnitIsMetric) {
    // Metric units
    double metersCoeff = 1 / 1000.0;
    double scaleFactor = metersCoeff / currentUnitCoefficient;
    rasterizationOptions.setPageWidth((float)(210 * scaleFactor));
    rasterizationOptions.setPageHeight((float)(297 * scaleFactor));
    rasterizationOptions.setUnitType(UnitType.Millimeter);
} else {
    // Imperial units
    rasterizationOptions.setPageWidth((float)(8.27f / currentUnitCoefficient));
    rasterizationOptions.setPageHeight((float)(11.69f / currentUnitCoefficient));
    rasterizationOptions.setUnitType(UnitType.Inch);
}
```

### Langkah 4: Konfigurasikan Opsi PDF

Buat instance `PdfOptions` dan lampirkan pengaturan rasterisasi. Ini memberi tahu Aspose.CAD cara menyematkan konten yang dirasterisasi ke dalam PDF akhir.

```java
PdfOptions pdfOptions = new PdfOptions();
pdfOptions.setVectorRasterizationOptions(new CadRasterizationOptions());
```

### Langkah 5: Simpan sebagai PDF

Akhirnya, ekspor gambar ke file PDF. Metode `save` menerima jalur output dan `PdfOptions` yang telah dikonfigurasi.

```java
objImage.save(dataDir + "Saved.pdf", pdfOptions);
```

Setelah kode selesai, Anda akan menemukan **Saved.pdf** di folder `DWGDrawings` Anda, siap untuk distribusi atau pengarsipan.

## Masalah Umum & Tips

- **Ukuran halaman tidak tepat** – Periksa kembali logika konversi satuan; koefisien yang tidak cocok dapat menghasilkan halaman terlalu besar.  
- **Font atau ketebalan garis hilang** – Pastikan DWG merujuk ke sumber daya eksternal apa pun sebelum konversi.  
- **Kinerja pada gambar besar** – Tingkatkan pengaturan `DPI` di `CadRasterizationOptions` hanya ketika kualitas lebih tinggi diperlukan; DPI lebih rendah mempercepat pemrosesan.

## Pertanyaan yang Sering Diajukan

**Q: Bisakah saya menggunakan Aspose.CAD untuk Java dengan kerangka kerja Java lain?**  
A: Ya, Aspose.CAD untuk Java terintegrasi secara mulus dengan kerangka kerja Java populer seperti Spring, Jakarta EE, dan Android.

**Q: Apakah lisensi sementara tersedia untuk Aspose.CAD untuk Java?**  
A: Ya, Anda dapat memperoleh lisensi sementara **[di sini](https://purchase.aspose.com/temporary-license/)**.

**Q: Di mana saya dapat menemukan dukungan untuk Aspose.CAD untuk Java?**  
A: Kunjungi **[forum Aspose.CAD](https://forum.aspose.com/c/cad/19)** untuk bantuan dari komunitas dan insinyur Aspose.

**Q: Bagaimana cara membeli lisensi untuk Aspose.CAD untuk Java?**  
A: Anda dapat membeli lisensi **[di sini](https://purchase.aspose.com/buy)**.

**Q: Unit apa yang didukung oleh Aspose.CAD untuk Java?**  
A: Aspose.CAD untuk Java mendukung baik satuan metrik maupun imperial, secara otomatis mendeteksi sistem satuan gambar.

**Q: Bisakah saya mengonversi DWG ke format gambar lain (mis., PNG, JPEG) menggunakan API yang sama?**  
A: Tentu saja. Ganti `PdfOptions` dengan opsi gambar raster yang sesuai (mis., `PngOptions`) dan gunakan kembali `CadRasterizationOptions` yang sama.

## Kesimpulan

Tutorial ini menunjukkan cara **mengekspor dwg ke pdf** dan gambar raster menggunakan Aspose.CAD untuk Java. Dengan mengikuti panduan langkah‑per‑langkah, Anda dapat mengintegrasikan konversi CAD yang handal ke dalam aplikasi Java apa pun, baik Anda memerlukan PDF untuk dokumentasi atau gambar raster untuk tampilan web.

---

**Last Updated:** 2025-12-18  
**Tested With:** Aspose.CAD for Java 24.10  
**Author:** Aspose  

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}