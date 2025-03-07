---
title: หมดเวลาในการบันทึกสำหรับ CAD ด้วย Aspose.CAD
linktitle: ใส่การหมดเวลาในการบันทึก
second_title: Aspose.CAD Java API
description: เรียนรู้วิธีเพิ่มประสิทธิภาพแอปพลิเคชัน Java ของคุณด้วย Aspose.CAD ตั้งเวลาบันทึกสำหรับแบบร่าง CAD ปฏิบัติตามคำแนะนำทีละขั้นตอนของเรา
weight: 15
url: /th/java/other-cad-operations/put-timeout-on-save/
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# หมดเวลาในการบันทึกสำหรับ CAD ด้วย Aspose.CAD

## การแนะนำ

ยินดีต้อนรับสู่บทช่วยสอนเกี่ยวกับการหมดเวลาในการบันทึกโดยใช้ Aspose.CAD สำหรับ Java ในคู่มือนี้ เราจะแนะนำคุณตลอดขั้นตอนการตั้งค่าการหมดเวลาสำหรับการบันทึกแบบ CAD เพื่อปรับปรุงประสิทธิภาพของแอปพลิเคชันของคุณ Aspose.CAD สำหรับ Java เป็นไลบรารีอันทรงพลังที่ช่วยให้คุณทำงานกับไฟล์ CAD ในแอปพลิเคชัน Java ของคุณได้อย่างราบรื่น

## ข้อกำหนดเบื้องต้น

