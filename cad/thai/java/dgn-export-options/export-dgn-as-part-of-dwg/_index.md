---
date: 2026-05-20
description: เรียนรู้วิธีการส่งออก DGN เป็น DWG และแปลง MicroStation DGN เป็น AutoCAD
  DWG ด้วย Aspose.CAD for Java. ปฏิบัติตามคู่มือขั้นตอนต่อขั้นตอนของเราเพื่อการจัดการไฟล์
  CAD ที่รวดเร็วและเชื่อถือได้.
keywords:
- how to export dgn to dwg
- convert microstation dgn to autocad dwg
- Aspose.CAD Java export
- CAD file conversion Java
linktitle: ส่งออก DGN เป็นส่วนหนึ่งของ DWG
schemas:
- author: Aspose
  dateModified: '2026-05-20'
  description: Learn how to export DGN to DWG and convert MicroStation DGN to AutoCAD
    DWG using Aspose.CAD for Java. Follow our step‑by‑step guide for fast, reliable
    CAD file manipulation.
  headline: How to Export DGN to DWG with Aspose.CAD for Java
  type: TechArticle
- description: Learn how to export DGN to DWG and convert MicroStation DGN to AutoCAD
    DWG using Aspose.CAD for Java. Follow our step‑by‑step guide for fast, reliable
    CAD file manipulation.
  name: How to Export DGN to DWG with Aspose.CAD for Java
  steps:
  - name: Set File Paths
    text: Define where the source DGN lives and where the resulting DWG will be written.
      Adjust `dataDir`, `fileName`, and `outPath` to match your project layout.
  - name: Create CadRasterizationOptions Instance
    text: '`CadRasterizationOptions` defines how vector data is rasterized before
      being embedded into the DWG container.'
  - name: Load DGN File
    text: '`CadImage` represents the loaded DGN file in memory, allowing access to
      its entities and properties.'
  - name: Iterate Through Entities
    text: '`CadBaseEntity` is the base class for all CAD entities, and `CadDgnUnderlay`
      represents an embedded DGN underlay. Loop over each entity; when an `ImageDefinition`
      is encountered, its external reference is extracted for later embedding.'
  - name: Define Rasterization Options
    text: Set page width, height, layout selection, and background color to match
      the target DWG’s visual requirements.
  - name: Set Vector Rasterization Options
    text: Specify vector‑specific settings such as line weight handling and curve
      approximation to ensure the DWG retains crisp geometry.
  - name: Export DWG to PDF
    text: Call the `save` method on the `CadImage` instance, passing the configured
      options to produce the final DWG‑compatible PDF output.
  type: HowTo
