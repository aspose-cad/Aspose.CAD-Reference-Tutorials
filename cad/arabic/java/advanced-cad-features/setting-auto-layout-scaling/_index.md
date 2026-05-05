---
date: 2026-02-15
description: تعلم كيفية تعيين حجم صفحة مخصص وإنشاء ملف PDF من CAD باستخدام Aspose.CAD
  للغة Java. يغطي هذا الدليل خطوة بخطوة تصدير CAD إلى PDF مع التحجيم التلقائي للتخطيط.
linktitle: Setting Auto Layout Scaling
second_title: Aspose.CAD Java API
title: تعيين حجم صفحة مخصص – PDF من CAD مع التحجيم التلقائي للتخطيط
url: /ar/java/advanced-cad-features/setting-auto-layout-scaling/
weight: 17
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# تعيين حجم صفحة مخصص – إنشاء PDF من CAD مع مقياس التخطيط التلقائي

## المقدمة

إذا كنت بحاجة إلى **set custom page size** أثناء **create PDF from CAD** بسرعة ومع مقياس مثالي، فإن Aspose.CAD for Java يغطي احتياجاتك. يقوم Auto Layout Scaling تلقائيًا بضبط أبعاد التخطيط بحيث يبدو ملف PDF الناتج تمامًا كما هو مقصود، بغض النظر عن حجم صفحة CAD الأصلي. في هذا الدرس سنستعرض العملية بالكامل — من تحميل ملف DXF إلى تصدير PDF — مع إبراز قدرات **export CAD to PDF** للمكتبة وإظهار كيفية **convert DWG to PDF** أو **increase PDF resolution** عند الحاجة.

## إجابات سريعة
- **What does Auto Layout Scaling do?** يقوم تلقائيًا بإعادة تحجيم تخطيطات CAD لتتناسب مع أبعاد الصفحة المستهدفة عند الرستر.
- **Which formats can I convert?** أي تنسيق مدعوم من Aspose.CAD (مثل DXF, DWG, DWF) يمكن تحويله إلى PDF.
- **Do I need a license for production?** نعم، يلزم الحصول على ترخيص تجاري للاستخدام غير التجريبي.
- **How long does the conversion take?** عادةً أقل من ثانية للملفات القياسية على الأجهزة الحديثة.
- **Can I change the page size?** نعم، يمكنك تعيين أبعاد صفحة مخصصة عبر `CadRasterizationOptions`.

## ما هو “إنشاء PDF من CAD”؟

إنشاء PDF من CAD يعني أخذ رسم هندسي قائم على المتجهات (DXF, DWG, إلخ) ورسترته إلى مستند PDF. يحتفظ PDF بوضوح الصورة الأصلي بينما يكون قابلًا للعرض على أي منصة.

## لماذا نستخدم مقياس التخطيط التلقائي؟

- **Consistent output:** يضمن أن جميع التخطيطات تملأ صفحة PDF دون الحاجة إلى حسابات حجم يدوية.
- **Time‑saving:** يلغي الحاجة إلى تعديل عوامل المقياس يدويًا لكل رسم.
- **High quality:** يحافظ على وزن الخط ودقة الهندسة أثناء التحويل.
- **Flexibility:** يعمل مع **convert dxf to pdf**, **convert dwg to pdf**, وحتى عندما تحتاج إلى **increase PDF resolution** للملفات الجاهزة للطباعة.

## المتطلبات المسبقة

