---
date: 2026-03-21
description: تعلم كيفية تحويل dxf إلى png وغيرها من صيغ الرسوم النقطية باستخدام Aspose.CAD
  لـ .NET. اتبع دليلنا خطوة بخطوة لتصدير طبقات CAD بسلاسة.
linktitle: Export CAD Layouts to Raster Image Formats
second_title: Aspose.CAD .NET - CAD and BIM File Format
title: تحويل DXF إلى PNG باستخدام Aspose.CAD لـ .NET
url: /ar/net/cad-export-formats/export-cad-layouts-to-raster-image-formats/
weight: 10
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# تصدير تخطيطات CAD إلى صيغ الصور النقطية في Aspose.CAD لـ .NET

## مقدمة

هل تبحث عن تحويل **dxf إلى png** وغيرها من صيغ الصور النقطية بكفاءة باستخدام Aspose.CAD لـ .NET؟ سيوضح لك هذا الدليل خطوة بخطوة العملية، مع توفير تعليمات مفصلة ومقاطع شفرة لجعل المهمة سلسة. سواء كنت مطورًا متمرسًا أو مبتدئًا في Aspose.CAD، فإن هذا البرنامج التعليمي يلبي جميع مستويات الخبرة.

### إجابات سريعة
- **ما المكتبة التي تتعامل مع التحويل؟** Aspose.CAD لـ .NET  
- **ما الصيغة الأساسية المدعومة مباشرةً؟** صور JPEG، PNG، BMP، وTIFF النقطية  
- **هل يمكنني تصدير طبقات CAD محددة؟** نعم – استخدم `CadRasterizationOptions.Layers` لاستهداف طبقات فردية  
- **هل أحتاج إلى ترخيص للإنتاج؟** يلزم وجود ترخيص Aspose.CAD صالح للاستخدام غير التجريبي  
- **الإصدارات المدعومة من .NET؟** .NET Framework 4.5+، .NET Core 3.1+، .NET 5/6/7  

## ما هو **convert dxf to png**؟

تحويل ملف DXF (Drawing Exchange Format) إلى PNG يعني تحويل بيانات CAD القائمة على المتجهات إلى صورة مبنية على البكسل. هذا مفيد عندما تحتاج إلى تضمين رسومات CAD في صفحات الويب أو التقارير أو أي بيئة تدعم فقط الرسومات النقطية.

## لماذا تصدير طبقات CAD بشكل منفصل؟

تصدير طبقات CAD بشكل فردي يمنحك تحكمًا دقيقًا في المظهر النهائي، يقلل حجم الملف لكل صورة، ويسمح لك بتطبيق تنسيقات أو معالجة لاحقة مخصصة لكل طبقة. هذا مفيد بشكل خاص للرسومات الهندسية الكبيرة حيث تكون مجموعة معينة فقط من الطبقات ذات صلة بجمهور معين.

## المتطلبات المسبقة

قبل الغوص في البرنامج التعليمي، تأكد من وجود ما يلي:

- **مكتبة Aspose.CAD لـ .NET** – قم بتنزيلها من [موقع Aspose.CAD](https://releases.aspose.com/cad/net/).  
- **ملف رسم CAD** – ملف DXF (مثال: `conic_pyramid.dxf`) الذي تريد تحويله إلى صيغ نقطية.  

## استيراد مساحات الأسماء

في مشروع .NET الخاص بك، استورد مساحات الأسماء اللازمة للاستفادة من وظائف Aspose.CAD. أدرج مساحات الأسماء التالية في بداية الشفرة:

```csharp
using System;
using System.Collections.Generic;
using System.Linq;
using System.Text;
using System.Threading.Tasks;
using Aspose.CAD;
```

## كيفية **convert dxf to png** – دليل خطوة بخطوة

### الخطوة 1: تحميل رسم CAD

أولاً، قم بتحميل ملف DXF إلى كائن `Image`. هذا الكائن يمثل الرسم الكامل لـ CAD في الذاكرة.

```csharp
string MyDir = "Your Document Directory";
string sourceFilePath = MyDir + "conic_pyramid.dxf";

// Load a CAD drawing in an instance of Image
using (var image = Image.Load(sourceFilePath))
{
    // Your code for loading the CAD drawing goes here
}
```

### الخطوة 2: إنشاء `CadRasterizationOptions`

قم بتكوين إعدادات الرستر مثل أبعاد الإخراج والدقة. تتحكم هذه الخيارات في طريقة تحويل البيانات المتجهة إلى صورة نقطية.

```csharp
// Create an instance of CadRasterizationOptions
var rasterizationOptions = new CadRasterizationOptions();
rasterizationOptions.PageWidth = 500;
rasterizationOptions.PageHeight = 500;
```

### الخطوة 3: تحديد الطبقات (تصدير طبقات CAD)

إذا كنت تحتاج إلى طبقة معينة فقط، ضع اسمها هنا. يوضح هذا **export cad layers** بشكل فردي.

```csharp
// Add the layer name to the CadRasterizationOptions's layer list
rasterizationOptions.Layers = new string[] { "LayerA" };
```

### الخطوة 4: اختيار صيغة الصورة – حفظ CAD كـ PNG (أو JPEG)

أنشئ كائن خيارات خاص بصيغة الصورة. استبدل `JpegOptions` بـ `PngOptions` عندما تريد **save cad as png**.

```csharp
// Create an instance of JpegOptions (or any ImageOptions for raster formats)
var options = new JpegOptions();
options.VectorRasterizationOptions = rasterizationOptions;
```

> **نصيحة احترافية:** لإنشاء ملفات PNG، ما عليك سوى إنشاء `new PngOptions()` بدلاً من `JpegOptions`.

### الخطوة 5: تصدير إلى صيغة JPEG (أو PNG)

أخيرًا، احفظ الصورة المرسومة إلى القرص. يحدد امتداد الملف الصيغة الناتجة.

```csharp
// Export each layer to Jpeg format
MyDir = MyDir + "CADLayersToRasterImageFormats_out.jpg";
image.Save(MyDir, options);
```

عند استبدال `JpegOptions` بـ `PngOptions`، سيقوم نفس الكود **convert dxf to png** وينتج ملفًا بامتداد `.png`.

### خطوة إضافية: تحويل جميع الطبقات

إذا كنت تحتاج إلى **convert cad to raster** لكل طبقة في الرسم، استدعِ الدالة المساعدة أدناه. تقوم بالتكرار على جميع الطبقات وتحفظ كل واحدة كصورة منفصلة.

```csharp
ConvertAllLayersToRasterImageFormats();
```

> *ملاحظة:* تنفيذ `ConvertAllLayersToRasterImageFormats` هو جزء من مجموعة عينات Aspose.CAD الكاملة ويظهر معالجة دفعة للطبقات.

## المشكلات الشائعة واستكشاف الأخطاء وإصلاحها

| العَرَض | السبب المحتمل | الحل |
|---------|--------------|-----|
| صورة فارغة أو بيضاء | لم يتم تعيين خيارات الرستر (مثل `PageWidth`/`PageHeight` = 0) | تأكد من أن `PageWidth` و `PageHeight` لهما قيم موجبة |
| طبقات مفقودة | اسم طبقة غير صحيح في مصفوفة `Layers` | تحقق من اسم الطبقة الدقيق في ملف CAD (حسّاس لحالة الأحرف) |
| PNG منخفض الجودة | DPI الافتراضي منخفض | اضبط `rasterizationOptions.Resolution = 300;` للحصول على جودة أعلى |

## الأسئلة المتكررة (الأصلية)

### س1: هل يمكنني استخدام صيغ صور أخرى للتصدير؟

ج1: نعم، يمكنك ذلك. ما عليك سوى استبدال `JpegOptions` بخيارات الصيغة المطلوبة، مثل `PngOptions` أو `BmpOptions`.

### س2: هل تتوفر نسخة تجريبية؟

ج2: نعم، يمكنك استكشاف وظائف Aspose.CAD بتحميل النسخة التجريبية [هنا](https://releases.aspose.com/).

### س3: كيف يمكنني الحصول على دعم Aspose.CAD؟

ج3: زر منتدى Aspose.CAD [المنتدى](https://forum.aspose.com/c/cad/19) للحصول على دعم المجتمع أو فكر في شراء ترخيص للحصول على دعم مخصص.

### س4: هل تتوفر تراخيص مؤقتة؟

ج4: نعم، يمكنك الحصول على ترخيص مؤقت [هنا](https://purchase.aspose.com/temporary-license/).

### س5: أين يمكنني العثور على الوثائق؟

ج5: راجع الوثائق التفصيلية [هنا](https://reference.aspose.com/cad/net/).

## أسئلة إضافية

**س: هل يمكنني تصدير جميع الطبقات بأمر واحد؟**  
ج: نعم، استخدم طريقة `ConvertAllLayersToRasterImageFormats` الموضحة أعلاه.

**س: هل يدعم Aspose.CAD صيغ المتجهات مثل SVG؟**  
ج: يركز أساسًا على الصيغ النقطية، لكن يمكنك التصدير إلى PDF الذي يحتفظ ببيانات المتجه.

**س: كيف يمكنني التحكم في لون الخلفية للـ PNG المُصدّر؟**  
ج: اضبط `rasterizationOptions.BackgroundColor` إلى اللون `Color` المطلوب قبل الحفظ.

**س: هل يمكن تصدير تخطيط واحد بدلاً من الرسم الكامل؟**  
ج: نعم، قم بتكوين `rasterizationOptions.Layouts` لتحديد اسم (أسماء) التخطيط الذي تريد رسترته.

## الخاتمة

لقد تعلمت الآن كيفية **convert dxf to png**، **export cad layers**، و**save cad as png** أو JPEG باستخدام Aspose.CAD لـ .NET. من خلال تعديل `CadRasterizationOptions` وتبديل خيارات صيغ الصور، يمكنك تخصيص التحويل لأي مخرج نقطي تحتاجه تقريبًا. استكشف خيارات الصيغ الأخرى في واجهة Aspose.CAD لتوسيع سير عمل التحويل من CAD إلى النقطية.

---

**آخر تحديث:** 2026-03-21  
**تم الاختبار مع:** Aspose.CAD لـ .NET 24.11 (أحدث نسخة وقت الكتابة)  
**المؤلف:** Aspose  

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}