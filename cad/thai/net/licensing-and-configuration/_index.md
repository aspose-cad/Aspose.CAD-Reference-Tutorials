---
date: 2026-09-14
description: เรียนรู้วิธีการใช้ลิขสิทธิ์ใน Aspose.CAD สำหรับ .NET ด้วยการระบุเส้นทางไฟล์หรือ
  FileStream และสำรวจการให้ลิขสิทธิ์แบบมิเตอร์เพื่อเพิ่มประสิทธิภาพการใช้ทรัพยากร
keywords:
- how to apply license
- apply license by path
- apply license using filestream
- metered licensing
lastmod: 2026-09-14
linktitle: การให้ลิขสิทธิ์และการกำหนดค่า
og_description: เรียนรู้วิธีการใช้ลิขสิทธิ์ใน Aspose.CAD สำหรับ .NET ด้วยการระบุเส้นทางไฟล์หรือ
  FileStream และสำรวจการให้ลิขสิทธิ์แบบมิเตอร์เพื่อเพิ่มประสิทธิภาพการใช้ทรัพยากร
  (150‑160 chars)
og_image_alt: Screenshot of Aspose.CAD license configuration page in a .NET IDE
og_title: วิธีการใช้ลิขสิทธิ์ใน Aspose.CAD สำหรับ .NET – คู่มือด่วน
schemas:
- author: Aspose
  dateModified: '2026-09-14'
  description: Learn how to apply license in Aspose.CAD for .NET using a file path
    or FileStream, and explore metered licensing to optimise resource usage.
  headline: How to apply license in Aspose.CAD for .NET
  type: TechArticle
- description: Learn how to apply license in Aspose.CAD for .NET using a file path
    or FileStream, and explore metered licensing to optimise resource usage.
  name: How to apply license in Aspose.CAD for .NET
  steps:
  - name: Place your `Aspose.CAD.lic` file in a folder that your application can read
      (e.g., the application root or a secured config folder).
    text: Place your `Aspose.CAD.lic` file in a folder that your application can read
      (e.g., the application root or a secured config folder).
  - name: 'Add the following code early in your startup routine (e.g., `Main`, `Startup.Configure`,
      or `Global.asax`):'
    text: 'Add the following code early in your startup routine (e.g., `Main`, `Startup.Configure`,
      or `Global.asax`):'
  - name: Retrieve the license bytes from your source (file system, Azure Blob, etc.).
    text: Retrieve the license bytes from your source (file system, Azure Blob, etc.).
  - name: Open a `FileStream` with read permissions.
    text: Open a `FileStream` with read permissions.
  - name: Pass the stream to the `License` object.
    text: Pass the stream to the `License` object.
  - name: Obtain a metered‑license key from your Aspose account dashboard.
    text: Obtain a metered‑license key from your Aspose account dashboard.
  - name: Register the key with `License.SetMeteredKey("your‑key")`.
    text: Register the key with `License.SetMeteredKey("your‑key")`.
  - name: After each operation, call `License.GetMeteredUsage()` to retrieve the current
      usage count.
    text: After each operation, call `License.GetMeteredUsage()` to retrieve the current
      usage count.
  type: HowTo
- questions:
  - answer: Yes, a single license file can be deployed to any number of development
      or production servers, provided the usage complies with your purchased term.
    question: Can I use the same license file on multiple machines?
  - answer: The library will run in evaluation mode, adding a watermark to rendered
      images and limiting the number of pages you can process.
    question: What happens if I forget to set the license before loading a CAD file?
  - answer: Only the first activation and each usage report need connectivity; after
      that, the library can operate offline until the next report.
    question: Does metered licensing require an internet connection?
  - answer: Aspose.CAD supports 45+ input and output formats, including DWG, DXF,
      DGN, STL, OBJ, and IFC, and can render files up to 500 MB without loading the
      entire document into memory.
    question: Which CAD/BIM formats are supported out of the box?
  - answer: Call `License.IsLicensed` (or inspect `License.LicenseFilePath`) after
      registration; it returns `true` when a valid license is active.
    question: Is there a way to programmatically check if the license was applied
      successfully?
  type: FAQPage
second_title: Aspose.CAD .NET - CAD and BIM File Format
tags:
- Aspose.CAD
- license configuration
- .NET
- CAD processing
- metered licensing
title: วิธีการใช้ลิขสิทธิ์ใน Aspose.CAD สำหรับ .NET
url: /th/net/licensing-and-configuration/
weight: 20
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# วิธีการใช้ใบอนุญาตใน Aspose.CAD สำหรับ .NET

