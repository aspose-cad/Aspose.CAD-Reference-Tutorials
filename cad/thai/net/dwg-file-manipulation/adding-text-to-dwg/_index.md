---
title: การเพิ่มข้อความลงในไฟล์ DWG ใน C# - บทช่วยสอน Aspose.CAD
linktitle: การเพิ่มข้อความลงในไฟล์ DWG ใน C #
second_title: Aspose.CAD .NET - รูปแบบไฟล์ CAD และ BIM
description: เรียนรู้วิธีเพิ่มข้อความลงในไฟล์ DWG โดยใช้ C# และ Aspose.CAD ปฏิบัติตามบทช่วยสอนทีละขั้นตอนนี้เพื่อการผสานรวมที่ราบรื่น สำรวจเอกสาร Aspose.CAD เพื่อดูคำแนะนำที่ครอบคลุม
weight: 14
url: /th/net/dwg-file-manipulation/adding-text-to-dwg/
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# การเพิ่มข้อความลงในไฟล์ DWG ใน C# - บทช่วยสอน Aspose.CAD

## การแนะนำ

ในขอบเขตไดนามิกของการออกแบบโดยใช้คอมพิวเตอร์ช่วย (CAD) และการพัฒนา .NET นั้น Aspose.CAD มีความโดดเด่นในฐานะเครื่องมืออันทรงพลังสำหรับจัดการไฟล์ DWG การเพิ่มข้อความลงในไฟล์ DWG เป็นข้อกำหนดทั่วไป และในบทช่วยสอนนี้ เราจะสำรวจวิธีการบรรลุเป้าหมายนี้โดยใช้ C# และ Aspose.CAD

## ข้อกำหนดเบื้องต้น

ก่อนที่จะเข้าสู่บทช่วยสอน ตรวจสอบให้แน่ใจว่าคุณมีสิ่งต่อไปนี้:

-  ไลบรารี Aspose.CAD: ดาวน์โหลดและติดตั้งไลบรารี Aspose.CAD จากไฟล์[ลิ้งค์ดาวน์โหลด](https://releases.aspose.com/cad/net/).

-  ไดเร็กทอรีเอกสาร: ตั้งค่าไดเร็กทอรีสำหรับเอกสารของคุณและจดบันทึกเส้นทางเป็น`MyDir`.

ตอนนี้ เรามาแบ่งกระบวนการออกเป็นขั้นตอนที่สามารถจัดการได้

## นำเข้าเนมสเปซ

ในโค้ด C# ของคุณ ให้รวมเนมสเปซที่จำเป็นเพื่อเข้าถึงฟังก์ชัน Aspose.CAD

```csharp
using System;
using System.Collections.Generic;
using System.Linq;
using System.Text;
using System.Threading.Tasks;
using Aspose.CAD;
using Aspose.CAD.FileFormats.Cad.CadObjects;
using Aspose.CAD.FileFormats.Cad.CadConsts;
using Aspose.CAD.FileFormats.Cad;
using Aspose.CAD.FileFormats.Cad.CadObjects.AttEntities;
using Aspose.CAD.ImageOptions;
```

## ขั้นตอนที่ 1: โหลดไฟล์ DWG

 โหลดไฟล์ DWG ลงในไฟล์`Image` วัตถุโดยใช้ไลบรารี Aspose.CAD

```csharp
string dwgPathToFile = MyDir + "SimpleEntites.dwg";
using (Image image = Image.Load(dwgPathToFile))
{
    // รหัสของคุณสำหรับขั้นตอนต่อไปอยู่ที่นี่
}
```

## ขั้นตอนที่ 2: สร้างวัตถุ CadText

 ยกตัวอย่าง`CadText` วัตถุเพื่อแสดงข้อความที่คุณต้องการเพิ่มลงในไฟล์ DWG

```csharp
CadText cadText = new CadText();
cadText.StyleType = "Standard";
cadText.DefaultValue = "Some custom text";
cadText.ColorId = 256;
cadText.LayerName = "0";
cadText.FirstAlignment.X = 47.90;
cadText.FirstAlignment.Y = 5.56;
cadText.TextHeight = 0.8;
cadText.ScaleX = 0.0;
```

## ขั้นตอนที่ 3: เพิ่มข้อความลงใน DWG

 เพิ่มที่สร้างขึ้น`CadText` คัดค้านไฟล์ DWG โดยใช้ Aspose.CAD

```csharp
CadImage cadImage = (CadImage)image;
cadImage.BlockEntities["*Model_Space"].AddEntity(cadText);
```

## ขั้นตอนที่ 4: กำหนดค่าตัวเลือก PDF

กำหนดค่าตัวเลือก PDF สำหรับบันทึกไฟล์ DWG ที่แก้ไขเป็น PDF

```csharp
PdfOptions pdfOptions = new PdfOptions();
CadRasterizationOptions cadRasterizationOptions = new CadRasterizationOptions();
pdfOptions.VectorRasterizationOptions = cadRasterizationOptions;
cadRasterizationOptions.DrawType = CadDrawTypeMode.UseObjectColor;
cadRasterizationOptions.PageHeight = 1600;
cadRasterizationOptions.PageWidth = 1600;
cadRasterizationOptions.Layouts = new string[] { "Model" };
```

## ขั้นตอนที่ 5: บันทึกเป็น PDF

บันทึกไฟล์ DWG ที่แก้ไขเป็น PDF พร้อมข้อความที่เพิ่ม

```csharp
image.Save(MyDir + "SimpleEntites_generated.pdf", pdfOptions);
```

ตอนนี้ คุณได้เพิ่มข้อความลงในไฟล์ DWG โดยใช้ C# และ Aspose.CAD เรียบร้อยแล้ว สำรวจคุณสมบัติและฟังก์ชันการทำงานเพิ่มเติมของ Aspose.CAD ได้ตามต้องการ เพื่อตอบสนองความต้องการด้านการปรับแต่ง CAD ของคุณ

## บทสรุป

ในบทช่วยสอนนี้ เราได้กล่าวถึงขั้นตอนสำคัญในการเพิ่มข้อความลงในไฟล์ DWG โดยใช้ C# และ Aspose.CAD การผสมผสานอันทรงพลังนี้เปิดโอกาสสำหรับการสร้างเอกสาร CAD แบบไดนามิกและแบบกำหนดเอง

## คำถามที่พบบ่อย

### คำถามที่ 1: Aspose.CAD เข้ากันได้กับไฟล์ DWG ทุกเวอร์ชันหรือไม่

A1: Aspose.CAD รองรับไฟล์ DWG หลากหลายเวอร์ชัน จึงมั่นใจได้ถึงความเข้ากันได้กับซอฟต์แวร์ CAD ต่างๆ

### คำถามที่ 2: ฉันสามารถเพิ่มเอนทิตีข้อความหลายรายการลงในไฟล์ DWG ไฟล์เดียวโดยใช้ Aspose.CAD ได้หรือไม่

A2: ได้ คุณสามารถเพิ่มเอนทิตีข้อความหลายรายการลงในไฟล์ DWG ได้โดยทำซ้ำขั้นตอนที่อธิบายไว้ในบทช่วยสอน

### คำถามที่ 3: ฉันจะเปลี่ยนแบบอักษรและสไตล์ของข้อความใน Aspose.CAD ได้อย่างไร

 A3: หากต้องการแก้ไขแบบอักษรและสไตล์ของข้อความ ให้ปรับคุณสมบัติของ`CadText` วัตถุก่อนที่จะเพิ่มลงในไฟล์ DWG

### คำถามที่ 4: มีข้อควรพิจารณาในการอนุญาตให้ใช้ Aspose.CAD ในโครงการเชิงพาณิชย์หรือไม่

 A4: ใช่ ตรวจสอบให้แน่ใจว่าปฏิบัติตามข้อกำหนดสิทธิ์การใช้งาน Aspose.CAD อ้างถึง[Aspose.CAD ซื้อ](https://purchase.aspose.com/buy) เพื่อดูรายละเอียด

### คำถามที่ 5: ฉันจะขอความช่วยเหลือหรือหารือเกี่ยวกับคำถามที่เกี่ยวข้องกับ Aspose.CAD ได้ที่ไหน

A5: เยี่ยมชม[ฟอรั่ม Aspose.CAD](https://forum.aspose.com/c/cad/19)เพื่อเชื่อมต่อกับชุมชนและรับการสนับสนุน
{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}
