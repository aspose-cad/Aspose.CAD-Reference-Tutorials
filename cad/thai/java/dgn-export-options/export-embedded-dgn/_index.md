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

## การแนะนำ

บทแนะนำนี้คุณจะได้สัมผัสกับการส่งออก CAD ในรูปแบบ PDF** โดยการพิจารณาไฟล์ DGN ที่ฝังอยู่เป็นเอกสาร PDF ห้องโถงด้วย Aspose.CAD สำหรับ Java Aspose.CAD เป็นไลบรารี่ที่ให้ส่วนผสม Java การควบคุมไฟล์ CAD คุณไม่จำเป็นต้อง ** แปลง DGN PDF**, ** แปลง DWG PDF**, หรือเพียงแค่เรนเดอร์ระบบ CAD เพียงอย่างเดียว CAD อื่นๆ ตามขั้นตอนข้างล่างนี้สิทธิพิเศษนี้แอปพลิเคชันในวิธีการทำงานของระบบ

## คำตอบด่วน
- **“ส่งออก CAD เป็น PDF” วิธีการอะไร** จะทำในลักษณะนี้ CAD (DWG, DGN และอื่นๆ) ให้เป็นไฟล์ PDF พร้อมคงคุณภาพไว้
- **ใช้ไลบรารีอะไร?** Aspose.CAD สำหรับ Java
- **ต้องมีลิขสิทธิ์หรือไม่** ต้องใช้ลิขสิทธิ์ของบริษัทผู้ผลิต; มีรุ่นทดลองฟรีให้ใช้
- ** ข้อกำหนดเบื้องต้นหลักคืออะไร?** ยังคงพัฒนา Java และไฟล์ JAR ของ Aspose.CAD สำหรับ Java
- ** บางครั้งผลลัพธ์จะทำได้สำเร็จ?** ได้ – จอภาพหลายเลเยอร์, ​​การตั้งค่าการเรสเตอร์ไลเซชัน, และควบคุมได้ PDF ได้

## “ส่งออก CAD เป็น PDF” คืออะไร

ไฟล์ CAD เป็น PDF รูปแบบไฟล์ CAD ดั้งเดิม (เช่น DWG หรือ DGN) มาสร้างเป็นเอกสาร PDF ที่ประสิทธิภาพเดิมอย่างมีประสิทธิภาพ PDF สามารถเปิดดูได้บนทุกแพลตฟอร์มโดยไม่ต้องใช้ CAD เลยที่แชร์, พิมพ์, หรือบันทึกเอกสาร

## เหตุใดจึงต้องใช้ Aspose.CAD สำหรับ Java เพื่อแปลง DGN เป็น PDF
- **การรับฟังความคิดเห็นภายนอก** – ดำเนินการโดยตรงใน Java
- **คงข้อมูลรายละเอียด** – PDF จะคมชัดแม้ขยายระดับขอบเขต
- **ควบคุมได้ละเอียด** – เลือกไลเนอร์เฉพาะ, การตั้งค่า DPI ของเรสเตอร์ไลเซชัน, และฝังฟอนต์
- **พร้อมใช้งานระดับองค์กร** – รองรับไฟล์ขนาดใหญ่, รองรับแบบแบตช์, และส่วนที่ลิขสิทธิ์ต่างๆ มากมาย

## ข้อกำหนดเบื้องต้น

ก่อนที่จะเริ่มดำเนินการอย่างจริงจังเพื่อรับฟังคุณและพร้อมแล้ว:

- **Java Development Environment** – ไม่จำเป็นต้องและ JDK 8 หรืออื่นๆ
- **Aspose.CAD สำหรับ Java** – อย่าลืม JAR ล่าสุดจาก [ที่นี่](https://releases.aspose.com/cad/java/)

## แพคเกจนำเข้า

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

## วิธีการส่งออกไฟล์ DGN เป็น PDF โดยใช้ Aspose.CAD สำหรับ Java?

ต่อไปนี้เป็นขั้นตอนที่เป็นลำดับเลขที่ชัดเจนซึ่งแสดงวิธีแปลงไฟล์ DGN ที่ฝังอยู่ (อยู่ภายใน DWG) ให้เป็น PDF

### ขั้นตอนที่ 1: ตั้งค่าเส้นทางนำเข้าและส่งออก

กำหนดไดเรกทอรีที่เก็บไฟล์ต้นทางและระบุ DWG ที่มี DGN ฝังอยู่

```java
String dataDir = "Your Document Directory" + "ExportingDGN/";
String fileName = dataDir + "BlockRefDgn.dwg";
```

### ขั้นตอนที่ 2: โหลดไฟล์ DWG

โหลดไฟล์ DWG เข้าไปในอ็อบเจกต์ `Image` Aspose.CAD จะตรวจจับข้อมูล DGN ที่ฝังอยู่โดยอัตโนมัติ

```java
Image objImage = Image.load(fileName);
```

### ขั้นตอนที่ 3: กำหนดค่าตัวเลือกการแปลงเป็นภาพแรสเตอร์

เลือกเลย์เอาต์ที่ต้องการใส่ใน PDF ในตัวอย่างนี้เราจะส่งออกเฉพาะเลย์เอาต์ **Model** เท่านั้น

```java
CadRasterizationOptions rasterizationOptions = new CadRasterizationOptions();
rasterizationOptions.setLayouts(new String[] {"Model"});
```

### ขั้นตอนที่ 4: กำหนดค่าตัวเลือก PDF

ผสานการตั้งค่าการเรสเตอร์ไลเซชันเข้ากับตัวเลือกการส่งออก PDF

```java
PdfOptions pdfOptions = new PdfOptions();
pdfOptions.setVectorRasterizationOptions(rasterizationOptions);
```

### ขั้นตอนที่ 5: บันทึกไฟล์ PDF

สุดท้ายให้บันทึกไฟล์ PDF ลงดิสก์โดยใช้ตัวเลือกที่กำหนดไว้

```java
objImage.save(dataDir + "BlockRefDgn.pdf", pdfOptions);
```

## แปลง DWG เป็น PDF – เคล็ดลับเพิ่มเติม

หากไฟล์เริ่มต้นทางของคุณเป็น DWG ธรรมดา (ไม่มี DGN ฝัง) โดยทั่วไปโค้ดเดียวกันได้ – เพียงเปลี่ยนค่า `fileName` ให้ชี้ไปที่ DWG ต้องการแปลงสัญญาณเรสเตอร์ไลเซชันและ PDF ต่อเนื่องตามปกติ อย่าลืมได้ดูโฟลว์ **แปลง DWG เป็น PDF**

## ปัญหาทั่วไปและแนวทางแก้ไข

| ปัญหา | เหตุผล | โซลูชั่น |
|-------|--------|----------|
| **เอาต์พุต PDF เปล่า** | ชื่อเค้าโครงไม่ตรงกัน | ตรวจสอบว่าชื่อเค้าโครงที่ส่งไปยัง `setLayouts` ตรงกับเค้าโครงในไฟล์ต้นฉบับทุกประการ (คำนึงถึงตัวพิมพ์เล็กและตัวพิมพ์ใหญ่) |
| **ข้อยกเว้นใบอนุญาต** | การใช้รุ่นทดลองใช้โดยไม่มีใบอนุญาต | ใช้ใบอนุญาต Aspose.CAD ที่ถูกต้องก่อนที่จะโหลดภาพ (`ใบอนุญาตใบอนุญาต = ใบอนุญาตใหม่(); License.setLicense("Aspose.CAD.lic");`) |
| **ไม่พบไฟล์** | เส้นทาง `dataDir` ไม่ถูกต้อง | ใช้เส้นทางแบบสัมบูรณ์หรือตรวจสอบให้แน่ใจว่าเส้นทางสัมพัทธ์ถูกต้องเมื่อเทียบกับไดเร็กทอรีการทำงานของโปรเจ็กต์ |

**กราฟิกความละเอียดต่ำ** | ค่า DPI ของการแรสเตอร์ไรเซชันเริ่มต้นต่ำ | ตั้งค่า `rasterizationOptions.setPageWidth/Height` หรือ `setResolution` เพื่อเพิ่มค่า DPI |

## คำถามที่พบบ่อย

**ถาม: การฟัง Aspose.CAD สำหรับ Java สามารถตรวจสอบได้?**
ตอบ: ได้ Aspose.CAD สำหรับ Java เป็นไลบรารีต่างๆ มากมายเช่นเซนส์ได้จาก [ที่นี่](https://purchase.aspose.com/buy)。

**ถาม: มีรุ่นทดลองฟรีหรือไม่?**
ตอบ: มี ไม่เคยเข้าถึงรุ่นทดลองฟรีของ Aspose.CAD สำหรับ Java ได้ที่ [ที่นี่](https://releases.aspose.com/)。

**ถาม: จะขอรับสำหรับ Aspose.CAD สำหรับ Java ได้อย่างไร**
ตอบ: ไม่ว่าเราจะสามารถรับชุมชน Aspose.CAD ได้ที่ [forum](https://forum.aspose.com/c/cad/19)。

**ถาม: เพราะเหตุนี้เซนส์ทำอย่างไร?**
ตอบ: คุณจะได้รับความรู้สึกเพลิดเพลินไปกับเซนส์ชั่วคราวจาก [ที่นี่](https://purchase.aspose.com/temporary-license/)。

**คำถาม: เอกสารอ้างอิงจากที่ไหน?**
ตอบ: เอกสารอ้างอิงพร้อมให้ใช้งานที่ [ที่นี่](https://reference.aspose.com/cad/java/)。

## บทสรุป

คุณได้เรียนรู้วิธี **ส่งออก CAD เป็น PDF** โดยเฉพาะวิธี **แปลง DGN เป็น PDF** และแม้กระทั่ง **แปลง DWG เป็น PDF** ด้วย Aspose.CAD สำหรับ Java ด้วยการทำตามขั้นตอนข้างต้น คุณสามารถผสานการแปลง CAD‑to‑PDF อย่างราบรื่นเข้าไปในโซลูชันที่ใช้ Java ใด ๆ ได้ ส่งมอบ PDF คุณภาพสูงให้กับผู้ใช้โดยไม่ต้องพึ่งซอฟต์แวร์ CAD เพิ่มเติม

---

**Last Updated:** 2026-01-07  
**Tested With:** Aspose.CAD for Java 24.12  
**Author:** Aspose

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}
