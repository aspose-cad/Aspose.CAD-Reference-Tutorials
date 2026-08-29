---
date: 2026-06-19
description: เรียนรู้วิธีตั้งค่า timeout บนการบันทึกภาพวาด CAD ด้วย Aspose.CAD สำหรับ
  Java. เพิ่มประสิทธิภาพ, ป้องกันการค้าง, และส่งออก CAD ไปเป็น PDF อย่างมีประสิทธิภาพ.
keywords:
- how to set timeout
- convert dwg to pdf
- export cad to pdf
linktitle: ตั้ง Timeout บนการบันทึก
schemas:
- author: Aspose
  dateModified: '2026-06-19'
  description: Learn how to set timeout on saving CAD drawings with Aspose.CAD for
    Java. Boost performance, avoid hangs, and export CAD to PDF efficiently.
  headline: How to Set Timeout on Save for CAD with Aspose.CAD
  type: TechArticle
- description: Learn how to set timeout on saving CAD drawings with Aspose.CAD for
    Java. Boost performance, avoid hangs, and export CAD to PDF efficiently.
  name: How to Set Timeout on Save for CAD with Aspose.CAD
  steps:
  - name: Set Source and Output Directories
    text: Ensure you have the correct source and output directories for your CAD drawings.
  - name: Create Interruption Token Source
    text: Initialize an interruption token source to manage interruptions during the
      save operation.
  - name: Load CAD Drawing
    text: The `CadImage` class is Aspose.CAD's core object that represents a CAD drawing
      in memory, offering methods for rendering and conversion.
  - name: Configure Rasterization Options
    text: '`CadRasterizationOptions` specifies how the CAD drawing is rasterized into
      an image. Configure rasterization options for the CAD drawing.'
  - name: Configure PDF Options
    text: '`PdfOptions` defines settings for saving a CAD drawing as a PDF document.
      Set up PDF options with vector rasterization options and the interruption token.'
  - name: Save Drawing with Timeout
    text: Save the CAD drawing to a PDF file with the specified timeout.
  - name: Handle Interruption
    text: '`OperationCanceledException` is thrown when a save operation exceeds the
      specified timeout. Create a thread to handle the save operation and interrupt
      it after a specified timeout.'
  type: HowTo
- questions:
  - answer: Yes, wrap each conversion in its own thread with a separate interruption
      token to enforce per‑file time limits.
    question: Can I use this feature to convert DWG to PDF in a batch job?
  - answer: The timeout mechanism is tied to the `InterruptionTokenSource` and works
      with any format that respects the token, including PDF, PNG, and SVG.
    question: Does the timeout work on all output formats?
  - answer: Aspose.CAD automatically discards incomplete output, so you won’t end
      up with corrupted PDFs.
    question: What happens to partially written files after a timeout?
  - answer: Yes, a valid Aspose.CAD license is required for commercial deployments;
      a free trial is available for evaluation.
    question: Is a license required for production use?
  - answer: The official Aspose.CAD documentation provides additional code snippets
      and best‑practice guidelines.
    question: Where can I find more examples of using interruption tokens?
  type: FAQPage
second_title: Aspose.CAD Java API
title: วิธีตั้งค่า Timeout บนการบันทึกสำหรับ CAD ด้วย Aspose.CAD
url: /th/java/other-cad-operations/put-timeout-on-save/
weight: 15
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# วิธีตั้งค่า Timeout บนการบันทึกสำหรับ CAD ด้วย Aspose.CAD

## บทนำ

ในคู่มือฉบับครอบคลุมนี้ คุณจะได้เรียนรู้ **วิธีตั้งค่า timeout** เมื่อบันทึกภาพวาด CAD ด้วย Aspose.CAD for Java การใช้ timeout จะป้องกันการทำงานบันทึกที่ใช้เวลานานทำให้แอปพลิเคชันของคุณค้าง ซึ่งสำคัญอย่างยิ่งเมื่อคุณต้อง **ส่งออก CAD เป็น PDF** หรือ **แปลง DWG เป็น PDF** ในสถานการณ์การประมวลผลแบบแบช Aspose.CAD for Java รองรับรูปแบบ CAD มากกว่า 50 รูปแบบและสามารถจัดการไฟล์หลายร้อยหน้าโดยไม่ต้องโหลดเอกสารทั้งหมดเข้าสู่หน่วยความจำ ทำให้คุณได้ประสิทธิภาพและการใช้ทรัพยากรที่คาดการณ์ได้

