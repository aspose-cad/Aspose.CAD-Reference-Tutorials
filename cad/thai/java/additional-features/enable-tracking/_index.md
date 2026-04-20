---
date: 2026-02-10
description: คู่มือแบบขั้นตอนต่อขั้นตอนเกี่ยวกับวิธีเปิดใช้งานการติดตามในไฟล์ DWG
  ด้วย Aspose.CAD สำหรับ Java และวิธีแปลง DXF เป็น PDF พร้อมตัวจัดการข้อผิดพลาดแบบกำหนดเอง
linktitle: Enable Tracking in DWG Files Using Java
second_title: Aspose.CAD Java API
title: วิธีเปิดใช้งานการติดตามในไฟล์ DWG ด้วย Aspose.CAD ใน Java
url: /th/java/additional-features/enable-tracking/
weight: 12
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# วิธีเปิดการติดตามในไฟล์ DWG ด้วย Aspose.CAD ใน Java

## บทนำ

หากคุณกำลังทำงานในโครงการ CAD ที่ทำงานร่วมกัน การรู้ **how to enable tracking** ในกระบวนการทำงาน DWG ของคุณเป็นการเปลี่ยนเกม มันให้ข้อมูลเชิงลึกแบบเรียลไทม์เกี่ยวกับปัญหาการเรนเดอร์ ช่วยให้คุณจับข้อบกพร่องในการแปลงได้ตั้งแต่ต้น และทำให้ผู้มีส่วนได้ส่วนเสียทุกคนรับทราบ ในบทแนะนำนี้เราจะพาคุณผ่านขั้นตอนที่แม่นยำเพื่อเปิดการติดตามด้วย Aspose.CAD สำหรับ Java และเราจะสาธิต **how to convert DXF to PDF** เป็นส่วนหนึ่งของสายงานเดียวกัน เมื่อเสร็จสิ้นคุณจะมีโค้ดสแนปช็อตที่พร้อมใช้งานในระดับการผลิตซึ่งรายงานข้อผิดพลาดผ่านคลาส **custom error handler Java** ขณะส่งออกภาพวาดของคุณ.

## คำตอบด่วน
- **What does “enable dwg tracking java” do?** It activates Aspose.CAD’s error‑handling callbacks so you can see rendering problems during export.  
  => มันเปิดใช้งาน callback การจัดการข้อผิดพลาดของ Aspose.CAD เพื่อให้คุณเห็นปัญหาการเรนเดอร์ระหว่างการส่งออก.  
- **Do I need a license?** A trial works for testing; a commercial license is required for production.  
  => รุ่นทดลองใช้งานได้สำหรับการทดสอบ; จำเป็นต้องมีใบอนุญาตเชิงพาณิชย์สำหรับการใช้งานจริง.  
- **Can I also convert DXF to PDF?** Yes – the same `PdfOptions` used for DWG works for DXF, fulfilling the *java convert dxf pdf* scenario.  
  => ได้ – `PdfOptions` เดียวกันที่ใช้กับ DWG ทำงานกับ DXF ได้เช่นกัน, ตอบสนองสถานการณ์ *java convert dxf pdf*.  
- **Which JDK version is required?** Java 8 or higher.  
  => Java 8 หรือสูงกว่า.  
- **Where can I find more examples?** Check the Aspose.CAD Java Documentation linked below.  
  => ตรวจสอบ Aspose.CAD Java Documentation ที่ลิงก์ด้านล่าง.

## วิธีเปิดการติดตามในไฟล์ DWG ด้วย Aspose.CAD

การเปิดการติดตาม DWG ในแอปพลิเคชัน Java หมายถึงการแนบตัวจัดการการเรนเดอร์แบบกำหนดเองที่จับคำเตือน, ข้อผิดพลาด, และข้อมูลวินิจฉัยอื่น ๆ ขณะไฟล์ CAD ถูกแรสเตอร์หรือส่งออก การมองเห็นนี้ช่วยนักพัฒนาแก้ไขข้อบกพร่องของสายการแปลงและรับประกันผลลัพธ์ที่มีคุณภาพสูงขึ้น.

## ทำไมต้องใช้ Aspose.CAD สำหรับ Java?

- **Full‑feature CAD support** – DWG, DXF, DGN, และอื่น ๆ.  
- **No external dependencies** – ไลบรารี Java แท้, เหมาะสำหรับการทำอัตโนมัติบนเซิร์ฟเวอร์.  
- **Built‑in tracking** – ผลลัพธ์การเรนเดอร์โดยละเอียดผ่าน `CadRenderHandler`.  
- **Easy PDF export** – การแปลงด้วยบรรทัดเดียวขณะรักษาข้อมูลเวกเตอร์.

## ข้อกำหนดเบื้องต้น

