---
date: 2026-03-05
description: Pelajari cara mengubah jalur xref, memperbarui referensi blok, dan mengelola
  hyperlink CAD menggunakan Aspose.CAD untuk .NET dalam beberapa langkah mudah.
linktitle: Editing Hyperlinks in CAD Files
second_title: Aspose.CAD .NET - CAD and BIM File Format
title: Cara mengubah jalur xref dan mengedit hyperlink dalam File CAD – Tutorial Aspose.CAD
url: /id/net/advanced-cad-techniques/editing-hyperlinks-in-cad-files/
weight: 14
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Mengedit Hyperlink dalam File CAD - Tutorial Aspise.CAD

## Introduction

Selamat datang di panduan langkah‑demi‑langkah kami tentang cara **change xref path** dan mengedit hyperlink dalam file CAD dengan Aspose.CAD untuk .NET. Apakah Anda perlu **update block reference** atau sekadar **manage CAD hyperlinks**, tutorial ini akan memandu Anda melalui proses lengkap, mulai dari memuat file DWG hingga menyimpan perubahan. Pada akhir tutorial, Anda akan memiliki pola yang jelas dan dapat digunakan kembali untuk memastikan dokumen CAD Anda terhubung dengan benar.

## Quick Answers
- **What does “change xref path” mean?** It updates the external reference (XRef) file path stored in a CAD block.  
- **Which library handles this?** Aspose.CAD for .NET provides a simple API for editing XRef paths and hyperlinks.  
- **Do I need a license?** A free trial works for development; a commercial license is required for production.  
- **Can I use this with .NET Core?** Yes, the library supports .NET Framework and .NET Core/.NET 5+.  
- **How long does the implementation take?** Typically under 10 minutes for a basic file.

## What is changing the XRef path?

Dalam terminologi CAD, **XRef** (external reference) mengacu pada file gambar lain yang dimasukkan sebagai blok. Mengubah XRef path berarti mengarahkan blok ke lokasi file baru, yang penting saat mengatur ulang folder proyek atau memperbarui sumber daya yang terhubung.

## Why update block reference and manage CAD hyperlinks?

- **Maintain consistency** when files are moved across environments.  
- **Avoid broken links** that can cause errors during rendering or downstream processing.  
- **Streamline BIM workflows** by programmatically ensuring all references are current.  

## Prerequisites

- Pengetahuan dasar tentang C# dan pengembangan .NET.  
- Aspose.CAD untuk .NET terpasang – unduh di [here](https://releases.aspose.com/cad/net/).  
- File CAD contoh (misalnya *AutoCad_Sample.dwg*) untuk percobaan.

## Import Namespaces

Di proyek C# Anda, sertakan namespace yang diperlukan:

```csharp
using Aspose.CAD.FileFormats.Cad;
using Aspose.CAD.FileFormats.Cad.CadObjects;
using System;
using System.Collections.Generic;
using System.Linq;
using System.Text;
```

Now let’s walk through the implementation step by step.

## Step 1: Load the CAD File

```csharp
// The path to the documents directory.
string MyDir = "Your Document Directory";
string dwgPathToFile = MyDir + "AutoCad_Sample.dwg";

using (CadImage cadImage = (CadImage)Image.Load(dwgPathToFile))
{
    // Your code for editing hyperlinks will go here.
}
```

## Step 2: Iterate Through Entities

```csharp
foreach (CadBaseEntity entity in cadImage.Entities)
{
    // Your code for handling each entity will go here.
}
```

## Step 3: Edit Insert Objects – Change XRef Path

```csharp
if (entity is CadInsertObject)
{
    CadBlockEntity block = cadImage.BlockEntities[((CadInsertObject)entity).Name];
    if (!string.IsNullOrEmpty(block.XRefPathName.Value))
    {
        // **Primary keyword usage:** change xref path
        block.XRefPathName.Value = "new file reference.dwg";
    }
}
```

*Here we **update block reference** by assigning a new XRef file name. This is the core of changing the XRef path.*

## Step 4: Modify Hyperlinks – Manage CAD Hyperlinks

```csharp
if (entity.Hyperlink == "https://products.aspose.com")
{
    // **Secondary keyword usage:** manage cad hyperlinks
    entity.Hyperlink = "https://www.aspose.com";
}
```

*This snippet demonstrates how to **update CAD links** (hyperlinks) to point to the correct web address.*

## Common Issues and Solutions

| Masalah | Penyebab | Solusi |
|-------|-------|-----|
| XRef path tidak terupdate | Blok bukan `CadInsertObject` | Verifikasi tipe entitas sebelum casting. |
| Hyperlink tidak berubah | Properti Hyperlink bernilai null atau case berbeda | Gunakan `StringComparison.OrdinalIgnoreCase` saat membandingkan. |
| File gagal dimuat | Lisensi Aspose.CAD tidak ada di produksi | Terapkan lisensi yang valid sebelum memuat gambar. |

## Conclusion

Anda kini telah mempelajari cara **change xref path**, **update block reference**, dan **manage CAD hyperlinks** menggunakan Aspose.CAD untuk .NET. Kemampuan ini memungkinkan Anda menjaga proyek CAD besar tetap terorganisir dan bebas dari referensi yang rusak, meningkatkan keandalan dalam pipeline otomatis.

## FAQ's

### Q1: Is Aspose.CAD compatible with other CAD file formats?

A1: Yes, Aspose.CAD supports various CAD formats, including DWG, DXF, DGN, and more.

### Q2: Can I try Aspose.CAD before purchasing?

A2: Absolutely! You can access a free trial [here](https://releases.aspose.com/).

### Q3: Where can I find detailed documentation for Aspose.CAD?

A3: Refer to the documentation [here](https://reference.aspose.com/cad/net/).

### Q4: How do I get a temporary license for Aspose.CAD?

A4: Obtain a temporary license [here](https://purchase.aspose.com/temporary-license/).

### Q5: Need assistance or have questions?

A5: Visit our support forum [here](https://forum.aspose.com/c/cad/19).

## Additional Frequently Asked Questions

**Q: Can I programmatically change multiple XRef paths in one pass?**  
A: Yes, iterate through all `CadInsertObject` entities and set `XRefPathName.Value` as needed.

**Q: Does changing the XRef path affect the visual appearance of the drawing?**  
A: The reference updates, but the drawing will display the new external file when opened in a CAD viewer.

**Q: Is there a way to list all current hyperlinks in a CAD file?**  
A: Loop through `cadImage.Entities` and collect `entity.Hyperlink` values that are not null or empty.

**Q: Will this approach work with large DWG files (hundreds of MB)?**  
A: Aspose.CAD is optimized for performance, but ensure sufficient memory and consider processing in chunks if needed.

---

**Last Updated:** 2026-03-05  
**Tested With:** Aspose.CAD 24.12 for .NET  
**Author:** Aspose  

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}