ก่อนที่จะเข้าสู่บทช่วยสอน ตรวจสอบให้แน่ใจว่าคุณมีข้อกำหนดเบื้องต้นต่อไปนี้:
-  Aspose.CAD สำหรับไลบรารี Java: ตรวจสอบให้แน่ใจว่าคุณมีไลบรารี Aspose.CAD สำหรับ Java ที่รวมอยู่ในโปรเจ็กต์ของคุณ คุณสามารถดาวน์โหลดห้องสมุดได้จาก[เว็บไซต์](https://releases.aspose.com/cad/java/).
- สภาพแวดล้อมการพัฒนา: ตั้งค่าสภาพแวดล้อมการพัฒนา Java ของคุณด้วยเครื่องมือและการขึ้นต่อกันที่จำเป็นทั้งหมด

## แพ็คเกจนำเข้า

ในการเริ่มต้น ให้นำเข้าแพ็คเกจที่จำเป็นลงในโปรเจ็กต์ Java ของคุณ เพิ่มบรรทัดต่อไปนี้ที่จุดเริ่มต้นของไฟล์ Java ของคุณ:

```java
import com.aspose.cad.Image;
import com.aspose.cad.InterruptionTokenSource;
import com.aspose.cad.fileformats.cad.CadImage;
import com.aspose.cad.imageoptions.CadRasterizationOptions;
import com.aspose.cad.imageoptions.PdfOptions;
import java.util.concurrent.TimeUnit;
```

ตอนนี้ เรามาแบ่งโค้ดตัวอย่างออกเป็นคำแนะนำทีละขั้นตอน:

## ขั้นตอนที่ 1: ตั้งค่าไดเรกทอรีต้นทางและเอาต์พุต

```java
final String SourceDir = Utils.getDataDir_DWGDrawings();
final String OutputDir = Utils.getDataDir_Output();
```

ตรวจสอบให้แน่ใจว่าคุณมีไดเรกทอรีต้นทางและเอาต์พุตที่ถูกต้องสำหรับแบบร่าง CAD ของคุณ

## ขั้นตอนที่ 2: สร้างแหล่งโทเค็นการหยุดชะงัก

```java
final InterruptionTokenSource source = new com.aspose.cad.InterruptionTokenSource();
```

เริ่มต้นแหล่งที่มาของโทเค็นการขัดจังหวะเพื่อจัดการการขัดจังหวะระหว่างการดำเนินการบันทึก

## ขั้นตอนที่ 3: โหลด CAD Drawing

```java
final CadImage cadImageBig = (CadImage)Image.load(SourceDir + "Drawing11.dwg");
```

 โหลดแบบ CAD ลงในไฟล์`CadImage` วัตถุ.

## ขั้นตอนที่ 4: กำหนดค่าตัวเลือกการแรสเตอร์

```java
CadRasterizationOptions rasterizationOptionsBig = new CadRasterizationOptions();
rasterizationOptionsBig.setPageWidth(cadImageBig.getSize().getWidth() / 2);
rasterizationOptionsBig.setPageHeight(cadImageBig.getSize().getHeight() / 2);
```

กำหนดค่าตัวเลือกแรสเตอร์สำหรับการวาด CAD

## ขั้นตอนที่ 5: กำหนดค่าตัวเลือก PDF

```java
final PdfOptions CADfBig = new PdfOptions();
CADfBig.setVectorRasterizationOptions(rasterizationOptionsBig);
CADfBig.setInterruptionToken(source.getToken());
```

ตั้งค่าตัวเลือก PDF ด้วยตัวเลือกการแรสเตอร์แบบเวกเตอร์และโทเค็นการขัดจังหวะ

## ขั้นตอนที่ 6: บันทึกการวาดด้วยการหมดเวลา

```java
cadImageBig.save(OutputDir + "PutTimeoutOnSave_out.pdf", CADfBig);
```

บันทึกแบบร่าง CAD ลงในไฟล์ PDF ด้วยการหมดเวลาที่ระบุ

## ขั้นตอนที่ 7: จัดการกับการหยุดชะงัก

```java
java.lang.Thread thread = new java.lang.Thread(new Runnable() {
    @Override
    public void run() {
        try {
            cadImageBig.save(OutputDir + "PutTimeoutOnSave_out.pdf", CADfBig);
        } catch (Throwable th) {
            System.out.println("interrupted !!!");
        }
    }
});
thread.start();
TimeUnit.SECONDS.sleep(3);
source.interrupt();
thread.join();
```

สร้างเธรดเพื่อจัดการการดำเนินการบันทึกและขัดจังหวะหลังจากหมดเวลาที่กำหนด

## บทสรุป

ยินดีด้วย! คุณได้เรียนรู้วิธีตั้งค่าการหมดเวลาในการบันทึกโดยใช้ Aspose.CAD สำหรับ Java เรียบร้อยแล้ว คุณสมบัตินี้สามารถเพิ่มประสิทธิภาพของแอปพลิเคชันที่เกี่ยวข้องกับ CAD ของคุณได้อย่างมาก

## คำถามที่พบบ่อย

### คำถามที่ 1: ฉันจะดาวน์โหลด Aspose.CAD สำหรับ Java ได้อย่างไร

 A1: คุณสามารถดาวน์โหลดได้จากไฟล์[หน้าเผยแพร่](https://releases.aspose.com/cad/java/).

### คำถามที่ 2: ฉันจะหาเอกสารสำหรับ Aspose.CAD สำหรับ Java ได้ที่ไหน

 A2: โปรดดูที่[เอกสารประกอบ](https://reference.aspose.com/cad/java/) เพื่อข้อมูลที่ครบถ้วน

### คำถามที่ 3: มีการทดลองใช้ฟรีหรือไม่?

A3: ได้ คุณสามารถทดลองใช้งานฟรีได้จาก[ลิงค์นี้](https://releases.aspose.com/).

### คำถามที่ 4: ฉันจะขอรับใบอนุญาตชั่วคราวได้อย่างไร

 A4: เยี่ยมเลย[ที่นี่](https://purchase.aspose.com/temporary-license/) สำหรับรายละเอียดใบอนุญาตชั่วคราว

### Q5: ต้องการความช่วยเหลือหรือมีคำถาม?

 A5: ตรงไปที่[ฟอรั่ม Aspose.CAD](https://forum.aspose.com/c/cad/19) เพื่อสนับสนุนชุมชน
{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}