## คำตอบสั้น
- **ฟังก์ชันของ timeout คืออะไร?** มันยกเลิกการดำเนินการบันทึกหลังจากช่วงเวลาที่กำหนด ปล่อยเธรดและป้องกันการรั่วของทรัพยากร.  
- **คลาสใดควบคุม timeout?** `InterruptionTokenSource` ให้ token การยกเลิกที่ใช้โดยขั้นตอนการบันทึก.  
- **ฉันยังสามารถส่งออก CAD เป็น PDF หลังจาก timeout ได้หรือไม่?** ได้ – คุณสามารถดักจับข้อยกเว้นการขัดจังหวะและลองใหม่หรือบันทึกความล้มเหลว.  
- **ต้องการใบอนุญาตพิเศษหรือไม่?** ใบอนุญาต Aspose.CAD ปกติเพียงพอ; ฟีเจอร์ timeout มีอยู่ในตัวแล้ว.  
- **วิธีนี้ปลอดภัยต่อเธรดหรือไม่?** ใช่, เมื่อการบันทึกแต่ละรายการทำงานในเธรดของตนเองพร้อม token ของตนเอง.

## timeout คืออะไรในการดำเนินการบันทึก CAD?
Timeout คือขีดจำกัดเวลาที่กำหนดได้ ซึ่งเมื่อเกินจะบังคับให้กระบวนการบันทึกหยุดและสร้างข้อยกเว้นการขัดจังหวะ สิ่งนี้ปกป้องแอปพลิเคชัน Java ของคุณจากการค้างไม่สิ้นสุดที่เกิดจากภาพวาดที่ซับซ้อนหรือคอขวด I/O.

## ทำไมต้องตั้ง timeout เมื่อบันทึกไฟล์ CAD?
Aspose.CAD สามารถ **แปลง DWG เป็น PDF** และ **ส่งออก CAD เป็น PDF** ได้ภายในไม่กี่วินาทีสำหรับภาพวาดทั่วไป แต่ไฟล์ที่ใหญ่มากหรือเสียหายอาจใช้เวลาหลายนาที โดยการกำหนด timeout คุณจะรับประกันว่าการบันทึกใด ๆ จะไม่เกินเช่น 30 วินาที ทำให้การประมวลผลแบบแบชโดยรวมคงที่และป้องกันการขาดแคลนเธรด.

## ข้อกำหนดเบื้องต้น

