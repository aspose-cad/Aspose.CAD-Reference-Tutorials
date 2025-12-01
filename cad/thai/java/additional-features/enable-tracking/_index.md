---
date: 2025-12-01
description: เรียนรู้วิธีตั้งขนาดหน้ากระดาษ PDF, แปลง DWG เป็น PDF และเปิดใช้งานการติดตามการเปลี่ยนแปลงของ
  DWG ด้วย Aspose.CAD for Java.
language: th
linktitle: Set PDF Page Size and Track DWG with Java
second_title: Aspose.CAD Java API
title: ตั้งขนาดหน้ากระดาษ PDF และติดตาม DWG ด้วย Aspose.CAD Java
url: /java/additional-features/enable-tracking/
weight: 12
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# ตั้งค่าขนาดหน้า PDF และติด DWG ด้วย Aspose.CAD Java

## บทนำ

เมื่อทำงานร่วมกันในโครงการ CAD คุณมักต้อง **ตั้งค่าขนาดหน้า PDF** เพื่อให้ได้เลย์เอาต์ที่สม่ำเสมอ, **แปลง DWG เป็น PDF**, และติดตามการเปลี่ยนแปลงทุกอย่างที่ทำกับแบบแปลน Aspose.CAD for Java ทำให้ทุกอย่างนี้เป็นไปได้ในกระบวนการทำงานเดียวที่ราบรื่น ในบทเรียนนี้เราจะเดินผ่านขั้นตอนที่แน่นอนเพื่อ **ตั้งค่าขนาดหน้า PDF**, เปิดใช้งาน **การติดตามการเปลี่ยนแปลงของ DWG**, และส่งออกแบบแปลนเป็น PDF—ทั้งหมดโดยใช้ Java

## คำตอบอย่างรวดเร็ว
- **ฉันจะตั้งค่าขนาดหน้า PDF อย่างไร?** ใช้ `CadRasterizationOptions.setPageWidth()` และ `setPageHeight()` ก่อนทำการส่งออก  
- **ฉันสามารถติดตามการเปลี่ยนแปลงขณะส่งออกได้หรือไม่?** ได้ – สร้าง `CadRenderHandler` แบบกำหนดเองเพื่อจับผลการติดตาม  
- **เมธอดใดที่แปลง DWG เป็น PDF?** เรียก `image.save(stream, pdfOptions)` หลังจากกำหนดค่าตัวเลือกแล้ว  
- **ข้อกำหนดเบื้องต้นหลักคืออะไร?** JDK, Aspose.CAD for Java, และโฟลเดอร์ที่มีไฟล์ DWG/DXF  
- **ต้องมีลิขสิทธิ์สำหรับการใช้งานในโปรดักชันหรือไม่?** ใช่, ต้องมีลิขสิทธิ์ Aspose.CAD ที่ถูกต้องสำหรับการใช้งานที่ไม่ใช่รุ่นทดลอง

## “ตั้งค่าขนาดหน้า PDF” หมายถึงอะไรในบริบทของการส่งออก DWG?

การตั้งค่าขนาดหน้า PDF กำหนดมิติของผ้าใบ PDF ที่สร้างขึ้น (ความกว้าง × ความสูงเป็นพิกเซล) สิ่งนี้สำคัญเมื่อคุณต้องการให้แบบแปลนที่ส่งออกพอดีกับขนาดกระดาษหรือเลย์เอาต์หน้าจอเฉพาะ เพื่อให้ทุกองค์ประกอบปรากฏตรงตามที่คุณคาดหวัง

## ทำไมต้องเปิดใช้งานการติดตามขณะส่งออกไฟล์ DWG?

การติดตาม (หรือ change‑tracking) บันทึกปัญหาการเรนเดอร์, ฟอนต์ที่หายไป, หรือเอนทิตีที่ไม่รองรับที่เกิดขึ้นระหว่างการแปลง โดยการจับข้อมูลนี้คุณสามารถ:

- ระบุปัญหาได้อย่างรวดเร็วเพื่อแก้ไขก่อนส่งมอบขั้นสุดท้าย  
- ให้ข้อเสนอแนะที่ชัดเจนแก่สมาชิกทีมเกี่ยวกับสิ่งที่ถูกเปลี่ยนหรือถูกละเว้น  
- รักษาบันทึกการตรวจสอบสำหรับอุตสาหกรรมที่ต้องการการปฏิบัติตามกฎระเบียบอย่างเข้มงวด

