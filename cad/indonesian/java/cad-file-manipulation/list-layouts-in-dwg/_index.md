---
date: 2026-02-28
description: Pelajari cara membaca file DWG menggunakan Aspose.CAD untuk Java dan
  dengan mudah menampilkan daftar layout dalam file DWG. Integrasikan fungsionalitas
  CAD yang kuat ke dalam aplikasi Java Anda.
linktitle: List Layouts in DWG
second_title: Aspose.CAD Java API
title: Cara Membaca DWG dan Daftar Layout dalam DWG Menggunakan Aspose.CAD untuk Java
url: /id/java/cad-file-manipulation/list-layouts-in-dwg/
weight: 12
---

ose.CAD untuk Java". Keep same heading level.

Proceed section by section.

Also need to translate "Quick Answers" etc.

Make sure to keep markdown formatting.

Let's produce final content.

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Cara Membaca DWG dan Daftar Layout dalam DWG Menggunakan Aspose.CAD untuk Java

## Pendahuluan

Jika Anda mencari cara yang andal **cara membaca dwg** secara programatis, Aspose.CAD untuk Java menyediakan API bersih lintas‑platform yang memungkinkan Anda memuat sebuah gambar dan mengambil informasi apa pun yang Anda butuhkan—seperti nama semua layout di dalam file. Pada tutorial langkah‑demi‑langkah ini kami akan menunjukkan **cara membaca DWG** dan mencantumkan setiap layout yang terdapat dalam file DWG (atau DXF), sehingga Anda dapat mengintegrasikan kemampuan ini ke dalam aplikasi Java apa pun yang bekerja dengan data CAD.

## Jawaban Cepat
- **Perpustakaan apa yang diperlukan?** Aspose.CAD untuk Java.  
- **Apakah saya dapat membaca file DWG di sistem operasi apa pun?** Ya – Java lintas‑platform, sehingga Anda dapat **membaca dwg di linux** dengan mudah seperti di Windows.  
- **Apakah saya memerlukan lisensi untuk menjalankan contoh?** Versi percobaan gratis cukup untuk evaluasi; lisensi diperlukan untuk produksi.  
- **Format CAD mana yang didukung?** DWG, DXF, DWF, dan lainnya.  
- **Apakah kode ini kompatibel dengan Java 8+?** Tentu saja.

## Apa itu “cara membaca dwg” dalam Java?

Membaca file DWG berarti memuat data CAD biner ke dalam model objek yang dapat Anda query. Aspose.CAD menyederhanakan struktur DWG yang kompleks di balik kelas Java sederhana, memungkinkan Anda fokus pada informasi yang dibutuhkan – dalam hal ini, nama layout.

## Mengapa mencantumkan layout dalam file DWG?

Sebuah DWG dapat berisi beberapa layout (paper space, model space, lembar khusus). Mengetahui nama layout memungkinkan Anda:

- Membuat laporan per layout.  
- Mengekspor layout tertentu ke gambar atau PDF.  
- Mengotomatiskan pemrosesan batch gambar.  

## Prasyarat

Sebelum masuk ke kode, pastikan Anda memiliki hal‑hal berikut:

- **Aspose.CAD untuk Java Library** – unduh JAR terbaru dari [website](https://releases.aspose.com/cad/java/).  
- **Lingkungan Pengembangan Java** – JDK 8 atau yang lebih tinggi, serta IDE atau alat build pilihan Anda.

## Impor Namespace

Di file sumber Java Anda, impor kelas Aspose.CAD yang diperlukan:

```java
import com.aspose.cad.Image;

import com.aspose.cad.fileformats.cad.CadImage;
import com.aspose.cad.fileformats.cad.CadLayoutDictionary;
import com.aspose.cad.fileformats.cad.cadobjects.CadLayout;
```

## Langkah 1: Siapkan Direktori Dokumen Anda

```java
String dataDir = "Your Document Directory" + "CADConversion/";
```

Ganti **“Your Document Directory”** dengan jalur absolut tempat file CAD Anda berada. Di Linux Anda dapat menggunakan jalur seperti `/home/user/cad/`.

## Langkah 2: Muat File DWG

```java
String sourceFilePath = dataDir + "conic_pyramid.dxf";
Image image = Image.load(sourceFilePath);
CadImage cadImage = (CadImage)image;
```

Metode `Image.load` secara otomatis mendeteksi format file, sehingga kode yang sama bekerja untuk file **DWG** maupun **DXF**.

## Langkah 3: Dapatkan Layout dan Cetak Nama

```java
CadLayoutDictionary layouts = cadImage.getLayouts();
for (CadLayout layout : layouts.getValues())
{
    System.out.println("Layout " + layout.getLayoutName());
}
```

Loop ini mengiterasi setiap objek layout dan mencetak namanya ke konsol – cara sederhana untuk memverifikasi bahwa Anda telah berhasil **membaca DWG** dan mengekstrak informasi layout.

## Cara Mengonversi DWG ke PDF di Linux

Jika Anda kemudian perlu mengubah layout tertentu menjadi PDF, Aspose.CAD dapat merender layout ke gambar dan kemudian Anda dapat menggunakan Aspose.PDF (atau perpustakaan PDF lain) untuk menyisipkan gambar tersebut ke dalam dokumen PDF. Kode konversi identik di Linux karena API murni Java.

## Kesalahan Umum & Tips

- **Jalur file tidak tepat** – Pastikan `dataDir` diakhiri dengan pemisah (`/` atau `\\`) yang sesuai untuk OS Anda.  
- **Versi DWG tidak didukung** – Pastikan Anda menggunakan versi Aspose.CAD terbaru; versi DWG lama mungkin memerlukan konversi.  
- **Penggunaan memori** – Gambar besar dapat mengonsumsi memori signifikan. Hapus objek `CadImage` setelah selesai: `cadImage.dispose();`.  
- **Menjalankan di server tanpa tampilan** – Tidak ada komponen UI yang diperlukan, sehingga kode berjalan di server Linux tanpa lingkungan grafis.

## Kesimpulan

Selamat! Anda kini tahu **cara membaca dwg** dan mencantumkan layout‑nya menggunakan Aspose.CAD untuk Java. Teknik ini menjadi dasar untuk otomasi CAD yang lebih maju, seperti mengekspor layout tertentu ke gambar, PDF, atau bahkan mengonversi DWG ke PDF di Linux. Untuk eksplorasi lebih dalam, lihat [dokumentasi resmi](https://reference.aspose.com/cad/java/).

## Pertanyaan yang Sering Diajukan

**T1: Bisakah saya menggunakan Aspose.CAD untuk Java dengan format file CAD lain?**  
J1: Ya, Aspose.CAD mendukung berbagai format CAD, termasuk DWG, DXF, DWF, dan lainnya.

**T2: Apakah tersedia versi percobaan gratis untuk Aspose.CAD untuk Java?**  
J2: Ya, Anda dapat memperoleh versi percobaan gratis dari [sini](https://releases.aspose.com/).

**T3: Di mana saya dapat mendapatkan dukungan komunitas untuk Aspose.CAD untuk Java?**  
J3: Kunjungi [forum Aspose.CAD](https://forum.aspose.com/c/cad/19) untuk dukungan komunitas.

**T4: Bagaimana cara membeli lisensi untuk Aspose.CAD untuk Java?**  
J4: Anda dapat membeli lisensi melalui [halaman pembelian](https://purchase.aspose.com/buy).

**T5: Bisakah saya menggunakan lisensi sementara untuk tujuan pengujian?**  
J5: Ya, Anda dapat memperoleh lisensi sementara [di sini](https://purchase.aspose.com/temporary-license/).

**Pertanyaan Tambahan**

**T: Apakah pendekatan ini bekerja untuk membaca file DWG di Linux?**  
J: Tentu saja. Karena solusinya murni Java, ia berjalan di OS apa pun dengan JDK yang kompatibel.

**T: Bisakah saya membaca file DWG tanpa memuat seluruh gambar ke memori?**  
J: Aspose.CAD memuat gambar ke memori; untuk file sangat besar pertimbangkan memprosesnya dalam thread terpisah atau menggunakan API streaming bila tersedia di rilis mendatang.

**T: Apakah ada cara untuk menyaring layout berdasarkan nama?**  
J: Ya – setelah mengambil `CadLayoutDictionary`, Anda dapat memeriksa `layout.getLayoutName().equalsIgnoreCase("MyLayout")` sebelum memprosesnya.

---

**Terakhir Diperbarui:** 2026-02-28  
**Diuji Dengan:** Aspose.CAD untuk Java 24.11  
**Penulis:** Aspose  

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}