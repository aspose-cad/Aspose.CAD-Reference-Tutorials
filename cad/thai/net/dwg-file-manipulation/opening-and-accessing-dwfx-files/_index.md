---
date: 2026-04-09
description: เรียนรู้วิธีโหลดไฟล์ DWFX ด้วย C# และแปลง CAD เป็น PDF ด้วย Aspose.CAD
  สำหรับ .NET คู่มือขั้นตอนต่อขั้นตอนเพื่อการรวมระบบอย่างราบรื่น
keywords:
- load dwfx file c#
- c# convert cad to pdf
- aspose.cad dwfx
linktitle: การเปิดและเข้าถึงไฟล์ DWFX ใน C#
second_title: Aspose.CAD .NET - CAD and BIM File Format
title: วิธีโหลดไฟล์ DWFX ใน C# ด้วยคู่มือ Aspose.CAD
url: /th/net/dwg-file-manipulation/opening-and-accessing-dwfx-files/
weight: 12
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# วิธีโหลดไฟล์ DWFX ใน C# ด้วยคู่มือ Aspose.CAD

## บทนำ

หากคุณต้องการ **โหลดไฟล์ DWFX C#** และแปลงเป็น PDF คุณมาถูกที่แล้ว ในบทแนะนำนี้เราจะอธิบายขั้นตอนที่ต้องทำเพื่อเปิดไฟล์ DWFX ด้วย Aspose.CAD for .NET ตั้งค่าการเรสเตอร์ไลซ์ และสุดท้าย **c# convert CAD to PDF** ไม่ว่าคุณจะสร้างยูทิลิตี้บนเดสก์ท็อปหรือบริการเว็บ วิธีการก็เหมือนกันและทำงานกับ .NET เวอร์ชันใดก็ได้ที่ Aspose.CAD รองรับ

## คำตอบอย่างรวดเร็ว
- **ต้องใช้ไลบรารีอะไร?** Aspose.CAD for .NET  
- **สามารถแปลง DWFX เป็น PDF ได้หรือไม่?** ได้ – เพียงกำหนด `CadRasterizationOptions` แล้วใช้ `PdfOptions`  
- **รองรับ .NET เวอร์ชันใดบ้าง?** .NET Framework 4.5+, .NET Core 3.1+, .NET 5/6+  
- **ต้องมีลิขสิทธิ์สำหรับการทดสอบหรือไม่?** เวอร์ชันทดลองฟรีใช้ได้สำหรับการพัฒนา; ต้องมีลิขสิทธิ์ถาวรสำหรับการผลิต  
- **โค้ดใช้เวลารันนานแค่ไหน?** การโหลดและแปลงไฟล์ DWFX ปกติเสร็จภายในไม่กี่วินาทีบน CPU สมัยใหม่

## DWFX คืออะไร?

DWFX (Design Web Format XPS) เป็นรูปแบบที่อิง XML สำหรับการแสดงภาพวาด CAD ที่สามารถเรนเดอร์ในเบราว์เซอร์และโปรแกรมดูอื่น ๆ เนื่องจากเก็บข้อมูลเวกเตอร์ ทำให้เหมาะสำหรับการแปลงเป็น PDF คุณภาพสูงโดยไม่สูญเสียรายละเอียด

## ทำไมต้องใช้ Aspose.CAD เพื่อโหลดไฟล์ DWFX ใน C#?

* **รองรับรูปแบบครบวงจร** – Aspose.CAD เข้าใจ DWFX รวมถึงรูปแบบ CAD อื่น ๆ อีกหลายสิบแบบ  
* **ไม่มีการพึ่งพาไลบรารีภายนอก** – ทำงานบน .NET อย่างเดียว ไม่ต้องใช้ AutoCAD หรือคอมโพเนนต์เนทีฟอื่น  
* **การแปลง raster‑to‑vector ง่าย** – สลับระหว่างภาพ raster และ PDF เวกเตอร์ได้ด้วยไม่กี่บรรทัดโค้ด  

## ข้อกำหนดเบื้องต้น

ก่อนจะลงมือเขียนโค้ด โปรดตรวจสอบว่าคุณมี:

1. **Aspose.CAD for .NET** ติดตั้งแล้ว คุณสามารถดาวน์โหลดได้ [ที่นี่](https://releases.aspose.com/cad/net/)  
2. โฟลเดอร์ที่บรรจุไฟล์ DWFX ที่ต้องการประมวลผล จดบันทึกพาธเต็มของโฟลเดอร์ต้นทางและปลายทาง

## วิธีโหลดไฟล์ DWFX ใน C#

ต่อไปนี้เป็นคำแนะนำแบบขั้นตอนต่อขั้นตอน แต่ละขั้นตอนมีคำอธิบายสั้น ๆ ตามด้วยโค้ดบล็อกที่ต้องคัดลอก

### นำเข้า Namespaces

```csharp
using Aspose.CAD.ImageOptions;
using System;
```

เนมสเปซเหล่านี้ให้คุณเข้าถึงคลาส `Image` สำหรับโหลดไฟล์ CAD และตัวเลือกที่จำเป็นสำหรับการเรสเตอร์ไลซ์และการส่งออกเป็น PDF

### ขั้นตอนที่ 1: ตั้งค่าไดเรกทอรีต้นทางและปลายทาง

```csharp
string SourceDir = "Your Document Directory";
string OutputDir = "Your Document Directory";
```

เปลี่ยน `"Your Document Directory"` ให้เป็นพาธที่ไฟล์ DWFX ของคุณอยู่และพาธที่ต้องการบันทึก PDF

### ขั้นตอนที่ 2: โหลดไฟล์ DWFX

```csharp
using (Image cadDrawing = Image.Load(SourceDir + "Tyrannosaurus.dwfx"))
```

`Image.Load` จะอ่านไฟล์ DWFX เข้าเป็นอ็อบเจกต์ `Image` ที่ Aspose.CAD สามารถทำงานได้ เปลี่ยน `"Tyrannosaurus.dwfx"` ให้เป็นชื่อไฟล์ของคุณเอง

### ขั้นตอนที่ 3: กำหนดค่าตัวเลือกการเรสเตอร์ไลซ์

```csharp
var rasterizationOptions = new CadRasterizationOptions();
rasterizationOptions.PageWidth = cadDrawing.Size.Width;
rasterizationOptions.PageHeight = cadDrawing.Size.Height;
```

ตัวเลือกการเรสเตอร์ไลซ์บอก Aspose.CAD ว่าหน้าผลลัพธ์ควรมีขนาดเท่าใด การใช้ขนาดเดิมของภาพวาดจะรักษาสเกลอย่างแม่นยำ

### ขั้นตอนที่ 4: บันทึกเป็น PDF (c# แปลง CAD เป็น PDF)

```csharp
PdfOptions CADf = new PdfOptions();
CADf.VectorRasterizationOptions = rasterizationOptions;
cadDrawing.Save(OutputDir + "OpenDwfxFile_out.pdf", CADf);
```

ที่นี่เราจะ **c# convert CAD to PDF** โดยผูกการตั้งค่าการเรสเตอร์ไลซ์กับอ็อบเจกต์ `PdfOptions` แล้วเรียก `Save` ไฟล์ผลลัพธ์จะถูกเก็บไว้ในโฟลเดอร์ที่คุณระบุ

### ขั้นตอนที่ 5: แสดงข้อความสำเร็จ

```csharp
Console.WriteLine("OpenDwfxFile executed successfully");
```

ข้อความคอนโซลง่าย ๆ จะบอกคุณว่าการแปลงเสร็จสมบูรณ์โดยไม่มีข้อผิดพลาด

## ปัญหาและเคล็ดลับทั่วไป

* **ไฟล์ไม่พบ** – ตรวจสอบพาธ `SourceDir` อีกครั้งและให้แน่ใจว่าชื่อไฟล์ตรงกันรวมถึงตัวพิมพ์ใหญ่‑เล็ก  
* **PDF ว่าง** – ตรวจสอบว่าไฟล์ DWFX มีข้อมูลเวกเตอร์จริง ๆ; บางเครื่องมือส่งออกอาจสร้างภาพวาดเปล่า  
* **ประสิทธิภาพ** – สำหรับภาพวาดขนาดใหญ่ ให้พิจารณาลด `PageWidth`/`PageHeight` หรือกำหนด `Resolution` ที่ต่ำลงใน `CadRasterizationOptions`

## คำถามที่พบบ่อย

### Q1: Aspose.CAD for .NET รองรับไฟล์ DWFX ทั้งหมดหรือไม่?

A1: Aspose.CAD for .NET รองรับรูปแบบ CAD จำนวนมากรวมถึง DWFX อย่างไรก็ตามควรตรวจสอบเอกสารเพื่อดูรายละเอียดความเข้ากันได้เฉพาะ

### Q2: จะหาเอกสารสำหรับ Aspose.CAD for .NET ได้ที่ไหน?

A2: เอกสารพร้อมให้บริการ [ที่นี่](https://reference.aspose.com/cad/net/)

### Q3: สามารถทดลองใช้ Aspose.CAD for .NET ก่อนซื้อได้หรือไม่?

A3: ใช่, คุณสามารถดาวน์โหลดเวอร์ชันทดลองฟรี [ที่นี่](https://releases.aspose.com/)

### Q4: จะขอรับลิขสิทธิ์ชั่วคราวสำหรับ Aspose.CAD for .NET ได้อย่างไร?

A4: สามารถขอรับลิขสิทธิ์ชั่วคราวได้ [ที่นี่](https://purchase.aspose.com/temporary-license/)

### Q5: ต้องการสนับสนุนหรือมีคำถามเพิ่มเติม?

A5: เยี่ยมชม [ฟอรั่ม Aspose.CAD](https://forum.aspose.com/c/cad/19) เพื่อขอความช่วยเหลือ

### Q6: สามารถประมวลผลไฟล์ DWFX หลายไฟล์พร้อมกันได้หรือไม่?

A6: ทำได้แน่นอน เพียงใส่ตรรกะการโหลดและบันทึกไว้ในลูป `foreach` ที่วนผ่านไฟล์ในไดเรกทอรี

### Q7: การแปลงจะคงเลเยอร์และสีไว้หรือไม่?

A7: ข้อมูลเวกเตอร์เช่นเลเยอร์และสีจะถูกเก็บไว้ใน PDF หากไฟล์ DWFX ต้นทางมีข้อมูลเหล่านั้น

---

**อัปเดตล่าสุด:** 2026-04-09  
**ทดสอบด้วย:** Aspose.CAD for .NET 24.11  
**ผู้เขียน:** Aspose  

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}