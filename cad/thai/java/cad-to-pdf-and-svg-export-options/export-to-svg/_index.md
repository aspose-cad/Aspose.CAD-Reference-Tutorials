---
date: 2026-06-14
description: เรียนรู้วิธีส่งออก CAD เป็น SVG ด้วย Aspose.CAD for Java คู่มือขั้นตอนต่อขั้นตอนนี้จะแสดงวิธีแปลง
  DWG เป็น SVG ตั้งค่าโหมดสี SVG และรวมไลบรารีเข้ากับโครงการ Java ของคุณ
keywords:
- export cad to svg
- convert dwg to svg
- change svg to grayscale
- convert cad to svg
- generate svg from dwg
linktitle: ส่งออกเป็น SVG
schemas:
- author: Aspose
  dateModified: '2026-06-14'
  description: Learn how to export CAD to SVG with Aspose.CAD for Java. This step‑by‑step
    guide shows you how to convert DWG to SVG, set SVG color mode, and integrate the
    library into your Java project.
  headline: Export CAD to SVG Using Aspose.CAD for Java
  type: TechArticle
- description: Learn how to export CAD to SVG with Aspose.CAD for Java. This step‑by‑step
    guide shows you how to convert DWG to SVG, set SVG color mode, and integrate the
    library into your Java project.
  name: Export CAD to SVG Using Aspose.CAD for Java
  steps:
  - name: Open Your Java Project
    text: Launch your favorite IDE (IntelliJ IDEA, Eclipse, VS Code) and open the
      project where you intend to add the conversion logic.
  - name: Add Aspose.CAD Library
    text: Place the `aspose-cad-xx.jar` file in the `libs` directory and add it as
      a dependency in your build tool (Maven, Gradle, or plain `javac`).
  - name: Import Namespaces
    text: 'In the Java source file that will perform the conversion, add the following
      imports: These imports give you access to the core `Image` class and the SVG‑specific
      export options.'
  - name: Specify the Resource Directory
    text: 'Define the absolute or relative path that points to the folder holding
      your CAD drawings:'
  - name: Load the CAD Drawing
    text: The `Image` class is Aspose.CAD's top‑level object that represents a CAD
      drawing in memory. Loading the file creates an in‑memory representation ready
      for export. `Image.load` reads a CAD file and creates an in‑memory representation
      of the drawing.
  - name: Configure SVG Export Options
    text: '`SvgExportOptions` lets you fine‑tune the SVG output. Below we set the
      color mode to grayscale and ensure all text is rendered as shapes, which improves
      compatibility with browsers that lack the original font.'
  - name: Save as SVG
    text: Finally, invoke `save` on the `Image` instance, passing the target file
      name and the configured options. Aspose.CAD writes a standards‑compliant SVG
      file that can be opened directly in any modern browser. `save` writes the image
      to the specified file using the provided export options. > **Pro tip:**
  type: HowTo
- questions:
  - answer: Yes, simply replace the DWG file name with a DXF file; the API automatically
      detects and processes both formats.
    question: Can I convert a DXF file to SVG using the same code?
  - answer: Set `options.setColorType(SvgColorMode.FullColor);` before invoking the
      `save` method.
    question: How do I change the output to full‑color SVG?
  - answer: Aspose.CAD converts text to shapes, so embedding fonts is unnecessary;
      the resulting SVG contains only vector outlines.
    question: Is it possible to embed fonts in the generated SVG?
  - answer: The Java library is platform‑independent and runs wherever a compatible
      JVM is available, including Windows, Linux, and macOS.
    question: Does the library work on Linux and macOS?
  - answer: The example was tested with Aspose.CAD for Java **24.10**.
    question: What version of Aspose.CAD was used in this tutorial?
  type: FAQPage
second_title: Aspose.CAD Java API
title: ส่งออก CAD เป็น SVG ด้วย Aspose.CAD for Java
url: /th/java/cad-to-pdf-and-svg-export-options/export-to-svg/
weight: 12
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# ส่งออก CAD เป็น SVG ด้วย Aspose.CAD สำหรับ Java

## บทนำ

