---
date: 2025-12-28
description: เรียนรู้วิธีสร้าง PDF จาก CAD โดยแปลง DWG เป็น PDF ด้วย Aspose.CAD สำหรับ
  Java ทำตามคำแนะนำขั้นตอนต่อขั้นตอนเพื่อส่งออกเลย์เอาต์ DWG เป็น PDF และสร้างภาพ
linktitle: Render DWG Document to Image with Java
second_title: Aspose.CAD Java API
title: 'สร้าง PDF จาก CAD - แปลง DWG เป็นภาพด้วย Aspose.CAD สำหรับ Java'
url: /th/java/cad-meta-data-and-rendering/render-dwg-to-image/
weight: 11
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# แปลงเอกสาร DWG เป็นภาพด้วย Aspose.CAD สำหรับ Java

## บทนำ

ในโลกที่เปลี่ยนแปลงอย่างรวดเร็วของการพัฒนา Java, Aspose.CAD โดดเด่นในฐานะเครื่องมือที่ทรงพลังสำหรับการจัดการไฟล์ Computer‑Aided Design (CAD). **บทเรียนนี้จะแสดงวิธีสร้าง PDF จาก CAD** โดยการเรนเดอร์เอกสาร DWG เป็นภาพและจากนั้นส่งออกเป็น PDF ไม่ว่าคุณจะเป็นนักพัฒนาที่มีประสบการณ์หรือเพิ่งเริ่มต้นการเขียนโค้ด คู่มือขั้นตอนต่อขั้นตอนนี้จะพาคุณผ่านกระบวนการด้วยความชัดเจนและง่ายดาย.

## คำตอบด่วน
- **ต้องใช้ไลบรารีอะไร?** Aspose.CAD for Java.
- **ฉันสามารถแปลง DWG เป็น PDF ได้หรือไม่?** ได้ – ตัวอย่างนี้แสดงการแปลงเลเอาต์ DWG เป็น PDF.
- **ต้องการไลเซนส์สำหรับการใช้งานจริงหรือไม่?** จำเป็นต้องมีไลเซนส์ Aspose.CAD ที่ถูกต้องสำหรับการใช้งานที่ไม่ใช่การประเมิน.
- **IDE ที่รองรับมีอะไรบ้าง?** Eclipse, IntelliJ IDEA, NetBeans, และ IDE ใด ๆ ที่รองรับ Java.
- **รูปแบบผลลัพธ์ที่มีให้เลือกคืออะไร?** PDF, PNG, JPEG, BMP, และรูปแบบ raster อื่น ๆ.

## การสร้าง PDF จาก CAD คืออะไร?

การสร้าง PDF จาก CAD หมายถึงการนำภาพวาดแบบเวกเตอร์ (เช่นไฟล์ DWG) มาทำให้เป็นภาพ raster หรือเวกเตอร์ในรูปแบบเอกสาร PDF ซึ่งทำให้สามารถแชร์ พิมพ์ และเก็บบันทึกภาพวาดทางเทคนิคได้อย่างง่ายดายโดยไม่ต้องใช้แอปพลิเคชัน CAD ดั้งเดิม.

## ทำไมต้องใช้ Aspose.CAD สำหรับ Java?

- **ไม่มีการพึ่งพาภายนอก** – ไลบรารีทำงานได้ทันที.
- **การเรนเดอร์คุณภาพสูง** – รักษาน้ำหนักเส้น, เลเยอร์, และเลเอาต์.
- **การประมวลผลแบบชุด** – คุณสามารถแปลงหลายภาพวาดในครั้งเดียว.
- **ข้ามแพลตฟอร์ม** – ทำงานบน Windows, Linux, และ macOS.

## ข้อกำหนดเบื้องต้น

