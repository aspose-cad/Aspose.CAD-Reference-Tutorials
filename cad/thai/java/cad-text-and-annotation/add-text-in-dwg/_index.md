---
title: เพิ่มข้อความใน DWG โดยใช้ Aspose.CAD สำหรับ Java
linktitle: เพิ่มข้อความใน DWG
second_title: Aspose.CAD Java API
description: ปรับปรุงภาพวาด DWG ของคุณอย่างง่ายดายด้วย Aspose.CAD สำหรับ Java เพิ่มข้อความได้อย่างราบรื่นด้วยคำแนะนำทีละขั้นตอนของเรา
type: docs
weight: 10
url: /th/java/cad-text-and-annotation/add-text-in-dwg/
---
## การแนะนำ

ในขอบเขตของการออกแบบโดยใช้คอมพิวเตอร์ช่วย (CAD) Aspose.CAD สำหรับ Java มีความโดดเด่นในฐานะเครื่องมืออันทรงพลังสำหรับจัดการและแปลงภาพวาด DWG หนึ่งในคุณสมบัติที่มีประโยชน์คือความสามารถในการเพิ่มข้อความลงในไฟล์ DWG ได้อย่างราบรื่น ในบทช่วยสอนนี้ เราจะแนะนำคุณตลอดขั้นตอนการเพิ่มข้อความลงในภาพวาด DWG ของคุณโดยใช้ Aspose.CAD สำหรับ Java

## ข้อกำหนดเบื้องต้น

ก่อนที่จะเข้าสู่บทช่วยสอน ตรวจสอบให้แน่ใจว่าคุณมีข้อกำหนดเบื้องต้นต่อไปนี้:

-  Aspose.CAD สำหรับ Java Library: ดาวน์โหลดและติดตั้งไลบรารีจากไฟล์[Aspose.CAD สำหรับหน้า Java](https://releases.aspose.com/cad/java/).

- Java Development Kit (JDK): ตรวจสอบให้แน่ใจว่าคุณได้ติดตั้ง JDK ล่าสุดในระบบของคุณ

- การวาด DWG: เตรียมไฟล์รูปวาด DWG ที่คุณต้องการเพิ่มข้อความ

## นำเข้าเนมสเปซ

ในโค้ด Java ของคุณ ให้นำเข้าเนมสเปซที่จำเป็นสำหรับ Aspose.CAD:

```java
import com.aspose.cad.Image;


import com.aspose.cad.fileformats.cad.CadDrawTypeMode;
import com.aspose.cad.fileformats.cad.CadImage;
import com.aspose.cad.fileformats.cad.cadobjects.CadText;
import com.aspose.cad.imageoptions.CadRasterizationOptions;
import com.aspose.cad.imageoptions.PdfOptions;
```

ตอนนี้ เรามาแจกแจงข้อมูลโค้ดที่ให้ไว้เป็นหลายขั้นตอน:

## ขั้นตอนที่ 1: ตั้งค่า Document Directory และ DWG File Path

```java
String dataDir = "Your Document Directory" + "DWGDrawings/";
String dwgPathToFile = dataDir + "SimpleEntites.dwg";
```

## ขั้นตอนที่ 2: โหลดอิมเมจ DWG

```java
Image image = Image.load(dwgPathToFile);
```

## ขั้นตอนที่ 3: สร้างวัตถุ CadText

```java
CadText cadText = new CadText();
cadText.setStyleType("Standard");
cadText.setDefaultValue("Some custom text");
cadText.setColorId(256);
cadText.setLayerName("0");
cadText.getFirstAlignment().setX(47.9);
cadText.getFirstAlignment().setY(5.56);
cadText.setTextHeight(0.8);
cadText.setScaleX(0);
```

## ขั้นตอนที่ 4: เพิ่มข้อความลงใน CadImage

```java
CadImage cadImage = ((CadImage)(image));
cadImage.getBlockEntities().get_Item("*Model_Space").addEntity(cadText);
```

## ขั้นตอนที่ 5: ตั้งค่าตัวเลือก PDF

```java
PdfOptions pdfOptions = new PdfOptions();
```

## ขั้นตอนที่ 6: กำหนดค่า CadRasterizationOptions

```java
CadRasterizationOptions cadRasterizationOptions = new CadRasterizationOptions();
pdfOptions.setVectorRasterizationOptions(cadRasterizationOptions);
cadRasterizationOptions.setDrawType(CadDrawTypeMode.UseObjectColor);
cadRasterizationOptions.setPageHeight(1600);
cadRasterizationOptions.setPageWidth(1600);
cadRasterizationOptions.setLayouts(new String[] {"Model"});
```

## ขั้นตอนที่ 7: บันทึก DWG ที่แก้ไขแล้วเป็น PDF

```java
image.save(dataDir + "SimpleEntites_generated.dwg.pdf", pdfOptions);
```

เมื่อทำตามขั้นตอนเหล่านี้ คุณจะสามารถเพิ่มข้อความลงในแบบร่าง DWG ของคุณได้อย่างราบรื่นโดยใช้ Aspose.CAD สำหรับ Java

## บทสรุป

Aspose.CAD สำหรับ Java ช่วยให้นักพัฒนาปรับปรุงและแก้ไขภาพวาด DWG โดยทางโปรแกรม บทช่วยสอนนี้ให้คำแนะนำทีละขั้นตอนที่ชัดเจนในการเพิ่มข้อความลงในไฟล์ DWG ของคุณ ซึ่งแสดงให้เห็นถึงความเรียบง่ายและประสิทธิภาพของ Aspose.CAD

## คำถามที่พบบ่อย

### คำถามที่ 1: Aspose.CAD เข้ากันได้กับไฟล์ DWG ทุกเวอร์ชันหรือไม่

A1: Aspose.CAD รองรับไฟล์ DWG หลากหลายเวอร์ชัน จึงรับประกันความเข้ากันได้กับซอฟต์แวร์ CAD หลากหลายประเภท

### คำถามที่ 2: ฉันสามารถปรับแต่งแบบอักษรและการจัดรูปแบบของข้อความที่เพิ่มเข้าไปได้หรือไม่

A2: ได้ คุณสามารถปรับแต่งแบบอักษร สไตล์ และตัวเลือกการจัดรูปแบบอื่นๆ สำหรับข้อความที่เพิ่มลงในไฟล์ DWG ได้โดยใช้ Aspose.CAD

### คำถามที่ 3: Aspose.CAD สำหรับ Java มีรุ่นทดลองใช้ฟรีหรือไม่

 A3: ได้ คุณสามารถสำรวจคุณสมบัติของ Aspose.CAD ได้โดยการทดลองใช้ฟรีจาก[ที่นี่](https://releases.aspose.com/).

### คำถามที่ 4: ฉันจะหาเอกสารโดยละเอียดสำหรับ Aspose.CAD สำหรับ Java ได้ที่ไหน

 A4: โปรดดูเอกสารประกอบ[ที่นี่](https://reference.aspose.com/cad/java/) สำหรับข้อมูลเชิงลึกและตัวอย่าง

### คำถามที่ 5: ฉันจะรับการสนับสนุนหรือขอความช่วยเหลือเกี่ยวกับ Aspose.CAD ได้อย่างไร

A5: เยี่ยมชม[ฟอรั่ม Aspose.CAD](https://forum.aspose.com/c/cad/19) เพื่อรับความช่วยเหลือและเชื่อมต่อกับชุมชน