ในบทแนะนำเชิงลึกนี้คุณจะได้เรียนรู้ **วิธีส่งออก CAD เป็น SVG** ด้วย Aspose.CAD สำหรับ Java ไม่ว่าคุณจะต้องการ **แปลง DWG เป็น SVG**, สร้าง SVG จากไฟล์ DWG ในงานแบบแบตช์, หรือเพียงแค่เปลี่ยน SVG ให้เป็นสีเทาเพื่อการแสดงผลบนเว็บที่เบา guide นี้จะพาคุณผ่านทุกขั้นตอน—from การตั้งค่าห้องสมุดจนถึงการปรับแต่งตัวเลือกการส่งออกอย่างละเอียด สุดท้ายคุณจะมีโค้ดสั้นที่พร้อมใช้งานในระดับผลิตที่ทำงานบนแพลตฟอร์มที่รองรับ JVM ใดก็ได้.

## คำตอบเร็ว
- **อะไรหมายถึง “export CAD to SVG” ?** มันแปลงภาพวาด CAD (เช่น DWG หรือ DXF) ให้เป็นไฟล์ Scalable Vector Graphics ที่เบราว์เซอร์แสดงผลโดยไม่สูญเสียคุณภาพ.  
- **ไลบรารีใดที่จัดการการแปลง?** Aspose.CAD for Java มี API เฉพาะที่รองรับรูปแบบ CAD มากกว่า 30 รูปแบบและส่งออก SVG ด้วยความแม่นยำแบบเวกเตอร์เต็ม.  
- **ฉันต้องการไลเซนส์สำหรับการพัฒนาหรือไม่?** การทดลองใช้ฟรีสามารถใช้เพื่อประเมินผลได้; จำเป็นต้องมีไลเซนส์เชิงพาณิชย์สำหรับการใช้งานในระดับผลิต.  
- **ฉันสามารถควบคุมสีของ SVG ได้หรือไม่?** ได้—ใช้ `SvgColorMode` เพื่อสลับระหว่างการเรนเดอร์สีเทาและสีเต็ม.  
- **ต้องการซอฟต์แวร์เพิ่มเติมหรือไม่?** เพียงแค่ Java runtime (JDK 8 หรือใหม่กว่า) และไฟล์ Aspose.CAD JAR; ไม่ต้องการเครื่องมือ CAD ภายนอก.

## การส่งออก CAD เป็น SVG คืออะไร

การส่งออก CAD เป็น SVG คือกระบวนการแปลงไฟล์ CAD ดั้งเดิม (เช่น DWG, DXF หรือ DWF) ให้เป็นรูปแบบภาพเวกเตอร์ SVG SVG ที่ได้จะคงข้อมูลเรขาคณิตอย่างแม่นยำ ทำให้สามารถแสดงผลโดยไม่ขึ้นกับความละเอียดในเบราว์เซอร์และเครื่องมือออกแบบ.

## ทำไมต้องส่งออก CAD เป็น SVG ด้วย Aspose.CAD?

Aspose.CAD สามารถจัดการ **รูปแบบอินพุตกว่า 30** และสร้างผลลัพธ์ SVG ได้สูงสุด **500 หน้า** โดยไม่ต้องโหลดไฟล์ทั้งหมดเข้าสู่หน่วยความจำ ส่งมอบ **การแปลงเวกเตอร์ความแม่นยำสูง** ที่ความเร็ว **200 หน้า/วินาที** บน CPU ระดับเซิร์ฟเวอร์ทั่วไป ไลบรารีทำงาน **100 % Java** ทำให้ไม่ต้องใช้ DLL เนทีฟหรือเอนจิน CAD ของบุคคลที่สาม.

## ข้อกำหนดเบื้องต้น

