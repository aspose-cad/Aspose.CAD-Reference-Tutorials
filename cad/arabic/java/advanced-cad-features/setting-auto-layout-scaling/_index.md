---
date: 2025-12-10
description: تعلم كيفية إنشاء ملف PDF من CAD باستخدام Aspose.CAD للغة Java مع مقياس
  التخطيط التلقائي. يوضح لك هذا الدليل خطوة بخطوة كيفية تصدير CAD إلى PDF بكفاءة وموثوقية.
linktitle: Setting Auto Layout Scaling
second_title: Aspose.CAD Java API
title: إنشاء PDF من CAD – التحجيم التلقائي للتخطيط باستخدام Aspose.CAD Java
url: /ar/java/advanced-cad-features/setting-auto-layout-scaling/
weight: 17
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# إنشاء PDF من CAD – التحجيم التلقائي للتخطيط باستخدام Aspose.CAD Java

## المقدمة

إذا كنت بحاجة إلى **إنشاء PDF من ملفات CAD** بسرعة وبتحجيم مثالي، فإن Aspose.CAD for Java يلبي احتياجاتك. يقوم التحجيم التلقائي للتخطيط تلقائيًا بضبط أبعاد التخطيط بحيث يبدو ملف PDF الناتج كما هو مقصود، بغض النظر عن حجم صفحة CAD الأصلي. في هذا البرنامج التعليمي سنستعرض العملية بالكامل — من تحميل ملف DXF إلى تصدير PDF — مع تسليط الضوء على قدرات **تصدير CAD إلى PDF** للمكتبة.

## إجابات سريعة
- **ماذا يفعل التحجيم التلقائي للتخطيط؟** يقوم تلقائيًا بإعادة تحجيم تخطيطات CAD لتتناسب مع أبعاد الصفحة المستهدفة عند التحويل إلى صورة نقطية.
- **ما الصيغ التي يمكنني تحويلها؟** أي صيغة يدعمها Aspose.CAD (مثل DXF، DWG، DWF) يمكن تحويلها إلى PDF.
- **هل أحتاج إلى ترخيص للاستخدام في الإنتاج؟** نعم، يلزم الحصول على ترخيص تجاري للاستخدام غير التجريبي.
- **كم يستغرق التحويل من وقت؟** عادةً أقل من ثانية للملفات القياسية على الأجهزة الحديثة.
- **هل يمكنني تغيير حجم الصفحة؟** نعم، يمكنك تعيين أبعاد صفحة مخصصة عبر `CadRasterizationOptions`.

## ما هو “إنشاء PDF من CAD”؟
إنشاء PDF من CAD يعني أخذ رسم هندسي قائم على المتجهات (DXF، DWG، إلخ) وتحويله إلى مستند PDF بصورة نقطية. يحتفظ PDF بدقة العرض الأصلية للرسم بينما يكون قابلًا للعرض على أي منصة.

## لماذا نستخدم التحجيم التلقائي للتخطيط؟
- **إنتاج ثابت:** يضمن أن جميع التخطيطات تملأ صفحة PDF دون الحاجة إلى حسابات يدوية للحجم.
- **توفير الوقت:** يلغي الحاجة إلى تعديل عوامل التحجيم يدويًا لكل رسم.
- **جودة عالية:** يحافظ على وزن الخط ودقة الهندسة أثناء التحويل.

## المتطلبات المسبقة

