---
date: 2026-01-12
description: เรียนรู้วิธีส่งออก CAD เป็น PDF พร้อมการละเว้นการตรวจจับหน้าโค้ดอัตโนมัติในไฟล์
  DWG โดยใช้ Aspose.CAD for Java รองรับการเข้ารหัสและไฟล์ CIF/MIF ที่ผิดรูปแบบ
linktitle: Override Automatic Code Page Detection in DWG Files
second_title: Aspose.CAD Java API
title: ส่งออก CAD เป็น PDF – ละเว้นการตรวจจับหน้าโค้ดอัตโนมัติในไฟล์ DWG ด้วย Java
url: /th/java/dwg-file-operations/override-code-page-detection/
weight: 13
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# ส่งออก CAD เป็น PDF – การละเว้นการตรวจจับ Code Page อัตโนมัติในไฟล์ DWG ด้วย Java

## บทนำ

ในคู่มือฉบับครอบคลุมนี้คุณจะค้นพบ **วิธีส่งออก CAD เป็น PDF** พร้อมกับการละเว้นการตรวจจับ code page อัตโนมัติที่อาจทำให้ข้อความในไฟล์ DWG เสียหาย Aspose.CAD for Java ให้การควบคุมการเข้ารหัสอย่างละเอียด ช่วยให้คุณกู้ข้อมูล CIF/MIF ที่เสียรูปและสร้างผลลัพธ์ PDF ที่เชื่อถือได้ ไม่ว่าคุณจะสร้างตัวแปลงแบบแบตช์หรือรวมการประมวลผล CAD เข้าในแอปพลิเคชัน Java ขนาดใหญ่ ขั้นตอนต่อไปนี้จะพาคุณผ่านขั้นตอนทำงานทั้งหมด

## คำตอบสั้น
- **What does “override code page” mean?** It forces Aspose.CAD to use a specific character encoding instead of guessing.  
  → มันบังคับให้ Aspose.CAD ใช้การเข้ารหัสอักขระที่ระบุแทนการเดา  
- **Can I export DWG directly to PDF?** Yes – after setting the correct code page, you can save the CAD image as PDF.  
  → ได้ – หลังจากตั้งค่า code page ที่ถูกต้องแล้ว คุณสามารถบันทึกภาพ CAD เป็น PDF ได้  
- **Which encoding works for Japanese text?** `CodePages.Japanese` and `MifCodePages.Japanese` are the right choices.  
  → `CodePages.Japanese` และ `MifCodePages.Japanese` เป็นตัวเลือกที่เหมาะสม  
- **Do I need a license for production use?** A commercial license is required; a temporary license is available for testing.  
  → จำเป็นต้องมีใบอนุญาตเชิงพาณิชย์; มีใบอนุญาตชั่วคราวสำหรับการทดสอบ  
- **What version of Aspose.CAD is needed?** Any recent version that supports `LoadOptions` and `PdfOptions`.  
  → เวอร์ชันล่าสุดใด ๆ ที่รองรับ `LoadOptions` และ `PdfOptions`

## “export CAD to PDF” คืออะไร?
การส่งออก CAD เป็น PDF จะเปลี่ยนภาพวาด CAD ที่เป็นเวกเตอร์ให้เป็นรูปแบบเอกสารที่รองรับอย่างกว้างขวางและมีการจัดวางคงที่ ผลลัพธ์เป็น PDF ที่คงรักษาเส้น, ชั้น, และข้อความไว้ในขณะที่ทำให้การวาดง่ายต่อการแชร์, พิมพ์, หรือฝังในแอปพลิเคชันอื่น ๆ

## ทำไมต้องละเว้นการตรวจจับ code page อัตโนมัติ?
ไฟล์ DWG มักเก็บข้อความโดยใช้ code page แบบเก่า Aspose.CAD ที่ตรวจจับอัตโนมัติอาจตีความไบต์เหล่านี้ผิดพลาด ทำให้เกิดอักขระเสียหาย โดยการระบุ code page ด้วยตนเอง คุณจะมั่นใจว่าข้อความจะแสดงตามที่ต้องการใน PDF ที่ส่งออก โดยเฉพาะสำหรับสคริปต์ที่ไม่ใช่ละติน เช่น ญี่ปุ่น, ซีริลลิก หรืออาหรับ

