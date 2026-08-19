---
date: 2026-03-07
description: تعلم كيفية تصدير ملفات CAD إلى SVG باستخدام Aspose.CAD لـ .NET، وتخصيص
  لون SVG، وتحويل DWG إلى SVG بكفاءة.
linktitle: Exporting CAD Drawings to SVG Format
second_title: Aspose.CAD .NET - CAD and BIM File Format
title: تصدير CAD إلى SVG – تصدير رسومات CAD إلى تنسيق SVG - دليل Aspose.CAD
url: /ar/net/advanced-export-techniques/exporting-cad-drawings-to-svg/
weight: 15
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# تصدير CAD إلى SVG – تصدير رسومات CAD إلى صيغة SVG

## المقدمة

تصدير رسومات CAD إلى SVG هو طلب شائع عندما تحتاج إلى رسومات مستقلة عن الدقة للصفحات الويب، التقارير، أو التصورات التفاعلية. في هذا البرنامج التعليمي ستتعلم **كيفية تصدير CAD إلى SVG** باستخدام Aspose.CAD لـ .NET، وتستكشف خيارات **تخصيص لون SVG**، وترى كيف **تحول DWG إلى SVG** (أو DXF إلى SVG) في بضع أسطر من الشيفرة فقط. الخطوات سريعة، وواجهة برمجة التطبيقات بديهية، وملفات SVG الناتجة تتناسب تمامًا مع أي جهاز.

## إجابات سريعة
- **ما المكتبة التي تتعامل مع التحويل؟** Aspose.CAD لـ .NET.  
- **هل يمكنني تغيير وضع اللون؟** نعم – استخدم `SvgColorMode` لتعيين التدرج الرمادي، الأبيض‑أسود، أو اللون الكامل.  
- **ما صيغ CAD المدعومة؟** DWG، DXF، والعديد غيرها (انظر مستندات Aspose.CAD).  
- **هل أحتاج إلى ترخيص للتطوير؟** ترخيص مؤقت متاح للاختبار.  
- **كم يستغرق التحويل؟** عادةً أقل من ثانية للرسومات القياسية.

## ما هو “تصدير CAD إلى SVG”؟
تصدير CAD إلى SVG يعني أخذ ملف CAD أصلي (مثل DWG أو DXF) وتحويله إلى صيغة Scalable Vector Graphics. SVG مبنية على XML، خفيفة الوزن، ويمكن تنسيقها باستخدام CSS—مما يجعلها مثالية لتطبيقات الويب والهواتف المحمولة الحديثة.

## لماذا نستخدم Aspose.CAD لتصدير CAD إلى SVG؟
- **بدون تبعيات خارجية** – واجهة .NET صافية، لا تحتاج إلى تثبيت AutoCAD.  
- **تحكم دقيق** – يمكنك **تخصيص لون SVG**، تحديد ما إذا كان النص سيبقى كأشكال، واختيار خيارات الرستر.  
- **دعم صيغ واسع** – نفس الشيفرة تعمل لـ **تحويل DWG إلى SVG**، **تحويل DXF إلى SVG**، وصيغ أخرى، مما يبسط قاعدة الشيفرة الخاصة بك.  
- **أداء عالي** – مُحسّن للسرعة واستهلاك الذاكرة المنخفض، مناسب للمعالجة الدفعة.

## المتطلبات المسبقة

قبل البدء، تأكد من وجود ما يلي:

