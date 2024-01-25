---
title: รองรับ 3D สำหรับ DGN V7 ใน Aspose.CAD สำหรับ .NET
linktitle: รองรับ 3D สำหรับ DGN V7
second_title: Aspose.CAD .NET - รูปแบบไฟล์ CAD และ BIM
description: ปลดล็อกพลังของการรองรับ 3D สำหรับ DGN V7 ใน Aspose.CAD สำหรับ .NET ปฏิบัติตามบทช่วยสอนทีละขั้นตอนของเรา
type: docs
weight: 20
url: /th/net/cad-features-and-support/support-of-3d-for-dgn-v7/
---
## การแนะนำ

ยินดีต้อนรับสู่บทช่วยสอนที่ครอบคลุมของเราเกี่ยวกับการใช้ประโยชน์จากการรองรับ 3D สำหรับ DGN V7 ใน Aspose.CAD สำหรับ .NET! Aspose.CAD เป็นไลบรารีอันทรงพลังที่ช่วยให้นักพัฒนาสามารถทำงานกับไฟล์ CAD ในแอปพลิเคชัน .NET ของตนได้อย่างราบรื่น ในบทช่วยสอนนี้ เราจะสำรวจขั้นตอนในการใช้การรองรับ 3D สำหรับ DGN V7 โดยให้ความรู้แก่คุณในการปรับปรุงโครงการที่เกี่ยวข้องกับ CAD ของคุณ

## ข้อกำหนดเบื้องต้น

ก่อนที่จะเข้าสู่บทช่วยสอน ตรวจสอบให้แน่ใจว่าคุณมีข้อกำหนดเบื้องต้นต่อไปนี้:

-  Aspose.CAD สำหรับ .NET: ตรวจสอบให้แน่ใจว่าคุณได้ติดตั้ง Aspose.CAD สำหรับ .NET แล้ว หากไม่ใช่คุณสามารถดาวน์โหลดได้จาก[ที่นี่](https://releases.aspose.com/cad/net/).

- สภาพแวดล้อมการพัฒนา: ตั้งค่าสภาพแวดล้อมการพัฒนาที่เหมาะสม เช่น Visual Studio สำหรับการพัฒนาแอปพลิเคชัน .NET

- ไฟล์ DGN ตัวอย่าง: เตรียมไฟล์ DGN ตัวอย่างให้พร้อมสำหรับการทดสอบ คุณสามารถใช้ไฟล์ตัวอย่าง "Nikon_D90_Camera.dgn" ที่ให้มา

ตอนนี้ มาดูขั้นตอนต่างๆ เพื่อให้รองรับ 3D สำหรับ DGN V7 โดยใช้ Aspose.CAD สำหรับ .NET กัน!

## นำเข้าเนมสเปซ

ในแอปพลิเคชัน .NET ของคุณ ให้เริ่มด้วยการนำเข้าเนมสเปซที่จำเป็น:

```csharp
using System;
using System.Collections.Generic;
using System.Linq;
using System.Text;
using System.Threading.Tasks;
using Aspose.CAD;
using Aspose.CAD.FileFormats.Dgn;
using Aspose.CAD.ImageOptions;
```

## ขั้นตอนที่ 1: ตั้งค่าไดเร็กทอรีเอกสารของคุณ

 ตรวจสอบให้แน่ใจว่าคุณได้ตั้งค่าไดเร็กทอรีเอกสารในโครงการของคุณ แทนที่`"Your Document Directory"` ด้วยเส้นทางจริงไปยังไดเร็กทอรีเอกสารของคุณ

```csharp
string MyDir = "Your Document Directory";
```

## ขั้นตอนที่ 2: โหลดไฟล์ DGN

โหลดไฟล์ DGN ที่มีอยู่เป็น CadImage โดยใช้รหัสต่อไปนี้:

```csharp
string sourceFilePath = MyDir + "Nikon_D90_Camera.dgn";
string outFile = MyDir + "Nikon_D90_Camera.dgn";

using (DgnImage dgnImage = (DgnImage)Image.Load(sourceFilePath))
{
    // รหัสของคุณสำหรับการประมวลผลเพิ่มเติมอยู่ที่นี่
}
```

## ขั้นตอนที่ 3: กำหนดค่าตัวเลือกการส่งออก PDF

ตั้งค่าตัวเลือกสำหรับการส่งออกเป็น PDF โดยระบุตัวเลือกการแรสเตอร์เวกเตอร์ เช่น ขนาดหน้า การปรับขนาดเค้าโครงอัตโนมัติ สีพื้นหลัง และเค้าโครงที่จะส่งออก

```csharp
var options = new PdfOptions
{
    VectorRasterizationOptions = new CadRasterizationOptions
    {
        PageWidth = 1500,
        PageHeight = 1500,
        AutomaticLayoutsScaling = true,
        BackgroundColor = Color.Black,
        Layouts = new string[] { "1", "2", "3", "9" } // ส่งออกมุมมองที่ระบุเท่านั้น
    }
};
```

## ขั้นตอนที่ 4: บันทึกภาพแรสเตอร์

บันทึกไฟล์ DGN เป็นภาพแรสเตอร์พร้อมตัวเลือกที่กำหนดค่าไว้

```csharp
dgnImage.Save(outFile, options);
```

## บทสรุป

ยินดีด้วย! คุณใช้ Aspose.CAD สำหรับ .NET เพื่อส่งออกไฟล์ DGN ที่รองรับ 3D ไปยังรูปภาพแรสเตอร์ได้สำเร็จ บทช่วยสอนนี้ได้จัดเตรียมขั้นตอนที่จำเป็นในการรวมฟังก์ชันนี้เข้ากับโปรเจ็กต์ CAD ของคุณ

## คำถามที่พบบ่อย

### คำถามที่ 1: ฉันสามารถใช้ Aspose.CAD สำหรับ .NET กับไฟล์ CAD รูปแบบอื่นได้หรือไม่

A1: ใช่ Aspose.CAD รองรับไฟล์ CAD หลากหลายรูปแบบ รวมถึง DWG และ DXF

### คำถามที่ 2: ฉันจะจัดการกับข้อยกเว้นเมื่อทำงานกับ Aspose.CAD ได้อย่างไร

A2: ตัดโค้ดของคุณในบล็อก try-catch ดังที่แสดงในตัวอย่างที่ให้ไว้ เพื่อจัดการกับข้อยกเว้นอย่างสวยงาม

### คำถามที่ 3: Aspose.CAD เหมาะสำหรับโครงการเชิงพาณิชย์หรือไม่

 A3: แน่นอน! คุณสามารถซื้อ Aspose.CAD สำหรับ .NET ได้[ที่นี่](https://purchase.aspose.com/buy).

### คำถามที่ 4: ฉันสามารถลองใช้ Aspose.CAD สำหรับ .NET ก่อนซื้อได้หรือไม่

A4: แน่นอน! สำรวจการทดลองใช้ฟรี[ที่นี่](https://releases.aspose.com/).

### คำถามที่ 5: ฉันจะหาการสนับสนุนชุมชนสำหรับ Aspose.CAD สำหรับ .NET ได้ที่ไหน

 A5: เยี่ยมชมฟอรั่มชุมชน[ที่นี่](https://forum.aspose.com/c/cad/19).