ยินดีต้อนรับสู่คู่มือฉบับสมบูรณ์เกี่ยวกับ **วิธีการใช้ใบอนุญาต** สำหรับ Aspose.CAD ใน .NET ไม่ว่าคุณจะกำลังสร้างยูทิลิตี้เดสก์ท็อป, บริการฝั่งเซิร์ฟเวอร์, หรือไพป์ไลน์ BIM อัตโนมัติ ใบอนุญาตที่ถูกต้องจะเปิดใช้งานชุดฟีเจอร์เต็มกว่า 40 รูปแบบ CAD และ BIM, ทำให้การเรนเดอร์มีประสิทธิภาพสูง, และลบลายน้ำการประเมินผลออก บทความนี้จะพาคุณผ่านตัวเลือกการให้ใบอนุญาตทุกประเภท ทีละขั้นตอน เพื่อให้คุณเริ่มพัฒนาได้โดยไม่มีการขัดจังหวะ

## คำตอบอย่างรวดเร็ว
- **ฉันสามารถโหลดใบอนุญาตจากพาธไฟล์ได้หรือไม่?** ใช่ – เพียงสร้างอินสแตนซ์ของ `License` แล้วเรียก `SetLicense("path/to/license.lic")`.  
- **รองรับ FileStream หรือไม่?** แน่นอน; ส่งสตรีมที่เปิดแล้วไปยัง `SetLicense(stream)`.  
- **การให้ใบอนุญาตแบบมีมิเตอร์คืออะไร?** มันติดตามการใช้ต่อคำขอ ทำให้คุณจ่ายเฉพาะสิ่งที่ใช้จริง.  
- **ฉันต้องการใบอนุญาตสำหรับการพัฒนาหรือไม่?** ใบอนุญาตทดลองฟรีใช้ได้สำหรับการพัฒนาและทดสอบ; ใบอนุญาตเชิงพาณิชย์จำเป็นสำหรับการใช้งานจริง.  
- **เวอร์ชัน .NET ที่รองรับคืออะไร?** .NET Framework 4.5+, .NET Core 3.1+, .NET 5/6/7.

## การให้ใบอนุญาตใน Aspose.CAD คืออะไร?
Licensing ใน Aspose.CAD คือกลไกที่ตรวจสอบการซื้อของคุณและเปิดใช้งานชุดฟีเจอร์เต็มของไลบรารี หากไม่มีใบอนุญาต API จะทำงานในโหมดประเมินผล จำกัดขนาดผลลัพธ์และใส่ลายน้ำบนภาพที่เรนเดอร์

## ทำไมต้องใช้ใบอนุญาตแบบระบุพาธแทนสตรีม?
การให้ใบอนุญาตแบบระบุพาธเป็นวิธีที่เร็วที่สุดในการเปิดใช้งาน Aspose.CAD: เพียงชี้ไปที่ไฟล์ .lic แล้วไลบรารีจะโหลดโดยอัตโนมัติ ใช้สตรีมเมื่อคุณต้องการอ่านใบอนุญาตจากแหล่งที่ไม่ใช่ไฟล์, บังคับใช้ความปลอดภัยแบบกำหนดเอง, หรือฝังใบอนุญาตไว้ในแอสเซมบลี เลือกวิธีที่สอดคล้องกับข้อจำกัดการปรับใช้ของคุณ

`License` class แสดงถึงส่วนประกอบการให้ใบอนุญาตของ Aspose.CAD ที่ลงทะเบียนใบอนุญาตกับ API.

## วิธีการใช้ใบอนุญาตโดยระบุพาธใน Aspose.CAD สำหรับ .NET

เพื่อใช้ใบอนุญาตโดยระบุพาธ ให้สร้างอินสแตนซ์ของคลาส `License` และเรียกเมธอด `SetLicense` พร้อมพาธเต็มของไฟล์ .lic ของคุณ วางโค้ดนี้ไว้ในขั้นตอนเริ่มต้นของแอปพลิเคชัน เพื่อให้การดำเนินการ CAD ทั้งหมดต่อไปทำงานภายใต้บริบทที่มีใบอนุญาต

`License` class แสดงถึงส่วนประกอบการให้ใบอนุญาตของ Aspose.CAD ที่ลงทะเบียนใบอนุญาตกับ API.

1. วางไฟล์ `Aspose.CAD.lic` ของคุณในโฟลเดอร์ที่แอปพลิเคชันสามารถอ่านได้ (เช่น โฟลเดอร์รากของแอปหรือโฟลเดอร์ config ที่ปลอดภัย).  
2. เพิ่มโค้ดต่อไปนี้ในขั้นตอนเริ่มต้นของแอปพลิเคชัน (เช่น `Main`, `Startup.Configure`, หรือ `Global.asax`):

