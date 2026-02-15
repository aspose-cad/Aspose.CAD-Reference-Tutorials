---
date: 2026-02-15
description: เรียนรู้วิธีตั้งขนาดหน้ากระดาษ PDF และแปลง CAD เป็น PDF ด้วย Aspose.CAD
  สำหรับ Java พร้อมการปรับสเกลเลย์เอาต์อัตโนมัติและการส่งออกเป็น TIFF.
linktitle: Set PDF Page Size – Convert CAD to PDF
second_title: Aspose.CAD Java API
title: ตั้งค่าขนาดหน้ากระดาษ PDF – แปลง CAD เป็น PDF (Java)
url: /th/java/advanced-cad-features/set-canvas-size-and-mode/
weight: 16
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# ตั้งขนาด Canvas และโหมด

## บทนำ

หากคุณต้องการ **ตั้งขนาดหน้า PDF** ขณะแปลงภาพวาด CAD เป็น PDF คุณมาถูกที่แล้ว ในบทเรียนนี้เราจะแสดงวิธีใช้ Aspose.CAD for Java เพื่อกำหนดขนาด canvas อย่างแม่นยำ เปิดใช้งานการปรับสเกลเลย์เอาต์อัตโนมัติ และส่งออกผลลัพธ์เป็นทั้ง PDF และ TIFF ไม่ว่าคุณจะเตรียมแผนผังวิศวกรรมสำหรับการพิมพ์หรือสร้างภาพย่อสำหรับแกลเลอรีเว็บ การควบคุมขนาดหน้าและความละเอียดของผลลัพธ์เป็นสิ่งสำคัญ

## คำตอบอย่างรวดเร็ว
- **What does “convert CAD to PDF” mean?** การแปลงภาพวาด CAD (เช่น DXF, DWG) เป็นเอกสาร PDF ที่สามารถดูได้บนทุกแพลตฟอร์ม  
- **Can I also export to TIFF?** ใช่—ใช้ `TiffOptions` เพื่อสร้างภาพเรสเตอร์ความละเอียดสูง  
- **Which option controls canvas size in Java?** `CadRasterizationOptions.setPageWidth/Height`  
- **What is automatic layout scaling?** ธง (`setAutomaticLayoutsScaling(true)`) ที่รักษาสัดส่วนของเลย์เอาต์เดิมเมื่อขนาด canvas เปลี่ยนแปลง  
- **Do I need a license for Aspose.CAD?** จำเป็นต้องมีใบอนุญาตชั่วคราวหรือถาวรสำหรับการใช้งานในสภาพการผลิต  

## วิธีตั้งขนาดหน้า PDF เมื่อแปลง CAD เป็น PDF (Java)

การตั้งขนาดหน้า PDF (หรือขนาด canvas) ช่วยให้คุณกำหนดมิติสุดท้ายของเอกสารได้ ซึ่งเป็นประโยชน์อย่างยิ่งเมื่อคุณต้อง **เปลี่ยนขนาด PDF** ให้ตรงกับมาตรฐานการพิมพ์หรือความต้องการของ UI ด้านล่างเราจะอธิบายขั้นตอนแต่ละขั้น พร้อมเหตุผลของแต่ละบรรทัดโค้ด

## อะไรคือ **convert CAD to PDF**?

การแปลง CAD เป็น PDF หมายถึงการนำภาพวาดวิศวกรรมแบบเวกเตอร์มารันเดอร์เป็นหน้า PDF โดยคงรักษาเส้น, ชั้น, และรูปทรงเรขาคณิตไว้ พร้อมทำให้ไฟล์สามารถเข้าถึงได้ทั่วทุกแพลตฟอร์ม

## ทำไมต้องตั้งขนาด canvas **java**?

การตั้งขนาด canvas ใน Java ช่วยให้คุณกำหนดความละเอียดของผลลัพธ์และมิติของหน้าได้ ทำให้ PDF หรือ TIFF ที่ได้ตรงตามข้อกำหนดการพิมพ์หรือการแสดงผลของคุณ อีกทั้งยังให้คุณควบคุมพฤติกรรมการสเกล ซึ่งสำคัญสำหรับภาพวาดขนาดใหญ่

## ข้อกำหนดเบื้องต้น

ก่อนเริ่มทำตามบทเรียน โปรดตรวจสอบว่าคุณมีสิ่งต่อไปนี้พร้อมใช้งานแล้ว:

- Aspose.CAD for Java: ตรวจสอบว่าคุณได้ติดตั้งไลบรารี Aspose.CAD ในสภาพแวดล้อม Java ของคุณแล้ว คุณสามารถดาวน์โหลดได้ [ที่นี่](https://releases.aspose.com/cad/java/)  
- Document Directory: ตั้งค่าโฟลเดอร์เอกสารเพื่อเก็บไฟล์ CAD ของคุณ โฟลเดอร์นี้จะถูกอ้างอิงในขั้นตอนของบทเรียน  

ตอนนี้เรามาเริ่มทำตามขั้นตอนทีละขั้นตอนกันเลย

## นำเข้า Namespaces

ในขั้นตอนนี้ เราจะนำเข้า namespaces ที่จำเป็นเพื่อเริ่มโครงการ Aspose.CAD ของคุณ

```java
import java.awt.Image;

import com.aspose.cad.fileformats.tiff.enums.TiffExpectedFormat;
import com.aspose.cad.imageoptions.CadRasterizationOptions;
import com.aspose.cad.imageoptions.PdfOptions;
import com.aspose.cad.imageoptions.TiffOptions;
```

## ขั้นตอนที่ 1: นำเข้าคลาส Aspose.CAD

```java
// The path to the resource directory.
String dataDir = "Your Document Directory" + "CADConversion/";

String srcFile = dataDir + "conic_pyramid.dxf";
com.aspose.cad.Image objImage = com.aspose.cad.Image.load(srcFile);
```

ในโค้ดสแนปนี้ เราตั้งค่าเส้นทางไปยังไดเรกทอรีทรัพยากรและโหลดไฟล์ DXF ด้วยคลาส `Image` ของ Aspose.CAD

## ขั้นตอนที่ 2: ตั้งค่าคุณสมบัติ **CadRasterizationOptions** (set canvas size java)

```java
// Create an instance of CadRasterizationOptions and set its various properties
CadRasterizationOptions rasterizationOptions = new CadRasterizationOptions();
rasterizationOptions.setPageWidth(1600);
rasterizationOptions.setPageHeight(1600);

rasterizationOptions.setAutomaticLayoutsScaling(true);
rasterizationOptions.setNoScaling(true);
```

ที่นี่ เราสร้างอินสแตนซ์ของ `CadRasterizationOptions` และกำหนดค่าต่าง ๆ เช่น ความกว้างของหน้า, ความสูงของหน้า, และ **automatic layout scaling** นี่คือหัวใจของ **configure canvas mode** สำหรับการแปลงของคุณ

## ขั้นตอนที่ 3: สร้าง PdfOptions และตั้งค่า VectorRasterizationOptions

```java
// Create an instance of PdfOptions
PdfOptions pdfOptions = new PdfOptions();

// Set the VectorRasterizationOptions property
pdfOptions.setVectorRasterizationOptions(rasterizationOptions);
```

ต่อไป เราสร้างอินสแตนซ์ของ `PdfOptions` และตั้งค่า property `VectorRasterizationOptions` ให้เป็น `CadRasterizationOptions` ที่กำหนดไว้ก่อนหน้า

## ขั้นตอนที่ 4: ส่งออกเป็น PDF (convert cad to pdf)

```java
// Export CAD to PDF
objImage.save(dataDir + "result_out_.pdf", pdfOptions);
```

สุดท้าย เราบันทึกภาพ CAD เป็นไฟล์ PDF โดยใช้ตัวเลือกที่ระบุไว้ ทำให้กระบวนการ **convert CAD to PDF** เสร็จสมบูรณ์

## ขั้นตอนที่ 5: สร้าง TiffOptions และตั้งค่า VectorRasterizationOptions (export cad to tiff)

```java
// Create an instance of TiffOptions
TiffOptions tiffOptions = new TiffOptions(TiffExpectedFormat.Default);

// Set the VectorRasterizationOptions property
tiffOptions.setVectorRasterizationOptions(rasterizationOptions);
```

ในขั้นตอนนี้ เราตั้งค่าอินสแตนซ์ของ `TiffOptions` และกำหนด property `VectorRasterizationOptions` ของมัน

## ขั้นตอนที่ 6: ส่งออกเป็น TIFF

```java
// Export CAD to TIFF
objImage.save(dataDir + "result_out_.tiff", tiffOptions);
```

สุดท้าย เราบันทึกภาพ CAD เป็นไฟล์ TIFF โดยใช้ตัวเลือกที่ระบุไว้ แสดงวิธี **export CAD to TIFF** หลังจากตั้งค่าขนาด canvas

## ปัญหาทั่วไปและวิธีแก้

| ปัญหา | สาเหตุ | วิธีแก้ |
|-------|-------|----------|
| PDF ที่ส่งออกเป็นไฟล์เปล่า | `setNoScaling(true)` ปิดการเรนเดอร์สำหรับบางภาพวาด | ลบ `setNoScaling(true)` หรือตั้งค่าเป็น `false` |
| ความละเอียดของ TIFF ดูต่ำ | ความกว้าง/ความสูงของหน้าเล็กเกินไป | เพิ่มค่าของ `setPageWidth` / `setPageHeight` |
| เลย์เอาต์ดูบิดเบี้ยว | การปรับสเกลเลย์เอาต์อัตโนมัติถูกปิด | ตรวจสอบให้แน่ใจว่าเปิดใช้งาน `setAutomaticLayoutsScaling(true)` |

## ทำไมต้องปรับขนาด Canvas และ DPI?

การปรับขนาด canvas มีผลโดยตรงต่อความละเอียดการเรสเตอร์ไลซ์ของผลลัพธ์ หากคุณต้องการ **เพิ่มความละเอียดของ TIFF** เพียงเพิ่มค่าของ `setPageWidth` / `setPageHeight` หรือเรียก `rasterizationOptions.setResolution(300)` ก่อนสร้าง `TiffOptions` จะทำให้คุณได้ภาพเรสเตอร์คุณภาพสูง เหมาะสำหรับการพิมพ์หรือการตรวจสอบรายละเอียด

## คำถามที่พบบ่อย

### Q1: Can I use Aspose.CAD for Java with other Java frameworks?

A1: ใช่, Aspose.CAD ถูกออกแบบให้สามารถรวมเข้ากับเฟรมเวิร์ก Java ต่าง ๆ ได้อย่างราบรื่น

### Q2: Is a temporary license available for Aspose.CAD?

A2: มี คุณสามารถรับใบอนุญาตชั่วคราวได้ [ที่นี่](https://purchase.aspose.com/temporary-license/)

### Q3: Where can I get community support for Aspose.CAD?

A3: เยี่ยมชม [ฟอรัม Aspose.CAD](https://forum.aspose.com/c/cad/19) เพื่อรับการสนับสนุนจากชุมชนและการสนทนาต่าง ๆ

### Q4: Can I try Aspose.CAD for free?

A4: แน่นอน! รับการทดลองใช้ฟรีได้ [ที่นี่](https://releases.aspose.com/)

### Q5: How do I purchase Aspose.CAD for Java?

A5: ซื้อผลิตภัณฑ์ได้ [ที่นี่](https://purchase.aspose.com/buy)

**Additional Q&A**

**Q: Does the canvas size affect vector quality in the PDF?**  
A: ไม่. ขนาด canvas ควบคุมมิติของหน้า; ข้อมูลเวกเตอร์ยังคงเป็นอิสระจากความละเอียด ทำให้การเรนเดอร์คมชัดที่ระดับการซูมใด ๆ

**Q: Can I set a different DPI for the TIFF output?**  
A: ได้. ปรับ `rasterizationOptions.setResolution(dpiValue)` ก่อนสร้าง `TiffOptions`

**Q: How can I **change PDF dimensions** for an existing PDF without re‑rendering the CAD?**  
A: ใช้ Aspose.PDF โหลด PDF ที่สร้างแล้วแล้วเรียก `pdf.getPages().setPageSize(PageSize.A4)` หรือขนาดที่กำหนดเอง

**Q: What is the best way to **convert dxf to pdf** while preserving layers?**  
A: รักษา `setAutomaticLayoutsScaling(true)` และหลีกเลี่ยง `setNoScaling(true)`; จะทำให้มองเห็นชั้นและเลย์เอาต์ได้อย่างครบถ้วน

## สรุป

ขอแสดงความยินดี! คุณได้ทำการ **convert CAD to PDF** และ **export CAD to TIFF** พร้อมกับ **set canvas size java**, เปิดใช้งาน **automatic layout scaling**, และเรียนรู้วิธี **configure canvas mode** เพื่อให้ได้ผลลัพธ์คุณภาพสูง บทเรียนนี้ให้พื้นฐานที่มั่นคงสำหรับโครงการแปลง CAD ของคุณ สำรวจคุณลักษณะและความเป็นไปได้เพิ่มเติมได้ใน [เอกสาร Aspose.CAD](https://reference.aspose.com/cad/java/)

---

**อัปเดตล่าสุด:** 2026-02-15  
**ทดสอบด้วย:** Aspose.CAD for Java 24.12  
**ผู้เขียน:** Aspose  

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}