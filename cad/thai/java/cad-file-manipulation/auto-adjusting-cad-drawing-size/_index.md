---
date: 2025-12-22
description: เรียนรู้วิธีส่งออกภาพวาด CAD และแปลงไฟล์ DWG เป็น BMP ใน Java ด้วย Aspose.CAD
  ปฏิบัติตามคู่มือขั้นตอนต่อขั้นตอนนี้เพื่อการจัดการไฟล์ CAD อย่างมีประสิทธิภาพ
linktitle: Auto Adjusting CAD Drawing Size
second_title: Aspose.CAD Java API
title: วิธีส่งออกภาพวาด CAD เป็น BMP ด้วย Aspose.CAD สำหรับ Java
url: /th/java/cad-file-manipulation/auto-adjusting-cad-drawing-size/
weight: 13
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# วิธีส่งออกภาพวาด CAD เป็น BMP ด้วย Aspise.CAD สำหรับ Java

## บทนำ

หากคุณกำลังมองหาวิธีที่ชัดเจนและเชื่อถือได้ในการ **how to export cad** ไฟล์จาก Java คุณมาถูกที่แล้ว ด้วย Aspose.CAD for Java คุณไม่เพียงแต่สามารถปรับขนาดภาพวาดอัตโนมัติได้เท่านั้น แต่ยังสามารถ **convert DWG to BMP** ได้ด้วยเพียงไม่กี่บรรทัดของโค้ด บทเรียนนี้จะพาคุณผ่านกระบวนการทั้งหมด ตั้งแต่การตั้งค่าสภาพแวดล้อมจนถึงการสร้างภาพ BMP ที่คงรูปแบบ CAD ดั้งเดิมไว้

## คำตอบอย่างรวดเร็ว
- **What does “how to export cad” mean?** หมายถึงการแปลงไฟล์ CAD (DWG, DXF ฯลฯ) ไปเป็นรูปแบบอื่น เช่น BMP, PNG หรือ PDF.  
- **Which library handles the conversion?** Aspose.CAD for Java ให้ API ที่ง่ายสำหรับงานนี้.  
- **Do I need a license?** ใบอนุญาตชั่วคราวใช้ได้สำหรับการทดสอบ; จำเป็นต้องมีใบอนุญาตเต็มสำหรับการใช้งานจริง.  
- **Can I export multiple layouts at once?** ได้ – โดยการตั้งค่า property `Layouts` คุณสามารถระบุว่า layout ใดบ้างที่ต้องการเรนเดอร์.  
- **Is BMP the only output format?** ไม่ – คุณยังสามารถส่งออกเป็น PNG, JPEG, TIFF และรูปแบบอื่น ๆ ได้อีก.

## อะไรคือ “how to export cad” กับ Aspose.CAD?

การส่งออก CAD หมายถึงการนำภาพวาด CAD ดั้งเดิม (เช่นไฟล์ DWG) มารันเดอร์เป็นภาพราสเตอร์หรือรูปแบบเวกเตอร์อื่น ๆ Aspose.CAD ดูแลการทำงานทั้งหมด: การวิเคราะห์โครงสร้าง CAD, การแปลงเวกเตอร์เป็นราสเตอร์, และการเขียนผลลัพธ์ไปยังรูปแบบภาพที่คุณเลือก.

## ทำไมต้องใช้ Aspose.CAD for Java เพื่อ **convert DWG to BMP**?

- **ไม่มีการพึ่งพาภายนอก** – Java แท้, ไม่มี DLL เนทีฟ.  
- **รองรับเต็มรูปแบบ** สำหรับ DWG, DXF, DGN และรูปแบบอื่น ๆ.  
- **การควบคุมละเอียด** ของตัวเลือกการราสเตอร์ เช่น การเลือก layout, การสเกล, และสีพื้นหลัง.  
- **ประสิทธิภาพสูง** เหมาะสำหรับการประมวลผลแบบแบชบนเซิร์ฟเวอร์.

## ข้อกำหนดเบื้องต้น

ก่อนที่คุณจะเริ่ม, ตรวจสอบว่าคุณมีสิ่งต่อไปนี้:

1. **Java Development Kit** – ดาวน์โหลดได้จาก [here](https://www.java.com/en/download/).  
2. **Aspose.CAD for Java library** – รับไฟล์ JAR ล่าสุดจาก [here](https://releases.aspose.com/cad/java/).  
3. **Sample CAD file** – ไฟล์ DWG (เช่น `sample.dwg`) ที่วางไว้ในไดเรกทอรีเอกสารของโปรเจคของคุณ.

## นำเข้า Namespaces

ในแอปพลิเคชัน Java ของคุณ, ให้รวม namespaces ที่จำเป็นเพื่อใช้ฟังก์ชันของ Aspose.CAD ตัวอย่างต่อไปนี้:

```java

import com.aspose.cad.Image;
import com.aspose.cad.ImageOptionsBase;

import com.aspose.cad.imageoptions.CadRasterizationOptions;
import com.aspose.cad.imageoptions.PngOptions;
```

ตอนนี้, เราจะวิเคราะห์กระบวนการของ **how to export cad** ให้เป็นขั้นตอนที่จัดการได้.

## คู่มือขั้นตอนต่อขั้นตอน

### ขั้นตอนที่ 1: โหลดภาพวาด CAD

```java
String dataDir = "Your Document Directory" + "CADConversion/";
String sourceFilePath = dataDir + "sample.dwg";
Image objImage = Image.load(sourceFilePath);
```

เราจะโหลดไฟล์ DWG ต้นฉบับเข้าสู่วัตถุ `Image`, ซึ่งทำหน้าที่เป็นจุดเริ่มต้นสำหรับการดำเนินการต่อไปทั้งหมด.

### ขั้นตอนที่ 2: สร้าง `BmpOptions`

```java
BmpOptions bmpOptions = new BmpOptions();
```

`BmpOptions` จะเก็บการตั้งค่าการราสเตอร์ที่เฉพาะเจาะจงสำหรับการส่งออกเป็น BMP.

### ขั้นตอนที่ 3: กำหนดค่าการราสเตอร์

```java
CadRasterizationOptions cadRasterizationOptions = new CadRasterizationOptions();
bmpOptions.setVectorRasterizationOptions(cadRasterizationOptions);
```

ที่นี่เราจะเชื่อมตัวเลือกการราสเตอร์กับ BMP options, เพื่อให้เราควบคุมวิธีการเรนเดอร์เอนทิตีของ CAD.

### ขั้นตอนที่ 4: ตั้งค่า Layout(s) ที่จะส่งออก

```java
cadRasterizationOptions.setLayouts(new String[]{"Model"});
```

property `Layouts` บอก Aspose.CAD ว่า layout ใดของภาพวาดที่จะรวมไว้. ในกรณีส่วนใหญ่, `"Model"` คือ layout หลักที่คุณต้องการแปลง.

### ขั้นตอนที่ 5: ส่งออกเป็นรูปแบบ BMP

```java
String outPath = sourceFilePath + ".bmp";
objImage.save(outPath, bmpOptions);
```

การเรียก `save` พร้อมกับ `BmpOptions` ที่กำหนดไว้ จะเขียนไฟล์ BMP ลงดิสก์. นี้เป็นการเสร็จสิ้น workflow ของ **convert DWG to BMP**.

## ปัญหาที่พบบ่อยและวิธีแก้

| ปัญหา | สาเหตุ | วิธีแก้ |
|-------|--------|-----|
| ภาพที่ส่งออกเป็นสีขาวเปล่า | ชื่อ layout ไม่ถูกต้องหรือไม่มี layout | ตรวจสอบว่าชื่อ layout ตรงกับไฟล์ CAD (เช่น `"Model"`). |
| ความละเอียดต่ำ | ค่า DPI เริ่มต้นต่ำ | ตั้งค่า `cadRasterizationOptions.setResolution(300);` ก่อนบันทึก. |
| ข้อผิดพลาด out‑of‑memory สำหรับไฟล์ขนาดใหญ่ | ภาพวาดขนาดใหญ่ต้องการ heap มากขึ้น | เพิ่มขนาด heap ของ JVM (`-Xmx2g`) หรือประมวลผลหน้าแยกกัน. |

## คำถามที่พบบ่อย

**Q: Aspose.CAD รองรับรูปแบบไฟล์ CAD ต่าง ๆ หรือไม่?**  
A: ใช่, Aspose.CAD รองรับ DWG, DXF, DGN และรูปแบบอื่น ๆ มากมาย.

**Q: ฉันสามารถใช้ Aspose.CAD สำหรับโครงการเชิงพาณิชย์ได้หรือไม่?**  
A: แน่นอน. ซื้อใบอนุญาตได้จาก [here](https://purchase.aspose.com/buy) สำหรับการใช้งานในผลิตภัณฑ์.

**Q: ฉันจะขอรับใบอนุญาตชั่วคราวสำหรับการทดสอบได้อย่างไร?**  
A: คุณสามารถรับใบอนุญาตชั่วคราวได้จาก [here](https://purchase.aspose.com/temporary-license/).

**Q: ฉันจะหาแหล่งสนับสนุนจากชุมชนได้จากที่ไหน?**  
A: เข้าร่วมฟอรั่มชุมชน Aspose.CAD ที่ [forum](https://forum.aspose.com/c/cad/19).

**Q: มีการทดลองใช้ฟรีสำหรับ Aspose.CAD for Java หรือไม่?**  
A: มี, ดาวน์โหลดการทดลองใช้ฟรีได้จาก [here](https://releases.aspose.com/).

## สรุป

ในคู่มือนี้เราได้สาธิต **how to export cad** ไฟล์จาก Java และ **convert DWG to BMP** ด้วย Aspose.CAD โดยการทำตามห้าขั้นตอนข้างต้น คุณสามารถรวมการแปลง CAD เป็นภาพเข้าไปในแอปพลิเคชัน Java ใดก็ได้ ไม่ว่าจะเป็นเครื่องมือเดสก์ท็อป, เว็บเซอร์วิส, หรือ pipeline การประมวลผลแบบแบช สำรวจรูปแบบผลลัพธ์อื่น ๆ (PNG, JPEG, PDF) โดยการเปลี่ยนคลาส options, และใช้ประโยชน์จากชุดฟีเจอร์ที่ครอบคลุมของ Aspose.CAD เพื่อตอบสนองความต้องการการจัดการ CAD ของคุณทั้งหมด.

---

**อัปเดตล่าสุด:** 2025-12-22  
**ทดสอบกับ:** Aspose.CAD for Java 24.12  
**ผู้เขียน:** Aspose  

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}