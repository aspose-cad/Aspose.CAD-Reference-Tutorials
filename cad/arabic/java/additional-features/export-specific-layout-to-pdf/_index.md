---
date: 2025-12-04
description: تعلم كيفية تصدير ملفات DXF إلى PDF باستخدام Aspose.CAD للغة Java، وإنشاء PDF
  من DXF، وتحديد حجم الصفحة في Java لتحويلات CAD دقيقة.
language: ar
linktitle: Export Specific DXF Layout to PDF with Java
second_title: Aspose.CAD Java API
title: كيفية تصدير تخطيط DXF إلى PDF باستخدام Aspose.CAD للغة Java
url: /java/additional-features/export-specific-layout-to-pdf/
weight: 17
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# كيفية تصدير تخطيط DXF إلى PDF باستخدام Aspose.CAD للـ Java

## المقدمة

إذا كنت مطور Java تعمل مع رسومات CAD، فأنت تعلم أن **كيفية تصدير dxf** بدقة يمكن أن تكون الفارق بين نجاح المشروع وفشله. سواءً كنت تُنشئ تقارير هندسية، أو تشارك التصاميم مع العملاء، أو تُؤتمت عمليات التحويل الجماعي، فإن مكتبة تحويل PDF موثوقة للـ Java ضرورية. في هذا الدرس سنرشدك إلى تصدير تخطيط DXF محدد إلى PDF باستخدام **Aspose.CAD للـ Java**، موضحين لك كيفية **إنشاء pdf من dxf**، وضبط أبعاد الصفحة، والحفاظ على جودة المتجهات.

## إجابات سريعة
- **ما هي المكتبة الأساسية؟** Aspose.CAD للـ Java، مكتبة تحويل PDF مخصصة للـ CAD.
- **هل يمكن اختيار تخطيط محدد؟** نعم – استخدم `CadRasterizationOptions.setLayouts()` لاستهداف اسم تخطيط معين.
- **كيف أضبط حجم الصفحة؟** عدّل `setPageWidth()` و `setPageHeight()` في خيارات الرستر (مثال: 1600 × 1600).
- **هل أحتاج إلى ترخيص للاستخدام الإنتاجي؟** يتطلب الاستخدام الإنتاجي ترخيصًا تجاريًا؛ يتوفر نسخة تجريبية مجانية.
- **ما نسخة Java المدعومة؟** Java 8 وما فوق (JDK 1.8+).

## ما هو “كيفية تصدير dxf” في Java؟

تصدير ملف DXF يعني تحويل بياناته المتجهة إلى تنسيق آخر—غالبًا PDF—مع الحفاظ على الطبقات، وزن الخطوط، ومعلومات التخطيط. يتولى Aspose.CAD الجزء الأكبر من العمل، مما يتيح لك التركيز على منطق الأعمال بدلاً من تحليل الملفات منخفض المستوى.

## لماذا نستخدم Aspose.CAD للـ Java؟

- **دعم CAD شامل** – يتعامل مع DWG، DXF، DWF، وأكثر.
- **بدون تبعيات خارجية** – جافا صافية، لا ملفات DLL أصلية.
- **رستر دقيقة** – اختر مخرجات متجهة أو رستر، عيّن DPI، حجم الصفحة، والتخطيط.
- **أداء عالي** – مُحسّن للمعالجة الدفعية وسيناريوهات الخادم.

## المتطلبات المسبقة

قبل البدء، تأكد من وجود ما يلي:

1. **مجموعة تطوير جافا (JDK)** – Java 8 أو أحدث. حمّلها من [Oracle](https://www.oracle.com/java/technologies/javase-downloads.html).
2. **Aspose.CAD للـ Java** – احصل على أحدث ملف JAR من [صفحة تنزيل Aspose.CAD](https://releases.aspose.com/cad/java/).
3. بيئة تطوير متكاملة أو أداة بناء (Maven/Gradle) لإضافة ملف JAR إلى مسار الفئة (classpath) الخاص بالمشروع.

## استيراد الحزم

أولاً، استورد الفئات التي ستحتاجها. تتيح لك هذه الاستيرادات تحميل الصور، خيارات الرستر، وإعدادات إخراج PDF.

```java
import com.aspose.cad.Image;
import com.aspose.cad.imageoptions.CadRasterizationOptions;
import com.aspose.cad.imageoptions.PdfOptions;
```

### دليل خطوة بخطوة

### الخطوة 1: ضبط دليل الموارد

عرّف المجلد الذي يحتوي على ملفات DXF الخاصة بك. استبدل العنصر النائب بالمسار الفعلي على جهازك.

```java
String dataDir = "Your Document Directory" + "DXFDrawings/";
```

> **نصيحة احترافية:** استخدم `System.getProperty("user.dir")` لإنشاء مسار نسبي يعمل عبر البيئات المختلفة.

### الخطوة 2: تحميل ملف DXF

حمّل ملف DXF المصدر باستخدام `Image.load()`. هذه الطريقة تقرأ ملف CAD إلى كائن `Image` الخاص بـ Aspose.CAD.

```java
String srcFile = dataDir + "conic_pyramid.dxf";
Image image = Image.load(srcFile); 
```

### الخطوة 3: ضبط خيارات الرستر (تعيين حجم الصفحة Java)

هنا ننشئ `CadRasterizationOptions` ونحدد حجم الصفحة الناتج. عدّل العرض/الارتفاع ليتطابق مع أبعاد PDF المطلوبة.

```java
CadRasterizationOptions rasterizationOptions = new CadRasterizationOptions();
rasterizationOptions.setPageWidth(1600);
rasterizationOptions.setPageHeight(1600);   
rasterizationOptions.setLayouts(new String[] {"Model"});
```

- `setPageWidth` / `setPageHeight` – يتحكم في **تعيين حجم الصفحة java** للـ PDF.
- `setLayouts` – يحدد أي تخطيط(ات) سيتم رسمها؛ `"Model"` هو مساحة النموذج الافتراضية في العديد من ملفات DXF.

### الخطوة 4: إنشاء خيارات PDF (Java Convert CAD PDF)

اربط إعدادات الرستر بمثيل `PdfOptions`. هذا يخبر Aspose.CAD بإنتاج PDF بدلاً من صورة رستر.

```java
PdfOptions pdfOptions = new PdfOptions();
pdfOptions.setVectorRasterizationOptions(rasterizationOptions);
```

### الخطوة 5: تصدير DXF إلى PDF (إنشاء PDF من DXF)

أخيرًا، احفظ الصورة كملف PDF. اسم الملف الناتج ينتهي بـ `_layout_out_.pdf` للدلالة على التحويل الخاص بالتخطيط.

```java
image.save(dataDir + "conic_pyramid_layout_out_.pdf", pdfOptions);
```

بعد التنفيذ، ستجد `conic_pyramid_layout_out_.pdf` في نفس الدليل، يحتوي فقط على تخطيط **Model** المرسوم بالأبعاد التي حددتها.

## المشكلات الشائعة والحلول

| المشكلة | السبب | الحل |
|-------|--------|-----|
| **PDF فارغ** | عدم تطابق اسم التخطيط | تحقق من اسم التخطيط الدقيق في ملف DXF (استخدم عارض CAD). |
| **حجم الصفحة غير صحيح** | عدم تطبيق `setPageWidth/Height` | تأكد من ضبط خيارات الرستر **قبل** إنشاء `PdfOptions`. |
| **نفاد الذاكرة للملفات الكبيرة** | تحميل DXF ضخم في الذاكرة | استخدم البث أو زد حجم heap للـ JVM (`-Xmx2g`). |
| **خطوط مفقودة** | عناصر النص تستخدم خطوطًا غير متوفرة | ثبّت الخطوط المطلوبة على الخادم أو أدخلها عبر `CadRasterizationOptions`. |

## الأسئلة المتكررة

**س: هل Aspose.CAD للـ Java مناسب للمبتدئين وكذلك للمطورين ذوي الخبرة؟**  
ج: بالتأكيد. الواجهة البرمجية سهلة للمبتدئين وتوفر تخصيصًا عميقًا للمستخدمين المتقدمين.

**س: هل يمكنني تخصيص خيارات الرستر لتخطيطات مختلفة؟**  
ج: نعم. عدّل `CadRasterizationOptions` (حجم الصفحة، DPI، لون الخلفية) لكل تخطيط حسب الحاجة.

**س: أين يمكنني العثور على الوثائق الشاملة لـ Aspose.CAD للـ Java؟**  
ج: الوثائق التفصيلية متاحة [هنا](https://reference.aspose.com/cad/java/).

**س: هل تتوفر نسخة تجريبية مجانية لـ Aspose.CAD للـ Java؟**  
ج: نعم، يمكنك تنزيل نسخة تجريبية [هنا](https://releases.aspose.com/).

**س: كيف يمكنني الحصول على الدعم لـ Aspose.CAD للـ Java؟**  
ج: زر منتدى الدعم [هنا](https://forum.aspose.com/c/cad/19) للحصول على مساعدة المجتمع والموظفين.

## الخاتمة

في هذا الدليل استعرضنا **كيفية تصدير dxf** إلى PDF باستخدام Aspose.CAD للـ Java، بدءًا من إعداد البيئة وحتى ضبط أبعاد الصفحة بدقة. من خلال الاستفادة من هذه **مكتبة تحويل pdf للـ java**، يمكنك أتمتة سير عمل CAD‑to‑PDF، الحفاظ على دقة المتجهات، ودمج توليد PDF بسلاسة في تطبيقات Java الخاصة بك.

---

**آخر تحديث:** 2025-12-04  
**تم الاختبار مع:** Aspose.CAD للـ Java 24.12 (أحدث نسخة وقت الكتابة)  
**المؤلف:** Aspose  

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}