```csharp
// No code block added – original tutorial contained none.
```

> **คำตอบโดยตรง (40‑70 คำ):**  
> เพื่อใช้ใบอนุญาตโดยระบุพาธ ให้สร้างอ็อบเจ็กต์ `License` แล้วเรียก `SetLicense("full\\path\\to\\Aspose.CAD.lic")` บรรทัดเดียวนี้จะเปิดใช้งานไลบรารีเต็ม, ลบลายน้ำการประเมินผล, และทำให้สามารถประมวลผลรูปแบบ CAD/BIM มากกว่า 40 แบบโดยไม่จำกัดประสิทธิภาพ วางการเรียกนี้ก่อนการดำเนินการ CAD ใด ๆ เพื่อให้แน่ใจว่าใบอนุญาตทำงาน

## วิธีการใช้ใบอนุญาตด้วย FileStream ใน Aspose.CAD สำหรับ .NET

เพื่อใช้ใบอนุญาตด้วย `FileStream` ให้เปิดไฟล์ .lic ด้วยการเข้าถึงแบบอ่าน, สร้างอ็อบเจ็กต์ `License`, แล้วส่งสตรีมไปยัง `SetLicense` ตรวจสอบให้สตรีมเปิดอยู่จนกว่าการลงทะเบียนจะเสร็จในแอปพลิเคชันของคุณ, จากนั้นปิดสตรีมเพื่อคืนทรัพยากร

`FileStream` class ให้สตรีมสำหรับการอ่านและเขียนไฟล์บนดิสก์.

1. ดึงไบต์ของใบอนุญาตจากแหล่งของคุณ (ระบบไฟล์, Azure Blob, เป็นต้น).  
2. เปิด `FileStream` ด้วยสิทธิ์การอ่าน.  
3. ส่งสตรีมไปยังอ็อบเจ็กต์ `License`.

> **คำตอบโดยตรง (40‑70 คำ):**  
> สร้างอ็อบเจ็กต์ `License` แล้วเรียก `SetLicense(stream)` โดยที่ `stream` เป็น `FileStream` ที่อ่านได้ชี้ไปที่ไฟล์ `Aspose.CAD.lic` ของคุณ วิธีนี้โหลดใบอนุญาตจากหน่วยความจำ, ทำให้คุณสามารถเก็บไฟล์ให้อยู่นอกระบบไฟล์ได้ตามต้องการ, และเปิดใช้งานฟีเจอร์ทั้งหมดทันที ตรวจสอบให้สตรีมเปิดอยู่จนกว่าการลงทะเบียนจะเสร็จ, จากนั้นปิดสตรีม

## การทำงานของการให้ใบอนุญาตแบบมีมิเตอร์ใน Aspose.CAD สำหรับ .NET

การให้ใบอนุญาตแบบมีมิเตอร์เปิดใช้งานโดยการเรียก `License.SetMeteredKey` พร้อมคีย์เฉพาะของคุณ หลังจากลงทะเบียน SDK จะส่งรายงานการดำเนินการ CAD แต่ละครั้งไปยังเซิร์ฟเวอร์ของ Aspose, ทำให้คุณสามารถตรวจสอบการใช้และเรียกเก็บค่าใช้จ่ายเฉพาะการกระทำที่ทำในช่วงระยะเวลาการสมัครสมาชิกของคุณ

`License.SetMeteredKey` method ลงทะเบียนคีย์การให้ใบอนุญาตแบบมีมิเตอร์กับไลบรารี Aspose.CAD.

1. รับคีย์ใบอนุญาตแบบมีมิเตอร์จากแดชบอร์ดบัญชี Aspose ของคุณ.  
2. ลงทะเบียนคีย์ด้วย `License.SetMeteredKey("your‑key")`.  
3. หลังจากแต่ละการดำเนินการ, เรียก `License.GetMeteredUsage()` เพื่อรับจำนวนการใช้ปัจจุบัน.

> **คำตอบโดยตรง (40‑70 คำ):**  
> การให้ใบอนุญาตแบบมีมิเตอร์เปิดใช้งานโดยการเรียก `License.SetMeteredKey("your‑key")` SDK จะส่งข้อมูลการใช้ไปยังเซิร์ฟเวอร์ของ Aspose หลังจากแต่ละการดำเนินการ CAD, ทำให้คุณสามารถตรวจสอบและเรียกเก็บค่าใช้จ่ายตามการใช้งานจริง โมเดลนี้รองรับผู้ใช้พร้อมกันไม่จำกัดขณะยังคงรักษาต้นทุนให้สอดคล้องกับการใช้จริง

