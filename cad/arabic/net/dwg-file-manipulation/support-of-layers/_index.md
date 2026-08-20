---
date: 2026-04-09
description: تعلم كيفية تصدير طبقات DWG، تحويل صورة DWG وحفظها كملف JPEG باستخدام
  C# مع Aspose.CAD لـ .NET. دليل خطوة بخطوة للتعامل الفعال مع ملفات CAD.
keywords:
- export dwg layers
- convert dwg image
- dwg layer visibility
- save dwg jpeg
linktitle: معالجة الطبقات في ملفات DWG باستخدام C#
second_title: Aspose.CAD .NET - CAD and BIM File Format
title: تصدير طبقات DWG باستخدام C# – دليل Aspose.CAD
url: /ar/net/dwg-file-manipulation/support-of-layers/
weight: 11
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# تصدير طبقات DWG باستخدام C# – دليل Aspose.CAD

## مقدمة

في هذا الدليل الشامل ستتعلم **كيفية تصدير طبقات DWG** باستخدام C# ومكتبة Aspose.CAD. سواء كنت بحاجة إلى **تحويل صيغ صورة DWG**، أو التحكم في **رؤية طبقة DWG**، أو ببساطة **حفظ ملفات DWG بصيغة JPEG**، ستوضح لك الخطوات أدناه كيفية القيام بذلك بكفاءة. في نهاية البرنامج التعليمي ستحصل على مقتطف جاهز للتنفيذ يعزل طبقة محددة ويحولها إلى صورة JPEG عالية الجودة.

## إجابات سريعة
- **ماذا يعني “تصدير طبقات dwg”؟** يعني تحويل الطبقات المحددة من ملف DWG إلى صيغة صورة مثل JPEG أو PNG.  
- **ما هي المكتبة الأفضل لهذه المهمة؟** Aspose.CAD لـ .NET توفر دعماً كاملاً دون الحاجة إلى AutoCAD.  
- **هل يمكنني تصدير عدة طبقات في آن واحد؟** نعم – مرّر مصفوفة من أسماء الطبقات إلى خيارات التحويل إلى نقطية.  
- **هل أحتاج إلى ترخيص للاستخدام في الإنتاج؟** يلزم الحصول على ترخيص تجاري؛ يتوفر نسخة تجريبية مجانية للتقييم.  
- **ما صيغ الإخراج المدعومة؟** JPEG، PNG، BMP، TIFF والعديد من الصيغ الأخرى عبر فئات ImageOptions.

## ما هو تصدير طبقات DWG؟
يعني تصدير طبقات DWG أخذ البيانات المتجهة التي تنتمي إلى طبقة أو أكثر داخل رسم DWG وتحويلها إلى صورة نقطية (bitmap). هذا مفيد عندما تريد مشاركة عرض لجزء محدد من الرسم دون الكشف عن ملف CAD بالكامل.

## لماذا التحكم في رؤية طبقة DWG؟
يتيح لك التحكم في رؤية الطبقة:

- إنشاء موارد بصرية نظيفة للعروض التقديمية أو الوثائق.  
- تقليل حجم الملف عن طريق تصدير الهندسة المطلوبة فقط.  
- حماية تفاصيل التصميم الملكية بإخفاء الطبقات السرية.

## المتطلبات المسبقة

قبل أن نبدأ، تأكد من أن لديك:

- معرفة أساسية بلغة البرمجة C#.  
- تثبيت Visual Studio على جهازك.  
- مكتبة Aspose.CAD لـ .NET، والتي يمكنك تنزيلها من [موقع Aspose.CAD](https://releases.aspose.com/cad/net/).

## استيراد المساحات الاسمية

لبدء العمل، استورد المساحات الاسمية التي تمنحك الوصول إلى ميزات التحويل إلى نقطية وتصدير الصور.

```csharp
using Aspose.CAD.ImageOptions;
using System;
using System.Collections.Generic;
using System.IO;
using System.Linq;
using System.Text;
```

## الخطوة 1: تحميل ملف DWG

حمّل ملف DWG (أو DWF) المصدر في كائن `Image`. هذا الكائن يمثل الرسم الكامل في الذاكرة.

```csharp
string MyDir = "Your Document Directory";
string sourceFilePath = MyDir + "for_layers_test.dwf";

using (Aspose.CAD.Image image = Aspose.CAD.Image.Load(sourceFilePath))
{
    // Your code for subsequent steps goes here
}
```

*لماذا هذا مهم:* تحميل الملف مرة واحدة يتيح لك إعادة استخدام نفس مثيل `image` لأي عدد من عمليات التصدير الخاصة بالطبقة، مما يحسن الأداء.

## الخطوة 2: تكوين خيارات التحويل إلى نقطية

أنشئ مثيل `CadRasterizationOptions` لتخبر Aspose.CAD كيفية عرض الرسم. هنا نحدد دقة عالية (1600 × 1600) لضمان أن يكون JPEG المصدّر حادًا.

```csharp
Aspose.CAD.ImageOptions.CadRasterizationOptions rasterizationOptions = new Aspose.CAD.ImageOptions.CadRasterizationOptions();
rasterizationOptions.PageWidth = 1600;
rasterizationOptions.PageHeight = 1600;
```

يمكنك أيضًا تعديل لون الخلفية، أو مقياس وزن الخطوط، أو إعدادات مضاد التعرج إذا لزم الأمر.

## الخطوة 3: تحديد الطبقات (رؤية طبقة DWG)

أضف الطبقات التي تريد **تصدير طبقات dwg** لها. في هذا المثال نقوم بتصدير “LayerA” فقط. لتصدير عدة طبقات، قم ببساطة بإدراجها في المصفوفة.

```csharp
rasterizationOptions.Layers = new string[] { "LayerA" };
```

*نصيحة احترافية:* استخدم الاسم الدقيق للطبقة كما هو موجود في الرسم؛ أسماء الطبقات حساسة لحالة الأحرف.

## الخطوة 4: تكوين خيارات تصدير الصورة

اختر صيغة الصورة التي ترغب في إنشائها. سنستخدم `JpegOptions` لأن JPEG يوفر توازنًا جيدًا بين الجودة وحجم الملف، وهو مثالي عندما تحتاج إلى **حفظ ملفات dwg jpeg** للمعاينة على الويب.

```csharp
JpegOptions jpegOptions = new JpegOptions();
jpegOptions.VectorRasterizationOptions = rasterizationOptions;
```

إذا كنت بحاجة إلى **تحويل صورة dwg** إلى PNG أو TIFF، استبدل `JpegOptions` بالفئة المقابلة للخيارات.

## الخطوة 5: حفظ الصورة المصدرة

حدد مسار ملف الإخراج واستدعِ `Save`. يحترم محرك التحويل إلى نقطية قائمة الطبقات التي قدمتها، لذا سيظهر “LayerA” فقط في JPEG النهائي.

```csharp
MyDir = MyDir + "for_layers_test.jpg";
image.Save(MyDir, jpegOptions);
```

بعد تنفيذ هذا السطر، ستجد `for_layers_test.jpg` في دليل المستندات الخاص بك، يحتوي فقط على الطبقة المحددة.

## المشكلات الشائعة والحلول

| المشكلة | الحل |
|-------|------------|
| **اسم الطبقة غير موجود** | تحقق من التهجئة الدقيقة وحالة الأحرف لاسم الطبقة في ملف DWG الأصلي. استخدم عارض CAD لعرض أسماء الطبقات. |
| **صورة الإخراج فارغة** | تأكد من أن خيارات التحويل إلى نقطية لديها خلفية غير شفافة وأن الطبقات المحددة تحتوي فعليًا على هندسة. |
| **إخراج منخفض الدقة** | زد من `PageWidth` و `PageHeight` أو اضبط `Resolution` في `CadRasterizationOptions`. |
| **إصدار DWG غير مدعوم** | قم بالتحديث إلى أحدث نسخة من Aspose.CAD؛ فهي تضيف دعمًا لإصدارات AutoCAD الأحدث. |

## الأسئلة المتكررة

### س1: هل يمكنني التعامل مع طبقات متعددة في وقت واحد؟
A1: نعم، يمكنك ذلك. ببساطة أضف أسماء الطبقات إلى مصفوفة `rasterizationOptions.Layers`.

### س2: هل تتوفر نسخة تجريبية من Aspose.CAD؟
A2: نعم، يمكنك الحصول على نسخة تجريبية مجانية من [هنا](https://releases.aspose.com/).

### س3: أين يمكنني العثور على الوثائق؟
A3: الوثائق متاحة [هنا](https://reference.aspose.com/cad/net/).

### س4: كيف يمكنني الحصول على الدعم لـ Aspose.CAD؟
A4: يمكنك طلب الدعم في [منتدى Aspose.CAD](https://forum.aspose.com/c/cad/19).

### س5: ما هي خيارات الترخيص لـ Aspose.CAD؟
A5: يمكنك استكشاف خيارات الترخيص وتفاصيل الشراء [هنا](https://purchase.aspose.com/buy).

**س: هل يمكنني تصدير الرسم إلى PNG بدلاً من JPEG؟**  
A: بالتأكيد. استبدل `JpegOptions` بـ `PngOptions` وعدّل امتداد الملف وفقًا لذلك.

**س: هل تحتفظ المكتبة بأنماط الخطوط والألوان؟**  
A: نعم. جميع خصائص المتجهات تُعرض بأمانة أثناء التحويل إلى نقطية.

**آخر تحديث:** 2026-04-09  
**تم الاختبار مع:** Aspose.CAD لـ .NET (أحدث إصدار)  
**المؤلف:** Aspose  

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}