---
date: 2026-02-15
description: เรียนรู้วิธีตั้งค่าขนาดหน้ากระดาษแบบกำหนดเองและสร้างไฟล์ PDF จาก CAD
  ด้วย Aspose.CAD for Java คู่มือขั้นตอนต่อขั้นตอนนี้ครอบคลุมการส่งออก CAD เป็น PDF
  พร้อมการปรับสเกลอัตโนมัติของเลย์เอาต์
linktitle: Setting Auto Layout Scaling
second_title: Aspose.CAD Java API
title: ตั้งค่าขนาดหน้ากระดาษแบบกำหนดเอง – PDF จาก CAD พร้อมการปรับสเกลอัตโนมัติของเลย์เอาต์
url: /th/java/advanced-cad-features/setting-auto-layout-scaling/
weight: 17
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# ตั้งค่าขนาดหน้ากระดาษแบบกำหนดเอง – สร้าง PDF จาก CAD ด้วย Auto Layout Scaling

## บทนำ

หากคุณต้องการ **set custom page size** ขณะ **create PDF from CAD** อย่างรวดเร็วและมีการสเกลที่สมบูรณ์แบบ Aspose.CAD for Java จะช่วยคุณได้ Auto Layout Scaling จะปรับขนาดมิติของเลย์เอาต์โดยอัตโนมัติเพื่อให้ PDF ที่ได้ตรงตามที่ต้องการโดยไม่คำนึงถึงขนาดหน้ากระดาษ CAD ดั้งเดิม ในบทแนะนำนี้เราจะเดินผ่านกระบวนการทั้งหมด—from การโหลดไฟล์ DXF ไปจนถึงการส่งออกเป็น PDF—พร้อมเน้นความสามารถ **export CAD to PDF** ของไลบรารีและแสดงวิธีที่คุณสามารถ **convert DWG to PDF** หรือ **increase PDF resolution** เมื่อจำเป็น

## คำตอบอย่างรวดเร็ว
- **Auto Layout Scaling ทำอะไร?** It automatically resizes CAD layouts to fit the target page dimensions when rasterizing.
- **รูปแบบใดบ้างที่ฉันสามารถแปลงได้?** Any format supported by Aspose.CAD (e.g., DXF, DWG, DWF) can be converted to PDF.
- **ฉันต้องมีลิขสิทธิ์สำหรับการใช้งานจริงหรือไม่?** Yes, a commercial license is required for non‑evaluation use.
- **การแปลงใช้เวลานานแค่ไหน?** Typically under a second for standard files on modern hardware.
- **ฉันสามารถเปลี่ยนขนาดหน้ากระดาษได้หรือไม่?** Yes, you can set custom page dimensions via `CadRasterizationOptions`.

## อะไรคือ “create PDF from CAD”?

การสร้าง PDF จาก CAD หมายถึงการนำภาพวาดวิศวกรรมแบบเวกเตอร์ (DXF, DWG ฯลฯ) มาราสเตอร์ไทซ์เป็นเอกสาร PDF PDF จะคงความละเอียดของภาพวาดต้นฉบับไว้ในขณะที่สามารถเปิดดูได้บนทุกแพลตฟอร์ม

## ทำไมต้องใช้ Auto Layout Scaling?

- **Consistent output:** Guarantees that all layouts fill the PDF page without manual size calculations.
- **Time‑saving:** Eliminates the need to manually adjust scaling factors for each drawing.
- **High quality:** Maintains line weight and geometry accuracy during conversion.
- **Flexibility:** Works for **convert dxf to pdf**, **convert dwg to pdf**, and even when you need to **increase PDF resolution** for print‑ready files.

## ข้อกำหนดเบื้องต้น