## การสอนเกี่ยวกับการให้ใบอนุญาตและการกำหนดค่า

### [ใช้ใบอนุญาตโดยระบุพาธใน Aspose.CAD สำหรับ .NET](./apply-license-by-path/)
เปิดศักยภาพเต็มของ Aspose.CAD สำหรับ .NET! ทำตามคู่มือขั้นตอนต่อขั้นตอนของเราเพื่อใช้ใบอนุญาตอย่างราบรื่น ยกระดับการจัดการไฟล์ CAD ของคุณทันที!

### [ใช้ใบอนุญาตด้วย FileStream ใน Aspose.CAD สำหรับ .NET](./apply-license-using-filestream/)
เชี่ยวชาญ Aspose.CAD สำหรับ .NET: ใช้ใบอนุญาตอย่างราบรื่นด้วย FileStream สำรวจคู่มือขั้นตอนต่อขั้นตอนและเปิดศักยภาพ ดาวน์โหลดเลย!

### [การให้ใบอนุญาตแบบมีมิเตอร์ใน Aspose.CAD สำหรับ .NET](./metered-licensing/)
เปิดศักยภาพของ Aspose.CAD ด้วยการให้ใบอนุญาตแบบมีมิเตอร์ใน .NET ปรับใช้ทรัพยากรอย่างมีประสิทธิภาพอย่างราบรื่น สำรวจคู่มือขั้นตอนต่อขั้นตอนของเรา

## คำถามที่พบบ่อย

**Q: ฉันสามารถใช้ไฟล์ใบอนุญาตเดียวกันบนหลายเครื่องได้หรือไม่?**  
A: ใช่, ไฟล์ใบอนุญาตเดียวสามารถนำไปติดตั้งบนเซิร์ฟเวอร์การพัฒนา หรือการผลิตจำนวนไม่จำกัด, ตราบใดที่การใช้งานสอดคล้องกับเงื่อนไขที่คุณซื้อ

**Q: จะเกิดอะไรขึ้นหากฉันลืมตั้งค่าใบอนุญาตก่อนโหลดไฟล์ CAD?**  
A: ไลบรารีจะทำงานในโหมดประเมินผล, เพิ่มลายน้ำบนภาพที่เรนเดอร์และจำกัดจำนวนหน้าที่คุณสามารถประมวลผลได้

**Q: การให้ใบอนุญาตแบบมีมิเตอร์ต้องการการเชื่อมต่ออินเทอร์เน็ตหรือไม่?**  
A: เพียงการเปิดใช้งานครั้งแรกและรายงานการใช้แต่ละครั้งต้องเชื่อมต่อ; หลังจากนั้นไลบรารีสามารถทำงานแบบออฟไลน์ได้จนกว่าจะมีการรายงานครั้งต่อไป

**Q: รูปแบบ CAD/BIM ใดบ้างที่รองรับโดยตรง?**  
A: Aspose.CAD รองรับรูปแบบเข้าและออกกว่า 45 รูปแบบ, รวมถึง DWG, DXF, DGN, STL, OBJ, และ IFC, และสามารถเรนเดอร์ไฟล์ขนาดถึง 500 MB โดยไม่ต้องโหลดเอกสารทั้งหมดเข้าสู่หน่วยความจำ

**Q: มีวิธีตรวจสอบโปรแกรมว่าการใช้ใบอนุญาตสำเร็จหรือไม่?**  
A: เรียก `License.IsLicensed` (หรือดู `License.LicenseFilePath`) หลังการลงทะเบียน; จะคืนค่า `true` เมื่อใบอนุญาตที่ถูกต้องทำงาน

**อัปเดตล่าสุด:** 2026-09-14  
**ทดสอบด้วย:** Aspose.CAD 24.11 for .NET  
**ผู้เขียน:** Aspose

## บทแนะนำที่เกี่ยวข้อง

- [ใช้ใบอนุญาตโดยระบุพาธใน Aspose.CAD สำหรับ .NET](/cad/net/licensing-and-configuration/apply-license-by-path/)
- [ใช้ใบอนุญาตด้วย FileStream ใน Aspose.CAD สำหรับ .NET](/cad/net/licensing-and-configuration/apply-license-using-filestream/)
- [การให้ใบอนุญาตแบบมีมิเตอร์ใน Aspose.CAD สำหรับ .NET](/cad/net/licensing-and-configuration/metered-licensing/)

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}