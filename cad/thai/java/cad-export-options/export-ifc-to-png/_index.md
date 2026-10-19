---
date: 2026-10-19
description: เรียนรู้วิธีสร้างไฟล์ภาพย่อ PNG ของ IFC ด้วย Aspose.CAD for Java เพียงไม่กี่บรรทัดของโค้ด
keywords:
- create png thumbnail ifc
- ifc to png conversion
- aspose cad java
- java image processing
- bIM visualization
lastmod: 2026-10-19
linktitle: ส่งออก IFC เป็น PNG
og_description: สร้างไฟล์ภาพย่อ PNG ของ IFC อย่างง่ายดายโดยใช้ Aspose.CAD for Java
  คู่มือขั้นตอนต่อขั้นตอนนี้จะแสดงวิธีโหลด, rasterize, และบันทึกโมเดล IFC เป็นภาพ
  PNG คุณภาพสูง
og_image_alt: Developer guide showing Java code that converts IFC files to PNG thumbnails
  using Aspose.CAD
og_title: สร้างภาพย่อ PNG ของ IFC ด้วย Aspose.CAD for Java
schemas:
- author: Aspose
  dateModified: '2026-10-19'
  description: Learn how to create PNG thumbnail IFC files with Aspose.CAD for Java
    in just a few lines of code.
  headline: How to create PNG thumbnail IFC with Aspose.CAD for Java
  type: TechArticle
- description: Learn how to create PNG thumbnail IFC files with Aspose.CAD for Java
    in just a few lines of code.
  name: How to create PNG thumbnail IFC with Aspose.CAD for Java
  steps:
  - name: load the IFC file
    text: First, point to the folder where your IFC file lives and load it with `CadImage.load`.
      `CadImage.load` reads a CAD file and returns an image object that can be rasterized.
      > **Why this matters:** Loading the file as a `CadImage` gives you access to
      vector‑raster conversion options that control resol
  - name: set rasterization options
    text: Define the output dimensions and any other vector‑related settings through
      `VectorRasterizationOptions`. `VectorRasterizationOptions` lets you specify
      output size, background color, and other rasterization parameters. > Adjust
      `PageWidth` and `PageHeight` to control the final PNG resolution, which i
  - name: configure PNG options
    text: Link the rasterization options to the PNG exporter by creating a `PngOptions`
      instance.
  - name: save the image as PNG
    text: Finally, write the rasterized image to disk using the `save` method. `save`
      writes the rasterized image to the specified file path in the chosen format.
      > After this step you have successfully **created a PNG thumbnail IFC** and
      can use the resulting `example.png` anywhere you need a raster image.
  type: HowTo
- questions:
  - answer: Yes, Aspose.CAD supports many formats (DWG, DXF, DGN, etc.). Simply change
      the file extension and load the appropriate image class.
    question: Can I use this approach to convert other CAD formats to PNG?
  - answer: DPI is controlled indirectly via `PageWidth`/`PageHeight`. Adjust these
      values relative to the desired physical size to achieve the required DPI.
    question: Does the library let me set a custom DPI?
  - answer: PNG is a lossless format, so the rasterized image retains the full visual
      fidelity of the original vector data.
    question: Is the PNG output loss‑less?
  type: FAQPage
second_title: Aspose.CAD Java API
tags:
- ifc conversion
- png thumbnail
- aspose.cad
- java image processing
- bim visualization
title: วิธีสร้างภาพย่อ PNG ของ IFC ด้วย Aspose.CAD for Java
url: /th/java/cad-export-options/export-ifc-to-png/
weight: 18
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# ส่งออก IFC เป็น PNG ด้วย Aspose.CAD สำหรับ Java

## บทนำ

ในบทเรียนนี้คุณจะได้เรียนรู้วิธี **create PNG thumbnail IFC** ด้วย Aspose.CAD for Java ไม่ว่าคุณจะต้องการตัวอย่างอย่างเร็วสำหรับพอร์ทัล BIM, สร้างภาพย่อสำหรับระบบจัดการเอกสาร, หรือทำการแปลงเป็นชุดอัตโนมัติ ขั้นตอนต่อไปนี้จะช่วยให้คุณแปลงโมเดล IFC 3‑D เป็นภาพ PNG 2‑D ที่คมชัดเพียงไม่กี่บรรทัดของโค้ด Java

