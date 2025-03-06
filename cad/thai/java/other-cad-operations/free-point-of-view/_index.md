---
title: การเรนเดอร์มุมมองฟรีด้วย Aspose.CAD สำหรับ Java
linktitle: มุมมองฟรี
second_title: Aspose.CAD Java API
description: สำรวจพลังของ Aspose.CAD สำหรับ Java ในบทช่วยสอนนี้เกี่ยวกับการเรนเดอร์มุมมองฟรีสำหรับภาพวาด CAD ปลดปล่อยศักยภาพของ Aspose.CAD
weight: 14
url: /th/java/other-cad-operations/free-point-of-view/
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# การเรนเดอร์มุมมองฟรีด้วย Aspose.CAD สำหรับ Java

## การแนะนำ

ยินดีต้อนรับสู่ "มุมมองฟรี - Aspose.CAD สำหรับการสอน Java" ในคู่มือที่ครอบคลุมนี้ เราจะแนะนำคุณตลอดกระบวนการใช้ประโยชน์จาก Aspose.CAD สำหรับ Java เพื่อให้ได้การเรนเดอร์มุมมองฟรีสำหรับแบบร่าง CAD Aspose.CAD เป็นไลบรารี Java ที่ทรงพลังซึ่งมีฟีเจอร์มากมายสำหรับการทำงานกับไฟล์ Computer-Aided Design (CAD) บทช่วยสอนจะครอบคลุมถึงข้อกำหนดเบื้องต้นที่จำเป็น การนำเข้าแพ็คเกจที่จำเป็น และแยกย่อยแต่ละตัวอย่างออกเป็นคำแนะนำทีละขั้นตอน

## ข้อกำหนดเบื้องต้น

