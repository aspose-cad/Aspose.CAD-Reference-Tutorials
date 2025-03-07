---
title: การสร้าง PDF แบบไดนามิกด้วย Aspose.CAD สำหรับ Java
linktitle: PDF เดียวที่มีเค้าโครงต่างกัน
second_title: Aspose.CAD Java API
description: สร้าง PDF ที่น่าทึ่งด้วยเลย์เอาต์ที่หลากหลายจากแบบร่าง CAD โดยใช้ Aspose.CAD สำหรับ Java การบูรณาการที่ง่ายดายและคุณสมบัติอันทรงพลังสำหรับนักพัฒนา Java
weight: 16
url: /th/java/other-cad-operations/single-pdf-different-layouts/
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# การสร้าง PDF แบบไดนามิกด้วย Aspose.CAD สำหรับ Java

## การแนะนำ

ยินดีต้อนรับสู่โลกของ Aspose.CAD สำหรับ Java ไลบรารีอันทรงพลังที่ช่วยให้นักพัฒนาสามารถจัดการแบบร่าง CAD ได้อย่างง่ายดาย ในบทช่วยสอนนี้ เราจะเจาะลึกเกี่ยวกับการสร้าง PDF ไฟล์เดียวที่มีเลย์เอาต์ที่แตกต่างกันโดยใช้ Aspose.CAD สำหรับ Java ไม่ว่าคุณจะเป็นนักพัฒนาที่มีประสบการณ์หรือเพิ่งเริ่มต้น คำแนะนำทีละขั้นตอนนี้จะแนะนำคุณตลอดกระบวนการ

## ข้อกำหนดเบื้องต้น

ก่อนที่เราจะเริ่มต้นการเดินทางครั้งนี้ ตรวจสอบให้แน่ใจว่าคุณมีข้อกำหนดเบื้องต้นต่อไปนี้:
- สภาพแวดล้อม Java: ตรวจสอบให้แน่ใจว่าคุณได้ติดตั้ง Java บนเครื่องของคุณแล้ว
-  ไลบรารี Aspose.CAD: ดาวน์โหลดและติดตั้งไลบรารี Aspose.CAD สำหรับ Java จาก[ลิ้งค์ดาวน์โหลด](https://releases.aspose.com/cad/java/).
- ไดเร็กทอรีเอกสาร: ตั้งค่าไดเร็กทอรีสำหรับภาพวาด DWG ของคุณ

## แพ็คเกจนำเข้า

ในโปรเจ็กต์ Java ของคุณ ให้นำเข้าแพ็คเกจที่จำเป็น:

```java
import com.aspose.cad.Image;
import com.aspose.cad.SizeF;
import com.aspose.cad.fileformats.cad.CadImage;
import com.aspose.cad.imageoptions.CadRasterizationOptions;
import com.aspose.cad.imageoptions.PdfOptions;
import com.aspose.cad.imageoptions.VectorRasterizationOptions;
```

## ขั้นตอนที่ 1: โหลด CAD Drawing

 เริ่มต้นด้วยการโหลดแบบ CAD ของคุณลงใน`CadImage` วัตถุ:

```java
String dataDir = "Your Document Directory" + "DWGDrawings/";
CadImage cadImage = (CadImage)Image.load(dataDir + "City skyway map.dwg");
```

## ขั้นตอนที่ 2: กำหนดค่าตัวเลือกการแรสเตอร์

ตั้งค่าตัวเลือกการแรสเตอร์สำหรับรูปภาพ CAD:

```java
CadRasterizationOptions rasterizationOptions = new CadRasterizationOptions();
rasterizationOptions.setPageWidth(1000);
rasterizationOptions.setPageHeight(1000);
```

## ขั้นตอนที่ 3: ปรับแต่งขนาดหน้าเค้าโครง

กำหนดขนาดที่กำหนดเองสำหรับเลย์เอาต์ต่างๆ ภายในแบบร่าง CAD:

```java
rasterizationOptions.getLayoutPageSizes().addItem("ANSI C Plot", new SizeF(500, 1000));
rasterizationOptions.getLayoutPageSizes().addItem("8.5 x 11 Plot", new SizeF(1000, 100));
```

## ขั้นตอนที่ 4: ตั้งค่าตัวเลือก PDF

กำหนดค่าตัวเลือก PDF โดยรวมการตั้งค่าแรสเตอร์:

```java
PdfOptions pdfOptions = new PdfOptions();
pdfOptions.setVectorRasterizationOptions(rasterizationOptions);
```

## ขั้นตอนที่ 5: บันทึกเป็น PDF

บันทึกภาพ CAD ที่ประมวลผลเป็น PDF:

```java
cadImage.save(dataDir + "singlePDF_out.pdf", pdfOptions);
```

ยินดีด้วย! คุณสร้าง PDF ไฟล์เดียวที่มีเค้าโครงต่างกันโดยใช้ Aspose.CAD สำหรับ Java สำเร็จแล้ว

## บทสรุป

ในบทช่วยสอนนี้ เราได้สำรวจการบูรณาการอย่างราบรื่นของ Aspose.CAD สำหรับ Java เพื่อสร้าง PDF ที่มีเค้าโครงที่หลากหลายจากแบบร่าง CAD ความยืดหยุ่นและคุณสมบัติที่แข็งแกร่งของไลบรารีทำให้เป็นตัวเลือกสำหรับงานจัดการ CAD

## คำถามที่พบบ่อย

### คำถามที่ 1: ฉันสามารถใช้ Aspose.CAD สำหรับ Java กับไลบรารี Java อื่นได้หรือไม่

ตอบ 1: ใช่ Aspose.CAD สำหรับ Java ได้รับการออกแบบมาเพื่อผสานรวมกับไลบรารี Java อื่นๆ ได้อย่างราบรื่น โดยมีฟังก์ชันการทำงานที่ครอบคลุม

### คำถามที่ 2: มีเวอร์ชันทดลองใช้งานหรือไม่

 A2: แน่นอน! คุณสามารถเข้าถึงเวอร์ชันทดลองใช้ฟรีได้[ที่นี่](https://releases.aspose.com/).

### คำถามที่ 3: ฉันจะรับการสนับสนุนเพิ่มเติมได้จากที่ไหน

 A3: เยี่ยมชม[ฟอรั่ม Aspose.CAD](https://forum.aspose.com/c/cad/19) สำหรับการสนับสนุนและการอภิปรายของชุมชน

### คำถามที่ 4: ฉันจะขอรับใบอนุญาตชั่วคราวได้อย่างไร

 A4: คุณสามารถขอรับใบอนุญาตชั่วคราวได้[ที่นี่](https://purchase.aspose.com/temporary-license/).

### คำถามที่ 5: ฉันจะซื้อเวอร์ชันเต็มได้ที่ไหน

A5: ซื้อเวอร์ชันเต็มของ Aspose.CAD สำหรับ Java[ที่นี่](https://purchase.aspose.com/buy).
{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}
