---
title: ส่งออกเค้าโครง CAD เป็นรูปแบบภาพแรสเตอร์ใน Aspose.CAD สำหรับ .NET
linktitle: ส่งออกเค้าโครง CAD เป็นรูปแบบภาพแรสเตอร์
second_title: Aspose.CAD .NET - รูปแบบไฟล์ CAD และ BIM
description: เรียนรู้วิธีส่งออกเค้าโครง CAD เป็นภาพแรสเตอร์โดยใช้ Aspose.CAD สำหรับ .NET ปฏิบัติตามคำแนะนำทีละขั้นตอนของเราเพื่อการแปลงที่ราบรื่น
type: docs
weight: 10
url: /th/net/cad-export-formats/export-cad-layouts-to-raster-image-formats/
---
## การแนะนำ

คุณต้องการแปลงเค้าโครง CAD เป็นรูปแบบภาพแรสเตอร์อย่างมีประสิทธิภาพโดยใช้ Aspose.CAD สำหรับ .NET หรือไม่? คำแนะนำทีละขั้นตอนนี้จะแนะนำคุณตลอดกระบวนการ โดยให้คำแนะนำโดยละเอียดและตัวอย่างโค้ดเพื่อทำให้งานราบรื่น ไม่ว่าคุณจะเป็นนักพัฒนาที่มีประสบการณ์หรือเพิ่งเริ่มใช้ Aspose.CAD บทช่วยสอนนี้เหมาะสำหรับทุกระดับของความเชี่ยวชาญ

## ข้อกำหนดเบื้องต้น

ก่อนที่จะเข้าสู่บทช่วยสอน ตรวจสอบให้แน่ใจว่าคุณมีสิ่งต่อไปนี้:

- Aspose.CAD สำหรับไลบรารี .NET: ตรวจสอบให้แน่ใจว่าคุณได้ติดตั้งไลบรารี Aspose.CAD แล้ว ถ้าไม่เช่นนั้นคุณสามารถดาวน์โหลดได้จาก[เว็บไซต์ Aspose.CAD](https://releases.aspose.com/cad/net/).

- ไฟล์เขียนแบบ CAD: เตรียมไฟล์เขียนแบบ CAD (เช่น conic_pyramid.dxf) ที่คุณต้องการแปลงเป็นรูปแบบภาพแรสเตอร์

## นำเข้าเนมสเปซ

ในโปรเจ็กต์ .NET ของคุณ ให้นำเข้าเนมสเปซที่จำเป็นเพื่อใช้ประโยชน์จากฟังก์ชัน Aspose.CAD รวมเนมสเปซต่อไปนี้ไว้ที่จุดเริ่มต้นของโค้ดของคุณ:

```csharp
using System;
using System.Collections.Generic;
using System.Linq;
using System.Text;
using System.Threading.Tasks;
using Aspose.CAD;
```

## ขั้นตอนที่ 1: โหลด CAD Drawing

```csharp
string MyDir = "Your Document Directory";
string sourceFilePath = MyDir + "conic_pyramid.dxf";

// โหลดแบบร่าง CAD ในอินสแตนซ์ของรูปภาพ
using (var image = Image.Load(sourceFilePath))
{
    // รหัสของคุณสำหรับการโหลดแบบร่าง CAD อยู่ที่นี่
}
```

## ขั้นตอนที่ 2: สร้าง CadRasterizationOptions

```csharp
// สร้างอินสแตนซ์ของ CadRasterizationOptions
var rasterizationOptions = new CadRasterizationOptions();
rasterizationOptions.PageWidth = 500;
rasterizationOptions.PageHeight = 500;
```

## ขั้นตอนที่ 3: ระบุเลเยอร์

```csharp
// เพิ่มชื่อเลเยอร์ลงในรายการเลเยอร์ของ CadRasterizationOptions
rasterizationOptions.Layers = new string[] { "LayerA" };
```

## ขั้นตอนที่ 4: สร้าง JpegOptions

```csharp
// สร้างอินสแตนซ์ของ JpegOptions (หรือ ImageOptions ใด ๆ สำหรับรูปแบบแรสเตอร์)
var options = new JpegOptions();
options.VectorRasterizationOptions = rasterizationOptions;
```

## ขั้นตอนที่ 5: ส่งออกเป็นรูปแบบ Jpeg

```csharp
// ส่งออกแต่ละเลเยอร์เป็นรูปแบบ Jpeg
MyDir = MyDir + "CADLayersToRasterImageFormats_out.jpg";
image.Save(MyDir, options);
```

## ขั้นตอนเพิ่มเติม: แปลงเลเยอร์ทั้งหมด

หากคุณต้องการแปลงเลเยอร์ทั้งหมด ให้ใช้วิธีการต่อไปนี้:

```csharp
ConvertAllLayersToRasterImageFormats();
```

วิธีการนี้จะวนซ้ำทุกเลเยอร์ในแบบร่าง CAD โดยส่งออกแต่ละเลเยอร์ไปยังไฟล์ Jpeg ที่แยกจากกัน

## บทสรุป

ยินดีด้วย! คุณได้เรียนรู้วิธีส่งออกเค้าโครง CAD เป็นรูปแบบภาพแรสเตอร์โดยใช้ Aspose.CAD สำหรับ .NET เรียบร้อยแล้ว บทช่วยสอนนี้ให้คำแนะนำที่ครอบคลุมสำหรับนักพัฒนาที่กำลังมองหาโซลูชันที่มีประสิทธิภาพและเชื่อถือได้สำหรับการแปลง CAD

## คำถามที่พบบ่อย

### คำถามที่ 1: ฉันสามารถใช้รูปแบบรูปภาพอื่นเพื่อส่งออกได้หรือไม่

 A1: ใช่คุณทำได้ เพียงแค่แทนที่`JpegOptions` โดยมีตัวเลือกรูปแบบที่ต้องการ เช่น`PngOptions` หรือ`BmpOptions`.

### คำถามที่ 2: มีเวอร์ชันทดลองใช้งานหรือไม่

 ตอบ 2: ได้ คุณสามารถสำรวจฟังก์ชันการทำงานของ Aspose.CAD ได้โดยดาวน์โหลดเวอร์ชันทดลองใช้งาน[ที่นี่](https://releases.aspose.com/).

### คำถามที่ 3: ฉันจะรับการสนับสนุนสำหรับ Aspose.CAD ได้อย่างไร

 A3: เยี่ยมชม Aspose.CAD[ฟอรั่ม](https://forum.aspose.com/c/cad/19) สำหรับการสนับสนุนจากชุมชนหรือพิจารณาซื้อใบอนุญาตสำหรับการสนับสนุนเฉพาะ

### คำถามที่ 4: มีใบอนุญาตชั่วคราวหรือไม่

 A4: ได้ คุณสามารถขอรับใบอนุญาตชั่วคราวได้[ที่นี่](https://purchase.aspose.com/temporary-license/).

### Q5: ฉันจะหาเอกสารได้จากที่ไหน?

 A5: โปรดดูเอกสารประกอบโดยละเอียด[ที่นี่](https://reference.aspose.com/cad/net/).