ก่อนที่จะเข้าสู่บทช่วยสอน ตรวจสอบให้แน่ใจว่าคุณมีข้อกำหนดเบื้องต้นต่อไปนี้:
-  Aspose.CAD สำหรับไลบรารี Java: ดาวน์โหลดและติดตั้ง Aspose.CAD สำหรับไลบรารี Java จาก[ลิ้งค์ดาวน์โหลด](https://releases.aspose.com/cad/java/).
- Java Development Kit (JDK): ตรวจสอบให้แน่ใจว่าคุณได้ติดตั้ง Java บนเครื่องของคุณ

## แพ็คเกจนำเข้า

ในการเริ่มต้น ให้นำเข้าแพ็คเกจที่จำเป็นลงในโปรเจ็กต์ Java ของคุณ เพิ่มบรรทัดโค้ดต่อไปนี้ที่จุดเริ่มต้นของไฟล์ Java ของคุณ:
```java
import com.aspose.cad.fileformats.ObserverPoint;
import com.aspose.cad.imageoptions.CadRasterizationOptions;
import com.aspose.cad.Image;
import com.aspose.cad.imageoptions.JpegOptions;
import com.aspose.cad.imageoptions.CadRasterizationOptions;
import com.aspose.cad.imageoptions.ObserverPoint;
```

แพ็คเกจเหล่านี้จำเป็นสำหรับการทำงานกับไฟล์ CAD และปรับแต่งตัวเลือกการเรนเดอร์

ตอนนี้ เรามาแบ่งตัวอย่างที่ให้ไว้ออกเป็นหลายขั้นตอน:

## ขั้นตอนที่ 1: ตั้งค่าไดเร็กทอรีเอกสารของคุณ

```java
String dataDir = "Your Document Directory" + "CADConversion/";
```

แทนที่ "Your Document Directory" ด้วยเส้นทางไปยังไดเร็กทอรีเอกสารจริงของคุณ

## ขั้นตอนที่ 2: โหลดแบบร่าง CAD

```java
String sourceFilePath = dataDir + "conic_pyramid.dxf";
Image objImage = Image.load(sourceFilePath);
```

ระบุเส้นทางไปยังแบบร่าง CAD ของคุณ และโหลดโดยใช้`Image` ระดับ.

## ขั้นตอนที่ 3: กำหนดค่าตัวเลือกการแรสเตอร์ CAD

```java
CadRasterizationOptions cadRasterizationOptions = new CadRasterizationOptions();
cadRasterizationOptions.setPageHeight(1500);
cadRasterizationOptions.setPageWidth(1500);
```

ปรับแต่งตัวเลือกการแรสเตอร์ CAD ตามความต้องการของคุณ เช่น ความสูงและความกว้างของหน้า

## ขั้นตอนที่ 4: ตั้งค่า JpegOptions

```java
JpegOptions options = new JpegOptions();
options.setVectorRasterizationOptions(cadRasterizationOptions);
```

 สร้างอินสแตนซ์ของ`JpegOptions` และเชื่อมโยงกับตัวเลือกการแรสเตอร์ที่กำหนดค่าไว้ก่อนหน้านี้

## ขั้นตอนที่ 5: กำหนดมุมการหมุน

```java
float xAngle = 10;
float yAngle = 30;
float zAngle = 40;
ObserverPoint obvPoint = new ObserverPoint(xAngle, yAngle, zAngle);
cadRasterizationOptions.setObserverPoint(obvPoint);
```

ระบุมุมการหมุนตามแนวแกน X, Y และ Z สำหรับการเรนเดอร์มุมมองอิสระ

## ขั้นตอนที่ 6: บันทึกภาพที่แสดงผล

```java
objImage.save(dataDir + "FreePointOfView_out.jpeg", options);
```

บันทึกภาพที่เรนเดอร์ด้วยตัวเลือกที่ระบุไปยังตำแหน่งที่ต้องการ

ทำซ้ำขั้นตอนเหล่านี้สำหรับกรณีการใช้งานเฉพาะของคุณ เพื่อให้มั่นใจว่าสามารถเรนเดอร์มุมมองฟรีสำหรับแบบร่าง CAD ของคุณ

## บทสรุป

ยินดีด้วย! คุณได้เรียนรู้วิธีใช้งานการเรนเดอร์มุมมองฟรีโดยใช้ Aspose.CAD สำหรับ Java เรียบร้อยแล้ว บทช่วยสอนนี้ครอบคลุมขั้นตอนที่สำคัญ ตั้งแต่การตั้งค่าข้อกำหนดเบื้องต้นไปจนถึงการปรับแต่งตัวเลือกการเรนเดอร์และการบันทึกภาพที่ส่งออก

## คำถามที่พบบ่อย

### คำถามที่ 1: ฉันสามารถใช้ Aspose.CAD สำหรับ Java บนหลายแพลตฟอร์มได้หรือไม่

ตอบ 1: ใช่ Aspose.CAD สำหรับ Java ไม่ขึ้นอยู่กับแพลตฟอร์มและสามารถใช้ได้กับระบบปฏิบัติการต่างๆ

### คำถามที่ 2: มีตัวเลือกสิทธิ์การใช้งานสำหรับ Aspose.CAD สำหรับ Java หรือไม่

 ตอบ 2: ได้ คุณสามารถสำรวจตัวเลือกใบอนุญาตและทำการซื้อได้[ที่นี่](https://purchase.aspose.com/buy).

### คำถามที่ 3: มีการทดลองใช้ฟรีหรือไม่?

 A3: ได้ คุณสามารถเข้าถึงเวอร์ชันทดลองใช้ฟรีได้[ที่นี่](https://releases.aspose.com/).

### คำถามที่ 4: ฉันจะรับการสนับสนุนสำหรับ Aspose.CAD สำหรับ Java ได้ที่ไหน

 A4: เยี่ยมชม[ฟอรั่ม Aspose.CAD](https://forum.aspose.com/c/cad/19) สำหรับการสนับสนุนและการอภิปรายของชุมชน

### คำถามที่ 5: ฉันจะขอรับใบอนุญาตชั่วคราวได้อย่างไร

 A5: รับใบอนุญาตชั่วคราว[ที่นี่](https://purchase.aspose.com/temporary-license/).
{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}
