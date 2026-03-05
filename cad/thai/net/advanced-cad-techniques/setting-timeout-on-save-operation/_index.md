---
date: 2026-03-05
description: เรียนรู้วิธีตั้งค่า timeout สำหรับการบันทึกขณะแปลง DWG เป็น PDF ด้วย
  Aspose.CAD สำหรับ .NET เพื่อเพิ่มประสิทธิภาพและการควบคุมในแอปพลิเคชัน .NET ของคุณ.
linktitle: Setting Timeout on Save Operation
second_title: Aspose.CAD .NET - CAD and BIM File Format
title: วิธีตั้งค่า Timeout ในการบันทึก - บทแนะนำ Aspose.CAD
url: /th/net/advanced-cad-techniques/setting-timeout-on-save-operation/
weight: 12
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# วิธีตั้งค่า Timeout ในการบันทึกการทำงาน - บทแนะนำ Aspose.CAD

## บทนำ

ในคู่มือนี้ คุณจะได้เรียนรู้ **วิธีตั้งค่า timeout** สำหรับการบันทึก CAD ซึ่งเป็นเทคนิคที่ช่วยให้การแปลงที่ใช้เวลานานไม่กลายเป็นกระบวนการที่ไม่ตอบสนอง การจัดการ timeout มีประโยชน์อย่างยิ่งเมื่อคุณ **แปลง DWG เป็น PDF** หรือ **ส่งออก CAD PDF** ในงานแบบแบชหรือบริการเว็บ Aspose.CAD สำหรับ .NET มี API ที่สะอาดตาให้คุณควบคุมการบันทึกขณะยังคงใช้ประโยชน์จากเอนจินการเรสเตอร์ไลเซชันที่ทรงพลัง

## คำตอบอย่างรวดเร็ว
- **Timeout ควบคุมอะไร?** จะยกเลิกการบันทึก/ส่งออกหากทำงานนานเกินช่วงเวลาที่กำหนด  
- **ฟอร์แมตใดได้ประโยชน์มากที่สุด?** การแปลงไฟล์ DWG ขนาดใหญ่เป็น PDF หรือภาพเรสเตอร์ที่เวลาการประมวลผลอาจแตกต่างกัน  
- **ต้องมีลิขสิทธิ์หรือไม่?** จำเป็นต้องมีลิขสิทธิ์ Aspose.CAD ที่ถูกต้องสำหรับการใช้งานในผลิตภัณฑ์; เวอร์ชันทดลองฟรีใช้ได้สำหรับการประเมินผล  
- **สามารถปรับระยะเวลาได้หรือไม่?** ได้ — เพียงเปลี่ยนค่า `Thread.Sleep` (เป็นมิลลิวินาที) ให้เหมาะกับสถานการณ์ของคุณ  
- **วิธีนี้รองรับ async หรือไม่?** ตัวอย่างใช้ `Task.Factory.StartNew` ทำให้ง่ายต่อการผสานเข้ากับ workflow แบบ async  

## “วิธีตั้งค่า timeout” ในบริบทของการบันทึก CAD คืออะไร?
การตั้งค่า timeout หมายถึงการแนบ `InterruptionToken` ไปยังตัวเลือกการบันทึกและทำการขัดจังหวะหลังจากช่วงเวลาที่กำหนดไว้ล่วงหน้า ซึ่งช่วยป้องกันไม่ให้การทำงานค้างโดยไม่มีที่สิ้นสุด ทำให้คุณได้ประสิทธิภาพที่คาดการณ์ได้และการจัดการทรัพยากรที่ดียิ่งขึ้น

## ทำไมต้องใช้ Aspose.CAD เพื่อแปลง DWG เป็น PDF พร้อม timeout?
- **ความน่าเชื่อถือ:** รับประกันว่าการแปลงที่ล้นจะไม่บล็อกบริการของคุณ  
- **ความสามารถในการขยาย:** สามารถประมวลผลไฟล์หลายไฟล์พร้อมกันโดยไม่ต้องกังวลว่าไฟล์เดียวจะทำให้ไพป์ไลน์หยุดชะงัก  
- **คุณภาพ:** รักษาการเรสเตอร์ไลเซชันคุณภาพสูงของ Aspose.CAD พร้อมเพิ่มการควบคุมด้านความปลอดภัย  

