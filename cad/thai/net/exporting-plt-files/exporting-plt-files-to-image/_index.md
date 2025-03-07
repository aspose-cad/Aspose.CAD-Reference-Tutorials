---
title: การส่งออกไฟล์ PLT ไปยังรูปภาพ - บทช่วยสอน Aspose.CAD
linktitle: การส่งออกไฟล์ PLT ไปยังรูปภาพ
second_title: Aspose.CAD .NET - รูปแบบไฟล์ CAD และ BIM
description: แปลงไฟล์ PLT เป็นรูปภาพได้อย่างง่ายดายโดยใช้ Aspose.CAD สำหรับ .NET สำรวจตัวเลือกที่ยืดหยุ่นและการผสานรวมที่ราบรื่นสำหรับความต้องการในการจัดการไฟล์ CAD ของคุณ
weight: 10
url: /th/net/exporting-plt-files/exporting-plt-files-to-image/
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# การส่งออกไฟล์ PLT ไปยังรูปภาพ - บทช่วยสอน Aspose.CAD

## การแนะนำ

ยินดีต้อนรับสู่บทช่วยสอนที่ครอบคลุมเกี่ยวกับการส่งออกไฟล์ PLT ไปยังรูปภาพโดยใช้ Aspose.CAD สำหรับ .NET! หากคุณต้องการแปลงไฟล์ PLT เป็นรูปแบบรูปภาพต่างๆ ได้อย่างราบรื่น คุณมาถูกที่แล้ว Aspose.CAD สำหรับ .NET มอบคุณสมบัติอันทรงพลังและความยืดหยุ่นสำหรับการจัดการไฟล์ CAD ที่มีประสิทธิภาพ และในบทช่วยสอนนี้ เราจะแนะนำคุณตลอดกระบวนการทีละขั้นตอน

## ข้อกำหนดเบื้องต้น

ก่อนที่เราจะเจาะลึกบทช่วยสอน ตรวจสอบให้แน่ใจว่าคุณมีข้อกำหนดเบื้องต้นต่อไปนี้:

-  Aspose.CAD สำหรับ .NET: ตรวจสอบให้แน่ใจว่าคุณได้ติดตั้งไลบรารี Aspose.CAD แล้ว คุณสามารถดาวน์โหลดได้จาก[ที่นี่](https://releases.aspose.com/cad/net/).

-  ไดเร็กทอรีเอกสาร: ตั้งค่าไดเร็กทอรีสำหรับเอกสารของคุณและจดบันทึกเส้นทาง ซึ่งก็จะเรียกกันว่า`MyDir`ในตัวอย่างโค้ด

ตอนนี้เรามาเริ่มด้วยบทช่วยสอนกันดีกว่า

## นำเข้าเนมสเปซ

เริ่มต้นด้วยการนำเข้าเนมสเปซที่จำเป็นในโปรเจ็กต์ .NET ของคุณเพื่อเข้าถึงฟังก์ชัน Aspose.CAD เพิ่มบรรทัดต่อไปนี้ที่จุดเริ่มต้นของโค้ดของคุณ:

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

## ขั้นตอนที่ 1: โหลดไฟล์ PLT

```csharp
string sourceFilePath = MyDir + "50states.plt";

using (Image cadImage = Image.Load(sourceFilePath))
{
    // รหัสของคุณสำหรับขั้นตอนต่อไปจะอยู่ที่นี่
}
```

 ในขั้นตอนนี้ เราจะโหลดไฟล์ PLT โดยใช้นามสกุลไฟล์`Image.Load` วิธีการจัดทำโดย Aspose.CAD

## ขั้นตอนที่ 2: กำหนดค่าตัวเลือกการส่งออกรูปภาพ

```csharp
ImageOptionsBase imageOptions = new JpegOptions();
CadRasterizationOptions options = new CadRasterizationOptions
{
    PageHeight = 500,
    PageWidth = 1000,
    // เพิ่มตัวเลือกเพิ่มเติมตามความจำเป็น
};
imageOptions.VectorRasterizationOptions = options;
```

 ที่นี่ เราตั้งค่าตัวเลือกการส่งออกรูปภาพ ในตัวอย่างนี้ เราใช้ JpegOptions แต่คุณสามารถเลือกรูปแบบอื่นได้ตามความต้องการของคุณ ปรับ`PageHeight` และ`PageWidth` ตามความจำเป็นสำหรับภาพที่ส่งออกของคุณ

## ขั้นตอนที่ 3: บันทึกรูปภาพ

```csharp
cadImage.Save(MyDir + "50states.jpg", imageOptions);
```

 สุดท้าย ให้บันทึกภาพที่แปลงแล้วโดยใช้ไฟล์`Save` วิธีการระบุเส้นทางเอาต์พุตและตัวเลือกรูปภาพที่กำหนดค่าไว้ก่อนหน้านี้

ทำซ้ำขั้นตอนเหล่านี้สำหรับไฟล์ PLT อื่นๆ หรือปรับแต่งตัวเลือกตามความต้องการเฉพาะของคุณ

## บทสรุป

ยินดีด้วย! คุณได้เรียนรู้วิธีส่งออกไฟล์ PLT ไปยังรูปภาพโดยใช้ Aspose.CAD สำหรับ .NET เรียบร้อยแล้ว ไลบรารีอันทรงพลังนี้มอบความยืดหยุ่นและประสิทธิภาพในการจัดการไฟล์ CAD ทำให้เป็นเครื่องมืออันมีค่าสำหรับโครงการของคุณ

## คำถามที่พบบ่อย

### คำถามที่ 1: ฉันสามารถส่งออกไฟล์ PLT ไปเป็นรูปแบบอื่นที่ไม่ใช่ JPEG ได้หรือไม่

A1: แน่นอน! คุณสามารถเลือกรูปแบบรูปภาพต่างๆ ที่ Aspose.CAD รองรับ เช่น PNG, GIF, BMP และอื่นๆ

### คำถามที่ 2: ฉันจะปรับแต่งตัวเลือกการแรสเตอร์เพื่อให้ควบคุมได้มากขึ้นได้อย่างไร

 A2: เพียงปรับคุณสมบัติของ`CadRasterizationOptions` ในขั้นตอนที่ 2 เพื่อปรับแต่งผลลัพธ์ให้ตรงตามความต้องการเฉพาะของคุณ

### คำถามที่ 3: มีเวอร์ชันทดลองใช้งานหรือไม่

 A3: ได้ คุณสามารถสำรวจความสามารถของ Aspose.CAD ได้โดยการทดลองใช้ฟรี[ที่นี่](https://releases.aspose.com/).

### Q4: ฉันจะหาเอกสารโดยละเอียดได้จากที่ไหน?

 A4: มีเอกสารประกอบที่ครอบคลุม[ที่นี่](https://reference.aspose.com/cad/net/).

### Q5: ต้องการความช่วยเหลือหรือมีคำถาม?

 A5: เยี่ยมชมชุมชนของเรา[ฟอรั่ม](https://forum.aspose.com/c/cad/19) สำหรับการสนับสนุนและการอภิปราย

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}