Before diving into the tutorial, make sure you have the following prerequisites in place:
- **Aspose.CAD for Java Library** – ตรวจสอบว่าคุณได้รวมไลบรารี Aspose.CAD for Java เข้ากับโปรเจกต์ของคุณแล้ว คุณสามารถดาวน์โหลดไลบรารีจาก [website](https://releases.aspose.com/cad/java/).
- **Development Environment** – ตั้งค่าสภาพแวดล้อมการพัฒนา Java ของคุณพร้อมเครื่องมือและการพึ่งพาที่จำเป็นทั้งหมด.

## นำเข้าแพ็กเกจ

เพื่อเริ่มต้น ให้นำเข้าแพ็กเกจที่จำเป็นเข้าสู่โปรเจกต์ Java ของคุณ เพิ่มบรรทัดต่อไปนี้ที่ส่วนต้นของไฟล์ Java ของคุณ:

```java
import com.aspose.cad.Image;
import com.aspose.cad.InterruptionTokenSource;
import com.aspose.cad.fileformats.cad.CadImage;
import com.aspose.cad.imageoptions.CadRasterizationOptions;
import com.aspose.cad.imageoptions.PdfOptions;
import java.util.concurrent.TimeUnit;
```

ต่อไปนี้ เราจะวิเคราะห์โค้ดตัวอย่างเป็นขั้นตอนต่อขั้นตอน:

## วิธีตั้ง timeout บนการบันทึกสำหรับภาพวาด CAD?

โหลดไฟล์ CAD ของคุณ สร้าง `InterruptionTokenSource` พร้อม timeout ที่ต้องการ และส่ง token ไปยังตัวเลือกการบันทึก PDF หากการดำเนินการเกิน timeout Aspose.CAD จะโยน `OperationCanceledException` ซึ่งคุณสามารถดักจับเพื่อจัดการความล้มเหลวอย่างราบรื่น.

### ขั้นตอนที่ 1: ตั้งค่าไดเรกทอรีต้นทางและปลายทาง

```java
final String SourceDir = Utils.getDataDir_DWGDrawings();
final String OutputDir = Utils.getDataDir_Output();
```

ตรวจสอบว่าคุณมีไดเรกทอรีต้นทางและปลายทางที่ถูกต้องสำหรับภาพวาด CAD ของคุณ.

### ขั้นตอนที่ 2: สร้าง Interruption Token Source

```java
final InterruptionTokenSource source = new com.aspose.cad.InterruptionTokenSource();
```

เริ่มต้นแหล่ง token การขัดจังหวะเพื่อจัดการการขัดจังหวะระหว่างการบันทึก.

### ขั้นตอนที่ 3: โหลดภาพวาด CAD

คลาส `CadImage` เป็นอ็อบเจ็กต์หลักของ Aspose.CAD ที่แสดงภาพวาด CAD ในหน่วยความจำ พร้อมเมธอดสำหรับการเรนเดอร์และการแปลง.

```java
final CadImage cadImageBig = (CadImage)Image.load(SourceDir + "Drawing11.dwg");
```

### ขั้นตอนที่ 4: กำหนดค่าตัวเลือกการเรสเตอร์ไลซ์

`CadRasterizationOptions` ระบุวิธีการที่ภาพวาด CAD จะถูกเรสเตอร์ไลซ์เป็นภาพ.

```java
CadRasterizationOptions rasterizationOptionsBig = new CadRasterizationOptions();
rasterizationOptionsBig.setPageWidth(cadImageBig.getSize().getWidth() / 2);
rasterizationOptionsBig.setPageHeight(cadImageBig.getSize().getHeight() / 2);
```

กำหนดค่าตัวเลือกการเรสเตอร์ไลซ์สำหรับภาพวาด CAD.

### ขั้นตอนที่ 5: กำหนดค่าตัวเลือก PDF

`PdfOptions` กำหนดการตั้งค่าสำหรับการบันทึกภาพวาด CAD เป็นเอกสาร PDF.

```java
final PdfOptions CADfBig = new PdfOptions();
CADfBig.setVectorRasterizationOptions(rasterizationOptionsBig);
CADfBig.setInterruptionToken(source.getToken());
```

ตั้งค่าตัวเลือก PDF พร้อมตัวเลือกการเรสเตอร์ไลซ์แบบเวกเตอร์และ token การขัดจังหวะ.

### ขั้นตอนที่ 6: บันทึกภาพวาดพร้อม Timeout

```java
cadImageBig.save(OutputDir + "PutTimeoutOnSave_out.pdf", CADfBig);
```

บันทึกภาพวาด CAD ไปยังไฟล์ PDF ด้วย timeout ที่กำหนด.

### ขั้นตอนที่ 7: จัดการการขัดจังหวะ

`OperationCanceledException` จะถูกโยนเมื่อการบันทึกเกิน timeout ที่กำหนด.

```java
java.lang.Thread thread = new java.lang.Thread(new Runnable() {
    @Override
    public void run() {
        try {
            cadImageBig.save(OutputDir + "PutTimeoutOnSave_out.pdf", CADfBig);
        } catch (Throwable th) {
            System.out.println("interrupted !!!");
        }
    }
});
thread.start();
TimeUnit.SECONDS.sleep(3);
source.interrupt();
thread.join();
```

สร้างเธรดเพื่อจัดการการบันทึกและทำการขัดจังหวะหลังจาก timeout ที่กำหนด.

## ปัญหาทั่วไปและวิธีแก้

- **Timeout สั้นเกินไป** – หากคุณได้รับการขัดจังหวะบ่อยครั้ง ให้เพิ่มค่าของ timeout เพื่อรองรับภาพวาดที่ใหญ่ขึ้น.  
- **InterruptedException ไม่ได้ถูกดักจับ** – ควรห่อการเรียกบันทึกด้วยบล็อก try‑catch สำหรับ `OperationCanceledException` เสมอเพื่อป้องกันแอปพลิเคชันจากการพัง.  
- **การใช้หน่วยความจำ** – ใช้ `PdfOptions.setVectorRasterizationOptions` เพื่อสตรีมผลลัพธ์แทนการโหลดไฟล์ทั้งหมดเข้าสู่หน่วยความจำ.

## คำถามที่พบบ่อย

**Q: ฉันสามารถใช้ฟีเจอร์นี้เพื่อแปลง DWG เป็น PDF ในงานแบชได้หรือไม่?**  
A: ใช่, ห่อการแปลงแต่ละรายการในเธรดของตนเองพร้อม token การขัดจังหวะแยกต่างหากเพื่อบังคับใช้ขีดจำกัดเวลาต่อไฟล์.

**Q: timeout ทำงานกับรูปแบบเอาต์พุตทั้งหมดหรือไม่?**  
A: กลไก timeout เชื่อมโยงกับ `InterruptionTokenSource` และทำงานกับรูปแบบใดก็ได้ที่เคารพ token รวมถึง PDF, PNG, และ SVG.

**Q: จะเกิดอะไรขึ้นกับไฟล์ที่เขียนบางส่วนหลังจาก timeout?**  
A: Aspose.CAD จะลบผลลัพธ์ที่ไม่สมบูรณ์โดยอัตโนมัติ ดังนั้นคุณจะไม่พบ PDF ที่เสียหาย.

**Q: จำเป็นต้องมีใบอนุญาตสำหรับการใช้งานในผลิตภัณฑ์หรือไม่?**  
A: ใช่, จำเป็นต้องมีใบอนุญาต Aspose.CAD ที่ถูกต้องสำหรับการใช้งานเชิงพาณิชย์; มีเวอร์ชันทดลองฟรีสำหรับการประเมิน.

**Q: ฉันจะหา ตัวอย่างเพิ่มเติมของการใช้ interruption token ได้จากที่ไหน?**  
A: เอกสารอย่างเป็นทางการของ Aspose.CAD มีโค้ดสแนปเพิ่มเติมและแนวทางปฏิบัติที่ดีที่สุด.

## แหล่งข้อมูลเพิ่มเติม

- [หน้าปล่อย](https://releases.aspose.com/cad/java/) – หน้าดาวน์โหลดโดยตรงสำหรับการปล่อย Aspose.CAD for Java ล่าสุด.  
- [เอกสาร](https://reference.aspose.com/cad/java/) – การอ้างอิง API อย่างเต็มรูปแบบและคู่มือสำหรับนักพัฒนา.  
- [ลิงก์นี้](https://releases.aspose.com/) – การปล่อยผลิตภัณฑ์ Aspose ทั่วไป.  
- [ที่นี่](https://purchase.aspose.com/temporary-license/) – รับใบอนุญาตชั่วคราวสำหรับการทดสอบ.  
- [ฟอรั่ม Aspose.CAD](https://forum.aspose.com/c/cad/19) – การสนับสนุนและการสนทนาชุมชน.

## สรุป

คุณได้เชี่ยวชาญ **วิธีตั้งค่า timeout** สำหรับการบันทึกภาพวาด CAD ด้วย Aspose.CAD for Java แล้ว โดยการผสาน `InterruptionTokenSource` เข้าในกระบวนการทำงานของคุณ คุณสามารถ **ส่งออก CAD เป็น PDF** หรือ **แปลง DWG เป็น PDF** อย่างเชื่อถือได้โดยไม่เสี่ยงต่อการค้างที่ใช้เวลานาน ทำให้แอปพลิเคชันของคุณตอบสนองและขยายขนาดได้.

---

**อัปเดตล่าสุด:** 2026-06-19  
**ทดสอบด้วย:** Aspose.CAD for Java 24.12  
**ผู้เขียน:** Aspose  

{{< blocks/products/products-backtop-button >}}

## บทแนะนำที่เกี่ยวข้อง

- [ส่งออก DWG เป็น PDF หรือ Raster ด้วย Aspose.CAD for Java](/cad/java/cad-drawing-conversion/export-dwg-to-pdf-or-raster/)
- [ส่งออก Layout DWG เฉพาะเป็น PDF ด้วย Aspose.CAD for Java](/cad/java/cad-drawing-conversion/export-specific-dwg-layout-to-pdf/)
- [แปลง DWG เป็น PNG และรูปแบบ Raster อื่น ๆ ด้วย Aspose.CAD for Java](/cad/java/cad-drawing-conversion/convert-cad-layout-to-raster-image/)


{{< /blocks/products/pf/tutorial-page-section >}}
{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}