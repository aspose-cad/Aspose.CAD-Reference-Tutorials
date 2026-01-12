---
date: 2026-01-12
description: เรียนรู้วิธีส่งออก DWG เป็น PDF ด้วย Java และ Aspose.CAD คู่มือขั้นตอนต่อขั้นตอนในการแปลง
  DWG เป็น PDF ปรับความละเอียดของผลลัพธ์ และบันทึก DWG เป็นภาพ
linktitle: Convert Particular DWG to PDF Using Java
second_title: Aspose.CAD Java API
title: dwg to pdf java – แปลง DWG เฉพาะเป็น PDF ด้วย Java
url: /th/java/dwg-file-operations/convert-dwg-to-image/
weight: 14
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# dwg to pdf java – แปลง DWG เฉพาะเป็น PDF ด้วย Java

## บทนำ

ในกระบวนการทำงานสถาปัตยกรรมและวิศวกรรมสมัยใหม่ การแปลงภาพวาด DWG เป็นเอกสาร PDF เป็นความต้องการที่พบบ่อย—ไม่ว่าจะเพื่อการตรวจสอบของลูกค้า, การจัดทำเอกสาร, หรือการเก็บรักษาแบบถาวร โดยใช้ **Aspose.CAD for Java** คุณสามารถส่งออก DWG เป็น PDF ได้โดยอัตโนมัติ ปรับความละเอียดของผลลัพธ์ และแม้กระทั่งกรองเอนทิตี้เฉพาะก่อนการเรนเดอร์ ในบทเรียนนี้เราจะเดินผ่านกระบวนการแปลง **dwg to pdf java** อย่างครบถ้วน ทีละขั้นตอน เพื่อให้คุณสามารถนำไปผสานในแอปพลิเคชัน Java ของคุณได้ทันที

## คำตอบเร็ว
- **ไลบรารีที่ทำการแปลงคืออะไร?** Aspose.CAD for Java.  
- **ฉันสามารถตั้งความละเอียดของภาพได้หรือไม่?** ใช่ – ใช้ `CadRasterizationOptions` เพื่อกำหนดความกว้างและความสูง.  
- **สามารถกรองเอนทิตี้ (เช่น เก็บเฉพาะข้อความ) ได้หรือไม่?** แน่นอน; คุณสามารถลบเอนทิตี้ที่ไม่ต้องการก่อนบันทึก.  
- **รูปแบบผลลัพธ์ของตัวอย่างคืออะไร?** ไฟล์ PDF, แต่ตัวเลือกการเรนเดอร์เดียวกันสามารถใช้กับ PNG, JPEG ฯลฯ.  
- **ต้องการไลเซนส์สำหรับการใช้งานในผลิตภัณฑ์หรือไม่?** จำเป็นต้องมีไลเซนส์เชิงพาณิชย์สำหรับการใช้งานที่ไม่ใช่การประเมินผล.

## dwg to pdf java คืออะไร?
`dwg to pdf java` หมายถึงการแปลงไฟล์ AutoCAD DWG เป็นเอกสาร PDF ด้วยโค้ด Java อย่างเป็นโปรแกรม วิธีนี้ช่วยขจัดขั้นตอนการส่งออกด้วยมือ, รองรับการประมวลผลแบบแบตช์, และให้คุณควบคุมตัวเลือกการเรนเดอร์ เช่น ขนาดหน้า, การสเกล, และการมองเห็นของเอนทิตี้ อย่างเต็มที่

## ทำไมต้องใช้ Aspose.CAD for Java?
- **ไม่ต้องติดตั้ง AutoCAD** – ไลบรารีจัดการการพาร์ส DWG ภายในเอง.  
- **การเรนเดอร์ที่แม่นยำสูง** – ข้อมูลเวกเตอร์จะถูกเก็บรักษาไว้, ข้อความยังคงเลือกได้.  
- **การควบคุมระดับละเอียด** – คุณสามารถกรองเอนทิตี้, ตั้ง DPI ที่กำหนดเอง, และเลือกฟอร์แมตราสเตอร์.  
- **ข้ามแพลตฟอร์ม** – ทำงานบนระบบปฏิบัติการใด ๆ ที่รองรับ Java.

