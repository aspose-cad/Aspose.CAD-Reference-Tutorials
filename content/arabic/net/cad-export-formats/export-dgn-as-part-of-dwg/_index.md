---
title: قم بتصدير DGN كجزء من DWG في Aspose.CAD لـ .NET
linktitle: تصدير DGN كجزء من DWG
second_title: Aspose.CAD .NET - تنسيق ملف CAD وBIM
description: تعرف على كيفية تصدير DGN كجزء من DWG في Aspose.CAD لـ .NET. اتبع دليلنا خطوة بخطوة للتكامل السلس.
type: docs
weight: 11
url: /ar/net/cad-export-formats/export-dgn-as-part-of-dwg/
---
## مقدمة

في عالم تطوير .NET، يبرز Aspose.CAD كمكتبة قوية للعمل مع ملفات التصميم بمساعدة الكمبيوتر (CAD). سيرشدك هذا البرنامج التعليمي خلال عملية تصدير ملف DGN (التصميم) كجزء من ملف DWG (الرسم) باستخدام Aspose.CAD لـ .NET. سواء كنت مطورًا متمرسًا أو بدأت للتو، سيساعدك هذا الدليل التفصيلي خطوة بخطوة على تسخير إمكانات Aspose.CAD لتحقيق هذه المهمة المحددة بكفاءة.

## المتطلبات الأساسية

قبل الغوص في البرنامج التعليمي، تأكد من توفر المتطلبات الأساسية التالية:

-  Aspose.CAD لـ .NET: تأكد من تثبيت مكتبة Aspose.CAD لـ .NET. يمكنك تنزيله[هنا](https://releases.aspose.com/cad/net/).

- بيئة التطوير: قم بإعداد بيئة تطوير .NET المفضلة لديك، مثل Visual Studio.

- المعرفة الأساسية بـ C#: تعرف على لغة البرمجة C#.

## استيراد مساحات الأسماء

في مشروع C# الخاص بك، قم بتضمين مساحات الأسماء الضرورية للوصول إلى وظيفة Aspose.CAD. أضف ما يلي باستخدام التوجيهات في بداية ملف التعليمات البرمجية الخاص بك:

```csharp
using System;
using System.Collections.Generic;
using System.Linq;
using System.Text;
using System.Threading.Tasks;
using Aspose.CAD;
```

الآن، دعونا نقسم الكود المقدم إلى خطوات متعددة:

## الخطوة 1: تحديد مسارات الملفات

```csharp
//مسارات ملفات الإدخال والإخراج
string fileName = "BlockRefDgn.dwg";
string outPath = fileName + ".pdf";
```

## الخطوة 2: إنشاء مثيل PdfOptions

```csharp
// قم بإنشاء مثيل لفئة PdfOptions لتصدير DWG إلى PDF
PdfOptions exportOptions = new PdfOptions();
```

## الخطوة 3: تحميل ملف DWG

```csharp
// قم بتحميل ملف DWG الموجود كصورة وقم بتحويله إلى نوع CadImage
using (CadImage cadImage = (CadImage)Image.Load(fileName))
```

## الخطوة 4: التكرار من خلال الكيانات

```csharp
// قم بالتكرار عبر كل كيان داخل ملف DWG
foreach (CadBaseEntity baseEntity in cadImage.Entities)
```

## الخطوة 5: التحقق من نوع الكيان

```csharp
// تحقق مما إذا كان الكيان عبارة عن تعريف صورة
if (baseEntity.TypeName == CadEntityTypeName.DGNUNDERLAY)
```

## الخطوة 6: الحصول على المسار الأساسي

```csharp
// إذا كان تعريفًا للصورة، فاحصل على المرجع الخارجي للكائن
CadDgnUnderlay dgnFile = (CadDgnUnderlay)baseEntity;
Console.WriteLine(dgnFile.UnderlayPath);
```

## الخطوة 7: تحديد خيارات التنقيط

```csharp
// تحديد الإعدادات لكائن CadRasterizationOptions
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

## الخطوة 8: تصدير DWG إلى PDF

```csharp
// قم بتصدير DWG إلى PDF عن طريق استدعاء طريقة الحفظ
cadImage.Save(outPath, exportOptions);
```

## خاتمة

تهانينا! لقد أكملت بنجاح عملية تصدير ملف DGN كجزء من ملف DWG باستخدام Aspose.CAD لـ .NET. لقد زودك هذا البرنامج التعليمي بالخطوات الأساسية ومقتطفات التعليمات البرمجية لتحقيق هذه المهمة المحددة بسلاسة.

## الأسئلة الشائعة

### س1: هل يمكنني استخدام Aspose.CAD لـ .NET في مشاريعي التجارية؟
 ج1: نعم يمكنك ذلك. يزور[هنا](https://purchase.aspose.com/buy) لاستكشاف خيارات الترخيص.

### س2: هل هناك أي قيود على حجم ملفات DWG التي يمكنني معالجتها؟
ج2: يدعم Aspose.CAD معالجة ملفات DWG الكبيرة، ولكن قد يتم تطبيق قيود على الأجهزة.

### س3: هل هناك نسخة تجريبية متاحة؟
 ج3: نعم، يمكنك الحصول على نسخة تجريبية مجانية[هنا](https://releases.aspose.com/).

### س4: كيف يمكنني الحصول على تراخيص مؤقتة؟
 ج4: يمكن الحصول على تراخيص مؤقتة[هنا](https://purchase.aspose.com/temporary-license/).

### س5: أين يمكنني طلب المساعدة إذا واجهت مشكلات؟
 ج5: يمكنك زيارة منتدى Aspose.CAD[هنا](https://forum.aspose.com/c/cad/19) للدعم.