---
title: แปลง DWG เฉพาะเป็นรูปภาพโดยใช้ Java
linktitle: แปลง DWG เฉพาะเป็นรูปภาพโดยใช้ Java
second_title: Aspose.CAD Java API
description: สำรวจการแปลง DWG เป็นรูปภาพอย่างราบรื่นด้วย Aspose.CAD สำหรับ Java ปฏิบัติตามคำแนะนำทีละขั้นตอนของเราเพื่อการแปลงรูปแบบไฟล์ที่มีประสิทธิภาพ
weight: 14
url: /th/java/dwg-file-operations/convert-dwg-to-image/
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# แปลง DWG เฉพาะเป็นรูปภาพโดยใช้ Java

## การแนะนำ

ในการออกแบบภูมิทัศน์ดิจิทัลที่มีการพัฒนาอยู่ตลอดเวลา ความจำเป็นในการแปลงภาพวาด DWG ให้เป็นรูปภาพถือเป็นข้อกำหนดทั่วไป Aspose.CAD สำหรับ Java กลายเป็นเครื่องมืออันทรงพลังที่ช่วยให้งานนี้สำเร็จลุล่วงได้อย่างราบรื่น ในบทช่วยสอนนี้ เราจะแนะนำคุณตลอดขั้นตอนการแปลงไฟล์ DWG เฉพาะเป็นรูปภาพโดยใช้ Aspose.CAD สำหรับ Java

## ข้อกำหนดเบื้องต้น

