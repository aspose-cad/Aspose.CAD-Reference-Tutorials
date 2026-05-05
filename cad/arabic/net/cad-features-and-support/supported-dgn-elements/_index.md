---
date: 2026-03-29
description: تعلم كيفية تحويل DGN إلى PNG باستخدام Aspose.CAD لـ .NET. يغطي هذا الدليل
  أيضًا دعم تنسيق ملفات CAD ومجموعة العناصر المدعومة بالكامل لـ DGN.
linktitle: Supported DGN Elements
second_title: Aspose.CAD .NET - CAD and BIM File Format
title: تحويل DGN إلى PNG باستخدام Aspose.CAD لـ .NET
url: /ar/net/cad-features-and-support/supported-dgn-elements/
weight: 18
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# تحويل DGN إلى PNG باستخدام Aspose.CAD لـ .NET

## المقدمة

هل أنت مطور .NET تبحث عن **تحويل DGN إلى PNG** بسلاسة؟ يوفر Aspose.CAD لـ .NET حلاً قويًا للتعامل مع ملفات DGN بفعالية. في هذا البرنامج التعليمي، سنستعرض عناصر DGN المدعومة، ونرشدك خلال عملية العمل مع Aspose.CAD لـ .NET مع إظهار كيفية تصدير تلك العناصر إلى صور PNG.

## إجابات سريعة
- **ماذا يفعل Aspose.CAD؟** يقرأ، يعدل، ويحويل ملفات CAD/BIM (بما في ذلك DGN) إلى صيغ نقطية مثل PNG.  
- **هل يمكنني تحويل عناصر DGN ثنائية وثلاثية الأبعاد؟** نعم – كل من الكيانات ثنائية الأبعاد وثلاثية الأبعاد مدعومة.  
- **ما إصدارات .NET المطلوبة؟** .NET Framework 4.5+, .NET Core 3.1+, .NET 5/6+.  
- **هل أحتاج إلى ترخيص للاختبار؟** تتوفر نسخة تجريبية مجانية؛ الترخيص مطلوب للإنتاج.  
- **من أين أحصل على المكتبة؟** قم بتنزيلها من موقع Aspose الرسمي (الرابط أدناه).

## ما هو “تحويل DGN إلى PNG”؟
يعني تحويل DGN إلى PNG تحويل الرسم المتجهي DGN (ثنائي أو ثلاثي الأبعاد) إلى صيغة صورة نقطية (PNG). هذا مفيد عندما تحتاج إلى عرض رسومات CAD على الويب، تضمينها في تقارير، أو إنشاء صور مصغرة دون الحاجة إلى عارض CAD.

## لماذا تستخدم Aspose.CAD لـ .NET لدعم صيغ ملفات CAD؟
- **دعم كامل لصيغ ملفات CAD** – DGN، DWG، DXF، DWF، وأكثر.  
- **بدون تبعيات خارجية** – مكتبة .NET صافية، لا تحتاج إلى تثبيت CAD محلي.  
- **رندرة عالية الدقة** – تحافظ على وزن الخطوط، الألوان، والهندسة ثلاثية الأبعاد.  
- **معالجة دفعات** – يمكن بسهولة تكرار العديد من الملفات في تطبيق خادم.

## المتطلبات المسبقة

قبل أن نبدأ، تأكد من وجود ما يلي:

- معرفة أساسية ببرمجة .NET.  
- تثبيت Visual Studio على جهازك.  
- مكتبة Aspose.CAD لـ .NET، والتي يمكنك تنزيلها [هنا](https://releases.aspose.com/cad/net/).

## استيراد المساحات الاسمية

لبدء مشروعك، استورد المساحات الاسمية الضرورية في تطبيق .NET الخاص بك. تضمن هذه الخطوة حصولك على الوظائف التي توفرها Aspose.CAD لـ .NET.

```csharp
using System;
using System.Collections.Generic;
using System.Linq;
using System.Text;
using System.Threading.Tasks;
using Aspose.CAD;
using Aspose.CAD.FileFormats.Dgn;
using Aspose.CAD.FileFormats.Dgn.DgnElements;
```

## كيفية تحويل DGN إلى PNG

فيما يلي دليل خطوة بخطوة يوضح لك كيفية تحميل ملف DGN، التجول عبر عناصره، معالجة الكيانات ثنائية وثلاثية الأبعاد، وأخيرًا تصدير النتيجة إلى صورة raster بصيغة PNG.

### الخطوة 1: تحميل ملف DGN

ابدأ بتحميل ملف DGN موجود كـ `DgnImage` في تطبيق .NET الخاص بك.

```csharp
string MyDir = "Your Document Directory";
string sourceFilePath = MyDir + "Nikon_D90_Camera.dgn";

using (DgnImage dgnImage = (DgnImage)Image.Load(sourceFilePath))
{
    // Your code here
}
```

### الخطوة 2: التجول عبر عناصر DGN

تجول عبر عناصر DGN باستخدام حلقة `foreach`. يوفر Aspose.CAD لـ .NET مجموعة متنوعة من أنواع عناصر DGN التي يمكنك العمل معها.

```csharp
foreach (DgnDrawingElementBase element in dgnImage.Elements)
{
    // Your code here
}
```

### الخطوة 3: معالجة الكيانات ثنائية الأبعاد المدعومة مسبقًا

هذه الكيانات مدعومة الآن أيضًا للرندرة ثلاثية الأبعاد. تسمح لك جملة switch بتوجيه المنطق بناءً على نوع العنصر.

```csharp
switch (element.Metadata.Type)
{
    case DgnElementType.Line:
    case DgnElementType.Ellipse:
    case DgnElementType.Curve:
    // Additional cases
        {
            // Your code here
            break;
        }
}
```

### الخطوة 4: معالجة الكيانات ثلاثية الأبعاد المدعومة

يضيف Aspose.CAD دعمًا كاملاً لعدة عناصر DGN ثلاثية الأبعاد. قم بتمديد جملة switch لمعالجتها حسب الحاجة.

```csharp
switch (element.Metadata.Type)
{
    case DgnElementType.SolidHeader3D:
    case DgnElementType.Cone:
    case DgnElementType.CellHeader:
        {
            // Your code here
            break;
        }
}
```

### الخطوة 5: تصدير وحفظ كـ PNG

بعد أي تعديل مطلوب، قم بتصدير رسم DGN إلى صورة raster بصيغة PNG واحفظها في الدليل المحدد.

```csharp
Console.WriteLine("\nThe DGN file exported successfully to raster image.\nFile saved at " + MyDir);
```

> **نصيحة احترافية:** استخدم `Image.Save` مع `new PngOptions()` للتحكم في الدقة، لون الخلفية، وإعدادات PNG الأخرى.

## نظرة عامة على دعم صيغ ملفات CAD

Aspose.CAD لـ .NET لا يقتصر على DGN فقط. فهو يدعم أيضًا DWG، DXF، DWF، والعديد من صيغ CAD الأخرى، مما يمنحك API واحد للتعامل مع طيف واسع من رسومات الهندسة. هذا يجعله مثاليًا للمشاريع التي تتطلب **دعم صيغ ملفات CAD** عبر معايير متعددة.

## المشكلات الشائعة والحلول

| المشكلة | السبب | الحل |
|-------|--------|-----|
| **الصورة تظهر فارغة** | تم التصدير بدقة DPI صفر | حدد `ResolutionX` و `ResolutionY` في `PngOptions`. |
| **الجيومتري ثلاثي الأبعاد مفقود** | نوع العنصر غير معالج في جملة switch | أضف حالة `DgnElementType` المفقودة وقم بالرندرة وفقًا لذلك. |
| **نفاد الذاكرة في الملفات الكبيرة** | تحميل الملف بالكامل مرة واحدة | عالج العناصر على دفعات أو استخدم البث حيثما أمكن. |

## الأسئلة المتكررة

### Q1: أين يمكنني العثور على الوثائق الخاصة بـ Aspose.CAD لـ .NET؟
A1: يمكنك العثور على الوثائق [هنا](https://reference.aspose.com/cad/net/).

### Q2: كيف يمكنني تنزيل Aspose.CAD لـ .NET؟
A2: يمكنك تنزيل المكتبة [هنا](https://releases.aspose.com/cad/net/).

### Q3: هل تتوفر نسخة تجريبية مجانية لـ Aspose.CAD لـ .NET؟
A3: نعم، يمكنك الوصول إلى النسخة التجريبية [هنا](https://releases.aspose.com/).

### Q4: أين يمكنني الحصول على تراخيص مؤقتة لـ Aspose.CAD لـ .NET؟
A4: التراخيص المؤقتة متاحة [هنا](https://purchase.aspose.com/temporary-license/).

### Q5: هل تحتاج إلى مساعدة أو لديك أسئلة؟
A5: زر منتدى مجتمع Aspose.CAD لـ .NET [منتدى الدعم](https://forum.aspose.com/c/cad/19).

---

**آخر تحديث:** 2026-03-29  
**تم الاختبار مع:** Aspose.CAD لـ .NET 24.11  
**المؤلف:** Aspose  

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}