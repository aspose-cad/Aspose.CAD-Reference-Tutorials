---
date: 2025-12-18
description: สำรวจวิธีการส่งออกไฟล์ DWG เป็น PDF หรือภาพเรสเตอร์ใน Java ด้วย Aspose.CAD
  คู่มือขั้นตอนนี้รับประกันความแม่นยำ ประสิทธิภาพ และการแปลงไฟล์ DWG อย่างง่ายดาย
linktitle: Export DWG to PDF or Raster
second_title: Aspose.CAD Java API
title: ส่งออก DWG เป็น PDF หรือ Raster ด้วย Aspose.CAD สำหรับ Java
url: /th/java/cad-drawing-conversion/export-dwg-to-pdf-or-raster/
weight: 13
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# ส่งออก DWG เป็น PDF หรือ Raster ด้วย Aspose.CAD for Java

## บทนำ

ในโลกที่เปลี่ยนแปลงอย่างรวดเร็วของการออกแบบด้วยคอมพิวเตอร์ (CAD) การจัดการแบบร่างอย่างมีประสิทธิภาพเป็นสิ่งสำคัญ ด้วย **Aspose.CAD for Java** คุณสามารถ **export dwg to pdf** — หรือภาพ raster — ได้ด้วยไม่กี่บรรทัดของโค้ด บทเรียนนี้จะพาคุณผ่านกระบวนการทั้งหมด ตั้งแต่การโหลดไฟล์ DWG จนถึงการสร้าง PDF คุณภาพสูง พร้อมเน้นเหตุผลที่ทำให้ Aspose.CAD Java เป็นไลบรารีที่เลือกใช้สำหรับงานแปลง CAD

## คำตอบอย่างรวดเร็ว
- **บทเรียนนี้ครอบคลุมอะไร?** การส่งออกไฟล์ DWG เป็น PDF หรือภาพ raster ด้วย Aspose.CAD for Java  
- **ต้องใช้ไลเซนส์หรือไม่?** มีไลเซนส์ชั่วคราวฟรีสำหรับการประเมิน; ต้องมีไลเซนส์เต็มสำหรับการใช้งานจริง  
- **รองรับเวอร์ชัน Java ใด?** ทุก Runtime Java 8+ ทำงานได้กับ Aspose.CAD Java API เวอร์ชันล่าสุด  
- **สามารถแปลง DWG ไปเป็นรูปแบบภาพอื่นได้หรือไม่?** ได้ – ตัวเลือก rasterization เดียวกันสามารถส่งออกเป็น PNG, JPEG, BMP ฯลฯ  
- **การแปลงใช้เวลานานแค่ไหน?** ปกติใช้เวลาน้อยกว่าวินาทีสำหรับแบบร่างมาตรฐาน; ไฟล์ขนาดใหญ่อาจใช้หลายวินาที

## “export dwg to pdf” คืออะไร?
การ export DWG ไปเป็น PDF หมายถึงการแปลงแบบร่าง AutoCAD ดั้งเดิมให้เป็นเอกสาร PDF ที่พกพาได้และอิสระต่ออุปกรณ์ PDF ที่ได้จะคงข้อมูลเวกเตอร์, ชั้น, และสเกลไว้ ทำให้เหมาะสำหรับการแชร์, พิมพ์, หรือเก็บรักษา

## ทำไมต้องใช้ Aspose.CAD Java สำหรับการแปลงนี้?
- **ไม่มีการพึ่งพาไลบรารีภายนอก** – Java แท้, ไม่ต้องใช้ DLL แบบเนทีฟ  
- **การจัดการหน่วยที่แม่นยำ** – ปรับให้สอดคล้องกับหน่วยเมตริกหรืออิมพีเรียลโดยอัตโนมัติ  
- **ผลลัพธ์ raster คุณภาพสูง** – ควบคุม DPI และขนาดหน้าได้อย่างละเอียด  
- **รองรับ PDF อย่างเต็มรูปแบบ** – การสร้าง PDF ที่คงเวกเตอร์โดยไม่ต้องใช้ไลบรารีเพิ่มเติม

