---
date: 2026-02-23
description: تعلم كيفية تحويل DWFX إلى PDF وحفظ ملفات CAD كـ PDF باستخدام Aspose.CAD
  للـ Java. دليل سريع لفتح ملفات DWFX وإنشاء ملفات PDF.
linktitle: Open DWFX File
second_title: Aspose.CAD Java API
title: تحويل DWFX إلى PDF باستخدام Aspose.CAD للغة Java
url: /ar/java/cad-file-manipulation/open-dwfx-file/
weight: 10
---

0}} etc. Keep them unchanged.

Make sure no extra spaces.

Proceed to final.{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# تحويل DWFX إلى PDF باستخدام Aspose.CAD للـ Java

## مقدمة

في عالم التصميم السريع اليوم، يحتاج المطورون غالبًا إلى **convert DWFX to PDF** حتى يمكن مشاركة رسومات CAD مع أصحاب المصلحة غير التقنيين. تجعل Aspose.CAD للـ Java هذه المهمة بسيطة، حيث تسمح لك بفتح ملف DWFX، تحويله إلى صورة نقطية، و**save CAD as PDF** ببضع أسطر من الشيفرة فقط. في هذا الدرس سنستعرض العملية بالكامل — من إعداد بيئتك إلى التحقق من ملف PDF النهائي — لتتمكن من التعامل بثقة مع ملفات DWFX في تطبيقات Java الخاصة بك.

## إجابات سريعة
- **What is the primary purpose of this guide?** ما هو الهدف الأساسي من هذا الدليل؟  
  لإظهار كيفية تحويل DWFX إلى PDF باستخدام Aspose.CAD للـ Java.  
- **Which library is required?** ما المكتبة المطلوبة؟  
  Aspose.CAD للـ Java (قم بتنزيله من الموقع الرسمي لـ Aspose).  
- **Do I need a license?** هل أحتاج إلى ترخيص؟  
  الإصدار التجريبي المجاني يعمل للتطوير؛ يتطلب الترخيص التجاري للإنتاج.  
- **Can I open DWFX files directly?** هل يمكنني فتح ملفات DWFX مباشرةً؟  
  نعم، استخدم `Image.load` لفتح ملفات DWFX.  
- **What output format does the example produce?** ما هو تنسيق الإخراج الذي ينتجه المثال؟  
  ملف PDF يُحفظ في دليل الإخراج المحدد.

## ما هو “convert DWFX to PDF”؟

تحويل DWFX إلى PDF يعني أخذ رسم DWFX قائم على المتجهات — يُستخدم عادةً في منتجات Autodesk — وتحويله إلى مستند PDF محمول ومدعوم على نطاق واسع. يتيح ذلك عرضًا وطباعةً ومشاركةً سهلة دون الحاجة إلى برنامج CAD لدى الطرف المستلم.

## لماذا تستخدم Aspose.CAD للـ Java لـ **save CAD as PDF**؟

- **No external dependencies:** لا توجد تبعيات خارجية: واجهة برمجة تطبيقات Java خالصة، لا حاجة لمحركات CAD الأصلية.  
- **High‑fidelity rendering:** عرض عالي الدقة: يحافظ على أوزان الخطوط، الألوان، والطبقات.  
- **Batch processing friendly:** ملائم للمعالجة الدفعية: مثالي لأتمتة الخادم أو الخدمات السحابية.  
- **Cross‑platform:** متعدد المنصات: يعمل على Windows وLinux وmacOS.

## المتطلبات المسبقة

قبل الغوص في الشيفرة، تأكد من وجود ما يلي:

- **Aspose.CAD for Java Library** – قم بتنزيله من [Aspose.CAD for Java download page](https://releases.aspose.com/cad/java/).  
- **Java Development Environment** – JDK 8 أو أحدث، مع IDE أو أداة بناء مفضلة.  
- **DWFX File** – ملف DWFX تجريبي (مثل `Tyrannosaurus.dwfx`) لاختبار التحويل.

## استيراد المساحات الاسمية

أولاً، استورد الفئات التي سنحتاجها:

```java
import com.aspose.cad.Image;

import com.aspose.cad.fileformats.cad.CadImage;
import com.aspose.cad.imageoptions.CadRasterizationOptions;
import com.aspose.cad.imageoptions.PdfOptions;
```

## كيفية تحويل DWFX إلى PDF باستخدام Aspose.CAD للـ Java

فيما يلي تفصيل خطوة بخطوة. كل خطوة تتضمن شرحًا قصيرًا يليه الشيفرة الدقيقة التي ستنفذها.

### الخطوة 1: تحميل ملف DWFX  

```java
String SourceDir = Utils.getDataDir_DWFXDrawings();
String OutputDir = Utils.getDataDir_Output();
String filePath = SourceDir + "Tyrannosaurus.dwfx";

Image cadImageDwf = Image.load(filePath);
```

طريقة `Image.load` تقرأ ملف DWFX إلى الذاكرة، وتمنحنا كائن `CadImage` جاهزًا للتحويل النقطي.

### الخطوة 2: تعيين خيارات التحويل النقطي  

```java
CadRasterizationOptions rasterizationOptions = new CadRasterizationOptions();
rasterizationOptions.setPageWidth(cadImageDwf.getSize().getWidth());
rasterizationOptions.setPageHeight(cadImageDwf.getSize().getHeight());
```

تحدد هذه الخيارات حجم الصفحة الناتجة، مما يضمن أن يتطابق PDF مع أبعاد الرسم الأصلي.

### الخطوة 3: تكوين خيارات PDF  

```java
PdfOptions CADf = new PdfOptions();
CADf.setVectorRasterizationOptions(rasterizationOptions);
```

هنا نربط إعدادات التحويل النقطي بتكوين تصدير PDF.

### الخطوة 4: حفظ كملف PDF  

```java
cadImageDwf.save(OutputDir + "OpenDwfxFile_out.pdf", CADf);
```

استدعاء `save` يكتب الصورة المُحوَّلة إلى ملف PDF في مجلد الإخراج.

### الخطوة 5: التحقق من النجاح  

```java
System.out.println("OpenDwfxFile executed successfully");
```

رسالة بسيطة في وحدة التحكم تؤكد أن التحويل اكتمل دون أخطاء.

## المشكلات الشائعة والحلول

| المشكلة | السبب المحتمل | الحل |
|-------|--------------|----------|
| **Blank PDF output** | تم ضبط عرض/ارتفاع التحويل النقطي إلى 0 | تأكد من أن `cadImageDwf.getSize()` يعيد أبعادًا صالحة قبل ضبط الخيارات. |
| **Out‑of‑memory error** | ملف DWFX كبير جدًا | زيادة حجم الذاكرة المخصصة للـ JVM (`-Xmx2g`) أو معالجة الملف بأقسام أصغر. |
| **Missing fonts** | الخط غير مضمن في ملف DWFX المصدر | قم بتثبيت الخطوط المطلوبة على الخادم أو استخدم `CadRasterizationOptions.setFontName` لتحديد بديل. |

## الأسئلة المتكررة

### Q1: هل يمكنني استخدام Aspose.CAD للـ Java مع صيغ CAD أخرى؟
نعم، يدعم Aspose.CAD للـ Java مجموعة واسعة من صيغ CAD، مما يوفر حلاً متعدد الاستخدامات للمطورين.

### Q2: هل تتوفر نسخة تجريبية مجانية لـ Aspose.CAD للـ Java؟
نعم، يمكنك استكشاف قدرات Aspose.CAD للـ Java من خلال نسخة تجريبية مجانية. زر [this link](https://releases.aspose.com/) للبدء.

### Q3: كيف يمكنني الحصول على دعم لـ Aspose.CAD للـ Java؟
انضم إلى مجتمع Aspose.CAD على [support forum](https://forum.aspose.com/c/cad/19) للحصول على المساعدة والتعاون.

### Q4: هل تتوفر تراخيص مؤقتة لـ Aspose.CAD للـ Java؟
نعم، يمكنك الحصول على ترخيص مؤقت لـ Aspose.CAD للـ Java. زر [this link](https://purchase.aspose.com/temporary-license/) لمزيد من التفاصيل.

### Q5: أين يمكنني العثور على الوثائق الخاصة بـ Aspose.CAD للـ Java؟
الوثائق الشاملة متاحة [here](https://reference.aspose.com/cad/java/).

---

**آخر تحديث:** 2026-02-23  
**تم الاختبار مع:** Aspose.CAD للـ Java 24.11  
**المؤلف:** Aspose  

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}