## ข้อกำหนดเบื้องต้น

- **Java Development Kit (JDK)** – เวอร์ชันล่าสุดใดก็ได้ (8+)  
- **Aspose.CAD for Java** – ดาวน์โหลดจาก [Aspose CAD download page](https://releases.aspose.com/cad/java/)  
- **Document Directory** – โฟลเดอร์ที่บรรจุไฟล์ DWG/DXF ที่คุณต้องการประมวลผล

## นำเข้า Namespaces

เริ่มต้นด้วยการนำเข้าคลาส Aspose.CAD ที่จำเป็นและคลาส I/O ของ Java มาตรฐาน

```java
import com.aspose.cad.Image;

import com.aspose.cad.imageoptions.CadRasterizationOptions;
import com.aspose.cad.imageoptions.CadRenderResult;
import com.aspose.cad.imageoptions.PdfOptions;
import com.aspose.cad.imageoptions.RenderResult;
import java.io.FileNotFoundException;
import java.io.FileOutputStream;
import java.io.OutputStream;
```

## ขั้นตอนที่ 1: โหลดไฟล์ DWG (หรือ DXF)

โหลดแบบแปลนต้นฉบับของคุณเข้าสู่วัตถุ `Image` ปรับเส้นทางให้ชี้ไปยังไดเรกทอรีของคุณเอง

```java
String dataDir = "Your Document Directory" + "DXFDrawings/";
Image image = Image.load(dataDir + "conic_pyramid.dxf");
```

## ขั้นตอนที่ 2: กำหนดค่าตัวเลือกการส่งออก PDF (รวมถึงขนาดหน้า)

ที่นี่เราตั้งค่าตัวเลือก PDF และ **ตั้งค่าขนาดหน้า PDF** ให้เป็น 800 × 600 พิกเซล นี่คือจุดที่คีย์เวิร์ดหลักถูกนำไปใช้

```java
OutputStream stream = new FileOutputStream(dataDir + "output_conic_pyramid.pdf");
PdfOptions pdfOptions = new PdfOptions();
CadRasterizationOptions cadRasterizationOptions = new CadRasterizationOptions();
pdfOptions.setVectorRasterizationOptions(cadRasterizationOptions);
cadRasterizationOptions.setPageWidth(800);   // set PDF page width
cadRasterizationOptions.setPageHeight(600);  // set PDF page height
```

## ขั้นตอนที่ 3: ดำเนินการติดตาม

สร้างตัวจัดการข้อผิดพลาดแบบกำหนดเองที่จะรับข้อมูลการติดตามระหว่างกระบวนการแปลง

```java
cadRasterizationOptions.RenderResult = new ErrorHandler();
```

## ขั้นตอนที่ 4: ส่งออกเป็น PDF

เมื่อกำหนดค่าตัวเลือกและตัวจัดการการติดตามเรียบร้อยแล้ว ให้ส่งออกแบบแปลน ขั้นตอนนี้ **แปลง DWG เป็น PDF** (หรือ DXF เป็น PDF ในตัวอย่างของเรา)

```java
System.out.println("Exporting to pdf format");
image.save(stream, pdfOptions);
```

## ขั้นตอนที่ 5: คลาส CadRenderHandler – การจับผลการติดตาม

คลาส `ErrorHandler` ขยาย `CadRenderHandler` และพิมพ์ปัญหาการเรนเดอร์ใด ๆ ที่เกิดขึ้นขณะ **ติดตามการเปลี่ยนแปลง DWG** ไฟล์

```java
public static class ErrorHandler extends CadRasterizationOptions.CadRenderHandler {
    @Override
    public void invoke(CadRenderResult result) {
        System.out.println("Tracking results of exporting");

        if (result.isRenderComplete())
            return;

        System.out.println("Have some problems:");

        int idxError = 1;
        for (RenderResult rr : result.getFailures()) {
            System.out.printf("{0}. {1}, {2}", idxError, rr.getRenderCode(), rr.getMessage());
            idxError++;
        }
    }
}
```

## ปัญหาทั่วไป & วิธีแก้ไข

| ปัญหา | สาเหตุ | วิธีแก้ |
|-------|--------|----------|
| **Missing fonts** | ไฟล์ CAD อ้างอิงฟอนต์ที่ไม่ได้ติดตั้งบนเซิร์ฟเวอร์ | ติดตั้งฟอนต์ที่จำเป็นหรือฝังฟอนต์ในแบบแปลนต้นฉบับ |
| **Unsupported entities** | มีเอนทิตี DWG บางประเภทที่ Aspose.CAD ยังไม่รองรับ | ใช้ผลการติดตามเพื่อระบุและทำให้แบบแปลนเรียบง่ายขึ้น |
| **Incorrect page size** | ไม่ได้เรียก `setPageWidth/Height` ก่อนทำการส่งออก | ตรวจสอบให้แน่ใจว่าได้ตั้งค่าขนาดหน้าใน `CadRasterizationOptions` ตามที่แสดงข้างต้น |

## คำถามที่พบบ่อย

### Q1: ฉันสามารถเปิดใช้งานการติดตามสำหรับรูปแบบไฟล์ CAD อื่น ๆ ด้วย Aspose.CAD for Java ได้หรือไม่?

A1: Aspose.CAD รองรับการติดตามหลัก ๆ สำหรับไฟล์ DWG/DXF สำหรับรูปแบบอื่น ๆ โปรดตรวจสอบเอกสารอย่างเป็นทางการเพื่อดูฟีเจอร์ที่มีให้

### Q2: ฉันจะจัดการตัวเลือกการส่งออกเพิ่มเติมใน Aspose.CAD for Java อย่างไร?

A2: ไลบรารีมีตัวเลือกหลายอย่าง เช่น DPI, สีพื้นหลัง, และการเรนเดอร์แบบเวกเตอร์ สำรวจรายละเอียดได้ใน [Aspose.CAD Java Documentation](https://reference.aspose.com/cad/java/)

### Q3: มีเวอร์ชันทดลองของ Aspose.CAD for Java หรือไม่?

A3: มี คุณสามารถดาวน์โหลดเวอร์ชันทดลองฟรีจาก [Aspose.CAD Free Trial](https://releases.aspose.com/)

### Q4: ฉันจะหาความช่วยเหลือหรือพูดคุยเกี่ยวกับปัญหา Aspose.CAD for Java ได้ที่ไหน?

A4: ฟอรั่มชุมชนที่ [Aspose.CAD forum](https://forum.aspose.com/c/cad/19) เป็นสถานที่ที่ดีสำหรับถามคำถามและแบ่งปันประสบการณ์

### Q5: ฉันจะขอรับลิขสิทธิ์ชั่วคราวสำหรับ Aspose.CAD for Java อย่างไร?

A5: ทำตามขั้นตอนในหน้า [Temporary License](https://purchase.aspose.com/temporary-license/) เพื่อขอรับลิขสิทธิ์ที่มีระยะเวลาจำกัดสำหรับการประเมินผล

### Q6: ฉันสามารถ **แปลง DWG เป็น PDF** พร้อมคงรักษาชั้น (layers) ได้หรือไม่?

A6: ได้ โดยการกำหนดค่า `CadRasterizationOptions` คุณสามารถคงข้อมูลชั้นใน PDF ที่สร้างขึ้นได้

### Q7: วิธีที่ดีที่สุดในการ **ส่งออก DWG เป็น PDF** ด้วยขนาดหน้าที่กำหนดเองคืออะไร?

A7: ตั้งค่าความกว้างและความสูงที่ต้องการโดยใช้ `setPageWidth` และ `setPageHeight` ก่อนเรียก `image.save()` – ตามที่แสดงในขั้นตอนที่ 2 อย่างชัดเจน

## สรุป

โดยทำตามขั้นตอนข้างต้น คุณสามารถ **ตั้งค่าขนาดหน้า PDF**, **แปลง DWG เป็น PDF**, และ **ติดตามการเปลี่ยนแปลงในไฟล์ DWG** ด้วย Aspose.CAD for Java กระบวนการนี้ให้คุณควบคุมเลย์เอาต์ผลลัพธ์ได้อย่างเต็มที่พร้อมกับการวินิจฉัยที่มีคุณค่าเพื่อให้การทำงานร่วมกันใน CAD ราบรื่นและปราศจากข้อผิดพลาด อย่าลังเลที่จะสำรวจตัวเลือกการเรนเดอร์เพิ่มเติมและรวมโค้ดนี้เข้าไปในสายงานอัตโนมัติที่ใหญ่ขึ้น

---

**อัปเดตล่าสุด:** 2025-12-01  
**ทดสอบกับ:** Aspose.CAD for Java 24.12 (ล่าสุด ณ เวลาที่เขียน)  
**ผู้เขียน:** Aspose  

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}