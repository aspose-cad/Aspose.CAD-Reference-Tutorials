---
date: 2026-02-23
description: เรียนรู้วิธีแปลง DWG เป็น BMP ใน Java ด้วย Aspose.CAD รวมถึงการส่งออกไฟล์
  CAD, การแปลง CAD แบบกลุ่ม, การเรนเดอร์เลย์เอาต์ CAD และการส่งออกหลายเลย์เอาต์ CAD
  อย่างมีประสิทธิภาพ
linktitle: Auto Adjusting CAD Drawing Size
second_title: Aspose.CAD Java API
title: วิธีแปลง DWG เป็น BMP ด้วย Aspose.CAD สำหรับ Java
url: /th/java/cad-file-manipulation/auto-adjusting-cad-drawing-size/
weight: 13
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# วิธีแปลง DWG เป็น BMP ด้วย Aspose.CAD สำหรับ Java

## คำแนะนำเบื้องต้น

หากคุณกำลังมองหาวิธีที่ชัดเจนและเชื่อถือได้ในการ **convert dwg to bmp** จาก Java คุณมาถูกที่แล้ว ด้วย Aspose.CAD สำหรับ Java คุณไม่เพียงแต่สามารถปรับขนาดการวาดอัตโนมัติได้เท่านั้น แต่ยังสามารถ **export CAD** ไปยัง BMP, PNG, PDF และรูปแบบอื่น ๆ อีกมากมาย บทแนะนำนี้จะพาคุณผ่านกระบวนการทั้งหมด—from การตั้งค่าสภาพแวดล้อมจนถึงการสร้างภาพ BMP ที่คงรูปแบบ CAD ดั้งเดิม—พร้อมแสดงวิธีที่คุณสามารถ **batch convert CAD** หรือ **render CAD layout** อย่างเลือกสรรได้

## คำตอบสั้น ๆ
- **“convert dwg to bmp” หมายถึงอะไร?** หมายถึงการเรนเดอร์ไฟล์ DWG (หรือไฟล์ CAD อื่น) เป็นภาพ BMP แบบ raster  
- **ไลบรารีที่ทำการแปลงคืออะไร?** Aspose.CAD สำหรับ Java ให้ API แบบ pure‑Java ที่ง่ายต่อการใช้งานสำหรับงานนี้  
- **ต้องใช้ไลเซนส์หรือไม่?** ไลเซนส์ชั่วคราวใช้สำหรับการทดสอบได้; ไลเซนส์เต็มจำเป็นสำหรับการใช้งานจริง  
- **สามารถ export หลาย layout พร้อมกันได้หรือไม่?** ได้ – โดยตั้งค่า property `Layouts` คุณสามารถระบุ layout ที่ต้องการเรนเดอร์ได้  
- **BMP เป็นรูปแบบผลลัพธ์เดียวหรือไม่?** ไม่ – คุณยังสามารถ export ไปยัง PNG, JPEG, TIFF, PDF และอื่น ๆ ได้อีก

## วิธีแปลง DWG เป็น BMP ด้วย Aspose.CAD สำหรับ Java
ในส่วนนี้เราตอบคำถามหลักโดยตรงและเตรียมพื้นฐานสำหรับคู่มือขั้นตอนต่อไป

### “convert dwg to bmp” กับ Aspose.CAD คืออะไร?
การแปลง DWG เป็น BMP หมายถึงการนำไฟล์ CAD ดั้งเดิม (เช่น DWG) มาทำ rasterization ให้เป็นภาพ bitmap Aspose.CAD ทำหน้าที่ทั้งหมด: วิเคราะห์โครงสร้าง CAD, เรนเดอร์เวกเตอร์, และเขียนผลลัพธ์เป็นไฟล์ BMP ที่ตรงกับขนาดและสีของ layout ดั้งเดิม

