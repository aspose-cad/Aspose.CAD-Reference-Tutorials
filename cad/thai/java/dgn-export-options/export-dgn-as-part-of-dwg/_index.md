---
title: ส่งออก DGN เป็น DWG ด้วย Aspose.CAD สำหรับ Java
linktitle: ส่งออก DGN โดยเป็นส่วนหนึ่งของ DWG
second_title: Aspose.CAD Java API
description: สำรวจวิธีการส่งออก DGN โดยเป็นส่วนหนึ่งของ DWG โดยใช้ Aspose.CAD สำหรับ Java ปฏิบัติตามคำแนะนำทีละขั้นตอนของเราเพื่อการจัดการไฟล์ CAD ที่มีประสิทธิภาพ
type: docs
weight: 10
url: /th/java/dgn-export-options/export-dgn-as-part-of-dwg/
---
## การแนะนำ

ในบทช่วยสอนนี้ เราจะสำรวจวิธีใช้ Aspose.CAD สำหรับ Java เพื่อส่งออกไฟล์ DGN (MicroStation Design) โดยเป็นส่วนหนึ่งของไฟล์ DWG (AutoCAD Drawing) Aspose.CAD เป็นไลบรารีที่มีประสิทธิภาพซึ่งมีฟังก์ชันการทำงานที่ครอบคลุมเพื่อทำงานกับรูปแบบไฟล์ CAD คำแนะนำทีละขั้นตอนนี้จะช่วยให้คุณเข้าใจกระบวนการส่งออก DGN โดยเป็นส่วนหนึ่งของ DWG โดยใช้ Java

## ข้อกำหนดเบื้องต้น

