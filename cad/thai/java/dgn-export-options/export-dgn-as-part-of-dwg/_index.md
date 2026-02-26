---
date: 2026-01-10
description: เรียนรู้วิธีการส่งออกไฟล์ DGN เป็น DWG และแปลงไฟล์ MicroStation DGN เป็น
  AutoCAD DWG ด้วย Aspose.CAD สำหรับ Java คู่มือแบบขั้นตอนต่อขั้นตอน
linktitle: Export DGN as Part of DWG
second_title: Aspose.CAD Java API
title: ส่งออก DGN ไปเป็น DWG ด้วย Aspose.CAD สำหรับ Java
url: /th/java/dgn-export-options/export-dgn-as-part-of-dwg/
weight: 10
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# ส่งออก DGN เป็น DWG ด้วย Aspose.CAD สำหรับ Java

## คำแนะนำ

ในบทแนะนำนี้ คุณจะได้เรียนรู้วิธี **export dgn to dwg** และฝังการออกแบบ MicroStation DGN ไว้ในไฟล์ AutoCAD DWG โดยใช้ไลบรารี Aspose.CAD สำหรับ Java ไม่ว่าคุณจะกำลังย้ายแบบภาพ MicroStation รุ่นเก่าหรือจำเป็นต้องรวม DGN underlay กับเลย์เอาต์ DWG คู่มือนี้จะพาคุณผ่านทุกขั้นตอน ตั้งแต่การตั้งค่าสภาพแวดล้อมจนถึงการสร้างตัวอย่าง PDF ของ DWG สุดท้าย

## คำตอบอย่างรวดเร็ว
- **What does “export dgn to dwg” achieve?** It embeds a DGN underlay into a DWG, enabling seamless viewing in AutoCAD.
- **Which format can I export the result to for quick preview?** You can **export cad file to pdf** using `PdfOptions`.
- **Do I need a license to run the code?** A temporary or paid Aspose.CAD license is required for production use.
- **What Java version is supported?** Java 8 or later works with the latest Aspose.CAD for Java release.
- **Is there a free trial available?** Yes – download a trial from the Aspose website.

## “export dgn to dwg” คืออะไร?
การส่งออก DGN ไปเป็น DWG หมายถึงการแปลงหรือฝังการออกแบบ MicroStation DGN เป็น underlay ภายในภาพวาด AutoCAD DWG ซึ่งช่วยให้ผู้เชี่ยวชาญ CAD สามารถใช้ประโยชน์จากทรัพย์สิน DGN ที่มีอยู่โดยไม่ต้องสร้างเรขาคณิตใหม่ตั้งแต่ต้น.

## ทำไมต้องแปลง MicroStation DGN เป็น AutoCAD DWG?
- **Collaboration:** ทีมที่ใช้ AutoCAD สามารถดูและแก้ไขเนื้อหา DGN ได้โดยตรง.
- **Standardization:** DWG เป็นรูปแบบมาตรฐานสำหรับกระบวนการต่อเนื่องหลายอย่าง (เช่น การสร้าง PDF, การเรนเดอร์ 3 มิติ).
- **Preservation:** รักษาการอ้างอิง DGN ดั้งเดิมไว้ไม่เสียหาย ลดการสูญเสียข้อมูล.

## ข้อกำหนดเบื้องต้น

ก่อนที่เราจะเริ่มบทแนะนำ โปรดตรวจสอบว่าคุณมีข้อกำหนดต่อไปนี้พร้อมแล้ว:

1. **Aspose.CAD Library:** ดาวน์โหลดและติดตั้งไลบรารี Aspose.CAD สำหรับ Java คุณสามารถหาไลบรารีได้จาก [here](https://releases.aspose.com/cad/java/).
2. **Java Development Kit (JDK):** ตรวจสอบว่าคุณได้ติดตั้ง Java บนระบบของคุณแล้ว.
3. **Integrated Development Environment (IDE):** เลือก IDE สำหรับ Java เช่น Eclipse หรือ IntelliJ เพื่อประสบการณ์การพัฒนาที่ราบรื่น.

## นำเข้าแพ็กเกจ

ในโครงการ Java ของคุณ ให้นำเข้าแพ็กเกจ Aspose.CAD ที่จำเป็นเพื่อเปิดใช้งานการจัดการไฟล์ CAD ตัวอย่างดังนี้:

```java
import com.aspose.cad;
import com.aspose.cad.imageoptions;
import com.aspose.cad.fileformats.cad.cadconsts;
import com.aspose.cad.fileformats.cad;
import com.aspose.cad.fileformats.cad.cadobjects;
```

## ขั้นตอนที่ 1: ตั้งค่าเส้นทางไฟล์

กำหนดเส้นทางไฟล์เข้าและออกสำหรับไฟล์ DWG ปรับค่า `dataDir`, `fileName`, และ `outPath` ให้สอดคล้อง.

```java
String dataDir = "Your Document Directory" + "ExportingDGN/";
String fileName = dataDir + "BlockRefDgn.dwg";
String outPath = dataDir + "BlockRefDgn.dwg.pdf";
```

## ขั้นตอนที่ 2: สร้างอินสแตนซ์ PdfOptions

สร้างอินสแตนซ์ของคลาส `PdfOptions` เนื่องจากเรากำลัง **exporting the CAD file to PDF** เพื่อการตรวจสอบอย่างรวดเร็ว.

```java
PdfOptions exportOptions = new PdfOptions();
```

## ขั้นตอนที่ 3: โหลดไฟล์ DWG

โหลดไฟล์ DWG ที่มีอยู่เป็นภาพและแปลงเป็นประเภท `CadImage`.

```java
CadImage cadImage = (CadImage) Image.load(fileName);
```

## ขั้นตอนที่ 4: วนลูปผ่าน Entities

วนลูปผ่านแต่ละ entity ภายในไฟล์ DWG และตรวจสอบว่าเป็นการกำหนดภาพหรือไม่ หากใช่ ให้ดึงอ้างอิงภายนอกของออบเจ็กต์นั้น.

```java
for (CadBaseEntity baseEntity : cadImage.getEntities()) {
    if (baseEntity.getTypeName() == CadEntityTypeName.DGNUNDERLAY) {
        CadDgnUnderlay dgnFile = (CadDgnUnderlay)baseEntity;
        System.out.println(dgnFile.getUnderlayPath());
    }
}
```

## ขั้นตอนที่ 5: กำหนด Rasterization Options

กำหนดการตั้งค่าสำหรับอ็อบเจ็กต์ `CadRasterizationOptions` รวมถึงความกว้างและความสูงของหน้า, เลย์เอาต์, และสีพื้นหลัง.

```java
CadRasterizationOptions vectorRasterizationOptions = new CadRasterizationOptions();
vectorRasterizationOptions.setPageWidth(1600);
vectorRasterizationOptions.setPageHeight(1600);
vectorRasterizationOptions.setLayouts(new String[] { "Model" });
vectorRasterizationOptions.setAutomaticLayoutsScaling(false);
vectorRasterizationOptions.setNoScaling(true);
vectorRasterizationOptions.setBackgroundColor(Color.getBlack());
vectorRasterizationOptions.setDrawType(CadDrawTypeMode.UseObjectColor);
```

## ขั้นตอนที่ 6: ตั้งค่า Vector Rasterization Options

ตั้งค่าตัวเลือกการเรสเตอร์เวกเตอร์สำหรับการส่งออก.

```java
exportOptions.setVectorRasterizationOptions(vectorRasterizationOptions);
```

## ขั้นตอนที่ 7: ส่งออก DWG เป็น PDF

สุดท้าย ส่งออก DWG เป็น PDF โดยเรียกเมธอด `save`.

```java
cadImage.save(outPath, exportOptions);
```

## ปัญหาทั่วไปและวิธีแก้

| ปัญหา | สาเหตุ | วิธีแก้ |
|-------|-------|----------|
| **No DGN underlay appears** | DWG ไม่ได้มีเอนทิตี้ `DGNUNDERLAY`. | ตรวจสอบว่า DWG ต้นฉบับมีการอ้างอิง DGN. |
| **PDF is blank** | ตัวเลือกการเรสเตอร์ตั้งค่าเป็นขนาดศูนย์หรือเลย์เอาต์ผิด. | ตรวจสอบว่า `setPageWidth`/`setPageHeight` มีค่าเป็นบวกและ `setLayouts` ตรงกับชื่อเลย์เอาต์ของ DWG. |
| **License exception** | ทำงานโดยไม่มีใบอนุญาต Aspose.CAD ที่ถูกต้อง. | ใช้ใบอนุญาตชั่วคราวหรือที่ซื้อแล้วก่อนเรียกใช้เมธอด API ใดๆ. |

## คำถามที่พบบ่อย

### Q1: คุณสามารถหาเอกสารสำหรับ Aspose.CAD for Java ได้ที่ไหน?
A1: เอกสารสามารถหาได้จาก [here](https://reference.aspose.com/cad/java/).

### Q2: คุณสามารถดาวน์โหลดไลบรารี Aspose.CAD สำหรับ Java ได้อย่างไร?
A2: คุณสามารถดาวน์โหลดไลบรารีจาก [this link](https://releases.aspose.com/cad/java/).

### Q3: มีเวอร์ชันทดลองฟรีสำหรับ Aspose.CAD for Java หรือไม่?
A3: ใช่ คุณสามารถหาเวอร์ชันทดลองได้ที่ [here](https://releases.aspose.com/).

### Q4: คุณสามารถรับใบอนุญาตชั่วคราวสำหรับ Aspose.CAD for Java ได้จากที่ไหน?
A4: รับใบอนุญาตชั่วคราวได้จาก [here](https://purchase.aspose.com/temporary-license/).

### Q5: ต้องการความช่วยเหลือหรือมีคำถาม?
A5: เยี่ยมชมฟอรั่มสนับสนุนชุมชน Aspose.CAD ที่ [here](https://forum.aspose.com/c/cad/19).

### Q6: ฉันสามารถแปลง PDF ที่ได้กลับเป็น DWG ได้หรือไม่?
A6: PDF เป็นตัวอย่างแบบเรสเตอร์; การแปลงกลับเป็น DWG ต้องใช้เครื่องมือรีเวิร์ส‑เอนจิเนียริ่งแยกต่างหาก.

### Q7: วิธีการนี้ทำงานกับรูปแบบ CAD อื่น ๆ เช่น DWF หรือ DXF หรือไม่?
A7: ใช่ Aspose.CAD รองรับหลายรูปแบบ; คุณเพียงต้องปรับส่วนขยายไฟล์และการตั้งค่าเรสเตอร์ให้สอดคล้อง.

---

**Last Updated:** 2026-01-10  
**Tested With:** Aspose.CAD for Java 24.11  
**Author:** Aspose  

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}