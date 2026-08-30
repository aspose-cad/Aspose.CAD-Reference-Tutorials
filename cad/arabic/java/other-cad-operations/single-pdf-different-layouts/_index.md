---
date: 2026-06-29
description: تعلم كيفية إنشاء PDF من DWG وتخصيص تخطيط PDF باستخدام Aspose.CAD for
  Java. دمج سهل لمطوري Java.
keywords:
- create pdf from dwg
- convert cad to pdf
- pdf different page sizes
- export dwg to pdf
- customize pdf layout
linktitle: PDF واحد بتخطيطات مختلفة
schemas:
- author: Aspose
  dateModified: '2026-06-29'
  description: Learn how to create PDF from DWG and customize PDF layout using Aspose.CAD
    for Java. Easy integration for Java developers.
  headline: Create PDF from DWG with Aspose.CAD for Java
  type: TechArticle
- questions:
  - answer: Yes, Aspose.CAD for Java integrates seamlessly with libraries such as
      Apache POI, Jackson, or Spring Boot.
    question: Can I use Aspose.CAD for Java with other Java libraries?
  - answer: Absolutely! You can access a free trial version [here](https://releases.aspose.com/).
    question: Is there a trial version available?
  - answer: Visit the [Aspose.CAD forum](https://forum.aspose.com/c/cad/19) for community
      support and discussions.
    question: Where can I find additional support?
  - answer: You can obtain a temporary license [here](https://purchase.aspose.com/temporary-license/).
    question: How do I obtain a temporary license?
  - answer: Purchase the full version of Aspose.CAD for Java [here](https://purchase.aspose.com/buy).
    question: Where can I purchase the full version?
  type: FAQPage
second_title: Aspose.CAD Java API
title: إنشاء PDF من DWG باستخدام Aspose.CAD for Java
url: /ar/java/other-cad-operations/single-pdf-different-layouts/
weight: 16
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# إنشاء PDF من DWG باستخدام Aspose.CAD للـ Java

## مقدمة

في هذا الدرس سوف **تنشئ PDF من ملفات DWG** وتطبق عدة تخطيطات بأحجام صفحات مختلفة باستخدام Aspose.CAD للـ Java. سواء كنت بحاجة إلى إنشاء مخططات بناء، أو مخططات هندسية، أو ملفات PDF جاهزة للتسويق، فإن الخطوات أدناه توضح لك كيفية تحويل رسومات CAD إلى PDF، وتخصيص أبعاد كل تخطيط، وإنتاج مستند واحد متعدد الصفحات — كل ذلك دون مغادرة بيئة Java الخاصة بك.

## إجابات سريعة
- **ما الذي يغطيه الدرس؟** تحويل رسم DWG إلى PDF واحد بأحجام صفحات متعددة.  
- **ما المكتبة المطلوبة؟** Aspose.CAD للـ Java (أحدث إصدار).  
- **هل أحتاج إلى رخصة؟** النسخة التجريبية المجانية تكفي للتطوير؛ تحتاج إلى رخصة تجارية للإنتاج.  
- **هل يمكنني تصدير صيغ أخرى؟** نعم – الواجهة البرمجية تدعم أيضاً التصدير إلى PNG و JPEG و SVG.  
- **هل Java 8 كافية؟** المكتبة تعمل مع Java 8 والإصدارات الأحدث.

## ما هو “إنشاء PDF من DWG”؟

**إنشاء PDF من DWG** يعني تحويل ملف AutoCAD DWG الأصلي إلى مستند PDF مع الحفاظ على دقة المتجهات، والطبقات، وسمك الخطوط، والسماح بتخصيص التخطيط. تقوم Aspose.CAD بهذا التحويل بالكامل في الذاكرة، لذا لا يلزم أي برنامج CAD خارجي، ويمكن تحرير أو طباعة PDF الناتج مباشرة.

## لماذا تخصيص تخطيط PDF من DWG؟

تدعم Aspose.CAD **أكثر من 30 صيغة CAD** ويمكنها إنشاء ملفات PDF تصل إلى **500 ميغابايت** دون تحميل الملف بالكامل في الذاكرة. من خلال تعريف أحجام صفحات فردية لكل تخطيط، يمكنك إنتاج أوراق قابلة للطباعة تتطابق مع معايير ISO أو ANSI أو أبعاد مخصصة – فائدة ملموسة توفر الوقت وتلغي المعالجة اليدوية بعد التحويل.

## المتطلبات المسبقة

قبل الشروع في هذه العملية، تأكد من توفر المتطلبات التالية:
- بيئة Java: تأكد من تثبيت Java على جهازك.  
- مكتبة Aspose.CAD: قم بتنزيل وتثبيت مكتبة Aspose.CAD للـ Java من [رابط التنزيل](https://releases.aspose.com/cad/java/).  
- دليل المستندات: أنشئ مجلدًا لرسومات DWG الخاصة بك.

## استيراد الحزم

الفئة `CadImage` هي الكائن الأساسي في Aspose.CAD الذي يمثل رسم CAD في الذاكرة. استورد المساحات الاسمية المطلوبة قبل البدء:

```java
import com.aspose.cad.Image;
import com.aspose.cad.SizeF;
import com.aspose.cad.fileformats.cad.CadImage;
import com.aspose.cad.imageoptions.CadRasterizationOptions;
import com.aspose.cad.imageoptions.PdfOptions;
import com.aspose.cad.imageoptions.VectorRasterizationOptions;
```

## الخطوة 1: تحميل رسم CAD

`CadImage` يحمل ملف DWG ويوفر الوصول إلى بياناته المتجهية. ابدأ بتحميل رسم CAD الخاص بك إلى كائن `CadImage`:

```java
String dataDir = "Your Document Directory" + "DWGDrawings/";
CadImage cadImage = (CadImage)Image.load(dataDir + "City skyway map.dwg");
```

## الخطوة 2: تكوين خيارات التحويل إلى نقطية

`RasterizationOptions` تحدد كيفية تحويل المتجهات إلى نقطية قبل وضعها في PDF. اضبط خيارات التحويل إلى نقطية لصورة CAD:

```java
CadRasterizationOptions rasterizationOptions = new CadRasterizationOptions();
rasterizationOptions.setPageWidth(1000);
rasterizationOptions.setPageHeight(1000);
```

## الخطوة 3: تخصيص أحجام صفحات التخطيط

`PdfOptions` تسمح لك بتعيين أبعاد صفحات مميزة لكل تخطيط داخل DWG. عرّف أحجامًا مخصصة لعدة تخطيطات داخل رسم CAD:

```java
rasterizationOptions.getLayoutPageSizes().addItem("ANSI C Plot", new SizeF(500, 1000));
rasterizationOptions.getLayoutPageSizes().addItem("8.5 x 11 Plot", new SizeF(1000, 100));
```

## الخطوة 4: ضبط خيارات PDF

`PdfOptions` هو الحاوية التي تجمع بين إعدادات التحويل إلى نقطية وتعريفات التخطيطات. قم بتهيئة خيارات PDF، مع دمج إعدادات التحويل إلى نقطية:

```java
PdfOptions pdfOptions = new PdfOptions();
pdfOptions.setVectorRasterizationOptions(rasterizationOptions);
```

## الخطوة 5: حفظ كملف PDF

`PdfSaveOptions` ينهى عملية التحويل ويكتب ملف الإخراج. احفظ صورة CAD المعالجة كملف PDF:

```java
cadImage.save(dataDir + "singlePDF_out.pdf", pdfOptions);
```

تهانينا! لقد نجحت في **إنشاء PDF من DWG** بأحجام صفحات مختلفة باستخدام Aspose.CAD للـ Java.

## المشكلات الشائعة والحلول

- **صفحات فارغة في PDF الناتج** – تأكد من أن قيم `PageSize` تتطابق مع أبعاد التخطيط الفعلية في ملف DWG.  
- **أخطاء نفاد الذاكرة على الرسومات الكبيرة** – استخدم `CadImage.load(..., LoadOptions)` مع `LoadOptions.setLoadMode(LoadMode.Memory)` لبث الملف بدلاً من تحميله بالكامل.  
- **تحجيم غير صحيح** – اضبط `RasterizationOptions.setPageWidth` و `setPageHeight` لتتناسب مع DPI المطلوب (نقطة في البوصة).

## الأسئلة المتكررة

**س: هل يمكنني استخدام Aspose.CAD للـ Java مع مكتبات Java أخرى؟**  
**ج:** نعم، Aspose.CAD للـ Java يندمج بسلاسة مع مكتبات مثل Apache POI و Jackson أو Spring Boot.

**س: هل هناك نسخة تجريبية متاحة؟**  
**ج:** بالتأكيد! يمكنك الوصول إلى نسخة تجريبية مجانية [هنا](https://releases.aspose.com/).

**س: أين يمكنني العثور على دعم إضافي؟**  
**ج:** زر [منتدى Aspose.CAD](https://forum.aspose.com/c/cad/19) للحصول على دعم المجتمع والنقاشات.

**س: كيف أحصل على رخصة مؤقتة؟**  
**ج:** يمكنك الحصول على رخصة مؤقتة [هنا](https://purchase.aspose.com/temporary-license/).

**س: أين يمكنني شراء النسخة الكاملة؟**  
**ج:** اشترِ النسخة الكاملة من Aspose.CAD للـ Java [هنا](https://purchase.aspose.com/buy).

---

**آخر تحديث:** 2026-06-29  
**تم الاختبار مع:** Aspose.CAD للـ Java 24.10  
**المؤلف:** Aspose

## دروس ذات صلة

- [تصدير DWG إلى PDF أو نقطية باستخدام Aspose.CAD للـ Java](/cad/java/cad-drawing-conversion/export-dwg-to-pdf-or-raster/)
- [تصدير تخطيطات CAD إلى PDF باستخدام Aspose.CAD للـ Java](/cad/java/cad-export-options/export-cad-layouts-to-pdf/)
- [تصدير تخطيط DWG محدد إلى PDF باستخدام Aspose.CAD للـ Java](/cad/java/cad-drawing-conversion/export-specific-dwg-layout-to-pdf/)


{{< /blocks/products/pf/tutorial-page-section >}}
{{< /blocks/products/pf/main-container >}}
{{< blocks/products/products-backtop-button >}}
{{< /blocks/products/pf/main-wrap-class >}}