- **สภาพแวดล้อมการพัฒนา Java** – ติดตั้ง JDK 8 หรือสูงกว่า.
- **ไลบรารี Aspose.CAD สำหรับ Java** – ดาวน์โหลดจาก [download link](https://releases.aspose.com/cad/java/).
- **เอกสาร DWG** – ไฟล์ DWG ที่คุณต้องการเรนเดอร์ (ตัวอย่างหรือของคุณเอง).

## นำเข้า Namespaces

ในโค้ด Java ของคุณ ให้นำเข้าคลาสที่จำเป็นเพื่อใช้ฟังก์ชันของ Aspose.CAD:

```java
import com.aspose.cad.Image;

import com.aspose.cad.imageoptions.CadRasterizationOptions;
import com.aspose.cad.imageoptions.PdfOptions;
```

ต่อไปนี้เป็นการแยกโค้ดตัวอย่างเป็นหลายขั้นตอนเพื่อความเข้าใจที่ครอบคลุม:

## ขั้นตอนที่ 1: ระบุไดเรกทอรีทรัพยากร

```java
// The path to the resource directory.
String dataDir = "Your Document Directory" + "DWGDrawings/";
```

แทนที่ `"Your Document Directory"` ด้วยพาธจริงที่เก็บไฟล์ DWG ของคุณ.

## ขั้นตอนที่ 2: โหลดเอกสาร DWG

```java
String srcFile = dataDir + "visualization_-_conference_room.dwg";
Image image = Image.load(srcFile);
```

ขั้นตอนนี้จะโหลดไฟล์ DWG เข้าไปในอ็อบเจ็กต์ `Image` ที่ Aspose.CAD สามารถทำงานได้.

## ขั้นตอนที่ 3: ตั้งค่าตัวเลือกการเรนเดอร์แบบ Raster

```java
CadRasterizationOptions rasterizationOptions = new CadRasterizationOptions();
rasterizationOptions.setPageWidth(1600);
rasterizationOptions.setPageHeight(1600);
rasterizationOptions.setLayouts(new String[] {"Layout1"});
```

ที่นี่เรากำหนดวิธีการแปลงภาพวาดเป็น raster: ขนาดหน้าและเลเอาต์เฉพาะที่จะเรนเดอร์ นี่เป็นขั้นตอนสำคัญสำหรับ **render dwg to image** และ **export dwg layout pdf**.

## ขั้นตอนที่ 4: สร้าง PDF Options

```java
PdfOptions pdfOptions = new PdfOptions();
pdfOptions.setVectorRasterizationOptions(rasterizationOptions);
```

`PdfOptions` เชื่อมการตั้งค่า rasterization กับรูปแบบการส่งออก PDF.

## ขั้นตอนที่ 5: ส่งออกเป็น PDF

```java
image.save(dataDir + "ExportSpecificLayoutToPDF_out_.pdf", pdfOptions);
```

เมธอด `save` จะเขียนภาพที่เรนเดอร์ลงในไฟล์ PDF ทำให้ **convert dwg to pdf** อย่างมีประสิทธิภาพ.

## ปัญหาทั่วไปและวิธีแก้

| ปัญหา | วิธีแก้ |
|-------|----------|
| **ไม่พบไฟล์** | ตรวจสอบว่า `dataDir` ชี้ไปยังโฟลเดอร์ที่ถูกต้องและชื่อไฟล์ DWG ถูกต้อง. |
| **ผลลัพธ์ PDF ว่าง** | ตรวจสอบว่าชื่อเลเอาต์ (`"Layout1"`) มีอยู่ในไฟล์ DWG; ใช้ `image.getAvailableLayouts()` เพื่อแสดงรายการ. |
| **คุณภาพภาพต่ำ** | เพิ่มค่า `PageWidth` และ `PageHeight` หรือกำหนด `rasterizationOptions.setResolution(300);`. |

## คำถามที่พบบ่อย

### Q1: ฉันสามารถเรนเดอร์หลายเลเอาต์จากไฟล์ DWG เดียวได้หรือไม่?

A1: ได้, คุณสามารถทำได้ เพียงปรับชื่อเลเอาต์ในอาร์เรย์ `setLayouts` ตามต้องการ.

### Q2: Aspose.CAD รองรับ IDE Java ต่าง ๆ หรือไม่?

A2: ใช่, Aspose.CAD รองรับ IDE Java ยอดนิยมเช่น Eclipse, IntelliJ IDEA และอื่น ๆ.

### Q3: ฉันจะหาแหล่งช่วยเหลือและสนับสนุนเพิ่มเติมได้จากที่ไหน?

A3: เยี่ยมชม [Aspose.CAD forum](https://forum.aspose.com/c/cad/19) เพื่อรับการสนับสนุนจากชุมชนและการสนทนา.

### Q4: ฉันจะขอรับไลเซนส์ชั่วคราวสำหรับ Aspose.CAD ได้อย่างไร?

A4: คุณสามารถรับไลเซนส์ชั่วคราวได้จาก [here](https://purchase.aspose.com/temporary-license/).

### Q5: มีตัวเลือกการเรนเดอร์เพิ่มเติมใน Aspose.CAD หรือไม่?

A5: แน่นอน, สำรวจ [documentation](https://reference.aspose.com/cad/java/) อย่างละเอียดเพื่อข้อมูลเพิ่มเติม.

---

**อัปเดตล่าสุด:** 2025-12-28  
**ทดสอบกับ:** Aspose.CAD for Java 24.11  
**ผู้เขียน:** Aspose  

---

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}
