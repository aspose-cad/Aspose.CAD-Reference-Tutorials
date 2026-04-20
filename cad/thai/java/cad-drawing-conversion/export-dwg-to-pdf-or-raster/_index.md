---
date: 2026-02-17
description: เรียนรู้วิธีที่ไลบรารี CAD สำหรับ Java อย่าง Aspose.CAD for Java สามารถส่งออกไฟล์
  DWG ไปเป็น PDF หรือภาพเรสเตอร์ได้อย่างรวดเร็วและแม่นยำ.
linktitle: Export DWG to PDF or Raster
second_title: Aspose.CAD Java API
title: ส่งออก DWG เป็น PDF หรือ Raster ด้วยไลบรารี CAD ของ Java Aspose.CAD สำหรับ
  Java
url: /th/java/cad-drawing-conversion/export-dwg-to-pdf-or-raster/
weight: 13
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# ส่งออก DWG เป็น PDF หรือ Raster ด้วยไลบรารี java cad Aspose.CAD for Java

## บทนำ

ในโลกที่เปลี่ยนแปลงอย่างรวดเร็วของการออกแบบด้วยคอมพิวเตอร์ (CAD) การจัดการแบบร่างอย่างมีประสิทธิภาพเป็นสิ่งสำคัญ ด้วย **java cad library** **Aspose.CAD for Java** คุณสามารถ **export dwg to pdf** — หรือภาพ raster — ได้เพียงไม่กี่บรรทัดของโค้ด บทเรียนนี้จะพาคุณผ่านกระบวนการทั้งหมด ตั้งแต่การโหลดไฟล์ DWG จนถึงการสร้าง PDF คุณภาพสูง พร้อมอธิบายเหตุผลที่ทำให้ Aspose.CAD Java เป็นไลบรารีที่เลือกใช้สำหรับงานแปลง CAD

## คำตอบด่วน
- **What does this tutorial cover?** การส่งออกไฟล์ DWG เป็น PDF หรือภาพ raster ด้วย Aspose.CAD for Java  
- **Do I need a license?** มีใบอนุญาตชั่วคราวฟรีสำหรับการประเมิน; จำเป็นต้องมีใบอนุญาตเต็มสำหรับการใช้งานจริง  
- **Which Java version is supported?** รองรับ Java 8+ ทุกเวอร์ชันกับ API Aspose.CAD Java ล่าสุด  
- **Can I convert DWG to other image formats?** ได้ – ตัวเลือก rasterization เดียวกันช่วยให้คุณส่งออกเป็น PNG, JPEG, BMP ฯลฯ  
- **How long does the conversion take?** ปกติใช้เวลาน้อยกว่า 1 วินาทีสำหรับแบบร่างมาตรฐาน; ไฟล์ขนาดใหญ่อาจใช้หลายวินาที

## ทำไม java cad library จึงเป็นตัวเลือกที่ดีที่สุดสำหรับการแปลง DWG?

- **Pure Java implementation** – ไม่ต้องใช้ DLL หรือเครื่องมือภายนอก  
- **Accurate unit handling** – ตรวจจับหน่วยเมตริกและอิมพีเรียลโดยอัตโนมัติ  
- **High‑quality raster output** – ควบคุม DPI และขนาดหน้าอย่างละเอียด  
- **Full PDF support** – สร้าง PDF ที่รักษาเวกเตอร์ได้โดยไม่มีการพึ่งพาไลบรารีเพิ่มเติม  
- **Flexible licensing** – เริ่มต้นด้วย **temporary license aspose** สำหรับการทดสอบ, แล้วอัปเกรดเมื่อใช้งานจริง

## “export dwg to pdf” คืออะไร?

การส่งออก DWG เป็น PDF หมายถึงการแปลงแบบร่าง AutoCAD ดั้งเดิมให้เป็นเอกสาร PDF ที่พกพาได้และอิสระจากอุปกรณ์ PDF ที่สร้างขึ้นจะคงข้อมูลเวกเตอร์, ชั้น, และสเกลไว้ ทำให้เหมาะสำหรับการแชร์, พิมพ์, หรือเก็บรักษา

