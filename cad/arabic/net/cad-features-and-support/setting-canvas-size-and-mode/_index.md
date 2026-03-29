---
date: 2026-03-29
description: تعلم كيفية إنشاء PDF من CAD، وتعيين حجم اللوحة، وتصدير CAD إلى PDF أو
  TIFF باستخدام Aspose.CAD لـ .NET في هذا الدليل خطوة بخطوة.
linktitle: Setting Canvas Size and Mode
second_title: Aspose.CAD .NET - CAD and BIM File Format
title: 'كيفية إنشاء PDF من CAD: تعيين حجم اللوحة والوضع في Aspose.CAD لـ .NET'
url: /ar/net/cad-features-and-support/setting-canvas-size-and-mode/
weight: 16
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# تعيين حجم القماش والوضع في Aspose.CAD لـ .NET

## مقدمة

هل أنت مستعد **إنشاء PDF من ملفات CAD** مع التحكم في أبعاد الإخراج؟ في هذا البرنامج التعليمي سنستعرض تعيين حجم القماش والوضع، تحميل ملف CAD، وتصديره إلى PDF أو TIFF باستخدام Aspose.CAD لـ .NET. سواء كنت بحاجة إلى **تحويل DXF إلى PDF**، أو إنشاء رسومات عالية الدقة، أو ببساطة تعديل منطقة الترصيص، ستوفر لك الخطوات أدناه حلاً ثابتًا وجاهزًا للإنتاج.

## إجابات سريعة
- **ما معنى “إنشاء PDF من CAD”؟** تحويل رسم CAD (مثل DXF, DWG) إلى مستند PDF يحافظ على تفاصيل المتجهات والراستر.  
- **ما الخيار الذي يتحكم في حجم الإخراج؟** `CadRasterizationOptions.PageWidth` و `PageHeight` (حجم القماش).  
- **هل يمكنني التصدير إلى TIFF أيضًا؟** نعم – استخدم `TiffOptions` مع نفس إعدادات الترصيص.  
- **هل أحتاج إلى ترخيص للإنتاج؟** يتطلب ترخيص تجاري؛ تتوفر نسخة تجريبية مجانية.  
- **الإصدارات المدعومة من .NET؟** .NET Framework 4.5+, .NET Core 3.1+, .NET 5/6/7.

## ما هو “إنشاء PDF من CAD”؟
إنشاء PDF من CAD يعني تحويل رسم CAD إلى تنسيق موجه للصفحات (PDF) يمكن عرضه أو طباعته أو مشاركته دون الحاجة إلى برنامج CAD. تقوم Aspose.CAD بالمعالجة الثقيلة، مما يتيح لك تحديد حجم القماش، والتحجيم، وتنسيق الإخراج.

## لماذا تعيين حجم القماش عند إنشاء PDF من CAD؟
تعيين حجم القماش يمنحك تحكمًا دقيقًا في الدقة والأبعاد للـ PDF أو TIFF الناتج. هذا مفيد بشكل خاص عندما:
- تحضير الرسومات للطباعة على أحجام ورق محددة.  
- إنشاء صور مصغرة أو صور عالية الدقة للمعاينة على الويب.  
- ضمان تخطيط متسق عبر مستندات متعددة.

## المتطلبات المسبقة

