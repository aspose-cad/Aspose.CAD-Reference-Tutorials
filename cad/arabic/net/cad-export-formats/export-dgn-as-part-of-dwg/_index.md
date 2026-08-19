---
date: 2026-03-21
description: تعلم كيفية إنشاء ملف PDF من DWG وتصدير DGN كجزء من DWG باستخدام Aspose.CAD
  لـ .NET. يوضح هذا الدليل أيضًا كيفية تحويل DWG إلى PDF وتعيين خيارات PDF.
linktitle: Export DGN as Part of DWG
second_title: Aspose.CAD .NET - CAD and BIM File Format
title: إنشاء PDF من DWG وتصدير DGN كجزء من DWG – Aspose.CAD لـ .NET
url: /ar/net/cad-export-formats/export-dgn-as-part-of-dwg/
weight: 11
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# إنشاء PDF من DWG وتصدير DGN كجزء من DWG – Aspose.CAD for .NET

## المقدمة

إذا كنت بحاجة إلى **إنشاء PDF من DWG** مع تضمين تصميم DGN كجزء من DWG، فإن Aspose.CAD for .NET يجعل ذلك بسيطًا. في هذا البرنامج التعليمي سنستعرض سير العمل بالكامل: تحميل ملف DWG، العثور على طبقة DGN المدمجة، ضبط خيارات التحويل إلى نقطية، وأخيرًا تصدير النتيجة إلى مستند PDF. سواءً كنت تبني أداة تحويل دفعي، أو محرك تقارير، أو خدمة تكامل CAD‑BIM، فإن الخطوات أدناه ستوفر لك أساسًا قويًا وجاهزًا للإنتاج.

## إجابات سريعة
- **ما المكتبة التي تتعامل مع تحويل DWG → PDF؟** Aspose.CAD for .NET  
- **هل يمكنني تصدير طبقة DGN أثناء إنشاء PDF؟** نعم – يتم الوصول إلى الطبقة عبر `CadDgnUnderlay`.  
- **ما الطريقة التي تحدد خيارات PDF؟** `PdfOptions` مع `CadRasterizationOptions`.  
- **هل أحتاج إلى ترخيص للاستخدام التجاري؟** نعم، يلزم وجود ترخيص Aspose.CAD صالح.  
- **الإصدارات المدعومة من .NET؟** .NET Framework 4.5+, .NET Core 3.1+, .NET 5/6/7.

## ما هو “إنشاء PDF من DWG”؟

إنشاء PDF من ملف DWG يعني تحويل الرسم المتجه إلى مستند PDF نقطي أو متجه. هذه العملية مفيدة لمشاركة الرسومات مع أصحاب المصلحة الذين لا يمتلكون برنامج CAD، أو للأرشفة، أو لإنشاء تقارير قابلة للطباعة. تقوم Aspose.CAD بتبسيط المهمة من خلال معالجة التحليل المعقد لكائنات DWG وتوفير تحكم دقيق في المخرجات عبر `PdfOptions`.

## لماذا تصدير DGN كجزء من DWG؟

غالبًا ما تمثل طبقة DGN الهندسة المرجعية من مشاريع MicroStation. من خلال تصدير DGN مع DWG تحتفظ بسياق التصميم الأصلي، مما يضمن أن يرى المستهلكون اللاحقون مجموعة الرسومات الكاملة. هذا يكون ذا قيمة خاصة في المشاريع متعددة التخصصات حيث تت coexist ملفات DWG و DGN.

## المتطلبات المسبقة

