---
date: 2026-03-19
description: تعلم كيفية تغيير حجم رسومات CAD في .NET باستخدام Aspose.CAD، بما في ذلك
  كيفية تعديل وحدات رسومات CAD وضبط حجم التخطيط. اتبع دليلنا خطوة بخطوة.
linktitle: Adjusting CAD Drawing Size
second_title: Aspose.CAD .NET - CAD and BIM File Format
title: كيفية تغيير حجم رسومات CAD باستخدام Aspose.CAD لـ .NET
url: /ar/net/cad-drawing-manipulation/adjust-cad-drawing-size/
weight: 10
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# كيفية تغيير حجم رسومات CAD باستخدام Aspose.CAD لـ .NET

## مقدمة

إذا كنت بحاجة إلى **how to resize CAD** الملفات مباشرةً من تطبيق .NET الخاص بك، فقد وجدت المكان المناسب. في هذا البرنامج التعليمي سنوضح لك كيفية تغيير إعدادات وحدة CAD، وتكبير أبعاد رسومات CAD، وضبط حجم CAD برمجياً باستخدام Aspose.CAD لـ .NET. في نهاية الدليل ستحصل على حل قوي وجاهز للإنتاج لتغيير حجم أي تنسيق CAD مدعوم.

## إجابات سريعة
- **ما المكتبة المطلوبة؟** Aspose.CAD for .NET  
- **هل يمكنني تغيير نوع الوحدة؟** نعم – عيّن `UnitType` في `CadRasterizationOptions`  
- **هل يلزم ترخيص للإنتاج؟** يلزم وجود ترخيص Aspose.CAD صالح للاستخدام غير التجريبي  
- **ما هو تنسيق الصورة الذي يصدره المثال؟** BMP (ولكن أي تنسيق نقطي مدعوم يعمل)  
- **كم عدد أسطر الشيفرة؟** أقل من 30 سطرًا لعملية تغيير الحجم الكاملة  

## ما هو “how to resize CAD” عمليًا؟
تغيير حجم رسم CAD يعني تحويل البيانات المتجهة إلى صورة نقطية بمقياس أو وحدة محددة (مثلاً السنتيمترات أو البوصات). هذا مفيد عندما تحتاج إلى تضمين الرسومات في التقارير، أو إنشاء صور مصغرة، أو دمج مرئيات CAD في صفحات الويب.

## لماذا تعديل حجم CAD باستخدام Aspose.CAD؟
- **لا يوجد برنامج CAD خارجي** – كل شيء يعمل داخل شفرة .NET الخاصة بك.  
- **تحكم دقيق** في الوحدات، والتخطيطات، وخيارات التحويل النقطي.  
- **دعم متعدد الصيغ** – نفس الشفرة تعمل مع DWG، DXF، DWF، وأكثر.  

## المتطلبات المسبقة

قبل أن نبدأ، تأكد من وجود ما يلي:

- مكتبة Aspose.CAD لـ .NET: قم بتنزيل وتثبيت المكتبة من [صفحة تنزيل Aspose.CAD لـ .NET](https://releases.aspose.com/cad/net/).  
- رسمة CAD تجريبية: ملف مثل `sample.dwg` موجود في دليل المستندات الخاص بمشروعك.  

## استيراد مساحات الأسماء

أولاً، استورد مساحات الأسماء التي تمنحك الوصول إلى فئات Aspose.CAD.

```csharp
using System;
using System.Collections.Generic;
using System.Linq;
using System.Text;
using System.Threading.Tasks;
using Aspose.CAD;
```

## الخطوة 1: تحميل رسم CAD

حمّل ملف المصدر في كائن `Image`. هذا الكائن يمثل رسم CAD في الذاكرة وسيكون الأساس لجميع العمليات اللاحقة.

```csharp
string MyDir = "Your Document Directory";
string sourceFilePath = MyDir + "sample.dwg";

// Load a CAD drawing in an instance of Image
using (var image = Aspose.CAD.Image.Load(sourceFilePath))
{
    // Your code here...
}
```

## الخطوة 2: إنشاء BmpOptions (أو أي تنسيق نقطي آخر)

`BmpOptions` تخبر Aspose.CAD كيفية عرض البيانات المتجهة عندما تقوم بحفظها كصورة bitmap. يمكنك استبداله بـ `PngOptions` أو `JpegOptions`، إلخ، حسب تنسيق الهدف.

```csharp
Aspose.CAD.ImageOptions.BmpOptions bmpOptions = new Aspose.CAD.ImageOptions.BmpOptions();
```

## الخطوة 3: تعيين CadRasterizationOptions

`CadRasterizationOptions` يحتوي على الإعدادات الأساسية للتكبير، وتحويل الوحدات، واختيار التخطيط. ربطه بخصائص `VectorRasterizationOptions` في `BmpOptions` يضمن أن يستخدم المرسّخ إعداداتك المخصصة.

```csharp
Aspose.CAD.ImageOptions.CadRasterizationOptions cadRasterizationOptions = new Aspose.CAD.ImageOptions.CadRasterizationOptions();
bmpOptions.VectorRasterizationOptions = cadRasterizationOptions;
```

## الخطوة 4: تعيين UnitType (تغيير وحدة CAD)

هنا نقوم بتغيير وحدة CAD من الافتراضية إلى السنتيمترات. هذا هو المكان الذي توجد فيه كلمة **change cad unit**، وتؤثر مباشرة على حجم الصورة النهائي.

```csharp
cadRasterizationOptions.UnitType = Aspose.CAD.ImageOptions.UnitType.Centimeter;
```

## الخطوة 5: اختيار التخطيطات (تعيين تخطيطات CAD)

إذا كان رسمك يحتوي على عدة تخطيطات (مثلاً Model، Sheet1)، حدد أي منها تريد تحويله إلى نقطي. اختيار التخطيط الصحيح أمر أساسي عندما **set cad layouts** لإخراج بحجم معدل.

```csharp
cadRasterizationOptions.Layouts = new string[] { "Model" };
```

## الخطوة 6: تصدير إلى BMP (تغيير حجم رسم CAD)

أخيرًا، احفظ الصورة النقطية. ملف الإخراج يعكس الحجم الجديد، والوحدة، والتخطيط الذي قمت بتكوينه—مما يكمل عملية **resize CAD drawing**.

```csharp
string outPath = sourceFilePath + ".bmp";
image.Save(outPath, bmpOptions);
```

الآن لديك ملف BMP يمثل رسم CAD المُعاد حجمه، جاهز للمعالجة أو العرض الإضافي.

## المشكلات الشائعة والحلول

| المشكلة | لماذا يحدث | الحل |
|-------|----------------|-----|
| الصورة غير واضحة | دقة DPI منخفضة (النقاط في البوصة) بشكل افتراضي | عيّن `cadRasterizationOptions.Resolution = 300;` قبل الحفظ |
| ظهور تخطيط خاطئ | خطأ إملائي في اسم التخطيط | تحقق من اسم التخطيط الدقيق باستخدام عارض CAD أو مجموعة `Layouts` |
| تحويل الوحدة غير صحيح | خلط الوحدات المترية والإمبراطورية | تأكد من أن `UnitType` يطابق نظام القياس المطلوب |

## الأسئلة المتكررة

### س1: هل Aspose.CAD لـ .NET متوافق مع جميع صيغ CAD؟

ج1: Aspose.CAD لـ .NET يدعم مجموعة واسعة من صيغ CAD، بما في ذلك DWG، DXF، DWF، وأكثر. راجع [التوثيق](https://reference.aspose.com/cad/net/) للقائمة الكاملة.

### س2: هل يمكنني تغيير حجم عدة تخطيطات في آن واحد؟

ج2: نعم، يمكنك تغيير حجم عدة تخطيطات عن طريق تعديل مصفوفة `Layouts` في `CadRasterizationOptions`.

### س3: أين يمكنني الحصول على دعم Aspose.CAD لـ .NET؟

ج3: زر [منتدى Aspose.CAD](https://forum.aspose.com/c/cad/19) للحصول على دعم المجتمع والمساعدة.

### س4: هل هناك نسخة تجريبية مجانية متاحة؟

ج4: نعم، يمكنك تجربة [نسخة تجريبية مجانية](https://releases.aspose.com/) لتقييم ميزات Aspose.CAD لـ .NET.

### س5: كيف يمكنني الحصول على ترخيص مؤقت لـ Aspose.CAD لـ .NET؟

ج5: احصل على ترخيص مؤقت لأغراض الاختبار [من هنا](https://purchase.aspose.com/temporary-license/).

## الأسئلة المتكررة

**س: كيف أقوم بتكبير رسم CAD دون تغيير نوع الوحدة؟**  
ج: اضبط خاصية `Zoom` في `CadRasterizationOptions` (مثلاً `cadRasterizationOptions.Zoom = 2.0;`) لتضاعف الحجم مع الحفاظ على الوحدة الأصلية.

**س: هل يمكنني التصدير إلى صيغ غير BMP؟**  
ج: بالتأكيد. استبدل `BmpOptions` بـ `PpngOptions` أو `JpegOptions` أو أي فئة تنسيق نقطي مدعومة أخرى.

**س: هل من الممكن معالجة مجموعة من الرسومات في مجلد دفعة واحدة؟**  
ج: نعم. قم بالتكرار عبر الملفات في دليل، طبق نفس منطق التحويل النقطي، واحفظ كل إخراج باسم فريد.

---

**آخر تحديث:** 2026-03-19  
**تم الاختبار باستخدام:** Aspose.CAD for .NET 24.11 (latest at time of writing)  
**المؤلف:** Aspose  

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}