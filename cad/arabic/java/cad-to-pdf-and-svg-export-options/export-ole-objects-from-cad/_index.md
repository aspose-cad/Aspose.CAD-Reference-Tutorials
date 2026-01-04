---
date: 2026-01-04
description: تعلم كيفية **حفظ CAD بصيغة PNG** وتصدير كائنات OLE بسهولة من ملفات CAD
  باستخدام Aspose.CAD للـ Java. إعداد سريع، عينة كود كاملة، ونصائح لأفضل الممارسات.
linktitle: Export OLE Objects from CAD
second_title: Aspose.CAD Java API
title: حفظ ملفات CAD كـ PNG وتصدير كائنات OLE باستخدام Aspose.CAD للغة Java
url: /ar/java/cad-to-pdf-and-svg-export-options/export-ole-objects-from-cad/
weight: 10
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# حفظ ملفات CAD بصيغة PNG وتصدير كائنات OLE باستخدام Aspose.CAD للـ Java

## المقدمة

في عالم التصميم بمساعدة الحاسوب (CAD) سريع التطور، القدرة على **حفظ CAD بصيغة PNG** مع استخراج كائنات OLE (الربط والتضمين) المدمجة يمكن أن تُسهل سير العمل بشكل كبير. سواء كنت تبني أداة تحويل دفعي، أو تُنشئ صورًا مصغرة لبُوابة ويب، أو تحتاج ببساطة إلى أرشفة محتوى OLE، فإن Aspose.CAD للـ Java يوفّر لك طريقة برمجية نظيفة للقيام بذلك. في هذا الدرس سنستعرض العملية بالكامل، من إعداد المشروع إلى تصدير كل كائن OLE كصورة PNG.

## إجابات سريعة
- **هل يمكن تصدير كائنات OLE مباشرة إلى PNG؟** نعم – Aspose.CAD يحمل ملف CAD ويسمح لك بتحويل كل تخطيط إلى PNG.  
- **ما نسخة Java المطلوبة؟** Java 8 أو أحدث.  
- **هل أحتاج إلى ترخيص لهذه الميزة؟** النسخة التجريبية المجانية تكفي للتقييم؛ الترخيص مطلوب للإنتاج.  
- **هل سيتم الحفاظ على البيانات المتجهية؟** التحويل إلى PNG يحافظ على المظهر البصري، لكن الناتج يكون صورة نقطية، وليس متجهية.  
- **هل يدعم المعالجة الدفعية؟** بالتأكيد – يمكنك التكرار على مجموعة من الملفات كما هو موضح في مثال الكود.

## المتطلبات المسبقة

قبل البدء، تأكد من توفر ما يلي:

- **مجموعة تطوير جافا (JDK)** – Java 8+ مثبتة ومُعَدّة.  
- **Aspose.CAD للـ Java** – حمّل أحدث مكتبة من [رابط التحميل](https://releases.aspose.com/cad/java/).  
- **ملفات CAD المصدرية** – أي ملفات DWG/DXF/DGN تحتوي على كائنات OLE تريد تصديرها.

## استيراد المساحات الاسمية

للعمل مع ملفات CAD تحتاج إلى استيراد الفئات الأساسية من Aspose.CAD. احتفظ بكتلة الاستيراد كما هي بالضبط – فهي توفر الفئات المستخدمة لاحقًا في الدرس.

```java
import com.aspose.cad.Image;

import com.aspose.cad.fileformats.cad.CadImage;
import com.aspose.cad.imageoptions.CadRasterizationOptions;
import com.aspose.cad.imageoptions.PngOptions;
```

## كيفية حفظ CAD بصيغة PNG

فيما يلي دليل مختصر خطوة بخطوة يوضح **كيفية تصدير كائنات OLE وحفظ CAD بصيغة PNG**. كل خطوة تتضمن شرحًا قصيرًا يليه الكود الدقيق الذي تحتاج إلى نسخه إلى مشروعك.

### الخطوة 1: تحديد مسار مجلد المستندات

عرّف المجلد الذي يحتوي على رسومات CAD الخاصة بك. استبدل العنصر النائب بالمسار الفعلي على جهازك.

```java
String dataDir = "Your Document Directory" + "DWGDrawings/";
```

### الخطوة 2: تعريف أسماء ملفات CAD

قائمة بكل ملف CAD تريد معالجته. يمكنك إضافة أي عدد من الإدخالات حسب الحاجة.

```java
String[] files = new String[] { "D ZD junior D10m H2m.dwg", "ZD - Senior D6m H2m45.dwg" };
```

### الخطوة 3: ضبط خيارات تصدير PNG

قم بتكوين إعدادات التحويل النقطي. هنا نستهدف تخطيطًا محددًا (`Layout1`) ونستخدم خيارات PNG الافتراضية.

```java
PngOptions pngOptions = new PngOptions();
CadRasterizationOptions rasterizationOptions = new CadRasterizationOptions();
pngOptions.setVectorRasterizationOptions(rasterizationOptions);
rasterizationOptions.setLayouts(new String[] { "Layout1" });
```

### الخطوة 4: التكرار عبر ملفات CAD وحفظها بصيغة PNG

حمّل كل ملف CAD، وحوّل كائنات OLE إلى صور نقطية، واكتب ملف PNG الناتج. يساعد اللاحقة `_out.png` في التعرف على الصور المولدة.

```java
for(String file : files)
{
    CadImage cadImage = (CadImage)Image.load(dataDir + file);
    cadImage.save(dataDir + file + "_out.png", pngOptions);
}
```

## المشكلات الشائعة والحلول

| المشكلة | السبب | الحل |
|---------|-------|------|
| **`Image.load` يطرح `FileNotFoundException`** | مسار `dataDir` غير صحيح أو اسم الملف به خطأ إملائي. | تحقق من سلسلة الدليل وتأكد من تطابق أسماء الملفات تمامًا، بما في ذلك المسافات. |
| **صورة PNG الناتجة فارغة** | اسم التخطيط غير موجود في ملف CAD المصدر. | استخدم `cadImage.getLayouts()` لسرد التخطيطات المتاحة، ثم حدّث `rasterizationOptions.setLayouts(...)`. |
| **ملفات CAD الكبيرة تسبب OutOfMemoryError** | تحويل صور عالية الدقة يستهلك مساحة كبيرة من الذاكرة. | زد حجم heap الخاص بـ JVM (`-Xmx2g`) أو قلل دقة التحويل عبر `rasterizationOptions.setResolution(...)`. |

## الأسئلة المتكررة

### س1: هل Aspose.CAD متوافق مع جميع صيغ ملفات CAD؟

ج1: يدعم Aspose.CAD صيغ CAD متعددة، بما في ذلك DWG وDXF وDGN. راجع [الوثائق](https://reference.aspose.com/cad/java/) للقائمة الكاملة.

### س2: هل يمكنني تخصيص إعدادات التصدير لكائنات OLE؟

ج2: نعم، يوفر Aspose.CAD خيارات واسعة لتخصيص إعدادات التصدير، مما يتيح لك تعديل الناتج وفقًا لمتطلباتك الخاصة.

### س3: هل هناك نسخة تجريبية مجانية متاحة لـ Aspose.CAD؟

ج3: نعم، يمكنك استكشاف قدرات Aspose.CAD بالحصول على نسخة تجريبية مجانية من [هنا](https://releases.aspose.com/).

### س4: أين يمكنني الحصول على دعم المجتمع لـ Aspose.CAD؟

ج4: انضم إلى مجتمع Aspose.CAD عبر [المنتدى](https://forum.aspose.com/c/cad/19) لطلب المساعدة ومشاركة تجاربك.

### س5: كيف يمكنني شراء ترخيص لـ Aspose.CAD؟

ج5: زر [صفحة الشراء](https://purchase.aspose.com/buy) للحصول على ترخيص يناسب احتياجات التطوير الخاصة بك.

## الخاتمة

باتباع هذه الخطوات الخمس البسيطة يمكنك **حفظ CAD بصيغة PNG** واستخراج كل كائن OLE مدمج ببضع أسطر من كود Java فقط. هذا النهج مثالي للتحويلات الدفعية، التقارير الآلية، أو أي سيناريو يتطلب صورًا نقطية لمحتوى CAD دون الحاجة إلى تصدير يدوي. لا تتردد في تجربة خيارات التحويل المختلفة لتتناسب مع متطلبات الجودة والأداء لديك.

---

**آخر تحديث:** 2026-01-04  
**تم الاختبار مع:** Aspose.CAD للـ Java 24.12 (أحدث نسخة وقت الكتابة)  
**المؤلف:** Aspose  

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}