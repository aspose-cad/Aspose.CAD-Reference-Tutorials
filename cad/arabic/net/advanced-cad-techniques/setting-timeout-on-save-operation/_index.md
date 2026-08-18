---
date: 2026-03-05
description: تعلم كيفية تعيين مهلة لعمليات الحفظ أثناء تحويل ملفات DWG إلى PDF باستخدام
  Aspose.CAD لـ .NET. عزّز الكفاءة والتحكم في تطبيقات .NET الخاصة بك.
linktitle: Setting Timeout on Save Operation
second_title: Aspose.CAD .NET - CAD and BIM File Format
title: كيفية تعيين مهلة لعملية الحفظ - دليل Aspose.CAD
url: /ar/net/advanced-cad-techniques/setting-timeout-on-save-operation/
weight: 12
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# كيفية تعيين مهلة لعملية الحفظ - دليل Aspose.CAD

## المقدمة

في هذا الدليل، ستتعلم **كيفية تعيين مهلة** على عمليات حفظ CAD، وهي تقنية تساعدك على منع التحويلات طويلة الأمد من التحول إلى عمليات غير مستجيبة. إدارة المهلة مفيدة بشكل خاص عندما **تحول DWG إلى PDF** أو **تصدير CAD PDF** في وظائف الدُفعات أو خدمات الويب. توفر Aspose.CAD for .NET واجهة برمجة تطبيقات نظيفة تتيح لك التحكم في عملية الحفظ مع الاستفادة من محرك الرستر القوي الخاص بها.

## إجابات سريعة
- **ماذا تتحكم فيه المهلة؟** تُلغي عملية الحفظ/التصدير إذا استغرقت وقتًا أطول من الفترة المحددة.  
- **أي الصيغ تستفيد أكثر؟** تحويل ملفات DWG الكبيرة إلى PDF أو صور رستر حيث قد يختلف وقت المعالجة.  
- **هل أحتاج إلى ترخيص؟** يلزم وجود ترخيص Aspose.CAD صالح للاستخدام في الإنتاج؛ نسخة تجريبية مجانية تكفي للتقييم.  
- **هل يمكنني تخصيص المدة؟** نعم—ما عليك سوى تغيير قيمة `Thread.Sleep` (بالمللي ثانية) لتناسب سيناريوك.  
- **هل هذا النهج متوافق مع البرمجة غير المتزامنة؟** يستخدم المثال `Task.Factory.StartNew`، مما يسهل دمجه في تدفقات العمل غير المتزامنة.

## ما معنى “كيفية تعيين مهلة” في سياق حفظ CAD؟
تعيين مهلة يعني إرفاق `InterruptionToken` بخيارات الحفظ وتفعيل مقاطعة بعد فترة محددة مسبقًا. هذا يمنع العملية من التعليق إلى ما لا نهاية، مما يمنحك أداءً متوقعًا وإدارة موارد أفضل.

## لماذا نستخدم Aspose.CAD لتحويل DWG إلى PDF مع مهلة؟
- **الموثوقية:** يضمن أن التحويل المتجاوز لن يعطل خدمتك.  
- **القابلية للتوسع:** يتيح لك معالجة العديد من الملفات بالتوازي دون الخوف من توقف ملف واحد يعرقل خط الأنابيب.  
- **الجودة:** يحافظ على دقة الرستر العالية لـ Aspose.CAD مع إضافة ضوابط أمان.

## المتطلبات المسبقة

قبل أن نبدأ، تأكد من وجود ما يلي:

- **Aspose.CAD for .NET** – مدمج في مشروعك. يمكنك تنزيله [هنا](https://releases.aspose.com/cad/net/).
- **دليل المستندات** – مجلد يحتوي على ملفات DWG المصدرية وملفات PDF الناتجة.

## استيراد المساحات الاسمية

أولاً، استورد المساحات الاسمية التي توفر الفئات التي سنحتاجها للرستر، خيارات PDF، وآلية المقاطعة.

```csharp
using Aspose.CAD.ImageOptions;
using System;
using System.Threading;
using System.Threading.Tasks;
```

## كيفية تعيين مهلة لعملية الحفظ

فيما يلي شرح خطوة بخطوة. كل خطوة تتضمن شرحًا موجزًا يليه كتلة الكود الأصلية (دون تغيير).

### الخطوة 1: تحميل رسم CAD

نحمّل ملف DWG المصدر من الدليل المحدد. تُعيد طريقة `Image.Load` كائن `Image` يمثل رسم CAD.

```csharp
// Example: Loading CAD Drawing
string SourceDir = "Your Document Directory";
string OutputDir = "Your Document Directory";

using (Image cadDrawing = Image.Load(SourceDir + "Drawing11.dwg"))
{
    // Code for subsequent steps will be placed here
}
```

### الخطوة 2: تكوين خيارات الرستر

حدد خيارات الرستر بحيث يتطابق PDF المُصدّر مع أبعاد الرسم الأصلي. هنا يمكنك التحكم في عرض الصفحة، ارتفاعها، وإعدادات العرض الأخرى.

```csharp
// Example: Configuring Rasterization Options
var rasterizationOptions = new CadRasterizationOptions();
rasterizationOptions.PageWidth = cadDrawing.Size.Width;
rasterizationOptions.PageHeight = cadDrawing.Size.Height;
```

### الخطوة 3: إنشاء خيارات PDF (تصدير CAD PDF)

أنشئ مثيلًا من `PdfOptions` وأرفق إعدادات الرستر. سيتم تمرير هذا الكائن إلى طريقة `Save` لإنشاء نسخة PDF من ملف DWG.

```csharp
// Example: Creating PDF Options
PdfOptions CADf = new PdfOptions();
CADf.VectorRasterizationOptions = rasterizationOptions;
```

### الخطوة 4: تنفيذ آلية المهلة

نستخدم `InterruptionTokenSource` للحصول على رمز يمكنه مقاطعة عملية الحفظ. تقوم مهمة خلفية بأداء التصدير، بينما ينام الخيط الرئيسي لمدة المهلة المطلوبة (مثلاً 10 ثوانٍ). بعد النوم، نستدعي `Interrupt()` لإلغاء العملية إذا كانت لا تزال تعمل.

```csharp
// Example: Implementing Timeout Mechanism
using (var its = new InterruptionTokenSource())
{
    CADf.InterruptionToken = its.Token;

    var exportTask = Task.Factory.StartNew(() =>
    {
        cadDrawing.Save(OutputDir + "PutTimeoutOnSave_out.pdf", CADf);
    });

    Thread.Sleep(10000); // Set your desired timeout duration in milliseconds
    its.Interrupt();

    exportTask.Wait();
}
```

### الخطوة 5: الإنهاء والتأكيد

بعد التصدير (أو المقاطعة)، نكتب رسالة تأكيد إلى وحدة التحكم. في تطبيق حقيقي قد تقوم بتسجيل النتيجة أو رفع حدث.

```csharp
// Example: Finalizing and Confirming
Console.WriteLine("PutTimeoutOnSave executed successfully");
```

## المشكلات الشائعة والحلول

| المشكلة | السبب | الحل |
|-------|-------|--------|
| التصدير يتعطل إلى ما لا نهاية | عدم إرفاق رمز المقاطعة | تأكد من ضبط `CADf.InterruptionToken = its.Token;` قبل بدء المهمة. |
| ملف PDF فارغ أو معطوب | مسار دليل الإخراج غير صحيح | تحقق من أن `OutputDir` ينتهي بفاصل مسار وأن اسم الملف صالح. |
| المهلة قصيرة جدًا، مما يسبب إلغاءًا مبكرًا | قيمة `Thread.Sleep` منخفضة بالنسبة للملفات الكبيرة | زد مدة النوم أو احسب مهلة تكيفية بناءً على حجم الملف. |

## الأسئلة المتكررة

**س1: هل يمكنني تخصيص مدة المهلة؟**  
ج: بالتأكيد. غيّر القيمة الممررة إلى `Thread.Sleep` (بالمللي ثانية) لتتناسب مع توقعات الأداء لديك.

**س2: هل هناك خيارات أخرى للرستر؟**  
ج: نعم. توفر `CadRasterizationOptions` خصائص مثل `Resolution`، `BackgroundColor`، و`DrawType` لضبط مخرجات PDF بدقة.

**س3: كيف يمكنني التعامل مع المقاطعات في تطبيقي؟**  
ج: استخدم فئتي `InterruptionToken` و`InterruptionTokenSource` كما هو موضح. توفران طريقة آمنة عبر الخيوط لإلغاء العمليات طويلة الأمد.

**س4: هل Aspose.CAD مناسب لكل من ملفات CAD الثنائية والثلاثية الأبعاد؟**  
ج: تدعم مجموعة واسعة من الصيغ الثنائية والثلاثية الأبعاد، بما في ذلك DWG، DXF، DGN، وغيرها.

**س5: أين يمكنني العثور على مزيد من المساعدة أو الدعم المجتمعي؟**  
ج: زر [منتدى Aspose.CAD](https://forum.aspose.com/c/cad/19) للمناقشات المجتمعية، عينات الكود، ونصائح استكشاف الأخطاء.

## الخاتمة

باتباع الخطوات أعلاه، أصبحت الآن تعرف **كيفية تعيين مهلة** على عمليات حفظ CAD، مما يتيح لك تحويل **DWG إلى PDF** أو **تصدير CAD PDF** بثقة دون خطر حدوث عمليات غير مستجيبة. دمج هذا النمط في محولات الدُفعات، خدمات الويب، أو أي خط أنابيب آلي حيث التنبؤ مهم.

---

**آخر تحديث:** 2026-03-05  
**تم الاختبار مع:** Aspose.CAD 24.12 for .NET  
**المؤلف:** Aspose  

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}