- مكتبة Aspose.CAD: قم بتنزيل وتثبيت مكتبة Aspose.CAD من [موقع Aspose.CAD](https://releases.aspose.com/cad/net/).
- بيئة التطوير: تأكد من وجود بيئة تطوير .NET مُعدة على جهازك.
- ملف CAD تجريبي: في هذا البرنامج التعليمي، سنستخدم ملف DXF تجريبي. يمكنك العثور على أحدهما في [توثيق Aspose.CAD](https://reference.aspose.com/cad/net/).

## استيراد مساحات الأسماء

أولاً، استورد مساحات الأسماء المطلوبة لمعالجة CAD:

```csharp
using System;
using System.Collections.Generic;
using System.Linq;
using System.Text;
using System.Threading.Tasks;
using Aspose.CAD;
```

## كيفية إنشاء PDF من CAD بحجم قماش مخصص

### الخطوة 1: تحميل ملف CAD

نبدأ بـ **تحميل ملف CAD** (مثل DXF) إلى كائن `Image`. هذه هي النقطة التي تقوم فيها **بتحميل ملف CAD** إلى الذاكرة.

```csharp
string MyDir = "Your Document Directory";
string sourceFilePath = MyDir + "conic_pyramid.dxf";

using (Image image = Image.Load(sourceFilePath))
{
    // Your code for further steps will go here
}
```

### الخطوة 2: إنشاء CadRasterizationOptions

أنشئ مثيلًا من `CadRasterizationOptions` وحدد حجم القماش. تسمح لك خصائص `PageWidth` و `PageHeight` **بتعيين حجم القماش** إلى الأبعاد الدقيقة التي تحتاجها.

```csharp
CadRasterizationOptions rasterizationOptions = new CadRasterizationOptions();
rasterizationOptions.PageWidth = 1600;
rasterizationOptions.PageHeight = 1600;
rasterizationOptions.AutomaticLayoutsScaling = true;
rasterizationOptions.NoScaling = false;
```

### الخطوة 3: إنشاء PdfOptions (تصدير CAD إلى PDF)

اربط إعدادات الترصيص بكائن `PdfOptions`. يتيح لك هذا التكوين **تصدير CAD إلى PDF** باستخدام القماش المخصص الذي حددته.

```csharp
PdfOptions pdfOptions = new PdfOptions();
pdfOptions.VectorRasterizationOptions = rasterizationOptions;
```

### الخطوة 4: التصدير إلى PDF (تحويل DXF إلى PDF)

الآن احفظ الصورة كملف PDF. هذه الخطوة **تنشئ PDF من CAD** باستخدام الخيارات التي حددناها.

```csharp
image.Save(MyDir + "result_out.pdf", pdfOptions);
```

### الخطوة 5: إنشاء TiffOptions (تصدير CAD إلى TIFF)

إذا كنت بحاجة أيضًا إلى صورة راستر، قم بتهيئة `TiffOptions`. يتم إعادة استخدام نفس إعدادات الترصيص، لذا فإن **تصدير CAD إلى TIFF** يحترم حجم القماش.

```csharp
TiffOptions tiffOptions = new TiffOptions(TiffExpectedFormat.Default);
tiffOptions.VectorRasterizationOptions = rasterizationOptions;
```

### الخطوة 6: التصدير إلى TIFF

أخيرًا، احفظ الرسم كملف TIFF.

```csharp
image.Save(MyDir + "result_out.tiff", tiffOptions);
```

## المشكلات الشائعة والحلول

- **القماش يظهر مقطوعًا** – تحقق من أن `AutomaticLayoutsScaling` مضبوط على `true` و `NoScaling` على `false` بحيث يتم تحجيم الرسم ليتناسب مع القماش.  
- **PDF منخفض الدقة** – زد `PageWidth`/`PageHeight` أو اضبط `Resolution` في `CadRasterizationOptions`.  
- **خطأ ملف غير موجود** – تأكد من أن `MyDir` يشير إلى دليل صالح وأن اسم ملف DXF يطابق تمامًا.

## الأسئلة المتكررة

### س1: هل يمكنني استخدام Aspose.CAD مع مكتبات .NET أخرى؟
A1: نعم، يتكامل Aspose.CAD بسلاسة مع مكتبات .NET الأخرى، مما يوفر قدرات محسنة لمعالجة CAD.

### س2: هل تتوفر نسخة تجريبية مجانية لـ Aspose.CAD؟
A2: نعم، يمكنك استكشاف ميزات Aspose.CAD من خلال نسخة تجريبية مجانية. زر [هنا](https://releases.aspose.com/) للبدء.

### س3: كيف يمكنني الحصول على الدعم لـ Aspose.CAD؟
A3: للحصول على الدعم والمناقشات، زر [منتدى Aspose.CAD](https://forum.aspose.com/c/cad/19).

### س4: أين يمكنني العثور على وثائق شاملة لـ Aspose.CAD؟
A4: راجع [توثيق Aspose.CAD](https://reference.aspose.com/cad/net/) للحصول على معلومات مفصلة وأمثلة.

### س5: كيف يمكنني شراء Aspose.CAD لـ .NET؟
A5: لشراء Aspose.CAD، زر [صفحة الشراء](https://purchase.aspose.com/buy).

**أسئلة وإجابات إضافية**

**س: هل يمكنني تصدير رسم CAD متعدد الصفحات إلى PDF واحد؟**  
A: نعم. اضبط `PageCount` في `CadRasterizationOptions` وستقوم المكتبة بدمج الصفحات في PDF واحد.

**س: هل يؤثر حجم القماش على جودة البيانات المتجهة؟**  
A: تظل البيانات المتجهة مستقلة عن الدقة؛ حجم القماش يؤثر فقط على العناصر المرسومة كراستر ودقة الصورة.

---

**آخر تحديث:** 2026-03-29  
**تم الاختبار مع:** Aspose.CAD 24.11 لـ .NET  
**المؤلف:** Aspose  

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}