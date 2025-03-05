---
title: แปลงเลย์เอาต์เป็นรูปภาพแรสเตอร์ใน Aspose.CAD สำหรับ .NET
linktitle: แปลงเลย์เอาต์เป็นภาพแรสเตอร์
second_title: Aspose.CAD .NET - รูปแบบไฟล์ CAD และ BIM
description: แปลงเค้าโครง CAD เป็นภาพแรสเตอร์ได้อย่างง่ายดายโดยใช้ Aspose.CAD สำหรับ .NET ยกระดับการพัฒนาของคุณด้วยความสามารถในการจัดการ CAD อันทรงพลัง
type: docs
weight: 12
url: /th/net/cad-drawing-manipulation/convert-layouts-to-raster-image/
---
## การแนะนำ

คุณกำลังมองหาการแปลงเค้าโครงเป็นรูปภาพแรสเตอร์ในแอปพลิเคชัน .NET ของคุณอย่างง่ายดายหรือไม่? ไม่ต้องมองอีกต่อไป! คำแนะนำทีละขั้นตอนนี้จะแนะนำคุณตลอดกระบวนการโดยใช้ Aspose.CAD สำหรับ .NET ซึ่งเป็นไลบรารีอันทรงพลังที่ทำให้งาน Computer-Aided Design (CAD) ง่ายขึ้น

## ข้อกำหนดเบื้องต้น

ก่อนที่จะเข้าสู่บทช่วยสอน ตรวจสอบให้แน่ใจว่าคุณมีข้อกำหนดเบื้องต้นต่อไปนี้:

- Aspose.CAD สำหรับ .NET Library: ดาวน์โหลดและติดตั้งไลบรารีจาก[หน้าดาวน์โหลด Aspose.CAD สำหรับ .NET](https://releases.aspose.com/cad/net/).

- สภาพแวดล้อมการพัฒนา: ตรวจสอบให้แน่ใจว่าคุณได้ตั้งค่าสภาพแวดล้อมการพัฒนา .NET ที่ใช้งานได้บนเครื่องของคุณ

- เอกสารที่จะแปลง: เตรียมเอกสาร CAD ที่มีเค้าโครงที่คุณต้องการแปลงเป็นภาพแรสเตอร์

- Your Document Directory: แทนที่ตัวยึด "Your Document Directory" ในโค้ดด้วยเส้นทางไปยังไดเร็กทอรีเอกสารของคุณ

## นำเข้าเนมสเปซ

ขั้นแรก เรามานำเข้าเนมสเปซที่จำเป็นเพื่อทำให้ฟังก์ชัน Aspose.CAD เข้าถึงได้ในโค้ดของคุณ

```csharp
using System;
using System.Collections.Generic;
using System.Linq;
using System.Text;
using System.Threading.Tasks;
using Aspose.CAD;
```

## ขั้นตอนที่ 1: โหลดเอกสาร CAD

เริ่มต้นด้วยการโหลดเอกสาร CAD โดยใช้ไลบรารี Aspose.CAD

```csharp
string sourceFilePath = MyDir + "conic_pyramid.dxf";
using (Image image = Image.Load(sourceFilePath))
{
    //รหัสของคุณสำหรับขั้นตอนต่อไปจะอยู่ที่นี่
}
```

## ขั้นตอนที่ 2: กำหนดค่าตัวเลือกการแรสเตอร์

 สร้างอินสแตนซ์ของ`CadRasterizationOptions` เพื่อตั้งค่าความกว้าง ความสูงของหน้า และระบุเค้าโครงที่คุณต้องการแปลง

```csharp
CadRasterizationOptions rasterizationOptions = new CadRasterizationOptions();
rasterizationOptions.PageWidth = 1200;
rasterizationOptions.PageHeight = 1200;
rasterizationOptions.Layouts = new string[] { "Model", "Layout1" };
```

## ขั้นตอนที่ 3: ตั้งค่า TiffOptions สำหรับรูปภาพผลลัพธ์

 สร้างอินสแตนซ์ของ`TiffOptions`เพื่อกำหนดรูปแบบของภาพที่ได้

```csharp
ImageOptionsBase options = new TiffOptions(TiffExpectedFormat.Default);
options.VectorRasterizationOptions = rasterizationOptions;
```

## ขั้นตอนที่ 4: บันทึกรูปภาพผลลัพธ์

ระบุเส้นทางเอาต์พุตและบันทึกภาพที่แปลงแล้ว

```csharp
string outputFilePath = MyDir + "conic_pyramid_layoutstorasterimage_out.tiff";
image.Save(outputFilePath, options);
```

## บทสรุป

ยินดีด้วย! คุณได้แปลงเค้าโครง CAD เป็นรูปแบบภาพแรสเตอร์สำเร็จแล้วโดยใช้ Aspose.CAD สำหรับ .NET ความเป็นไปได้มีมากมาย และคู่มือนี้ทำหน้าที่เป็นจุดเริ่มต้นสำหรับความพยายามที่เกี่ยวข้องกับ CAD ของคุณ

## คำถามที่พบบ่อย

### คำถามที่ 1: Aspose.CAD เข้ากันได้กับรูปแบบ CAD ทั้งหมดหรือไม่

 A1: Aspose.CAD รองรับรูปแบบ CAD ที่หลากหลาย รวมถึง DWG, DXF, DWF, STL และอื่นๆ ตรวจสอบ[เอกสารประกอบ](https://reference.aspose.com/cad/net/) สำหรับรายการที่ครอบคลุม

### คำถามที่ 2: ฉันจะขอรับใบอนุญาตชั่วคราวสำหรับ Aspose.CAD ได้อย่างไร

 A2: เยี่ยมชม[หน้าใบอนุญาตชั่วคราว](https://purchase.aspose.com/temporary-license/) เพื่อรับใบอนุญาตชั่วคราวเพื่อวัตถุประสงค์ในการทดสอบและประเมินผล

### คำถามที่ 3: ฉันจะรับการสนับสนุนสำหรับ Aspose.CAD ได้ที่ไหน

 A3: ฟอรัมเป็นสถานที่ที่ดีเยี่ยมในการขอความช่วยเหลือ เยี่ยมชม[ฟอรั่ม Aspose.CAD](https://forum.aspose.com/c/cad/19) เพื่อเชื่อมต่อกับชุมชนและรับความช่วยเหลือ

### คำถามที่ 4: ฉันสามารถทดลองใช้ Aspose.CAD ได้ฟรีหรือไม่

 A4: แน่นอน! คว้าของคุณ[ทดลองฟรี](https://releases.aspose.com/) เพื่อสำรวจคุณสมบัติและความสามารถของ Aspose.CAD

### คำถามที่ 5: ฉันจะซื้อใบอนุญาตสำหรับ Aspose.CAD ได้ที่ไหน

 A5: นำทางไปยัง[หน้าซื้อ](https://purchase.aspose.com/buy) เพื่อซื้อใบอนุญาตและปลดล็อคศักยภาพสูงสุดของ Aspose.CAD