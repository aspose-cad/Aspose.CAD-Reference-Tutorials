---
title: รองรับ DGN V7 ใน Aspose.CAD สำหรับ .NET
linktitle: รองรับ DGN V7
second_title: Aspose.CAD .NET - รูปแบบไฟล์ CAD และ BIM
description: สำรวจ Aspose.CAD สำหรับการรองรับ .NET อย่างราบรื่นสำหรับ DGN V7 แปลงไฟล์ DGN เป็นภาพแรสเตอร์ได้อย่างง่ายดายพร้อมคำแนะนำทีละขั้นตอน
weight: 19
url: /th/net/cad-features-and-support/support-for-dgn-v7/
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# รองรับ DGN V7 ใน Aspose.CAD สำหรับ .NET

## การแนะนำ

ในขอบเขตของการพัฒนา .NET นั้น Aspose.CAD มีความโดดเด่นในฐานะไลบรารีที่ทรงพลังสำหรับการจัดการไฟล์ Computer-Aided Design (CAD) บทช่วยสอนนี้จะเจาะลึกคุณสมบัติเฉพาะของ Aspose.CAD สำหรับ .NET ซึ่งรองรับไฟล์ DGN V7 DGN ย่อมาจาก Design เป็นรูปแบบไฟล์ที่ใช้กันอย่างแพร่หลายในโดเมน CAD Aspose.CAD ทำให้กระบวนการทำงานกับไฟล์ DGN V7 ง่ายขึ้น ช่วยให้นักพัฒนาได้รับประสบการณ์ที่ราบรื่น

## ข้อกำหนดเบื้องต้น

ก่อนที่เราจะเจาะลึกการนำไปปฏิบัติ ตรวจสอบให้แน่ใจว่าคุณมีข้อกำหนดเบื้องต้นต่อไปนี้:

-  Aspose.CAD สำหรับ .NET: ตรวจสอบให้แน่ใจว่าคุณได้ติดตั้งไลบรารี Aspose.CAD แล้ว คุณสามารถดาวน์โหลดได้จาก[เว็บไซต์](https://releases.aspose.com/cad/net/).

- สภาพแวดล้อมการพัฒนา: ตั้งค่าสภาพแวดล้อมการพัฒนา .NET ที่ใช้งานได้ รวมถึง Visual Studio หรือ IDE ที่ต้องการอื่นๆ

ตอนนี้เราได้เรียงลำดับข้อกำหนดเบื้องต้นแล้ว เรามาสำรวจวิธีใช้ประโยชน์จากการสนับสนุน DGN V7 ใน Aspose.CAD สำหรับ .NET กันดีกว่า

## นำเข้าเนมสเปซ

เริ่มต้นด้วยการนำเข้าเนมสเปซที่จำเป็นเพื่อเข้าถึงฟังก์ชันการทำงานของ Aspose.CAD:

```csharp
using System;
using System.Collections.Generic;
using System.Linq;
using System.Text;
using System.Threading.Tasks;
using Aspose.CAD;
```

## ขั้นตอนที่ 1: โหลดไฟล์ DGN

 เริ่มต้นด้วยการโหลดไฟล์ DGN ที่มีอยู่เป็นไฟล์`CadImage` แทนที่`"Your Document Directory"` และ`"Nikon_D90_Camera.dgn"` ด้วยเส้นทางไดเร็กทอรีและชื่อไฟล์ที่เหมาะสม

```csharp
string MyDir = "Your Document Directory";
string sourceFilePath = MyDir + "Nikon_D90_Camera.dgn";

using (CadImage cadImage = (CadImage)Image.Load(sourceFilePath))
{
    // รหัสสำหรับขั้นตอนต่อไปอยู่ที่นี่...
}
```

## ขั้นตอนที่ 2: กำหนดค่าตัวเลือกการแรสเตอร์

 สร้างก`CadRasterizationOptions` วัตถุเพื่อกำหนดและตั้งค่าคุณสมบัติต่าง ๆ ที่เกี่ยวข้องกับการแรสเตอร์

```csharp
CadRasterizationOptions rasterizationOptions = new CadRasterizationOptions
{
    PageWidth = 600,
    PageHeight = 300,
    NoScaling = true,
    AutomaticLayoutsScaling = false
};
```

## ขั้นตอนที่ 3: ตั้งค่าตัวเลือกการแรสเตอร์เวกเตอร์

 สร้างก`JpegOptions` object ตามที่เราตั้งใจจะแปลงไฟล์ DGN เป็น JPEG กำหนดสิ่งที่สร้างไว้ก่อนหน้านี้`CadRasterizationOptions` คัดค้านมัน

```csharp
ImageOptionsBase options = new JpegOptions
{
    VectorRasterizationOptions = rasterizationOptions
};
```

## ขั้นตอนที่ 4: บันทึกภาพแรสเตอร์

 โทรหา`Save` วิธีการของ`CadImage` วัตถุคลาสเพื่อส่งออกไฟล์ DGN ไปยังภาพแรสเตอร์ ในกรณีนี้คือ JPEG

```csharp
cadImage.Save(MyDir + "ExportDGNToRasterImage_out.jpeg", options);
```

เมื่อขั้นตอนเหล่านี้เสร็จสิ้น ไฟล์ DGN จะถูกส่งออกไปยังภาพแรสเตอร์ได้สำเร็จ

## บทสรุป

ในบทช่วยสอนนี้ เราได้สำรวจการสนับสนุนที่ราบรื่นสำหรับ DGN V7 ใน Aspose.CAD สำหรับ .NET ด้วยการทำตามคำแนะนำทีละขั้นตอน นักพัฒนาสามารถแปลงไฟล์ DGN เป็นภาพแรสเตอร์ได้อย่างง่ายดาย ซึ่งขยายขีดความสามารถของแอปพลิเคชัน .NET ของตน

## คำถามที่พบบ่อย

### คำถามที่ 1: Aspose.CAD เข้ากันได้กับข้อกำหนด DGN V7 ล่าสุดหรือไม่

ตอบ 1: ใช่ Aspose.CAD ได้รับการออกแบบมาเพื่อจัดการไฟล์ DGN V7 ได้อย่างราบรื่น ทำให้มั่นใจได้ถึงความเข้ากันได้กับข้อกำหนดล่าสุด

### คำถามที่ 2: ฉันสามารถปรับแต่งตัวเลือกการแรสเตอร์สำหรับการแปลงไฟล์ DGN ได้หรือไม่

 A2: แน่นอน. บทช่วยสอนสาธิตวิธีการสร้างและกำหนดค่า`CadRasterizationOptions` เพื่อปรับแต่งกระบวนการแปลง

### คำถามที่ 3: มีรูปแบบเอาต์พุตอื่นที่รองรับนอกเหนือจาก JPEG หรือไม่

A3: ใช่ Aspose.CAD รองรับรูปแบบเอาต์พุตที่หลากหลาย คุณสามารถสำรวจเอกสารเพื่อดูรายการที่ครอบคลุมได้

### คำถามที่ 4: ฉันจะได้รับการสนับสนุนสำหรับการสอบถามที่เกี่ยวข้องกับ Aspose.CAD ได้อย่างไร

 A4: เยี่ยมชม[ฟอรั่ม Aspose.CAD](https://forum.aspose.com/c/cad/19) สำหรับการสนับสนุนและการอภิปรายของชุมชน

### คำถามที่ 5: Aspose.CAD สำหรับ .NET มีรุ่นทดลองใช้ฟรีหรือไม่

 A5: ได้ คุณสามารถทดลองใช้ฟรีได้[ที่นี่](https://releases.aspose.com/).
{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}