1. **Aspose.CAD for Java Library** – قم بتنزيل أحدث نسخة من [download page](https://releases.aspose.com/cad/java/).  
2. **Resource Directory** – أنشئ مجلدًا على جهازك لتخزين ملفات CAD؛ استبدل `"Your Document Directory"` في الشيفرة بهذا المسار.  
3. **Sample CAD File** – في هذا الدليل سنستخدم `conic_pyramid.dxf`، المتضمن في مجموعة بيانات Aspose التجريبية.

## استيراد المساحات الاسمية

أولاً، استورد الفئات المطلوبة. يتيح لنا ذلك الوصول إلى ميزات تحميل الصور والرستر وتصدير PDF.

```java
import com.aspose.cad.Image;

import com.aspose.cad.imageoptions.CadRasterizationOptions;
import com.aspose.cad.imageoptions.PdfOptions;
```

## كيفية تعيين حجم صفحة مخصص لإنشاء PDF من CAD

قبل الغوص في الشيفرة خطوة بخطوة، دعنا نفهم لماذا يعتبر تعيين حجم صفحة مخصص مهمًا. عندما **set custom page size**، تتحكم في الأبعاد الفيزيائية للـ PDF الناتج (مثل A4، Letter، أو حجم مخصص). هذا أساسي في سير عمل الهندسة حيث يجب أن تتطابق الرسومات مع معايير الأوراق أو عندما تحتاج إلى دمج PDF في مستندات أكبر.

### الخطوة 1: تحميل ملف CAD

تحميل الملف المصدر هو الخطوة الأولى في **how to export CAD** إلى مستند PDF.

```java
String srcFile = dataDir + "conic_pyramid.dxf";
Image image = Image.load(srcFile);
```

### الخطوة 2: إنشاء خيارات الرستر

حدد أبعاد الصفحة المستهدفة. يمكنك أيضًا استخدام هذا القسم **set CAD page size** يدويًا إذا كنت تفضل تخطيطًا مخصصًا.

```java
CadRasterizationOptions rasterizationOptions = new CadRasterizationOptions();
rasterizationOptions.setPageWidth(1600);
rasterizationOptions.setPageHeight(1600);
```

### الخطوة 3: تعيين مقياس التخطيط التلقائي

فعّل ميزة المقياس التلقائي. هذا هو جوهر **how to set scaling** لتحويل CAD إلى PDF.

```java
rasterizationOptions.setAutomaticLayoutsScaling(true);
```

### الخطوة 4: إنشاء خيارات PDF

اربط إعدادات الرستر بخيارات تصدير PDF.

```java
PdfOptions pdfOptions = new PdfOptions();
pdfOptions.setVectorRasterizationOptions(rasterizationOptions);
```

### الخطوة 5: تصدير إلى PDF

أخيرًا، احفظ الصورة المرسومة كملف PDF. تكمل هذه الخطوة سير عمل **convert dxf to pdf**.

```java
image.save(dataDir + "result_out_.pdf", pdfOptions);
```

كرر الخطوات أعلاه لأي ملفات CAD إضافية تحتاج إلى معالجتها، سواء كانت **DWG**, **DWF**, أو أي تنسيقات مدعومة أخرى.

## حالات الاستخدام الشائعة

| السيناريو | لماذا تعيين حجم صفحة مخصص؟ |
|----------|-----------------------------|
| **تقديم رسومات الإنشاء** | يطابق PDF مع أحجام الأوراق القياسية A1/A2 المطلوبة من الجهات التنظيمية. |
| **إدراج في الأدلة التقنية** | يضمن أن الرسم يتناسب مع التخطيط المحدد مسبقًا للدليل دون الحاجة إلى مقياس إضافي. |
| **الطباعة عالية الدقة** | يسمح لك بزيادة DPI (مثل `rasterizationOptions.setResolution(300)`) مع الحفاظ على أبعاد الصفحة ثابتة. |

## المشكلات الشائعة & استكشاف الأخطاء وإصلاحها

| العَرَض | السبب المحتمل | الحل |
|---------|--------------|-----|
| ملف PDF فارغ | لم يتم تعيين خيارات الرستر أو مسار الملف غير صحيح | تحقق من مسار `srcFile` وتأكد من أن `setPageWidth/Height` غير صفرية |
| تشويه في المقياس | ترك `setAutomaticLayoutsScaling` كـ `false` | فعّل المقياس التلقائي أو احسب عامل المقياس يدويًا |
| طبقات مفقودة | يحتوي DXF المصدر على كيانات غير مدعومة | راجع ملاحظات إصدار Aspose.CAD للكيانات المدعومة |

## الأسئلة المتكررة

**س: هل Aspose.CAD for Java متوافق مع جميع تنسيقات ملفات CAD؟**  
ج: يدعم Aspose.CAD for Java تنسيقات CAD متعددة، بما في ذلك DWG, DXF, و DWF.

**س: هل يمكنني تخصيص خيارات المقياس أكثر؟**  
ج: نعم، توفر فئة `CadRasterizationOptions` خصائص لضبط المقياس، DPI، وإعدادات الرستر الأخرى بدقة.

**س: أين يمكنني العثور على وثائق إضافية لـ Aspose.CAD for Java؟**  
ج: راجع [documentation](https://reference.aspose.com/cad/java/) للحصول على معلومات مفصلة وأمثلة.

**س: هل هناك تجربة مجانية متاحة لـ Aspose.CAD for Java؟**  
ج: نعم، يمكنك تجربة [free trial](https://releases.aspose.com/) لاستكشاف قدرات Aspose.CAD for Java.

**س: كيف يمكنني طلب المساعدة أو المشاركة في مناقشات حول Aspose.CAD for Java؟**  
ج: زر [Aspose.CAD forum](https://forum.aspose.com/c/cad/19) للتواصل مع المجتمع وطلب الدعم.

**أسئلة شائعة إضافية**

**س: كيف أحول ملف DWG إلى PDF بدلاً من DXF؟**  
ج: نفس الشيفرة تعمل؛ فقط غيّر امتداد الملف في `srcFile` إلى `.dwg`.

**س: هل يمكنني تعيين DPI مخصص لملفات PDF ذات الدقة الأعلى؟**  
ج: نعم، استخدم `rasterizationOptions.setResolution(300);` (أو أي DPI تحتاجه).

**س: هل يمكن تضمين الخطوط في PDF المُولد؟**  
ج: يقوم Aspose.CAD برستر الرسم، لذا تُعرض الخطوط كمتجهات؛ لا يلزم تضمين خطوط منفصلة.

## الخلاصة

باتباعك لهذا الدليل، أصبحت الآن تعرف كيفية **set custom page size** و**create PDF from CAD** باستخدام Aspose.CAD for Java مع Auto Layout Scaling. تُبسّط العملية سير عمل **export CAD to PDF**، وتضمن مقياسًا ثابتًا، وتوفر لك وقتًا ثمينًا في التطوير. لا تتردد في تجربة أحجام صفحات مختلفة، ودقات مختلفة، وتنسيقات CAD لتلبية احتياجات مشروعك، سواء كنت **converting DWG to PDF**, **increasing PDF resolution**, أو بناء معالج دفعي **java CAD to PDF**.

---

**آخر تحديث:** 2026-02-15  
**تم الاختبار مع:** Aspose.CAD for Java 24.12 (latest)  
**المؤلف:** Aspose  

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}