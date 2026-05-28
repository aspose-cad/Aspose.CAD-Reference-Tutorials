---
date: 2026-03-02
description: تعلم كيفية إنشاء ملف PDF واحد بتصاميم مختلفة باستخدام Aspise.CAD لـ .NET
  – تحويل CAD إلى PDF، تصدير DWG إلى PDF، وحفظ CAD كملف PDF بكفاءة.
linktitle: Creating Single PDF with Different Layouts
second_title: Aspose.CAD .NET - CAD and BIM File Format
title: كيفية إنشاء ملف PDF واحد بتصاميم مختلفة - دليل Aspose.CAD
url: /ar/net/advanced-cad-techniques/creating-single-pdf-with-different-layouts/
weight: 13
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# كيفية إنشاء ملف PDF واحد بتنسيقات مختلفة - دليل Aspose.CAD

## مقدمة

إذا كنت بحاجة إلى **create single pdf** ملفات تحتوي على عدة تخطيطات CAD، فأنت في المكان الصحيح. في هذا الدرس سنستعرض الخطوات الدقيقة المطلوبة لتحويل رسومات CAD إلى مستند PDF واحد، مع معالجة عدة تخطيطات على طول الطريق. ستشاهد كيف يجعل Aspose.CAD for .NET من السهل **convert CAD to PDF**، **export DWG to PDF**، و **save CAD as PDF** ببضع أسطر من كود C# فقط.

## إجابات سريعة
- **ما الذي يغطيه هذا الدرس؟** إنشاء ملف PDF واحد يتضمن عدة تخطيطات CAD.  
- **ما المكتبة المستخدمة؟** Aspose.CAD for .NET.  
- **هل أحتاج إلى ترخيص؟** النسخة التجريبية المجانية تكفي للتقييم؛ الترخيص مطلوب للإنتاج.  
- **ما هي صيغ CAD المدعومة؟** DWG، DXF، DGN والعديد غيرها.  
- **الوقت النموذجي للتنفيذ؟** حوالي 10‑15 دقيقة للتحويل الأساسي.

## ما معنى “create single pdf” في سياق CAD؟

إنشاء ملف PDF واحد يعني أخذ ملف CAD مصدر قد يحتوي على عدة تعريفات تخطيط (مساحات ورقية) ودمج كل تخطيط في صفحات منفصلة داخل مستند PDF واحد. هذا مفيد بشكل خاص لخطط الهندسة المعمارية، المخططات الهندسية، أو أي سيناريو يتوقع فيه العميل حزمة PDF موحدة.

## لماذا نستخدم Aspose.CAD لهذه المهمة؟

- **لا توجد تبعيات خارجية** – .NET نقي، لا حاجة لتثبيت AutoCAD.  
- **تحكم كامل في التحويل إلى نقطية** – يمكنك ضبط حجم الصفحة، DPI، وأبعاد التخطيط المخصصة.  
- **عرض عالي الدقة** – يتم الحفاظ على البيانات المتجهية حيثما أمكن، لضمان مخرجات واضحة.  
- **جاهز للدفعات** – يمكن وضع نفس الكود داخل حلقة لمعالجة العديد من الرسومات تلقائيًا.

## المتطلبات المسبقة

