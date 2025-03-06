---
title: ضبط حجم رسم CAD في Aspose.CAD لـ .NET
linktitle: ضبط حجم رسم CAD
second_title: Aspose.CAD .NET - تنسيق ملف CAD وBIM
description: تعرف على كيفية ضبط أحجام رسم CAD في .NET بسهولة باستخدام Aspose.CAD. اتبع دليلنا خطوة بخطوة لتغيير الحجم بسلاسة.
weight: 10
url: /ar/net/cad-drawing-manipulation/adjust-cad-drawing-size/
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# ضبط حجم رسم CAD في Aspose.CAD لـ .NET

## مقدمة

هل تتطلع إلى ضبط حجم رسومات CAD بسلاسة في تطبيقات .NET الخاصة بك؟ يوفر Aspose.CAD for .NET حلاً قويًا، مما يسمح لك بالتعامل بسهولة مع تغيير حجم رسم CAD. في هذا البرنامج التعليمي، سنرشدك خلال العملية، مع تفصيل كل خطوة للتأكد من فهمك لتعقيدات تغيير حجم رسومات CAD باستخدام Aspose.CAD.

## المتطلبات الأساسية

قبل أن نتعمق في البرنامج التعليمي، تأكد من توفر المتطلبات الأساسية التالية:

- Aspose.CAD for .NET Library: قم بتنزيل المكتبة وتثبيتها من ملف[صفحة تنزيل Aspose.CAD لـ .NET](https://releases.aspose.com/cad/net/).
- نموذج رسم CAD: تأكد من وجود نموذج لملف رسم CAD (على سبيل المثال، "sample.dwg") في دليل المستند.

## استيراد مساحات الأسماء

ابدأ باستيراد مساحات الأسماء الضرورية إلى تطبيق .NET الخاص بك. تعتبر هذه الخطوة ضرورية للوصول إلى الوظائف التي يوفرها Aspose.CAD لـ .NET.

```csharp
using System;
using System.Collections.Generic;
using System.Linq;
using System.Text;
using System.Threading.Tasks;
using Aspose.CAD;
```

## الخطوة 1: تحميل رسم CAD

ابدأ بتحميل رسم CAD في مثيل للفئة Aspose.CAD.Image. تأكد من أن لديك مسار الملف الصحيح لنموذج الرسم الخاص بك.

```csharp
string MyDir = "Your Document Directory";
string sourceFilePath = MyDir + "sample.dwg";

// قم بتحميل رسم CAD في مثيل الصورة
using (var image = Aspose.CAD.Image.Load(sourceFilePath))
{
    // الكود الخاص بك هنا...
}
```

## الخطوة 2: إنشاء BmpOptions

قم بإنشاء مثيل لفئة BmpOptions، المسؤولة عن تحديد الخيارات عند حفظ رسم CAD كملف BMP.

```csharp
Aspose.CAD.ImageOptions.BmpOptions bmpOptions = new Aspose.CAD.ImageOptions.BmpOptions();
```

## الخطوة 3: قم بتعيين خيارات CadRasterization

قم بإنشاء مثيل لفئة CadRasterizationOptions وقم بتكوين خصائصها لتنقيط المتجهات.

```csharp
Aspose.CAD.ImageOptions.CadRasterizationOptions cadRasterizationOptions = new Aspose.CAD.ImageOptions.CadRasterizationOptions();
bmpOptions.VectorRasterizationOptions = cadRasterizationOptions;
```

## الخطوة 4: تعيين خاصية UnitType

قم بتعيين خاصية UnitType لـ CadRasterizationOptions لتحديد نوع الوحدة لتغيير الحجم. في هذا المثال، تم ضبطه على سنتيمتر.

```csharp
cadRasterizationOptions.UnitType = Aspose.CAD.ImageOptions.UnitType.Centimeter;
```

## الخطوة 5: تعيين خاصية التخطيطات

حدد التخطيطات التي تريد تضمينها في الرسم الذي تم تغيير حجمه عن طريق تعيين خاصية التخطيطات.

```csharp
cadRasterizationOptions.Layouts = new string[] { "Model" };
```

## الخطوة 6: التصدير إلى BMP

وأخيرًا، احفظ التخطيط الذي تم تغيير حجمه كملف BMP باستخدام طريقة الحفظ.

```csharp
string outPath = sourceFilePath + ".bmp";
image.Save(outPath, bmpOptions);
```

لقد نجحت الآن في ضبط حجم رسم CAD الخاص بك باستخدام Aspose.CAD لـ .NET!

## خاتمة

في هذا البرنامج التعليمي، تناولنا عملية تغيير حجم رسومات CAD في .NET باستخدام Aspose.CAD. باتباع هذه الخطوات، يمكنك دمج هذه الوظيفة بسلاسة في تطبيقاتك، مما يوفر تجربة مستخدم سلسة.

## الأسئلة الشائعة

### س1: هل يتوافق Aspose.CAD for .NET مع كافة تنسيقات CAD؟

 ج1: يدعم Aspose.CAD for .NET نطاقًا واسعًا من تنسيقات CAD، بما في ذلك DWG وDXF وDWF والمزيد. افحص ال[توثيق](https://reference.aspose.com/cad/net/) للحصول على القائمة الكاملة.

### س2: هل يمكنني تغيير حجم تخطيطات متعددة في وقت واحد؟

ج2: نعم، يمكنك تغيير حجم تخطيطات متعددة عن طريق ضبط صفيف التخطيطات في CadRasterizationOptions.

### س3: أين يمكنني الحصول على دعم Aspose.CAD لـ .NET؟

 ج3: قم بزيارة[منتدى Aspose.CAD](https://forum.aspose.com/c/cad/19) لدعم المجتمع ومساعدته.

### س4: هل هناك نسخة تجريبية مجانية متاحة؟

 ج4: نعم، يمكنك استكشاف أ[تجربة مجانية](https://releases.aspose.com/) لتقييم ميزات Aspose.CAD لـ .NET.

### س5: كيف يمكنني الحصول على ترخيص مؤقت لـ Aspose.CAD لـ .NET؟

 ج5: الحصول على ترخيص مؤقت لأغراض الاختبار[هنا](https://purchase.aspose.com/temporary-license/).
{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}
