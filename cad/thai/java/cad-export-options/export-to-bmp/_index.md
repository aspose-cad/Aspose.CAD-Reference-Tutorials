---
title: ส่งออกเป็น BMP ด้วย Aspose.CAD สำหรับ Java
linktitle: ส่งออกเป็น BMP
second_title: Aspose.CAD Java API
description: สำรวจการแปลง CAD เป็น BMP อย่างราบรื่นด้วย Aspose.CAD สำหรับ Java ปฏิบัติตามคำแนะนำทีละขั้นตอนของเราเพื่อการส่งออกที่มีประสิทธิภาพและแม่นยำ
weight: 12
url: /th/java/cad-export-options/export-to-bmp/
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# ส่งออกเป็น BMP ด้วย Aspose.CAD สำหรับ Java

## การแนะนำ

ในการออกแบบดิจิทัลที่มีการเปลี่ยนแปลงตลอดเวลา ความสามารถในการส่งออกไฟล์ Computer-Aided Design (CAD) ไปยังรูปแบบต่างๆ ได้อย่างราบรื่นถือเป็นสิ่งสำคัญ Aspose.CAD สำหรับ Java โดดเด่นในฐานะโซลูชันอันทรงพลัง โดยมอบเครื่องมือที่จำเป็นสำหรับนักพัฒนาในการส่งออกไฟล์ CAD เป็นรูปแบบ BMP ได้อย่างมีประสิทธิภาพ บทช่วยสอนนี้จะแนะนำคุณตลอดกระบวนการทีละขั้นตอน เพื่อให้มั่นใจว่าการส่งออกจะราบรื่นและประสบความสำเร็จทุกครั้ง

## ข้อกำหนดเบื้องต้น

ก่อนที่จะเข้าสู่บทช่วยสอน ตรวจสอบให้แน่ใจว่าคุณมีข้อกำหนดเบื้องต้นต่อไปนี้:

- Aspose.CAD สำหรับไลบรารี Java: ดาวน์โหลดและติดตั้ง Aspose.CAD สำหรับไลบรารี Java จาก[ที่นี่](https://releases.aspose.com/cad/java/).

- สภาพแวดล้อมการพัฒนา Java: ตรวจสอบให้แน่ใจว่าคุณได้ตั้งค่าสภาพแวดล้อมการพัฒนา Java บนระบบของคุณ

- ความรู้ Java ขั้นพื้นฐาน: ทำความคุ้นเคยกับแนวคิดการเขียนโปรแกรม Java ขั้นพื้นฐาน

## นำเข้าเนมสเปซ

ในโปรเจ็กต์ Java ของคุณ ให้นำเข้าเนมสเปซที่จำเป็นเพื่อเข้าถึงฟังก์ชันการทำงานของ Aspose.CAD:

```java
import com.aspose.cad.Image;
import com.aspose.cad.InterpolationMode;
import com.aspose.cad.SmoothingMode;
import com.aspose.cad.TextRenderingHint;

import com.aspose.cad.imageoptions.BmpOptions;
import com.aspose.cad.imageoptions.CadRasterizationOptions;
import com.aspose.cad.imageoptions.PdfOptions;
//นำเข้า com.aspose.cad.imageoptions.TypeOfEntities;
```

## ขั้นตอนที่ 1: ตั้งค่าเส้นทางไดเรกทอรีทรัพยากร

เริ่มต้นด้วยการกำหนดเส้นทางไปยังไดเร็กทอรีทรัพยากรของคุณซึ่งมีไฟล์ CAD อยู่

```java
String dataDir = "Your Document Directory" + "ExportingCAD/";
```

## ขั้นตอนที่ 2: โหลดไฟล์ CAD

 โหลดไฟล์ CAD ลงใน Aspose.CAD`Image` วัตถุ.

```java
String fileName = (dataDir + "site.dwf");
Image image = Image.load(fileName);
```

## ขั้นตอนที่ 3: กำหนดค่าตัวเลือกการส่งออก BMP

สร้างและกำหนดค่าตัวเลือกการส่งออก BMP รวมถึงการตั้งค่าแรสเตอร์

```java
BmpOptions bmpOptions = new BmpOptions();
CadRasterizationOptions rasterizationOptions = new CadRasterizationOptions();
bmpOptions.setVectorRasterizationOptions(rasterizationOptions);
```

## ขั้นตอนที่ 4: ตั้งค่าพารามิเตอร์การแรสเตอร์

กำหนดพารามิเตอร์ เช่น ความสูงของหน้า ความกว้างของหน้า และเค้าโครงสำหรับการแรสเตอร์

```java
rasterizationOptions.setPageHeight(500);
rasterizationOptions.setPageWidth(500);
rasterizationOptions.setLayouts(new String[] { "Model" });
```

## ขั้นตอนที่ 5: ส่งออกเป็น BMP

ระบุเส้นทางเอาต์พุตและบันทึกไฟล์ BMP

```java
String outPath = dataDir + "site.bmp";
image.save(outPath, bmpOptions);
```

ทำซ้ำขั้นตอนเหล่านี้สำหรับไฟล์ CAD แต่ละไฟล์ที่คุณต้องการส่งออกไปยัง BMP โดยใช้ Aspose.CAD สำหรับ Java

## บทสรุป

ส่งออกไฟล์ CAD เป็นรูปแบบ BMP ได้อย่างง่ายดายด้วย Aspose.CAD สำหรับ Java ด้วยการทำตามคำแนะนำทีละขั้นตอนนี้ คุณสามารถรวมฟังก์ชันการทำงานนี้เข้ากับแอปพลิเคชัน Java ของคุณได้อย่างราบรื่น รับรองการแปลงที่มีประสิทธิภาพและแม่นยำ

## คำถามที่พบบ่อย

### คำถามที่ 1: Aspose.CAD สำหรับ Java เหมาะสำหรับการประมวลผลเป็นชุดหรือไม่

A1: แน่นอน! Aspose.CAD สำหรับ Java รองรับการประมวลผลเป็นชุด ช่วยให้คุณสามารถจัดการไฟล์ CAD หลายไฟล์พร้อมกันได้อย่างมีประสิทธิภาพ

### คำถามที่ 2: ฉันสามารถปรับแต่งตัวเลือกการแรสเตอร์สำหรับเลย์เอาต์ต่างๆ ได้หรือไม่

ตอบ 2: ได้ คุณสามารถปรับแต่งตัวเลือกการแรสเตอร์ เช่น ขนาดหน้าและเค้าโครงได้ตามความต้องการเฉพาะของคุณ

### คำถามที่ 3: ฉันจะรับการสนับสนุนเพิ่มเติมสำหรับ Aspose.CAD สำหรับ Java ได้ที่ไหน

 A3: เยี่ยมชม[ฟอรั่ม Aspose.CAD](https://forum.aspose.com/c/cad/19) สำหรับการสนับสนุนและการอภิปรายของชุมชน

### คำถามที่ 4: มีการทดลองใช้ฟรีหรือไม่?

 A4: ได้ คุณสามารถทดลองใช้ Aspose.CAD สำหรับ Java ได้ฟรี[ที่นี่](https://releases.aspose.com/).

### คำถามที่ 5: ฉันจะขอรับใบอนุญาตชั่วคราวได้อย่างไร

 A5: รับใบอนุญาตชั่วคราวสำหรับ Aspose.CAD สำหรับ Java[ที่นี่](https://purchase.aspose.com/temporary-license/).
{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}