## ข้อกำหนดเบื้องต้น

ก่อนเริ่มทำงาน, โปรดตรวจสอบว่าคุณมีสิ่งต่อไปนี้:

1. **Java Development Kit (JDK)** – JDK ที่เข้ากันได้ติดตั้งบนเครื่องของคุณ คุณสามารถดาวน์โหลด JDK ล่าสุดจาก [Oracle's website](https://www.oracle.com/java/technologies/javase-downloads.html).  
2. **Aspose.CAD for Java Library** – รับไลบรารีจาก [Aspose.CAD download page](https://releases.aspose.com/cad/java/).  
3. **IDE ที่คุณชอบ** – IntelliJ IDEA, Eclipse, หรือ IDE Java ใด ๆ ที่คุณต้องการ.

## นำเข้าแพ็กเกจ

ในโครงการ Java ของคุณ, ให้ทำการนำเข้าแพ็กเกจ Aspose.CAD ที่จำเป็นเพื่อการผสานที่ราบรื่น รวมโค้ดต่อไปนี้ในโปรเจคของคุณ:

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

## คู่มือขั้นตอนต่อขั้นตอน

### ขั้นตอนที่ 1: ตั้งค่าโปรเจคของคุณ
เพิ่มไฟล์ JAR ของ Aspose.CAD ไปยัง classpath ของโปรเจคและตรวจสอบว่า JDK ถูกตั้งค่าอย่างถูกต้องใน IDE ของคุณ ซึ่งจะทำให้คลาส `Image` และ `CadImage` พร้อมใช้งานในขั้นตอนคอมไพล์

### ขั้นตอนที่ 2: ระบุเส้นทางไฟล์ DWG
กำหนดตำแหน่งของไฟล์ DWG ที่ต้องการแปลง ปรับตัวแปร `dataDir` และ `sourceFilePath` ให้ชี้ไปยังไดเรกทอรีของคุณเอง

```java
String dataDir = "Your Document Directory" + "DWGDrawings/";
String sourceFilePath = dataDir + "visualization_-_conference_room.dwg";
```

### ขั้นตอนที่ 3: กรองเอนทิตี้ข้อความ (ไม่บังคับ)
หากคุณต้องการเอนทิตี้บางประเภทเท่านั้น—เช่น คำอธิบายข้อความ—คุณสามารถกรองออกก่อนการเรนเดอร์ โค้ดด้านล่างจะวนผ่านเอนทิตี้ทั้งหมดของ DWG, เก็บเฉพาะประเภท `TEXT` และละทิ้งส่วนที่เหลือ

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

### ขั้นตอนที่ 4: ตั้งค่าตัวเลือกการเรนเดอร์ – ปรับความละเอียดของผลลัพธ์
สร้างอินสแตนซ์ของ `CadRasterizationOptions` และกำหนดค่าคุณสมบัติต่าง ๆ ปรับ `pageWidth` และ `pageHeight` เพื่อควบคุมความละเอียดของ PDF ที่สร้าง (หรือฟอร์แมตราสเตอร์อื่น)

```java
CadRasterizationOptions rasterizationOptions = new CadRasterizationOptions();
rasterizationOptions.setPageWidth(1600);
rasterizationOptions.setPageHeight(1600);
rasterizationOptions.setAutomaticLayoutsScaling(true);
```

### ขั้นตอนที่ 5: ส่งออกเป็น PDF – การบันทึกขั้นสุดท้าย
ห่อหุ้มตัวเลือกการเรนเดอร์ไว้ในอ็อบเจ็กต์ `PdfOptions` แล้วบันทึกผลลัพธ์ ไฟล์ผลลัพธ์จะเป็น PDF ที่สะท้อนเอนทิตี้ที่กรองและความละเอียดที่คุณตั้งค่าไว้

```java
PdfOptions pdfOptions = new PdfOptions();
pdfOptions.setVectorRasterizationOptions(rasterizationOptions);
String outFile = dataDir + "result_out_generated.pdf";
cadImage.save(outFile, pdfOptions);
```

> **เคล็ดลับ:** หากต้องการฟอร์แมตภาพอื่น (PNG, JPEG, TIFF) ให้แทนที่ `PdfOptions` ด้วยคลาสตัวเลือกภาพที่สอดคล้องกันโดยคงการตั้งค่าการเรนเดอร์ไว้เช่นเดิม

ยินดีด้วย! คุณได้ทำการแปลง **dwg to pdf java** สำเร็จโดยใช้ Aspose.CAD for Java

## ปัญหาที่พบบ่อยและวิธีแก้

| ปัญหา | สาเหตุที่เป็นไปได้ | วิธีแก้ |
|-------|-------------------|----------|
| **Empty PDF** | ไฟล์ DWG ไม่ได้โหลดอย่างถูกต้อง (เส้นทางผิด) | ตรวจสอบให้ `sourceFilePath` ชี้ไปยังไฟล์ DWG ที่มีอยู่จริง |
| **Missing text** | ลอจิกการกรองลบเอนทิตี้ที่ต้องการ | ปรับเงื่อนไข `if` หรือข้ามการกรองหากต้องการทุกเอนทิตี้ |
| **Low resolution** | `pageWidth`/`pageHeight` มีค่าต่ำเกินไป | เพิ่มค่า; 1600 × 1600 เป็นจุดเริ่มต้นที่ดีสำหรับ PDF คุณภาพสูง |
| **OutOfMemoryError** on large DWG files | หน่วยความจำ heap ไม่เพียงพอ | รัน JVM ด้วย heap ที่ใหญ่ขึ้น (`-Xmx2g` หรือมากกว่า) |

## คำถามที่พบบ่อย

**Q: Aspose.CAD รองรับไฟล์ DWG ทุกเวอร์ชันหรือไม่?**  
A: รองรับ, Aspose.CAD รองรับช่วงเวอร์ชัน DWG ที่กว้าง ตั้งแต่รุ่นแรกจนถึงฟอร์แมต AutoCAD ล่าสุด

**Q: ฉันสามารถปรับความละเอียดของภาพผลลัพธ์ได้หรือไม่?**  
A: แน่นอน. ใช้ `CadRasterizationOptions.setPageWidth()` และ `setPageHeight()` เพื่อกำหนด DPI หรือขนาดพิกเซลที่ต้องการ

**Q: สามารถทำการแปลงแบบแบตช์ได้หรือไม่?**  
A: ได้. ให้วนลูปตรรกะการแปลงภายในลูปที่ทำงานกับคอลเลกชันของเส้นทางไฟล์ DWG

**Q: จะหาแหล่งสนับสนุนหรือการสนทนาชุมชนเพิ่มเติมได้จากที่ไหน?**  
A: เยี่ยมชม [Aspose.CAD forum](https://forum.aspose.com/c/cad/19) เพื่อรับความช่วยเหลือจากชุมชนและวิศวกรของ Aspose

**Q: สามารถทดลองใช้ Aspose.CAD ก่อนซื้อได้หรือไม่?**  
A: ได้, ลองใช้เครื่องมือด้วยการทดลองฟรีที่มีให้ที่ [this link](https://releases.aspose.com/)

## สรุป

การส่งออก DWG เป็น PDF ด้วย Java ทำได้อย่างง่ายดายด้วย Aspose.CAD โดยทำตามขั้นตอนข้างต้น คุณสามารถ **export dwg as pdf**, **save dwg as image**, และ **customize output resolution** ให้ตรงกับความต้องการของโครงการของคุณ ผสานเวิร์กโฟลว์นี้เข้าสู่สายงานอัตโนมัติเพื่อเพิ่มประสิทธิภาพและรับประกันเอกสารคุณภาพสูงอย่างสม่ำเสมอ

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}

---

**อัปเดตล่าสุด:** 2026-01-12  
**ทดสอบด้วย:** Aspose.CAD for Java 24.12  
**ผู้เขียน:** Aspose  

---