## ทำไมต้องใช้ Aspose.CAD Java สำหรับการแปลงนี้?

เพราะ **java cad library** จัดการทุกอย่างตั้งแต่การแปลงหน่วยจนถึงการ rasterization ภายใน ทำให้คุณไม่ต้องพึ่งพาเครื่องมือของบุคคลที่สามและได้ผลลัพธ์ที่สม่ำเสมอข้ามแพลตฟอร์ม

## ข้อกำหนดเบื้องต้น

ก่อนเริ่มเขียนโค้ด ให้ตรวจสอบว่าคุณมี:

- ความรู้พื้นฐานด้านการเขียนโปรแกรม Java  
- ไลบรารี Aspose.CAD for Java ติดตั้งแล้ว หากยังไม่ได้ดาวน์โหลด สามารถรับได้จาก **[here](https://releases.aspose.com/cad/java/)**  
- ไฟล์ DWG สำหรับทดสอบ – ตัวอย่าง **Bottom_plate.dwg** จะใช้ในคู่มือนี้

## นำเข้า Namespaces

ในโปรเจกต์ Java ของคุณ ให้นำเข้าคลาสที่จำเป็นเพื่อเริ่มกระบวนการแปลง:

```java
import com.aspose.cad.Image;

import com.aspose.cad.imageoptions.CadRasterizationOptions;
import com.aspose.cad.imageoptions.PdfOptions;
import com.aspose.cad.imageoptions.UnitType;
```

## คู่มือขั้นตอนโดยละเอียด

### ขั้นตอนที่ 1: โหลดไฟล์ DWG

แรกเริ่มให้โหลดแบบร่าง DWG ของคุณด้วยคลาส `Image` ซึ่งจะสร้างออบเจ็กต์ในหน่วยความจำที่ Aspose.CAD สามารถทำงานได้

```java
String dataDir = "Your Document Directory" + "DWGDrawings/";
String srcFile = dataDir + "Bottom_plate.dwg";
Image objImage = Image.load(srcFile);
```

### ขั้นตอนที่ 2: กำหนดประเภทหน่วย

การรู้ว่าแบบร่างใช้หน่วยเมตริกหรืออิมพีเรียลเป็นสิ่งสำคัญสำหรับการสเกลที่ถูกต้อง เมธอดช่วยเหลือ `IsMetric` (การทำงานไม่ได้แสดงในที่นี้) จะคืนค่า boolean

```java
Boolean currentUnitIsMetric = IsMetric(objImage.getUnitType());
int currentUnitCoefficient = objImage.getUnitType();
```

### ขั้นตอนที่ 3: ตั้งค่า Rasterization Options

อิงตามระบบหน่วย ให้กำหนดขนาดหน้า, การสเกล, และประเภทหน่วยเป้าหมาย ตัวเลือกเหล่านี้จะกำหนดวิธีที่ DWG ถูก rasterize ก่อนจะถูกบรรจุลงใน PDF

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

### ขั้นตอนที่ 4: กำหนดค่า PDF Options (pdf options cad)

สร้างอินสแตนซ์ `PdfOptions` แล้วแนบการตั้งค่า rasterization นี้ให้กับมัน เพื่อบอก Aspose.CAD ว่าจะฝังเนื้อหา rasterized ลงใน PDF อย่างไร

```java
PdfOptions pdfOptions = new PdfOptions();
pdfOptions.setVectorRasterizationOptions(new CadRasterizationOptions());
```

### ขั้นตอนที่ 5: บันทึกเป็น PDF

สุดท้ายให้ส่งออกแบบร่างเป็นไฟล์ PDF เมธอด `save` รับพาธไฟล์ผลลัพธ์และ `PdfOptions` ที่กำหนดไว้

```java
objImage.save(dataDir + "Saved.pdf", pdfOptions);
```

เมื่อโค้ดทำงานเสร็จ คุณจะพบ **Saved.pdf** ในโฟลเดอร์ `DWGDrawings` ของคุณ พร้อมสำหรับการแจกจ่ายหรือเก็บรักษา

## วิธีแปลงภาพ raster dwg ด้วย java cad library

หากต้องการภาพ raster แทน PDF เพียงเปลี่ยน `PdfOptions` เป็นตัวเลือกภาพ raster ที่เหมาะสม (เช่น `PngOptions`, `JpegOptions`) อินสแตนซ์ `CadRasterizationOptions` เดิมสามารถใช้ซ้ำได้ ทำให้คุณ **convert dwg raster** ได้ด้วยการแก้ไขโค้ดเพียงเล็กน้อย

## วิธีสร้าง pdf dwg ด้วย pdf options cad

ตัวอย่างข้างต้นได้ **generates pdf dwg** แล้ว คุณสามารถปรับ `pdfOptions` เช่น `pdfOptions.setCompress(true)` เพื่อควบคุมขนาดและคุณภาพของ PDF ได้ ซึ่งแสดงถึงความยืดหยุ่นของ API **pdf options cad**

## ปัญหาและเคล็ดลับทั่วไป

- **Incorrect page size** – ตรวจสอบตรรกะการแปลงหน่วยอีกครั้ง; ค่าสัมประสิทธิ์ที่ไม่ตรงกันอาจทำให้หน้ามีขนาดใหญ่เกินไป  
- **Missing fonts or lineweights** – ตรวจสอบให้แน่ใจว่า DWG อ้างอิงทรัพยากรภายนอกทั้งหมดก่อนทำการแปลง  
- **Performance on large drawings** – เพิ่มค่า `DPI` ใน `CadRasterizationOptions` เฉพาะเมื่อต้องการคุณภาพสูง; ค่า DPI ต่ำจะทำให้ประมวลผลเร็วขึ้น  
- **License concerns** – สำหรับการประเมินคุณสามารถใช้ **temporary license aspose**; จำเป็นต้องมีใบอนุญาตเต็มสำหรับการใช้งานในผลิตภัณฑ์

## คำถามที่พบบ่อย

**Q: Can I use Aspose.CAD for Java with other Java frameworks?**  
A: ใช่, Aspose.CAD for Java สามารถรวมกับเฟรมเวิร์ก Java ยอดนิยมเช่น Spring, Jakarta EE, และ Android ได้อย่างราบรื่น  

**Q: Is a temporary license available for Aspose.CAD for Java?**  
A: มี คุณสามารถรับใบอนุญาตชั่วคราว **[here](https://purchase.aspose.com/temporary-license/)**  

**Q: Where can I find support for Aspose.CAD for Java?**  
A: เยี่ยมชม **[Aspose.CAD forum](https://forum.aspose.com/c/cad/19)** เพื่อรับความช่วยเหลือจากชุมชนและวิศวกรของ Aspose  

**Q: How can I purchase a license for Aspose.CAD for Java?**  
A: คุณสามารถซื้อใบอนุญาต **[here](https://purchase.aspose.com/buy)**  

**Q: What units does Aspose.CAD for Java support?**  
A: Aspose.CAD for Java รองรับทั้งหน่วยเมตริกและอิมพีเรียล โดยตรวจจับระบบหน่วยของแบบร่างโดยอัตโนมัติ  

**Q: Can I convert DWG to other image formats (e.g., PNG, JPEG) using the same API?**  
A: แน่นอน. แทนที่ `PdfOptions` ด้วยตัวเลือกภาพ raster ที่เหมาะสม (เช่น `PngOptions`) แล้วใช้ `CadRasterizationOptions` เดิมต่อไป

## สรุป

บทเรียนนี้ได้สาธิตวิธี **export dwg to pdf** และภาพ raster ด้วย **java cad library** Aspose.CAD for Java โดยทำตามขั้นตอนที่อธิบาย คุณสามารถผสานการแปลง CAD ที่เชื่อถือได้เข้าไปในแอปพลิเคชัน Java ใดก็ได้ ไม่ว่าจะต้องการ PDF สำหรับเอกสารหรือภาพ raster สำหรับการแสดงบนเว็บ

---

**อัปเดตล่าสุด:** 2026-02-17  
**ทดสอบกับ:** Aspose.CAD for Java 24.10  
**ผู้เขียน:** Aspose  

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}