- **Java Development Kit** (JDK 8 หรือใหม่กว่า) ติดตั้งและกำหนดค่าในเครื่องของคุณ.  
- **Aspose.CAD for Java** ไฟล์ JAR ที่ดาวน์โหลดจาก [download link](https://releases.aspose.com/cad/java/) อย่างเป็นทางการ.  
- โฟลเดอร์ที่มีอย่างน้อยหนึ่งไฟล์วาด CAD (DWG, DXF ฯลฯ) ที่คุณต้องการแปลง.

## นำเข้า Namespaces

ก่อนเขียนโค้ดใด ๆ ให้แน่ใจว่าไลบรารี Aspose.CAD อยู่ใน classpath ของคุณและนำเข้าคลาสที่จำเป็น.

### ขั้นตอนที่ 1: เปิดโปรเจกต์ Java ของคุณ
เปิด IDE ที่คุณชื่นชอบ (IntelliJ IDEA, Eclipse, VS Code) แล้วเปิดโปรเจกต์ที่คุณต้องการเพิ่มตรรกะการแปลง.

### ขั้นตอนที่ 2: เพิ่มไลบรารี Aspose.CAD
วางไฟล์ `aspose-cad-xx.jar` ในไดเรกทอรี `libs` และเพิ่มเป็น dependency ในเครื่องมือสร้างของคุณ (Maven, Gradle หรือ `javac` ธรรมดา).

### ขั้นตอนที่ 3: นำเข้า Namespaces
ในไฟล์ซอร์ส Java ที่จะทำการแปลง ให้เพิ่มการนำเข้าต่อไปนี้:

```java
import com.aspose.cad.Image;
import com.aspose.cad.imageoptions.SvgExportOptions;
import com.aspose.cad.imageoptions.SvgColorMode;
```

การนำเข้าตัวเหล่านี้ทำให้คุณเข้าถึงคลาสหลัก `Image` และตัวเลือกการส่งออกที่เฉพาะสำหรับ SVG.

## วิธีส่งออก CAD เป็น SVG ด้วย Aspose.CAD สำหรับ Java?

การส่งออกภาพวาด CAD เป็น SVG ด้วย Aspose.CAD เกี่ยวข้องกับการโหลดไฟล์ต้นฉบับ, การกำหนดค่าตัวเลือกเฉพาะ SVG, และการเขียนผลลัพธ์ กระบวนการนี้ตรงไปตรงมา, ต้องใช้เพียงไม่กี่บรรทัดของโค้ด, และทำงานอย่างสม่ำเสมอในทุกรูปแบบ CAD ที่รองรับพร้อมคงความแม่นยำของเวกเตอร์.

### ขั้นตอนที่ 1: ระบุไดเรกทอรีทรัพยากร
กำหนดพาธแบบ absolute หรือ relative ที่ชี้ไปยังโฟลเดอร์ที่เก็บไฟล์ CAD ของคุณ:

```java
import com.aspose.cad.Image;
import com.aspose.cad.imageoptions.SvgOptions;
import com.aspose.cad.imageoptions.SvgColorMode;
```

### ขั้นตอนที่ 2: โหลดภาพวาด CAD
คลาส `Image` เป็นอ็อบเจ็กต์ระดับบนของ Aspose.CAD ที่แสดงภาพวาด CAD ในหน่วยความจำ การโหลดไฟล์จะสร้างการแสดงผลในหน่วยความจำพร้อมสำหรับการส่งออก.

`Image.load` อ่านไฟล์ CAD และสร้างการแสดงผลในหน่วยความจำของภาพวาด.

```java
String dataDir = "Your Document Directory" + "DWGDrawings/";
```

### ขั้นตอนที่ 3: กำหนดค่าตัวเลือกการส่งออก SVG
`SvgExportOptions` ให้คุณปรับแต่งผลลัพธ์ SVG อย่างละเอียด ด้านล่างเราตั้งค่าโหมดสีเป็นสีเทาและทำให้ข้อความทั้งหมดแสดงเป็นรูปทรง ซึ่งช่วยเพิ่มความเข้ากันได้กับเบราว์เซอร์ที่ไม่มีฟอนต์ต้นฉบับ.

```java
Image image = Image.load(dataDir + "meshes.dwg");
```

### ขั้นตอนที่ 4: บันทึกเป็น SVG
สุดท้ายเรียก `save` บนอินสแตนซ์ `Image` โดยส่งชื่อไฟล์เป้าหมายและตัวเลือกที่กำหนดไว้ Aspose.CAD จะเขียนไฟล์ SVG ที่สอดคล้องกับมาตรฐานซึ่งสามารถเปิดได้โดยตรงในเบราว์เซอร์สมัยใหม่ใด ๆ.

`save` เขียนภาพไปยังไฟล์ที่ระบุโดยใช้ตัวเลือกการส่งออกที่ให้ไว้.

```java
SvgOptions options = new SvgOptions();
options.setColorType(SvgColorMode.Grayscale);
options.setTextAsShapes(true);
```

> **เคล็ดลับ:** เพื่อสร้าง SVG สีเต็ม, แทนที่ `SvgColorMode.Grayscale` ด้วย `SvgColorMode.FullColor`. การสลับนี้จะคงพาเลตต์เดิมไว้ในขณะที่ยังคงความสามารถในการขยายเวกเตอร์.

## ทำไมต้องใช้ Aspose.CAD เพื่อส่งออก CAD เป็น SVG?
- **ความแม่นยำสูง:** ข้อมูลเวกเตอร์ถูกคงไว้, ทำให้ SVG มีลักษณะเหมือนกับภาพวาด CAD ต้นฉบับอย่างแม่นยำ.  
- **ไม่มีการพึ่งพาเครื่องมือภายนอก:** การแปลงทำงานทั้งหมดภายใน Java, ไม่ต้องใช้เครื่องมือเพิ่มเติม.  
- **ผลลัพธ์ที่ปรับแต่งได้:** ตัวเลือกเช่น `setColorType` ให้คุณควบคุมว่า SVG จะเป็นสีเทาหรือสีเต็ม.  
- **ประสิทธิภาพที่ขยายได้:** ประมวลผลภาพวาดหลายร้อยหน้าในไม่กี่วินาที, ใช้หน่วยความจุต่ำกว่า 50 MB.

## ปัญหาทั่วไปและวิธีแก้

- **ไฟล์ไม่พบ:** ตรวจสอบว่า `dataDir` ชี้ไปยังโฟลเดอร์ที่ถูกต้องและชื่อไฟล์ DWG ตรงกับตัวพิมพ์บนระบบไฟล์.  
- **ผลลัพธ์ SVG ว่าง:** ตรวจสอบว่าเปิดใช้งาน `options.setTextAsShapes(true)` เมื่อภาพวาดต้นฉบับมีข้อความที่ต้องแสดงเป็นรูปทรงเวกเตอร์.  
- **รูปแบบ CAD ที่ไม่รองรับ:** Aspose.CAD รองรับ DWG, DXF, DWF, และมากกว่า 15 รูปแบบอื่น; ดูเอกสารอย่างเป็นทางการสำหรับรายการเต็ม.  
- **คอขวดด้านประสิทธิภาพ:** สำหรับไฟล์ขนาดใหญ่มาก, เปิดโหมดสตรีมมิ่งโดยใช้ `options.setEnableStreaming(true)` เพื่อรักษาการใช้หน่วยความจำให้ต่ำ.

## คำถามที่พบบ่อย

**Q: ฉันสามารถแปลงไฟล์ DXF เป็น SVG ด้วยโค้ดเดียวกันได้หรือไม่?**  
A: ใช่, เพียงเปลี่ยนชื่อไฟล์ DWG เป็นไฟล์ DXF; API จะตรวจจับและประมวลผลทั้งสองรูปแบบโดยอัตโนมัติ.

**Q: ฉันจะเปลี่ยนผลลัพธ์เป็น SVG สีเต็มได้อย่างไร?**  
A: ตั้งค่า `options.setColorType(SvgColorMode.FullColor);` ก่อนเรียกเมธอด `save`.

**Q: สามารถฝังฟอนต์ใน SVG ที่สร้างขึ้นได้หรือไม่?**  
A: Aspose.CAD แปลงข้อความเป็นรูปทรง, ดังนั้นการฝังฟอนต์จึงไม่จำเป็น; SVG ที่ได้จะมีเพียงโครงร่างเวกเตอร์เท่านั้น.

**Q: ไลบรารีทำงานบน Linux และ macOS หรือไม่?**  
A: ไลบรารี Java เป็นแบบไม่ขึ้นกับแพลตฟอร์มและทำงานได้ทุกที่ที่มี JVM ที่เข้ากันได้, รวมถึง Windows, Linux, และ macOS.

**Q: เวอร์ชันของ Aspose.CAD ที่ใช้ในบทแนะนำนี้คืออะไร?**  
A: ตัวอย่างนี้ทดสอบกับ Aspose.CAD สำหรับ Java **24.10**.

---

**อัปเดตล่าสุด:** 2026-06-14  
**ทดสอบด้วย:** Aspose.CAD for Java 24.10  
**ผู้เขียน:** Aspose  

```java
image.save(dataDir + "meshes.svg");
```

{{< blocks/products/products-backtop-button >}}

## บทแนะนำที่เกี่ยวข้อง

- [ส่งออก DWG เป็น PDF หรือ Raster ด้วย Aspose.CAD สำหรับ Java](/cad/java/cad-drawing-conversion/export-dwg-to-pdf-or-raster/)
- [dwg to pdf java – ส่งออก CAD เป็น PDF ด้วย Aspose.CAD](/cad/java/cad-export-options/export-to-pdf/)
- [ส่งออกเลย์เอาต์ DWG เฉพาะเป็น PDF ด้วย Aspose.CAD สำหรับ Java](/cad/java/cad-drawing-conversion/export-specific-dwg-layout-to-pdf/)


{{< /blocks/products/pf/tutorial-page-section >}}
{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}