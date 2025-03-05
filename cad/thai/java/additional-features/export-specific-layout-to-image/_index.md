---
title: ส่งออกเค้าโครง DXF เฉพาะไปยังรูปภาพด้วย Aspose.CAD ใน Java
linktitle: ส่งออกเค้าโครง DXF เฉพาะไปยังรูปภาพด้วย Java
second_title: Aspose.CAD Java API
description: เรียนรู้วิธีส่งออกเค้าโครง DXF เฉพาะไปยังรูปภาพโดยใช้ Aspose.CAD สำหรับ Java ปฏิบัติตามคำแนะนำทีละขั้นตอนของเราเพื่อการบูรณาการที่ราบรื่น
type: docs
weight: 16
url: /th/java/additional-features/export-specific-layout-to-image/
---
## การแนะนำ

คุณต้องการแปลงเค้าโครง DXF เฉพาะให้เป็นรูปภาพโดยใช้ Java หรือไม่? ด้วย Aspose.CAD สำหรับ Java คุณสามารถทำงานนี้ให้สำเร็จได้อย่างราบรื่น ในคำแนะนำทีละขั้นตอนนี้ เราจะแนะนำคุณตลอดขั้นตอนการส่งออกเค้าโครง DXF เฉพาะไปยังรูปภาพ โดยให้คำแนะนำและตัวอย่างที่ชัดเจนสำหรับแต่ละขั้นตอน

## ข้อกำหนดเบื้องต้น

ก่อนที่คุณจะเริ่มต้น ตรวจสอบให้แน่ใจว่าคุณมีข้อกำหนดเบื้องต้นต่อไปนี้:

-  Aspose.CAD สำหรับ Java: ตรวจสอบให้แน่ใจว่าคุณได้ติดตั้งไลบรารี Aspose.CAD สำหรับ Java แล้ว คุณสามารถดาวน์โหลดได้[ที่นี่](https://releases.aspose.com/cad/java/).

## นำเข้าเนมสเปซ

ในการเริ่มต้น ให้นำเข้าเนมสเปซที่จำเป็นในโปรเจ็กต์ Java ของคุณ:

```java
import com.aspose.cad.Image;

import com.aspose.cad.imageoptions.CadRasterizationOptions;
import com.aspose.cad.imageoptions.PdfOptions;
import com.aspose.cad.fileformats.dwf.whip.objects.DwfWhipLayer;
import com.aspose.cad.fileformats.cad.CadImage;
import com.aspose.cad.fileformats.dwf.DwfImage;
import com.aspose.cad.imageoptions.JpegOptions;
import java.util.ArrayList;
import java.util.Arrays;
import java.util.List;
```

ตอนนี้เรามาดูรายละเอียดแต่ละขั้นตอนกัน

## ขั้นตอนที่ 1: ตั้งค่าไดเรกทอรีทรัพยากร

กำหนดเส้นทางไปยังไดเร็กทอรีทรัพยากรในโครงการ Java ของคุณ ไดเร็กทอรีนี้ควรมีภาพวาด DXF ที่คุณต้องการแปลง

```java
String dataDir = "Your Document Directory" + "DXFDrawings\\";
```

ตรวจสอบให้แน่ใจว่าได้แทนที่ "Your Document Directory" ด้วยเส้นทางจริง

## ขั้นตอนที่ 2: โหลดภาพ DXF

โหลดอิมเมจ DXF โดยใช้ไลบรารี Aspose.CAD

```java
String srcFile = dataDir + "for_layers_test.dwf";
DwfImage image = (DwfImage) Image.load(srcFile);
```

แทนที่ "for_layers_test.dwf" ด้วยชื่อไฟล์ DXF ของคุณ

## ขั้นตอนที่ 3: รับชื่อเลเยอร์

รับชื่อของเลเยอร์ที่มีอยู่ในอิมเมจ DXF

```java
List<String> layersNames = image.getLayers().getLayersNames();
```

ขั้นตอนนี้ช่วยให้แน่ใจว่าคุณมีรายการเลเยอร์ที่มีอยู่

## ขั้นตอนที่ 4: ตั้งค่าตัวเลือกการแรสเตอร์

 สร้างอินสแตนซ์ของ`CadRasterizationOptions` และตั้งค่าคุณสมบัติที่ต้องการ เช่น ความกว้างและความสูงของหน้า

```java
CadRasterizationOptions rasterizationOptions = new CadRasterizationOptions();
rasterizationOptions.setPageWidth(1600);
rasterizationOptions.setPageHeight(1600);
```

ปรับขนาดหน้าตามความต้องการของคุณ

## ขั้นตอนที่ 5: ระบุเลเยอร์

แปลงรายชื่อเลเยอร์ให้อยู่ในรูปแบบที่เหมาะสมสำหรับตัวเลือกการแรสเตอร์

```java
String[] stringArray = Arrays.copyOf(layersNames.toArray(), layersNames.toArray().length, String[].class);
List<String> stringList = Arrays.asList(stringArray);
rasterizationOptions.setLayers(stringList);
```

ขั้นตอนนี้ช่วยให้แน่ใจว่าคุณรวมเฉพาะเลเยอร์ที่ต้องการในกระบวนการส่งออกเท่านั้น

## ขั้นตอนที่ 6: กำหนดค่าตัวเลือก JPEG

 สร้างอินสแตนซ์ของ`JpegOptions` และตั้งค่าตัวเลือกการแรสเตอร์เวกเตอร์

```java
JpegOptions jpegOptions = new JpegOptions();
jpegOptions.setVectorRasterizationOptions(rasterizationOptions);
```

เพื่อเตรียมตัวเลือกสำหรับการบันทึกภาพในรูปแบบ JPEG

## ขั้นตอนที่ 7: ส่งออก DXF ไปยังรูปภาพ

ระบุเส้นทางเอาต์พุตและบันทึกภาพ DXF เป็น JPEG

```java
String output = dataDir + "for_layers_test.jpg";
image.save(output, jpegOptions);
```

ปรับเส้นทางเอาต์พุตและชื่อไฟล์ตามความต้องการของคุณ

ด้วยขั้นตอนเหล่านี้ คุณได้ส่งออกเค้าโครง DXF เฉพาะไปยังรูปภาพโดยใช้ Aspose.CAD สำหรับ Java ได้สำเร็จ

## บทสรุป

ในบทช่วยสอนนี้ เราได้กล่าวถึงกระบวนการส่งออกเค้าโครง DXF เฉพาะไปยังรูปภาพโดยใช้ Aspose.CAD สำหรับ Java ด้วยการทำตามขั้นตอนโดยละเอียดและใช้ข้อมูลโค้ดที่ให้มา คุณจะสามารถรวมฟังก์ชันการทำงานนี้เข้ากับโปรเจ็กต์ Java ของคุณได้อย่างราบรื่น

## คำถามที่พบบ่อย

### คำถามที่ 1: ฉันสามารถส่งออกเค้าโครง DXF หลายรายการในคราวเดียวได้หรือไม่

A1: ได้ คุณสามารถแก้ไขโค้ดเพื่อจัดการหลายเลย์เอาต์ได้โดยการวนซ้ำและส่งออกแต่ละเลย์เอาท์ทีละรายการ

### คำถามที่ 2: Aspose.CAD สำหรับ Java เข้ากันได้กับ Java เวอร์ชันต่างๆ หรือไม่

ตอบ 2: Aspose.CAD สำหรับ Java ได้รับการออกแบบมาให้เข้ากันได้กับ Java เวอร์ชันต่างๆ ตรวจสอบเอกสารสำหรับรายละเอียดความเข้ากันได้เฉพาะ

### คำถามที่ 3: ฉันจะจัดการกับข้อผิดพลาดระหว่างกระบวนการแปลง DXF เป็นรูปภาพได้อย่างไร

A3: คุณสามารถใช้การจัดการข้อผิดพลาดโดยใช้บล็อก try-catch เพื่อรวบรวมและจัดการข้อยกเว้นที่อาจเกิดขึ้นระหว่างการแปลง

### คำถามที่ 4: มีรูปแบบเอาต์พุตอื่นๆ ที่สนับสนุนนอกเหนือจาก JPEG หรือไม่

A4: ใช่ Aspose.CAD สำหรับ Java รองรับรูปแบบเอาต์พุตที่หลากหลาย รวมถึง PNG, BMP, TIFF และอื่นๆ คุณสามารถปรับโค้ดได้ตามนั้น

### คำถามที่ 5: ฉันสามารถปรับแต่งตัวเลือกการแรสเตอร์เพิ่มเติมได้หรือไม่

 A5: แน่นอนว่า`CadRasterizationOptions` คลาสมีคุณสมบัติต่างๆ สำหรับการปรับแต่ง สำรวจเอกสารประกอบเพื่อดูตัวเลือกเพิ่มเติม