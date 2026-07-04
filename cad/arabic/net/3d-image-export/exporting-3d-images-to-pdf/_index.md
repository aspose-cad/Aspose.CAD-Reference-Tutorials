---
date: 2026-07-04
description: تعلم كيفية تعيين حجم صفحة PDF وتصدير PDF من صور CAD ثلاثية الأبعاد باستخدام
  Aspose.CAD لـ .NET – دليل خطوة بخطوة لتحويل DWG إلى PDF وحفظ CAD كملف PDF.
keywords:
- set pdf page size
- export pdf from cad
- convert dwg to pdf
- save cad as pdf
- cad to pdf tutorial
linktitle: تصدير صور 3D إلى PDF
schemas:
- author: Aspose
  dateModified: '2026-07-04'
  description: Learn how to set PDF page size and export PDF from 3D CAD images using
    Aspose.CAD for .NET – a step‑by‑step guide to convert DWG to PDF and save CAD
    as PDF.
  headline: Set PDF page size – Export 3D Images to PDF with Aspose.CAD
  type: TechArticle
- description: Learn how to set PDF page size and export PDF from 3D CAD images using
    Aspose.CAD for .NET – a step‑by‑step guide to convert DWG to PDF and save CAD
    as PDF.
  name: Set PDF page size – Export 3D Images to PDF with Aspose.CAD
  steps:
  - name: Load the CAD Image
    text: '`Image` class represents a CAD drawing loaded into memory, ready for rasterization.'
  - name: Configure Rasterization Options (Save CAD as PDF)
    text: '`RasterizationOptions` class defines how the CAD data is rasterized, including
      page size, DPI, and whether 3‑D entities are rendered.'
  - name: Set PDF Options (Create PDF from CAD)
    text: '`PdfOptions` class holds the output format settings and links the rasterization
      options to PDF generation.'
  - name: Save as PDF (Generate PDF from 3D Model)
    text: '`Save` method on the `Image` object writes the rasterized content to the
      specified PDF file, producing a ready‑to‑share document.'
  type: HowTo
