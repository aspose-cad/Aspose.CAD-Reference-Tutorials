---
title: ส่งออกเค้าโครง CAD เป็น PDF ด้วย Aspose.CAD สำหรับ Java
linktitle: ส่งออกเค้าโครง CAD เป็น PDF
second_title: Aspose.CAD Java API
description: สำรวจ Aspose.CAD สำหรับ Java เพื่อส่งออกเค้าโครง CAD เป็น PDF ได้อย่างง่ายดาย มีประสิทธิภาพ เชื่อถือได้ และเป็นมิตรกับนักพัฒนา
type: docs
weight: 11
url: /th/java/cad-export-options/export-cad-layouts-to-pdf/
---
## การแนะนำ

ในสาขาการออกแบบโดยใช้คอมพิวเตอร์ช่วย (CAD) ที่มีการพัฒนาอย่างต่อเนื่อง Aspose.CAD สำหรับ Java มีความโดดเด่นในฐานะเครื่องมืออันทรงพลังสำหรับจัดการและแปลงไฟล์ CAD ในบทช่วยสอนนี้ เราจะแนะนำคุณตลอดขั้นตอนการส่งออกเค้าโครง CAD เป็น PDF โดยใช้ Aspose.CAD สำหรับ Java ไม่ว่าคุณจะเป็นนักพัฒนาที่มีประสบการณ์หรือเพียงแค่ดำดิ่งสู่โลกของ CAD คำแนะนำทีละขั้นตอนนี้จะช่วยให้คุณควบคุมศักยภาพของไลบรารี Java อเนกประสงค์นี้ได้อย่างเต็มที่

## ข้อกำหนดเบื้องต้น

ก่อนที่เราจะเจาะลึกบทช่วยสอน ตรวจสอบให้แน่ใจว่าคุณมีข้อกำหนดเบื้องต้นต่อไปนี้:

-  Aspose.CAD สำหรับ Java: ตรวจสอบให้แน่ใจว่าคุณได้ติดตั้งไลบรารีแล้ว คุณสามารถดาวน์โหลดได้จากเว็บไซต์ Aspose[ที่นี่](https://releases.aspose.com/cad/java/).

- สภาพแวดล้อมการพัฒนา Java: ตรวจสอบให้แน่ใจว่าคุณได้ตั้งค่าสภาพแวดล้อมการพัฒนา Java บนเครื่องของคุณ

เมื่อคุณตั้งค่าทุกอย่างเรียบร้อยแล้ว เรามาเริ่มด้วยบทช่วยสอนกันดีกว่า

## นำเข้าเนมสเปซ

ในโค้ด Java ของคุณ ให้เริ่มด้วยการนำเข้าเนมสเปซที่จำเป็น การนำเข้าเหล่านี้ให้การเข้าถึงคลาสและวิธีการที่จำเป็นสำหรับการทำงานกับ Aspose.CAD สำหรับ Java

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

 เริ่มต้นด้วยการโหลดไฟล์ CAD ลงในแอปพลิเคชัน Java ของคุณโดยใช้นามสกุลไฟล์`Image.load` วิธี. แทนที่`"conic_pyramid.dxf"` พร้อมเส้นทางไปยังไฟล์ CAD ของคุณ

```java
String dataDir = "Your Document Directory" + "ExportingCAD/";
String srcFile = dataDir + "conic_pyramid.dxf";
Image cadImage = Image.load(srcFile);
```

## ขั้นตอนที่ 2: ตั้งค่าตัวเลือกการแรสเตอร์

 สร้างอินสแตนซ์ของ`CadRasterizationOptions` เพื่อกำหนดวิธีการแรสเตอร์เอนทิตี CAD ปรับพารามิเตอร์ต่างๆ เช่น ความกว้างของหน้า ความสูงของหน้า และการปรับขนาดเค้าโครงตามความต้องการของคุณ

```java
CadRasterizationOptions rasterizationOptions = new CadRasterizationOptions();
rasterizationOptions.setPageWidth(1600);
rasterizationOptions.setPageHeight(1600);
rasterizationOptions.setAutomaticLayoutsScaling(true);
rasterizationOptions.setNoScaling(false);
rasterizationOptions.setContentAsBitmap(true);
rasterizationOptions.setLayouts(new String[]{"Model"});
```

## ขั้นตอนที่ 3: ตั้งค่าตัวเลือก PDF

 สร้างอินสแตนซ์ของ`PdfOptions` และเชื่อมโยงกับตัวเลือกการแรสเตอร์ นอกจากนี้ ให้ตั้งค่าตัวเลือกกราฟิกสำหรับการส่งออก PDF เช่น โหมดการปรับให้เรียบ คำใบ้การแสดงข้อความ และโหมดการแก้ไข

```java
PdfOptions pdfOptions = new PdfOptions();
pdfOptions.setVectorRasterizationOptions(rasterizationOptions);
rasterizationOptions.getGraphicsOptions().setSmoothingMode(SmoothingMode.HighQuality);
rasterizationOptions.getGraphicsOptions().setTextRenderingHint(TextRenderingHint.AntiAliasGridFit);
rasterizationOptions.getGraphicsOptions().setInterpolationMode(InterpolationMode.HighQualityBicubic);
```

## ขั้นตอนที่ 4: ส่งออกเป็น PDF

 สุดท้าย ส่งออกเค้าโครง CAD ไปเป็นไฟล์ PDF โดยใช้นามสกุลไฟล์`save` วิธีการของ`cadImage` วัตถุ.

```java
cadImage.save(dataDir + "CADLayoutsToPDF_out_.pdf", pdfOptions);
```

ยินดีด้วย! คุณได้ส่งออกเค้าโครง CAD เป็น PDF โดยใช้ Aspose.CAD สำหรับ Java สำเร็จแล้ว รู้สึกอิสระที่จะสำรวจคุณสมบัติและฟังก์ชันเพิ่มเติมที่นำเสนอโดย Aspose.CAD เพื่อปรับปรุงประสบการณ์การจัดการไฟล์ CAD ของคุณ

## บทสรุป

ในบทช่วยสอนนี้ เราได้อธิบายขั้นตอนการส่งออกเค้าโครง CAD เป็น PDF โดยใช้ Aspose.CAD สำหรับ Java ด้วยคุณสมบัติที่แข็งแกร่งและ API ที่ใช้งานง่าย Aspose.CAD ช่วยให้นักพัฒนาสามารถทำงานกับไฟล์ CAD ในแอปพลิเคชัน Java ได้อย่างมีประสิทธิภาพ

## คำถามที่พบบ่อย

### คำถามที่ 1: ฉันสามารถใช้ Aspose.CAD สำหรับ Java กับไฟล์ CAD รูปแบบอื่นได้หรือไม่

 A1: ใช่ Aspose.CAD รองรับรูปแบบ CAD หลากหลาย รวมถึง DWG, DXF, DWF และอื่นๆ ตรวจสอบเอกสาร[ที่นี่](https://reference.aspose.com/cad/java/) สำหรับรายการทั้งหมด

### คำถามที่ 2: Aspose.CAD สำหรับ Java มีรุ่นทดลองใช้ฟรีหรือไม่

 ตอบ 2: ได้ คุณสามารถสำรวจคุณสมบัติของ Aspose.CAD ได้ด้วยการทดลองใช้ฟรี[ที่นี่](https://releases.aspose.com/).

### คำถามที่ 3: ฉันจะรับการสนับสนุนสำหรับ Aspose.CAD สำหรับ Java ได้อย่างไร

 A3: เยี่ยมชมฟอรั่ม Aspose.CAD[ที่นี่](https://forum.aspose.com/c/cad/19) เพื่อสนับสนุนชุมชน สำหรับการสนับสนุนระดับพรีเมียม ให้พิจารณาซื้อใบอนุญาต[ที่นี่](https://purchase.aspose.com/buy).

### คำถามที่ 4: การปรับขนาดโครงร่างแบบอัตโนมัติและแบบแมนนวลแตกต่างกันอย่างไร

A4: การปรับขนาดเลย์เอาต์อัตโนมัติจะปรับขนาดเลย์เอาต์ตามขนาดหน้าที่ระบุ ในขณะที่การปรับขนาดด้วยตนเองทำให้คุณสามารถตั้งค่าการปรับขนาดแบบกำหนดเองได้

### คำถามที่ 5: ฉันสามารถปรับแต่งลักษณะที่ปรากฏของไฟล์ PDF ที่ส่งออกได้หรือไม่

A5: ได้ คุณสามารถปรับแต่งตัวเลือกกราฟิกในโค้ดเพื่อควบคุมคุณภาพและรูปลักษณ์ของ PDF ที่ส่งออกได้