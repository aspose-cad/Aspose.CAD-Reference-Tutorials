---
date: 2025-12-21
description: تعلم كيفية تصدير تخطيطات CAD إلى PDF باستخدام Aspose.CAD للغة Java –
  طريقة سريعة وموثوقة لإنشاء PDF من ملفات CAD.
linktitle: Export CAD Layouts to PDF
second_title: Aspose.CAD Java API
title: كيفية تصدير تخطيطات CAD إلى PDF باستخدام Aspose.CAD للـ Java
url: /ar/java/cad-export-options/export-cad-layouts-to-pdf/
weight: 11
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# كيفية تصدير تخطيطات CAD إلى PDF باستخدام Aspose.CAD للـ Java

## المقدمة

في هذا الدرس، سنوضح لك **كيفية تصدير تخطيطات CAD** إلى PDF باستخدام Aspose.CAD للـ Java. سواء كنت تعمل مع ملفات DWG أو DXF أو أي صيغ CAD أخرى، فإن هذا الدليل يرشّحك إلى نهج برمجي نظيف لتوليد PDF من ملفات CAD بسرعة وبشكل موثوق.

## إجابات سريعة
- **ماذا تفعل المكتبة؟** تقوم بتحويل رسومات CAD (DWG، DXF، DWF، إلخ) إلى PDF، صور نقطية، وصيغ أخرى.  
- **ما اللغة المستخدمة؟** Java – يعمل الكود على أي منصة متوافقة مع JVM.  
- **هل أحتاج إلى ترخيص؟** يتوفر نسخة تجريبية مجانية؛ يلزم الحصول على ترخيص تجاري للاستخدام في الإنتاج.  
- **هل يمكنني تحويل DWG إلى PDF في Java؟** نعم – نفس الـ API يدعم تحويلات **dwg to pdf java**.  
- **ما هي الخطوات الرئيسية؟** تحميل ملف CAD، ضبط خيارات الرستر، تكوين خيارات PDF، ثم حفظ النتيجة.

## المتطلبات المسبقة

قبل الغوص في الدرس، تأكد من توفر المتطلبات التالية:

- Aspose.CAD للـ Java: تأكد من تثبيت المكتبة. يمكنك تحميلها من موقع Aspose [هنا](https://releases.aspose.com/cad/java/).

- بيئة تطوير Java: تأكد من إعداد بيئة تطوير Java على جهازك.

الآن بعد أن تم إعداد كل شيء، لنبدأ الدرس.

## ما هو “كيفية تصدير CAD”؟

تصدير CAD يعني تحويل بيانات الرسم الأصلية (مثل DWG أو DXF أو DWF) إلى صيغة أكثر قابلية للقراءة عالميًا مثل PDF. هذه العملية أساسية لمشاركة التصاميم مع أصحاب المصلحة الذين قد لا يمتلكون برنامج CAD.

## لماذا نستخدم Aspose.CAD للـ Java لتصدير CAD إلى PDF؟

- **دقة عالية** – يتم الحفاظ على الرسومات المتجهة، وتتيح خيارات الرستر ضبط الجودة بدقة.  
- **بدون تبعيات خارجية** – جافا صافية، لا تحتاج إلى DLLs أو مكونات COM.  
- **يدعم صيغًا متعددة** – يمكنك أيضًا **generate pdf from cad** للملفات التي تم إنشاؤها بـ DWG أو DWF أو صيغ أخرى.  
- **قابلية التوسع للوظائف الدفعية** – مثالي لأتمتة الخوادم، خطوط CI، أو أدوات سطح المكتب.

## استيراد المساحات الاسمية

في كود Java الخاص بك، ابدأ باستيراد المساحات الاسمية اللازمة. هذه الاستيرادات توفر الوصول إلى الفئات والطرق المطلوبة للعمل مع Aspose.CAD للـ Java.

```java
import com.aspose.cad.Image;
import com.aspose.cad.InterpolationMode;
import com.aspose.cad.SmoothingMode;
import com.aspose.cad.TextRenderingHint;

import com.aspose.cad.imageoptions.CadRasterizationOptions;
import com.aspose.cad.imageoptions.PdfOptions;
//import com.aspose.cad.imageoptions.TypeOfEntities;
```

## الخطوة 1: تحميل ملف CAD

ابدأ بتحميل ملف CAD إلى تطبيق Java باستخدام طريقة `Image.load`. استبدل `"conic_pyramid.dxf"` بمسار ملف CAD الخاص بك.

```java
String dataDir = "Your Document Directory" + "ExportingCAD/";
String srcFile = dataDir + "conic_pyramid.dxf";
Image cadImage = Image.load(srcFile);
```

## الخطوة 2: ضبط خيارات الرستر

أنشئ كائنًا من `CadRasterizationOptions` لتحديد كيفية رستر الكيانات في CAD. عدّل معلمات مثل عرض الصفحة، ارتفاع الصفحة، وتوسيع التخطيط وفقًا لمتطلباتك.

```java
CadRasterizationOptions rasterizationOptions = new CadRasterizationOptions();
rasterizationOptions.setPageWidth(1600);
rasterizationOptions.setPageHeight(1600);
rasterizationOptions.setAutomaticLayoutsScaling(true);
rasterizationOptions.setNoScaling(false);
rasterizationOptions.setContentAsBitmap(true);
rasterizationOptions.setLayouts(new String[]{"Model"});
```

## الخطوة 3: ضبط خيارات PDF

أنشئ كائنًا من `PdfOptions` واربطه بخيارات الرستر. بالإضافة إلى ذلك، اضبط خيارات الرسومات لتصدير PDF، مثل وضع التنعيم، تلميح عرض النص، ووضع الاستيفاء.

```java
PdfOptions pdfOptions = new PdfOptions();
pdfOptions.setVectorRasterizationOptions(rasterizationOptions);
rasterizationOptions.getGraphicsOptions().setSmoothingMode(SmoothingMode.HighQuality);
rasterizationOptions.getGraphicsOptions().setTextRenderingHint(TextRenderingHint.AntiAliasGridFit);
rasterizationOptions.getGraphicsOptions().setInterpolationMode(InterpolationMode.HighQualityBicubic);
```

## الخطوة 4: التصدير إلى PDF

أخيرًا، صدّر تخطيطات CAD إلى ملف PDF باستخدام طريقة `save` لكائن `cadImage`.

```java
cadImage.save(dataDir + "CADLayoutsToPDF_out_.pdf", pdfOptions);
```

## المشكلات الشائعة والحلول

| المشكلة | السبب | الحل |
|-------|--------|-----|
| **ملف PDF فارغ** | خيارات الرستر غير مضبوطة بشكل صحيح (مثل عدم تطابق اسم التخطيط) | تحقق من أن `rasterizationOptions.setLayouts()` يطابق أسماء التخطيطات في ملف CAD الخاص بك. |
| **صور منخفضة الدقة** | `PageWidth`/`PageHeight` صغيرة جدًا | زد أبعاد الصفحة أو اضبط DPI أعلى عبر `rasterizationOptions.setResolution()`. |
| **إصدار CAD غير مدعوم** | قد تحتاج إصدارات DWG/DXF القديمة إلى نسخة أحدث من Aspose.CAD | حمّل أحدث نسخة من المكتبة من موقع Aspose. |

## الأسئلة المتكررة

### س1: هل يمكنني استخدام Aspose.CAD للـ Java مع صيغ CAD أخرى؟

ج1: نعم، يدعم Aspose.CAD صيغ CAD متعددة، بما في ذلك DWG، DXF، DWF، وأكثر. راجع الوثائق [هنا](https://reference.aspose.com/cad/java/) للقائمة الكاملة.

### س2: هل تتوفر نسخة تجريبية مجانية لـ Aspose.CAD للـ Java؟

ج2: نعم، يمكنك تجربة ميزات Aspose.CAD عبر نسخة تجريبية مجانية [هنا](https://releases.aspose.com/).

### س3: كيف يمكنني الحصول على دعم لـ Aspose.CAD للـ Java؟

ج3: زر منتدى Aspose.CAD [هنا](https://forum.aspose.com/c/cad/19) للحصول على دعم المجتمع. للدعم المميز، فكر في شراء ترخيص [هنا](https://purchase.aspose.com/buy).

### س4: ما الفرق بين توسيع التخطيط التلقائي واليدوي؟

ج4: توسيع التخطيط التلقائي يضبط حجم التخطيط بناءً على أبعاد الصفحة المحددة، بينما يتيح التوسيع اليدوي ضبط قيم مخصصة للتوسيع.

### س5: هل يمكنني تخصيص مظهر ملفات PDF المصدرة؟

ج5: نعم، يمكنك تعديل خيارات الرسومات في الكود للتحكم في الجودة والمظهر النهائي لملف PDF المصدّر.

### س6: هل يدعم Aspose.CAD تحويل **dwg to pdf java** مباشرة؟

ج6: بالتأكيد. نفس خيارات الرستر وPDF تعمل مع ملفات DWG، مما يتيح تحويلات **dwg to pdf java** سلسة.

### س7: هل هناك طريقة **generate pdf from cad** دون رستر إلى صورة نقطية؟

ج7: عبر ضبط `rasterizationOptions.setContentAsBitmap(false)` يمكنك الحفاظ على البيانات المتجهة حيثما أمكن، مما ينتج PDF قائم على المتجهات فعليًا.

---

**آخر تحديث:** 2025-12-21  
**تم الاختبار مع:** Aspose.CAD للـ Java 24.10  
**المؤلف:** Aspose  

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}