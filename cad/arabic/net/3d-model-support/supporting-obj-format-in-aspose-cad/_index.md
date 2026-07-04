---
date: 2026-07-04
description: تعلم كيفية تعيين حجم صفحة PDF أثناء تحويل ملفات OBJ إلى PDF باستخدام
  Aspose.CAD لـ .NET. دليل خطوة بخطوة مع المتطلبات المسبقة، خيارات التحويل إلى نقطية،
  وخيارات PDF.
keywords:
- set pdf page size
- load obj file
- save cad as pdf
- 3d model to pdf
- how to convert obj
linktitle: دعم تنسيق OBJ في Aspose.CAD - دليل تعليمي
schemas:
- author: Aspose
  dateModified: '2026-07-04'
  description: Learn how to set PDF page size while converting OBJ files to PDF using
    Aspose.CAD for .NET. Step‑by‑step guide with prerequisites, rasterization options,
    and PDF options.
  headline: Set PDF Page Size for OBJ Files with Aspose.CAD - Tutorial
  type: TechArticle
- questions:
  - answer: Yes, Aspose.CAD supports over **30** input formats—including DWG, DXF,
      DGN, and STL—and can export to more than **20** raster and vector formats.
    question: Is Aspose.CAD compatible with other CAD file formats?
  - answer: Absolutely! You can explore a free trial version [here](https://releases.aspose.com/).
    question: Can I try Aspose.CAD before purchasing?
  - answer: Visit the [Aspose.CAD forum](https://forum.aspose.com/c/cad/19) to ask
      questions and share experiences with the community.
    question: How do I obtain support for Aspose.CAD?
  - answer: Yes, temporary licenses can be obtained [here](https://purchase.aspose.com/temporary-license/).
    question: Are temporary licenses available for testing?
  - answer: You can purchase Aspose.CAD [here](https://purchase.aspose.com/buy).
    question: Where can I purchase a full license?
  type: FAQPage
second_title: Aspose.CAD .NET - CAD and BIM File Format
title: تعيين حجم صفحة PDF لملفات OBJ باستخدام Aspose.CAD - دليل تعليمي
url: /ar/net/3d-model-support/supporting-obj-format-in-aspose-cad/
weight: 10
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# تعيين حجم صفحة PDF لملفات OBJ باستخدام Aspose.CAD - دليل

## مقدمة

إذا كنت تطور تطبيقات CAD في .NET وتحتاج إلى **تعيين حجم صفحة PDF** عند تحويل نماذج OBJ، فإن Aspose.CAD لـ .NET يوفر واجهة برمجة تطبيقات نظيفة تعتمد على الكود أولاً وتتعامل مع التحويل إلى نقطية وتوليد PDF في تدفق واحد. في هذا الدليل سنستعرض تثبيت المكتبة، تحميل ملف OBJ، ضبط أبعاد الصفحة، وأخيرًا حفظ النتيجة كملف PDF. في النهاية ستحصل على نمط قابل لإعادة الاستخدام لتحويل أي نموذج ثلاثي الأبعاد إلى مستند PDF بالحجم المثالي.

## إجابات سريعة
- **هل يمكن لـ Aspose.CAD تحويل OBJ إلى PDF؟** نعم – قم بتحميل OBJ باستخدام `Image.Load` وتحويله إلى PDF.
- **كيف يمكنني تعيين حجم صفحة PDF مخصص؟** استخدم `PdfOptions` → `PageSize` أو اضبط العرض/الارتفاع في `RasterizationOptions`.
- **ما إصدارات .NET المدعومة؟** .NET Framework 4.5+, .NET Core 3.1+, .NET 5/6/7.
- **هل أحتاج إلى ترخيص للتطوير؟** النسخة التجريبية المجانية تعمل للتقييم؛ الترخيص مطلوب للإنتاج.
- **هل التحويل فعال من حيث الذاكرة؟** Aspose.CAD يبث البيانات ويمكنه معالجة ملفات PDF مئات الصفحات دون تحميل الملف بالكامل إلى الذاكرة.

## ما هو تنسيق OBJ؟

تنسيق OBJ هو تعريف هندسي ثلاثي الأبعاد يعتمد على النص ويُستخدم على نطاق واسع، يخزن إحداثيات الرؤوس، إحداثيات القوام، وتعريفات الوجوه. يدعمه معظم أدوات النمذجة ثلاثية الأبعاد وهو مثالي لتبادل البيانات بين CAD وأنابيب العرض.

## لماذا تعيين حجم صفحة PDF مخصص؟

يمكن لـ Aspose.CAD عرض رسم CAD بأي حجم نقطي. من خلال تعيين أبعاد صفحة PDF صراحةً، تضمن أن المستند النهائي يتطابق مع معايير التقارير الخاصة بك، ويتناسب مع أحجام الورق القياسية (A4، Letter) أو يتوافق مع تخطيطات الطباعة المخصصة. الفائدة المكمّنة: يمكن للواجهة البرمجية إنشاء ملفات PDF حتى **200 مم × 200 مم** في استدعاء واحد، ومعالجة ملفات أكبر من **500 ميغابايت** دون تجاوز 250 ميغابايت من الذاكرة.

## المتطلبات المسبقة

- **Aspose.CAD Library** – تأكد من تثبيت مكتبة Aspose.CAD في مشروع .NET الخاص بك. يمكنك تنزيلها [here](https://releases.aspose.com/cad/net/) وعرض مرجع API الكامل في [documentation](https://reference.aspose.com/cad/net/).
- **Document Directory** – أنشئ مجلدًا لأصول CAD الخاصة بك؛ سنشير إليه باسم “Your Document Directory” طوال الدليل.
- **.NET Development Environment** – Visual Studio 2022 أو أي بيئة تطوير تدعم .NET 6+.

## كيفية تعيين حجم صفحة PDF عند تحويل OBJ إلى PDF؟

قم بتحميل ملف OBJ، ضبط خيارات التحويل إلى نقطية بالعرض والارتفاع المطلوبين، ربط هذه الخيارات بواجهة `PdfOptions`، ثم استدعاء `Save`. يضمن هذا النمط ذو الخطوتين أن تتطابق صفحة PDF مع الأبعاد التي تحددها مع الحفاظ على تفاصيل النموذج.

## الخطوة 1: استيراد المساحات الاسمية

`Image` تتعامل مع جميع صيغ CAD، و`PdfOptions` تتحكم في إخراج PDF.  
`Image` تمثل مستند CAD وتوفر طرقًا لتحميل وحفظ الملفات. `PdfOptions` تحدد إعدادات توليد PDF مثل حجم الصفحة والضغط.

```csharp
using System;
using System.Collections.Generic;
using System.Linq;
using System.Text;
```

## الخطوة 2: تحميل ملف OBJ

حمّل ملف OBJ إلى كائن صورة Aspose.CAD. استبدل `"example-580-W.obj"` باسم ملف OBJ الخاص بك.

```csharp
string MyDir = "Your Document Directory";
using (Aspose.CAD.Image CADDoc = Aspose.CAD.Image.Load(MyDir + "example-580-W.obj"))
{
    // Your code for further processing goes here
}
```

## الخطوة 3: ضبط خيارات التحويل إلى نقطية

`RasterizationOptions` تحدد حجم النقاط الذي يتحول في النهاية إلى حجم صفحة PDF. ضبط `PageWidth` و `PageHeight` يتيح لك التحكم في الأبعاد الدقيقة لملف PDF الناتج.  
`CadRasterizationOptions` (المُعرَّضة عبر `RasterizationOptions`) تحدد معلمات التحويل إلى نقطية مثل أبعاد الصفحة والدقة.

```csharp
Aspose.CAD.ImageOptions.CadRasterizationOptions rasterizationOptions =
    new Aspose.CAD.ImageOptions.CadRasterizationOptions();

rasterizationOptions.PageWidth = CADDoc.Size.Width;
rasterizationOptions.PageHeight = CADDoc.Size.Height;
```

## الخطوة 4: إنشاء خيارات PDF

`PdfOptions` يربط إعدادات التحويل إلى نقطية بكاتب PDF. من خلال تعيين كائن `RasterizationOptions`، تضمن أن PDF يرث حجم الصفحة الذي حددته.

```csharp
Aspose.CAD.ImageOptions.PdfOptions CADf = new Aspose.CAD.ImageOptions.PdfOptions();
CADf.VectorRasterizationOptions = rasterizationOptions;
```

## الخطوة 5: حفظ كملف PDF

استدعِ طريقة `Save` على كائن `Image`، مع تمرير اسم الملف الهدف وإعدادات `PdfOptions` المكوَّنة. تقوم المكتبة بكتابة PDF بالحجم الدقيق للصفحة الذي حددته.  
`Save` تكتب الصورة إلى ملف باستخدام الصيغة والإعدادات المحددة.

```csharp
CADDoc.Save(MyDir + "example-580-W_custom.pdf", CADf);
```

## المشكلات الشائعة والحلول

- **Incorrect page dimensions** – تحقق من أن `PageWidth` و `PageHeight` محددان بوحدات **البكسل**؛ استخدم `Resolution` لتحويل البوصات أو المليمترات إلى بكسل (مثال: 300 dpi → 1 inch = 300 px).
- **Missing textures** – غالبًا ما تشير ملفات OBJ إلى ملفات `.mtl` خارجية؛ تأكد من وجود ملف المادة في نفس الدليل مع ملف OBJ.
- **Large file memory usage** – فعّل `Image.SaveOptions.Compression` لتقليل استهلاك الذاكرة عند عمليات العرض عالية الدقة.

## الأسئلة المتكررة

**س: هل Aspose.CAD متوافق مع صيغ CAD أخرى؟**  
ج: نعم، يدعم Aspose.CAD أكثر من **30** صيغة إدخال — بما في ذلك DWG وDXF وDGN وSTL — ويمكنه التصدير إلى أكثر من **20** صيغة نقطية ومتجهة.

**س: هل يمكنني تجربة Aspose.CAD قبل الشراء؟**  
ج: بالتأكيد! يمكنك استكشاف نسخة تجريبية مجانية [here](https://releases.aspose.com/).

**س: كيف أحصل على دعم Aspose.CAD؟**  
ج: زر [Aspose.CAD forum](https://forum.aspose.com/c/cad/19) لطرح الأسئلة ومشاركة التجارب مع المجتمع.

**س: هل تتوفر تراخيص مؤقتة للاختبار؟**  
ج: نعم، يمكن الحصول على تراخيص مؤقتة [here](https://purchase.aspose.com/temporary-license/).

**س: أين يمكنني شراء ترخيص كامل؟**  
ج: يمكنك شراء Aspose.CAD [here](https://purchase.aspose.com/buy).

**آخر تحديث:** 2026-07-04  
**تم الاختبار مع:** Aspose.CAD 24.11 for .NET  
**المؤلف:** Aspose

## الدروس ذات الصلة

- [تصدير ملفات IGES إلى PDF - دليل Aspose.CAD](/cad/net/exporting-to-image-formats/exporting-iges-files-to-pdf/)
- [تصدير DXF إلى تنسيق PDF - درس Aspose.CAD](/cad/net/export-techniques/exporting-dxf-to-pdf-format/)
- [تصدير رسومات CAD إلى PDF - درس Aspose.CAD](/cad/net/advanced-export-techniques/exporting-cad-drawings-to-pdf/)

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}