1. **مكتبة Aspose.CAD for Java** – قم بتنزيل أحدث نسخة من [صفحة التنزيل](https://releases.aspose.com/cad/java/).  
2. **دليل الموارد** – أنشئ مجلدًا على جهازك لتخزين ملفات CAD؛ استبدل `"Your Document Directory"` في الشيفرة بمسار ذلك المجلد.  
3. **ملف CAD تجريبي** – في هذا الدليل سنستخدم `conic_pyramid.dxf`، وهو مدرج في مجموعة بيانات Aspose التجريبية.

## استيراد المساحات الاسمية

أولاً، استورد الفئات المطلوبة. يتيح لنا ذلك الوصول إلى ميزات تحميل الصور، التحويل إلى صورة نقطية، وتصدير PDF.

```java
import com.aspose.cad.Image;

import com.aspose.cad.imageoptions.CadRasterizationOptions;
import com.aspose.cad.imageoptions.PdfOptions;
```

## الخطوة 1: تحميل ملف CAD

تحميل الملف المصدر هو الخطوة الأولى في **كيفية تصدير CAD** إلى مستند PDF.

```java
String srcFile = dataDir + "conic_pyramid.dxf";
Image image = Image.load(srcFile);
```

## الخطوة 2: إنشاء خيارات التحويل إلى صورة نقطية

حدد أبعاد الصفحة المستهدفة. يمكنك أيضًا استخدام هذا القسم **لتعيين حجم صفحة CAD** يدويًا إذا كنت تفضل تخطيطًا مخصصًا.

```java
CadRasterizationOptions rasterizationOptions = new CadRasterizationOptions();
rasterizationOptions.setPageWidth(1600);
rasterizationOptions.setPageHeight(1600);
```

## الخطوة 3: تفعيل التحجيم التلقائي للتخطيط

فعّل ميزة التحجيم التلقائي. هذه هي جوهر **كيفية ضبط التحجيم** لتحويل CAD إلى PDF.

```java
rasterizationOptions.setAutomaticLayoutsScaling(true);
```

## الخطوة 4: إنشاء خيارات PDF

اربط إعدادات التحويل إلى صورة نقطية بخيارات تصدير PDF.

```java
PdfOptions pdfOptions = new PdfOptions();
pdfOptions.setVectorRasterizationOptions(rasterizationOptions);
```

## الخطوة 5: تصدير إلى PDF

أخيرًا، احفظ الصورة المرسومة كملف PDF. تكمل هذه الخطوة سير عمل **تحويل DXF إلى PDF**.

```java
image.save(dataDir + "result_out_.pdf", pdfOptions);
```

كرر الخطوات أعلاه لأي ملفات CAD إضافية تحتاج إلى معالجتها.

## المشكلات الشائعة & استكشاف الأخطاء وإصلاحها

| العرض | السبب المحتمل | الحل |
|---------|--------------|-----|
| PDF فارغ | لم يتم ضبط خيارات التحويل إلى صورة نقطية أو مسار الملف غير صحيح | تحقق من مسار `srcFile` وتأكد من أن `setPageWidth/Height` غير صفرية |
| تحجيم مشوه | ترك `setAutomaticLayoutsScaling` على `false` | فعّل التحجيم التلقائي أو احسب عامل التحجيم يدويًا |
| طبقات مفقودة | يحتوي ملف DXF المصدر على كيانات غير مدعومة | راجع ملاحظات إصدار Aspose.CAD للكيانات المدعومة |

## الأسئلة المتكررة

### س1: هل Aspose.CAD for Java متوافق مع جميع صيغ ملفات CAD؟

ج1: يدعم Aspose.CAD for Java صيغ CAD متعددة، بما في ذلك DWG، DXF، و DWF.

### س2: هل يمكنني تخصيص خيارات التحجيم أكثر؟

ج2: نعم، توفر فئة `CadRasterizationOptions` خصائص متعددة لضبط التحجيم وإعدادات أخرى بدقة.

### س3: أين يمكنني العثور على وثائق إضافية لـ Aspose.CAD for Java؟

ج3: راجع [الوثائق](https://reference.aspose.com/cad/java/) للحصول على معلومات متعمقة وأمثلة.

### س4: هل هناك نسخة تجريبية مجانية متاحة لـ Aspose.CAD for Java؟

ج4: نعم، يمكنك تجربة [نسخة تجريبية مجانية](https://releases.aspose.com/) لاستكشاف قدرات Aspose.CAD for Java.

### س5: كيف يمكنني طلب المساعدة أو المشاركة في مناقشات حول Aspose.CAD for Java؟

ج5: زر [منتدى Aspose.CAD](https://forum.aspose.com/c/cad/19) للتواصل مع المجتمع وطلب الدعم.

**أسئلة شائعة إضافية**

**س: كيف أحول ملف DWG إلى PDF بدلاً من DXF؟**  
ج: نفس الشيفرة تعمل؛ فقط غيّر امتداد الملف في `srcFile` إلى `.dwg`.

**س: هل يمكنني تعيين DPI مخصص للحصول على PDF بدقة أعلى؟**  
ج: نعم، استخدم `rasterizationOptions.setResolution(300);` (أو أي قيمة DPI تحتاجها).

**س: هل يمكن تضمين الخطوط في PDF المُنشأ؟**  
ج: يقوم Aspose.CAD بتحويل الرسم إلى صورة نقطية، لذا تُرسم الخطوط كمتجهات؛ لا يلزم تضمين خطوط منفصلة.

## الخاتمة

باتباعك لهذا الدليل، أصبحت الآن تعرف **كيفية إنشاء PDF من ملفات CAD** باستخدام Aspose.CAD for Java مع التحجيم التلقائي للتخطيط. تُبسّط العملية سير عمل **تصدير CAD إلى PDF**، وتضمن تحجيمًا ثابتًا، وتوفر لك وقتًا ثمينًا في التطوير. لا تتردد في تجربة أحجام صفحات مختلفة، دقة أعلى، وصيغ CAD متعددة لتلبية احتياجات مشروعك.

---

**آخر تحديث:** 2025-12-10  
**تم الاختبار مع:** Aspose.CAD for Java 24.12 (أحدث نسخة)  
**المؤلف:** Aspose  

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}