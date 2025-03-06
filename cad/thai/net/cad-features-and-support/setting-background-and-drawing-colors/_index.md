---
title: การตั้งค่าสีพื้นหลังและการวาดใน Aspose.CAD สำหรับ .NET
linktitle: การตั้งค่าพื้นหลังและสีการวาด
second_title: Aspose.CAD .NET - รูปแบบไฟล์ CAD และ BIM
description: ปรมาจารย์ Aspose.CAD สำหรับ .NET ตั้งค่าสีพื้นหลังและการวาดภาพได้อย่างง่ายดาย ปฏิบัติตามคำแนะนำทีละขั้นตอนของเรา
weight: 15
url: /th/net/cad-features-and-support/setting-background-and-drawing-colors/
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# การตั้งค่าสีพื้นหลังและการวาดใน Aspose.CAD สำหรับ .NET

## การแนะนำ

ในโลกแบบไดนามิกของการพัฒนา .NET Aspose.CAD กลายเป็นเครื่องมืออันทรงพลังสำหรับการจัดการไฟล์ Computer-Aided Design (CAD) หากคุณกระตือรือร้นที่จะพัฒนาทักษะในการจัดการภาพวาด CAD บทช่วยสอนนี้คือประตูของคุณ เราจะเจาะลึกความซับซ้อนของการตั้งค่าพื้นหลังและการวาดสีโดยใช้ Aspose.CAD สำหรับ .NET ซึ่งจะให้คำแนะนำทีละขั้นตอนเพื่อให้มั่นใจถึงความชัดเจนและประสิทธิผล

## ข้อกำหนดเบื้องต้น

ก่อนที่เราจะเริ่มต้นการเดินทางนี้ ตรวจสอบให้แน่ใจว่าคุณมีข้อกำหนดเบื้องต้นต่อไปนี้:

- ความเข้าใจพื้นฐานเกี่ยวกับการพัฒนา .NET
-  การติดตั้ง Aspose.CAD สำหรับ .NET หากคุณยังไม่ได้ทำคุณสามารถดาวน์โหลดได้[ที่นี่](https://releases.aspose.com/cad/net/).
- ไฟล์ CAD ตัวอย่างสำหรับการทดลอง คุณสามารถค้นหาได้ในไดเร็กทอรีเอกสารของคุณ

## นำเข้าเนมสเปซ

ในโปรเจ็กต์ .NET ของคุณ ให้เริ่มด้วยการนำเข้าเนมสเปซที่จำเป็น:

```csharp
using System;
using System.Collections.Generic;
using System.Linq;
using System.Text;
using System.Threading.Tasks;
using Aspose.CAD;
```

## ขั้นตอนที่ 1: โหลดไฟล์ CAD

เริ่มต้นด้วยการโหลดไฟล์ CAD ที่คุณต้องการใช้งานโดยใช้ข้อมูลโค้ดต่อไปนี้:

```csharp
string MyDir = "Your Document Directory";
string sourceFilePath = MyDir + "conic_pyramid.dxf";

using (Image image = Image.Load(sourceFilePath))
{
    // รหัสของคุณสำหรับการประมวลผลเพิ่มเติมอยู่ที่นี่
}
```

## ขั้นตอนที่ 2: กำหนดค่าตัวเลือกการแรสเตอร์

 สร้างอินสแตนซ์ของ`CadRasterizationOptions` และตั้งค่าคุณสมบัติสำหรับการตั้งค่าสีพื้นหลังและการวาด:

```csharp
CadRasterizationOptions rasterizationOptions = new CadRasterizationOptions();
rasterizationOptions.PageWidth = 1600;
rasterizationOptions.PageHeight = 1600;
rasterizationOptions.BackgroundColor = Color.Beige;
rasterizationOptions.DrawType = CadDrawTypeMode.UseDrawColor;
rasterizationOptions.DrawColor = Color.Blue;
```

## ขั้นตอนที่ 3: ส่งออกเป็น PDF

 สร้างอินสแตนซ์ของ`PdfOptions` และตั้งค่า`VectorRasterizationOptions` คุณสมบัติ:

```csharp
PdfOptions pdfOptions = new PdfOptions();
pdfOptions.VectorRasterizationOptions = rasterizationOptions;

// ส่งออก CAD เป็น PDF
image.Save(MyDir + "result_out.pdf", pdfOptions);
```

## ขั้นตอนที่ 4: ส่งออกเป็น TIFF

 สร้างอินสแตนซ์ของ`TiffOptions` และตั้งค่า`VectorRasterizationOptions` คุณสมบัติ:

```csharp
TiffOptions tiffOptions = new TiffOptions(TiffExpectedFormat.Default);
tiffOptions.VectorRasterizationOptions = rasterizationOptions;

// ส่งออก CAD เป็น TIFF
image.Save(MyDir + "result_out.tiff", tiffOptions);
```

## บทสรุป

ยินดีด้วย! คุณได้เรียนรู้วิธีการตั้งค่าสีพื้นหลังและการวาดใน Aspose.CAD สำหรับ .NET เรียบร้อยแล้ว บทช่วยสอนนี้จะช่วยให้คุณมีทักษะในการจัดการไฟล์ CAD ได้อย่างง่ายดาย

## คำถามที่พบบ่อย

### คำถามที่ 1: ฉันสามารถใช้ Aspose.CAD สำหรับ .NET กับไฟล์ CAD ประเภทใดก็ได้ได้หรือไม่

A1: ใช่ Aspose.CAD รองรับรูปแบบ CAD หลากหลาย รวมถึง DWG, DXF และ DGN

### คำถามที่ 2: Aspose.CAD สำหรับ .NET มีให้ทดลองใช้ฟรีหรือไม่

 A2: ได้ คุณสามารถทดลองใช้งานฟรีได้[ที่นี่](https://releases.aspose.com/).

### คำถามที่ 3: ฉันจะหาเอกสารโดยละเอียดสำหรับ Aspose.CAD สำหรับ .NET ได้ที่ไหน

 A3: โปรดดูเอกสารประกอบ[ที่นี่](https://reference.aspose.com/cad/net/).

### คำถามที่ 4: ฉันจะรับสิทธิ์การใช้งานชั่วคราวสำหรับ Aspose.CAD ได้อย่างไร

 A4: สามารถรับใบอนุญาตชั่วคราวได้[ที่นี่](https://purchase.aspose.com/temporary-license/).

### Q5: ต้องการความช่วยเหลือหรือต้องการเชื่อมต่อกับชุมชน?

 A5: เยี่ยมชมฟอรั่มการสนับสนุน[ที่นี่](https://forum.aspose.com/c/cad/19).

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}