## คำตอบอย่างรวดเร็ว
- **ต้องใช้ไลบรารีอะไร?** Aspose.CAD for Java.  
- **ฉันสามารถสร้าง PNG thumbnail IFC ด้วยไม่กี่บรรทัดของโค้ดได้หรือไม่?** Yes – the entire workflow fits in under 20 lines.  
- **ต้องการใบอนุญาตสำหรับการผลิตหรือไม่?** A temporary license works for testing; a full license is required for commercial deployment.  
- **ผลลัพธ์สามารถขยายขนาดได้หรือไม่?** You can set any pixel dimensions, so the PNG scales to any size you need.  
- **รองรับเวอร์ชัน Java ใด?** Java 8 or higher.

## “convert IFC to PNG” คืออะไร?
การแปลง IFC (Industry Foundation Classes) เป็น PNG หมายถึงการทำให้โมเดลอาคาร 3‑D เป็นภาพบิตแมพ 2‑D การทำเช่นนี้สร้างภาพย่อที่สามารถแสดงในเบราว์เซอร์, รายงาน หรือแอปมือถือโดยไม่ต้องใช้ตัวดู CAD เต็มรูปแบบ

## ทำไมต้องใช้ Aspose.CAD สำหรับ Java?
Aspose.CAD รองรับ **30+ CAD and BIM formats** รวมถึง IFC, DWG, DXF, และ DGN และสามารถประมวลผลไฟล์ได้ถึง **2 GB** โดยไม่ต้องโหลดเอกสารทั้งหมดเข้าสู่หน่วยความจำ ไลบรารีนี้เป็น Java แท้, มี **zero external dependencies** และทำงานบน Windows, Linux, และ macOS ทำให้เหมาะสำหรับการสร้างภาพบนเซิร์ฟเวอร์  
มันให้การเรสเตอร์ไลซ์ที่มีประสิทธิภาพสูง, รองรับรูปแบบอย่างกว้างขวาง, และการผสานรวมที่ง่ายในแอปพลิเคชัน Java

