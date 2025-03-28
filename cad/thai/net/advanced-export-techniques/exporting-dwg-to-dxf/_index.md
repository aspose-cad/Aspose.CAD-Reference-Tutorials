---
title: การส่งออก DWG เป็นรูปแบบ DXF ใน C# - บทช่วยสอน Aspose.CAD
linktitle: ส่งออก DWG เป็นรูปแบบ DXF ใน C #
second_title: Aspose.CAD .NET - รูปแบบไฟล์ CAD และ BIM
description: ปลดล็อกการจัดการไฟล์ CAD ใน C# ด้วย Aspose.CAD เรียนรู้การส่งออก DWG ไปยัง DXF ได้อย่างง่ายดาย ปฏิบัติตามคำแนะนำทีละขั้นตอนของเราเพื่อการบูรณาการที่ราบรื่น
weight: 10
url: /th/net/advanced-export-techniques/exporting-dwg-to-dxf/
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# การส่งออก DWG เป็นรูปแบบ DXF ใน C# - บทช่วยสอน Aspose.CAD

## การแนะนำ

หากคุณเป็นนักพัฒนา .NET ที่กำลังมองหาโซลูชันที่มีประสิทธิภาพสำหรับจัดการไฟล์ CAD Aspose.CAD คือเครื่องมือที่ใช่สำหรับคุณ ในบทช่วยสอนทีละขั้นตอนนี้ เราจะแนะนำคุณตลอดขั้นตอนการส่งออกไฟล์ DWG เป็นรูปแบบ DXF โดยใช้ C# กับ Aspose.CAD

## ข้อกำหนดเบื้องต้น

ก่อนที่จะเข้าสู่บทช่วยสอน ตรวจสอบให้แน่ใจว่าคุณมีข้อกำหนดเบื้องต้นต่อไปนี้:

1.  ไลบรารี Aspose.CAD: ดาวน์โหลดและติดตั้งไลบรารี Aspose.CAD จาก[ลิงค์นี้](https://releases.aspose.com/cad/net/).

2. สภาพแวดล้อมการพัฒนา: ตั้งค่าสภาพแวดล้อมการพัฒนา C# เช่น Visual Studio

3. ไฟล์ DWG ตัวอย่าง: เตรียมไฟล์ DWG ตัวอย่างที่คุณต้องการส่งออก สำหรับบทช่วยสอนนี้ เราจะใช้ไฟล์ชื่อ "Line.dwg" ในไดเร็กทอรี "Your Document Directory"

## นำเข้าเนมสเปซ

ในโปรเจ็กต์ C# ของคุณ ให้รวมเนมสเปซที่จำเป็นสำหรับการทำงานกับ Aspose.CAD:

```csharp
using Aspose.CAD.FileFormats.Cad;
using System;
using System.Collections.Generic;
using System.Linq;
using System.Text;
```

## ขั้นตอนที่ 1: โหลดไฟล์ DWG

เริ่มต้นด้วยการโหลดไฟล์ DWG ลงในแอปพลิเคชัน C# ของคุณ นี่คือข้อมูลโค้ดเพื่อให้บรรลุเป้าหมายนี้:

```csharp
string MyDir = "Your Document Directory";
string inputFile = MyDir + "Line.dwg";
using (var cadImage = (CadImage)Image.Load(inputFile))
{
    //รหัสของคุณสำหรับขั้นตอนต่อไปจะอยู่ที่นี่
}
```

## ขั้นตอนที่ 2: บันทึกเป็น DXF

เมื่อโหลดไฟล์ DWG แล้ว ขั้นตอนต่อไปคือบันทึกเป็นไฟล์ DXF เพิ่มรหัสต่อไปนี้ภายในบล็อกการใช้ก่อนหน้า:

```csharp
string outFile = MyDir + "Line_19.2.dxf";
cadImage.Save(outFile);
```

## บทสรุป

ยินดีด้วย! คุณได้ส่งออกไฟล์ DWG เป็นรูปแบบ DXF โดยใช้ Aspose.CAD ใน C# เรียบร้อยแล้ว กระบวนการที่เรียบง่ายแต่ทรงพลังนี้เปิดโลกแห่งความเป็นไปได้สำหรับการจัดการไฟล์ CAD ในแอปพลิเคชันของคุณ

## คำถามที่พบบ่อย

### คำถามที่ 1: Aspose.CAD เข้ากันได้กับรูปแบบไฟล์ CAD ล่าสุดหรือไม่

ตอบ 1: ใช่ Aspose.CAD ได้รับการอัปเดตเป็นประจำเพื่อให้แน่ใจว่าเข้ากันได้กับรูปแบบไฟล์ CAD ล่าสุด

### คำถามที่ 2: ฉันสามารถใช้ Aspose.CAD ในโครงการเชิงพาณิชย์ของฉันได้หรือไม่

 A2: แน่นอน! Aspose.CAD มาพร้อมกับตัวเลือกสิทธิ์การใช้งานสำหรับการใช้งานส่วนบุคคลและเชิงพาณิชย์ เยี่ยม[ลิงค์นี้](https://purchase.aspose.com/buy) เพื่อดูรายละเอียด

### คำถามที่ 3: มีการทดลองใช้ฟรีหรือไม่?

 A3: ได้ คุณสามารถสำรวจ Aspose.CAD ได้ด้วยการทดลองใช้ฟรี เยี่ยม[ลิงค์นี้](https://releases.aspose.com/) ที่จะเริ่มต้น.

### คำถามที่ 4: ฉันจะหาเอกสารโดยละเอียดสำหรับ Aspose.CAD ได้ที่ไหน

 A4: โปรดดูเอกสารประกอบที่[ลิงค์นี้](https://reference.aspose.com/cad/net/) เพื่อรับคำแนะนำอย่างครอบคลุม

### Q5: ต้องการความช่วยเหลือหรือมีคำถามเฉพาะเจาะจง?

 A5: เยี่ยมชมฟอรั่มชุมชน Aspose.CAD[ที่นี่](https://forum.aspose.com/c/cad/19)สำหรับความช่วยเหลือจากผู้เชี่ยวชาญและการสนับสนุนจากชุมชน
{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}
