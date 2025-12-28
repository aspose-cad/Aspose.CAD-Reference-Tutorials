---
date: 2025-12-28
description: Pelajari cara membaca file DWG menggunakan Aspose.CAD untuk Java dan
  dengan mudah menampilkan daftar layout dalam file DWG. Integrasikan fungsi CAD yang
  kuat ke dalam aplikasi Java Anda.
linktitle: List Layouts in DWG
second_title: Aspose.CAD Java API
title: Cara Membaca DWG dan Daftar Layout di DWG Menggunakan Aspose.CAD untuk Java
url: /id/java/cad-file-manipulation/list-layouts-in-dwg/
weight: 12
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Cara Membaca DWG dan Daftar Layout dalam DWG Menggunakan Aspose.CAD untuk Java

## Pendahuluan

Jika Anda perlu **membaca DWG** secara programatis dan mengekstrak informasi seperti nama layout, Aspose.CAD untuk Java mempermudahnya. Dalam tutorial langkah‑demi‑langkah ini kami akan menunjukkan **cara membaca DWG** dan mendaftar semua layout yang terdapat dalam file DWG (atau DXF). Pada akhir panduan Anda akan dapat menambahkan kemampuan ini ke aplikasi Java apa pun yang bekerja dengan data CAD.

## Jawaban Cepat
- **Perpustakaan apa yang diperlukan?** Aspose.CAD untuk Java.
- **Apakah saya dapat membaca file DWG di sistem operasi apa pun?** Ya – Java bersifat lintas‑platform.
- **Apakah saya memerlukan lisensi untuk menjalankan contoh?** Versi percobaan gratis dapat digunakan untuk evaluasi; lisensi diperlukan untuk produksi.
- **Format CAD apa yang didukung?** DWG, DXF, DWF, dan lainnya.
- **Apakah kode kompatibel dengan Java 8+?** Tentu saja.

## Apa itu “cara membaca dwg” dalam Java?

Membaca file DWG berarti memuat data CAD biner ke dalam model objek yang dapat Anda query. Aspose.CAD menyederhanakan struktur DWG yang kompleks di balik kelas .NET/Java yang sederhana, memungkinkan Anda fokus pada informasi yang dibutuhkan – dalam hal ini, nama layout.

## Mengapa mendaftar layout dalam file DWG?

A DWG dapat berisi beberapa layout (paper space, model space, lembar khusus). Mengetahui nama layout memungkinkan Anda:
- Membuat laporan per layout.
- Mengekspor layout tertentu ke gambar atau PDF.
- Mengotomatiskan pemrosesan batch gambar.

## Prasyarat

Sebelum kita masuk ke kode, pastikan Anda memiliki hal berikut:

- **Aspose.CAD untuk Java Library** – unduh JAR terbaru dari [situs web](https://releases.aspose.com/cad/java/).
- **Lingkungan Pengembangan Java** – JDK 8 atau lebih tinggi, serta IDE atau alat build pilihan Anda.

## Impor Namespace

Dalam file sumber Java Anda, impor kelas Aspose.CAD yang diperlukan:

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

Ganti **“Your Document Directory”** dengan path absolut tempat file CAD Anda berada.

## Langkah 2: Muat File DWG

```java
String sourceFilePath = dataDir + "conic_pyramid.dxf";
Image image = Image.load(sourceFilePath);
CadImage cadImage = (CadImage)image;
```

Metode `Image.load` mendeteksi format file secara otomatis, sehingga Anda dapat menggunakan kode yang sama untuk file **DWG** dan **DXF**.

## Langkah 3: Dapatkan Layout dan Cetak Nama

```java
CadLayoutDictionary layouts = cadImage.getLayouts();
for (CadLayout layout : layouts.getValues())
{
    System.out.println("Layout " + layout.getLayoutName());
}
```

Loop tersebut mengiterasi setiap objek layout dan mencetak namanya ke konsol – cara sederhana untuk memverifikasi bahwa Anda telah berhasil **membaca DWG** dan mengekstrak informasi layout.

## Kesalahan Umum & Tips

- **Path file tidak tepat** – Periksa kembali bahwa `dataDir` diakhiri dengan pemisah (`/` atau `\\`) yang sesuai untuk OS Anda.
- **Versi DWG tidak didukung** – Pastikan Anda menggunakan versi Aspose.CAD terbaru; versi DWG lama mungkin memerlukan konversi.
- **Penggunaan memori** – Gambar besar dapat mengonsumsi memori yang signifikan. Hapus objek `CadImage` setelah selesai: `cadImage.dispose();`.

## Kesimpulan

Selamat! Anda kini mengetahui **cara membaca DWG** dan mendaftar layout-nya menggunakan Aspose.CAD untuk Java. Teknik ini menjadi dasar untuk otomasi CAD yang lebih maju, seperti mengekspor layout tertentu ke gambar atau PDF. Untuk eksplorasi lebih lanjut, lihat [dokumentasi](https://reference.aspose.com/cad/java/) resmi.

## FAQ

### Q1: Bisakah saya menggunakan Aspose.CAD untuk Java dengan format file CAD lainnya?

A1: Ya, Aspose.CAD mendukung berbagai format CAD, termasuk DWG, DXF, DWF, dan lainnya.

### Q2: Apakah tersedia versi percobaan gratis untuk Aspose.CAD untuk Java?

A2: Ya, Anda dapat memperoleh versi percobaan gratis dari [sini](https://releases.aspose.com/).

### Q3: Di mana saya dapat mendapatkan dukungan komunitas untuk Aspose.CAD untuk Java?

A3: Kunjungi [forum Aspose.CAD](https://forum.aspose.com/c/cad/19) untuk dukungan komunitas.

### Q4: Bagaimana cara membeli lisensi untuk Aspose.CAD untuk Java?

A4: Anda dapat membeli lisensi dari [halaman pembelian](https://purchase.aspose.com/buy).

### Q5: Bisakah saya menggunakan lisensi sementara untuk tujuan pengujian?

A5: Ya, Anda dapat memperoleh lisensi sementara [di sini](https://purchase.aspose.com/temporary-license/).

**Q: Apakah pendekatan ini bekerja untuk membaca file DWG di Linux?**  
A: Tentu saja. Karena solusinya murni Java, ia dapat dijalankan di OS apa pun dengan JDK yang kompatibel.

**Q: Bisakah saya membaca file DWG tanpa memuat seluruh gambar ke memori?**  
A: Aspose.CAD memuat gambar ke memori; untuk file yang sangat besar pertimbangkan memprosesnya dalam thread terpisah atau menggunakan API streaming jika tersedia pada rilis mendatang.

**Q: Apakah ada cara untuk memfilter layout berdasarkan nama?**  
A: Ya – setelah mengambil `CadLayoutDictionary`, Anda dapat memeriksa `layout.getLayoutName().equalsIgnoreCase("MyLayout")` sebelum memproses.

---

**Terakhir Diperbarui:** 2025-12-28  
**Diuji Dengan:** Aspose.CAD untuk Java 24.11  
**Penulis:** Aspose  

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}