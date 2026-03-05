---
date: 2026-03-05
description: เรียนรู้วิธีการเปลี่ยนเส้นทาง xref, อัปเดตการอ้างอิงบล็อกและจัดการไฮเปอร์ลิงก์
  CAD ด้วย Aspose.CAD สำหรับ .NET ในไม่กี่ขั้นตอนง่าย ๆ.
linktitle: Editing Hyperlinks in CAD Files
second_title: Aspose.CAD .NET - CAD and BIM File Format
title: วิธีเปลี่ยนเส้นทาง xref และแก้ไขไฮเปอร์ลิงก์ในไฟล์ CAD - บทเรียน Aspose.CAD
url: /th/net/advanced-cad-techniques/editing-hyperlinks-in-cad-files/
weight: 14
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# การแก้ไขไฮเปอร์ลิงก์ในไฟล์ CAD - บทแนะนำ Aspise.CAD

## Introduction

ยินดีต้อนรับสู่คู่มือแบบขั้นตอนของเราว่าจะ **เปลี่ยนเส้นทาง xref** และแก้ไขไฮเปอร์ลิงก์ในไฟล์ CAD ด้วย Aspose.CAD สำหรับ .NET ไม่ว่าคุณจะต้องการ **อัปเดตข้อมูลอ้างอิงบล็อก** หรือเพียงแค่ **จัดการไฮเปอร์ลิงก์ CAD** บทแนะนำนี้จะพาคุณผ่านกระบวนการทั้งหมด ตั้งแต่การโหลดไฟล์ DWG จนถึงการบันทึกการเปลี่ยนแปลง เมื่อเสร็จสิ้นคุณจะมีรูปแบบที่ชัดเจนและนำกลับมาใช้ใหม่ได้สำหรับการเชื่อมโยงเอกสาร CAD ของคุณอย่างถูกต้อง

## Quick Answers
- **What does “change xref path” mean?** It updates the external reference (XRef) file path stored in a CAD block.  
- **Which library handles this?** Aspose.CAD for .NET provides a simple API for editing XRef paths and hyperlinks.  
- **Do I need a license?** A free trial works for development; a commercial license is required for production.  
- **Can I use this with .NET Core?** Yes, the library supports .NET Framework and .NET Core/.NET 5+.  
- **How long does the implementation take?** Typically under 10 minutes for a basic file.

## What is changing the XRef path?

ในศัพท์ของ CAD, **XRef** (external reference) จะชี้ไปยังไฟล์การวาดอื่นที่ถูกแทรกเป็นบล็อก การเปลี่ยนเส้นทาง XRef หมายถึงการกำหนดตำแหน่งไฟล์ใหม่ให้กับบล็อก ซึ่งเป็นสิ่งสำคัญเมื่อจัดระเบียบโฟลเดอร์โครงการหรืออัปเดตทรัพยากรที่เชื่อมโยง

## Why update block reference and manage CAD hyperlinks?

- **Maintain consistency** when files are moved across environments.  
- **Avoid broken links** that can cause errors during rendering or downstream processing.  
- **Streamline BIM workflows** by programmatically ensuring all references are current.  

## Prerequisites

- ความรู้พื้นฐานเกี่ยวกับ C# และการพัฒนา .NET  
- ติดตั้ง Aspose.CAD สำหรับ .NET – ดาวน์โหลดได้จาก [here](https://releases.aspose.com/cad/net/)  
- ไฟล์ CAD ตัวอย่าง (เช่น *AutoCad_Sample.dwg*) เพื่อทดลอง

## Import Namespaces

ในโปรเจกต์ C# ของคุณ ให้เพิ่ม namespace ที่จำเป็น:

```csharp
using Aspose.CAD.FileFormats.Cad;
using Aspose.CAD.FileFormats.Cad.CadObjects;
using System;
using System.Collections.Generic;
using System.Linq;
using System.Text;
```

ตอนนี้เราจะเดินผ่านการทำงานขั้นตอนต่อขั้นตอน

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

*ที่นี่เราจะ **อัปเดตอ้างอิงบล็อก** โดยกำหนดชื่อไฟล์ XRef ใหม่ นี่คือหัวใจของการเปลี่ยนเส้นทาง XRef*

## Step 4: Modify Hyperlinks – Manage CAD Hyperlinks

```csharp
if (entity.Hyperlink == "https://products.aspose.com")
{
    // **Secondary keyword usage:** manage cad hyperlinks
    entity.Hyperlink = "https://www.aspose.com";
}
```

*โค้ดส่วนนี้แสดงวิธี **อัปเดตลิงก์ CAD** (hyperlinks) ให้ชี้ไปยังที่อยู่เว็บที่ถูกต้อง*

## Common Issues and Solutions

| Issue | Cause | Fix |
|-------|-------|-----|
| XRef path not updating | Block is not an `CadInsertObject` | Verify entity type before casting. |
| Hyperlink unchanged | Hyperlink property is null or different case | Use `StringComparison.OrdinalIgnoreCase` when comparing. |
| File fails to load | Missing Aspose.CAD license in production | Apply a valid license before loading the image. |

## Conclusion

คุณได้เรียนรู้วิธี **เปลี่ยนเส้นทาง xref**, **อัปเดตอ้างอิงบล็อก**, และ **จัดการไฮเปอร์ลิงก์ CAD** ด้วย Aspose.CAD สำหรับ .NET ความสามารถเหล่านี้ช่วยให้คุณจัดระเบียบโครงการ CAD ขนาดใหญ่และหลีกเลี่ยงการอ้างอิงที่เสียหาย เพิ่มความน่าเชื่อถือในกระบวนการอัตโนมัติ

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