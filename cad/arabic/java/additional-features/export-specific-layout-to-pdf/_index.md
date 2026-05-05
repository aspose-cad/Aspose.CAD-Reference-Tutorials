---
date: 2026-02-04
description: تعلم كيفية إنشاء ملف PDF من DXF وتصدير DXF إلى PDF باستخدام Aspose.CAD
  للغة Java، وضبط عرض صفحة PDF، وإنشاء PDF من CAD مع تحكم دقيق.
linktitle: Export Specific DXF Layout to PDF with Java
second_title: Aspose.CAD Java API
title: إنشاء PDF من تخطيط DXF إلى PDF باستخدام Aspose.CAD لجافا
url: /ar/java/additional-features/export-specific-layout-to-pdf/
weight: 17
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# إنشاء pdf من تخطيط dxf إلى PDF باستخدام Aspose.CAD للـ Java

## مقدمة

إذا كنت مطور Java تعمل مع رسومات CAD، فأنت تعلم أن **كيفية تصدير ملفات dxf** بدقة يمكن أن تكون الفارق بين نجاح أو فشل المشروع. سواءً كنت تولد تقارير هندسية، أو تشارك التصاميم مع العملاء، أو تقوم بأتمتة تحويلات دفعة، فإن مكتبة تحويل PDF موثوقة للـ Java أساسية. في هذا الدرس سنرشدك إلى **إنشاء pdf من تخطيط dxf**، وضبط أبعاد الصفحة، والحفاظ على جودة المتجهات باستخدام **Aspose.CAD للـ Java**.

## إجابات سريعة
- **ما هي المكتبة الأساسية؟** Aspose.CAD للـ Java، مكتبة تحويل pdf مخصصة للـ Java للـ CAD.
- **هل يمكنني اختيار تخطيط محدد؟** نعم – استخدم `CadRasterizationOptions.setLayouts()` لاستهداف اسم تخطيط.
- **كيف يمكنني ضبط حجم الصفحة؟** اضبط `setPageWidth()` و `setPageHeight()` في خيارات الرستر (مثال: 1600 × 1600).
- **هل أحتاج إلى ترخيص للإنتاج؟** يلزم ترخيص تجاري للاستخدام في الإنتاج؛ يتوفر نسخة تجريبية مجانية.
- **ما نسخة Java المدعومة؟** Java 8 وما فوق (JDK 1.8+).

## كيف تنشئ pdf من تخطيط DXF؟

تصدير ملف DXF يعني تحويل بياناته المتجهة إلى تنسيق آخر—غالبًا PDF—مع الحفاظ على الطبقات، وزن الخطوط، ومعلومات التخطيط. تقوم Aspose.CAD بالعمل الشاق، مما يتيح لك التركيز على منطق الأعمال بدلاً من تحليل الملفات على مستوى منخفض.

## لماذا تستخدم Aspose.CAD للـ Java؟

- **دعم CAD كامل الميزات** – يتعامل مع DWG، DXF، DWF، وأكثر.
- **بدون تبعيات خارجية** – جافا صافية، بدون ملفات DLL أصلية.
- **رستر دقيقة** – اختر مخرجات متجهة أو رستر، اضبط DPI، حجم الصفحة، والتخطيط.
- **أداء عالي** – مُحسّن للمعالجة الدفعية وسيناريوهات الخادم.
- **تصدير dxf إلى pdf** بسطر واحد من الكود، مما يجعله مثاليًا لتدفقات عمل **java convert cad pdf**.

## المتطلبات المسبقة

قبل أن تبدأ، تأكد من وجود ما يلي:

1. **Java Development Kit (JDK)** – Java 8 أو أحدث. قم بتنزيله من [Oracle](https://www.oracle.com/java/technologies/javase-downloads.html).
2. **Aspose.CAD للـ Java** – احصل على أحدث ملف JAR من [صفحة تنزيل Aspose.CAD](https://releases.aspose.com/cad/java/).
3. بيئة تطوير متكاملة أو أداة بناء (Maven/Gradle) لإضافة ملف JAR الخاص بـ Aspose.CAD إلى مسار الفئة في مشروعك.

## استيراد المساحات الاسمية

أولاً، استورد الفئات التي ستحتاجها. هذه الاستيرادات تمنحك الوصول إلى تحميل الصور، خيارات الرستر، وإعدادات إخراج PDF.

```java
import com.aspose.cad.Image;
import com.aspose.cad.imageoptions.CadRasterizationOptions;
import com.aspose.cad.imageoptions.PdfOptions;
```

## دليل خطوة بخطوة

### الخطوة 1: تعيين دليل الموارد

حدد المجلد الذي يحتوي على ملفات DXF الخاصة بك. استبدل العنصر النائب بالمسار الفعلي على جهازك.

```java
String dataDir = "Your Document Directory" + "DXFDrawings/";
```

> **نصيحة احترافية:** استخدم `System.getProperty("user.dir")` لإنشاء مسار نسبي يعمل عبر البيئات.

### الخطوة 2: تحميل ملف DXF

حمّل ملف DXF المصدر باستخدام `Image.load()`. هذه الطريقة تقرأ ملف CAD إلى كائن `Image` الخاص بـ Aspose.CAD.

```java
String srcFile = dataDir + "conic_pyramid.dxf";
Image image = Image.load(srcFile); 
```

### الخطوة 3: تكوين خيارات الرستر (تعيين عرض صفحة PDF في Java)

هنا نقوم بإنشاء `CadRasterizationOptions` وتحديد حجم صفحة الإخراج. اضبط العرض/الارتفاع لتتناسب مع أبعاد PDF المطلوبة.

```java
CadRasterizationOptions rasterizationOptions = new CadRasterizationOptions();
rasterizationOptions.setPageWidth(1600);
rasterizationOptions.setPageHeight(1600);   
rasterizationOptions.setLayouts(new String[] {"Model"});
```

- `setPageWidth` / `setPageHeight` – يتحكم في **set pdf page width** (والارتفاع) للـ PDF.  
- `setLayouts` – يحدد أي تخطيط(ات) يتم عرضها؛ `"Model"` هو مساحة النموذج الافتراضية في العديد من ملفات DXF.

### الخطوة 4: إنشاء خيارات PDF (Java Convert CAD PDF)

اربط إعدادات الرستر بكائن `PdfOptions`. هذا يخبر Aspose.CAD بإنتاج PDF بدلاً من صورة رستر.

```java
PdfOptions pdfOptions = new PdfOptions();
pdfOptions.setVectorRasterizationOptions(rasterizationOptions);
```

### الخطوة 5: تصدير DXF إلى PDF (إنشاء PDF من DXF)

أخيرًا، احفظ الصورة كملف PDF. اسم الملف الناتج ينتهي بـ `_layout_out_.pdf` للدلالة على التحويل الخاص بالتخطيط.

```java
image.save(dataDir + "conic_pyramid_layout_out_.pdf", pdfOptions);
```

بعد التنفيذ، ستجد `conic_pyramid_layout_out_.pdf` في نفس الدليل، يحتوي فقط على تخطيط **Model** المرسوم بالأبعاد التي ضبطتها.

## حالات الاستخدام الشائعة

| السيناريو | لماذا تساعد هذه الطريقة |
|----------|--------------------------|
| **إنشاء تقارير آلية** | يضمن تصدير كل رسم بنفس حجم الصفحة، مما يجعل ملفات PDF الدفعية متجانسة. |
| **معاينات التصميم للعميل** | تصدير تخطيط واحد (مثل “Model” أو “Sheet1”) يقلل حجم الملف مع الحفاظ على دقة المتجهات. |
| **ترحيل DWG القديم إلى PDF** | على الرغم من أن هذا المثال يستخدم DXF، فإن نفس الـ API يعمل لـ **convert dwg to pdf** مع أقل تغييرات في الكود. |
| **دمج رسومات CAD في البوابات الإلكترونية** | يمكن بث ملف PDF المُولد مباشرةً إلى المتصفحات دون أدوات تحويل إضافية. |

## المشكلات الشائعة والحلول

| المشكلة | السبب | الحل |
|---------|-------|------|
| **PDF فارغ** | عدم تطابق اسم التخطيط | تحقق من اسم التخطيط الدقيق في ملف DXF (استخدم عارض CAD). |
| **حجم صفحة غير صحيح** | `setPageWidth/Height` لم يتم تطبيقه | تأكد من ضبط خيارات الرستر **قبل** إنشاء `PdfOptions`. |
| **نفاد الذاكرة للملفات الكبيرة** | تحميل ملف DXF ضخم في الذاكرة | استخدم البث أو زد حجم كومة JVM (`-Xmx2g`). |
| **خطوط مفقودة** | العناصر النصية تستخدم خطوطًا غير متوفرة | ثبت الخطوط المطلوبة على الخادم أو دمجها عبر `CadRasterizationOptions`. |
| **الحاجة لتصدير تخطيطات متعددة** | استدعاء تخطيط واحد فقط | استدعِ `setLayouts` بمصفوفة من أسماء التخطيطات وكرر خطوة `save` لكل منها. |

## الأسئلة المتكررة

**س: هل Aspose.CAD للـ Java مناسب لكل من المبتدئين والمطورين ذوي الخبرة؟**  
**ج:** بالتأكيد. الـ API سهل الفهم للمبتدئين بينما يوفر تخصيصًا عميقًا للمستخدمين المتقدمين.

**س: هل يمكنني تخصيص خيارات الرستر لتخطيطات مختلفة؟**  
**ج:** نعم. اضبط `CadRasterizationOptions` (حجم الصفحة، DPI، لون الخلفية) لكل تخطيط حسب الحاجة.

**س: أين يمكنني العثور على وثائق شاملة لـ Aspose.CAD للـ Java؟**  
**ج:** الوثائق التفصيلية متاحة [هنا](https://reference.aspose.com/cad/java/).

**س: هل هناك نسخة تجريبية مجانية متاحة لـ Aspose.CAD للـ Java؟**  
**ج:** نعم، يمكنك تنزيل نسخة تجريبية [هنا](https://releases.aspose.com/).

**س: كيف يمكنني الحصول على دعم لـ Aspose.CAD للـ Java؟**  
**ج:** زر منتدى الدعم [هنا](https://forum.aspose.com/c/cad/19) للحصول على مساعدة من المجتمع والموظفين.

## الخلاصة

في هذا الدليل أظهرنا **كيفية إنشاء pdf من تخطيطات dxf** إلى PDF باستخدام Aspose.CAD للـ Java، مع تغطية كل شيء من إعداد البيئة إلى ضبط أبعاد الصفحة بدقة. من خلال الاستفادة من هذه **java pdf conversion library**، يمكنك أتمتة سير عمل CAD‑to‑PDF، الحفاظ على دقة المتجهات، ودمج توليد PDF بسلاسة في تطبيقات Java الخاصة بك. سواءً كنت بحاجة إلى **export dxf to pdf**، **convert dwg to pdf**، أو **generate pdf from cad** للمعالجة اللاحقة، فإن الخطوات أعلاه تمنحك أساسًا قويًا.

---

**آخر تحديث:** 2026-02-04  
**تم الاختبار مع:** Aspose.CAD للـ Java 24.12 (الأحدث وقت الكتابة)  
**المؤلف:** Aspose  

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}