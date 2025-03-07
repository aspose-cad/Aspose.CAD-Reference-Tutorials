---
title: ส่งออก DGN เป็น AutoCAD PDF ได้อย่างง่ายดายด้วย Aspose.CAD สำหรับ Java
linktitle: ส่งออก DGN ในรูปแบบ AutoCAD เป็น PDF
second_title: Aspose.CAD Java API
description: สำรวจคำแนะนำทีละขั้นตอนในการส่งออกไฟล์ DGN เป็นรูปแบบ AutoCAD ในรูปแบบ PDF โดยใช้ Aspose.CAD สำหรับ Java ยกระดับความสามารถในการจัดการ CAD ของแอปพลิเคชัน Java ของคุณได้อย่างง่ายดาย
weight: 12
url: /th/java/dgn-export-options/exporting-dgn-to-pdf/
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# ส่งออก DGN เป็น AutoCAD PDF ได้อย่างง่ายดายด้วย Aspose.CAD สำหรับ Java

## การแนะนำ

ยินดีต้อนรับสู่บทช่วยสอนที่ครอบคลุมเกี่ยวกับการใช้ Aspose.CAD สำหรับ Java เพื่อส่งออกไฟล์ DGN ในรูปแบบ AutoCAD เป็น PDF หากคุณต้องการเพิ่มขีดความสามารถของแอปพลิเคชัน Java ของคุณในการจัดการไฟล์ CAD Aspose.CAD เป็นตัวเลือกที่ยอดเยี่ยม ในบทช่วยสอนนี้ เราจะแนะนำคุณตลอดขั้นตอนการส่งออกไฟล์ DGN ทีละขั้นตอน


## ข้อกำหนดเบื้องต้น
ก่อนที่เราจะเจาะลึกบทช่วยสอน ตรวจสอบให้แน่ใจว่าคุณมีข้อกำหนดเบื้องต้นดังต่อไปนี้:
-  ไลบรารี Aspose.CAD: ตรวจสอบให้แน่ใจว่าคุณได้ติดตั้งไลบรารี Aspose.CAD สำหรับ Java แล้ว คุณสามารถดาวน์โหลดได้[ที่นี่](https://releases.aspose.com/cad/java/).
- ไดเร็กทอรีเอกสาร: ตั้งค่าไดเร็กทอรีเอกสารที่จะจัดเก็บไฟล์อินพุตและเอาต์พุตของคุณ

## แพ็คเกจนำเข้า

ในโปรเจ็กต์ Java ของคุณ ให้นำเข้าแพ็คเกจที่จำเป็นเพื่อเข้าถึงฟังก์ชัน Aspose.CAD:

```java
import java.io.FileNotFoundException;
import java.io.FileOutputStream;
import java.io.OutputStream;
import com.aspose.cad.Image;
import com.aspose.cad.fileformats.dgn.DgnImage;
import com.aspose.cad.imageoptions.CadRasterizationOptions;
import com.aspose.cad.imageoptions.PdfOptions;
```

ตอนนี้ เรามาแบ่งโค้ดตัวอย่างออกเป็นหลายขั้นตอน:

## ขั้นตอนที่ 1: กำหนดเส้นทางไฟล์

```java
String dataDir = "Your Document Directory" + "ExportingDGN/";
String fileName = dataDir + "Nikon_D90_Camera.dgn";
String outFile  = dataDir + "Nikon_D90_Camera.pdf";
```

ตรวจสอบให้แน่ใจว่าได้แทนที่ "Your Document Directory" ด้วยเส้นทางจริงที่มีไฟล์ของคุณอยู่

## ขั้นตอนที่ 2: โหลดอิมเมจ DGN

```java
DgnImage objImage = (DgnImage) Image.load(fileName);
```

โหลดไฟล์ DGN โดยใช้ Aspose.CAD

## ขั้นตอนที่ 3: ตั้งค่าตัวเลือกการส่งออก PDF

```java
PdfOptions options = new PdfOptions();
CadRasterizationOptions vectorOptions = new CadRasterizationOptions();
vectorOptions.setPageWidth(1500);
vectorOptions.setPageHeight(1500);
vectorOptions.setAutomaticLayoutsScaling(true);
vectorOptions.setLayouts(new String[] { "1", "2", "3", "9" }); // ส่งออกมุมมองเฉพาะ
options.setVectorRasterizationOptions(vectorOptions);
```

กำหนดตัวเลือกการส่งออก PDF รวมถึงขนาดหน้าและการกำหนดลักษณะเค้าโครง

## ขั้นตอนที่ 4: บันทึกไฟล์ PDF

```java
objImage.save(outFile, options);
```

บันทึกไฟล์ PDF ที่ส่งออก

ทำซ้ำขั้นตอนเหล่านี้สำหรับไฟล์ DGN เพิ่มเติมที่คุณต้องการแปลง ยินดีด้วย! คุณได้ส่งออกไฟล์ DGN เป็นรูปแบบ AutoCAD ในรูปแบบ PDF ได้สำเร็จโดยใช้ Aspose.CAD สำหรับ Java

## บทสรุป

ในบทช่วยสอนนี้ เราได้สำรวจวิธีใช้ประโยชน์จาก Aspose.CAD สำหรับ Java เพื่อปรับปรุงความสามารถในการจัดการไฟล์ CAD ของแอปพลิเคชันของคุณ ด้วยขั้นตอนและตัวอย่างโค้ดที่ปฏิบัติตามได้ง่าย ตอนนี้คุณสามารถส่งออกไฟล์ DGN เป็นรูปแบบ AutoCAD ในรูปแบบ PDF ได้อย่างราบรื่น

## คำถามที่พบบ่อย

### คำถามที่ 1: Aspose.CAD เข้ากันได้กับไฟล์ CAD ทุกรูปแบบหรือไม่

ตอบ 1: ใช่ Aspose.CAD รองรับรูปแบบ CAD ที่หลากหลาย ทำให้มั่นใจได้ถึงความคล่องตัวในการจัดการไฟล์ประเภทต่างๆ

### คำถามที่ 2: ฉันสามารถปรับแต่งการตั้งค่าการส่งออก PDF ได้หรือไม่

A2: แน่นอน. ดังที่แสดงในบทช่วยสอน คุณสามารถปรับเปลี่ยนตัวเลือกต่างๆ เช่น ขนาดหน้าและเค้าโครงเพื่อให้เหมาะกับความต้องการของคุณได้

### คำถามที่ 3: ฉันจะรับการสนับสนุนหรือความช่วยเหลือเพิ่มเติมได้จากที่ไหน

 A3: เยี่ยมชม[ฟอรั่ม Aspose.CAD](https://forum.aspose.com/c/cad/19) สำหรับการสนับสนุนและการอภิปรายของชุมชน

### คำถามที่ 4: มีการทดลองใช้ฟรีหรือไม่?

 A4: ได้ คุณสามารถเข้าถึงรุ่นทดลองใช้ฟรีได้[ที่นี่](https://releases.aspose.com/).

### คำถามที่ 5: ฉันจะขอรับใบอนุญาตชั่วคราวได้อย่างไร

 A5: รับใบอนุญาตชั่วคราว[ที่นี่](https://purchase.aspose.com/temporary-license/).
{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}
