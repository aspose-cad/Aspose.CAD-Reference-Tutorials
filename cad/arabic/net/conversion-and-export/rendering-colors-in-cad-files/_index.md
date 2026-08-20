---
date: 2026-04-03
description: تعلم كيفية عرض ملفات CAD وتحويل DWG إلى PNG باستخدام Aspose.CAD لـ .NET.
  دليل خطوة بخطوة لحفظ CAD كصورة.
keywords:
- how to render cad
- convert dwg to png
- export cad to png
- save cad as image
- load dwg in .net
linktitle: تصيير الألوان في ملفات CAD
second_title: Aspose.CAD .NET - CAD and BIM File Format
title: كيفية تصيير ملفات CAD بالألوان – دليل Aspose.CAD
url: /ar/net/conversion-and-export/rendering-colors-in-cad-files/
weight: 10
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# كيفية عرض ملفات CAD بالألوان – دليل Aspose.CAD

## مقدمة

هل تواجه صعوبة في **كيفية عرض ملفات CAD** بألوان زاهية باستخدام .NET؟ في هذا الدليل الشامل خطوة بخطوة سنوضح لك بالضبط كيفية عرض الألوان في ملفات CAD، وتحويل DWG إلى PNG، وحفظ رسومات CAD كصور عالية الجودة باستخدام مكتبة Aspose.CAD.

## إجابات سريعة
- **ما هي المكتبة الأفضل لعرض ألوان CAD؟** Aspose.CAD for .NET  
- **هل يمكنني تحويل DWG إلى PNG في خطوة واحدة؟** نعم – قم بتحويل DWG إلى صورة نقطية واحفظه كـ PNG.  
- **هل أحتاج إلى ترخيص للاستخدام في الإنتاج؟** ترخيص مؤقت يعمل للاختبار؛ يلزم ترخيص كامل للإنتاج.  
- **ما إصدارات .NET المدعومة؟** .NET Framework 4.5+, .NET Core 3.1+, .NET 5/6/7.  
- **هل العملية سريعة بما يكفي للتحويل على دفعات؟** يتم تنفيذ العرض في الذاكرة وهو مناسب للعمليات الضخمة.

## ما هو عرض الألوان في ملفات CAD؟

يعني عرض الألوان أخذ المعلومات المتجهية المخزنة في رسم CAD (DWG، DXF، إلخ) وتحويلها إلى صورة نقطية مع الحفاظ على ألوان الكائنات الأصلية. هذا أمر أساسي عندما تحتاج إلى مشاركة مرئيات CAD مع أصحاب المصلحة الذين لا يمتلكون برنامج CAD.

## لماذا تستخدم Aspose.CAD لتحويل DWG إلى PNG؟

- **بدون تبعيات خارجية** – يعمل بالكامل دون اتصال.  
- **دقة كاملة** – يتم الاحتفاظ بألوان الكائنات، وسماكات الخطوط، والطبقات.  
- **واجهة برمجة تطبيقات بسيطة** – سطر واحد من الكود للتحميل، الإعداد، والحفظ.  
- **متعدد المنصات** – يعمل على أنظمة Windows وLinux وmacOS runtimes الخاصة بـ .NET.

## المتطلبات المسبقة