1. **Aspose.CAD for Java Library** – ดาวน์โหลดเวอร์ชันล่าสุดจาก [หน้าโหลด](https://releases.aspose.com/cad/java/).  
2. **Resource Directory** – สร้างโฟลเดอร์บนเครื่องของคุณเพื่อเก็บไฟล์ CAD; แทนที่ `"Your Document Directory"` ในโค้ดด้วยเส้นทางนั้น.  
3. **Sample CAD File** – สำหรับคู่มือนี้เราจะใช้ `conic_pyramid.dxf` ซึ่งรวมอยู่ในชุดข้อมูลตัวอย่างของ Aspose

## นำเข้า Namespaces

ก่อนอื่นให้ทำการนำเข้าคลาสที่จำเป็น ซึ่งจะทำให้เราสามารถเข้าถึงฟีเจอร์การโหลดภาพ, ราสเตอร์ไทซ์, และการส่งออกเป็น PDF ได้

```java
import com.aspose.cad.Image;

import com.aspose.cad.imageoptions.CadRasterizationOptions;
import com.aspose.cad.imageoptions.PdfOptions;
```

## วิธีตั้งค่าขนาดหน้ากระดาษแบบกำหนดเองสำหรับ PDF จาก CAD

ก่อนที่เราจะลงลึกในโค้ดขั้นตอนต่อขั้นตอน ให้เข้าใจว่าการตั้งค่าขนาดหน้ากระดาษแบบกำหนดเองมีความสำคัญอย่างไร เมื่อคุณ **set custom page size** คุณจะควบคุมมิติจริงของ PDF ที่ได้ (เช่น A4, Letter หรือขนาดที่กำหนดเอง) ซึ่งเป็นสิ่งจำเป็นสำหรับกระบวนการวิศวกรรมที่ต้องการให้ภาพวาดตรงตามมาตรฐานแผ่นหรือเมื่อคุณต้องฝัง PDF ลงในเอกสารที่ใหญ่กว่า

### ขั้นตอนที่ 1: โหลดไฟล์ CAD

การโหลดไฟล์ต้นทางเป็นขั้นตอนแรกใน **how to export CAD** ไปยังเอกสาร PDF

```java
String srcFile = dataDir + "conic_pyramid.dxf";
Image image = Image.load(srcFile);
```

### ขั้นตอนที่ 2: สร้าง Rasterization Options

กำหนดมิติของหน้ากระดาษเป้าหมาย คุณยังสามารถใช้บล็อกนี้เพื่อ **set CAD page size** ด้วยตนเองหากต้องการเลย์เอาต์แบบกำหนดเอง

```java
CadRasterizationOptions rasterizationOptions = new CadRasterizationOptions();
rasterizationOptions.setPageWidth(1600);
rasterizationOptions.setPageHeight(1600);
```

### ขั้นตอนที่ 3: ตั้งค่า Auto Layout Scaling

เปิดใช้งานฟีเจอร์การสเกลอัตโนมัติ นี่คือหัวใจของ **how to set scaling** สำหรับการแปลง CAD‑to‑PDF

```java
rasterizationOptions.setAutomaticLayoutsScaling(true);
```

### ขั้นตอนที่ 4: สร้าง PDF Options

เชื่อมการตั้งค่าราสเตอร์ไทซ์กับตัวเลือกการส่งออก PDF

```java
PdfOptions pdfOptions = new PdfOptions();
pdfOptions.setVectorRasterizationOptions(rasterizationOptions);
```

### ขั้นตอนที่ 5: ส่งออกเป็น PDF

สุดท้ายให้บันทึกภาพที่เราสร้างเป็นไฟล์ PDF ขั้นตอนนี้ทำให้เวิร์กโฟลว์ **convert dxf to pdf** เสร็จสมบูรณ์

```java
image.save(dataDir + "result_out_.pdf", pdfOptions);
```

ทำซ้ำขั้นตอนข้างต้นสำหรับไฟล์ CAD ใด ๆ ที่คุณต้องการประมวลผลเพิ่มเติม ไม่ว่าจะเป็น **DWG**, **DWF** หรือรูปแบบที่รองรับอื่น ๆ

## กรณีการใช้งานทั่วไป

| Scenario | ทำไมต้องตั้งค่าขนาดหน้ากระดาษแบบกำหนดเอง? |
|----------|--------------------------------------------|
| **Construction drawing submission** | Aligns the PDF with standard A1/A2 sheet sizes required by regulatory bodies. |
| **Embedding in technical manuals** | Guarantees the drawing fits the predefined layout of the manual without extra scaling. |
| **High‑resolution printing** | Allows you to increase DPI (e.g., `rasterizationOptions.setResolution(300)`) while keeping the page dimensions consistent. |

## ปัญหาทั่วไปและการแก้ไข

| Symptom | Likely Cause | Fix |
|---------|--------------|-----|
| Blank PDF output | Rasterization options not set or file path incorrect | Verify `srcFile` path and ensure `setPageWidth/Height` are non‑zero |
| Distorted scaling | `setAutomaticLayoutsScaling` left as `false` | Enable automatic scaling or manually calculate scaling factor |
| Missing layers | Source DXF contains unsupported entities | Check the Aspose.CAD release notes for supported entity types |

## คำถามที่พบบ่อย

**Q: Aspose.CAD for Java รองรับรูปแบบไฟล์ CAD ทั้งหมดหรือไม่?**  
A: Aspose.CAD for Java supports various CAD formats, including DWG, DXF, and DWF.

**Q: ฉันสามารถปรับแต่งตัวเลือกการสเกลเพิ่มเติมได้หรือไม่?**  
A: Yes, the `CadRasterizationOptions` class provides properties for fine‑tuning scaling, DPI, and other rasterization settings.

**Q: ฉันจะหาเอกสารเพิ่มเติมเกี่ยวกับ Aspose.CAD for Java ได้จากที่ไหน?**  
A: Refer to the [documentation](https://reference.aspose.com/cad/java/) for in‑depth information and examples.

**Q: มีการทดลองใช้ฟรีสำหรับ Aspose.CAD for Java หรือไม่?**  
A: Yes, you can explore a [free trial](https://releases.aspose.com/) to experience the capabilities of Aspose.CAD for Java.

**Q: ฉันจะขอความช่วยเหลือหรือเข้าร่วมการสนทนาเกี่ยวกับ Aspose.CAD for Java ได้อย่างไร?**  
A: Visit the [Aspose.CAD forum](https://forum.aspose.com/c/cad/19) to connect with the community and seek support.

### คำถามเพิ่มเติมทั่วไป

**Q: ฉันจะแปลงไฟล์ DWG เป็น PDF แทน DXF อย่างไร?**  
A: The same code works; just change the file extension in `srcFile` to `.dwg`.

**Q: ฉันสามารถตั้งค่า DPI แบบกำหนดเองสำหรับ PDF ความละเอียดสูงได้หรือไม่?**  
A: Yes, use `rasterizationOptions.setResolution(300);` (or any DPI you need).

**Q: สามารถฝังฟอนต์ใน PDF ที่สร้างขึ้นได้หรือไม่?**  
A: Aspose.CAD rasterizes the drawing, so fonts are rendered as vectors; no separate font embedding is required.

## สรุป

ด้วยการทำตามคู่มือนี้คุณจะรู้วิธี **set custom page size** และ **create PDF from CAD** ด้วย Aspose.CAD for Java พร้อม Auto Layout Scaling กระบวนการนี้ทำให้เวิร์กโฟลว์ **export CAD to PDF** มีความสม่ำเสมอในการสเกลและช่วยประหยัดเวลาการพัฒนาอย่างมาก อย่าลังเลที่จะทดลองขนาดหน้ากระดาษ, ความละเอียด, และรูปแบบ CAD ต่าง ๆ เพื่อให้ตรงกับความต้องการของโครงการ ไม่ว่าจะเป็น **converting DWG to PDF**, **increasing PDF resolution**, หรือการสร้าง **java CAD to PDF** batch processor

---

**อัปเดตล่าสุด:** 2026-02-15  
**ทดสอบด้วย:** Aspose.CAD for Java 24.12 (latest)  
**ผู้เขียน:** Aspose  

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}