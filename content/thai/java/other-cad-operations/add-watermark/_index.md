---
title: เพิ่มลายน้ำให้กับแบบร่าง CAD - Aspose.CAD สำหรับการสอน Java
linktitle: ใส่ลายน้ำ
second_title: Aspose.CAD Java API
description: ปรับปรุงภาพวาด CAD ของคุณด้วยลายน้ำส่วนตัวโดยใช้ Aspose.CAD สำหรับ Java ปฏิบัติตามคำแนะนำทีละขั้นตอนของเราเพื่อการบูรณาการที่ราบรื่น
type: docs
weight: 12
url: /th/java/other-cad-operations/add-watermark/
---
## การแนะนำ

ยินดีต้อนรับสู่คู่มือที่ครอบคลุมเกี่ยวกับการเพิ่มลายน้ำให้กับแบบร่าง CAD โดยใช้ Aspose.CAD สำหรับ Java ในบทช่วยสอนนี้ คุณจะได้เรียนรู้วิธีรวมลายน้ำอย่างมีประสิทธิภาพ ปรับปรุงเอกสาร CAD ของคุณด้วยข้อความส่วนตัวหรือการสร้างแบรนด์ Aspose.CAD สำหรับ Java มีชุดคุณสมบัติอันทรงพลัง ทำให้กระบวนการเพิ่มลายน้ำตรงไปตรงมา

## ข้อกำหนดเบื้องต้น

ก่อนที่เราจะเจาะลึกบทช่วยสอน ตรวจสอบให้แน่ใจว่าคุณมีข้อกำหนดเบื้องต้นดังต่อไปนี้:

-  Aspose.CAD สำหรับ Java: ตรวจสอบให้แน่ใจว่าคุณได้ติดตั้งไลบรารี Aspose.CAD ในสภาพแวดล้อม Java ของคุณ คุณสามารถดาวน์โหลดได้[ที่นี่](https://releases.aspose.com/cad/java/).
- Java Development Kit (JDK): ตรวจสอบให้แน่ใจว่าคุณได้ติดตั้ง JDK เวอร์ชันล่าสุดบนระบบของคุณ

## แพ็คเกจนำเข้า

ในโปรเจ็กต์ Java ของคุณ ให้นำเข้าแพ็คเกจ Aspose.CAD ที่จำเป็นเพื่อเริ่มต้น:

```java
import com.aspose.cad.Image;
import com.aspose.cad.fileformats.cad.CadImage;
import com.aspose.cad.fileformats.cad.cadobjects.Cad3DPoint;
import com.aspose.cad.fileformats.cad.cadobjects.CadMText;
import com.aspose.cad.fileformats.cad.cadobjects.CadText;
import com.aspose.cad.imageoptions.CadRasterizationOptions;
import com.aspose.cad.imageoptions.PdfOptions;
```

## ขั้นตอนที่ 1: เพิ่ม MTEXT ใหม่

```java
//เพิ่ม MTEXT ใหม่
CadMText watermark = new CadMText();
watermark.setText("Watermark message");
watermark.setInitialTextHeight(40);
watermark.setInsertionPoint(new Cad3DPoint(300, 40));
watermark.setLayerName("0");
cadImage.getBlockEntities().get_Item("*Model_Space").addEntity(watermark);
```

## ขั้นตอนที่ 2: เพิ่มเอนทิตีแบบง่ายเช่นข้อความ

คุณยังสามารถเพิ่มเอนทิตีที่ตรงไปตรงมามากขึ้น เช่น ข้อความ:

```java
// หรือเพิ่มเอนทิตีที่เรียบง่ายมากขึ้น เช่น ข้อความ
CadText text = new CadText();
text.setDefaultValue("Watermark text");
text.setTextHeight(40);
text.setFirstAlignment(new Cad3DPoint(300, 40));
text.setLayerName("0") ;
cadImage.getBlockEntities().get_Item("*Model_Space").addEntity(text);
```

## ขั้นตอนที่ 3: ส่งออกเป็น PDF

ส่งออกแบบร่าง CAD ที่มีลายน้ำเพิ่มเป็นไฟล์ PDF:

```java
// ส่งออกเป็น pdf
CadRasterizationOptions rasterizationOptions = new CadRasterizationOptions();
rasterizationOptions.setPageWidth(1600);
rasterizationOptions.setPageHeight(1600);
rasterizationOptions.setLayouts(new String[]{"Model"});
PdfOptions pdfOptions = new PdfOptions();
pdfOptions.setVectorRasterizationOptions(rasterizationOptions);
cadImage.save(dataDir + "AddWatermark_out.pdf", pdfOptions);

```

## บทสรุป

ยินดีด้วย! คุณได้เพิ่มลายน้ำให้กับแบบร่าง CAD ของคุณโดยใช้ Aspose.CAD สำหรับ Java สำเร็จแล้ว กระบวนการที่เรียบง่ายแต่ทรงพลังนี้ช่วยให้คุณปรับแต่งการออกแบบของคุณให้เป็นแบบส่วนตัวหรือปกป้องด้วยการสร้างแบรนด์ได้

## คำถามที่พบบ่อย

### คำถามที่ 1: Aspose.CAD เข้ากันได้กับไฟล์ CAD ทุกรูปแบบหรือไม่

A1: Aspose.CAD รองรับรูปแบบ CAD หลากหลาย รวมถึง DWG, DXF, DWT และ DWF

### คำถามที่ 2: ฉันสามารถปรับแต่งลักษณะที่ปรากฏของข้อความลายน้ำได้หรือไม่

A2: ได้ คุณสามารถควบคุมลักษณะที่ปรากฏของลายน้ำได้อย่างเต็มที่ รวมถึงขนาดข้อความ สี และตำแหน่ง

### คำถามที่ 3: มี Aspose.CAD สำหรับ Java รุ่นทดลองใช้งานหรือไม่

 A3: ได้ คุณสามารถดาวน์โหลดเวอร์ชันทดลองได้[ที่นี่](https://releases.aspose.com/).

### คำถามที่ 4: ฉันจะรับการสนับสนุนสำหรับ Aspose.CAD ได้อย่างไร

 A4: เยี่ยมชม[ฟอรั่ม Aspose.CAD](https://forum.aspose.com/c/cad/19) เพื่อสนับสนุนชุมชน

### คำถามที่ 5: ฉันจะหาเอกสารฉบับสมบูรณ์สำหรับ Aspose.CAD สำหรับ Java ได้ที่ไหน

 A5: โปรดดูที่[เอกสารประกอบ](https://reference.aspose.com/cad/java/) สำหรับข้อมูลโดยละเอียด