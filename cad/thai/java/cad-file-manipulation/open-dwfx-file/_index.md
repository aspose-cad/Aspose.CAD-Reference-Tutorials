---
date: 2026-02-23
description: เรียนรู้วิธีแปลง DWFX เป็น PDF และบันทึก CAD เป็น PDF ด้วย Aspose.CAD
  สำหรับ Java คู่มือสั้นเพื่อเปิดไฟล์ DWFX และสร้าง PDF.
linktitle: Open DWFX File
second_title: Aspose.CAD Java API
title: แปลง DWFX เป็น PDF ด้วย Aspose.CAD สำหรับ Java
url: /th/java/cad-file-manipulation/open-dwfx-file/
weight: 10
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# แปลง DWFX เป็น PDF ด้วย Aspose.CAD for Java

## บทนำ

ในโลกการออกแบบที่เคลื่อนที่อย่างรวดเร็วในปัจจุบัน นักพัฒนามักต้องการ **แปลง DWFX เป็น PDF** เพื่อให้ภาพวาด CAD สามารถแชร์กับผู้มีส่วนได้ส่วนเสียที่ไม่ใช่เทคนิคได้ Aspose.CAD for Java ทำให้ภารกิจนี้ง่ายขึ้น โดยให้คุณเปิดไฟล์ DWFX, แปลงเป็น raster, และ **บันทึก CAD เป็น PDF** เพียงไม่กี่บรรทัดของโค้ด ในบทเรียนนี้เราจะอธิบายขั้นตอนทั้งหมด — ตั้งแต่การตั้งค่าสภาพแวดล้อมจนถึงการตรวจสอบ PDF สุดท้าย — เพื่อให้คุณมั่นใจในการจัดการไฟล์ DWFX ในแอปพลิเคชัน Java ของคุณ

## คำตอบด่วน
- **วัตถุประสงค์หลักของคู่มือนี้คืออะไร?** เพื่อแสดงวิธีแปลง DWFX เป็น PDF ด้วย Aspose.CAD for Java.  
- **ต้องใช้ไลบรารีใด?** Aspose.CAD for Java (ดาวน์โหลดจากเว็บไซต์อย่างเป็นทางการของ Aspose).  
- **ต้องการไลเซนส์หรือไม่?** การทดลองใช้ฟรีทำงานได้สำหรับการพัฒนา; จำเป็นต้องมีไลเซนส์เชิงพาณิชย์สำหรับการใช้งานจริง.  
- **สามารถเปิดไฟล์ DWFX ได้โดยตรงหรือไม่?** ได้, ใช้ `Image.load` เพื่อเปิดไฟล์ DWFX.  
- **รูปแบบผลลัพธ์ที่ตัวอย่างสร้างคืออะไร?** ไฟล์ PDF ที่บันทึกลงในไดเรกทอรีผลลัพธ์ที่ระบุ.

## “การแปลง DWFX เป็น PDF” คืออะไร

การแปลง DWFX เป็น PDF หมายถึงการนำภาพวาด DWFX ที่เป็นเวกเตอร์ — ที่มักใช้ในผลิตภัณฑ์ของ Autodesk — มาสร้างเป็นเอกสาร PDF ที่พกพาได้และได้รับการสนับสนุนอย่างกว้างขวาง ซึ่งทำให้สามารถดู, พิมพ์, และแชร์ได้ง่ายโดยไม่ต้องใช้ซอฟต์แวร์ CAD ที่ฝั่งผู้รับ

## ทำไมต้องใช้ Aspose.CAD for Java เพื่อ **บันทึก CAD เป็น PDF**?

- **ไม่มีการพึ่งพาภายนอก:** API แบบ Java แท้, ไม่ต้องการเครื่องยนต์ CAD เนทีฟ.  
- **การเรนเดอร์ความละเอียดสูง:** รักษาน้ำหนักเส้น, สี, และเลเยอร์.  
- **เหมาะสำหรับการประมวลผลแบบแบตช์:** เหมาะสำหรับการทำงานอัตโนมัติบนเซิร์ฟเวอร์หรือบริการคลาวด์.  
- **ข้ามแพลตฟอร์ม:** ทำงานบน Windows, Linux, และ macOS.

## ข้อกำหนดเบื้องต้น

