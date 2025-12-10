---
date: 2025-12-10
description: เรียนรู้วิธีสร้าง PDF จาก CAD ด้วย Aspose.CAD for Java พร้อม Auto Layout
  Scaling คู่มือขั้นตอนนี้จะแสดงให้คุณเห็นวิธีส่งออก CAD ไปเป็น PDF อย่างมีประสิทธิภาพและเชื่อถือได้
linktitle: Setting Auto Layout Scaling
second_title: Aspose.CAD Java API
title: สร้าง PDF จาก CAD – ปรับสเกลการจัดวางอัตโนมัติด้วย Aspose.CAD Java
url: /th/java/advanced-cad-features/setting-auto-layout-scaling/
weight: 17
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# สร้าง PDF จาก CAD – Auto Layout Scaling ด้วย Aspose.CAD Java

## บทนำ

หากคุณต้องการ **สร้าง PDF จาก CAD** อย่างรวดเร็วและมีการปรับขนาดที่สมบูรณ์แบบ Aspose.CAD สำหรับ Java มีให้คุณใช้งาน Auto Layout Scaling จะปรับขนาดมิติของเลย์เอาต์โดยอัตโนมัติเพื่อให้ PDF ที่ได้ดูตรงตามที่ต้องการโดยไม่คำนึงถึงขนาดหน้าต้นฉบับของ CAD ในบทเรียนนี้เราจะอธิบายขั้นตอนทั้งหมดตั้งแต่การโหลดไฟล์ DXF ไปจนถึงการส่งออกเป็น PDF พร้อมเน้นความสามารถ **export CAD to PDF** ของไลบรารี

## คำตอบสั้น
- **Auto Layout Scaling ทำอะไร?** มันจะปรับขนาดเลย์เอาต์ของ CAD โดยอัตโนมัติเพื่อให้พอดีกับมิติของหน้าที่ต้องการเมื่อทำการแรสเตอร์ไลซ์
- **ฉันสามารถแปลงรูปแบบใดได้บ้าง?** รูปแบบใดก็ได้ที่ Aspose.CAD รองรับ (เช่น DXF, DWG, DWF) สามารถแปลงเป็น PDF ได้
- **ฉันต้องการไลเซนส์สำหรับการใช้งานจริงหรือไม่?** ใช่ จำเป็นต้องมีไลเซนส์เชิงพาณิชย์สำหรับการใช้งานที่ไม่ใช่การประเมินผล
- **การแปลงใช้เวลานานเท่าไหร่?** โดยทั่วไปใช้เวลาน้อยกว่าวินาทีหนึ่งสำหรับไฟล์มาตรฐานบนฮาร์ดแวร์สมัยใหม่
- **ฉันสามารถเปลี่ยนขนาดหน้าได้หรือไม่?** ใช่ คุณสามารถตั้งค่ามิติหน้าที่กำหนดเองได้ผ่าน `CadRasterizationOptions`

## “สร้าง PDF จาก CAD” คืออะไร?
การสร้าง PDF จาก CAD หมายถึงการนำภาพวาดวิศวกรรมแบบเวกเตอร์ (DXF, DWG ฯลฯ) มาทำการแรสเตอร์ไลซ์เป็นเอกสาร PDF PDF จะคงความแม่นยำของภาพต้นฉบับไว้ในขณะที่สามารถดูได้บนทุกแพลตฟอร์ม

## ทำไมต้องใช้ Auto Layout Scaling?
- **ผลลัพธ์สม่ำเสมอ:** รับประกันว่าเลย์เอาต์ทั้งหมดจะเติมเต็มหน้า PDF โดยไม่ต้องคำนวณขนาดด้วยตนเอง
- **ประหยัดเวลา:** ไม่ต้องปรับสเกลด้วยตนเองสำหรับแต่ละภาพวาด
- **คุณภาพสูง:** รักษาน้ำหนักเส้นและความแม่นยำของเรขาคณิตระหว่างการแปลง