## ข้อกำหนดเบื้องต้น
- **Java Development Environment** – JDK 8+ และ IDE ที่คุณชื่นชอบ  
- **Aspose.CAD for Java** – ดาวน์โหลดไลบรารีจากเว็บไซต์อย่างเป็นทางการ [here](https://releases.aspose.com/cad/java/).  
- **DWG Sample File** – ใช้ไฟล์ `SimpleEntities.dwg` ที่ให้มา หรือ DWG ใด ๆ ที่คุณต้องการแปลง  

## นำเข้าแพ็กเกจ
ในโครงการ Java ของคุณ ให้นำเข้าคลาส Aspose.CAD ที่จำเป็น:

```java
import com.aspose.cad.CodePages;
import com.aspose.cad.Image;
import com.aspose.cad.LoadOptions;
import com.aspose.cad.MifCodePages;
import com.aspose.cad.fileformats.cad.CadImage;
```

## คู่มือขั้นตอนต่อขั้นตอน

### ขั้นตอนที่ 1: ตั้งค่าโครงการ Java
สร้างโครงการ Maven หรือ Gradle ใหม่และเพิ่มไฟล์ JAR ของ Aspose.CAD ไปยัง classpath ขั้นตอนนี้ทำให้ IDE สามารถค้นหาคลาสที่นำเข้าได้

### ขั้นตอนที่ 2: โหลดไฟล์ DWG ด้วย Code Page ที่ระบุ
บอก Aspose.CAD ว่าจะใช้การเข้ารหัสใดและว่าจะพยายามกู้ข้อมูล CIF/MIF ที่เสียรูปหรือไม่

```java
String SourceDir = "Your Document Directory";
String dwgPathToFile = SourceDir + "SimpleEntites.dwg";
LoadOptions opts = new LoadOptions();
opts.setSpecifiedEncoding(CodePages.Japanese);
opts.setSpecifiedMifEncoding(MifCodePages.Japanese);
opts.setRecoverMalformedCifMif(false);
CadImage cadImage = (CadImage) Image.load(dwgPathToFile, opts);
```

### ขั้นตอนที่ 3: ส่งออกภาพ CAD เป็น PDF
เมื่อกำหนด code page ที่ถูกต้องแล้ว คุณสามารถส่งออกภาพวาดได้อย่างปลอดภัย วัตถุ `PdfOptions` ช่วยให้คุณปรับแต่งผลลัพธ์ PDF ได้อย่างละเอียด (การบีบอัด, การเรสเตอร์ไลซ์ ฯลฯ)

```java
// Perform export or other operations with cadImage
// For example, exporting to PDF
PdfOptions pdfOptions = new PdfOptions();
cadImage.save("output.pdf", pdfOptions);
```

### ขั้นตอนที่ 4: ตรวจสอบความสำเร็จ
ข้อความคอนโซลง่าย ๆ จะยืนยันว่ากระบวนการเสร็จสมบูรณ์โดยไม่มีข้อยกเว้น

```java
System.out.println("OverrideAutomaticCodePageDetectionDwg executed successfully");
```

คุณสามารถทำซ้ำขั้นตอนเหล่านี้สำหรับไฟล์ DWG หลายไฟล์โดยปรับเส้นทางต้นทางและชื่อไฟล์ผลลัพธ์ตามต้องการ

## ปัญหาทั่วไปและวิธีแก้
- **Garbage characters still appear:** ตรวจสอบอีกครั้งว่า `specifiedEncoding` ตรงกับ code page ของ DWG ดั้งเดิมหรือไม่ ใช้ enum `CodePages` ตัวอื่นหากจำเป็น  
- **`NullPointerException` on `cadImage.save`:** ตรวจสอบว่าไฟล์ DWG โหลดสำเร็จ; ยืนยันเส้นทางและสิทธิ์การเข้าถึงไฟล์  
- **PDF size is large:** เปิดการบีบอัดใน `PdfOptions` (เช่น `pdfOptions.setCompress(true)`)  

## คำถามที่พบบ่อย

**Q1: Aspose.CAD รองรับเวอร์ชันทั้งหมดของไฟล์ DWG หรือไม่?**  
A1: Aspose.CAD รองรับช่วงเวอร์ชัน DWG ที่หลากหลาย รวมถึง AutoCAD 2018 และรุ่นก่อนหน้า  

**Q2: ฉันสามารถใช้ Aspose.CAD สำหรับโครงการเชิงพาณิชย์ได้หรือไม่?**  
A2: ใช่, จำเป็นต้องมีใบอนุญาตเชิงพาณิชย์สำหรับการใช้งานในผลิตภัณฑ์ คุณสามารถรับใบอนุญาตได้ [here](https://purchase.aspose.com/buy).  

**Q3: มีข้อจำกัดใดในเวอร์ชันทดลองฟรีหรือไม่?**  
A3: รุ่นทดลองมีการจำกัดขนาดและคุณสมบัติบางอย่าง; โปรดดูเอกสารอย่างเป็นทางการสำหรับรายละเอียด  

**Q4: ฉันจะขอรับการสนับสนุนสำหรับ Aspose.CAD ได้อย่างไร?**  
A4: เยี่ยมชมชุมชน [Aspose.CAD forum](https://forum.aspose.com/c/cad/19) สำหรับการช่วยเหลือและการสนทนา  

**Q5: มีใบอนุญาตชั่วคราวสำหรับการทดสอบหรือไม่?**  
A5: ใช่, สามารถขอใบอนุญาตชั่วคราวได้ [here](https://purchase.aspose.com/temporary-license/).  

---

**อัปเดตล่าสุด:** 2026-01-12  
**ทดสอบด้วย:** Aspose.CAD for Java 24.11 (latest at time of writing)  
**ผู้เขียน:** Aspose  

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}