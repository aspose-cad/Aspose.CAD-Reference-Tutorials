---
title: ส่งออก DGN แบบฝังเป็น PDF ด้วย Aspose.CAD สำหรับ Java
linktitle: ส่งออก DGN แบบฝัง
second_title: Aspose.CAD Java API
description: สำรวจคำแนะนำทีละขั้นตอนในการส่งออกไฟล์ DGN ที่ฝังไว้เป็น PDF โดยใช้ Aspose.CAD สำหรับ Java ปรับปรุงแอปพลิเคชัน Java ของคุณด้วยการจัดการไฟล์ CAD ได้อย่างราบรื่น
type: docs
weight: 11
url: /th/java/dgn-export-options/export-embedded-dgn/
---
## การแนะนำ

ยินดีต้อนรับสู่บทช่วยสอนที่ครอบคลุมเกี่ยวกับการส่งออกไฟล์ DGN ที่ฝังไว้โดยใช้ Aspose.CAD สำหรับ Java Aspose.CAD เป็นไลบรารีอันทรงพลังที่ช่วยให้นักพัฒนา Java สามารถทำงานกับไฟล์ CAD ได้อย่างราบรื่น ในบทช่วยสอนนี้ เราจะแนะนำคุณตลอดขั้นตอนการส่งออกไฟล์ DGN ที่ฝังไว้เป็น PDF โดยใช้คำแนะนำทีละขั้นตอน ไม่ว่าคุณจะเป็นนักพัฒนาที่มีประสบการณ์หรือเพิ่งเริ่มต้น บทช่วยสอนนี้จะช่วยให้คุณควบคุมความสามารถของ Aspose.CAD เพื่อปรับปรุงแอปพลิเคชัน Java ของคุณ

## ข้อกำหนดเบื้องต้น

ก่อนที่เราจะเจาะลึกบทช่วยสอน ตรวจสอบให้แน่ใจว่าคุณมีข้อกำหนดเบื้องต้นดังต่อไปนี้:
- สภาพแวดล้อมการพัฒนา Java: ตรวจสอบให้แน่ใจว่าคุณได้ตั้งค่าสภาพแวดล้อมการพัฒนา Java บนเครื่องของคุณ
-  Aspose.CAD สำหรับ Java: ดาวน์โหลดและติดตั้ง Aspose.CAD สำหรับไลบรารี Java จาก[ที่นี่](https://releases.aspose.com/cad/java/).

## แพ็คเกจนำเข้า

ในการเริ่มต้น คุณต้องนำเข้าแพ็คเกจที่จำเป็นในโปรเจ็กต์ Java ของคุณ เพิ่มคำสั่งการนำเข้าต่อไปนี้ลงในโค้ดของคุณ:

```java
import java.io.FileNotFoundException;
import java.io.FileOutputStream;
import java.io.OutputStream;
import com.aspose.cad.Image;
import com.aspose.cad.ImageOptionsBase;
import com.aspose.cad.fileformats.cad.CadImage;
import com.aspose.cad.fileformats.dgn.DgnImage;
import com.aspose.cad.imageoptions.CadRasterizationOptions;
import com.aspose.cad.imageoptions.JpegOptions;
import com.aspose.cad.imageoptions.PdfOptions;
```

ตอนนี้ เรามาแบ่งโค้ดตัวอย่างออกเป็นหลายขั้นตอน:

## ขั้นตอนที่ 1: ตั้งค่าเส้นทางอินพุตและเอาต์พุต

กำหนดเส้นทางไดเร็กทอรีที่มีเอกสารของคุณอยู่และระบุชื่อไฟล์ DWG อินพุต

```java
String dataDir = "Your Document Directory" + "ExportingDGN/";
String fileName = dataDir + "BlockRefDgn.dwg";
```

## ขั้นตอนที่ 2: โหลดไฟล์ DWG

 โหลดไฟล์ DWG ลงในไฟล์`Image` วัตถุโดยใช้ Aspose.CAD

```java
Image objImage = Image.load(fileName);
```

## ขั้นตอนที่ 3: กำหนดค่าตัวเลือกการแรสเตอร์

กำหนดค่าตัวเลือกการแรสเตอร์ เช่น เค้าโครงที่จะรวมไว้ในการส่งออก

```java
CadRasterizationOptions rasterizationOptions = new CadRasterizationOptions();
rasterizationOptions.setLayouts(new String[] {"Model"});
```

## ขั้นตอนที่ 4: กำหนดค่าตัวเลือก PDF

ตั้งค่าตัวเลือก PDF รวมถึงตัวเลือกการแรสเตอร์เวกเตอร์

```java
PdfOptions pdfOptions = new PdfOptions();
pdfOptions.setVectorRasterizationOptions(rasterizationOptions);
```

## ขั้นตอนที่ 5: บันทึกไฟล์ PDF

บันทึกไฟล์ PDF ด้วยตัวเลือกที่กำหนดค่าไว้
```java
objImage.save(dataDir + "BlockRefDgn.pdf", pdfOptions);
```

## บทสรุป

ยินดีด้วย! คุณได้ส่งออกไฟล์ DGN ที่ฝังไว้เป็น PDF โดยใช้ Aspose.CAD สำหรับ Java สำเร็จแล้ว บทช่วยสอนนี้ครอบคลุมขั้นตอนสำคัญในการรวม Aspose.CAD เข้ากับแอปพลิเคชัน Java ของคุณเพื่อการจัดการไฟล์ CAD ที่มีประสิทธิภาพ

## คำถามที่พบบ่อย

### คำถามที่ 1: ฉันสามารถใช้ Aspose.CAD สำหรับ Java ในโครงการเชิงพาณิชย์ได้หรือไม่

 A1: ใช่ Aspose.CAD สำหรับ Java เป็นไลบรารีเชิงพาณิชย์ คุณสามารถขอรับใบอนุญาตได้จาก[ที่นี่](https://purchase.aspose.com/buy).

### คำถามที่ 2: มีการทดลองใช้ฟรีหรือไม่?

 A2:ได้ คุณสามารถเข้าถึง Aspose.CAD สำหรับ Java รุ่นทดลองใช้ฟรีได้[ที่นี่](https://releases.aspose.com/).

### คำถามที่ 3: ฉันจะรับการสนับสนุนสำหรับ Aspose.CAD สำหรับ Java ได้อย่างไร

A3: คุณสามารถขอรับการสนับสนุนจากชุมชน Aspose.CAD บน[ฟอรั่ม](https://forum.aspose.com/c/cad/19).

### คำถามที่ 4: หากฉันต้องการใบอนุญาตชั่วคราวจะต้องทำอย่างไร

 A4: คุณสามารถขอรับใบอนุญาตชั่วคราวได้[ที่นี่](https://purchase.aspose.com/temporary-license/).

### Q5: ฉันจะหาเอกสารได้จากที่ไหน?

 A5: มีเอกสารประกอบให้[ที่นี่](https://reference.aspose.com/cad/java/).