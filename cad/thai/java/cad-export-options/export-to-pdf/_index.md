---
title: ส่งออกเป็น PDF ด้วย Aspose.CAD สำหรับ Java
linktitle: ส่งออกเป็น PDF
second_title: Aspose.CAD Java API
description: เรียนรู้วิธีส่งออกไฟล์ CAD เป็น PDF ได้อย่างง่ายดายด้วย Aspose.CAD สำหรับ Java ปฏิบัติตามคำแนะนำทีละขั้นตอนของเราเพื่อการบูรณาการที่ราบรื่น
weight: 13
url: /th/java/cad-export-options/export-to-pdf/
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# ส่งออกเป็น PDF ด้วย Aspose.CAD สำหรับ Java

## การแนะนำ

ยินดีต้อนรับสู่บทช่วยสอนที่ครอบคลุมเกี่ยวกับการส่งออกไฟล์ CAD เป็น PDF โดยใช้ Aspose.CAD สำหรับ Java หากคุณต้องการแปลงแบบร่าง CAD ของคุณเป็นรูปแบบ PDF ที่รองรับอย่างกว้างขวางได้อย่างราบรื่น คุณมาถูกที่แล้ว ในคำแนะนำทีละขั้นตอนนี้ เราจะแจกแจงรายละเอียดกระบวนการ เพื่อให้มั่นใจว่าคุณเข้าใจแต่ละขั้นตอนเพื่อให้ส่งออก PDF ได้สำเร็จ

## ข้อกำหนดเบื้องต้น

ก่อนที่จะเข้าสู่บทช่วยสอน ตรวจสอบให้แน่ใจว่าคุณมีข้อกำหนดเบื้องต้นต่อไปนี้:

-  Aspose.CAD สำหรับ Java: ตรวจสอบให้แน่ใจว่าคุณได้ติดตั้งไลบรารี Aspose.CAD ในสภาพแวดล้อม Java ของคุณ คุณสามารถดาวน์โหลดได้[ที่นี่](https://releases.aspose.com/cad/java/).

- ไดเรกทอรีทรัพยากร: ตั้งค่าไดเรกทอรีสำหรับจัดเก็บไฟล์ CAD ของคุณ แทนที่ "ไดเรกทอรีเอกสารของคุณ" ในข้อมูลโค้ดที่ให้มาด้วยเส้นทางจริง

ตอนนี้เรามาดูขั้นตอนหลักกันดีกว่า

## นำเข้าเนมสเปซ

ในโปรเจ็กต์ Java ของคุณ ให้เริ่มต้นด้วยการนำเข้าเนมสเปซที่จำเป็นเพื่อเปิดใช้งานฟังก์ชัน Aspose.CAD

```java
import com.aspose.cad.Image;
import com.aspose.cad.InterpolationMode;
import com.aspose.cad.SmoothingMode;
import com.aspose.cad.TextRenderingHint;

import com.aspose.cad.imageoptions.CadRasterizationOptions;
import com.aspose.cad.imageoptions.PdfOptions;
//นำเข้า com.aspose.cad.imageoptions.TypeOfEntities;
```

## ขั้นตอนที่ 1: โหลดไฟล์ CAD

โหลดไฟล์ CAD ของคุณลงในวัตถุ Aspose.CAD Image แทนที่ "site.dwf" ด้วยชื่อไฟล์ CAD จริงของคุณ

```java
String fileName = (dataDir + "site.dwf");
Image image = Image.load(fileName);
```

## ขั้นตอนที่ 2: กำหนดค่าตัวเลือก PDF

ตั้งค่าตัวเลือกการส่งออก PDF รวมถึงตัวเลือกการแรสเตอร์เวกเตอร์ เช่น ความสูงของหน้า ความกว้าง และเค้าโครง

```java
PdfOptions pdfOptions = new PdfOptions();
CadRasterizationOptions rasterizationOptions = new CadRasterizationOptions();
pdfOptions.setVectorRasterizationOptions(rasterizationOptions);

rasterizationOptions.setPageHeight(500);
rasterizationOptions.setPageWidth(500);
rasterizationOptions.setLayouts(new String[] { "Model" });
```

## ขั้นตอนที่ 3: ส่งออกเป็น PDF

ระบุเส้นทางเอาต์พุตสำหรับไฟล์ PDF ที่สร้างขึ้น และบันทึกรูปภาพด้วยตัวเลือก PDF ที่กำหนดค่าไว้

```java
String outPath = dataDir + "site.pdf";
image.save(outPath, pdfOptions);
```

ยินดีด้วย! คุณได้ส่งออกไฟล์ CAD ของคุณเป็น PDF โดยใช้ Aspose.CAD สำหรับ Java สำเร็จแล้ว

## บทสรุป

ในบทช่วยสอนนี้ เราได้สำรวจกระบวนการส่งออกไฟล์ CAD เป็น PDF ทีละขั้นตอนโดยใช้ Aspose.CAD สำหรับ Java ด้วยการทำตามขั้นตอนง่ายๆ แต่มีประสิทธิภาพเหล่านี้ คุณสามารถรวมฟังก์ชันการทำงานนี้เข้ากับแอปพลิเคชัน Java ของคุณได้อย่างราบรื่น

## คำถามที่พบบ่อย

### คำถามที่ 1: Aspose.CAD เข้ากันได้กับไฟล์ CAD ทุกรูปแบบหรือไม่

ตอบ 1: ใช่ Aspose.CAD รองรับรูปแบบ CAD ที่หลากหลาย ทำให้มั่นใจได้ถึงความเข้ากันได้กับซอฟต์แวร์การออกแบบต่างๆ

### คำถามที่ 2: ฉันสามารถปรับแต่งการตั้งค่าเอาต์พุต PDF ได้หรือไม่

A2: แน่นอน. บทช่วยสอนจะแสดงตัวเลือกการปรับแต่งคร่าวๆ แต่คุณสามารถสำรวจเพิ่มเติมเพื่อปรับแต่งผลลัพธ์ตามความต้องการของคุณได้

### คำถามที่ 3: ฉันจะรับการสนับสนุนเพิ่มเติมสำหรับ Aspose.CAD ได้ที่ไหน

 A3: สำหรับข้อสงสัยหรือปัญหาใดๆ โปรดไปที่[ฟอรั่ม Aspose.CAD](https://forum.aspose.com/c/cad/19) เพื่อขอความช่วยเหลือจากชุมชน

### คำถามที่ 4: มีการทดลองใช้ฟรีหรือไม่?

 A4: ได้ คุณสามารถเข้าถึง Aspose.CAD รุ่นทดลองใช้ฟรีได้[ที่นี่](https://releases.aspose.com/).

### คำถามที่ 5: ฉันจะขอรับใบอนุญาตชั่วคราวสำหรับ Aspose.CAD ได้อย่างไร

 A5: สำหรับใบอนุญาตชั่วคราว โปรดไปที่[ลิงค์นี้](https://purchase.aspose.com/temporary-license/).
{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}
