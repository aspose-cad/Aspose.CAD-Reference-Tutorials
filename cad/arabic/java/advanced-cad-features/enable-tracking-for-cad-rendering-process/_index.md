---
date: 2026-02-12
description: تعرّف على كيفية ضبط حجم صفحة PDF أثناء تحويل CAD إلى PDF باستخدام Aspose.CAD
  للغة Java. اتبع هذا الدليل خطوة بخطوة لتمكين التتبع، وتحويل CAD إلى PDF، وحفظ CAD
  كملف PDF بكفاءة.
linktitle: Set PDF Page Size – Enable Tracking for CAD Rendering
second_title: Aspose.CAD Java API
title: كيفية ضبط حجم صفحة PDF وتمكين التتبع لعملية تصيير CAD
url: /ar/java/advanced-cad-features/enable-tracking-for-cad-rendering-process/
weight: 10
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# تمكين التتبع لعملية تصيير CAD

## مقدمة

في هذا الدرس ستتعلم كيفية **تحديد حجم صفحة PDF** أثناء **تحويل CAD إلى PDF** باستخدام **Aspose.CAD for Java**. من خلال تمكين التتبع ستحصل على رؤية كاملة على خط أنابيب التصيير، مما يسهل تصحيح الأخطاء وتحسين عملية التحويل من ملفات CAD (مثل DXF) إلى PDF. سواء كنت بحاجة إلى **حفظ CAD كـ PDF**، أو إنشاء PDF من DXF، أو ببساطة التحكم في أبعاد الإخراج، فإن الخطوات أدناه ستقودك عبر العملية بالكامل.

## إجابات سريعة
- **ماذا يفعل “تحديد حجم صفحة PDF”؟** يحدد عرض وارتفاع صفحة PDF الناتجة أثناء تصيير CAD.  
- **لماذا يتم تمكين التتبع؟** يسجل التتبع كل مرحلة من مراحل التحويل، مما يساعدك على اكتشاف عنق الزجاجة أو الأخطاء.  
- **هل أحتاج إلى ترخيص؟** نسخة تجريبية مجانية تكفي للتقييم؛ الترخيص التجاري مطلوب للإنتاج.  
- **ما هي صيغ CAD المدعومة؟** DWG، DXF، DGN، والعديد غيرها – راجع وثائق Aspose.CAD للقائمة الكاملة.  
- **هل يمكنني تغيير أبعاد الصفحة أثناء التشغيل؟** نعم – فقط عدل قيم `PageWidth` و `PageHeight` في `CadRasterizationOptions`.

## ما هو “تحديد حجم صفحة PDF” في تصيير CAD؟

تحديد حجم صفحة PDF يخبر أداة الرستر كيف يكون حجم القماش عندما يتم تحويل بيانات CAD المتجهة إلى صفحة PDF. هذا أمر حاسم للحفاظ على الدقة البصرية، خاصةً عند التعامل مع رسومات هندسية مفصلة.

## لماذا تمكين التتبع لتصير CAD؟

يقدم تمكين التتبع سجلًا مفصلاً لكل خطوة—من تحميل الملف المصدر إلى كتابة مخرجات PDF. يساعدك ذلك على:

- تشخيص سبب ظهور رسم معين بصورة غير صحيحة.  
- قياس الوقت المستغرق لكل مرحلة، وهو مفيد لضبط الأداء.  
- التحقق من أن حجم الصفحة الذي قمت بتكوينه تم تطبيقه فعليًا.

## المتطلبات المسبقة

قبل الخوض في إعداد التتبع، تأكد من توفر المتطلبات التالية:

1. **بيئة تطوير Java** – Java 8 أو أحدث مثبتة على جهازك.  
2. **مكتبة Aspose.CAD** – قم بتحميل ودمج مكتبة Aspose.CAD في مشروع Java الخاص بك. يمكنك العثور على رابط التحميل [هنا](https://releases.aspose.com/cad/java/).  
3. **دليل المستندات** – جهّز دليلًا لتخزين ملفات CAD وملفات PDF المُولدة.

## استيراد المساحات الاسمية

في مشروع Java الخاص بك، استورد المساحات الاسمية اللازمة للاستفادة من وظائف Aspose.CAD. أضف الأسطر التالية في بداية الكود:

```java
import java.io.FileNotFoundException;
import java.io.FileOutputStream;
import java.io.OutputStream;

import com.aspose.cad.Image;

import com.aspose.cad.imageoptions.CadRasterizationOptions;
import com.aspose.cad.imageoptions.PdfOptions;
```

## تعيين مسار دليل الموارد

```java
String dataDir = "Your Document Directory" + "CADConversion/";
```

استبدل `"Your Document Directory"` بالمسار الفعلي لدليل المستندات الخاص بك.

## تحميل ملف CAD

```java
String srcFile = dataDir + "conic_pyramid.dxf";
Image image = Image.load(srcFile);
```

حدد المسار إلى ملف CAD الخاص بك، مع التأكد من أنه داخل دليل المستندات المحدد.

## تعيين خيارات إخراج PDF

```java
OutputStream stream = new FileOutputStream(dataDir + "conic_pyramid.pdf");
PdfOptions pdfOptions = new PdfOptions();
```

أنشئ تدفق إخراج واضبط خيارات PDF للتحويل.

## تكوين CadRasterizationOptions (تحديد حجم صفحة PDF)

```java
CadRasterizationOptions cadRasterizationOptions = new CadRasterizationOptions();
pdfOptions.setVectorRasterizationOptions(cadRasterizationOptions);
cadRasterizationOptions.setPageWidth(800);
cadRasterizationOptions.setPageHeight(600);
```

هنا نقوم **بتحديد حجم صفحة PDF** عن طريق تعريف `PageWidth` و `PageHeight`. عدل هذه القيم لتتناسب مع الأبعاد المطلوبة لرسمك الهندسي. هذه هي الخطوة الأساسية التي تجيب على **كيفية تحديد حجم PDF** عندما **java cad to pdf**.

## حفظ ملف PDF

```java
image.save(stream, pdfOptions);
```

احفظ ملف PDF المصور باستخدام الخيارات المحددة.

## التحقق من تمكين التتبع

```java
System.out.println("Tracking enabled successfully for CAD rendering process.");
```

تأكد من أن التتبع تم تمكينه بنجاح لعملية تصيير CAD.

## المشكلات الشائعة & استكشاف الأخطاء

| العَرَض | السبب المحتمل | الحل |
|---------|--------------|-----|
| تظهر صفحة PDF فارغة | `PageWidth`/`PageHeight` مُعينة إلى 0 | تأكد من توفير أبعاد غير صفرية. |
| ملف الإخراج تالف | تدفق الإخراج غير مغلق | استدعِ `stream.close()` بعد `image.save(...)`. |
| طبقات مفقودة في PDF | ملف CAD يستخدم كيانات غير مدعومة | تحقق من أن صيغة الملف مدعومة بالكامل من قبل Aspose.CAD. |

## الأسئلة المتكررة

### س1: هل Aspose.CAD متوافق مع جميع صيغ ملفات CAD؟

ج1: يدعم Aspose.CAD مجموعة واسعة من صيغ CAD، بما في ذلك DWG، DXF، DGN، وأكثر. راجع [الوثائق](https://reference.aspose.com/cad/java/) للقائمة الشاملة.

### س2: هل يمكنني تخصيص أبعاد إخراج ملف PDF؟

ج2: بالتأكيد! عدل معلمات `PageWidth` و `PageHeight` في `CadRasterizationOptions` لتلائم أبعاد الإخراج المطلوبة.

### س3: هل هناك نسخة تجريبية مجانية متاحة لـ Aspose.CAD for Java؟

ج3: نعم، يمكنك استكشاف قدرات Aspose.CAD بالحصول على نسخة تجريبية مجانية [هنا](https://releases.aspose.com/).

### س4: كيف يمكنني الحصول على دعم المجتمع لأسئلة تتعلق بـ Aspose.CAD؟

ج4: زر [منتدى Aspose.CAD](https://forum.aspose.com/c/cad/19) للتفاعل مع المجتمع وطلب المساعدة.

### س5: هل تتوفر تراخيص مؤقتة لـ Aspose.CAD؟

ج5: نعم، إذا كنت بحاجة إلى ترخيص مؤقت، يمكنك الحصول عليه [هنا](https://purchase.aspose.com/temporary-license/).

## الخاتمة

تهانينا! لقد تعلمت الآن كيفية **تحديد حجم صفحة PDF** وتمكين التتبع لتصير CAD باستخدام **Aspose.CAD for Java**. يزودك هذا الدليل بالقدرة على **تحويل CAD إلى PDF**، **حفظ CAD كـ PDF**، وإنشاء PDF من DXF مع تحكم كامل في أبعاد الصفحة وسجلات تنفيذ مفصلة. لا تتردد في تجربة أحجام صفحات مختلفة واستكشاف خيارات الرستر الإضافية لتناسب سير عملك الهندسي المحدد.

---

**آخر تحديث:** 2026-02-12  
**تم الاختبار مع:** Aspose.CAD for Java 24.12 (أحدث نسخة وقت الكتابة)  
**المؤلف:** Aspose  

---

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}