- **Aspose.CAD لـ .NET** مثبت. يمكنك تنزيل المكتبة [هنا](https://releases.aspose.com/cad/net/).  
- بيئة تطوير .NET (Visual Studio، Rider، أو .NET CLI).  
- ملف CAD (DWG أو DXF) ترغب في تحويله.

## استيراد المساحات الاسمية

أولاً، استورد المساحات الاسمية المطلوبة إلى مشروعك لتصبح الفئات متاحة.

```csharp
using Aspose.CAD.ImageOptions;
using System;
using System.Collections.Generic;
using System.Linq;
using System.Text;
```

## دليل خطوة بخطوة

### الخطوة 1: تعيين دليل المستند  
حدد المجلد الذي يتواجد فيه ملف CAD المصدر والمكان الذي سيُحفظ فيه ملف SVG الناتج.

```csharp
// The path to the documents directory.
string MyDir = "Your Document Directory";
```

### الخطوة 2: تحميل رسم CAD  
استخدم `Image.Load` لقراءة ملف DWG (أو DXF). هذا يعمل لسيناريوهات **load DWG .NET**.

```csharp
using (Image image = Image.Load(MyDir + "sample.dwg"))
{
```

### الخطوة 3: تكوين خيارات تصدير SVG  
اضبط إعدادات التصدير لتتناسب مع احتياجاتك. هنا نحدد وضع اللون إلى تدرج رمادي ونفرض أن يتم رسم كل النص كأشكال متجهة.

```csharp
    var options = new SvgOptions();
    options.ColorType = SvgColorMode.Grayscale;   // customize SVG color mode
    options.TextAsShapes = true;                  // ensures text appears as shapes
```

### الخطوة 4: حفظ ملف SVG  
أخيرًا، اكتب ملف SVG إلى القرص. هذه الخطوة **تحفظ CAD كـ SVG** وتكمل عملية التحويل.

```csharp
    image.Save(MyDir + "sample.svg", options);
}
```

باتباع هذه الخطوات الأربعة المختصرة، يمكنك **تحويل DWG إلى SVG** (أو **تحويل DXF إلى SVG**) مع تحكم كامل في مظهر النتيجة.

## المشكلات الشائعة والحلول

| المشكلة | السبب | الحل |
|-------|-------|-----|
| **إخراج SVG فارغ** | مسار الملف المصدر غير صحيح أو الملف تالف. | تحقق من `MyDir` وتأكد من أن ملف CAD يفتح دون أخطاء. |
| **الألوان غير صحيحة** | تم تعيين `SvgColorMode` إلى Grayscale عن غير قصد. | غيّر `options.ColorType` إلى `SvgColorMode.FullColor` للاحتفاظ بالألوان الأصلية. |
| **النص مفقود** | تم تعيين `TextAsShapes` إلى `false` ولا يدعم العارض الخطوط المدمجة. | أبقِ `TextAsShapes = true` أو دمج الخطوط المطلوبة في SVG. |

## الأسئلة المتكررة

### س1: هل Aspose.CAD متوافق مع جميع صيغ CAD؟

ج1: يدعم Aspose.CAD صيغ CAD متعددة، بما في ذلك DWG وDXF، مما يضمن توافقًا واسعًا.

### س2: هل يمكنني تخصيص وضع اللون عند التصدير إلى SVG؟

ج2: نعم، يتيح لك Aspose.CAD اختيار وضع اللون، مما يوفر مرونة في المخرجات.

### س3: هل تتوفر تراخيص مؤقتة لأغراض الاختبار؟

ج3: نعم، يمكنك الحصول على ترخيص مؤقت [هنا](https://purchase.aspose.com/temporary-license/) للتقييم.

### س4: أين يمكنني العثور على وثائق مفصلة لـ Aspose.CAD؟

ج4: الوثائق متاحة [هنا](https://reference.aspose.com/cad/net/).

### س5: كيف يمكنني الحصول على دعم أو طرح أسئلة متعلقة بـ Aspose.CAD؟

ج5: زر منتدى المجتمع [هنا](https://forum.aspose.com/c/cad/19) للحصول على الدعم والنقاشات.

## أسئلة شائعة أخرى

**س: هل يمكن استخدام هذا الكود مع .NET Core أو .NET 6؟**  
ج: بالتأكيد. Aspose.CAD لـ .NET متوافق مع .NET Framework، .NET Core، و .NET 5/6+.

**س: هل يمكن تصدير تخطيط أو طبقة محددة فقط؟**  
ج: نعم. استخدم `SvgOptions` لتعيين `PageIndex` أو تصفية الطبقات قبل الحفظ.

**س: كيف يمكنني تضمين أنماط CSS مخصصة في SVG المُولد؟**  
ج: بعد الحفظ، يمكنك معالجة XML الخاص بـ SVG لإدخال عناصر `<style>`، أو استخدم `options.CustomCss` إذا كان متاحًا في الإصدارات الأحدث.

**س: ما حدود حجم ملف CAD المصدر؟**  
ج: المكتبة تتعامل مع ملفات كبيرة، لكن استهلاك الذاكرة يزداد مع تعقيد الرسم. للرسومات الضخمة جدًا، يُفضَّل معالجة الصفحات بشكل منفصل.

**س: هل يحافظ التحويل على وزن الخطوط وأنواع الخطوط؟**  
ج: بشكل افتراضي، يتم الحفاظ على وزن الخطوط. يمكنك تعديل خيارات العرض في `SvgOptions` للحصول على تحكم أدق.

---

**آخر تحديث:** 2026-03-07  
**تم الاختبار مع:** Aspose.CAD لـ .NET 24.12  
**المؤلف:** Aspose  

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}