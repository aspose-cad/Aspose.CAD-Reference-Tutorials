---
date: 2026-03-13
description: تعلم كيفية ضبط خيارات التحويل النقطي لبرنامج CAD وتصدير تخطيطات DWG المحددة
  إلى PDF باستخدام Aspose.CAD لـ .NET – الدليل الشامل لإنشاء PDF من ملف CAD.
linktitle: Exporting Specific Layouts to PDF
second_title: Aspose.CAD .NET - CAD and BIM File Format
title: تعيين خيارات التحويل النقطي لـ CAD – تصدير تخطيطات محددة إلى PDF - دليل Aspose.CAD
url: /ar/net/advanced-export-techniques/exporting-specific-layouts-to-pdf/
weight: 13
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# تصدير تخطيطات محددة إلى PDF - دليل Aspose.CAD

## مقدمة

في هذا البرنامج التعليمي ستكتشف **كيفية ضبط خيارات تمثيل CAD النقطية** حتى تتمكن من تصدير تخطيط واحد — أو عدة تخطيطات — من ملف DWG مباشرةً إلى PDF. تجعل Aspose.CAD لـ .NET عملية *dwg to pdf conversion c#* سهلة، وتمنحك التحكم الكامل في حجم الصفحة، الدقة، واختيار التخطيط. بنهاية الدليل ستكون قادرًا على **إنشاء PDF من ملف CAD** ببضع أسطر من الشيفرة.

## إجابات سريعة
- **ماذا يفعل “set cad rasterization options”?**  
  يخبر Aspose.CAD كيف يقوم برسم بيانات المتجه (التخطيطات، الطبقات، أوزان الخط) إلى صفحات PDF نقطية.  
- **ما الطريقة التي تصدر تخطيط DWG إلى PDF؟**  
  استخدم `Image.Save` مع `PdfOptions` مكوَّن يحتوي على `CadRasterizationOptions` الخاص بك.  
- **هل يمكنني تصدير أكثر من تخطيط في آن واحد؟**  
  نعم – قدم مصفوفة من أسماء التخطيطات في الخاصية `Layouts`.  
- **هل أحتاج إلى ترخيص للاستخدام الإنتاجي؟**  
  يلزم ترخيص تجاري؛ يتوفر نسخة تجريبية مجانية للتقييم.  
- **ما إصدارات .NET المدعومة؟**  
  .NET Framework 4.5+، .NET Core 3.1+، .NET 5/6 وما بعده.

## ما هو “set cad rasterization options”؟
`CadRasterizationOptions` هي الفئة التي تتحكم في كيفية تمثيل كائنات CAD نقطيًا عند التحويل إلى صيغ تعتمد على النقاط مثل PDF. من خلال ضبط خصائصها — أبعاد الصفحة، اختيار التخطيط، لون الخلفية، إلخ — تتحكم في النتيجة البصرية لعملية **export dwg layout to pdf**.

## لماذا ضبط خيارات تمثيل CAD النقطية؟
- **الدقة** – الحفاظ على أوزان الخطوط والمقاييس تمامًا كما تظهر في الرسم الأصلي لـ CAD.  
- **الأداء** – رسم فقط التخطيطات التي تحتاجها، مما يقلل من حجم الملف ووقت المعالجة.  
- **المرونة** – تعديل عرض/ارتفاع الصفحة، DPI، والخلفية لتتناسب مع معايير التقارير الخاصة بك.  

## المتطلبات المسبقة

قبل الغوص في الشيفرة، تأكد من أن لديك:

- **Aspose.CAD لـ .NET** مثبت. يمكنك تنزيله [هنا](https://releases.aspose.com/cad/net/).  
- بيئة تطوير .NET (Visual Studio، VS Code، أو أي IDE تفضله).  
- ملف DWG يحتوي على تخطيط واحد على الأقل (ملف العينة المستخدم هنا هو `visualization_-_conference_room.dwg`).

## استيراد مساحات الأسماء

في مشروع .NET الخاص بك، استورد مساحات الأسماء اللازمة لـ Aspose.CAD:

```csharp
using System;
using System.Collections.Generic;
using System.Linq;
using System.Text;
using System.Threading.Tasks;
using Aspose.CAD;
```

## دليل خطوة بخطوة

### الخطوة 1: تحميل ملف DWG

أولاً، وجه Aspose.CAD إلى ملف DWG المصدر الذي تريد تحويله.

```csharp
// The path to the documents directory.
string MyDir = "Your Document Directory";
string sourceFilePath = MyDir + "visualization_-_conference_room.dwg";

using (Image image = Image.Load(sourceFilePath))
{
    // Your code for further steps goes here.
}
```

### الخطوة 2: ضبط **CadRasterizationOptions**

هنا نقوم بضبط إعدادات التمثيل النقطي التي تحدد حجم صفحة PDF والدقة.

```csharp
// Create an instance of CadRasterizationOptions and set its various properties
CadRasterizationOptions rasterizationOptions = new CadRasterizationOptions();
rasterizationOptions.PageWidth = 1600;
rasterizationOptions.PageHeight = 1600;
```

> **نصيحة احترافية:** اضبط `PageWidth` و `PageHeight` لتتناسب مع أبعاد تخطيط PDF المستهدف. القيم الأكبر تزيد من التفاصيل ولكنها تزيد أيضًا من حجم الملف.

### الخطوة 3: تحديد اسم التخطيط

أخبر Aspose.CAD أي تخطيط(ات) يجب رسمها. استبدل `"Layout1"` بالاسم الدقيق للتخطيط في ملف DWG الخاص بك.

```csharp
// Specify desired layout name
rasterizationOptions.Layouts = new string[] { "Layout1" };
```

> **لماذا هذا مهم:** من خلال تقييد مصفوفة `Layouts` تتجنب تصدير الأوراق غير المرغوب فيها، مما يجعل عملية **dwg to pdf conversion c#** أسرع والـ PDF الناتج أنظف.

### الخطوة 4: إنشاء `PdfOptions`

ربط إعدادات التمثيل النقطي بخيارات تصدير PDF.

```csharp
// Create an instance of PdfOptions
PdfOptions pdfOptions = new PdfOptions();
// Set the VectorRasterizationOptions property
pdfOptions.VectorRasterizationOptions = rasterizationOptions;
```

### الخطوة 5: تصدير إلى PDF

أخيرًا، احفظ التخطيط المرسوم كملف PDF.

```csharp
MyDir = MyDir + "ExportSpecificLayoutToPDF_out.pdf";
// Export the DWG to PDF
image.Save(MyDir, pdfOptions);
```

### الخطوة 6: عرض رسالة نجاح

إخراج سريع إلى وحدة التحكم يؤكد نجاح العملية.

```csharp
// Display success message
Console.WriteLine("\nThe DWG file with a specific layout exported successfully to PDF.\nFile saved at " + MyDir);
```

## المشكلات الشائعة والحلول

| المشكلة | السبب | الحل |
|-------|-------|-----|
| **لم يتم إنشاء PDF** | مصفوفة `Layouts` لا تطابق أي اسم تخطيط في الـ DWG. | تحقق من أسماء التخطيطات باستخدام عارض CAD وقم بتحديث خاصية `Layouts`. |
| **صفحات فارغة** | تم ضبط `PageWidth`/`PageHeight` على 0 أو قيم صغيرة جدًا. | استخدم أبعادًا واقعية (مثال: 1600 × 1600) أو دع Aspose يحسب تلقائيًا بتجاهل تلك الخصائص. |
| **تحجيم غير صحيح** | لم يتم ضبط DPI عندما يكون الإخراج عالي الدقة مطلوبًا. | اضبط `rasterizationOptions.Resolution = 300;` (أو DPI المطلوب) قبل التصدير. |

## الأسئلة المتكررة

**س: هل يمكنني تصدير عدة تخطيطات في وقت واحد؟**  
ج: نعم، ما عليك سوى تعديل مصفوفة `Layouts` في الخطوة 3 لتشمل جميع أسماء التخطيطات المطلوبة، مثال: `new string[] { "Layout1", "Layout2" }`.

**س: هل Aspose.CAD متوافق مع صيغ CAD أخرى؟**  
ج: بالتأكيد. يدعم DWG، DXF، DWF، DGN، والعديد من الصيغ الأخرى.

**س: كيف يمكنني تعديل إعدادات إخراج PDF بخلاف حجم الصفحة؟**  
ج: استكشف خصائص إضافية في `CadRasterizationOptions` مثل `Resolution`، `BackgroundColor`، و `DrawType` لضبط النتيجة بدقة.

**س: أين يمكنني العثور على وثائق Aspose.CAD إضافية؟**  
ج: زر [documentation](https://reference.aspose.com/cad/net/) للحصول على مراجع API مفصلة وأمثلة.

**س: هل تتوفر نسخة تجريبية مجانية؟**  
ج: نعم، يمكنك الوصول إلى النسخة التجريبية المجانية [هنا](https://releases.aspose.com/).

## الخلاصة

لقد تعلمت الآن كيفية **ضبط خيارات تمثيل CAD النقطية** واستخدامها **لتصدير تخطيطات DWG محددة إلى PDF** باستخدام Aspose.CAD لـ .NET. يمنحك هذا النهج تحكمًا دقيقًا في عملية التحويل، مما يتيح لك دمج وظيفة CAD‑to‑PDF في أي تطبيق C# بسرعة وموثوقية.

---

**آخر تحديث:** 2026-03-13  
**تم الاختبار مع:** Aspose.CAD 24.11 for .NET  
**المؤلف:** Aspose  

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}