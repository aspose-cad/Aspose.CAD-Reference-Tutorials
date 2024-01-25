---
title: แปลงการวาด CAD เป็นภาพแรสเตอร์ใน Aspose.CAD สำหรับ .NET
linktitle: แปลงการวาด CAD เป็นภาพแรสเตอร์
second_title: Aspose.CAD .NET - รูปแบบไฟล์ CAD และ BIM
description: สำรวจกระบวนการที่ราบรื่นในการแปลงภาพวาด CAD เป็นภาพแรสเตอร์ใน .NET ด้วย Aspose.CAD ปลดล็อกขั้นตอนการทำงานที่มีประสิทธิภาพและปรับปรุงโครงการ CAD ของคุณได้อย่างง่ายดาย
type: docs
weight: 11
url: /th/net/cad-drawing-manipulation/convert-cad-drawing-to-raster-image/
---
## การแนะนำ

ในภูมิทัศน์ที่เปลี่ยนแปลงตลอดเวลาของการออกแบบโดยใช้คอมพิวเตอร์ช่วย (CAD) ความจำเป็นในการแปลงแบบร่าง CAD ให้เป็นภาพแรสเตอร์ได้อย่างราบรื่นถือเป็นสิ่งสำคัญยิ่ง คำแนะนำทีละขั้นตอนนี้จะสำรวจวิธีการบรรลุเป้าหมายนี้โดยใช้ไลบรารี Aspose.CAD สำหรับ .NET อันทรงพลัง Aspose.CAD ทำให้กระบวนการง่ายขึ้น โดยมอบชุดเครื่องมือที่แข็งแกร่งแก่นักพัฒนาเพื่อปรับปรุงเวิร์กโฟลว์ที่เกี่ยวข้องกับ CAD

## ข้อกำหนดเบื้องต้น

ก่อนที่จะเข้าสู่บทช่วยสอน ตรวจสอบให้แน่ใจว่าคุณมีข้อกำหนดเบื้องต้นต่อไปนี้:

1.  Aspose.CAD สำหรับไลบรารี .NET: ดาวน์โหลดและติดตั้งไลบรารี Aspose.CAD จากไฟล์[หน้าดาวน์โหลด](https://releases.aspose.com/cad/net/).

2. สภาพแวดล้อมการพัฒนา: ตั้งค่าสภาพแวดล้อมการพัฒนาการทำงานด้วย IDE ที่เข้ากันได้สำหรับการพัฒนา .NET

## นำเข้าเนมสเปซ

ในโปรเจ็กต์ .NET ของคุณ ให้นำเข้าเนมสเปซที่จำเป็นเพื่อเข้าถึงฟังก์ชัน Aspose.CAD เพิ่มสิ่งต่อไปนี้ที่จุดเริ่มต้นของไฟล์โค้ดของคุณ:

```csharp
using System;
using System.Collections.Generic;
using System.Linq;
using System.Text;
using System.Threading.Tasks;
using Aspose.CAD;
```

## ขั้นตอนที่ 1: กำหนดเส้นทางไฟล์

```csharp
// เส้นทางไปยังไดเร็กทอรีเอกสาร
string MyDir = "Your Document Directory";
string sourceFilePath = MyDir + "conic_pyramid.dxf";
```

ตรวจสอบให้แน่ใจว่าได้แทนที่ "Your Document Directory" ด้วยเส้นทางจริงไปยังไฟล์ CAD ของคุณ

## ขั้นตอนที่ 2: โหลด CAD Drawing

```csharp
using (Aspose.CAD.Image image = Aspose.CAD.Image.Load(sourceFilePath))
{
```

ขั้นตอนนี้จะเริ่มต้นวัตถุรูปภาพ Aspose.CAD และโหลดแบบร่าง CAD จากเส้นทางไฟล์ที่ระบุ

## ขั้นตอนที่ 3: กำหนดค่าตัวเลือกการแรสเตอร์

```csharp
// สร้างอินสแตนซ์ของ CadRasterizationOptions
Aspose.CAD.ImageOptions.CadRasterizationOptions rasterizationOptions = new Aspose.CAD.ImageOptions.CadRasterizationOptions();
// กำหนดความกว้างและความสูงของหน้า
rasterizationOptions.PageWidth = 1200;
rasterizationOptions.PageHeight = 1200;
```

ที่นี่ เราตั้งค่าตัวเลือกการแรสเตอร์ โดยกำหนดความกว้างและความสูงของหน้าผลลัพธ์

## ขั้นตอนที่ 4: สร้าง PNGOptions สำหรับรูปภาพผลลัพธ์

```csharp
// สร้างอินสแตนซ์ของ PngOptions สำหรับรูปภาพผลลัพธ์
ImageOptionsBase options = new Aspose.CAD.ImageOptions.PngOptions();
// ตั้งค่าตัวเลือกการแรสเตอร์
options.VectorRasterizationOptions = rasterizationOptions;
```

ขั้นตอนนี้เกี่ยวข้องกับการกำหนดค่าตัวเลือกสำหรับรูปภาพผลลัพธ์ โดยระบุตัวเลือกการแรสเตอร์ที่กำหนดไว้ก่อนหน้านี้

## ขั้นตอนที่ 5: บันทึกรูปภาพผลลัพธ์

```csharp
MyDir = MyDir + "conic_pyramid_raster_image_out.png";
// บันทึกภาพผลลัพธ์
image.Save(MyDir, options);
```

บันทึกภาพแรสเตอร์ที่แปลงแล้วไปยังเส้นทางไฟล์เอาต์พุตที่ระบุ

## ขั้นตอนที่ 6: แสดงข้อความแสดงความสำเร็จ

```csharp
// ตัวอย่าง: แปลง DrawingToRasterImage
Console.WriteLine("\nCAD drawing converted successfully to raster image format.\nFile saved at " + MyDir);
```

แสดงข้อความแสดงความสำเร็จที่ระบุว่ากระบวนการแปลงเสร็จสมบูรณ์

## บทสรุป

ในบทช่วยสอนนี้ เราได้สำรวจกระบวนการทีละขั้นตอนในการแปลงภาพวาด CAD เป็นภาพแรสเตอร์โดยใช้ Aspose.CAD สำหรับไลบรารี .NET ด้วยคุณสมบัติอันทรงพลังและการผสานรวมที่ง่ายดาย Aspose.CAD ช่วยให้นักพัฒนาปรับปรุงเวิร์กโฟลว์ CAD ของตนได้อย่างง่ายดาย

## คำถามที่พบบ่อย

### คำถามที่ 1: Aspose.CAD เข้ากันได้กับไฟล์ CAD ทุกรูปแบบหรือไม่

A1: Aspose.CAD รองรับรูปแบบไฟล์ CAD ที่หลากหลาย รวมถึง DWG, DXF, DGN และอื่นๆ อ้างถึง[เอกสารประกอบ](https://reference.aspose.com/cad/net/) สำหรับรายการที่ครอบคลุม

### คำถามที่ 2: ฉันสามารถปรับแต่งตัวเลือกการแรสเตอร์สำหรับโปรเจ็กต์ต่างๆ ได้หรือไม่

ตอบ 2: ใช่ Aspose.CAD อนุญาตให้ปรับแต่งตัวเลือกการแรสเตอร์ได้อย่างกว้างขวาง ช่วยให้นักพัฒนาสามารถปรับแต่งเอาต์พุตตามความต้องการของโปรเจ็กต์ได้

### คำถามที่ 3: Aspose.CAD มีรุ่นทดลองใช้ฟรีหรือไม่

 A3: ได้ คุณสามารถสำรวจคุณสมบัติของ Aspose.CAD ได้ด้วยการทดลองใช้ฟรี เยี่ยม[ที่นี่](https://releases.aspose.com/) ที่จะเริ่มต้น.

### คำถามที่ 4: ฉันจะรับการสนับสนุนสำหรับ Aspose.CAD ได้อย่างไร

 A4: สำหรับความช่วยเหลือหรือข้อสงสัยใดๆ โปรดไปที่ Aspose.CAD[ฟอรั่มการสนับสนุน](https://forum.aspose.com/c/cad/19).

### คำถามที่ 5: Aspose.CAD มีใบอนุญาตชั่วคราวหรือไม่
 
 A5: ได้ นักพัฒนาสามารถขอรับใบอนุญาตชั่วคราวสำหรับ Aspose.CAD ได้จาก[ลิงค์นี้](https://purchase.aspose.com/temporary-license/).