## ข้อกำหนดเบื้องต้น

ก่อนเริ่มเขียนโค้ด โปรดตรวจสอบว่าคุณมี:

- ความรู้พื้นฐานด้านการเขียนโปรแกรม Java  
- ไลบรารี Aspose.CAD for Java ติดตั้งแล้ว หากยังไม่ได้ดาวน์โหลด สามารถรับได้จาก **[ที่นี่](https://releases.aspose.com/cad/java/)**  
- ไฟล์ DWG สำหรับทดสอบ – ตัวอย่าง **Bottom_plate.dwg** จะใช้ในคู่มือนี้

## นำเข้า Namespaces

ในโปรเจกต์ Java ของคุณ ให้ import คลาสที่จำเป็นเพื่อเริ่มต้นการแปลง:

```java
import com.aspose.cad.Image;

import com.aspose.cad.imageoptions.CadRasterizationOptions;
import com.aspose.cad.imageoptions.PdfOptions;
import com.aspose.cad.imageoptions.UnitType;
```

## คู่มือขั้นตอนโดยละเอียด

### ขั้นตอนที่ 1: โหลดไฟล์ DWG

แรกเริ่มให้โหลดแบบร่าง DWG ของคุณด้วยคลาส `Image` ซึ่งจะสร้างการแสดงผลในหน่วยความจำที่ Aspose.CAD สามารถทำงานได้

```java
String dataDir = "Your Document Directory" + "DWGDrawings/";
String srcFile = dataDir + "Bottom_plate.dwg";
Image objImage = Image.load(srcFile);
```

### ขั้นตอนที่ 2: กำหนดประเภทหน่วย

การเข้าใจว่าแบบร่างใช้หน่วยเมตริกหรืออิมพีเรียลเป็นสิ่งสำคัญสำหรับการสเกลที่ถูกต้อง วิธีช่วยเหลือ `IsMetric` (การทำงานไม่ได้แสดงในที่นี้) จะคืนค่า boolean

```java
Boolean currentUnitIsMetric = IsMetric(objImage.getUnitType());
int currentUnitCoefficient = objImage.getUnitType();
```

### ขั้นตอนที่ 3: ตั้งค่าตัวเลือกการ Rasterization

อิงตามระบบหน่วยที่ตรวจพบ ให้กำหนดขนาดหน้า, การสเกล, และประเภทหน่วยเป้าหมาย ตัวเลือกเหล่านี้จะกำหนดวิธีที่ DWG ถูก rasterize ก่อนนำไปบรรจุใน PDF

```java
CadRasterizationOptions rasterizationOptions = new CadRasterizationOptions();

if (currentUnitIsMetric) {
    // Metric units
    double metersCoeff = 1 / 1000.0;
    double scaleFactor = metersCoeff / currentUnitCoefficient;
    rasterizationOptions.setPageWidth((float)(210 * scaleFactor));
    rasterizationOptions.setPageHeight((float)(297 * scaleFactor));
    rasterizationOptions.setUnitType(UnitType.Millimeter);
} else {
    // Imperial units
    rasterizationOptions.setPageWidth((float)(8.27f / currentUnitCoefficient));
    rasterizationOptions.setPageHeight((float)(11.69f / currentUnitCoefficient));
    rasterizationOptions.setUnitType(UnitType.Inch);
}
```

### ขั้นตอนที่ 4: ตั้งค่าตัวเลือก PDF

สร้างอินสแตนซ์ `PdfOptions` แล้วแนบการตั้งค่า rasterization นี้ จะบอก Aspose.CAD ว่าจะฝังเนื้อหา raster ลงใน PDF อย่างไร

```java
PdfOptions pdfOptions = new PdfOptions();
pdfOptions.setVectorRasterizationOptions(new CadRasterizationOptions());
```

### ขั้นตอนที่ 5: บันทึกเป็น PDF

สุดท้าย ให้ส่งออกแบบร่างเป็นไฟล์ PDF วิธี `save` จะรับพาธไฟล์ผลลัพธ์และ `PdfOptions` ที่กำหนดไว้

```java
objImage.save(dataDir + "Saved.pdf", pdfOptions);
```

เมื่อโค้ดทำงานเสร็จ คุณจะพบไฟล์ **Saved.pdf** ในโฟลเดอร์ `DWGDrawings` ของคุณ พร้อมใช้งานสำหรับการแจกจ่ายหรือเก็บรักษา

## ปัญหาทั่วไป & เคล็ดลับ

- **ขนาดหน้าผิด** – ตรวจสอบตรรกะการแปลงหน่วย; ค่าสัมประสิทธิ์ที่ไม่ตรงกันอาจทำให้หน้ามีขนาดใหญ่เกินไป  
- **ฟอนต์หรือ lineweight หาย** – ตรวจสอบให้แน่ใจว่า DWG อ้างอิงทรัพยากรภายนอกทั้งหมดก่อนทำการแปลง  
- **ประสิทธิภาพกับแบบร่างขนาดใหญ่** – เพิ่มค่า `DPI` ใน `CadRasterizationOptions` เฉพาะเมื่อจำเป็นต้องการคุณภาพสูง; ลด DPI จะช่วยเร่งการประมวลผล

## คำถามที่พบบ่อย

**ถาม: สามารถใช้ Aspose.CAD for Java กับเฟรมเวิร์ก Java อื่นได้หรือไม่?**  
ตอบ: ใช่, Aspose.CAD for Java สามารถผสานรวมได้อย่างราบรื่นกับเฟรมเวิร์ก Java ยอดนิยมเช่น Spring, Jakarta EE, และ Android

**ถาม: มีไลเซนส์ชั่วคราวสำหรับ Aspose.CAD for Java หรือไม่?**  
ตอบ: มี, คุณสามารถรับไลเซนส์ชั่วคราว **[ที่นี่](https://purchase.aspose.com/temporary-license/)**

**ถาม: จะหาแหล่งสนับสนุนสำหรับ Aspose.CAD for Java ได้จากที่ไหน?**  
ตอบ: เยี่ยมชม **[ฟอรั่ม Aspose.CAD](https://forum.aspose.com/c/cad/19)** เพื่อรับความช่วยเหลือจากชุมชนและวิศวกรของ Aspose

**ถาม: จะซื้อไลเซนส์สำหรับ Aspose.CAD for Java ได้อย่างไร?**  
ตอบ: คุณสามารถสั่งซื้อไลเซนส์ **[ที่นี่](https://purchase.aspose.com/buy)**

**ถาม: Aspose.CAD for Java รองรับหน่วยใดบ้าง?**  
ตอบ: รองรับทั้งหน่วยเมตริกและอิมพีเรียล โดยจะตรวจจับระบบหน่วยของแบบร่างโดยอัตโนมัติ

**ถาม: สามารถแปลง DWG ไปเป็นรูปแบบภาพอื่น (เช่น PNG, JPEG) ด้วย API เดียวกันได้หรือไม่?**  
ตอบ: แน่นอน. เพียงแทนที่ `PdfOptions` ด้วยตัวเลือกภาพ raster ที่เหมาะสม (เช่น `PngOptions`) แล้วใช้ `CadRasterizationOptions` เดิมต่อไป

## สรุป

บทเรียนนี้ได้สาธิตวิธี **export dwg to pdf** และภาพ raster ด้วย Aspose.CAD for Java โดยการทำตามขั้นตอนที่อธิบาย คุณสามารถผสานการแปลง CAD ที่เชื่อถือได้เข้าไปในแอปพลิเคชัน Java ใดก็ได้ ไม่ว่าจะต้องการ PDF สำหรับเอกสารหรือภาพ raster สำหรับการแสดงบนเว็บ

---

**Last Updated:** 2025-12-18  
**Tested With:** Aspose.CAD for Java 24.10  
**Author:** Aspose  

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}