ก่อนที่เราจะเจาะลึกบทช่วยสอน ตรวจสอบให้แน่ใจว่าคุณมีข้อกำหนดเบื้องต้นต่อไปนี้:
1. ไลบรารี Aspose.CAD: ดาวน์โหลดและติดตั้งไลบรารี Aspose.CAD สำหรับ Java คุณสามารถค้นหาห้องสมุด[ที่นี่](https://releases.aspose.com/cad/java/).
2. Java Development Kit (JDK): ตรวจสอบให้แน่ใจว่าคุณได้ติดตั้ง Java บนระบบของคุณ
3. สภาพแวดล้อมการพัฒนาแบบรวม (IDE): เลือก Java IDE เช่น Eclipse หรือ IntelliJ เพื่อประสบการณ์การพัฒนาที่ราบรื่นยิ่งขึ้น

## แพ็คเกจนำเข้า

ในโปรเจ็กต์ Java ของคุณ ให้นำเข้าแพ็คเกจ Aspose.CAD ที่จำเป็นเพื่อเปิดใช้งานการจัดการไฟล์ CAD นี่คือตัวอย่าง:

```java
import com.aspose.cad;
import com.aspose.cad.imageoptions;
import com.aspose.cad.fileformats.cad.cadconsts;
import com.aspose.cad.fileformats.cad;
import com.aspose.cad.fileformats.cad.cadobjects;
```

## ขั้นตอนที่ 1: ตั้งค่าเส้นทางไฟล์

 กำหนดเส้นทางไฟล์อินพุตและเอาต์พุตสำหรับไฟล์ DWG อัพเดต`dataDir`, `fileName` , และ`outPath` ตัวแปรตาม

```java
String dataDir = "Your Document Directory" + "ExportingDGN/";
String fileName = dataDir + "BlockRefDgn.dwg";
String outPath = dataDir + "BlockRefDgn.dwg.pdf";
```

## ขั้นตอนที่ 2: สร้างอินสแตนซ์ PdfOptions

 สร้างอินสแตนซ์ของ`PdfOptions` เนื่องจากเรากำลังส่งออกไฟล์ DWG เป็นรูปแบบ PDF

```java
PdfOptions exportOptions = new PdfOptions();
```

## ขั้นตอนที่ 3: โหลดไฟล์ DWG

 โหลดไฟล์ DWG ที่มีอยู่เป็นรูปภาพและแปลงเป็นไฟล์`CadImage` พิมพ์.

```java
CadImage cadImage = (CadImage) Image.load(fileName);
```

## ขั้นตอนที่ 4: วนซ้ำผ่านเอนทิตี

ตรวจสอบแต่ละเอนทิตีภายในไฟล์ DWG และตรวจสอบว่าเป็นคำจำกัดความของรูปภาพหรือไม่ ถ้าเป็นเช่นนั้น ให้ดึงข้อมูลการอ้างอิงภายนอกไปยังออบเจ็กต์

```java
for (CadBaseEntity baseEntity : cadImage.getEntities()) {
    if (baseEntity.getTypeName() == CadEntityTypeName.DGNUNDERLAY) {
        CadDgnUnderlay dgnFile = (CadDgnUnderlay)baseEntity;
        System.out.println(dgnFile.getUnderlayPath());
    }
}
```

## ขั้นตอนที่ 5: กำหนดตัวเลือกการแรสเตอร์

 กำหนดการตั้งค่าสำหรับ`CadRasterizationOptions`ออบเจ็กต์ รวมถึงความกว้างของหน้า ความสูง เค้าโครง และสีพื้นหลัง

```java
CadRasterizationOptions vectorRasterizationOptions = new CadRasterizationOptions();
vectorRasterizationOptions.setPageWidth(1600);
vectorRasterizationOptions.setPageHeight(1600);
vectorRasterizationOptions.setLayouts(new String[] { "Model" });
vectorRasterizationOptions.setAutomaticLayoutsScaling(false);
vectorRasterizationOptions.setNoScaling(true);
vectorRasterizationOptions.setBackgroundColor(Color.getBlack());
vectorRasterizationOptions.setDrawType(CadDrawTypeMode.UseObjectColor);
```

## ขั้นตอนที่ 6: ตั้งค่าตัวเลือกการแรสเตอร์เวกเตอร์

ตั้งค่าตัวเลือกการแรสเตอร์เวกเตอร์สำหรับการส่งออก

```java
exportOptions.setVectorRasterizationOptions(vectorRasterizationOptions);
```

## ขั้นตอนที่ 7: ส่งออก DWG เป็น PDF

 สุดท้าย ส่งออก DWG เป็น PDF โดยการเรียกไฟล์`save` วิธี.

```java
cadImage.save(outPath, exportOptions);
```

## บทสรุป

ยินดีด้วย! คุณได้เรียนรู้วิธีส่งออกไฟล์ DGN โดยเป็นส่วนหนึ่งของไฟล์ DWG โดยใช้ Aspose.CAD สำหรับ Java เรียบร้อยแล้ว ไลบรารีอันทรงพลังนี้มีความสามารถที่กว้างขวางสำหรับการทำงานกับไฟล์ CAD ทำให้งานการจัดการไฟล์ CAD ของคุณมีประสิทธิภาพและตรงไปตรงมา

## คำถามที่พบบ่อย

### คำถามที่ 1: ฉันจะหาเอกสารสำหรับ Aspose.CAD สำหรับ Java ได้ที่ไหน

 A1: สามารถดูเอกสารประกอบได้[ที่นี่](https://reference.aspose.com/cad/java/).

### คำถามที่ 2: ฉันจะดาวน์โหลดไลบรารี Aspose.CAD สำหรับ Java ได้อย่างไร

 A2: คุณสามารถดาวน์โหลดไลบรารีได้จาก[ลิงค์นี้](https://releases.aspose.com/cad/java/).

### คำถามที่ 3: Aspose.CAD สำหรับ Java มีรุ่นทดลองใช้ฟรีหรือไม่

 A3: ใช่ คุณสามารถค้นหารุ่นทดลองใช้ฟรีได้[ที่นี่](https://releases.aspose.com/).

### คำถามที่ 4: ฉันจะรับใบอนุญาตชั่วคราวสำหรับ Aspose.CAD สำหรับ Java ได้ที่ไหน

 A4: รับใบอนุญาตชั่วคราว[ที่นี่](https://purchase.aspose.com/temporary-license/).

### Q5: ต้องการความช่วยเหลือหรือมีคำถาม?

 A5: เยี่ยมชมฟอรั่มสนับสนุนชุมชน Aspose.CAD[ที่นี่](https://forum.aspose.com/c/cad/19).