- **Aspose.CAD for .NET** – قم بتنزيله [هنا](https://releases.aspose.com/cad/net/).  
- **بيئة التطوير** – Visual Studio (أي نسخة حديثة) أو IDE .NET المفضلة لديك.  
- **معرفة أساسية بـ C#** – يجب أن تكون مرتاحًا مع بنية C# وهيكل مشروع .NET.

## استيراد المساحات الاسمية

أضف توجيهات `using` المطلوبة في أعلى ملف C# الخاص بك:

```csharp
using System;
using System.Collections.Generic;
using System.Linq;
using System.Text;
using System.Threading.Tasks;
using Aspose.CAD;
```

## دليل خطوة بخطوة

### الخطوة 1: تعريف مسارات الملفات

حدد ملف DWG الإدخال واسم ملف PDF الناتج.

```csharp
// Input and Output file paths
string fileName = "BlockRefDgn.dwg";
string outPath = fileName + ".pdf";
```

### الخطوة 2: إنشاء كائن `PdfOptions` (ضبط خيارات PDF)

`PdfOptions` يتيح لك التحكم في كيفية إنشاء PDF، مثل حجم الصفحة، الضغط، والبيانات الوصفية.

```csharp
// Create an instance of PdfOptions class for exporting DWG to PDF
PdfOptions exportOptions = new PdfOptions();
```

### الخطوة 3: تحميل ملف DWG

حمّل DWG كـ `CadImage` لتتمكن من فحص كائناته.

```csharp
// Load the existing DWG file as an image and convert it to CadImage type
using (CadImage cadImage = (CadImage)Image.Load(fileName))
```

### الخطوة 4: التجوال عبر الكائنات

تجول عبر كل كائن في الرسم للعثور على طبقة DGN.

```csharp
// Iterate through each entity inside the DWG file
foreach (CadBaseEntity baseEntity in cadImage.Entities)
```

### الخطوة 5: فحص نوع الكائن (كيفية تصدير DGN)

حدد ما إذا كان الكائن الحالي هو طبقة DGN.

```csharp
// Check if the entity is an image definition
if (baseEntity.TypeName == CadEntityTypeName.DGNUNDERLAY)
```

### الخطوة 6: الحصول على مسار الطبقة

استرجع مسار الإشارة الخارجية لملف DGN.

```csharp
// If it's an image definition, get the external reference to the object
CadDgnUnderlay dgnFile = (CadDgnUnderlay)baseEntity;
Console.WriteLine(dgnFile.UnderlayPath);
```

### الخطوة 7: تعريف خيارات التحويل إلى نقطية (تحويل DWG إلى PDF)

اضبط كيفية تحويل DWG إلى نقطية قبل وضعه في PDF.

```csharp
// Define settings for CadRasterizationOptions object
exportOptions.VectorRasterizationOptions = new CadRasterizationOptions()
{
    PageWidth = 1600,
    PageHeight = 1600,
    Layouts = new string[] { "Model" },
    AutomaticLayoutsScaling = false,
    NoScaling = true,
    BackgroundColor = Color.Black,
    DrawType = CadDrawTypeMode.UseObjectColor
};
```

### الخطوة 8: تصدير DWG إلى PDF

أخيرًا، احفظ الصورة المرسومة كملف PDF.

```csharp
// Export the DWG to PDF by calling Save method
cadImage.Save(outPath, exportOptions);
```

## المشكلات الشائعة والحلول

| المشكلة | السبب | الحل |
|-------|--------|-----|
| **`Image.Load` يرمي “File not found”** | مسار غير صحيح أو ملف مفقود. | استخدم مسارًا مطلقًا أو تأكد من نسخ ملف DWG إلى مجلد الإخراج. |
| **مسار الطبقة فارغ** | طبقة DGN غير مدمجة أو الإشارة مكسورة. | تحقق من أن DWG يحتوي فعليًا على طبقة DGN وأن ملف DGN الخارجي قابل للوصول. |
| **مخرجات PDF فارغة** | تم ضبط خيارات التحويل إلى نقطية بحجم صفر. | قم بضبط `PageWidth`/`PageHeight` أو عيّن `NoScaling = false`. |
| **استثناء الترخيص** | تشغيل بدون ترخيص Aspose.CAD صالح. | طبق الترخيص قبل تحميل الصورة: `License lic = new License(); lic.SetLicense("Aspose.CAD.lic");` |

## الأسئلة المتكررة

### س1: هل يمكنني استخدام Aspose.CAD for .NET في مشاريعي التجارية؟
A1: نعم، يمكنك ذلك. زر [هنا](https://purchase.aspose.com/buy) لاستكشاف خيارات الترخيص.

### س2: هل هناك أي قيود على حجم ملفات DWG التي يمكنني معالجتها؟
A2: يدعم Aspose.CAD معالجة ملفات DWG الكبيرة، لكن قد تنطبق قيود الأجهزة.

### س3: هل تتوفر نسخة تجريبية؟
A3: نعم، يمكنك الحصول على نسخة تجريبية مجانية [هنا](https://releases.aspose.com/).

### س4: كيف يمكنني الحصول على تراخيص مؤقتة؟
A4: يمكن الحصول على تراخيص مؤقتة [هنا](https://purchase.aspose.com/temporary-license/).

### س5: أين يمكنني طلب المساعدة إذا واجهت مشاكل؟
A5: يمكنك زيارة منتدى Aspose.CAD [هنا](https://forum.aspose.com/c/cad/19) للحصول على الدعم.

**س: كيف يمكنني ضبط بيانات تعريف PDF إضافية (المؤلف، العنوان، إلخ)؟**  
**ج:** استخدم خصائص `exportOptions.Metadata` قبل استدعاء `Save`.

**س: هل يمكنني تصدير تخطيطات متعددة إلى صفحات PDF منفصلة؟**  
**ج:** نعم – اضبط `Layouts = new string[] { "Layout1", "Layout2" }` في `CadRasterizationOptions`.

**س: هل يدعم Aspose.CAD تحويل DWG إلى صيغ صور أخرى؟**  
**ج:** بالتأكيد. يمكنك التصدير إلى PNG، JPEG، SVG، والمزيد باستخدام الدوال المتعددة `Image.Save` المناسبة.

**آخر تحديث:** 2026-03-21  
**تم الاختبار مع:** Aspose.CAD 24.11 for .NET  
**المؤلف:** Aspose  

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}