---
date: 2026-02-20
description: تعلم كيفية تحويل STL إلى PNG باستخدام Aspose.CAD للـ Java. يوضح هذا الدليل
  خطوة بخطوة كيفية تصدير ملفات STL بكفاءة.
linktitle: Export STL to PNG
second_title: Aspose.CAD Java API
title: كيفية تحويل STL إلى PNG باستخدام Aspose.CAD للـ Java
url: /ar/java/cad-export-options/export-stl-to-png/
weight: 20
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# تحويل STL إلى PNG باستخدام Aspose.CAD للـ Java

## المقدمة

إذا كنت بحاجة إلى **تحويل STL إلى PNG** في تطبيق Java، فإن Aspose.CAD للـ Java يجعل المهمة سريعة وموثوقة. في هذا الدرس سنستعرض العملية بالكامل—من إعداد مشروعك إلى حفظ صورة PNG النهائية—حتى تتمكن من دمج تحويل STL في سير عملك بثقة.

## إجابات سريعة
- **ماذا تفعل المكتبة؟** تقوم بتحويل صيغ CAD (بما في ذلك STL) إلى صور نقطية مثل PNG.  
- **ما اللغة المستخدمة؟** Java، باستخدام Aspose.CAD API.  
- **هل أحتاج إلى ترخيص؟** يلزم الحصول على ترخيص مؤقت أو كامل للاستخدام في الإنتاج.  
- **كم يستغرق التنفيذ؟** حوالي 10‑15 دقيقة لتحويل أساسي.  
- **هل يمكنني تخصيص حجم الصورة؟** نعم، عبر `CadRasterizationOptions`.

## ما هو تحويل STL إلى PNG؟

تحويل STL إلى PNG يحول ملف شبكة ثلاثية الأبعاد (STL) إلى صورة نقطية ثنائية الأبعاد (PNG). هذا مفيد عندما تحتاج إلى معاينة بصرية سريعة، أو إنشاء صور مصغرة، أو تضمين النموذج في صفحات الويب دون الحاجة إلى عارض ثلاثي الأبعاد.

## لماذا تستخدم Aspose.CAD للـ Java؟

- **API كامل المميزات** – يدعم العديد من صيغ CAD، ليس فقط STL.  
- **بدون تبعيات خارجية** – جافا صافية، سهل إضافتها إلى أي مشروع Maven/Gradle.  
- **إخراج نقطي عالي الجودة** – تحكم في الدقة، الخلفية، وإزالة التعرجات.  
- **يدعم سيناريوهات “كيفية تصدير STL”** – مثالي للمعالجة الدفعية أو التحويلات الفورية.

## المتطلبات المسبقة

قبل أن تبدأ، تأكد من أن لديك:

- مجموعة تطوير جافا (JDK) مثبتة على جهازك.  
- مكتبة Aspose.CAD للـ Java تم تنزيلها. يمكنك الحصول عليها [هنا](https://releases.aspose.com/cad/java/).  
- ترخيص صالح أو ترخيص مؤقت من [هنا](https://purchase.aspose.com/temporary-license/).

## استيراد الحزم

في مشروع Java الخاص بك، استورد الفئات اللازمة:

```java
import com.aspose.cad.Image;

import com.aspose.cad.fileformats.dgn.DgnImage;
import com.aspose.cad.imageoptions.CadRasterizationOptions;
import com.aspose.cad.fileformats.cad.CadImage;
import com.aspose.cad.imageoptions.CadRasterizationOptions;
import com.aspose.cad.imageoptions.PngOptions;
```

الآن، دعنا نقسم المثال إلى عدة خطوات.

## الخطوة 1: إعداد مشروعك

أنشئ مشروع Java جديد وأضف مكتبة Aspose.CAD للـ Java إلى تبعيات مشروعك (Maven أو Gradle أو إضافة JAR يدويًا).

## الخطوة 2: تحديد ملف STL الخاص بك

حدد المسار إلى ملف STL الذي تريد تحويله:

```java
String dataDir = "Your Document Directory" + "ExportingSTL/";
String fileName = dataDir + "example.stl";
```

## الخطوة 3: تحميل ملف STL

حمّل ملف STL باستخدام طريقة `Image.load`. هذا ينشئ كائن **صورة CAD** يمكنك تحويله إلى نقطية:

```java
CadImage cadImage = (CadImage)Image.load(fileName);
```

## الخطوة 4: تكوين خيارات التحويل إلى نقطية

قم بإعداد خيارات التحويل إلى نقطية للتحكم في حجم وجودة صورة PNG الناتجة. هذه الخيارات هي جزء من عملية تحويل **cad image to png**:

```java
CadRasterizationOptions vectorOptions = new CadRasterizationOptions();
vectorOptions.setPageWidth(1500);
vectorOptions.setPageHeight(1500);
```

## الخطوة 5: تكوين خيارات PNG

أنشئ مثيلًا من `PngOptions`. إذا كنت تريد تطبيق إعدادات التحويل إلى نقطية، ألغِ التعليق عن السطر أدناه:

```java
PngOptions pngOptions = new PngOptions();
// Uncomment the line below if you want to set vector rasterization options
// pngOptions.setVectorRasterizationOptions(vectorOptions);
```

## الخطوة 6: حفظ كـ PNG

أخيرًا، صدّر صورة CAD إلى ملف PNG—هذه هي خطوة **save PNG Java**:

```java
String outPath = dataDir + "galeon.stl.png";
cadImage.save(outPath, pngOptions);
```

> **نصيحة احترافية:** اضبط `PageWidth` و `PageHeight` لتتناسب مع أبعاد الصورة المصغرة المطلوبة للحصول على معالجة أسرع.

تهانينا! لقد نجحت في **تحويل ملف STL إلى PNG** باستخدام Aspose.CAD للـ Java.

## المشكلات الشائعة والحلول

| المشكلة | السبب | الحل |
|-------|--------|----------|
| مخرجات PNG فارغة | لم يتم ضبط خيارات التحويل إلى نقطية | ألغِ التعليق عن `pngOptions.setVectorRasterizationOptions(vectorOptions);` أو حدد لون خلفية |
| OutOfMemoryError في ملفات STL الكبيرة | نقص في ذاكرة الـ heap | زد حجم heap للـ JVM (`-Xmx2g`) أو عالج الملف على دفعات |
| LicenseException | لا يوجد ترخيص صالح | طبّق ترخيصًا مؤقتًا أو مُشتَرًى قبل تحميل الصورة |

## الأسئلة المتكررة

### س1: هل Aspose.CAD للـ Java متوافق مع جميع إصدارات ملفات STL؟
A1: يدعم Aspose.CAD للـ Java إصدارات مختلفة من ملفات STL، مما يضمن التوافق مع معظم الصيغ الشائعة.

### س2: هل يمكنني استخدام Aspose.CAD للـ Java في مشروع تجاري؟
A2: نعم، يمكنك ذلك. فقط احصل على ترخيص صالح من [هنا](https://purchase.aspose.com/buy).

### س3: هل أحتاج إلى ترخيص مؤقت للتجربة المجانية؟
A3: لا، لا يلزم ترخيص مؤقت للتجربة المجانية. يمكنك البدء فورًا بإصدار التجربة [هنا](https://releases.aspose.com/).

### س4: أين يمكنني العثور على دعم إضافي أو طرح أسئلة؟
A4: زر منتدى Aspose.CAD [هنا](https://forum.aspose.com/c/cad/19) لأي دعم أو استفسارات.

### س5: هل هناك وثائق شاملة متاحة؟
A5: نعم، يمكن العثور على الوثائق [هنا](https://reference.aspose.com/cad/java/).

## الخاتمة

في هذا الدليل شرحنا كيفية **تحويل STL إلى PNG** بفعالية باستخدام Aspose.CAD للـ Java. باتباع الخطوات أعلاه، يمكنك دمج تحويل STL إلى PNG في أي خط أنابيب مبني على Java، سواء كنت تبني أداة سطح مكتب، خدمة ويب، أو أداة تقارير آلية.

---

**آخر تحديث:** 2026-02-20  
**تم الاختبار مع:** Aspose.CAD for Java 24.12 (latest at time of writing)  
**المؤلف:** Aspose  

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}