- questions:
  - answer: Yes, Aspose.CAD supports more than 50 input and output formats, including
      DWG, DXF, DGN, STL, and IFC, ensuring flexibility for any project.
    question: Is Aspose.CAD compatible with all CAD file formats?
  - answer: Absolutely. Set `PageWidth` and `PageHeight` in `RasterizationOptions`
      to any size in points, inches, or millimetres before calling `Save`.
    question: Can I customize the page dimensions when exporting to PDF?
  - answer: Yes, you can obtain temporary licenses for Aspose.CAD by visiting [Temporary
      License](https://purchase.aspose.com/temporary-license/).
    question: Are temporary licenses available for Aspose.CAD?
  - answer: Head to the [Aspose.CAD Forum](https://forum.aspose.com/c/cad/19) for
      expert help and peer‑to‑peer advice.
    question: Where can I find additional support or community discussions?
  - answer: Yes, you can explore the features of Aspose.CAD by accessing the [free
      trial](https://releases.aspose.com/).
    question: Is there a free trial version of Aspose.CAD?
  type: FAQPage
second_title: Aspose.CAD .NET - CAD and BIM File Format
title: تعيين حجم صفحة PDF – تصدير صور 3D إلى PDF باستخدام Aspose.CAD
url: /ar/net/3d-image-export/exporting-3d-images-to-pdf/
weight: 10
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# تصدير صور ثلاثية الأبعاد إلى PDF - دليل Aspose.CAD

## مقدمة

إذا كنت بحاجة إلى **set PDF page size** أثناء تحويل رسم CAD ثلاثي الأبعاد إلى PDF، فقد وصلت إلى المكان الصحيح. يوضح لك هذا الدليل، خطوة بخطوة، كيفية تحميل ملف CAD، تكوين خيارات الترصيص—بما في ذلك أبعاد الصفحة المخصصة—وتوليد PDF عالي الدقة باستخدام Aspose.CAD لـ .NET. في النهاية ستتمكن من **export PDF from CAD**، **save CAD as PDF**، والتحكم في كل تفاصيل التخطيط دون الحاجة لتثبيت AutoCAD.

## إجابات سريعة
- **What does “export PDF from CAD” mean?** يحول رسم CAD (DWG، DXF، DGN، إلخ) إلى PDF يمكن فتحه على أي جهاز.  
- **Which library performs the conversion?** Aspose.CAD لـ .NET يوفر الترصيص وتصدير PDF دون تبعيات خارجية.  
- **Do I need a license?** يلزم وجود ترخيص مؤقت أو كامل للإنتاج؛ يتوفر إصدار تجريبي مجاني.  
- **Can I set custom page dimensions?** نعم—استخدم `PageWidth` و `PageHeight` في `RasterizationOptions`.  
- **Will 3‑D geometry be retained?** الكيانات ثلاثية الأبعاد تُرصّص؛ فعّل `TypeOfEntities.Entities3D` للحصول على دعم كامل ثلاثي الأبعاد.

## ما هو “export PDF” في سياق CAD؟

تصدير PDF من CAD يعني أخذ رسم CAD (DWG، DXF، DGN، إلخ) وتحويله إلى ملف PDF يمكن أن يحتوي على رسومات متجهة، عروض ثلاثية الأبعاد مرصّصة، ومعلومات تخطيط صفحة دقيقة، مما يسهل مشاركته مع أي شخص لا يملك برنامج CAD.

## لماذا تستخدم Aspose.CAD لتصدير PDF؟

يتيح لك Aspose.CAD **set PDF page size** وتصدير ملفات PDF بالكامل في كود .NET مُدار. يدعم أكثر من 50 صيغة CAD، يعالج ملفات تصل إلى 2 GB دون تحميل المستند بالكامل في الذاكرة، ويحافظ على وزن الخطوط، الألوان، وإمكانية عرض الكيانات ثلاثية الأبعاد بخيارات DPI تصل إلى 1200. تعمل المكتبة على Windows وLinux وmacOS، لذا تعمل ملفات PDF المُولدة على أي منصة.

## المتطلبات المسبقة

- **Aspose.CAD لـ .NET** مثبت. حمّله من [صفحة تحميل Aspose.CAD لـ .NET](https://releases.aspose.com/cad/net/).  
- مجلد يحتوي على ملفات CAD التي تريد تحويلها (مثال: `C:\CAD\`).  
- .NET 6.0 أو أحدث (أو .NET Framework 4.7.2).  

## استيراد مساحات الأسماء

عبارات `using` تستورد مساحات أسماء Aspose.CAD اللازمة للعمل مع خيارات الترصيص وPDF.  

```csharp
using System;
using System.Collections.Generic;
using System.Linq;
using System.Text;
using System.Threading.Tasks;
using Aspose.CAD;
using Aspose.CAD.ImageOptions;
```

## دليل خطوة بخطوة

### كيفية تعيين حجم صفحة PDF عند تصدير CAD إلى PDF؟

حمّل ملف CAD الخاص بك، قم بتكوين أبعاد الصفحة في `RasterizationOptions`، اربط تلك الخيارات بكائن `PdfOptions`، ثم استدعِ `Save`. يوفّر لك هذا التدفق المكوّن من أربع خطوات تحكمًا كاملاً في حجم وجودة الناتج مع الحفاظ على بساطة الكود.

### الخطوة 1: تحميل صورة CAD

فئة `Image` تمثل رسم CAD محمّلاً في الذاكرة، جاهزًا للرصيص.  

```csharp
string MyDir = "Your Document Directory";
string sourceFilePath = MyDir + "conic_pyramid.dxf";
using (Image cadImage = Image.Load(sourceFilePath))
{
    // Your code for loading the CAD image goes here
}
```

### الخطوة 2: تكوين خيارات الترصيص (حفظ CAD كـ PDF)

فئة `RasterizationOptions` تحدد كيفية رصص بيانات CAD، بما في ذلك حجم الصفحة، DPI، وما إذا كانت الكيانات ثلاثية الأبعاد تُعرض.  

```csharp
CadRasterizationOptions rasterizationOptions = new CadRasterizationOptions();
rasterizationOptions.PageWidth = 500;
rasterizationOptions.PageHeight = 500;
// rasterizationOptions.TypeOfEntities = TypeOfEntities.Entities3D;

rasterizationOptions.Layouts = new string[] { "Model" };
```

### الخطوة 3: تعيين خيارات PDF (إنشاء PDF من CAD)

فئة `PdfOptions` تحتفظ بإعدادات تنسيق الإخراج وتربط خيارات الترصيص بإنشاء PDF.  

```csharp
PdfOptions pdfOptions = new PdfOptions();
pdfOptions.VectorRasterizationOptions = rasterizationOptions;
```

### الخطوة 4: حفظ كـ PDF (إنشاء PDF من نموذج ثلاثي الأبعاد)

طريقة `Save` على كائن `Image` تكتب المحتوى المرصّص إلى ملف PDF المحدد، منتجةً مستندًا جاهزًا للمشاركة.  

```csharp
MyDir = MyDir + "Export3DImagestoPDF_out.pdf";
cadImage.Save(MyDir, pdfOptions);
```

## المشكلات الشائعة والحلول

| المشكلة | السبب | الحل |
|-------|--------|-----|
| **Output PDF is blank** | اسم التخطيط غير صحيح أو عدم وجود تخطيط `Model`. | تحقق من أن `rasterizationOptions.Layouts` يطابق تخطيطًا موجودًا في ملف CAD. |
| **Low resolution** | DPI الترصيص الافتراضي منخفض. | عيّن `rasterizationOptions.Resolution = 300;` قبل الحفظ. |
| **3‑D entities not shown** | `TypeOfEntities` مُعَلَّق. | ألغِ التعليق عن `rasterizationOptions.TypeOfEntities = TypeOfEntities.Entities3D;`. |
| **License exception** | استخدام نسخة تجريبية بدون ترخيص. | طبّق ترخيصًا مؤقتًا أو دائمًا عبر `License license = new License(); license.SetLicense("Aspose.CAD.lic");`. |

## الأسئلة المتكررة

**س: هل Aspose.CAD متوافق مع جميع صيغ ملفات CAD؟**  
ج: نعم، يدعم Aspose.CAD أكثر من 50 صيغة إدخال وإخراج، بما في ذلك DWG، DXF، DGN، STL، وIFC، مما يضمن مرونة لأي مشروع.

**س: هل يمكنني تخصيص أبعاد الصفحة عند التصدير إلى PDF؟**  
ج: بالتأكيد. عيّن `PageWidth` و `PageHeight` في `RasterizationOptions` إلى أي حجم بالنقاط أو البوصات أو المليمترات قبل استدعاء `Save`.

**س: هل تتوفر تراخيص مؤقتة لـ Aspose.CAD؟**  
ج: نعم، يمكنك الحصول على تراخيص مؤقتة لـ Aspose.CAD بزيارة [Temporary License](https://purchase.aspose.com/temporary-license/).

**س: أين يمكنني العثور على دعم إضافي أو مناقشات المجتمع؟**  
ج: توجه إلى [Aspose.CAD Forum](https://forum.aspose.com/c/cad/19) للحصول على مساعدة خبراء ونصائح من الأقران.

**س: هل هناك نسخة تجريبية مجانية من Aspose.CAD؟**  
ج: نعم، يمكنك استكشاف ميزات Aspose.CAD عبر الوصول إلى [free trial](https://releases.aspose.com/).

## الخلاصة

أصبح لديك الآن طريقة كاملة وجاهزة للإنتاج **set PDF page size** و**export PDF from 3D CAD images** باستخدام Aspose.CAD لـ .NET. من خلال تعديل خيارات الترصيص يمكنك ضبط الدقة، تخطيط الصفحة، وعرض الكيانات ثلاثية الأبعاد لتلبية أي متطلبات توثيق. جرّب إعدادات DPI مختلفة وأبعاد صفحات مختلفة لتحقيق التوازن المثالي بين حجم الملف وجودة العرض.

{{< blocks/products/products-backtop-button >}}

## دروس ذات صلة

- [Exporting Specific Layouts to PDF - Aspose.CAD Guide](/cad/net/advanced-export-techniques/exporting-specific-layouts-to-pdf/)
- [Exporting DWG to PDF or Raster Images - Aspose.CAD Guide](/cad/net/advanced-export-techniques/exporting-dwg-to-pdf-or-raster-images/)
- [Export DGN to PDF in Aspose.CAD for .NET](/cad/net/cad-export-formats/export-dgn-to-pdf/)


{{< /blocks/products/pf/tutorial-page-section >}}
{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

--- 

**آخر تحديث:** 2026-07-04  
**تم الاختبار مع:** Aspose.CAD 24.11 for .NET  
**المؤلف:** Aspose