ก่อนที่เราจะลงลึกในขั้นตอนการทำงาน โปรดตรวจสอบว่าคุณมีข้อกำหนดต่อไปนี้พร้อมใช้งาน:
- Java Development Kit (JDK): ตรวจสอบว่าคุณได้ติดตั้ง Java บนระบบของคุณแล้ว  
- Aspose.CAD for Java: ดาวน์โหลดและติดตั้ง Aspose.CAD for Java จาก [download link](https://releases.aspose.com/cad/java/).  
- Document Directory: เตรียมโฟลเดอร์ที่เก็บไฟล์ DWG ของคุณ  

## นำเข้า Namespaces

ในโครงการ Java ของคุณ ให้เริ่มต้นด้วยการนำเข้า namespaces ที่จำเป็นเพื่อใช้ฟังก์ชันของ Aspose.CAD:
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

เริ่มต้นด้วยการโหลดไฟล์ DWG (หรือ DXF) เข้าไปในแอปพลิเคชัน Java ของคุณ ปรับเส้นทางไฟล์ให้เหมาะสม:
```java
String dataDir = "Your Document Directory" + "DXFDrawings/";
Image image = Image.load(dataDir + "conic_pyramid.dxf");
```

## ขั้นตอนที่ 2: ตั้งค่า PDF Export Options (How to Convert DXF to PDF)

ตั้งค่าตัวเลือกการส่งออก PDF โดยระบุตัวเลือกการแรสเตอร์เวกเตอร์สำหรับ CAD ซึ่งยังแสดงความสามารถ *java convert dxf pdf* ด้วย:
```java
OutputStream stream = new FileOutputStream(dataDir + "output_conic_pyramid.pdf");
PdfOptions pdfOptions = new PdfOptions();
CadRasterizationOptions cadRasterizationOptions = new CadRasterizationOptions();
pdfOptions.setVectorRasterizationOptions(cadRasterizationOptions);
cadRasterizationOptions.setPageWidth(800);
cadRasterizationOptions.setPageHeight(600);
```

## ขั้นตอนที่ 3: ใช้งานการติดตาม (Custom Error Handler Java)

ใช้งานการติดตามโดยใช้คลาส custom error handler. คลาสนี้จะจับปัญหาการเรนเดอร์และแสดงผลในคอนโซล:
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

กำหนดคลาส `ErrorHandler` (สืบทอดจาก `CadRenderHandler`) เพื่อประมวลผลผลลัพธ์การเรนเดอร์และแสดงข้อมูลการติดตาม:
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

## ทำไมเรื่องนี้ถึงสำคัญ

โดยการเปิดการติดตาม คุณจะได้เส้นทางการตรวจสอบที่ชัดเจนของทุกขั้นตอนการแปลง ซึ่งมีคุณค่าสูงในอุตสาหกรรมที่มีการควบคุม (สถาปัตยกรรม, วิศวกรรม, ก่อสร้าง) ที่ต้องการหลักฐานการเรนเดอร์ที่แม่นยำสำหรับการตรวจสอบการปฏิบัติตามกฎระเบียบ ตัวจัดการข้อผิดพลาดแบบกำหนดเองยังให้จุดเชื่อมต่อเพื่อบันทึกปัญหาไปยังระบบมอนิเตอร์หรือเพื่อเรียกใช้การลองใหม่อัตโนมัติ

## ปัญหาทั่วไปและวิธีแก้

- **`NullPointerException` on `RenderResult`** – ตรวจสอบว่าคุณใช้ Aspose.CAD เวอร์ชัน 23.10 หรือใหม่กว่า; เวอร์ชันเก่าขาด API `RenderResult`.  
- **File not found** – ตรวจสอบว่า `dataDir` ชี้ไปยังโฟลเดอร์ที่ถูกต้องและชื่อไฟล์ตรงกันอย่างแม่นยำ รวมถึงตัวพิมพ์ใหญ่‑เล็ก.  
- **Missing tracking output** – ยืนยันว่า `ErrorHandler` แบบกำหนดเองได้ถูกกำหนดให้กับ `cadRasterizationOptions.RenderResult` อย่างถูกต้อง.  

## คำถามที่พบบ่อย

**Q:** ฉันสามารถเปิดการติดตามสำหรับรูปแบบไฟล์ CAD อื่นโดยใช้ Aspose.CAD for Java ได้หรือไม่?  
A: Aspose.CAD รองรับการติดตาม DWG เป็นหลัก สำหรับรูปแบบอื่น ๆ โปรดดูเอกสารอย่างเป็นทางการ.  

**Q:** ฉันจะจัดการตัวเลือกการส่งออกเพิ่มเติมใน Aspose.CAD for Java ได้อย่างไร?  
A: สำรวจเอกสารที่ครอบคลุมได้ที่ [Aspose.CAD Java Documentation](https://reference.aspose.com/cad/java/).  

**Q:** มีเวอร์ชันทดลองสำหรับ Aspose.CAD for Java หรือไม่?  
A: มี, คุณสามารถเข้าถึงเวอร์ชันทดลองได้ที่ [Aspose.CAD Free Trial](https://releases.aspose.com/).  

**Q:** ฉันจะขอความช่วยเหลือหรือหารือเกี่ยวกับปัญหา Aspose.CAD for Java ได้จากที่ไหน?  
A: เยี่ยมชม [Aspose.CAD forum](https://forum.aspose.com/c/cad/19) เพื่อรับการสนับสนุนจากชุมชน.  

**Q:** ฉันจะขอรับใบอนุญาตชั่วคราวสำหรับ Aspose.CAD for Java ได้อย่างไร?  
A: ทำตามขั้นตอนที่อธิบายไว้ที่ [Temporary License](https://purchase.aspose.com/temporary-license/).  

## สรุป

การเปิดการติดตาม DWG ใน Java ด้วย Aspose.CAD ไม่เพียงให้คุณมองเห็นปัญหาการแปลงเท่านั้น แต่ยังทำให้กระบวนการออกแบบร่วมกันเป็นระบบมากขึ้น โดยทำตามขั้นตอนข้างต้นคุณสามารถ **how to enable tracking**, แปลง DXF เป็น PDF, และจัดการกับปัญหาการเรนเดอร์ใด ๆ อย่างราบรื่น.

---

**Last Updated:** 2026-02-10  
**Tested With:** Aspose.CAD for Java 24.12  
**Author:** Aspose  

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}