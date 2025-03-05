---
title: การส่งออกรูปภาพ 3 มิติเป็น PDF - บทช่วยสอน Aspose.CAD
linktitle: การส่งออกภาพ 3 มิติเป็น PDF
second_title: Aspose.CAD .NET - รูปแบบไฟล์ CAD และ BIM
description: แปลงรูปภาพ 3D CAD เป็น PDF ได้อย่างง่ายดายด้วย Aspose.CAD สำหรับ .NET ปฏิบัติตามบทช่วยสอนทีละขั้นตอนของเราเพื่อการส่งออก PDF ได้อย่างราบรื่น
type: docs
weight: 10
url: /th/net/3d-image-export/exporting-3d-images-to-pdf/
---
## การแนะนำ

คุณต้องการส่งออกรูปภาพ 3 มิติเป็น PDF ได้อย่างราบรื่นโดยใช้ Aspose.CAD สำหรับ .NET หรือไม่? บทช่วยสอนแบบทีละขั้นตอนนี้จะแนะนำคุณตลอดกระบวนการ เพื่อให้มั่นใจว่าคุณจะได้ใช้ประโยชน์จากพลังของ Aspose.CAD เพื่อแปลงภาพ 3D ของคุณเป็นรูปแบบ PDF ได้อย่างง่ายดาย

## ข้อกำหนดเบื้องต้น

ก่อนที่จะเข้าสู่บทช่วยสอน ตรวจสอบให้แน่ใจว่าคุณมีข้อกำหนดเบื้องต้นต่อไปนี้:

-  Aspose.CAD สำหรับ .NET: ตรวจสอบให้แน่ใจว่าคุณได้ติดตั้งไลบรารี Aspose.CAD สำหรับ .NET แล้ว ถ้าไม่เช่นนั้นคุณสามารถดาวน์โหลดได้จาก[หน้าดาวน์โหลด Aspose.CAD สำหรับ .NET](https://releases.aspose.com/cad/net/).

- ไดเร็กทอรีเอกสาร: ตั้งค่าไดเร็กทอรีที่เก็บไฟล์ CAD ของคุณ และจดบันทึกเส้นทาง

## นำเข้าเนมสเปซ

ในโปรเจ็กต์ .NET ของคุณ ให้นำเข้าเนมสเปซที่จำเป็นสำหรับการทำงานกับ Aspose.CAD เพิ่มบรรทัดต่อไปนี้ที่ด้านบนของไฟล์โค้ดของคุณ:

```csharp
using System;
using System.Collections.Generic;
using System.Linq;
using System.Text;
using System.Threading.Tasks;
using Aspose.CAD;
using Aspose.CAD.ImageOptions;
```

## ขั้นตอนที่ 1: โหลดอิมเมจ CAD

 เริ่มต้นด้วยการโหลดอิมเมจ CAD ที่คุณต้องการส่งออกเป็น PDF ใช้`Load` วิธีการจากไลบรารี Aspose.CAD แทนที่`"conic_pyramid.dxf"` พร้อมเส้นทางไปยังไฟล์ CAD ของคุณ

```csharp
string MyDir = "Your Document Directory";
string sourceFilePath = MyDir + "conic_pyramid.dxf";
using (Image cadImage = Image.Load(sourceFilePath))
{
    // รหัสของคุณสำหรับการโหลดอิมเมจ CAD อยู่ที่นี่
}
```

## ขั้นตอนที่ 2: กำหนดค่าตัวเลือกการแรสเตอร์

 กำหนดค่าตัวเลือกการแรสเตอร์สำหรับรูปภาพ CAD ตั้งค่าพารามิเตอร์ เช่น ความกว้างของหน้า ความสูงของหน้า และเค้าโครง ยกเลิกการแสดงความคิดเห็นบรรทัดที่เกี่ยวข้อง`TypeOfEntities` หากเอนทิตีของคุณเป็นแบบ 3 มิติ

```csharp
CadRasterizationOptions rasterizationOptions = new CadRasterizationOptions();
rasterizationOptions.PageWidth = 500;
rasterizationOptions.PageHeight = 500;
// rasterizationOptions.TypeOfEntities = TypeOfEntities.Entities3D;

rasterizationOptions.Layouts = new string[] { "Model" };
```

## ขั้นตอนที่ 3: ตั้งค่าตัวเลือก PDF

สร้างตัวเลือก PDF และเชื่อมโยงกับตัวเลือกการแรสเตอร์

```csharp
PdfOptions pdfOptions = new PdfOptions();
pdfOptions.VectorRasterizationOptions = rasterizationOptions;
```

## ขั้นตอนที่ 4: บันทึกเป็น PDF

บันทึกอิมเมจ CAD เป็นไฟล์ PDF โดยใช้ตัวเลือกที่กำหนดค่าไว้ ระบุเส้นทางเอาต์พุตสำหรับไฟล์ PDF

```csharp
MyDir = MyDir + "Export3DImagestoPDF_out.pdf";
cadImage.Save(MyDir, pdfOptions);
```

## บทสรุป

ยินดีด้วย! คุณได้ส่งออกรูปภาพ 3 มิติเป็น PDF โดยใช้ Aspose.CAD สำหรับ .NET สำเร็จแล้ว บทช่วยสอนที่ตรงไปตรงมานี้ช่วยให้แน่ใจว่าคุณแปลงไฟล์ CAD ของคุณให้อยู่ในรูปแบบที่เข้าถึงได้ง่ายขึ้นได้อย่างง่ายดาย

## คำถามที่พบบ่อย

### คำถามที่ 1: Aspose.CAD เข้ากันได้กับไฟล์ CAD ทุกรูปแบบหรือไม่

ตอบ 1: ใช่ Aspose.CAD รองรับรูปแบบ CAD ที่หลากหลาย ทำให้มั่นใจได้ถึงความยืดหยุ่นในการจัดการไฟล์ประเภทต่างๆ

### คำถามที่ 2: ฉันสามารถกำหนดขนาดหน้าเองเมื่อส่งออกเป็น PDF ได้หรือไม่

A2: แน่นอน. บทช่วยสอนสาธิตวิธีกำหนดค่าความกว้างและความสูงของหน้าตามความต้องการของคุณ

### คำถามที่ 3: Aspose.CAD มีใบอนุญาตชั่วคราวหรือไม่

 A3: ได้ คุณสามารถขอรับใบอนุญาตชั่วคราวสำหรับ Aspose.CAD ได้โดยเข้าไปที่[ใบอนุญาตชั่วคราว](https://purchase.aspose.com/temporary-license/).

### คำถามที่ 4: ฉันจะรับการสนับสนุนเพิ่มเติมหรือการสนทนาในชุมชนได้จากที่ไหน

 A4: มุ่งหน้าไปที่[ฟอรั่ม Aspose.CAD](https://forum.aspose.com/c/cad/19) เพื่อการสนับสนุนและการมีส่วนร่วมกับชุมชน

### คำถามที่ 5: Aspose.CAD มีเวอร์ชันทดลองใช้ฟรีหรือไม่

 A5: ได้ คุณสามารถสำรวจคุณสมบัติของ Aspose.CAD ได้โดยเข้าไปที่[ทดลองฟรี](https://releases.aspose.com/).