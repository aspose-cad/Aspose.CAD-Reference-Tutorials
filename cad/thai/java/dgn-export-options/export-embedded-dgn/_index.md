---
date: 2026-01-07
description: เรียนรู้วิธีส่งออก CAD เป็น PDF และแปลง DGN เป็น PDF ด้วย Aspose.CAD
  สำหรับ Java คู่มือขั้นตอนต่อขั้นตอนสำหรับนักพัฒนา Java
linktitle: Export Embedded DGN
second_title: Aspose.CAD Java API
title: ส่งออก CAD เป็น PDF – ส่งออก DGN ที่ฝังไว้ด้วย Aspose.CAD สำหรับ Java
url: /th/java/dgn-export-options/export-embedded-dgn/
weight: 11
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# ส่งออก CAD เป็น PDF – ส่งออก DGN ฝังด้วย Aspose.CAD สำหรับ Java

## Introduction

ในบทแนะนำนี้คุณจะได้ค้นพบ **วิธีส่งออก CAD เป็น PDF** โดยการแปลงไฟล์ DGN ที่ฝังอยู่ให้เป็นเอกสาร PDF คุณภาพสูงด้วย Aspose.CAD สำหรับ Java Aspose.CAD เป็นไลบรารีที่แข็งแกร่งซึ่งให้ผู้พัฒนา Java ควบคุมการจัดการไฟล์ CAD ได้อย่างเต็มที่ ไม่ว่าจะต้อง **แปลง DGN เป็น PDF**, **แปลง DWG เป็น PDF**, หรือเพียงแค่เรนเดอร์ภาพวาด CAD ในรูปแบบอื่น ๆ ตามขั้นตอนด้านล่าง คุณจะสามารถผสานความสามารถนี้เข้าไปในแอปพลิเคชันของคุณได้ในไม่กี่นาที

## Quick Answers
- **“export CAD to PDF” หมายถึงอะไร?** จะทำการแปลงภาพวาด CAD (DWG, DGN ฯลฯ) ให้เป็นไฟล์ PDF พร้อมคงคุณภาพเวกเตอร์ไว้  
- **ใช้ไลบรารีอะไร?** Aspose.CAD สำหรับ Java  
- **ต้องมีลิขสิทธิ์หรือไม่?** จำเป็นต้องมีลิขสิทธิ์สำหรับการใช้งานในสภาพแวดล้อมการผลิต; มีรุ่นทดลองฟรีให้ใช้  
- **ข้อกำหนดเบื้องต้นหลักคืออะไร?** สภาพแวดล้อมการพัฒนา Java และไฟล์ JAR ของ Aspose.CAD สำหรับ Java  
- **สามารถปรับแต่งผลลัพธ์ได้หรือไม่?** ได้ – สามารถเลือกเลย์เอาต์, ตั้งค่าการเรสเตอร์ไลเซชัน, และควบคุมการตั้งค่า PDF ได้

## What is “export CAD to PDF”?

การส่งออก CAD เป็น PDF หมายถึงการนำไฟล์ CAD ดั้งเดิม (เช่น DWG หรือ DGN) มาสร้างเป็นเอกสาร PDF ที่แสดงผลรูปทรงเรขาคณิตเดิมอย่างแม่นยำ PDF สามารถเปิดดูได้บนทุกแพลตฟอร์มโดยไม่ต้องใช้ซอฟต์แวร์ CAD ทำให้เหมาะสำหรับการแชร์, พิมพ์, หรือเก็บรักษาเอกสาร

## Why use Aspose.CAD for Java to convert DGN to PDF?
- **ไม่มีการพึ่งพาไลบรารีภายนอก** – ทำงานได้โดยตรงใน Java  
- **คงข้อมูลเวกเตอร์** – PDF จะคมชัดแม้ขยายระดับใดก็ได้  
- **ควบคุมได้ละเอียด** – เลือกเลย์เอาต์เฉพาะ, ตั้งค่า DPI ของการเรสเตอร์ไลเซชัน, และฝังฟอนต์  
- **พร้อมใช้งานระดับองค์กร** – รองรับไฟล์ขนาดใหญ่, การประมวลผลแบบแบตช์, และตัวเลือกลิขสิทธิ์ต่าง ๆ  

## Prerequisites

ก่อนเริ่มทำตามขั้นตอนต่อไปนี้ ให้ตรวจสอบว่าคุณมีสิ่งต่อไปนี้พร้อมแล้ว:

- **Java Development Environment** – ติดตั้งและกำหนดค่า JDK 8 หรือสูงกว่า  
- **Aspose.CAD for Java** – ดาวน์โหลดไฟล์ JAR ล่าสุดจาก [here](https://releases.aspose.com/cad/java/)  

## Import Packages

เพื่อเริ่มต้น คุณต้องนำเข้าคลาสที่จำเป็นในโปรเจกต์ Java ของคุณ เพิ่มบรรทัด import ด้านล่างนี้ลงในไฟล์ซอร์สของคุณ:

```java
import java.io.FileNotFoundException;
import java.io.FileOutputStream;
import java.io.OutputStream;
import com.aspose.cad.Image;
import com.aspose.cad.ImageOptionsBase;
import com.aspose.cad.fileformats.cad.CadImage;
import com.aspose.cad.fileformats.dgn.DgnImage;
import com.aspose.cad.imageoptions.CadRasterizationOptions;
import com.aspose.cad.imageoptions.JpegOptions;
import com.aspose.cad.imageoptions.PdfOptions;
```

## How to export DGN to PDF using Aspose.CAD for Java?

ต่อไปนี้เป็นขั้นตอนที่เป็นลำดับเลขที่ชัดเจนซึ่งแสดงวิธีแปลงไฟล์ DGN ที่ฝังอยู่ (อยู่ภายใน DWG) ให้เป็น PDF

### Step 1: Set Up Input and Output Paths

กำหนดไดเรกทอรีที่เก็บไฟล์ต้นทางและระบุ DWG ที่มี DGN ฝังอยู่

```java
String dataDir = "Your Document Directory" + "ExportingDGN/";
String fileName = dataDir + "BlockRefDgn.dwg";
```

### Step 2: Load DWG File

โหลดไฟล์ DWG เข้าไปในอ็อบเจกต์ `Image` Aspose.CAD จะตรวจจับข้อมูล DGN ที่ฝังอยู่โดยอัตโนมัติ

```java
Image objImage = Image.load(fileName);
```

### Step 3: Configure Rasterization Options

เลือกเลย์เอาต์ที่ต้องการใส่ใน PDF ในตัวอย่างนี้เราจะส่งออกเฉพาะเลย์เอาต์ **Model** เท่านั้น

```java
CadRasterizationOptions rasterizationOptions = new CadRasterizationOptions();
rasterizationOptions.setLayouts(new String[] {"Model"});
```

### Step 4: Configure PDF Options

ผสานการตั้งค่าการเรสเตอร์ไลเซชันเข้ากับตัวเลือกการส่งออก PDF

```java
PdfOptions pdfOptions = new PdfOptions();
pdfOptions.setVectorRasterizationOptions(rasterizationOptions);
```

### Step 5: Save PDF File

สุดท้ายให้บันทึกไฟล์ PDF ลงดิสก์โดยใช้ตัวเลือกที่กำหนดไว้

```java
objImage.save(dataDir + "BlockRefDgn.pdf", pdfOptions);
```

## Convert DWG to PDF – an additional tip

หากไฟล์ต้นทางของคุณเป็น DWG ธรรมดา (ไม่มี DGN ฝัง) คุณสามารถใช้โค้ดเดียวกันได้ – เพียงเปลี่ยนค่า `fileName` ให้ชี้ไปยัง DWG ที่ต้องการแปลง ตัวเลือกการเรสเตอร์ไลเซชันและ PDF จะยังคงเหมือนเดิม ทำให้คุณได้เวิร์กโฟลว์ **convert DWG to PDF** ที่สอดคล้องกัน

## Common Issues and Solutions

| Issue | Reason | Solution |
|-------|--------|----------|
| **Blank PDF output** | Layout name mismatch | Verify that the layout name passed to `setLayouts` exactly matches the layout in the source file (case‑sensitive). |
| **License exception** | Using the trial without a license | Apply a valid Aspose.CAD license before loading the image (`License license = new License(); license.setLicense("Aspose.CAD.lic");`). |
| **File not found** | Incorrect `dataDir` path | Use an absolute path or ensure the relative path is correct relative to the project’s working directory. |
| **Low‑resolution graphics** | Default rasterization DPI is low | Set `rasterizationOptions.setPageWidth/Height` or `setResolution` to increase DPI. |

## Frequently Asked Questions

**Q: สามารถใช้ Aspose.CAD สำหรับ Java ในโครงการเชิงพาณิชย์ได้หรือไม่?**  
A: ได้, Aspose.CAD สำหรับ Java เป็นไลบรารีเชิงพาณิชย์ คุณสามารถซื้อไลเซนส์ได้จาก [here](https://purchase.aspose.com/buy)。

**Q: มีรุ่นทดลองฟรีหรือไม่?**  
A: มี, คุณสามารถเข้าถึงรุ่นทดลองฟรีของ Aspose.CAD สำหรับ Java ได้ที่ [here](https://releases.aspose.com/)。

**Q: จะขอรับการสนับสนุนสำหรับ Aspose.CAD สำหรับ Java ได้อย่างไร?**  
A: คุณสามารถขอรับการสนับสนุนจากชุมชน Aspose.CAD ได้ที่ [forum](https://forum.aspose.com/c/cad/19)。

**Q: หากต้องการไลเซนส์ชั่วคราวทำอย่างไร?**  
A: คุณสามารถขอรับไลเซนส์ชั่วคราวได้จาก [here](https://purchase.aspose.com/temporary-license/)。

**Q: จะหาเอกสารอ้างอิงได้จากที่ไหน?**  
A: เอกสารอ้างอิงพร้อมให้ใช้งานที่ [here](https://reference.aspose.com/cad/java/)。

## Conclusion

คุณได้เรียนรู้วิธี **ส่งออก CAD เป็น PDF** โดยเฉพาะวิธี **แปลง DGN เป็น PDF** และแม้กระทั่ง **แปลง DWG เป็น PDF** ด้วย Aspose.CAD สำหรับ Java ด้วยการทำตามขั้นตอนข้างต้น คุณสามารถผสานการแปลง CAD‑to‑PDF อย่างราบรื่นเข้าไปในโซลูชันที่ใช้ Java ใด ๆ ได้ ส่งมอบ PDF คุณภาพสูงให้กับผู้ใช้โดยไม่ต้องพึ่งซอฟต์แวร์ CAD เพิ่มเติม

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}

---

**Last Updated:** 2026-01-07  
**Tested With:** Aspose.CAD for Java 24.12  
**Author:** Aspose