ก่อนที่จะเข้าสู่บทช่วยสอน ตรวจสอบให้แน่ใจว่าคุณมีข้อกำหนดเบื้องต้นต่อไปนี้:
1.  Java Development Kit (JDK): Aspose.CAD สำหรับ Java ต้องมี JDK ที่เข้ากันได้ติดตั้งอยู่บนระบบของคุณ คุณสามารถดาวน์โหลด JDK ล่าสุดได้จาก[เว็บไซต์ของออราเคิล](https://www.oracle.com/java/technologies/javase-downloads.html).
2.  Aspose.CAD สำหรับไลบรารี Java: ดาวน์โหลดและติดตั้ง Aspose.CAD สำหรับไลบรารี Java จาก[หน้าดาวน์โหลด Aspose.CAD](https://releases.aspose.com/cad/java/).
3. สภาพแวดล้อมการพัฒนาแบบรวม (IDE): เลือก IDE ที่คุณต้องการสำหรับการพัฒนา Java เช่น IntelliJ IDEA หรือ Eclipse

## แพ็คเกจนำเข้า

ในโปรเจ็กต์ Java ของคุณ ให้นำเข้าแพ็คเกจ Aspose.CAD ที่จำเป็นสำหรับการผสานรวมที่ราบรื่น รวมสิ่งต่อไปนี้ในรหัสของคุณ:

```java
import com.aspose.cad.Image;
import com.aspose.cad.fileformats.cad.CadImage;
import com.aspose.cad.fileformats.cad.cadconsts.CadEntityTypeName;
import com.aspose.cad.fileformats.cad.cadobjects.CadBaseEntity;
import com.aspose.cad.imageoptions.CadRasterizationOptions;
import com.aspose.cad.imageoptions.PdfOptions;
import java.util.ArrayList;
import java.util.Collection;
import java.util.Iterator;
import java.util.List;
import java.util.ListIterator;
```

## ขั้นตอนที่ 1: ตั้งค่าโครงการของคุณ

ตรวจสอบให้แน่ใจว่าโปรเจ็กต์ Java ของคุณได้รับการตั้งค่าด้วยไลบรารี Aspose.CAD ที่จำเป็น และ JDK ได้รับการกำหนดค่าอย่างเหมาะสมใน IDE ของคุณ

## ขั้นตอนที่ 2: ระบุเส้นทางไฟล์ DWG

กำหนดเส้นทางไปยังไฟล์ DWG ที่คุณต้องการแปลง อัพเดต`dataDir` และ`sourceFilePath` ตัวแปรตาม

```java
String dataDir = "Your Document Directory" + "DWGDrawings/";
String sourceFilePath = dataDir + "visualization_-_conference_room.dwg";
```

## ขั้นตอนที่ 3: กรองเอนทิตีข้อความ

วนซ้ำเอนทิตี DWG และกรองเอนทิตีข้อความโดยใช้ไลบรารี Aspose.CAD

```java
CadImage cadImage = (CadImage) (Image.load(sourceFilePath));
CadBaseEntity[] entities = cadImage.getEntities();
List<CadBaseEntity> filteredEntities = new ArrayList<>();
for (CadBaseEntity baseEntity : entities) {
    if ((baseEntity.getTypeName() == CadEntityTypeName.TEXT)) {
        filteredEntities.add(baseEntity);
    }
}
CadBaseEntity[] arr = new CadBaseEntity[filteredEntities.size()];
cadImage.setEntities(filteredEntities.toArray(arr));
```

## ขั้นตอนที่ 4: ตั้งค่าตัวเลือกการแรสเตอร์

 สร้างอินสแตนซ์ของ`CadRasterizationOptions` และกำหนดค่าคุณสมบัติสำหรับการแปลง PDF

```java
CadRasterizationOptions rasterizationOptions = new CadRasterizationOptions();
rasterizationOptions.setPageWidth(1600);
rasterizationOptions.setPageHeight(1600);
rasterizationOptions.setAutomaticLayoutsScaling(true);
```

## ขั้นตอนที่ 5: ส่งออกเป็น PDF

 สร้างก`PdfOptions` ตั้งค่าตัวเลือกการแรสเตอร์เวกเตอร์ และบันทึกไฟล์ PDF ที่แปลงแล้ว

```java
PdfOptions pdfOptions = new PdfOptions();
pdfOptions.setVectorRasterizationOptions(rasterizationOptions);
String outFile = dataDir + "result_out_generated.pdf";
cadImage.save(outFile, pdfOptions);
```

ยินดีด้วย! คุณได้แปลงไฟล์ DWG เฉพาะเป็นรูปภาพโดยใช้ Aspose.CAD สำหรับ Java สำเร็จแล้ว

## บทสรุป

Aspose.CAD สำหรับ Java ลดความซับซ้อนของกระบวนการ DWG เป็นการแปลงรูปภาพ ให้ความยืดหยุ่นและประสิทธิภาพในขั้นตอนการออกแบบของคุณ รวมเครื่องมือนี้เข้ากับโครงการของคุณเพื่อปรับปรุงประสิทธิภาพการทำงานและปรับปรุงการแปลงรูปแบบไฟล์

## คำถามที่พบบ่อย

### คำถามที่ 1: Aspose.CAD เข้ากันได้กับไฟล์ DWG ทุกเวอร์ชันหรือไม่

A1: Aspose.CAD รองรับ DWG เวอร์ชันต่างๆ มากมาย ทำให้มั่นใจได้ถึงความเข้ากันได้กับรูปแบบไฟล์ต่างๆ

### คำถามที่ 2: ฉันสามารถปรับแต่งความละเอียดของภาพที่ส่งออกได้หรือไม่

A2: ใช่ บทช่วยสอนสาธิตวิธีการตั้งค่าความกว้างและความสูงของหน้า ช่วยให้คุณสามารถควบคุมความละเอียดได้

### คำถามที่ 3: Aspose.CAD เหมาะสำหรับการแปลงเป็นชุดหรือไม่

A3: แน่นอน. Aspose.CAD อนุญาตให้มีการประมวลผลเป็นชุด ทำให้คุณสามารถแปลงไฟล์ DWG หลายไฟล์พร้อมกันได้

### คำถามที่ 4: ฉันจะรับการสนับสนุนเพิ่มเติมหรือการสนทนาในชุมชนได้จากที่ไหน

 A4: เยี่ยมชม[ฟอรั่ม Aspose.CAD](https://forum.aspose.com/c/cad/19) สำหรับการสนับสนุนและการอภิปราย

### คำถามที่ 5: ฉันสามารถลองใช้ Aspose.CAD ก่อนซื้อได้หรือไม่

 A5: ใช่ สำรวจเครื่องมือพร้อมทดลองใช้ฟรีได้ที่[ลิงค์นี้](https://releases.aspose.com/).
{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}
