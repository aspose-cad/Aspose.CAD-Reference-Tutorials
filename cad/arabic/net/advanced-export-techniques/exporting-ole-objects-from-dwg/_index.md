---
description: تعلم كيفية تحويل DWG إلى PNG واستخراج كائنات OLE من ملفات DWG باستخدام
  Aspose.CAD لـ .NET – دليل سريع يركز على الكود.
linktitle: Exporting OLE Objects from DWG Files
second_title: Aspose.CAD .NET - CAD and BIM File Format
title: تحويل DWG إلى PNG وتصدير كائنات OLE - دليل Aspose.CAD
url: /ar/net/advanced-export-techniques/exporting-ole-objects-from-dwg/
weight: 12
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# تصدير كائنات OLE من ملفات DWG - دليل Aspose.CAD

## المقدمة

إذا كنت بحاجة إلى **convert DWG to PNG** مع استخراج كائنات OLE المدمجة، فقد وصلت إلى المكان الصحيح. يجعل Aspose.CAD for .NET هذه العملية ذات الخطوتين بسيطة، حيث يتيح لك أتمتة الاستخراج والرستر في بضع أسطر من C#. خلال الدقائق القليلة القادمة سنستعرض سير العمل بالكامل، من إعداد البيئة حتى حفظ كل ملف DWG كصورة PNG تحتوي على بيانات OLE المستخرجة.

## إجابات سريعة
- **ما الذي يغطيه هذا الدليل؟** تحويل DWG إلى PNG واستخراج كائنات OLE باستخدام Aspose.CAD for .NET.  
- **هل أحتاج إلى ترخيص؟** النسخة التجريبية المجانية تكفي للتطوير؛ يلزم ترخيص تجاري للإنتاج.  
- **ما إصدارات .NET المدعومة؟** .NET Framework 4.5+، .NET Core 3.1+، .NET 5/6+.  
- **هل يمكنني معالجة عدة ملفات DWG في آن واحد؟** نعم – العينة تقوم بالتكرار عبر مصفوفة من أسماء الملفات.  
- **أين يمكنني العثور على المزيد من الأمثلة؟** اطلع على وثائق Aspose.CAD الرسمية وروابط المنتدى أدناه.

## ما هو **convert DWG to PNG**؟
تحويل DWG (رسم AutoCAD) إلى صورة PNG يقوم برسترة البيانات المتجهة، مما يجعل من السهل عرضها أو تضمينها في صفحات الويب، التقارير، أو التطبيقات الأخرى التي لا تدعم DWG أصلاً. عندما تكون كائنات OLE موجودة، يمكن استخراجها وحفظها كملفات منفصلة أثناء التحويل.

## لماذا نحتاج إلى استخراج كائنات OLE من ملفات CAD؟
العديد من رسومات DWG تدمج جداول بيانات، مخططات، أو مستندات Office أخرى ككائنات OLE. يتيح لك استخراجها إعادة استخدام البيانات الأصلية، أتمتة إعداد التقارير، أو نقل المحتوى إلى صيغ أحدث دون فقدان المعلومات المدمجة.

## المتطلبات المسبقة

