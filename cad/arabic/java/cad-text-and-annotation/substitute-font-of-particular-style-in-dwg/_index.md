---
date: 2026-03-07
description: تعلم كيفية استبدال الخط في ملفات DWG باستخدام Aspose.CAD للغة Java. يوضح
  هذا الدليل خطوة بخطوة **كيفية استبدال الخط** لنمط معين بدقة.
linktitle: Substitute Font of a Particular Style in DWG
second_title: Aspose.CAD Java API
title: كيفية استبدال خط نمط معين في DWG باستخدام Aspose.CAD للـ Java
url: /ar/java/cad-text-and-annotation/substitute-font-of-particular-style-in-dwg/
weight: 12
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# كيفية استبدال الخط لنمط معين في DWG باستخدام Aspose.CAD للـ Java

## مقدمة

في عالم الـ CAD (التصميم بمساعدة الحاسوب)، الدقة والتفاصيل أمران أساسيان، و**معرفة كيفية استبدال الخط** في الرسم يمكن أن توفر لك ساعات لا تحصى من إعادة العمل. توفر Aspose.CAD للـ Java للمطورين طريقة برمجية نظيفة لتعديل ملفات DWG، بما في ذلك القدرة على تغيير خط نمط نص معين. في هذا الدرس سنستعرض الخطوات الدقيقة لاستبدال خط نمط معين في ملف DWG، نشرح لماذا قد ترغب في ذلك، ونظهر لك كيفية التحقق من النتيجة.

## إجابات سريعة

- **What does “replace font” mean in a DWG?** تغيير الخط الأساسي المرتبط بتعريف نمط النص.  
- **Which library handles this?** Aspose.CAD للـ Java.  
- **Do I need a license?** النسخة التجريبية المجانية تعمل للاختبار؛ يلزم الحصول على ترخيص تجاري للإنتاج.  
- **Can I change multiple styles at once?** نعم – يمكن التكرار على مجموعة الأنماط وتعيين الخط لكل منها.  
- **Is the code compatible with Java 8+?** بالتأكيد، الـ API تستهدف Java 8 وما بعدها.

## ما هو استبدال الخط في DWG؟

## لماذا تعديل نمط نص DWG؟

- **Maintain brand consistency:** استخدم الخطوط المؤسسية في جميع الرسومات.  
- **Fix missing fonts:** استبدل الخطوط غير المتوفرة بأخرى مثبتة على النظام المستهدف.  
- **Prepare for printing/plotting:** بعض الطابعات تتطلب خطوطًا محددة للحصول على مخرجات دقيقة.

## المتطلبات المسبقة

قبل أن تبدأ هذا الدرس، تأكد من إعداد ما يلي:

1. **Aspose.CAD for Java Library:** قم بتنزيل وتثبيت مكتبة Aspose.CAD. يمكنك العثور على المكتبة ووثائقها [هنا](https://releases.aspose.com/cad/java/).

2. **Java Development Kit (JDK):** تأكد من تثبيت Java على جهازك.

الآن بعد أن لديك الأدوات اللازمة، دعنا ننتقل إلى القسم التالي.

## استيراد المساحات الاسمية (مطلوب لتعديل نمط نص DWG)

في Java، استيراد المساحات الاسمية الصحيحة أمر حاسم لاستخدام المكتبات الخارجية. في هذه الحالة، تأكد من استيراد مساحات أسماء Aspose.CAD اللازمة. إليك كيفية القيام بذلك:

```java
import com.aspose.cad.Image;

import com.aspose.cad.fileformats.cad.CadImage;
```

## الخطوة 1: تعيين دليل الموارد

استبدل `"Your Document Directory"` بالمسار إلى دليل المستندات الفعلي الخاص بك.

```java
// The path to the resource directory.
String dataDir = "Your Document Directory" + "CADConversion/";
```

## الخطوة 2: تحميل رسم CAD

تأكد من استبدال `"conic_pyramid.dxf"` بالاسم الفعلي لرسم CAD الخاص بك.

```java
String srcFile = dataDir + "conic_pyramid.dxf";

// Load a CAD drawing in an instance of CadImage
CadImage cadImage = (CadImage)Image.load(srcFile);
```

## الخطوة 3: تحديد الخط لنمط (تغيير خط نمط DWG)

قم بتعديل اسم الخط ("Arial" في هذا المثال) وفقًا لمتطلباتك. هذه السطر **يحدد الخط الأساسي لنمط DWG**، مما يستبدل الخط القديم فعليًا.

```java
// Specify the font for one particular style
((CadStyleTableObject)cadImage.getStyles().get_Item(0)).setPrimaryFontName("Arial");
```

## المشكلات الشائعة والحلول

| المشكلة | السبب | الحل |
|-------|-------|----------|
| الخط لا يتغير بعد الحفظ | لم يتم حفظ الرسم بعد التعديل | استدعِ `cadImage.save(outputPath);` بعد تعيين الخط. |
| اسم الخط غير معترف به | الخط غير مثبت على النظام الذي يُشغل الكود | قم بتثبيت الخط أو استخدم اسم خط عام (مثال: "Tahoma"). |
| `ClassCastException` | نوع كائن غير صحيح من `get_Item` | تأكد من أن الفهرس يشير إلى `CadStyleTableObject`. |

## الأسئلة المتكررة

### Q1: هل يمكنني استبدال خطوط متعددة في ملف DWG واحد؟

نعم، يمكنك التكرار عبر الأنماط المختلفة وتعيين الخط الأساسي لكل نمط على حدة.

### Q2: هل هناك حد لأسماء الخطوط التي يمكنني استخدامها؟

لا، يمكنك استخدام أي اسم خط صالح متوفر على نظامك.

### Q3: هل يمكنني التراجع عن استبدال الخطوط؟

توفر Aspose.CAD مرونة؛ يمكنك إرجاع التغييرات أو حفظ إصدارات مختلفة من ملف DWG.

### Q4: هل ينطبق هذا الدرس على صيغ CAD أخرى؟

على الرغم من تركيز المثال على DWG، يمكن تطبيق مبادئ مماثلة على صيغ CAD الأخرى المدعومة.

### Q5: كيف يمكنني الحصول على دعم Aspose.CAD للـ Java؟

قم بزيارة [منتدى Aspose.CAD](https://forum.aspose.com/c/cad/19) للحصول على دعم المجتمع والنقاشات.

## أسئلة متكررة إضافية

**س: كيف أحفظ الرسم المعدل؟**  
ج: بعد تعيين الخط الجديد، استدعِ `cadImage.save(dataDir + "output.dwg");` لكتابة التغييرات إلى ملف جديد.

**س: هل يمكنني استبدال خط كائنات التعليق فقط؟**  
ج: نعم، قم بفلترة مجموعة الأنماط للأنماط المتعلقة بالتعليقات قبل تطبيق `setPrimaryFontName`.

**س: هل يمكن معاينة تغيير الخط دون حفظ؟**  
ج: يمكنك تصيير الصورة إلى bitmap باستخدام `cadImage.save(outputStream, new ImageOptions());` لمعاينة في الذاكرة.

**س: هل يدعم Aspose.CAD خطوط TrueType و OpenType؟**  
ج: كلا من خطوط TrueType (.ttf) و OpenType (.otf) مدعومة بالكامل طالما أنها مثبتة على نظام التشغيل المضيف.

## الأسئلة المتكررة

**س: ما هو إصدار Aspose.CAD المطلوب لهذا الكود؟**  
ج: الـ API المستخدم في هذا الدرس متوفر في Aspose.CAD للـ Java 24.11 وما بعده.

**س: هل يمكن تشغيل هذا الكود على خادم Linux؟**  
ج: نعم، طالما تم تثبيت الخطوط المطلوبة على الخادم وتتوفر Java 8+.

**س: كيف يمكنني سرد جميع أنماط النص المتاحة قبل تغيير الخط؟**  
ج: قم بالتكرار على `cadImage.getStyles()` واطبع اسم كل نمط والخط الأساسي الحالي.

**س: هل هناك طريقة لمعالجة دفعة من ملفات DWG؟**  
ج: ضع المنطق داخل حلقة تقوم بتحميل كل ملف، وتحديث النمط المطلوب، وحفظ النتيجة.

**س: هل سيؤثر تغيير الخط الأساسي على الأبعاد أو التباعد؟**  
ج: قد تختلف مقاييس الخط، لذا قد تحتاج إلى تعديل ارتفاع النص أو موضعه بعد التغيير.

## الخلاصة

يفتح Aspose.CAD للـ Java إمكانيات قوية لمعالجة CAD، و**كيفية استبدال الخط** هي مجرد واحدة من قدراته المتعددة. جرّب أنماطًا مختلفة، واستخدم الكلمات المفتاحية الثانوية مثل *modify DWG text style* أو *set primary font dwg* لضبط رسوماتك بدقة، ودمج الكود في خطوط أتمتة أكبر لمعالجة دفعات.

---

**آخر تحديث:** 2026-03-07  
**تم الاختبار مع:** Aspose.CAD للـ Java 24.11  
**المؤلف:** Aspose  

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}