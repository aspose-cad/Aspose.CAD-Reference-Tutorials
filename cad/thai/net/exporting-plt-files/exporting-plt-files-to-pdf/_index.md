---
title: การส่งออกไฟล์ PLT เป็น PDF - คู่มือ Aspose.CAD
linktitle: การส่งออกไฟล์ PLT เป็น PDF
second_title: Aspose.CAD .NET - รูปแบบไฟล์ CAD และ BIM
description: แปลงไฟล์ PLT เป็น PDF ได้อย่างง่ายดายโดยใช้ Aspose.CAD สำหรับ .NET ปฏิบัติตามคำแนะนำทีละขั้นตอนของเราเพื่อการบูรณาการที่ราบรื่นและผลลัพธ์ที่เชื่อถือได้
weight: 11
url: /th/net/exporting-plt-files/exporting-plt-files-to-pdf/
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# การส่งออกไฟล์ PLT เป็น PDF - คู่มือ Aspose.CAD

ในขอบเขตแบบไดนามิกของการออกแบบโดยใช้คอมพิวเตอร์ช่วย (CAD) ความสามารถในการแปลงไฟล์ PLT เป็นรูปแบบ PDF ได้อย่างราบรื่นถือเป็นทักษะที่มีคุณค่า Aspose.CAD สำหรับ .NET ช่วยให้นักพัฒนาสามารถทำงานนี้ให้สำเร็จได้อย่างง่ายดาย ในบทช่วยสอนนี้ เราจะอธิบายกระบวนการทีละขั้นตอน เพื่อให้มั่นใจในความชัดเจนและความเข้าใจทุกครั้ง

## ข้อกำหนดเบื้องต้น

ก่อนที่เราจะเจาะลึกบทช่วยสอน ตรวจสอบให้แน่ใจว่าคุณมีข้อกำหนดเบื้องต้นต่อไปนี้:

1.  Aspose.CAD สำหรับไลบรารี .NET: ตรวจสอบให้แน่ใจว่าคุณได้ติดตั้งไลบรารี Aspose.CAD แล้ว คุณสามารถดาวน์โหลดได้[ที่นี่](https://releases.aspose.com/cad/net/).

2. สภาพแวดล้อมการพัฒนา: เตรียมสภาพแวดล้อมการพัฒนา .NET ที่ใช้งานได้ให้พร้อม

## นำเข้าเนมสเปซ

ในโปรเจ็กต์ .NET ของคุณ ให้เริ่มด้วยการนำเข้าเนมสเปซที่จำเป็น:

```csharp
using Aspose.CAD.FileFormats.Cad;
using Aspose.CAD.FileFormats.Cad.CadConsts;
using Aspose.CAD.FileFormats.Cad.CadObjects;
using System;
using System.Collections.Generic;
using System.Linq;
using System.Text;
using static Aspose.CAD.Examples.CSharp.DWG_Drawings.SupportMLeaderEntityForDWGFormat;
using Aspose.CAD.ImageOptions;
```

เนมสเปซเหล่านี้จะจัดเตรียมคลาสและฟังก์ชันที่จำเป็นสำหรับการจัดการการทำงานของ CAD

## ขั้นตอนที่ 1: ตั้งค่าไดเร็กทอรีเอกสาร

เริ่มต้นด้วยการกำหนดเส้นทางไปยังไดเร็กทอรีเอกสารของคุณในโค้ดของคุณ:

```csharp
string MyDir = "Your Document Directory";
```

แทนที่ "Your Document Directory" ด้วยเส้นทางจริงไปยังเอกสารของคุณ

## ขั้นตอนที่ 2: โหลดไฟล์ PLT

โหลดไฟล์ PLT ลงในอิมเมจ CAD โดยใช้ข้อมูลโค้ดต่อไปนี้:

```csharp
string sourceFilePath = MyDir + "50states.plt";

using (Image cadImage = Image.Load(sourceFilePath))
{
    // รหัสของคุณอยู่ที่นี่
}
```

## ขั้นตอนที่ 3: กำหนดค่าตัวเลือกการแรสเตอร์

กำหนดค่าตัวเลือกการแรสเตอร์สำหรับการส่งออกเป็น PDF ตั้งค่าขนาดหน้า ประเภทการวาด และสีพื้นหลัง:

```csharp
CadRasterizationOptions options = new CadRasterizationOptions
{
    PageHeight = 1600,
    PageWidth = 1600,
    DrawType = CadDrawTypeMode.UseObjectColor,
    BackgroundColor = Color.White
};
```

## ขั้นตอนที่ 4: ตั้งค่าตัวเลือก PDF

กำหนดตัวเลือก PDF และเชื่อมโยงกับตัวเลือกการแรสเตอร์ที่ตั้งไว้ก่อนหน้านี้:

```csharp
PdfOptions pdfOptions = new PdfOptions();
pdfOptions.VectorRasterizationOptions = options;
```

## ขั้นตอนที่ 5: บันทึกเป็น PDF

บันทึกรูปภาพ CAD เป็นไฟล์ PDF:

```csharp
cadImage.Save(MyDir + "50states.pdf", pdfOptions);
```

## บทสรุป

ในบทช่วยสอนนี้ เราได้อธิบายขั้นตอนการส่งออกไฟล์ PLT เป็น PDF โดยใช้ Aspose.CAD สำหรับ .NET แล้ว ไลบรารีอเนกประสงค์นี้ทำให้การทำงานของ CAD ง่ายขึ้น ทำให้เป็นเครื่องมืออันล้ำค่าสำหรับนักพัฒนาที่ต้องการการแปลงไฟล์ที่มีประสิทธิภาพและเชื่อถือได้

## คำถามที่พบบ่อย

### คำถามที่ 1: ฉันสามารถใช้ Aspose.CAD สำหรับ .NET ในเว็บแอปพลิเคชันของฉันได้หรือไม่

ตอบ 1: ใช่ Aspose.CAD สำหรับ .NET เข้ากันได้กับทั้งเดสก์ท็อปและเว็บแอปพลิเคชัน

### คำถามที่ 2: Aspose.CAD สำหรับ .NET มีรุ่นทดลองใช้ฟรีหรือไม่

 A2: แน่นอน คุณสามารถทดลองใช้งานฟรีได้[ที่นี่](https://releases.aspose.com/).

### คำถามที่ 3: ฉันจะรับการสนับสนุนสำหรับ Aspose.CAD สำหรับ .NET ได้อย่างไร

 A3: เยี่ยมชม[ฟอรั่ม Aspose.CAD](https://forum.aspose.com/c/cad/19) สำหรับการสนับสนุนและคำแนะนำจากชุมชน

### คำถามที่ 4: Aspose.CAD รองรับไฟล์รูปแบบใดบ้าง

A4: Aspose.CAD รองรับรูปแบบ CAD ที่หลากหลาย รวมถึง DWG, DXF และ PLT

### คำถามที่ 5: ฉันจะหาเอกสารโดยละเอียดสำหรับ Aspose.CAD สำหรับ .NET ได้ที่ไหน

 A5: โปรดดูที่[เอกสาร Aspose.CAD](https://reference.aspose.com/cad/net/) เพื่อข้อมูลเชิงลึก
{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}
