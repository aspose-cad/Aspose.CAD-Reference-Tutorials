---
date: 2025-12-09
description: เรียนรู้วิธีสร้าง PDF จากไฟล์ DWG ด้วย Aspose.CAD สำหรับ Java. แปลง DWG
  เป็น PDF อย่างง่ายดายด้วยการสนับสนุนเมช.
linktitle: Mesh Support in CAD
second_title: Aspose.CAD Java API
title: สร้าง PDF จาก DWG ด้วย Aspose.CAD สำหรับ Java
url: /th/java/advanced-cad-features/mesh-support-in-cad/
weight: 12
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# สร้าง PDF จาก DWG ด้วย Aspose.CAD สำหรับ Java

## บทนำ

ในบทเรียนนี้คุณจะได้เรียนรู้ **วิธีสร้าง PDF จากไฟล์ DWG** ด้วย Aspose.CAD สำหรับ Java ไลบรารีนี้รองรับเมชที่ซับซ้อน ทำให้คุณสามารถแปลงภาพวาด CAD ที่มีเมช 3‑D ไปเป็น PDF ได้โดยไม่สูญเสียรายละเอียด ไม่ว่าคุณจะต้อง **แปลง DWG เป็น PDF** เพื่อการรายงาน การเก็บถาวร หรือการประมวลผลต่อไป ขั้นตอนต่อไปนี้จะช่วยคุณสร้างโซลูชันที่เชื่อถือได้และพร้อมใช้งานในระดับผลิตภัณฑ์

## คำตอบอย่างรวดเร็ว
- **บทเรียนครอบคลุมอะไร?** การแปลงไฟล์ DWG ที่มีเมชเป็น PDF ด้วย Aspose.CAD สำหรับ Java  
- **ฉันต้องการใบอนุญาตหรือไม่?** ใบอนุญาตชั่วคราวใช้ได้สำหรับการทดสอบ; ต้องมีใบอนุญาตเต็มสำหรับการใช้งานเชิงพาณิชย์  
- **เวอร์ชัน Java ที่รองรับคืออะไร?** Java 8 หรือใหม่กว่า  
- **ฉันสามารถส่งออกเป็นรูปแบบอื่นได้หรือไม่?** ใช่ – Aspose.CAD ยังรองรับ PNG, JPEG, BMP และอื่น ๆ อีกมาก  
- **การแปลงใช้เวลานานเท่าไหร่?** ปกติใช้เวลาน้อยกว่าวินาทีสำหรับภาพวาดขนาดมาตรฐาน

## วิธีสร้าง PDF จาก DWG?

ด้านล่างนี้เป็นคู่มือสั้น ๆ ที่อธิบายขั้นตอนอย่างละเอียด ตั้งแต่การตั้งค่าโปรเจกต์จนถึงการบันทึกไฟล์ PDF สุดท้าย

## ข้อกำหนดเบื้องต้น

