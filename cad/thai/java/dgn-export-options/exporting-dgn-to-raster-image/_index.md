---
title: การแปลง Java DGN เป็น JPEG ด้วยบทช่วยสอน Aspose.CAD
linktitle: การส่งออก DGN ในรูปแบบ AutoCAD เป็นรูปแบบภาพแรสเตอร์
second_title: Aspose.CAD Java API
description: เรียนรู้วิธีส่งออกไฟล์ DGN เป็นภาพ JPEG ใน Java โดยใช้ Aspose.CAD บทช่วยสอนแบบทีละขั้นตอนนี้จะแนะนำคุณตลอดกระบวนการอย่างง่ายดาย
weight: 13
url: /th/java/dgn-export-options/exporting-dgn-to-raster-image/
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# การแปลง Java DGN เป็น JPEG ด้วยบทช่วยสอน Aspose.CAD

## การแนะนำ

ยินดีต้อนรับสู่บทช่วยสอนที่ครอบคลุมเกี่ยวกับการส่งออกไฟล์ DGN (การออกแบบ) ไปเป็นรูปแบบภาพแรสเตอร์โดยใช้ Aspose.CAD สำหรับ Java Aspose.CAD เป็นไลบรารีอันทรงพลังที่ช่วยให้นักพัฒนา Java สามารถทำงานกับไฟล์ CAD ได้อย่างราบรื่น ในบทช่วยสอนนี้ เราจะแนะนำคุณตลอดขั้นตอนการแปลงไฟล์ DGN เป็นภาพ JPEG พร้อมคำแนะนำทีละขั้นตอนและตัวอย่างโค้ด

## ข้อกำหนดเบื้องต้น

ก่อนที่จะเข้าสู่บทช่วยสอน ตรวจสอบให้แน่ใจว่าคุณมีข้อกำหนดเบื้องต้นต่อไปนี้:
1.  ไลบรารี Aspose.CAD: ตรวจสอบให้แน่ใจว่าคุณได้ติดตั้งไลบรารี Aspose.CAD สำหรับ Java แล้ว คุณสามารถดาวน์โหลดได้[ที่นี่](https://releases.aspose.com/cad/java/).
2. Java Development Kit (JDK): ตรวจสอบให้แน่ใจว่าคุณได้ติดตั้ง Java บนเครื่องของคุณแล้ว
3. สภาพแวดล้อมการพัฒนาแบบรวม (IDE): ใช้ IDE ที่เข้ากันได้กับ Java เช่น IntelliJ หรือ Eclipse

## แพ็คเกจนำเข้า

ในโปรเจ็กต์ Java ของคุณ ให้นำเข้าแพ็คเกจที่จำเป็นสำหรับ Aspose.CAD เพิ่มบรรทัดต่อไปนี้ลงในโค้ดของคุณ:

```java
import java.io.FileNotFoundException;
import java.io.FileOutputStream;
import java.io.OutputStream;
import com.aspose.cad.Image;
import com.aspose.cad.ImageOptionsBase;
import com.aspose.cad.fileformats.dgn.DgnImage;
import com.aspose.cad.imageoptions.CadRasterizationOptions;
import com.aspose.cad.imageoptions.JpegOptions;
```

## ขั้นตอนที่ 1: โหลดไฟล์ DGN

```java
String dataDir = "Your Document Directory" + "ExportingDGN/";
DgnImage dgnImage = (DgnImage) Image.load(dataDir + "Nikon_D90_Camera.dgn");
```

## ขั้นตอนที่ 2: สร้างวัตถุ JpegOptions

```java
ImageOptionsBase options = new JpegOptions();
```

## ขั้นตอนที่ 3: กำหนดตัวเลือกการแรสเตอร์

```java
CadRasterizationOptions vectorOptions = new CadRasterizationOptions();
vectorOptions.setPageWidth(600);
vectorOptions.setPageHeight(400);
vectorOptions.setNoScaling(true);
vectorOptions.setAutomaticLayoutsScaling(false);
options.setVectorRasterizationOptions(vectorOptions);
```

## ขั้นตอนที่ 4: บันทึกภาพที่แปลงแล้ว

```java
OutputStream outStream = new FileOutputStream(dataDir + "ExportDGNToRasterImage_Out.jpg");
dgnImage.save(outStream, options);
```

ทำซ้ำขั้นตอนเหล่านี้สำหรับไฟล์ DGN เฉพาะของคุณ โดยปรับเส้นทางของไฟล์ให้เหมาะสม

## บทสรุป

ยินดีด้วย! คุณได้เรียนรู้วิธีส่งออกไฟล์ DGN เป็นรูปแบบภาพแรสเตอร์โดยใช้ Aspose.CAD สำหรับ Java เรียบร้อยแล้ว บทช่วยสอนนี้ช่วยให้คุณมีความรู้ในการรวมฟังก์ชันนี้เข้ากับแอปพลิเคชัน Java ของคุณ

## คำถามที่พบบ่อย

### คำถามที่ 1: ฉันสามารถใช้ Aspose.CAD สำหรับ Java กับไฟล์ CAD รูปแบบอื่นได้หรือไม่

ตอบ 1: ใช่ Aspose.CAD รองรับรูปแบบ CAD ที่หลากหลาย ซึ่งเป็นโซลูชั่นที่หลากหลายสำหรับนักพัฒนา Java

### คำถามที่ 2: Aspose.CAD สำหรับ Java มีรุ่นทดลองใช้ฟรีหรือไม่

 A2: ได้ คุณสามารถทดลองใช้ฟรีได้[ที่นี่](https://releases.aspose.com/).

### คำถามที่ 3: ฉันจะหาเอกสารสำหรับ Aspose.CAD สำหรับ Java ได้ที่ไหน

 A3: โปรดดูเอกสารประกอบ[ที่นี่](https://reference.aspose.com/cad/java/).

### คำถามที่ 4: ฉันจะรับการสนับสนุนสำหรับ Aspose.CAD สำหรับ Java ได้อย่างไร

 A4: เยี่ยมชมฟอรั่มการสนับสนุน[ที่นี่](https://forum.aspose.com/c/cad/19).

### คำถามที่ 5: ฉันจะซื้อใบอนุญาตสำหรับ Aspose.CAD สำหรับ Java ได้ที่ไหน

 A5: คุณสามารถซื้อใบอนุญาตได้[ที่นี่](https://purchase.aspose.com/buy).
{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}
