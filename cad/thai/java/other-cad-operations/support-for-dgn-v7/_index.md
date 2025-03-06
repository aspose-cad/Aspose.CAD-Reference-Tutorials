---
title: คู่มือการแปลง DGN เป็น PDF - Aspose.CAD สำหรับ Java
linktitle: รองรับ DGN V7
second_title: Aspose.CAD Java API
description: แปลงไฟล์ DGN เป็น PDF ได้อย่างง่ายดายโดยใช้ Aspose.CAD สำหรับ Java ปฏิบัติตามคำแนะนำทีละขั้นตอนของเราเพื่อการบูรณาการที่ราบรื่นและขั้นตอนการทำงานที่มีประสิทธิภาพ
weight: 11
url: /th/java/other-cad-operations/support-for-dgn-v7/
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# คู่มือการแปลง DGN เป็น PDF - Aspose.CAD สำหรับ Java

## การแนะนำ

ในโลกที่มีการเปลี่ยนแปลงตลอดเวลาของ CAD (Computer-Aided Design) การแปลงไฟล์ DGN (การออกแบบ) เป็น PDF (Portable Document Format) อย่างมีประสิทธิภาพถือเป็นข้อกำหนดที่สำคัญ Aspose.CAD สำหรับ Java กลายเป็นโซลูชันที่ทรงพลัง นำเสนอการบูรณาการที่ราบรื่นและความสามารถที่แข็งแกร่ง คำแนะนำทีละขั้นตอนนี้มีจุดมุ่งหมายเพื่อแนะนำคุณตลอดกระบวนการส่งออกไฟล์ DGN เป็น PDF โดยใช้ Aspose.CAD สำหรับ Java เพื่อให้มั่นใจว่าขั้นตอนการทำงานจะราบรื่นและมีประสิทธิภาพ

## ข้อกำหนดเบื้องต้น

ก่อนที่จะเข้าสู่บทช่วยสอน ตรวจสอบให้แน่ใจว่าคุณมีข้อกำหนดเบื้องต้นต่อไปนี้:
-  Aspose.CAD สำหรับ Java Library: ดาวน์โหลดและติดตั้งไลบรารีจากไฟล์[Aspose.CAD สำหรับหน้าดาวน์โหลด Java](https://releases.aspose.com/cad/java/).
- สภาพแวดล้อมการพัฒนา Java: ตรวจสอบให้แน่ใจว่าคุณได้ตั้งค่าสภาพแวดล้อมการพัฒนา Java บนเครื่องของคุณ

## แพ็คเกจนำเข้า

เริ่มต้นด้วยการนำเข้าแพ็คเกจที่จำเป็นไปยังโปรเจ็กต์ Java ของคุณ:

## ขั้นตอนที่ 1: นำเข้าแพ็คเกจที่จำเป็น

ในโปรเจ็กต์ Java ของคุณ ให้นำเข้าแพ็คเกจที่จำเป็นสำหรับ Aspose.CAD สำหรับ Java
```java
import com.aspose.cad.Image;
import com.aspose.cad.fileformats.cad.CadRasterizationOptions;
import com.aspose.cad.fileformats.cad.cadobjects.DgnImage;
import com.aspose.cad.imageoptions.PdfOptions;
import java.awt.Color;
```

## ขั้นตอนที่ 2: ตั้งค่าเส้นทางไฟล์

กำหนดเส้นทางสำหรับไฟล์ DGN อินพุตและไฟล์ PDF เอาต์พุต

```java
String dataDir = "Your Document Directory" + "ExportingDGN/";
String fileName = dataDir + "Nikon_D90_Camera.dgn";
String outFile  = dataDir + "Nikon_D90_Camera.pdf";
```

## ขั้นตอนที่ 3: โหลดอิมเมจ DGN

โหลดอิมเมจ DGN โดยใช้ไลบรารี Aspose.CAD

```java
DgnImage objImage = (DgnImage)Image.load(fileName);
```

## ขั้นตอนที่ 4: กำหนดค่าตัวเลือกการส่งออก PDF

ตั้งค่าตัวเลือกสำหรับการส่งออกเป็น PDF รวมถึงขนาดหน้า การปรับขนาดเค้าโครงอัตโนมัติ สีพื้นหลัง และเค้าโครงเฉพาะที่จะส่งออก

```java
PdfOptions options = new PdfOptions();
CadRasterizationOptions vectorOptions = new CadRasterizationOptions();
vectorOptions.setPageWidth(1500);
vectorOptions.setPageHeight(1500);
vectorOptions.setAutomaticLayoutsScaling(true);
vectorOptions.setBackgroundColor(Color.getBlack());
vectorOptions.setLayouts(new String[] { "1", "2", "3", "9" }); //ส่งออกมุมมอง 4 (1,2,3 และ 9) เท่านั้น
options.setVectorRasterizationOptions(vectorOptions);
```

## ขั้นตอนที่ 5: บันทึกไฟล์ PDF

บันทึกรูปภาพ DGN เป็นไฟล์ PDF ด้วยตัวเลือกที่ระบุ

```java
objImage.save(outFile, options);
```

ทำซ้ำขั้นตอนเหล่านี้สำหรับไฟล์ DGN ต่างๆ ปรับเส้นทางไฟล์และตัวเลือกตามต้องการ

## บทสรุป

ด้วย Aspose.CAD สำหรับ Java การแปลงไฟล์ DGN เป็น PDF จะกลายเป็นกระบวนการที่ไม่ซับซ้อน คู่มือนี้จะช่วยให้คุณมีความรู้ในการผสานรวมไลบรารีเข้ากับโปรเจ็กต์ Java ของคุณได้อย่างราบรื่น ซึ่งช่วยอำนวยความสะดวกในการแปลงไฟล์ CAD ที่มีประสิทธิภาพ

## คำถามที่พบบ่อย

### คำถามที่ 1: ฉันสามารถใช้ Aspose.CAD สำหรับ Java กับไฟล์ CAD รูปแบบอื่นได้หรือไม่

ตอบ 1: ใช่ Aspose.CAD รองรับรูปแบบ CAD หลากหลายรูปแบบ โดยมีฟังก์ชันการทำงานที่หลากหลายนอกเหนือจากการแปลง DGN เป็น PDF

### คำถามที่ 2: Aspose.CAD สำหรับ Java มีใบอนุญาตชั่วคราวหรือไม่

 A2: ได้ คุณสามารถขอรับใบอนุญาตชั่วคราวได้[ที่นี่](https://purchase.aspose.com/temporary-license/) เพื่อวัตถุประสงค์ในการทดสอบ

### คำถามที่ 3: ฉันจะขอรับการสนับสนุนหรือถามคำถามเกี่ยวกับ Aspose.CAD สำหรับ Java ได้อย่างไร

 A3: เยี่ยมชม[ฟอรั่ม Aspose.CAD](https://forum.aspose.com/c/cad/19)เพื่อเชื่อมต่อกับชุมชนและขอความช่วยเหลือ

### คำถามที่ 4: ฉันสามารถส่งออกเค้าโครงใดได้บ้างเมื่อแปลง DGN เป็น PDF

 A4: คุณสามารถระบุเค้าโครงที่จะส่งออกได้โดยการปรับแต่ง`setLayouts` อาร์เรย์ในโค้ด

### คำถามที่ 5: ฉันจะหาเอกสารที่ครอบคลุมสำหรับ Aspose.CAD สำหรับ Java ได้ที่ไหน

 A5: โปรดดูที่[Aspose.CAD สำหรับเอกสาร Java](https://reference.aspose.com/cad/java/) สำหรับข้อมูลโดยละเอียด
{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}