- **สภาพแวดล้อมการพัฒนา Java:** JDK 8 หรือใหม่กว่าติดตั้งบนเครื่องของคุณ  
- **ไลบรารี Aspose.CAD สำหรับ Java:** ดาวน์โหลด JAR ล่าสุดจาก [download link](https://releases.aspose.com/cad/java/)  
- **เอกสารที่มีเมช:** ไฟล์ DWG ที่บรรจุข้อมูลเมช (เช่น `meshes.dwg`)  

## นำเข้า Namespaces

ในไฟล์ซอร์ส Java ของคุณ ให้รวมคลาส Aspose.CAD ที่จำเป็น:

```java
import com.aspose.cad.Image;

import com.aspose.cad.fileformats.cad.CadImage;
import com.aspose.cad.imageoptions.CadRasterizationOptions;
import com.aspose.cad.imageoptions.PdfOptions;
```

## ขั้นตอนที่ : ตั้งค่าโครงการ

สร้างโปรเจกต์ Java ใหม่ (หรือเพิ่มในโปรเจกต์ที่มีอยู่) แล้วเพิ่ม JAR ของ Aspose.CAD ไปยัง classpath ของโครงการ กำหนดไดเรกทอรีฐานที่ใช้เก็บไฟล์ DWG ต้นฉบับและ PDF ที่สร้างขึ้น

## ขั้นตอนที่ 2: กำหนดเส้นทางไฟล์

ระบุตำแหน่งที่ไฟล์ DWG อยู่และที่ที่ต้องการบันทึกไฟล์ PDF

```java
String dataDir = "Your Document Directory" + "CADConversion/";
String sourceFilePath = dataDir + "meshes.dwg";
String outPath = dataDir + "meshes.pdf";
```

## ขั้นตอนที่ 3: โหลดภาพ CAD

โหลดไฟล์ DWG ลงในอ็อบเจ็กต์ `CadImage` เพื่อให้ Aspose.CAD สามารถทำงานกับโครงสร้างภายในได้

```java
CadImage cadImage = (CadImage)Image.load(sourceFilePath);
```

## ขั้นตอนที่ 4: ตั้งค่าตัวเลือกการเรสเตอร์ไลเซชัน

กำหนดตัวเลือกการเรสเตอร์ไลเซชันที่ควบคุมขนาดและเลย์เอาต์ของหน้าที่สร้างใน PDF ค่าที่อยู่ในอาเรย์ `Layouts` จะบอก Aspose.CAD ให้เรนเดอร์พื้นที่ **Model** ซึ่งรวมถึงเอนทิตีเมช

```java
CadRasterizationOptions rasterizationOptions = new CadRasterizationOptions();
rasterizationOptions.setPageWidth(1600);
rasterizationOptions.setPageHeight(1600);
rasterizationOptions.setLayouts(new String[] { "Model" });
```

## ขั้นตอนที่ 5: ตั้งค่าตัวเลือก PDF

ผูกการตั้งค่าการเรสเตอร์ไลเซชันเข้ากับอินสแตนซ์ `PdfOptions` ซึ่งบอกไลบรารีให้ใช้ตัวเลือกที่กำหนดไว้เมื่อต้องสร้าง PDF

```java
PdfOptions pdfOptions = new PdfOptions();
pdfOptions.setVectorRasterizationOptions(rasterizationOptions);
```

## ขั้นตอนที่ 6: บันทึก PDF

สุดท้ายให้บันทึกภาพ CAD ที่โหลดไว้เป็นไฟล์ PDF เอกสารที่ได้จะมีการแสดงผลที่ตรงกับ DWG ดั้งเดิม รวมถึงเรขาคณิตเมชด้วย

```java
cadImage.save(outPath, pdfOptions);
```

### ทำไมวิธีนี้จึงทำงานสำหรับ **การแปลง CAD เป็น PDF**

Aspose.CAD ทำการเรสเตอร์ไลเซชันแบบเวกเตอร์ คงน้ำหนักเส้น สี และรายละเอียดเมช 3‑D ไว้ได้โดยตรง การกำหนดค่าตัวเลือกการเรสเตอร์ไลเซชันช่วยควบคุมความละเอียดและเลย์เอาต์ ทำให้ **การส่งออกภาพวาด CAD** ปรากฏใน PDF อย่างที่ต้องการ

## กรณีการใช้งานทั่วไป

- **การรายงานอัตโนมัติ:** สร้างรายงาน PDF จากภาพวาดวิศวกรรมแบบเรียลไทม์  
- **การเก็บเอกสาร:** เก็บภาพวาด CAD เป็น PDF เพื่อการเก็บรักษาระยะยาว  
- **บริการเว็บ:** เปิด API ที่รับไฟล์ DWG แล้วคืนค่าเป็น PDF เหมาะสำหรับแพลตฟอร์ม SaaS  

## เคล็ดลับการแก้ไขปัญหา

- **เมชหายไปในผลลัพธ์:** ตรวจสอบให้แน่ใจว่า property `Layouts` มีค่า `"Model"`; เมชมักอยู่ใน Model space  
- **การสเกลที่ไม่ถูกต้อง:** ปรับ `PageWidth` และ `PageHeight` ให้ตรงกับหน่วยของภาพวาดต้นฉบับ  
- **ข้อผิดพลาดเกี่ยวกับใบอนุญาต:** เรียก `License.setLicense()` พร้อมไฟล์ใบอนุญาตที่ถูกต้องก่อนโหลดภาพ  

## สรุป

โดยทำตามขั้นตอนเหล่านี้ คุณสามารถ **แปลง DWG เป็น PDF** ได้อย่างมั่นใจและใช้ประโยชน์จากการสนับสนุนเมชของ Aspose.CAD ความสามารถนี้ช่วยทำให้กระบวนการทำงานที่ต้องการ PDF คุณภาพสูงจากภาพวาด CAD ที่ซับซ้อนง่ายขึ้น ไม่ว่าจะใช้ภายในองค์กรหรือสำหรับเอกสารที่ต้องส่งมอบให้ลูกค้า

## คำถามที่พบบ่อย

### Q1: Aspose.CAD สำหรับ Java เหมาะสำหรับการใช้งานเชิงพาณิชย์หรือไม่?

A1: ใช่, Aspose.CAD สำหรับ Java ถูกออกแบบให้ใช้ได้ทั้งส่วนบุคคลและเชิงพาณิชย์ คุณสามารถดูรายละเอียดการให้สิทธิ์ได้ที่ [purchase page](https://purchase.aspose.com/buy)

### Q2: ฉันจะขอใบอนุญาตชั่วคราวเพื่อการทดสอบได้อย่างไร?

A2: รับใบอนุญาตชั่วคราวจาก [here](https://purchase.aspose.com/temporary-license/) สำหรับการทดสอบและประเมินผล

### Q3: ฉันจะหาแหล่งสนับสนุนจากชุมชนสำหรับ Aspose.CAD สำหรับ Java ได้ที่ไหน?

A3: เยี่ยมชมฟอรั่มเฉพาะของ Aspose.CAD ที่ [https://forum.aspose.com/c/cad/19](https://forum.aspose.com/c/cad/19) เพื่อรับการสนับสนุนจากชุมชน

### Q4: มีรูปแบบผลลัพธ์อื่น ๆ ที่รองรับนอกจาก PDF หรือไม่?

A4: มี, Aspose.CAD สำหรับ Java รองรับรูปแบบผลลัพธ์หลายรูปแบบ เช่น PNG, JPEG, BMP และอื่น ๆ ดูรายละเอียดในเอกสารประกอบ

### Q5: ฉันสามารถลองใช้ Aspose.CAD สำหรับ Java ได้ฟรีหรือไม่?

A5: ใช่, คุณสามารถทดลองใช้เวอร์ชันฟรีของ Aspose.CAD สำหรับ Java ได้ที่ [here](https://releases.aspose.com/)

---

**Last Updated:** 2025-12-09  
**Tested With:** Aspose.CAD for Java 24.11  
**Author:** Aspose  

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}