---
date: 2026-06-09
description: เรียนรู้วิธีส่งออก DXF และแปลงภาพวาด CAD เป็น PDF ด้วย Aspose.CAD for
  Java คู่มือทีละขั้นตอนนี้จะแสดงวิธีแปลง DXF เป็น PDF อย่างรวดเร็วและเชื่อถือได้
keywords:
- how to export dxf
- convert cad drawing pdf
- export dxf layer java
linktitle: ส่งออกเลเยอร์เฉพาะของภาพวาด DXF ไปเป็น PDF ด้วย Java
schemas:
- author: Aspose
  dateModified: '2026-06-09'
  description: Learn how to export dxf and convert CAD drawing PDF using Aspose.CAD
    for Java. This step‑by‑step guide shows you how to convert DXF to PDF quickly
    and reliably.
  headline: How to Export DXF Layer to PDF with Aspose.CAD for Java
  type: TechArticle
- questions:
  - answer: Yes. Modify the `stringList` in Step 3 to include all desired layer names,
      e.g., `Arrays.asList("LayerA", "LayerB")`.
    question: Can I export multiple layers simultaneously?
  - answer: Aspose.CAD supports over 30 DXF versions, from the early R12 format up
      to the latest 2023 release, ensuring broad compatibility.
    question: Is Aspose.CAD compatible with all DXF versions?
  - answer: Wrap the loading and saving code in a `try‑catch` block and log `Exception`
      details. This lets you gracefully handle corrupted files or permission issues.
    question: How should I handle errors during the export process?
  - answer: Yes. A temporary license is fine for evaluation, but a purchased license
      removes evaluation watermarks and unlocks full functionality.
    question: Do I need a commercial license for production use?
  - answer: Visit the [Aspose.CAD forum](https://forum.aspose.com/c/cad/19) for community
      support, or check the official API documentation for more code samples.
    question: Where can I get additional help or examples?
  type: FAQPage
second_title: Aspose.CAD Java API
title: วิธีส่งออกเลเยอร์ DXF ไปเป็น PDF ด้วย Aspose.CAD for Java
url: /th/java/additional-features/export-specific-layer-to-pdf/
weight: 18
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# วิธีส่งออกชั้น DXF ไปเป็น PDF ด้วย Aspose.CAD for Java

## บทนำ

หากคุณต้องการเรียนรู้ **วิธีส่งออก dxf** จากแบบร่างไปเป็น PDF พร้อมคงไว้เฉพาะชั้นที่คุณสนใจ Aspose.CAD for Java ทำให้ขั้นตอนนี้ง่ายดาย ในบทแนะนำนี้เราจะเดินผ่านสถานการณ์จริง: การส่งออกชั้นเดียวของไฟล์ DXF ไปเป็นเอกสาร PDF คุณจะเห็นว่าการทำเช่นนี้มีประโยชน์อย่างไรสำหรับการสร้างแบบร่างที่มีน้ำหนักเบา การแชร์รายละเอียดการออกแบบกับผู้ใช้ที่ไม่มี CAD หรือการสร้างสายงานการรายงานอัตโนมัติ

## คำตอบอย่างรวดเร็ว
- **บทเรียนนี้ครอบคลุมอะไร?** การส่งออกชั้น DXF เฉพาะไปเป็น PDF ด้วย Aspose.CAD for Java  
- **ประโยชน์หลัก?** คุณจะเก็บเฉพาะเรขาคณิตที่ต้องการ ลดขนาดไฟล์และความรกของภาพ  
- **ข้อกำหนดเบื้องต้น?** Java SDK, ไลบรารี Aspose.CAD for Java, และไฟล์ DXF ที่จะทำงานด้วย  
- **ใช้เวลานานเท่าไหร่ในการทำงาน?** ประมาณ 10‑15 นาทีสำหรับการตั้งค่าเบื้องต้น  
- **สามารถส่งออกหลายชั้นได้หรือไม่?** ได้ – เพียงปรับรายการชั้น (ดูขั้นตอน 3)

## วิธีส่งออกชั้น DXF ไปเป็น PDF?

ใช้คลาส `Image` ของ Aspose.CAD เพื่อโหลดไฟล์ DXF กำหนดค่า `CadRasterizationOptions` ด้วยชื่อชั้นที่ต้องการ แล้วบันทึกภาพเป็น PDF ผ่าน `PdfOptions` เพียงสามบรรทัดของโค้ดคุณก็สามารถแยกชั้นเดียวและสร้าง PDF ที่มีน้ำหนักเบาสำหรับการแชร์ได้

## “สร้าง PDF จาก DXF” คืออะไร?

กระบวนการแปลงไฟล์ DXF (Drawing Exchange Format) ให้เป็นเอกสาร PDF เป็นความต้องการทั่วไปเมื่อข้อมูล CAD ต้องแชร์กับผู้มีส่วนได้ส่วนเสียที่ไม่มีซอฟต์แวร์ CAD รูปแบบ PDF รักษาความแม่นยำของภาพขณะเป็นรูปแบบที่ทุกคนสามารถเปิดดูได้

## ทำไมต้องใช้ Aspose.CAD for Java เพื่อแปลง DXF เป็น PDF?

Aspose.CAD for Java ให้โซลูชันแบบ pure‑Java ที่ไม่ต้องพึ่งพาคอมโพเนนต์ CAD แบบเนทีฟ ทำให้การแปลงทำงานได้อย่างน่าเชื่อถือบนทุกแพลตฟอร์ม มีการเลือกชั้นที่แม่นยำ การเรเซอร์ความละเอียดสูง และรองรับเวอร์ชัน DXF มากมาย เหมาะสำหรับงานอัตโนมัติและการสร้าง PDF ที่มีน้ำหนักเบา

- **ไม่มีการพึ่งพาไลบรารีภายนอก** – pure Java, ไม่ต้องใช้ DLL เนทีฟ  
- **การควบคุมชั้นแบบละเอียด** – สามารถเลือกได้สูงสุด 100 ชั้นต่อการส่งออก ทำให้ผลลัพธ์เบา  
- **เรเซอร์คุณภาพสูง** – ปรับ DPI, ขนาดหน้า, และตัวเลือกการเรนเดอร์ได้; Aspose.CAD รองรับเวอร์ชัน DXF มากกว่า 30 เวอร์ชัน ตั้งแต่ R12 จนถึงรุ่นล่าสุด 2023  
- **ข้ามแพลตฟอร์ม** – ทำงานบน Windows, Linux, และ macOS  
- **ประสิทธิภาพ** – ประมวลผลแบบร่างหลายร้อยหน้าในเวลาน้อยกว่า 2 วินาทีบนเซิร์ฟเวอร์มาตรฐานเมื่อเรเซอร์จำกัดที่ชั้นเดียว

## ข้อกำหนดเบื้องต้น

- **Aspose.CAD for Java Library** – ดาวน์โหลดจาก [Aspose.CAD Java documentation](https://reference.aspose.com/cad/java/)  
- **สภาพแวดล้อมการพัฒนา Java** – JDK 8 หรือสูงกว่า พร้อม IDE หรือเครื่องมือสร้างที่คุณเลือก

## นำเข้า Namespace

Namespace `com.aspose.cad` มีคลาสหลักสำหรับการโหลดและเรนเดอร์ไฟล์ CAD การจัดกลุ่ม import ไว้ด้วยกันช่วยให้โค้ดอ่านง่ายและอัปเดตในอนาคตได้สะดวก

```java
import com.aspose.cad.Image;

import com.aspose.cad.imageoptions.CadRasterizationOptions;
import com.aspose.cad.imageoptions.PdfOptions;
import java.util.ArrayList;
import java.util.Arrays;
import java.util.List;
```

## ขั้นตอน 1: ตั้งค่าโฟลเดอร์ทรัพยากร

กำหนดโฟลเดอร์ที่เก็บไฟล์ DXF ต้นฉบับของคุณ แทนที่ตัวแปร placeholder ด้วยพาธจริงบนเครื่องของคุณ

```java
String dataDir = "Your Document Directory" + "DXFDrawings/";
```

## ขั้นตอน 2: โหลดแบบร่าง DXF

คลาส `Image` แสดงแบบร่าง CAD ที่ถูกเรเซอร์แล้วและสามารถบันทึกในหลายรูปแบบ โหลดไฟล์ DXF เข้าออบเจ็กต์ `Image`; Aspose.CAD จะตรวจจับรูปแบบไฟล์โดยอัตโนมัติ

```java
String srcFile = dataDir + "conic_pyramid.dxf";
Image image = Image.load(srcFile);
```

## ขั้นตอน 3: กำหนดค่า Rasterization Options (เลือกชั้น)

ที่นี่เราบอก Aspose.CAD ว่าจะเรนเดอร์ชั้นใด `CadRasterizationOptions` ให้คุณระบุรายการชื่อชั้น, DPI, และขนาดหน้า ตัวอย่างใช้เฉพาะชั้นเริ่มต้น `"0"` หากต้องการส่งออกชั้นอื่นให้แทนที่ `"0"` ด้วยชื่อชั้นที่ตรงกับแบบร่างของคุณ

```java
CadRasterizationOptions rasterizationOptions = new CadRasterizationOptions();
rasterizationOptions.setPageWidth(1600);
rasterizationOptions.setPageHeight(1600);

List<String> stringList = new ArrayList<>(Arrays.asList("0"));
rasterizationOptions.setLayers(stringList);
```

**เคล็ดลับ:** คุณสามารถเพิ่มชื่อชั้นหลายชื่อลงใน `stringList` (เช่น `Arrays.asList("Layer1", "Layer2")`) เพื่อส่งออกหลายชั้นพร้อมกัน

## ขั้นตอน 4: สร้าง PDF Options

คลาส `PdfOptions` เชื่อมการตั้งค่า rasterization กับการกำหนดค่า PDF โดยการส่งออบเจ็กต์ `CadRasterizationOptions` ไปยัง `PdfOptions` คุณจะมั่นใจว่าชั้นที่เลือกเป็นเนื้อหาเดียวที่เรนเดอร์ใน PDF สุดท้าย

```java
PdfOptions pdfOptions = new PdfOptions();
pdfOptions.setVectorRasterizationOptions(rasterizationOptions);
```

## ขั้นตอน 5: ส่งออกเป็น PDF (สร้าง PDF จาก DXF)

สุดท้ายบันทึกชั้นที่เลือกเป็นไฟล์ PDF PDF ที่ได้จะมีเพียงเรขาคณิตจากชั้นที่คุณระบุ ทำให้ไฟล์เบาและง่ายต่อการแชร์

```java
image.save(dataDir + "conic_pyramid_layer_out_.pdf", pdfOptions);
```

## ปัญหาที่พบบ่อย & วิธีแก้

| ปัญหา | สาเหตุ | วิธีแก้ |
|-------|--------|-----|
| **ไม่มีผลลัพธ์หรือ PDF ว่าง** | ชื่อชั้นไม่ตรงหรือความแตกต่างของตัวพิมพ์ | ตรวจสอบชื่อชั้นที่แน่นอนใน DXF (ใช้ CAD viewer) แล้วให้ตรงกับที่ตั้งค่าใน `setLayers` |
| **สเกลไม่ถูกต้อง** | ความกว้าง/สูงของหน้าไม่ตรงกับหน่วยของแบบร่าง | ปรับ `setPageWidth` / `setPageHeight` หรือกำหนด `setResolution` ใน `CadRasterizationOptions` |
| **ข้อยกเว้นไลเซนส์** | ใช้รุ่นทดลองโดยไม่ได้ตั้งค่าไลเซนส์ | โหลดไฟล์ไลเซนส์ด้วย `License license = new License(); license.setLicense("Aspose.CAD.Java.lic");` |
| **ความช้าเมื่อไฟล์ใหญ่** | เรนเดอร์ทุกชั้นโดยไม่จำเป็น | จำกัด `stringList` ให้มีเฉพาะชั้นที่ต้องการและลด DPI หากไม่ต้องการความละเอียดสูง |
| **สีไม่ตรงตามที่คาด** | การจัดการสีเริ่มต้นต่างจาก CAD ต้นฉบับ | ใช้ `setBackgroundColor` หรือ `setColorMode` ใน `CadRasterizationOptions` เพื่อให้ตรงกับพาเลตต์ต้นฉบับ |

## คำถามที่พบบ่อย

**ถาม: สามารถส่งออกหลายชั้นพร้อมกันได้หรือไม่?**  
ตอบ: ได้. ปรับ `stringList` ในขั้นตอน 3 ให้รวมชื่อชั้นที่ต้องการทั้งหมด เช่น `Arrays.asList("LayerA", "LayerB")`

**ถาม: Aspose.CAD รองรับเวอร์ชัน DXF ทั้งหมดหรือไม่?**  
ตอบ: Aspose.CAD รองรับเวอร์ชัน DXF มากกว่า 30 เวอร์ชัน ตั้งแต่รูปแบบ R12 เริ่มต้นจนถึงรุ่นล่าสุด 2023 ทำให้เข้ากันได้อย่างกว้างขวาง

**ถาม: ควรจัดการข้อผิดพลาดระหว่างการส่งออกอย่างไร?**  
ตอบ: ห่อโค้ดการโหลดและบันทึกในบล็อก `try‑catch` แล้วบันทึกรายละเอียดของ `Exception` เพื่อให้สามารถจัดการไฟล์เสียหายหรือปัญหาการเข้าถึงได้อย่างราบรื่น

**ถาม: ต้องใช้ไลเซนส์เชิงพาณิชย์สำหรับการใช้งานในผลิตภัณฑ์หรือไม่?**  
ตอบ: ใช่. ไลเซนส์ชั่วคราวเพียงพอสำหรับการประเมินผล แต่ไลเซนส์ที่ซื้อจะลบลายน้ำการประเมินและเปิดใช้งานฟังก์ชันเต็มรูปแบบ

**ถาม: จะหาแนวทางช่วยเหลือหรือโค้ดตัวอย่างเพิ่มเติมได้จากที่ไหน?**  
ตอบ: เยี่ยมชม [Aspose.CAD forum](https://forum.aspose.com/c/cad/19) เพื่อรับการสนับสนุนจากชุมชน หรือดูเอกสาร API อย่างเป็นทางการสำหรับตัวอย่างโค้ดเพิ่มเติม

## สรุป

คุณได้เรียนรู้ **วิธีส่งออก dxf** โดยเลือกชั้นเฉพาะและแปลงเป็น PDF ด้วย Aspose.CAD for Java เทคนิคนี้ให้คุณควบคุมเนื้อหาภาพที่สร้างใน PDF อย่างเต็มที่ เหมาะสำหรับการแชร์แบบร่างเบา, รายงานอัตโนมัติ, หรือการผสานข้อมูล CAD เข้ากับแอปพลิเคชัน Java ขนาดใหญ่ อย่าลังเลทดลองปรับตั้งค่า rasterization, การเลือกชั้น, และตัวเลือก PDF ต่าง ๆ ให้ตรงกับความต้องการของโครงการของคุณ

---

**Last Updated:** 2026-06-09  
**Tested With:** Aspose.CAD for Java 24.11  
**Author:** Aspose

## บทแนะนำที่เกี่ยวข้อง

- [วิธีแปลง DXF เป็น PDF ด้วย Aspose.CAD for Java](/cad/java/additional-features/)
- [สร้าง PDF จาก CAD – ส่งออก DXF เป็น PDF ด้วย Aspose.CAD for Java](/cad/java/additional-features/export-dxf-to-pdf/)
- [วิธีส่งออกเลเอาต์ DXF ไปเป็น PDF ด้วย Aspose.CAD for Java](/cad/java/additional-features/export-specific-layout-to-pdf/)

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}