- **Aspose.CAD for Java Library** – ดาวน์โหลดจาก [หน้าดาวน์โหลด Aspose.CAD for Java](https://releases.aspose.com/cad/java/).  
- **สภาพแวดล้อมการพัฒนา Java** – JDK 8 หรือใหม่กว่า, พร้อม IDE หรือเครื่องมือสร้างที่คุณชื่นชอบ.  
- **ไฟล์ DWFX** – ไฟล์ DWFX ตัวอย่าง (เช่น `Tyrannosaurus.dwfx`) เพื่อทดสอบการแปลง.

## นำเข้า Namespaces

ก่อนอื่นให้นำเข้าคลาสที่เราต้องการใช้:

```java
import com.aspose.cad.Image;

import com.aspose.cad.fileformats.cad.CadImage;
import com.aspose.cad.imageoptions.CadRasterizationOptions;
import com.aspose.cad.imageoptions.PdfOptions;
```

## วิธีแปลง DWFX เป็น PDF ด้วย Aspose.CAD for Java

ต่อไปนี้เป็นการอธิบายขั้นตอนทีละขั้นตอน แต่ละขั้นตอนมีคำอธิบายสั้น ๆ ตามด้วยโค้ดที่ต้องรัน

### ขั้นตอนที่ 1: โหลดไฟล์ DWFX  

```java
String SourceDir = Utils.getDataDir_DWFXDrawings();
String OutputDir = Utils.getDataDir_Output();
String filePath = SourceDir + "Tyrannosaurus.dwfx";

Image cadImageDwf = Image.load(filePath);
```

เมธอด `Image.load` จะอ่านไฟล์ DWFX เข้าไปในหน่วยความจำ, ให้เราได้อ็อบเจกต์ `CadImage` ที่พร้อมสำหรับการแปลงเป็น raster.

### ขั้นตอนที่ 2: ตั้งค่าตัวเลือกการแปลงเป็น Raster  

```java
CadRasterizationOptions rasterizationOptions = new CadRasterizationOptions();
rasterizationOptions.setPageWidth(cadImageDwf.getSize().getWidth());
rasterizationOptions.setPageHeight(cadImageDwf.getSize().getHeight());
```

ตัวเลือกเหล่านี้กำหนดขนาดหน้าผลลัพธ์, ทำให้ PDF มีขนาดตรงกับมิติของภาพวาดต้นฉบับ.

### ขั้นตอนที่ 3: กำหนดค่าตัวเลือก PDF  

```java
PdfOptions CADf = new PdfOptions();
CADf.setVectorRasterizationOptions(rasterizationOptions);
```

ที่นี่เราจะผูกการตั้งค่าการแปลงเป็น raster กับการกำหนดค่าการส่งออก PDF.

### ขั้นตอนที่ 4: บันทึกเป็น PDF  

```java
cadImageDwf.save(OutputDir + "OpenDwfxFile_out.pdf", CADf);
```

การเรียก `save` จะเขียนภาพที่แปลงแล้วลงไฟล์ PDF ในโฟลเดอร์ผลลัพธ์.

### ขั้นตอนที่ 5: ตรวจสอบความสำเร็จ  

```java
System.out.println("OpenDwfxFile executed successfully");
```

ข้อความคอนโซลง่าย ๆ จะยืนยันว่าการแปลงเสร็จสมบูรณ์โดยไม่มีข้อผิดพลาด.

## ปัญหาที่พบบ่อยและวิธีแก้

| ปัญหา | สาเหตุที่เป็นไปได้ | วิธีแก้ |
|-------|-------------------|----------|
| **ผลลัพธ์ PDF ว่าง** | ความกว้าง/สูงของการแปลงเป็น raster ตั้งเป็น 0 | ตรวจสอบให้ `cadImageDwf.getSize()` คืนค่ามิติที่ถูกต้องก่อนตั้งค่าตัวเลือก. |
| **ข้อผิดพลาดหน่วยความจำไม่พอ** | ไฟล์ DWFX ขนาดใหญ่มาก | เพิ่มขนาด heap ของ JVM (`-Xmx2g`) หรือประมวลผลไฟล์เป็นส่วนย่อย ๆ |
| **ฟอนต์หาย** | ฟอนต์ไม่ได้ฝังใน DWFX ต้นฉบับ | ติดตั้งฟอนต์ที่จำเป็นบนเซิร์ฟเวอร์หรือใช้ `CadRasterizationOptions.setFontName` เพื่อระบุฟอนต์สำรอง. |

## คำถามที่พบบ่อย

### Q1: ฉันสามารถใช้ Aspose.CAD for Java กับรูปแบบไฟล์ CAD อื่นได้หรือไม่?  
A1: ได้, Aspose.CAD for Java รองรับรูปแบบไฟล์ CAD หลากหลาย ให้เป็นโซลูชันที่หลากหลายสำหรับนักพัฒนา.

### Q2: มีการทดลองใช้ฟรีสำหรับ Aspose.CAD for Java หรือไม่?  
A2: มี, คุณสามารถสำรวจความสามารถของ Aspose.CAD for Java ด้วยการทดลองใช้ฟรี เยี่ยมชม [ลิงก์นี้](https://releases.aspose.com/) เพื่อเริ่มต้น.

### Q3: ฉันจะขอรับการสนับสนุนสำหรับ Aspose.CAD for Java ได้อย่างไร?  
A3: เข้าร่วมชุมชน Aspose.CAD ใน [ฟอรั่มสนับสนุน](https://forum.aspose.com/c/cad/19) เพื่อขอความช่วยเหลือและการร่วมมือ.

### Q4: มีไลเซนส์ชั่วคราวสำหรับ Aspose.CAD for Java หรือไม่?  
A4: มี, คุณสามารถขอรับไลเซนส์ชั่วคราวสำหรับ Aspose.CAD for Java ได้ เยี่ยมชม [ลิงก์นี้](https://purchase.aspose.com/temporary-license/) เพื่อดูรายละเอียดเพิ่มเติม.

### Q5: ฉันจะหาเอกสารสำหรับ Aspose.CAD for Java ได้ที่ไหน?  
A5: เอกสารที่ครอบคลุมพร้อมให้บริการ [ที่นี่](https://reference.aspose.com/cad/java/).

---

**อัปเดตล่าสุด:** 2026-02-23  
**ทดสอบด้วย:** Aspose.CAD for Java 24.11  
**ผู้เขียน:** Aspose  

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}