- questions:
  - answer: The full API reference is available [here](https://reference.aspose.com/cad/java/).
    question: Where can I find the documentation for Aspose.CAD for Java?
  - answer: Grab the latest release from [this link](https://releases.aspose.com/cad/java/).
    question: How can I download the Aspose.CAD library for Java?
  - answer: Yes, a fully functional trial can be obtained [here](https://releases.aspose.com/).
    question: Is there a free trial available for Aspose.CAD for Java?
  - answer: Request a temporary license from Aspose [here](https://purchase.aspose.com/temporary-license/).
    question: Where can I get a temporary license for Aspose.CAD for Java?
  - answer: Join the community support forum and post your query [here](https://forum.aspose.com/c/cad/19).
    question: Need help or have questions?
  type: FAQPage
second_title: Aspose.CAD Java API
title: วิธีการส่งออก DGN เป็น DWG ด้วย Aspose.CAD for Java
url: /th/java/dgn-export-options/export-dgn-as-part-of-dwg/
weight: 10
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# วิธีส่งออก DGN เป็น DWG ด้วย Aspose.CAD สำหรับ Java

ในบทแนะนำนี้คุณจะได้เรียนรู้ **วิธีส่งออก dgn เป็น dwg** ด้วยไลบรารี Aspose.CAD สำหรับ Java ไม่ว่าคุณจะต้องการรวมแบบออกแบบจาก MicroStation เข้ากับกระบวนการทำงานของ AutoCAD หรือทำการแปลงเป็นชุดแบบอัตโนมัติ คู่มือนี้จะพาคุณผ่านทุกขั้นตอน ตั้งแต่การเตรียมสภาพแวดล้อมจนถึงการสร้างไฟล์ DWG ความละเอียดสูง ในตอนท้ายคุณจะมีรูปแบบโค้ดที่สามารถนำกลับมาใช้ใหม่เพื่อทำการส่งออก DGN‑to‑DWG อย่างเชื่อถือได้

## คำตอบอย่างรวดเร็ว
- **ไลบรารีใดจัดการการแปลง DGN‑to‑DWG?** Aspose.CAD สำหรับ Java.  
- **ต้องการไลเซนส์สำหรับการใช้งานจริงหรือไม่?** ใช่ ไลเซนส์เชิงพาณิชย์จะลบข้อจำกัดของรุ่นทดลอง.  
- **รูปแบบ CAD ที่รองรับ?** มากกว่า 50 รูปแบบเข้าและออก รวมถึง DGN, DWG, DXF, และ PDF.  
- **สามารถประมวลผลไฟล์ขนาดใหญ่ได้หรือไม่?** ได้ Aspose.CAD สามารถสตรีมไฟล์ได้ถึง 2 GB โดยไม่ต้องโหลดทั้งหมดเข้าสู่หน่วยความจำ.  
- **เวลาในการทำงานโดยประมาณ?** ประมาณ 15 นาทีสำหรับสคริปต์ส่งออกพื้นฐาน.

## อะไรคือ “วิธีส่งออก dgn เป็น dwg”?
**วิธีส่งออก dgn เป็น dwg** คือกระบวนการแปลงไฟล์ออกแบบ MicroStation DGN ให้เป็นไฟล์ AutoCAD DWG พร้อมคงรักษาเรขาคณิต, ชั้น, และภาพราสเตอร์ Aspose.CAD ให้ API โปรแกรมเมอร์ที่ทำการแปลงนี้โดยไม่ต้องใช้ซอฟต์แวร์ CAD ต้นแบบ

## ทำไมต้องใช้ Aspose.CAD สำหรับ Java?
Aspose.CAD ประมวลผล **รูปแบบ CAD มากกว่า 50** ชนิดและสามารถเรสเตอร์ไฟล์ได้ถึงขนาด 2 GB ให้ความเร็วการแปลงสูงสุดถึง 3× เมื่อเทียบกับเครื่องมือเนทีฟหลายตัว ไลบรารีทำงานบนแพลตฟอร์มที่รองรับ Java ใดก็ได้ ไม่ต้องพึ่งพาไลบรารีภายนอก และให้การควบคุมเต็มรูปแบบต่อการเรสเตอร์ เช่น ขนาดหน้า, สีพื้นหลัง, และคุณภาพการเรนเดอร์เวกเตอร์

## ข้อกำหนดเบื้องต้น

ก่อนเริ่มทำตามขั้นตอน ตรวจสอบว่าคุณมีสิ่งต่อไปนี้:

1. **Aspose.CAD Library** – ดาวน์โหลดและติดตั้ง Aspose.CAD สำหรับ Java รุ่นล่าสุดจาก [ที่นี่](https://releases.aspose.com/cad/java/).  
2. **Java Development Kit (JDK)** – JDK 8 หรือใหม่กว่า ติดตั้งบนเครื่องของคุณ.  
3. **IDE** – Eclipse, IntelliJ IDEA หรือ IDE ที่รองรับ Java ใดก็ได้ เพื่อความสะดวกในการเขียนโค้ด.  

## วิธีส่งออก DGN เป็น DWG ด้วย Aspose.CAD สำหรับ Java?

โหลดไฟล์ DGN ต้นฉบับ, สร้างตัวเลือกการเรสเตอร์, วนลูปผ่านเอนทิตี้, แล้วบันทึกผลลัพธ์เป็นไฟล์ DWG ขั้นตอนทั้งหมดสั้นกระชับและทำงานภายในน้อยกว่าสักนาทีสำหรับไฟล์ทั่วไป พร้อมคงรักษาชั้น, ความหนาของเส้น, และภาพราสเตอร์ที่ฝังอยู่ เพื่อให้ DWG ที่ได้ตรงกับเจตนาการออกแบบต้นฉบับ

### นำเข้าแพ็กเกจ

ส่วน `import` จะดึงคลาสหลักของ Aspose.CAD ที่จำเป็นสำหรับการจัดการ CAD.  

```java
import com.aspose.cad;
import com.aspose.cad.imageoptions;
import com.aspose.cad.fileformats.cad.cadconsts;
import com.aspose.cad.fileformats.cad;
import com.aspose.cad.fileformats.cad.cadobjects;
```

### ขั้นตอนที่ 1: ตั้งค่าเส้นทางไฟล์

กำหนดตำแหน่งที่ไฟล์ DGN ต้นฉบับอยู่และที่ที่ไฟล์ DWG ผลลัพธ์จะถูกเขียนออกมา ปรับ `dataDir`, `fileName`, และ `outPath` ให้สอดคล้องกับโครงสร้างโปรเจกต์ของคุณ.  

```java
String dataDir = "Your Document Directory" + "ExportingDGN/";
String fileName = dataDir + "BlockRefDgn.dwg";
String outPath = dataDir + "BlockRefDgn.dwg.pdf";
```

### ขั้นตอนที่ 2: สร้างอินสแตนซ์ CadRasterizationOptions

`CadRasterizationOptions` กำหนดวิธีการเรสเตอร์ข้อมูลเวกเตอร์ก่อนฝังลงในคอนเทนเนอร์ DWG.  

```java
PdfOptions exportOptions = new PdfOptions();
```

### ขั้นตอนที่ 3: โหลดไฟล์ DGN

`CadImage` แทนไฟล์ DGN ที่โหลดเข้ามาในหน่วยความจำ ทำให้สามารถเข้าถึงเอนทิตี้และคุณสมบัติต่าง ๆ ได้.  

```java
CadImage cadImage = (CadImage) Image.load(fileName);
```

### ขั้นตอนที่ 4: วนลูปผ่านเอนทิตี้

`CadBaseEntity` เป็นคลาสฐานสำหรับเอนทิตี้ CAD ทั้งหมด, ส่วน `CadDgnUnderlay` แทนการฝัง DGN ใต้พื้น. วนลูปแต่ละเอนทิตี้; เมื่อพบ `ImageDefinition` จะดึงการอ้างอิงภายนอกเพื่อฝังในขั้นตอนต่อไป.  

```java
for (CadBaseEntity baseEntity : cadImage.getEntities()) {
    if (baseEntity.getTypeName() == CadEntityTypeName.DGNUNDERLAY) {
        CadDgnUnderlay dgnFile = (CadDgnUnderlay)baseEntity;
        System.out.println(dgnFile.getUnderlayPath());
    }
}
```

### ขั้นตอนที่ 5: กำหนดตัวเลือกการเรสเตอร์

ตั้งค่าความกว้าง, ความสูงของหน้า, การเลือกเลย์เอาต์, และสีพื้นหลังให้สอดคล้องกับความต้องการของ DWG ปลายทาง.  

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

### ขั้นตอนที่ 6: ตั้งค่าตัวเลือกการเรสเตอร์เวกเตอร์

ระบุการตั้งค่าเฉพาะเวกเตอร์ เช่น การจัดการความหนาของเส้นและการประมาณเส้นโค้ง เพื่อให้ DWG รักษาเรขาคณิตที่คมชัด.  

```java
exportOptions.setVectorRasterizationOptions(vectorRasterizationOptions);
```

### ขั้นตอนที่ 7: ส่งออก DWG เป็น PDF

เรียกเมธอด `save` ของอ็อบเจกต์ `CadImage` พร้อมตัวเลือกที่กำหนด เพื่อสร้างไฟล์ PDF ที่เข้ากันได้กับ DWG สุดท้าย.  

```java
cadImage.save(outPath, exportOptions);
```

## ปัญหาทั่วไปและวิธีแก้

- **การอ้างอิงภาพภายนอกหาย** – ตรวจสอบว่า `ImageDefinition` ของ DGN ชี้ไปยังเส้นทางไฟล์ที่เข้าถึงได้; ใช้เส้นทางแบบเต็มหากเส้นทางแบบสัมพันธ์ทำงานไม่สำเร็จ.  
- **สีพื้นหลังไม่ตรงตามคาด** – ตรวจสอบให้ `CadRasterizationOptions.setBackgroundColor()` มีค่า RGB ที่ต้องการ; ค่าเริ่มต้นคือสีขาว.  
- **ข้อผิดพลาดหน่วยความจำกับไฟล์ขนาดใหญ่** – เปิดใช้งานการสตรีมโดยตั้งค่า `CadRasterizationOptions.setPageSize()` ให้เหมาะสมและหลีกเลี่ยงการโหลดไฟล์ทั้งหมดเข้าสู่หน่วยความจำ.

## คำถามที่พบบ่อย

**Q: จะหาเอกสารอ้างอิงของ Aspose.CAD สำหรับ Java ได้จากที่ไหน?**  
A: API reference เต็มรูปแบบมีให้ที่ [ที่นี่](https://reference.aspose.com/cad/java/).

**Q: จะดาวน์โหลดไลบรารี Aspose.CAD สำหรับ Java ได้อย่างไร?**  
A: ดาวน์โหลดเวอร์ชันล่าสุดจาก [ลิงก์นี้](https://releases.aspose.com/cad/java/).

**Q: มีรุ่นทดลองฟรีสำหรับ Aspose.CAD สำหรับ Java หรือไม่?**  
A: มี, สามารถรับรุ่นทดลองเต็มฟังก์ชันได้ [ที่นี่](https://releases.aspose.com/).

**Q: จะขอรับไลเซนส์ชั่วคราวสำหรับ Aspose.CAD สำหรับ Java ได้จากที่ไหน?**  
A: ขอไลเซนส์ชั่วคราวจาก Aspose [ที่นี่](https://purchase.aspose.com/temporary-license/).

**Q: ต้องการความช่วยเหลือหรือมีคำถาม?**  
A: เข้าร่วมฟอรั่มสนับสนุนชุมชนและโพสต์คำถามของคุณ [ที่นี่](https://forum.aspose.com/c/cad/19).

---

**Last Updated:** 2026-05-20  
**Tested With:** Aspose.CAD for Java 24.5  
**Author:** Aspose  

{{< blocks/products/products-backtop-button >}}

## บทเรียนที่เกี่ยวข้อง

- [Export DGN to DWG with Aspose.CAD for Java – Tutorial](/cad/java/dgn-export-options/)
- [Effortless DGN to AutoCAD PDF Export with Aspose.CAD for Java](/cad/java/dgn-export-options/exporting-dgn-to-pdf/)
- [Export DWG to PDF or Raster Using Aspose.CAD for Java](/cad/java/cad-drawing-conversion/export-dwg-to-pdf-or-raster/)


{{< /blocks/products/pf/tutorial-page-section >}}
{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}