## ข้อกำหนดเบื้องต้น
- **Aspose.CAD Library** – ดาวน์โหลด JAR ล่าสุดจาก the [download link](https://releases.aspose.com/cad/java/).  
- **Java Development Kit** – JDK 8 หรือใหม่กว่า ติดตั้งบนเครื่องของคุณ.  
- **IFC source file** – วางไฟล์ในโฟลเดอร์ที่คุณสามารถอ้างอิงจากโค้ดของคุณ.

## นำเข้า namespace
แพคเกจ `com.aspose.cad` ให้คลาสทั้งหมดที่คุณต้องการ `CadImage` เป็นจุดเริ่มต้นสำหรับการโหลดไฟล์ CAD, ส่วน `PngOptions` กำหนดค่าการเรสเตอร์ไลซ์

```java
import com.aspose.cad.Image;

import com.aspose.cad.fileformats.ifc.IfcImage;
import com.aspose.cad.imageoptions.CadRasterizationOptions;
import com.aspose.cad.imageoptions.PngOptions;
```

## วิธีสร้าง PNG thumbnail IFC ด้วย Java?
โหลดไฟล์ IFC, กำหนดตัวเลือกการเรสเตอร์ไลซ์, และบันทึกผลลัพธ์เป็นภาพ PNG – นี่คือเวิร์กโฟลว์การแปลงที่สมบูรณ์ ส่วนต่อไปนี้จะแยกแต่ละขั้นตอนเพื่อให้คุณคัดลอก‑วางโค้ดส่วนนั้นลงในโปรเจกต์และรันได้ทันที

### ขั้นตอนที่ 1: โหลดไฟล์ IFC
แรกสุด, ระบุตำแหน่งโฟลเดอร์ที่ไฟล์ IFC ของคุณอยู่และโหลดด้วย `CadImage.load`.  
`CadImage.load` อ่านไฟล์ CAD และคืนค่าเป็นอ็อบเจกต์ภาพที่สามารถเรสเตอร์ไลซ์ได้.

```java
String dataDir = "Your Document Directory" + "ExportingIFC/";
String fileName = dataDir + "example.ifc";
IfcImage cadImage = (IfcImage)Image.load(fileName);
```

> **ทำไมเรื่องนี้สำคัญ:** การโหลดไฟล์เป็น `CadImage` ทำให้คุณเข้าถึงตัวเลือกการแปลงเวกเตอร์‑แรสเตอร์ที่ควบคุมความละเอียด, สีพื้นหลัง, และความหนาของเส้น.

### ขั้นตอนที่ 2: ตั้งค่าตัวเลือกการเรสเตอร์ไลซ์
กำหนดขนาดผลลัพธ์และการตั้งค่าอื่น ๆ ที่เกี่ยวกับเวกเตอร์ผ่าน `VectorRasterizationOptions`.  
`VectorRasterizationOptions` ให้คุณระบุขนาดผลลัพธ์, สีพื้นหลัง, และพารามิเตอร์การเรสเตอร์ไลซ์อื่น ๆ.

```java
CadRasterizationOptions vectorOptions = new CadRasterizationOptions();
vectorOptions.setPageWidth(1500);
vectorOptions.setPageHeight(1500);
```

> ปรับ `PageWidth` และ `PageHeight` เพื่อควบคุมความละเอียด PNG สุดท้าย ซึ่งสำคัญเมื่อคุณ **save PNG java** ไฟล์สำหรับการพิมพ์คุณภาพสูงหรือภาพย่อบนเว็บ.

### ขั้นตอนที่ 3: กำหนดค่า PNG options
เชื่อมตัวเลือกการเรสเตอร์ไลซ์กับตัวส่งออก PNG โดยสร้างอินสแตนซ์ของ `PngOptions`.

```java
PngOptions pngOptions = new PngOptions();
pngOptions.setVectorRasterizationOptions(vectorOptions);
```

### ขั้นตอนที่ 4: บันทึกภาพเป็น PNG
สุดท้าย, เขียนภาพที่เรสเตอร์ไลซ์ลงดิสก์โดยใช้เมธอด `save`.  
`save` จะเขียนภาพที่เรสเตอร์ไลซ์ไปยังเส้นทางไฟล์ที่ระบุในรูปแบบที่เลือก.

```java
String outPath = dataDir + "example.png";
cadImage.save(outPath, pngOptions);
```

> หลังจากขั้นตอนนี้คุณได้ **create PNG thumbnail IFC** สำเร็จและสามารถใช้ `example.png` ที่ได้ในที่ใดก็ได้ที่คุณต้องการภาพแรสเตอร์.

## กรณีการใช้งานทั่วไป
- **Generating thumbnails** สำหรับโมเดล BIM ในพอร์ทัลเว็บ.  
- **Embedding floor‑plan snapshots** ลงในรายงาน PDF หรือ Word.  
- **Automated batch conversion** ของไลบรารี IFC ขนาดใหญ่สำหรับโครงการจัดเก็บหรือย้ายข้อมูล.

## การแก้ไขปัญหาและเคล็ดลับ
- **Memory issues:** สำหรับไฟล์ IFC ขนาดใหญ่มาก, เพิ่มขนาด heap ของ JVM (`-Xmx2g` หรือสูงกว่า).  
- **Missing textures:** ตรวจสอบให้แน่ใจว่าแหล่งข้อมูลภายนอกของไฟล์ IFC สามารถเข้าถึงได้จาก `dataDir`.  
- **Pro tip:** ใช้ `vectorOptions.setBackgroundColor(Color.getWhite())` หากคุณต้องการพื้นหลังสีขาวแทน PNG โปร่งใสเริ่มต้น.

## คำถามที่พบบ่อย

### Q1: Aspose.CAD รองรับเวอร์ชันของไฟล์ IFC ทั้งหมดหรือไม่?
A1: Aspose.CAD รองรับเวอร์ชันต่าง ๆ ของ IFC. ดูที่ [documentation](https://reference.aspose.com/cad/java/) สำหรับข้อมูลความเข้ากันได้โดยละเอียด.

### Q2: ฉันสามารถปรับแต่งตัวเลือกการเรสเตอร์ไลซ์เพิ่มเติมได้หรือไม่?
A2: แน่นอน! สำรวจ [documentation](https://reference.aspose.com/cad/java/) สำหรับการตั้งค่าขั้นสูง เช่น การควบคุม DPI, การป้องกันการแทะรอย, และความหนาของเส้น.

### Q3: มีเวอร์ชันทดลองหรือไม่?
A3: ใช่, คุณสามารถดาวน์โหลดเวอร์ชันทดลองฟรีจาก [Aspose.CAD free trial](https://releases.aspose.com/).

### Q4: ฉันจะขอรับใบอนุญาตชั่วคราวสำหรับการทดสอบได้อย่างไร?
A4: รับใบอนุญาตชั่วคราวจาก [Aspose.CAD temporary license page](https://purchase.aspose.com/temporary-license/).

### Q5: ฉันสามารถถามคำถามหรือรายงานปัญหาได้ที่ไหน?
A5: เข้าร่วมชุมชนที่ [Aspose.CAD forum](https://forum.aspose.com/c/cad/19) เพื่อรับการสนับสนุนจากวิศวกรของ Aspose และนักพัฒนาคนอื่น ๆ.

## คำถามที่พบบ่อย

**Q: ฉันสามารถใช้วิธีนี้แปลงรูปแบบ CAD อื่นเป็น PNG ได้หรือไม่?**  
A: ใช่, Aspose.CAD รองรับหลายรูปแบบ (DWG, DXF, DGN, ฯลฯ). เพียงเปลี่ยนส่วนขยายไฟล์และโหลดคลาสภาพที่เหมาะสม.

**Q: ไลบรารีนี้ให้ฉันตั้งค่า DPI ที่กำหนดเองได้หรือไม่?**  
A: DPI ถูกควบคุมโดยอ้อมผ่าน `PageWidth`/`PageHeight`. ปรับค่าต่าง ๆ ตามขนาดทางกายภาพที่ต้องการเพื่อให้ได้ DPI ที่ต้องการ.

**Q: ผลลัพธ์ PNG เป็นแบบ loss‑less หรือไม่?**  
A: PNG เป็นรูปแบบ lossless, ดังนั้นภาพที่เรสเตอร์ไลซ์จะรักษาความละเอียดภาพเต็มของข้อมูลเวกเตอร์ต้นฉบับ.

## สรุป

ตอนนี้คุณมีวิธีที่ครบถ้วนและพร้อมใช้งานในระดับการผลิตเพื่อ **create PNG thumbnail IFC** ด้วย Aspose.CAD สำหรับ Java. ผสานขั้นตอนเหล่านี้เข้ากับเครื่องมือเดสก์ท็อป, เซอร์วิสด้านเซิร์ฟเวอร์, หรือฟังก์ชันคลาวด์เพื่ออัตโนมัติพายป์ไลน์การแสดงผล BIM และส่งมอบภาพย่อที่เร็วและคุณภาพสูงให้กับผู้ใช้.

---

**อัปเดตล่าสุด:** 2026-10-19  
**ทดสอบด้วย:** Aspose.CAD for Java 24.11  
**ผู้เขียน:** Aspose

## บทเรียนที่เกี่ยวข้อง

- [วิธีแปลง STL เป็น PNG ด้วย Aspose.CAD สำหรับ Java](/cad/java/cad-export-options/export-stl-to-png/)
- [แปลง DWG เป็น PNG – บันทึก CAD เป็น PNG ด้วย Aspose.CAD สำหรับ Java](/cad/java/cad-drawing-conversion/convert-cad-drawing-to-raster-image/)
- [ส่งออก DWG เป็น PDF ใน Java – ตั้งขนาดหน้า PDF ด้วย Aspose.CAD](/cad/java/cad-export-options/export-to-pdf/)


{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}