- مكتبة Aspose.CAD for .NET: تأكد من تثبيت المكتبة. يمكنك تنزيلها من [صفحة تنزيل Aspose.CAD for .NET](https://releases.aspose.com/cad/net/).
- دليل المستندات: أنشئ دليلًا يحتوي على ملفات DWG الخاصة بك. استبدل `"Your Document Directory"` في المقتطف البرمجي بالمسار الفعلي.

## استيراد المساحات الاسمية

في مشروع .NET الخاص بك، استورد المساحات الاسمية المطلوبة:

```csharp
using Aspose.CAD.FileFormats.Cad;
using Aspose.CAD.ImageOptions;
using System;
using System.Collections.Generic;
using System.Linq;
using System.Text;
```

## دليل خطوة بخطوة

### الخطوة 1: تعيين دليل المستندات

```csharp
string MyDir = "Your Document Directory";
```

استبدل `"Your Document Directory"` بالمسار الذي توجد فيه ملفات DWG.

### الخطوة 2: سرد ملفات DWG التي تريد معالجتها

```csharp
string[] files = new string[] { "D ZD junior D10m H2m.dwg", "ZD - Senior D6m H2m45.dwg" };
```

### الخطوة 3: تكوين خيارات التصدير لتحويل PNG

```csharp
PngOptions pngOptions = new PngOptions { };
CadRasterizationOptions rasterizationOptions = new CadRasterizationOptions();
pngOptions.VectorRasterizationOptions = rasterizationOptions;
rasterizationOptions.Layouts = new string[] { "Layout1" };
```

يمكنك تعديل `CadRasterizationOptions` (مثل `PageWidth`، `PageHeight`، `BackgroundColor`) لتتناسب مع الدقة المطلوبة للخرج.

### الخطوة 4: التكرار عبر كل ملف DWG وإجراء التحويل

```csharp
foreach (string file in files)
{
    using (CadImage cadImage = (CadImage)Image.Load(MyDir + file))
    {
        cadImage.Save(MyDir + file + "_out.png", pngOptions);
    }
}
```

خلال هذه الحلقة تقوم المكتبة تلقائيًا **extracts OLE objects** المدمجة في كل رسم وتضمّنها في صورة PNG المُولدة. إذا كنت بحاجة إلى تدفقات OLE الخام، يمكنك الوصول إلى مجموعة `cadImage.OleObjects` – طريقة مفيدة لـ **how to extract ole** برمجيًا.

## المشكلات الشائعة & استكشاف الأخطاء

- **اسم التخطيط مفقود** – تأكد من أن التخطيط الذي تحدده (`"Layout1"` في المثال) موجود في ملف DWG المصدر؛ وإلا سيعود الرستر إلى مساحة النموذج الافتراضية.  
- **الملفات الكبيرة تسبب ضغطًا على الذاكرة** – عالج الملفات واحدةً تلو الأخرى (كما هو موضح) وتخلص من كائنات `CadImage` فورًا باستخدام `using`.  
- **ألوان غير متوقعة** – اضبط `rasterizationOptions.BackgroundColor` لتطابق خلفية الرسم إذا كانت الشفافية مطلوبة.

## الأسئلة المتكررة

### س1: هل Aspose.CAD for .NET مناسب لكل من ملفات CAD المبتدئة والمتقدمة؟
ج1: نعم، Aspose.CAD for .NET متعدد الاستخدامات ويمكنه التعامل مع مجموعة واسعة من ملفات CAD، بما في ذلك الإصدارات المبتدئة والمتقدمة.

### س2: هل يمكنني تخصيص خيارات التصدير لتخطيطات مختلفة؟
ج2: بالتأكيد! كما هو موضح في الدليل، يمكنك تعديل خيارات التصدير، بما في ذلك التخطيطات، لتناسب احتياجاتك الخاصة.

### س3: أين يمكنني العثور على وثائق مفصلة لـ Aspose.CAD for .NET؟
ج3: استكشف [وثائق Aspose.CAD for .NET](https://reference.aspose.com/cad/net/) للحصول على معلومات متعمقة وأمثلة.

### س4: هل هناك نسخة تجريبية مجانية؟
ج4: نعم، يمكنك تجربة إمكانيات Aspose.CAD for .NET عبر نسخة تجريبية مجانية. زر [هذا الرابط](https://releases.aspose.com/) للبدء.

### س5: كيف يمكنني الحصول على الدعم أو التواصل مع المجتمع؟
ج5: للحصول على الدعم والتفاعل مع المجتمع، زر [منتدى Aspose.CAD](https://forum.aspose.com/c/cad/19).

### س6: كيف يمكنني **extract OLE from CAD** دون تحويل إلى PNG؟
ج6: استخدم مجموعة `CadImage.OleObjects` بعد تحميل ملف DWG؛ يمكنك التكرار عبر كل `OleObject` وحفظ بياناته الخام إلى ملف.

## الخاتمة

لقد رأيت الآن كيفية **convert DWG to PNG** مع **extracting OLE objects** بسلاسة باستخدام Aspose.CAD for .NET. هذه الطريقة توفر الوقت، وتلغي خطوات النسخ اليدوي، وتندمج بسهولة في خطوط الأنابيب الآلية. لا تتردد في تجربة صيغ رستر أخرى (JPEG، BMP) أو استكشاف مجموعة ميزات معالجة CAD الغنية التي يقدمها Aspose.

---

**آخر تحديث:** 2026-03-13  
**تم الاختبار مع:** Aspose.CAD 24.11 for .NET  
**المؤلف:** Aspose  

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}