## ข้อกำหนดเบื้องต้น

1. **Aspose.CAD for Java Library** – ดาวน์โหลดเวอร์ชันล่าสุดจาก [download page](https://releases.aspose.com/cad/java/).  
2. **Resource Directory** – สร้างโฟลเดอร์บนเครื่องของคุณเพื่อเก็บไฟล์ CAD; แทนที่ `"Your Document Directory"` ในโค้ดด้วยเส้นทางนั้น  
3. **Sample CAD File** – สำหรับคู่มือนี้เราจะใช้ไฟล์ `conic_pyramid.dxf` ซึ่งรวมอยู่ในชุดข้อมูลตัวอย่างของ Aspose  

## นำเข้า Namespaces
แรกเริ่มให้ทำการนำเข้าคลาสที่จำเป็น ซึ่งจะทำให้เราเข้าถึงการโหลดภาพ, การแรสเตอร์ไลซ์, และฟีเจอร์การส่งออก PDF  

```java
import com.aspose.cad.Image;

import com.aspose.cad.imageoptions.CadRasterizationOptions;
import com.aspose.cad.imageoptions.PdfOptions;
```

## ขั้นตอนที่ 1: โหลดไฟล์ CAD
การโหลดไฟล์ต้นฉบับเป็นขั้นตอนแรกใน **วิธีการ export CAD** ไปยังเอกสาร PDF  

```java
String srcFile = dataDir + "conic_pyramid.dxf";
Image image = Image.load(srcFile);
```

## ขั้นตอนที่ 2: สร้าง Rasterization Options
กำหนดมิติของหน้าที่ต้องการ คุณยังสามารถใช้บล็อกนี้เพื่อ **ตั้งค่าขนาดหน้าของ CAD** ด้วยตนเองหากต้องการเลย์เอาต์ที่กำหนดเอง  

```java
CadRasterizationOptions rasterizationOptions = new CadRasterizationOptions();
rasterizationOptions.setPageWidth(1600);
rasterizationOptions.setPageHeight(1600);
```

## ขั้นตอนที่ 3: ตั้งค่า Auto Layout Scaling
เปิดใช้งานฟีเจอร์การปรับสเกลอัตโนมัติ นี่คือหัวใจของ **วิธีการตั้งค่าสเกล** สำหรับการแปลง CAD‑to‑PDF  

```java
rasterizationOptions.setAutomaticLayoutsScaling(true);
```

## ขั้นตอนที่ 4: สร้าง PDF Options
เชื่อมการตั้งค่าแรสเตอร์ไลซ์กับตัวเลือกการส่งออก PDF  

```java
PdfOptions pdfOptions = new PdfOptions();
pdfOptions.setVectorRasterizationOptions(rasterizationOptions);
```

## ขั้นตอนที่ 5: ส่งออกเป็น PDF
สุดท้ายให้บันทึกภาพที่เรนเดอร์เป็นไฟล์ PDF ขั้นตอนนี้จะทำให้กระบวนการ **convert DXF to PDF** เสร็จสมบูรณ์  

```java
image.save(dataDir + "result_out_.pdf", pdfOptions);
```

ทำซ้ำขั้นตอนข้างต้นสำหรับไฟล์ CAD เพิ่มเติมที่คุณต้องการประมวลผล

## ปัญหาที่พบบ่อยและการแก้ไข

| อาการ | สาเหตุที่เป็นไปได้ | วิธีแก้ |
|---------|--------------|-----|
| PDF ว่างเปล่า | ไม่ได้ตั้งค่า Rasterization options หรือเส้นทางไฟล์ไม่ถูกต้อง | ตรวจสอบเส้นทาง `srcFile` และให้แน่ใจว่า `setPageWidth/Height` ไม่เป็นศูนย์ |
| สเกลผิดรูป | `setAutomaticLayoutsScaling` ถูกตั้งเป็น `false` | เปิดใช้งานการสเกลอัตโนมัติหรือคำนวณสเกลด้วยตนเอง |
| เลเยอร์หายไป | ไฟล์ DXF ต้นฉบับมีเอนทิตีที่ไม่รองรับ | ตรวจสอบบันทึกการปล่อยของ Aspose.CAD เพื่อดูประเภทเอนทิตีที่รองรับ |

## คำถามที่พบบ่อย

### Q1: Aspose.CAD for Java รองรับรูปแบบไฟล์ CAD ทั้งหมดหรือไม่?
A1: Aspose.CAD for Java รองรับรูปแบบ CAD หลากหลายรวมถึง DWG, DXF, และ DWF.

### Q2: ฉันสามารถปรับแต่งตัวเลือกการสเกลเพิ่มเติมได้หรือไม่?
A2: ใช่ คลาส `CadRasterizationOptions` มีคุณสมบัติต่าง ๆ สำหรับการปรับสเกลและการตั้งค่าอื่น ๆ อย่างละเอียด

### Q3: ฉันจะหาเอกสารเพิ่มเติมสำหรับ Aspose.CAD for Java ได้จากที่ไหน?
A3: ดูที่ [documentation](https://reference.aspose.com/cad/java/) เพื่อรับข้อมูลเชิงลึกและตัวอย่าง

### Q4: มีการทดลองใช้ฟรีสำหรับ Aspose.CAD for Java หรือไม่?
A4: มี คุณสามารถลองใช้ [free trial](https://releases.aspose.com/) เพื่อสัมผัสความสามารถของ Aspose.CAD for Java

### Q5: ฉันจะขอความช่วยเหลือหรือเข้าร่วมการสนทนาเกี่ยวกับ Aspose.CAD for Java อย่างไร?
A5: เยี่ยมชม [Aspose.CAD forum](https://forum.aspose.com/c/cad/19) เพื่อเชื่อมต่อกับชุมชนและขอรับการสนับสนุน

**คำถามทั่วไปเพิ่มเติม**

**Q: ฉันจะแปลงไฟล์ DWG เป็น PDF แทน DXF อย่างไร?**  
A: โค้ดเดียวกันทำงานได้; เพียงเปลี่ยนส่วนขยายไฟล์ใน `srcFile` เป็น `.dwg`.

**Q: ฉันสามารถตั้งค่า DPI ที่กำหนดเองเพื่อให้ PDF มีความละเอียดสูงขึ้นได้หรือไม่?**  
A: ใช่ ใช้ `rasterizationOptions.setResolution(300);` (หรือ DPI ใด ๆ ที่คุณต้องการ).

**Q: สามารถฝังฟอนต์ใน PDF ที่สร้างขึ้นได้หรือไม่?**  
A: Aspose.CAD ทำการแรสเตอร์ไลซ์ภาพวาด ดังนั้นฟอนต์จะถูกเรนเดอร์เป็นเวกเตอร์; ไม่จำเป็นต้องฝังฟอนต์แยกต่างหาก.

## สรุป
โดยทำตามคู่มือนี้คุณจะรู้วิธี **สร้าง PDF จาก CAD** ด้วย Aspose.CAD for Java พร้อม Auto Layout Scaling กระบวนการนี้ทำให้การทำงาน **export CAD to PDF** ราบรื่นขึ้น, รับประกันการสเกลที่สม่ำเสมอ, และช่วยประหยัดเวลาการพัฒนาที่มีค่า คุณสามารถทดลองใช้ขนาดหน้า, ความละเอียด, และรูปแบบ CAD ต่าง ๆ เพื่อให้เหมาะกับความต้องการของโครงการของคุณ

---

**อัปเดตล่าสุด:** 2025-12-10  
**ทดสอบด้วย:** Aspose.CAD for Java 24.12 (latest)  
**ผู้เขียน:** Aspose  

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}