## ข้อกำหนดเบื้องต้น

ก่อนเริ่มทำงาน โปรดตรวจสอบว่าคุณมีสิ่งต่อไปนี้:

- **Aspose.CAD for .NET** – รวมไว้ในโปรเจกต์ของคุณแล้ว คุณสามารถดาวน์โหลดได้จาก [ที่นี่](https://releases.aspose.com/cad/net/)  
- **Document Directory** – โฟลเดอร์ที่เก็บไฟล์ DWG ต้นฉบับและไฟล์ PDF ผลลัพธ์  

## นำเข้า Namespaces

ก่อนอื่น ให้นำเข้า namespaces ที่ให้คลาสที่เราต้องการสำหรับการเรสเตอร์ไลเซชัน, ตัวเลือก PDF, และกลไกการขัดจังหวะ

```csharp
using Aspose.CAD.ImageOptions;
using System;
using System.Threading;
using System.Threading.Tasks;
```

## วิธีตั้งค่า Timeout ในการบันทึกการทำงาน

ต่อไปนี้เป็นขั้นตอนแบบละเอียดแต่ละขั้นตอนประกอบด้วยคำอธิบายสั้น ๆ ตามด้วยบล็อกโค้ดต้นฉบับ (ไม่เปลี่ยนแปลง)

### ขั้นตอนที่ 1: โหลด CAD Drawing

เราจะโหลดไฟล์ DWG ต้นฉบับจากไดเรกทอรีที่กำหนด เมธอด `Image.Load` จะคืนค่าอ็อบเจกต์ `Image` ที่แสดงถึงการวาด CAD

```csharp
// Example: Loading CAD Drawing
string SourceDir = "Your Document Directory";
string OutputDir = "Your Document Directory";

using (Image cadDrawing = Image.Load(SourceDir + "Drawing11.dwg"))
{
    // Code for subsequent steps will be placed here
}
```

### ขั้นตอนที่ 2: ตั้งค่า Rasterization Options

กำหนดตัวเลือกการเรสเตอร์ไลเซชันเพื่อให้ PDF ที่ส่งออกมีขนาดเท่ากับภาพวาดต้นฉบับ ที่นี่คุณสามารถควบคุมความกว้าง, ความสูงของหน้าและการตั้งค่าเรนเดอร์อื่น ๆ

```csharp
// Example: Configuring Rasterization Options
var rasterizationOptions = new CadRasterizationOptions();
rasterizationOptions.PageWidth = cadDrawing.Size.Width;
rasterizationOptions.PageHeight = cadDrawing.Size.Height;
```

### ขั้นตอนที่ 3: สร้าง PDF Options (Export CAD PDF)

สร้างอินสแตนซ์ `PdfOptions` และแนบการตั้งค่าเรสเตอร์ไลเซชัน วัตถุนี้จะถูกส่งต่อให้เมธอด `Save` เพื่อสร้างไฟล์ PDF จากไฟล์ DWG

```csharp
// Example: Creating PDF Options
PdfOptions CADf = new PdfOptions();
CADf.VectorRasterizationOptions = rasterizationOptions;
```

### ขั้นตอนที่ 4: ใช้กลไก Timeout

เราใช้ `InterruptionTokenSource` เพื่อรับโทเคนที่สามารถขัดจังหวะการบันทึกได้ งานพื้นหลังทำการส่งออก ในขณะที่เธรดหลักจะหยุดพักตามระยะเวลา timeout ที่ต้องการ (เช่น 10 วินาที) หลังจากหยุดพัก เราเรียก `Interrupt()` เพื่อยกเลิกการทำงานหากยังคงทำงานอยู่

```csharp
// Example: Implementing Timeout Mechanism
using (var its = new InterruptionTokenSource())
{
    CADf.InterruptionToken = its.Token;

    var exportTask = Task.Factory.StartNew(() =>
    {
        cadDrawing.Save(OutputDir + "PutTimeoutOnSave_out.pdf", CADf);
    });

    Thread.Sleep(10000); // Set your desired timeout duration in milliseconds
    its.Interrupt();

    exportTask.Wait();
}
```

### ขั้นตอนที่ 5: สรุปและยืนยัน

หลังจากการส่งออก (หรือการขัดจังหวะ) ให้พิมพ์ข้อความยืนยันลงคอนโซล ในแอปพลิเคชันจริงคุณอาจบันทึกผลลัพธ์หรือส่งเหตุการณ์ต่อไป

```csharp
// Example: Finalizing and Confirming
Console.WriteLine("PutTimeoutOnSave executed successfully");
```

## ปัญหาที่พบบ่อยและวิธีแก้

| ปัญหา | สาเหตุ | วิธีแก้ |
|-------|-------|--------|
| การส่งออกค้างไม่หยุด | ไม่ได้แนบ InterruptionToken | ตรวจสอบให้แน่ใจว่า `CADf.InterruptionToken = its.Token;` ถูกตั้งค่าก่อนเริ่มงาน |
| PDF ว่างหรือเสียหาย | เส้นทางไดเรกทอรีเอาต์พุตไม่ถูกต้อง | ตรวจสอบว่า `OutputDir` ลงท้ายด้วยตัวคั่นเส้นทางและชื่อไฟล์ถูกต้อง |
| Timeout สั้นเกินไปทำให้ยกเลิกก่อนเวลา | ค่า `Thread.Sleep` ต่ำเกินไปสำหรับไฟล์ขนาดใหญ่ | เพิ่มระยะเวลาการหยุดพักหรือคำนวณ timeout แบบปรับตามขนาดไฟล์ |

## คำถามที่พบบ่อย

**Q1: สามารถปรับระยะเวลา timeout ได้หรือไม่?**  
A: แน่นอน เพียงเปลี่ยนค่าที่ส่งให้ `Thread.Sleep` (เป็นมิลลิวินาที) ให้สอดคล้องกับความคาดหวังด้านประสิทธิภาพของคุณ  

**Q2: มีตัวเลือกอื่นสำหรับการเรสเตอร์ไลเซชันหรือไม่?**  
A: มี `CadRasterizationOptions` มีคุณสมบัติเช่น `Resolution`, `BackgroundColor` และ `DrawType` เพื่อปรับแต่งผลลัพธ์ PDF อย่างละเอียด  

**Q3: จะจัดการกับการขัดจังหวะในแอปพลิเคชันอย่างไร?**  
A: ใช้คลาส `InterruptionToken` และ `InterruptionTokenSource` ตามที่แสดง พวกมันให้วิธีที่ปลอดภัยต่อเธรดในการยกเลิกการทำงานที่ใช้เวลานาน  

**Q4: Aspose.CAD รองรับไฟล์ CAD 2D และ 3D หรือไม่?**  
A: รองรับรูปแบบ 2D และ 3D หลากหลาย รวมถึง DWG, DXF, DGN และอื่น ๆ  

**Q5: จะหาแหล่งช่วยเหลือหรือชุมชนเพิ่มเติมได้จากที่ไหน?**  
A: เยี่ยมชม [ฟอรั่ม Aspose.CAD](https://forum.aspose.com/c/cad/19) เพื่อเข้าร่วมการสนทนาชุมชน, ตัวอย่างโค้ด, และเคล็ดลับการแก้ปัญหา  

## สรุป

โดยทำตามขั้นตอนข้างต้น คุณจะรู้ **วิธีตั้งค่า timeout** สำหรับการบันทึก CAD อย่างมั่นใจ ทำให้คุณสามารถ **แปลง DWG เป็น PDF** หรือ **ส่งออก CAD PDF** ได้อย่างเชื่อถือได้โดยไม่ต้องกังวลว่าจะเกิดกระบวนการที่ไม่ตอบสนอง นำรูปแบบนี้ไปใช้ในตัวแปลงแบบแบช, บริการเว็บ หรือไพป์ไลน์อัตโนมัติใด ๆ ที่ต้องการความคาดการณ์ได้

---

**อัปเดตล่าสุด:** 2026-03-05  
**ทดสอบด้วย:** Aspose.CAD 24.12 for .NET  
**ผู้เขียน:** Aspose  

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}