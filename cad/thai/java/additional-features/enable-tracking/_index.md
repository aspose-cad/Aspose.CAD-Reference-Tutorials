---
date: 2025-12-09
description: เรียนรู้วิธีเปิดใช้งานการติดตาม DWG ด้วย Java และดูวิธีแปลงไฟล์ DXF เป็น
  PDF ด้วย Aspose.CAD ใน Java คู่มือขั้นตอนนี้จะแสดงกระบวนการทำงานเต็มรูปแบบสำหรับโครงการ
  CAD แบบร่วมมือ
linktitle: Enable Tracking in DWG Files Using Java
second_title: Aspose.CAD Java API
title: เปิดใช้งานการติดตามในไฟล์ DWG ด้วย Aspose.CAD ใน Java
url: /th/java/additional-features/enable-tracking/
weight: 12
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# เปิดการติดตามในไฟล์ DWG ด้วย Aspose.CAD ใน Java

## บทนำ

ในกระบวนการทำงาน CAD สมัยใหม่ การ **enable dwg tracking java** เป็นสิ่งสำคัญสำหรับทีมที่ต้องการตรวจสอบการเปลี่ยนแปลง, จับข้อผิดพลาดตั้งแต่ต้น, และทำให้ผู้มีส่วนได้ส่วนเสียทุกคนอยู่บนหน้าเดียวกัน การสอนนี้จะพาคุณผ่านขั้นตอนที่จำเป็นเพื่อเปิดการติดตามสำหรับไฟล์ DWG ด้วย Aspose.CAD สำหรับ Java และในระหว่างนั้นคุณจะได้เห็นวิธี **java convert dxf pdf** เป็นส่วนหนึ่งของกระบวนการส่งออก เมื่อเสร็จสิ้นคุณจะมีโค้ดสั้นที่พร้อมรันซึ่งไม่เพียงแค่แปลงไฟล์แต่ยังรายงานปัญหาการเรนเดอร์ใด ๆ ด้วย

## คำตอบอย่างรวดเร็ว
- **“enable dwg tracking java” ทำอะไร?** มันเปิดใช้งาน callback การจัดการข้อผิดพลาดของ Aspose.CAD เพื่อให้คุณเห็นปัญหาการเรนเดอร์ระหว่างการส่งออก  
- **ต้องใช้ไลเซนส์หรือไม่?** รุ่นทดลองใช้ได้สำหรับการทดสอบ; ต้องมีไลเซนส์เชิงพาณิชย์สำหรับการใช้งานจริง  
- **สามารถแปลง DXF เป็น PDF ได้หรือไม่?** ได้ – `PdfOptions` เดียวกันที่ใช้กับ DWG สามารถใช้กับ DXF ทำให้รองรับสถานการณ์ *java convert dxf pdf*  
- **ต้องการ JDK เวอร์ชันใด?** Java 8 หรือสูงกว่า  
- **หาตัวอย่างเพิ่มเติมได้ที่ไหน?** ดูเอกสาร Aspose.CAD Java ที่ลิงก์ด้านล่าง

## อะไรคือการเปิดการติดตาม DWG ใน Java?
การเปิดการติดตาม DWG ในแอปพลิเคชัน Java หมายถึงการแนบตัวจัดการเรนเดอร์แบบกำหนดเองที่จับคำเตือน, ข้อผิดพลาด, และข้อมูลวินิจฉัยอื่น ๆ ขณะไฟล์ CAD ถูกเรสเตอร์ไลซ์หรือส่งออก การมองเห็นนี้ช่วยนักพัฒนาดีบัก pipeline การแปลงและทำให้ผลลัพธ์มีคุณภาพสูงขึ้น

## ทำไมต้องใช้ Aspose.CAD สำหรับ Java?
- **สนับสนุน CAD อย่างเต็มรูปแบบ** – DWG, DXF, DGN, และอื่น ๆ  
- **ไม่มีการพึ่งพาไลบรารีภายนอก** – ไลบรารี Java แท้, เหมาะสำหรับการทำงานอัตโนมัติบนเซิร์ฟเวอร์  
- **มีการติดตามในตัว** – รายละเอียดผลการเรนเดอร์ผ่าน `CadRenderHandler`  
- **ส่งออก PDF ง่าย** – การแปลงบรรทัดเดียวพร้อมรักษาข้อมูลเวกเตอร์

## ข้อกำหนดเบื้องต้น

ก่อนที่เราจะลงลึกในขั้นตอนการทำงาน, โปรดตรวจสอบว่าคุณมีสิ่งต่อไปนี้พร้อมใช้งาน:

- Java Development Kit (JDK): ตรวจสอบว่าคุณได้ติดตั้ง Java บนระบบของคุณแล้ว  
- Aspose.CAD for Java: ดาวน์โหลดและติดตั้ง Aspose.CAD for Java จาก [download link](https://releases.aspose.com/cad/java/)  
- Document Directory: เตรียมโฟลเดอร์ที่เก็บไฟล์ DWG ของคุณไว้

## นำเข้า Namespaces

ในโปรเจกต์ Java ของคุณ, เริ่มต้นด้วยการนำเข้า namespaces ที่จำเป็นเพื่อใช้ฟังก์ชันของ Aspose.CAD:

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

## ขั้นตอนที่ 1: โหลดไฟล์ DWG

เริ่มต้นด้วยการโหลดไฟล์ DWG (หรือ DXF) เข้าสู่แอปพลิเคชัน Java ของคุณ ปรับเส้นทางไฟล์ให้ตรงตามที่ตั้งจริง:

```java
String dataDir = "Your Document Directory" + "DXFDrawings/";
Image image = Image.load(dataDir + "conic_pyramid.dxf");
```

## ขั้นตอนที่ 2: กำหนดค่าตัวเลือกการส่งออก PDF

ตั้งค่าตัวเลือกการส่งออก PDF, ระบุตัวเลือกการเรสเตอร์ไลซ์เวกเตอร์สำหรับ CAD. ตัวอย่างนี้ยังแสดงความสามารถ *java convert dxf pdf*:

```java
OutputStream stream = new FileOutputStream(dataDir + "output_conic_pyramid.pdf");
PdfOptions pdfOptions = new PdfOptions();
CadRasterizationOptions cadRasterizationOptions = new CadRasterizationOptions();
pdfOptions.setVectorRasterizationOptions(cadRasterizationOptions);
cadRasterizationOptions.setPageWidth(800);
cadRasterizationOptions.setPageHeight(600);
```

## ขั้นตอนที่ 3: ใช้การติดตาม

ใช้การติดตามด้วยคลาสตัวจัดการข้อผิดพลาดแบบกำหนดเอง. คลาสนี้จะจับปัญหาการเรนเดอร์และแสดงผลในคอนโซล:

```java
cadRasterizationOptions.RenderResult = new ErrorHandler();
```

## ขั้นตอนที่ 4: ส่งออกเป็น PDF

เริ่มกระบวนการส่งออกเพื่อแปลงไฟล์ DWG/DXF เป็น PDF พร้อมเปิดการติดตาม:

```java
System.out.println("Exporting to pdf format");
image.save(stream, pdfOptions);
```

## ขั้นตอนที่ 5: คลาส CadRenderHandler

กำหนดคลาส `ErrorHandler` (สืบทอดจาก `CadRenderHandler`) เพื่อประมวลผลผลการเรนเดอร์และแสดงข้อมูลการติดตาม:

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

## ปัญหาทั่วไปและวิธีแก้

- **`NullPointerException` บน `RenderResult`** – ตรวจสอบว่าคุณใช้ Aspose.CAD เวอร์ชัน 23.10 หรือใหม่กว่า; รุ่นเก่าจะไม่มี API `RenderResult`  
- **ไฟล์ไม่พบ** – ยืนยันว่า `dataDir` ชี้ไปยังโฟลเดอร์ที่ถูกต้องและชื่อไฟล์ตรงกันอย่างแม่นยำ, รวมถึงตัวพิมพ์ใหญ่‑เล็ก  
- **ไม่มีผลลัพธ์การติดตาม** – ตรวจสอบว่าได้กำหนด `ErrorHandler` ที่กำหนดเองให้กับ `cadRasterizationOptions.RenderResult` อย่างถูกต้อง

## คำถามที่พบบ่อย

**ถาม:** ฉันสามารถเปิดการติดตามสำหรับรูปแบบไฟล์ CAD อื่น ๆ ด้วย Aspose.CAD for Java ได้หรือไม่?  
**ตอบ:** Aspose.CAD มุ่งเน้นการสนับสนุนการติดตาม DWG เป็นหลัก. สำหรับรูปแบบอื่น ๆ โปรดดูเอกสารอย่างเป็นทางการ

**ถาม:** ฉันจะจัดการตัวเลือกการส่งออกเพิ่มเติมใน Aspose.CAD for Java อย่างไร?  
**ตอบ:** สำรวจเอกสารที่ครอบคลุมได้ที่ [Aspose.CAD Java Documentation](https://reference.aspose.com/cad/java/)

**ถาม:** มีรุ่นทดลองของ Aspose.CAD for Java หรือไม่?  
**ตอบ:** มี, คุณสามารถเข้าถึงรุ่นทดลองได้ที่ [Aspose.CAD Free Trial](https://releases.aspose.com/)

**ถาม:** ฉันจะหาความช่วยเหลือหรือพูดคุยเกี่ยวกับปัญหา Aspose.CAD for Java ได้ที่ไหน?  
**ตอบ:** เยี่ยมชม [Aspose.CAD forum](https://forum.aspose.com/c/cad/19) เพื่อรับการสนับสนุนจากชุมชน

**ถาม:** ฉันจะขอรับไลเซนส์ชั่วคราวสำหรับ Aspose.CAD for Java อย่างไร?  
**ตอบ:** ทำตามขั้นตอนที่อธิบายไว้ที่ [Temporary License](https://purchase.aspose.com/temporary-license/)

## สรุป

การเปิดการติดตาม DWG ใน Java ด้วย Aspose.CAD ไม่เพียงให้คุณมองเห็นปัญหาการแปลงเท่านั้น, แต่ยังช่วยทำให้กระบวนการออกแบบร่วมกันมีประสิทธิภาพมากขึ้น ด้วยการทำตามขั้นตอนข้างต้น คุณสามารถ **enable dwg tracking java**, แปลง DXF เป็น PDF, และจัดการกับข้อผิดพลาดการเรนเดอร์ได้อย่างราบรื่น

---

**Last Updated:** 2025-12-09  
**Tested With:** Aspose.CAD for Java 24.12  
**Author:** Aspose  

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}