---
date: 2026-02-17
description: เรียนรู้วิธีบันทึกไฟล์ DWG เป็น JPEG ใน Java ด้วย Aspose.CAD, เพิ่มหลายเลเยอร์,
  และปรับขนาด CAD เพื่อการแปลงภาพที่แม่นยำ.
linktitle: Support of Layers in CAD
second_title: Aspose.CAD Java API
title: บันทึก DWG เป็น JPEG พร้อมการสนับสนุนเลเยอร์ใน Java
url: /th/java/advanced-cad-features/support-of-layers-in-cad/
weight: 18
---

 preserved. Keep code block placeholders unchanged.

Now produce final answer.{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# บันทึก DWG เป็น JPEG พร้อมการสนับสนุนเลเยอร์ใน Java

## บทนำ

ในบทแนะนำนี้คุณจะได้เรียนรู้วิธี **บันทึก DWG เป็น JPEG** พร้อมใช้ประโยชน์เต็มที่จากการสนับสนุนเลเยอร์ใน Aspose.CAD สำหรับ Java. เลเยอร์ช่วยให้คุณแยกส่วนเฉพาะของภาพวาด ทำให้การส่งออกเฉพาะสิ่งที่ต้องการเป็นเรื่องง่าย เราจะเดินผ่านแต่ละขั้นตอน ตั้งแต่การตั้งค่าสภาพแวดล้อมจนถึงการส่งออก JPEG ที่รวมเฉพาะเลเยอร์ที่คุณเลือก.

## คำตอบอย่างรวดเร็ว
- **“บันทึก DWG เป็น JPEG” หมายถึงอะไร?** มันแปลงภาพวาด DWG (หรือ CAD ประเภทอื่น) เป็นภาพ JPEG แบบแรสเตอร์.  
- **ฉันสามารถรวมเฉพาะเลเยอร์ที่เลือกได้หรือไม่?** ได้ – ใช้เมธอด `setLayers` เพื่อระบุว่าเลเยอร์ใดจะเรนเดอร์.  
- **ฉันจะเปลี่ยนขนาดภาพได้อย่างไร?** ปรับ `setPageWidth` และ `setPageHeight` ใน `CadRasterizationOptions`.  
- **นี่เป็นโซลูชันสำหรับ Java เท่านั้นหรือไม่?** ตัวอย่างใช้ Aspose.CAD สำหรับ Java แต่แนวคิดเดียวกันสามารถใช้กับภาษาอื่นได้.  
- **ฉันต้องการไลเซนส์หรือไม่?** การทดลองใช้ฟรีสามารถใช้สำหรับการทดสอบได้; จำเป็นต้องมีไลเซนส์เชิงพาณิชย์สำหรับการใช้งานจริง.

## “บันทึก DWG เป็น JPEG” คืออะไร?
การบันทึก DWG เป็น JPEG หมายถึงการทำให้ไฟล์ CAD แบบเวกเตอร์ (DWG, DWF, DXF ฯลฯ) เป็นบิตแมพ JPEG มาตรฐาน การทำเช่นนี้มีประโยชน์เมื่อคุณต้องการฝังภาพวาด CAD ลงในหน้าเว็บ, อีเมล, หรือรายงานที่รองรับเฉพาะภาพแรสเตอร์เท่านั้น.

## ทำไมต้องใช้การแปลง JPEG ที่รับรู้เลเยอร์?
- **มุ่งเน้นข้อมูลที่เกี่ยวข้อง:** ส่งออกเฉพาะเลเยอร์ที่คุณต้องการ ลดขนาดไฟล์และความยุ่งเหยิงของภาพ  
- **รักษาวัตถุประสงค์การออกแบบ:** เลเยอร์รักษาการจัดกลุ่มเชิงตรรกะของวัตถุ ทำให้คุณสามารถใช้ไฟล์ต้นฉบับเดียวกันสำหรับผลลัพธ์ที่แตกต่างกัน  
- **ควบคุมขนาดได้เต็มที่:** โดยการปรับตัวเลือกการเรซอร์ไรซ์ คุณสามารถสร้างภาพความละเอียดสูงที่ตรงกับความต้องการการเผยแพร่ของคุณ  

## ข้อกำหนดเบื้องต้น

ก่อนเริ่มทำงาน ตรวจสอบให้แน่ใจว่าคุณมีสิ่งต่อไปนี้:

1. **Aspose.CAD for Java Library** – ดาวน์โหลดจาก [website](https://releases.aspose.com/cad/java/). ทำตามคู่มือการติดตั้งเพื่อเพิ่มไฟล์ JAR ไปยัง classpath ของโปรเจกต์ของคุณ.  
2. **Java Development Environment** – JDK รุ่นล่าสุด (8 หรือใหม่กว่า) ที่ติดตั้งบนเครื่องของคุณ.

เมื่อเราตั้งค่าเรียบร้อยแล้ว มาดูโค้ดที่จำเป็นสำหรับ **บันทึก DWG เป็น JPEG** พร้อมการเรนเดอร์เลเยอร์แบบเลือก.

## นำเข้า Namespaces

เริ่มต้นด้วยการนำเข้าคลาส Aspose.CAD ที่จำเป็นและยูทิลิตี้มาตรฐานของ Java:

```java
import com.aspose.cad.Image;

import com.aspose.cad.imageoptions.CadRasterizationOptions;
import com.aspose.cad.imageoptions.JpegOptions;
import java.util.ArrayList;
import java.util.Arrays;
import java.util.List;
```

## คู่มือขั้นตอนต่อขั้นตอน

### ขั้นตอนที่ 1: ตั้งค่าเส้นทางไฟล์

กำหนดตำแหน่งที่ไฟล์ DWF ต้นทางอยู่และที่ที่ไฟล์ JPEG ผลลัพธ์จะถูกเขียน.

```java
String dataDir = "Your Document Directory" + "DWFDrawings/";
String srcFile = dataDir + "for_layers_test.dwf";
String outFile = dataDir + "for_layers_test.jpg";
```

### ขั้นตอนที่ 2: โหลดภาพ DWF

ใช้เมธอด `Image.load` ของ Aspose.CAD เพื่ออ่านภาพวาด CAD.

```java
Image image = Image.load(srcFile);
```

### ขั้นตอนที่ 3: กำหนดค่าตัวเลือกการเรซอร์ไรซ์ (ปรับขนาด CAD)

สร้างอินสแตนซ์ `CadRasterizationOptions` และตั้งค่าขนาดผลลัพธ์ที่ต้องการ การเปลี่ยนค่าเหล่านี้ทำให้คุณ **ปรับขนาด CAD** สำหรับ JPEG สุดท้าย.

```java
CadRasterizationOptions rasterizationOptions = new CadRasterizationOptions();
rasterizationOptions.setPageWidth(1600);
rasterizationOptions.setPageHeight(1600);
```

### ขั้นตอนที่ 4: ระบุเลเยอร์ (เพิ่มหลายเลเยอร์)

หากคุณต้องการเรนเดอร์มากกว่าหนึ่งเลเยอร์ เพียงเพิ่มชื่อของพวกมันลงในรายการ ที่นี่เราเริ่มต้นด้วยเลเยอร์เดียวชื่อ “LayerA”.

```java
List<String> stringList = new ArrayList<>(Arrays.asList("LayerA"));
rasterizationOptions.setLayers(stringList);
```

*เคล็ดลับ:* เพื่อ **เพิ่มหลายเลเยอร์**, ขยายการเรียก `Arrays.asList` เช่น `Arrays.asList("LayerA", "LayerB", "LayerC")`. สิ่งนี้ทำให้คุณ **เลือกเลเยอร์ CAD เฉพาะ** สำหรับการแปลง.

### ขั้นตอนที่ 5: กำหนดค่าตัวเลือก JPEG (Java แปลงภาพ CAD)

เชื่อมการตั้งค่าการเรซอร์ไรซ์กับรูปแบบผลลัพธ์ JPEG.

```java
JpegOptions jpegOptions = new JpegOptions();
jpegOptions.setVectorRasterizationOptions(rasterizationOptions);
```

### ขั้นตอนที่ 6: ส่งออกเป็น JPG (บันทึก DWG เป็น JPEG)

สุดท้าย เขียนภาพลงดิสก์ ขั้นตอนนี้ **บันทึกภาพวาด CAD เป็นไฟล์ JPEG** ที่มีเฉพาะเลเยอร์ที่เลือก.

```java
image.save(outFile, jpegOptions);
```

โดยทำตามขั้นตอนเหล่านี้ คุณได้ **บันทึก DWG เป็น JPEG** อย่างสำเร็จ พร้อมควบคุมว่าเลเยอร์ใดปรากฏและปรับขนาดภาพตามต้องการ.

## วิธีแปลง DWF เป็น JPEG พร้อมการเลือกเลเยอร์

แม้ว่าตัวอย่างจะใช้แหล่ง DWF แต่กระบวนการเรซอร์ไรซ์เดียวกันทำงานกับรูปแบบ CAD ที่รองรับทั้งหมด (DWG, DXF, DGN ฯลฯ) เพียงเปลี่ยนส่วนขยายไฟล์ใน `srcFile` แล้วไลบรารีจะจัดการการ **แปลง DWF เป็น JPEG** (หรือรูปแบบอื่น) โดยอัตโนมัติ.

## ปัญหาที่พบบ่อยและวิธีแก้

| ปัญหา | วิธีแก้ |
|-------|----------|
| **เลเยอร์ไม่แสดง** | ตรวจสอบว่าชื่อเลเยอร์ตรงกับที่เก็บในไฟล์ DWF อย่างแม่นยำ (คำนึงถึงตัวพิมพ์ใหญ่‑เล็ก). |
| **ภาพผลลัพธ์เป็นสีขาว** | ตรวจสอบให้แน่ใจว่า `setPageWidth` และ `setPageHeight` มีขนาดเพียงพอสำหรับขอบเขตของภาพวาด. |
| **ข้อยกเว้นไลเซนส์** | ใช้ไลเซนส์ทดลองสำหรับการทดสอบ; รับไลเซนส์เต็มสำหรับสภาพแวดล้อมการผลิต. |

## คำถามที่พบบ่อย

**Q: ฉันสามารถเพิ่มหลายเลเยอร์ในตัวเลือกการเรซอร์ไรซ์ได้หรือไม่?**  
A: แน่นอน. ขยาย `stringList` ด้วยชื่อเลเยอร์เพิ่มเติม เช่น `Arrays.asList("LayerA", "LayerB")`.

**Q: Aspose.CAD รองรับรูปแบบ CAD อื่นหรือไม่?**  
A: ใช่, รองรับ DWG, DXF, DWF และรูปแบบอื่น ๆ อีกหลายรูปแบบ.

**Q: ฉันจะเปลี่ยนขนาดภาพผลลัพธ์ได้อย่างไร?**  
A: ปรับ `setPageWidth` และ `setPageHeight` ในอินสแตนซ์ `CadRasterizationOptions`.

**Q: ฉันสามารถซื้อไลเซนส์สำหรับ Aspose.CAD ได้จากที่ไหน?**  
A: คุณสามารถสำรวจตัวเลือกการไลเซนส์ได้ [ที่นี่](https://purchase.aspose.com/buy).

**Q: ฉันจะได้รับการสนับสนุนจากชุมชนได้จากที่ไหน?**  
A: เข้าร่วมชุมชน Aspose.CAD ใน [ฟอรั่ม](https://forum.aspose.com/c/cad/19) เพื่อรับความช่วยเหลือและการสนทนา.

---

**อัปเดตล่าสุด:** 2026-02-17  
**ทดสอบด้วย:** Aspose.CAD for Java 24.11  
**ผู้เขียน:** Aspose  

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}