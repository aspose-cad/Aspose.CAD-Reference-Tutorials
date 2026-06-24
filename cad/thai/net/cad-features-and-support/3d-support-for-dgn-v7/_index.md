---
date: 2026-03-24
description: เรียนรู้วิธีแปลง DGN เป็น PDF (และ PNG) พร้อมการสนับสนุน 3D สำหรับ DGN
  V7 ด้วย Aspose.CAD สำหรับ .NET – คู่มือขั้นตอนโดยละเอียด
linktitle: 3D Support for DGN V7
second_title: Aspose.CAD .NET - CAD and BIM File Format
title: แปลง DGN เป็น PDF (รองรับ 3 มิติ) ด้วย Aspose.CAD สำหรับ .NET
url: /th/net/cad-features-and-support/3d-support-for-dgn-v7/
weight: 10
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# แปลง DGN เป็น PDF (รองรับ 3D) ด้วย Aspose.CAD สำหรับ .NET

## บทนำ

ในกระบวนการทำงาน CAD สมัยใหม่ การ **แปลง DGN เป็น PDF** อย่างรวดเร็วและคงสภาพเรขาคณิต 3‑D ไว้เป็นสิ่งสำคัญ ไม่ว่าคุณจะสร้างเอกสาร, แชร์แบบออกแบบกับผู้ที่ไม่ได้ใช้ CAD, หรือเก็บโครงการไว้เป็นระยะยาว Aspose.CAD สำหรับ .NET จะมอบวิธีที่เชื่อถือได้ในการเปลี่ยนไฟล์ DGN V7 ให้เป็น PDF คุณภาพสูง (และแม้กระทั่ง PNG) ในบทแนะนำนี้เราจะเดินผ่านขั้นตอนที่จำเป็นทั้งหมดเพื่อเปิดใช้งานการสนับสนุน 3D และสร้าง PDF จากไฟล์ DGN

## คำตอบอย่างรวดเร็ว
- **บทเรียนนี้ครอบคลุมอะไร?** การเปิดใช้งานการสนับสนุน 3D และการแปลง DGN V7 เป็น PDF ด้วย Aspose.CAD สำหรับ .NET  
- **รูปแบบหลักที่ได้คืออะไร?** PDF (พร้อมการส่งออก PNG เป็นตัวเลือก)  
- **ต้องมีลิขสิทธิ์หรือไม่?** สามารถใช้รุ่นทดลองฟรีสำหรับการทดสอบ; ต้องมีลิขสิทธิ์เชิงพาณิชย์สำหรับการใช้งานจริง  
- **รองรับเวอร์ชัน .NET ใด?** .NET Framework 4.5+, .NET Core 3.1+, .NET 5/6+  
- **ใช้เวลาติดตั้งเท่าไหร่?** ประมาณ 10‑15 นาทีสำหรับการแปลงพื้นฐาน

## “convert DGN to PDF” คืออะไร?

การแปลง DGN เป็น PDF หมายถึงการเรนเดอร์ข้อมูลเวกเตอร์ที่เก็บอยู่ในไฟล์ MicroStation DGN ให้เป็นรูปแบบเอกสารพกพาที่สามารถดูได้บนอุปกรณ์ใดก็ได้โดยไม่ต้องใช้ซอฟต์แวร์ CAD พิเศษ ด้วยเอนจินการเรสเตอร์ 3‑D ของ Aspose.CAD การแปลงจะคงการจัดวาง, สี, และสัญญาณความลึกไว้ ทำให้ได้ภาพที่ตรงกับต้นฉบับ

## ทำไมต้องใช้ Aspose.CAD สำหรับการแปลงนี้?

- **การเรสเตอร์ 3‑D เต็มรูปแบบ** – คงข้อมูลความลึกและการจัดวางไว้  
- **ไม่มีการพึ่งพาภายนอก** – ไลบรารี .NET แท้ ๆ ไม่ต้องใช้ MicroStation  
- **หลายรูปแบบผลลัพธ์** – PDF, PNG, JPEG, TIFF ฯลฯ (คีย์เวิร์ดรอง *convert dgn to png* รองรับโดยตรง)  
- **ข้ามแพลตฟอร์ม** – ทำงานบน Windows, Linux, และ macOS

## ข้อกำหนดเบื้องต้น

ก่อนเริ่มทำงาน ให้ตรวจสอบว่าคุณมีสิ่งต่อไปนี้:

- Aspose.CAD สำหรับ .NET ติดตั้งแล้ว คุณสามารถดาวน์โหลดได้จาก [หน้าดาวน์โหลด Aspose.CAD สำหรับ .NET](https://releases.aspose.com/cad/net/)  
- ไฟล์ DGN V7 ที่ต้องการประมวลผล  
- สภาพแวดล้อมการพัฒนา .NET (Visual Studio, VS Code หรือ CLI) คำแนะนำการติดตั้งมีใน [เอกสาร .NET](https://docs.microsoft.com/en-us/dotnet/core/install/)

## นำเข้า Namespaces

```csharp
using System;
using System.Collections.Generic;
using System.Linq;
using System.Text;
using System.Threading.Tasks;
using Aspose.CAD;
```

Namespaces เหล่านี้ทำให้คุณเข้าถึงคลาสหลักของ Aspose.CAD และยูทิลิตี้มาตรฐานของ .NET

## ขั้นตอนที่ 1: ตั้งค่าสภาพแวดล้อม

กำหนดตำแหน่งที่ไฟล์ DGN ต้นฉบับอยู่และที่ที่ต้องการบันทึก PDF ผลลัพธ์

```csharp
string MyDir = "Your Document Directory";
string sourceFilePath = MyDir + "Nikon_D90_Camera.dgn";
```

> **เคล็ดลับ:** ใช้ `Path.Combine` เพื่อสร้างเส้นทางที่เป็นอิสระต่อแพลตฟอร์ม

## ขั้นตอนที่ 2: โหลดไฟล์ DGN

สร้างอินสแตนซ์ `DgnImage` โดยโหลดไฟล์ด้วย `Image.Load` ขั้นตอนนี้เตรียมข้อมูล CAD สำหรับการเรสเตอร์

```csharp
using (DgnImage dgnImage = (DgnImage)Image.Load(sourceFilePath))
{
    // Code snippet continues...
}
```

## ขั้นตอนที่ 3: กำหนดค่าตัวเลือกการส่งออก

ตั้งค่า `PdfOptions` ร่วมกับ `CadRasterizationOptions` ที่นี่คุณสามารถควบคุมขนาดหน้า, พื้นหลัง, และเลเอาต์ (มุมมอง) ที่ต้องการส่งออก

```csharp
var options = new PdfOptions
{
    VectorRasterizationOptions = new CadRasterizationOptions
    {
        PageWidth = 1500,
        PageHeight = 1500,
        CenterDrawing = true,
        AutomaticLayoutsScaling = true,
        BackgroundColor = Color.Black,
        Layouts = new string[] { "1", "2", "3", "9" } // Export specific views
    }
};
```

หากต้องการ **convert DGN to PNG** แทน ให้เปลี่ยน `PdfOptions` เป็น `PngOptions` โดยคงการตั้งค่าเรสเตอร์เดิมไว้

## ขั้นตอนที่ 4: บันทึกผลลัพธ์

สุดท้ายให้เขียนผลลัพธ์ที่เรสเตอร์แล้วไปยังตำแหน่งที่กำหนด

```csharp
string outFile = "Your Output Directory"; // Specify the output directory
dgnImage.Save(outFile, options);
```

หลังจากรันเสร็จ คุณจะพบไฟล์ PDF (หรือ PNG หากเปลี่ยนตัวเลือก) ที่แสดงภาพ 3‑D ของแบบ DGN ต้นฉบับอย่างแม่นยำ

## ปัญหาทั่วไป & เคล็ดลับ

- **ไม่มีเลเอาต์:** ตรวจสอบให้แน่ใจว่าชื่อเลเอาต์ใน `Layouts` ตรงกับในไฟล์ DGN มิฉะนั้นจะถูกละเว้น  
- **ไฟล์ขนาดใหญ่:** เพิ่มค่า `PageWidth`/`PageHeight` อย่างค่อยเป็นค่อยไปเพื่อหลีกเลี่ยงการใช้หน่วยความจำสูง  
- **ความแม่นยำของสี:** หากพื้นหลังดูมืด ให้ตรวจสอบว่า `BackgroundColor` ตั้งค่าเป็นค่าที่ต้องการ (เช่น `Color.White`)

## สรุป

คุณได้เรียนรู้วิธี **แปลง DGN เป็น PDF** พร้อมการสนับสนุน 3‑D อย่างเต็มที่ด้วย Aspose.CAD สำหรับ .NET แล้ว กระบวนการนี้สามารถนำไปผสานในพายป์ไลน์อัตโนมัติ, ยูทิลิตี้เดสก์ท็อป, หรือบริการเว็บเพื่อให้การแสดงผล CAD แก่ผู้ชมทุกประเภท

## คำถามที่พบบ่อย

### Q1: สามารถประมวลผลไฟล์ DGN หลายไฟล์พร้อมกันด้วยวิธีนี้ได้หรือไม่?

A1: ได้ คุณสามารถปรับโค้ดให้ทำงานกับหลายไฟล์ในลูปหรือเป็นส่วนหนึ่งของระบบประมวลผลแบบแบตช์

### Q2: ฟอร์แมตการส่งออกอื่น ๆ ที่ Aspose.CAD สำหรับ .NET รองรับมีอะไรบ้าง?

A2: Aspose.CAD สำหรับ .NET รองรับฟอร์แมตการส่งออกหลายรูปแบบ รวมถึง PDF, PNG, JPG และอื่น ๆ ดูรายละเอียดใน [documentation](https://reference.aspose.com/cad/net/)

### Q3: Aspose.CAD สำหรับ .NET เข้ากันได้กับเวอร์ชัน .NET Core ล่าสุดหรือไม่?

A3: ใช่ Aspose.CAD สำหรับ .NET ถูกออกแบบให้เข้ากันได้กับเวอร์ชัน .NET Core ล่าสุด เพียงตรวจสอบว่าคุณติดตั้งเวอร์ชันที่เหมาะสมในสภาพแวดล้อมของคุณ

### Q4: สามารถปรับแต่งการตั้งค่าการส่งออกเพิ่มเติมตามความต้องการเฉพาะของฉันได้หรือไม่?

A4: แน่นอน! โค้ดตัวอย่างที่ให้เป็นจุดเริ่มต้น คุณสามารถสำรวจตัวเลือกและการกำหนดค่าเพิ่มเติมได้ใน [Aspose.CAD documentation](https://reference.aspose.com/cad/net/)

### Q5: จะหาแหล่งช่วยเหลือหรือแบ่งปันประสบการณ์เกี่ยวกับ Aspose.CAD สำหรับ .NET ได้จากที่ไหน?

A5: เข้าร่วมชุมชน Aspose.CAD ได้ที่ [forum](https://forum.aspose.com/c/cad/19) เพื่อโต้ตอบกับนักพัฒนาคนอื่นและขอความช่วยเหลือ

---

**อัปเดตล่าสุด:** 2026-03-24  
**ทดสอบกับ:** Aspose.CAD 24.11 สำหรับ .NET  
**ผู้เขียน:** Aspose  

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}