- مكتبة Aspose.CAD: قم بتنزيل وتثبيت مكتبة Aspose.CAD من [هنا](https://releases.aspose.com/cad/net/).  
- بيئة التطوير: تأكد من إعداد بيئة تطوير .NET.  
- ملف CAD: احرص على وجود ملف CAD تجريبي جاهز للاختبار. يمكنك استخدام “test1.dwg” لهذا الدرس.

## استيراد مساحات الأسماء

في مشروع .NET الخاص بك، استورد مساحات الأسماء اللازمة للوصول إلى وظائف Aspose.CAD. أضف الأسطر التالية في بداية الكود الخاص بك:

```csharp
using Aspose.CAD.ImageOptions;
using System;
using System.Collections.Generic;
using System.IO;
using System.Linq;
using System.Text;
```

## الخطوة 1: إعداد مشروعك

أنشئ مشروع .NET جديدًا وقم بإعداد الأدلة المطلوبة. تأكد من أن مكتبة Aspose.CAD مُشار إليها في مشروعك.

## الخطوة 2: تعريف مسارات الملفات

حدد مسارات ملف CAD الإدخالي وملف PNG الناتج. حدّث الأسطر التالية في الكود الخاص بك:

```csharp
string MyDir = "Your Document Directory";
string inputFile = MyDir + "test1.dwg";
string outputFile = MyDir + "test1.png";
```

## الخطوة 3: تحميل ملف CAD

استخدم الكود التالي لفتح وتحميل ملف CAD:

```csharp
using (FileStream fs = new FileStream(inputFile, FileMode.Open))
{
    using (FileStream output = new FileStream(outputFile, FileMode.Create))
    {
        Image document = Image.Load(fs);
```

## الخطوة 4: تكوين خيارات التحويل إلى صورة نقطية

قم بتكوين خيارات التحويل إلى صورة نقطية لتخصيص عملية العرض. حدّث الأسطر التالية:

```csharp
PngOptions saveOptions = new PngOptions();

CadRasterizationOptions options = new CadRasterizationOptions();
options.NoScaling = false;
options.PageHeight = document.Height * 10;
options.PageWidth = document.Width * 10;
options.DrawType = Aspose.CAD.FileFormats.Cad.CadDrawTypeMode.UseObjectColor;
saveOptions.VectorRasterizationOptions = options;
```

## الخطوة 5: حفظ الصورة المُعالجة

احفظ الصورة المُعالجة باستخدام الخيارات المحددة:

```csharp
document.Save(output, saveOptions);
```

## لماذا هذا مهم

حفظ CAD كصورة (PNG، JPEG، إلخ) هو طلب شائع عندما تحتاج إلى تضمين الرسومات في التقارير أو صفحات الويب أو مرفقات البريد الإلكتروني. من خلال إتقان **كيفية عرض CAD**، تلغي الحاجة إلى عارضين من طرف ثالث وتضمن إخراجًا بصريًا متسقًا عبر جميع المنصات.

## المشكلات الشائعة والحلول

| المشكلة | السبب | الحل |
|-------|-------|----------|
| صورة فارغة | تم تعيين `NoScaling` إلى `true` بأبعاد صفرية | تأكد من حساب `PageHeight` و `PageWidth` من الصورة المحملة (كما هو موضح). |
| الألوان تظهر بشكل غير صحيح | `DrawType` غير صحيح | استخدم `CadDrawTypeMode.UseObjectColor` للحفاظ على ألوان الكائنات الأصلية. |
| الملف غير موجود | مسار `MyDir` غير صحيح | تحقق من أن مسار الدليل ينتهي بشرطة مائلة أو استخدم `Path.Combine`. |
| نفاد الذاكرة على ملفات كبيرة | العرض بدقة DPI عالية جدًا | قلل عامل التحجيم (مثلاً `*5` بدلاً من `*10`). |

## الخاتمة

تهانينا! لقد تعلمت بنجاح **كيفية عرض CAD**، وتحويل DWG إلى PNG، و**حفظ CAD كصورة** باستخدام Aspose.CAD لـ .NET. تتيح لك هذه المعرفة دمج عرض CAD مباشرةً في تطبيقاتك، وأتمتة إنشاء التقارير، ومعاينات الويب، وأكثر.

## الأسئلة المتكررة

### س1: هل يمكنني استخدام Aspose.CAD مجانًا؟

ج1: تقدم Aspose.CAD نسخة تجريبية مجانية متاحة [هنا](https://releases.aspose.com/). يمكنك استكشاف ميزاتها قبل الشراء.

### س2: أين يمكنني العثور على وثائق مفصلة لـ Aspose.CAD؟

ج2: راجع الوثائق [هنا](https://reference.aspose.com/cad/net/) للحصول على معلومات متعمقة حول وظائف Aspose.CAD.

### س3: كيف أحصل على ترخيص مؤقت لـ Aspose.CAD؟

ج3: احصل على ترخيص مؤقت [هنا](https://purchase.aspose.com/temporary-license/) لأغراض الاختبار.

### س4: هل تحتاج إلى مساعدة أو لديك أسئلة؟

ج4: زر منتدى مجتمع Aspose.CAD [المنتدى](https://forum.aspose.com/c/cad/19) للحصول على الدعم والنقاشات.

### س5: أين يمكنني شراء مكتبة Aspose.CAD؟

ج5: اشترِ Aspose.CAD [هنا](https://purchase.aspose.com/buy) لفتح إمكاناته الكاملة.

## أسئلة متكررة إضافية

**س: كيف يمكنني **تحويل DWG إلى PNG** دون فقدان سماكة الخط؟**  
ج: احتفظ بالتحجيم الافتراضي لـ `PageHeight` و `PageWidth` (مثلاً، اضرب في 10) واضبط `options.DrawType` إلى `UseObjectColor`. هذا يحافظ على سماكات الخطوط والألوان.

**س: هل من الممكن **تصدير CAD إلى PNG** في خدمة خلفية؟**  
ج: نعم. واجهة برمجة تطبيقات Aspose.CAD آمنة للثريد للعمليات القراءة فقط، لذا يمكنك تحميل وتحويل الملفات داخل عامل خلفية.

**س: هل يمكنني **تحميل DWG في .NET** من مصفوفة بايت بدلاً من ملف؟**  
ج: بالتأكيد. استخدم `Image.Load(byteArray)` بدلاً من `FileStream` واتبع نفس خطوات التحويل إلى صورة نقطية.

**س: أي تنسيق يجب أن أختاره للحصول على أفضل جودة عند **حفظ CAD كصورة**؟**  
ج: PNG يوفر ضغطًا بدون فقدان ويحافظ على دقة الألوان، مما يجعله مثاليًا للرسومات التقنية.

**س: هل تدعم Aspose.CAD صيغ نقطية أخرى مثل JPEG أو BMP؟**  
ج: نعم – استبدل ببساطة `PngOptions` بـ `JpegOptions` أو `BmpOptions` واضبط أي إعدادات خاصة بالتنسيق.

**آخر تحديث:** 2026-04-03  
**تم الاختبار مع:** Aspose.CAD 24.11 لـ .NET  
**المؤلف:** Aspose  

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}