### ทำไมต้องใช้ Aspose.CAD สำหรับ Java เพื่อ **convert DWG to BMP**?
- **Pure Java implementation** – ไม่ต้องใช้ DLL หรือเครื่องมือภายนอก  
- **Broad format support** – รองรับ DWG, DXF, DGN และรูปแบบ CAD อื่น ๆ อย่างเนทีฟ  
- **Fine‑grained control** – สามารถเลือก layout เฉพาะ, ตั้งค่า DPI, สีพื้นหลัง ฯลฯ  
- **Scalable performance** – เหมาะสำหรับการ batch converting CAD บนเซิร์ฟเวอร์หรือยูทิลิตี้เดสก์ท็อป  

## ข้อกำหนดเบื้องต้น

ก่อนเริ่มทำตามขั้นตอนต่อไปนี้ให้แน่ใจว่าคุณมี:

1. **Java Development Kit** – ดาวน์โหลดได้จาก [ที่นี่](https://www.java.com/en/download/)  
2. **Aspose.CAD สำหรับ Java library** – รับ JAR ล่าสุดจาก [ที่นี่](https://releases.aspose.com/cad/java/)  
3. **ไฟล์ CAD ตัวอย่าง** – ไฟล์ DWG (เช่น `sample.dwg`) ที่วางไว้ในโฟลเดอร์ `document` ของโปรเจกต์คุณ  

## นำเข้า Namespaces

ในแอปพลิเคชัน Java ของคุณ ให้รวม namespaces ที่จำเป็นเพื่อใช้ฟังก์ชันของ Aspose.CAD ตัวอย่างเช่น:

```java
import com.aspose.cad.Image;
import com.aspose.cad.ImageOptionsBase;

import com.aspose.cad.imageoptions.CadRasterizationOptions;
import com.aspose.cad.imageoptions.PngOptions;
```

ต่อไปเราจะแบ่งกระบวนการ **convert dwg to bmp** ออกเป็นขั้นตอนที่จัดการได้ง่าย

## คู่มือขั้นตอนโดยละเอียด

### ขั้นตอนที่ 1: โหลดภาพ CAD

```java
String dataDir = "Your Document Directory" + "CADConversion/";
String sourceFilePath = dataDir + "sample.dwg";
Image objImage = Image.load(sourceFilePath);
```

เราจะโหลดไฟล์ DWG ต้นฉบับเข้าเป็นอ็อบเจ็กต์ `Image` ซึ่งเป็นจุดเริ่มต้นสำหรับการดำเนินการต่อไปทั้งหมด

### ขั้นตอนที่ 2: สร้าง `BmpOptions`

```java
BmpOptions bmpOptions = new BmpOptions();
```

`BmpOptions` จะเก็บการตั้งค่าการ rasterization เฉพาะสำหรับการส่งออกเป็น BMP

### ขั้นตอนที่ 3: ตั้งค่าการ Rasterization

```java
CadRasterizationOptions cadRasterizationOptions = new CadRasterizationOptions();
bmpOptions.setVectorRasterizationOptions(cadRasterizationOptions);
```

ที่นี่เราจะเชื่อมต่อ options การ rasterization กับ `BmpOptions` เพื่อควบคุมวิธีการเรนเดอร์เอนทิตีของ CAD

### ขั้นตอนที่ 4: กำหนด Layout(s) ที่จะ Export

```java
cadRasterizationOptions.setLayouts(new String[]{"Model"});
```

property `Layouts` บอก Aspose.CAD ว่าจะรวม layout ใดบ้าง ในหลายกรณี `"Model"` เป็น layout หลักที่ต้องการแปลง แต่คุณก็สามารถ **export multiple CAD layouts** ได้โดยส่งอาร์เรย์ของชื่อ layout

### ขั้นตอนที่ 5: Export เป็นรูปแบบ BMP

```java
String outPath = sourceFilePath + ".bmp";
objImage.save(outPath, bmpOptions);
```

การเรียก `save` พร้อมกับ `BmpOptions` ที่กำหนดไว้จะเขียนไฟล์ BMP ลงดิสก์ ขั้นตอนนี้จบกระบวนการ **convert dwg to bmp** แล้ว

## ปัญหาที่พบบ่อยและวิธีแก้

| Issue | Reason | Fix |
|-------|--------|-----|
| ภาพผลลัพธ์เป็นค่าว่าง | ชื่อ layout ไม่ถูกต้องหรือไม่มี layout | ตรวจสอบให้แน่ใจว่าชื่อ layout ตรงกับไฟล์ CAD (เช่น `"Model"`) |
| ความละเอียดต่ำ | DPI เริ่มต้นต่ำ | ตั้งค่า `cadRasterizationOptions.setResolution(300);` ก่อนบันทึก |
| เกิด Out‑of‑memory สำหรับไฟล์ขนาดใหญ่ | การวาดขนาดใหญ่ต้องการ heap มาก | เพิ่มขนาด heap ของ JVM (`-Xmx2g`) หรือประมวลผลหน้าแยกส่วน |

## คำถามที่พบบ่อย

**Q: Aspose.CAD รองรับรูปแบบไฟล์ CAD ต่าง ๆ หรือไม่?**  
A: รองรับ DWG, DXF, DGN และรูปแบบอื่น ๆ มากมาย  

**Q: สามารถใช้ Aspose.CAD ในโครงการเชิงพาณิชย์ได้หรือไม่?**  
A: แน่นอน ซื้อไลเซนส์ได้จาก [ที่นี่](https://purchase.aspose.com/buy) สำหรับการใช้งานจริง  

**Q: จะขอรับไลเซนส์ชั่วคราวสำหรับการทดสอบได้อย่างไร?**  
A: รับไลเซนส์ชั่วคราวได้จาก [ที่นี่](https://purchase.aspose.com/temporary-license/)  

**Q: จะหาชุมชนสนับสนุนได้จากที่ไหน?**  
A: เข้าร่วมฟอรั่ม Aspose.CAD ที่ [forum](https://forum.aspose.com/c/cad/19)  

**Q: มีรุ่นทดลองฟรีสำหรับ Aspose.CAD สำหรับ Java หรือไม่?**  
A: มี ดาวน์โหลดรุ่นทดลองฟรีได้จาก [ที่นี่](https://releases.aspose.com/)  

## เคล็ดลับเพิ่มเติมสำหรับการ Batch Converting ไฟล์ CAD

- **วนลูปผ่านไดเรกทอรี** และใช้ขั้นตอนเดียวกันกับแต่ละไฟล์ DWG; ทำให้สามารถ **batch convert CAD** ได้ง่าย  
- **Reuse `CadRasterizationOptions`** เมื่อเป็นไปได้ เพื่อลดภาระการสร้างอ็อบเจ็กต์ใหม่  
- **บันทึก log ของแต่ละการแปลง** พร้อมชื่อไฟล์ต้นฉบับและเส้นทางผลลัพธ์ เพื่ออำนวยความสะดวกในการแก้ไขปัญหา  

## สรุป

ในคู่มือนี้เราได้สาธิตวิธี **convert dwg to bmp** ด้วย Aspose.CAD สำหรับ Java และอธิบายขั้นตอนสำคัญเพื่อ **export CAD**, **render CAD layout**, รวมถึง **export multiple CAD layouts** ในการรันเดียว ด้วยการทำตามห้าขั้นตอนข้างต้น คุณสามารถผสานการแปลง CAD‑to‑image เข้าไปในแอปพลิเคชัน Java ใดก็ได้ ไม่ว่าจะเป็นเครื่องมือเดสก์ท็อป, เว็บเซอร์วิส, หรือ pipeline การประมวลผลแบบ batch ลองสำรวจรูปแบบผลลัพธ์อื่น ๆ (PNG, JPEG, PDF) โดยเปลี่ยนคลาส options และใช้คุณสมบัติอันหลากหลายของ Aspose.CAD เพื่อรองรับทุกความต้องการในการจัดการ CAD ของคุณ

---

**Last Updated:** 2026-02-23  
**Tested With:** Aspose.CAD for Java 24.12  
**Author:** Aspose  

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}