- Aspose.CAD for .NET: تأكد من تثبيت Aspose.CAD for .NET. يمكنك تنزيله من [here](https://releases.aspose.com/cad/net/).  
- بيئة التطوير: قم بإعداد بيئة تطوير .NET، ويجب أن تكون لديك معرفة أساسية ببرمجة C#.

## استيراد مساحات الأسماء

في مشروع C# الخاص بك، قم بتضمين مساحات الأسماء اللازمة للاستفادة من وظائف Aspose.CAD for .NET:

```csharp
using Aspose.CAD.FileFormats.Cad;
using Aspose.CAD.ImageOptions;
using System;
using System.Collections.Generic;
using System.Linq;
using System.Text;
```

## دليل خطوة بخطوة

### الخطوة 1: تحميل صورة CAD

أولاً، حمّل ملف CAD المصدر (مثلاً رسم DWG). توفر لك فئة `CadImage` إمكانية الوصول إلى جميع التخطيطات داخل الملف.

```csharp
// The path to the documents directory.
string MyDir = "Your Document Directory";

using (CadImage cadImage = (CadImage)Image.Load(MyDir + "City skyway map.dwg"))
{
    // Your code for Step 1 goes here
}
```

### الخطوة 2: تخصيص خيارات التحويل إلى نقطية

حدد كيف يجب تحويل كل تخطيط إلى نقطية. يمكنك تعيين حجم صفحة افتراضي ثم تجاوزه لتخطيطات محددة باستخدام `LayoutPageSizes`.

```csharp
CadRasterizationOptions rasterizationOptions = new CadRasterizationOptions();
rasterizationOptions.PageWidth = 1000;
rasterizationOptions.PageHeight = 1000;

// Custom sizes for several layouts
rasterizationOptions.LayoutPageSizes.Add("ANSI C Plot", new SizeF(500, 1000));
rasterizationOptions.LayoutPageSizes.Add("8.5 x 11 Plot", new SizeF(1000, 100));
```

> **نصيحة احترافية:** اضبط DPI (`rasterizationOptions.Resolution`) إذا كنت بحاجة إلى مخرجات ذات دقة أعلى للرسومات التفصيلية.

### الخطوة 3: تعريف خيارات PDF

قم بلف إعدادات التحويل إلى نقطية داخل كائن `PdfOptions`. هذا يخبر Aspose.CAD بإنشاء تدفق PDF مباشرة من بيانات CAD.

```csharp
PdfOptions pdfOptions = new PdfOptions() { VectorRasterizationOptions = rasterizationOptions };
```

### الخطوة 4: حفظ كملف PDF

أخيرًا، استدعِ `Save` على كائن `CadImage`، مع تمرير اسم ملف PDF الهدف والإعدادات المُحضرة. ستولد المكتبة ملف PDF واحد يحتوي على صفحة لكل تخطيط قمت بتكوينه.

```csharp
cadImage.Save(MyDir + "singlePDF_out.pdf", pdfOptions);
```

بعد هذا الاستدعاء، ستحصل على PDF يجمع تخطيطي “ANSI C Plot” و “8.5 x 11 Plot” في مستند موحد.

## المشكلات الشائعة & استكشاف الأخطاء

| المشكلة | السبب | الحل |
|-------|--------|-----|
| الطبقات مفقودة في PDF | `LayoutPageSizes` غير معرف لاسم تخطيط | تحقق من أسماء التخطيطات الدقيقة في ملف CAD (حساسة لحالة الأحرف). |
| جودة منخفضة | DPI الافتراضي هو 96 | عيّن `rasterizationOptions.Resolution = 300` (أو أعلى) قبل الحفظ. |
| الملف غير موجود | مسار `MyDir` غير صحيح | استخدم `Path.Combine` لإنشاء مسارات مستقلة عن النظام. |

## الأسئلة المتكررة

### س1: هل يمكنني استخدام Aspose.CAD for .NET مع صيغ CAD أخرى؟

نعم، يدعم Aspose.CAD for .NET صيغ CAD متعددة مثل DWG، DXF، DGN، وأكثر.

### س2: هل تتوفر نسخة تجريبية مجانية؟

نعم، يمكنك تجربة نسخة تجريبية مجانية [here](https://releases.aspose.com/).

### س3: كيف يمكنني الحصول على الدعم لـ Aspose.CAD for .NET؟

قم بزيارة [منتدى Aspose.CAD](https://forum.aspose.com/c/cad/19) للحصول على دعم المجتمع.

### س4: أين يمكنني العثور على الوثائق التفصيلية؟

راجع الوثائق [here](https://reference.aspose.com/cad/net/).

### س5: هل يمكنني شراء ترخيص لـ Aspose.CAD for .NET؟

نعم، يمكنك شراء ترخيص [here](https://purchase.aspose.com/buy).

**أسئلة إضافية**

**س:** كيف يمكنني **export DWG to PDF** بأحجام صفحات مخصصة؟  
**ج:** استخدم `CadRasterizationOptions.LayoutPageSizes` لتعيين كل تخطيط DWG إلى أبعاد صفحة PDF المطلوبة، كما هو موضح في الخطوة 2.

**س:** هل يمكن **save CAD as PDF** دون تحويل البيانات المتجهية إلى نقطية؟  
**ج:** Aspose.CAD دائمًا يحول إلى نقطية عند إنشاء PDF، لكن يمكنك زيادة DPI للحفاظ على الدقة البصرية.

## الخلاصة

في هذا الدليل أظهرنا كيفية **create single pdf** من رسومات CAD التي تحتوي على عدة تخطيطات، باستخدام Aspose.CAD for .NET. الآن لديك اللبنات الأساسية لـ **convert CAD to PDF**، **export DWG to PDF**، و **save CAD as PDF** في سير عمل آلي واحد. جرّب إعدادات التحويل إلى نقطية المختلفة لتتناسب مع متطلبات جودة مشروعك، ودمج هذا الكود في خطوط معالجة دفعات أكبر حسب الحاجة.

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}

---

**آخر تحديث:** 2026-03-02  
**تم الاختبار مع:** Aspose.CAD for .NET 24.11  
**المؤلف:** Aspose