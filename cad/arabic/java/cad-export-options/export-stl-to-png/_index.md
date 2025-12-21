---
date: 2025-12-21
description: تعلم كيفية تصدير ملفات STL إلى PNG باستخدام Aspose.CAD للغة Java – دليل
  خطوة بخطوة يبسط عملية تحويل ملفات STL إلى PNG في مشاريع Java الخاصة بك.
linktitle: Export STL to PNG
second_title: Aspose.CAD Java API
title: تصدير STL إلى PNG باستخدام Aspose.CAD للـ Java
url: /ar/java/cad-export-options/export-stl-to-png/
weight: 20
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# تصدير STL إلى PNG باستخدام Aspose.CAD للـ Java

## مقدمة

إذا كنت بحاجة إلى **تصدير stl إلى png** بسرعة وبشكل موثوق في بيئة Java، فإن Aspose.CAD للـ Java هو الأداة المثالية. في هذا الدرس سنستعرض كل ما تحتاجه — من إعداد المشروع إلى حفظ صورة PNG عالية الجودة — حتى تتمكن من دمج الأصول البصرية ثلاثية الأبعاد في تطبيقاتك بثقة.

## إجابات سريعة
- **ماذا يعني “تصدير stl إلى png”؟** يحول نموذج STL ثلاثي الأبعاد إلى صورة PNG نقطية ثنائية الأبعاد.  
- **ما المكتبة التي تتعامل مع التحويل؟** Aspose.CAD للـ Java يوفر دعمًا أصليًا لصيغ STL و PNG.  
- **هل أحتاج إلى ترخيص؟** يلزم وجود ترخيص Aspose.CAD مؤقت أو دائم للاستخدام في الإنتاج.  
- **كم من الوقت تستغرق العملية؟** تقريبًا 10‑15 دقيقة لكتابة سكريبت تحويل أساسي.  
- **هل يمكنني تعديل حجم الصورة؟** نعم – خيارات التحويل إلى نقطية تتيح لك ضبط العرض والارتفاع حسب الحاجة.

## ما هو تصدير stl إلى png؟

يعني تصدير STL إلى PNG أخذ نموذج ثلاثي الأبعاد (STL) وعرضه كصورة مسطحة (PNG). هذا مفيد عندما تريد عرض معاينات، إنشاء صور مصغرة، أو تضمين النماذج في التقارير دون الحاجة إلى عارض ثلاثي الأبعاد.

## لماذا تحويل STL إلى PNG في Java؟

- **التوافق عبر الأنظمة** – PNG يعمل على المتصفحات، تطبيقات الهواتف المحمولة، وواجهات المستخدم المكتبية.  
- **الأداء** – عرض صورة ثابتة أسرع بكثير من تحميل نموذج ثلاثي الأبعاد كامل.  
- **البساطة** – Aspose.CAD يبسط عملية التحويل إلى نقطية المعقدة، مما يتيح لك التركيز على منطق الأعمال.  

## المتطلبات المسبقة

قبل أن تبدأ، تأكد من أن لديك:

- مجموعة تطوير Java (JDK) مثبتة على جهازك.  
- مكتبة Aspose.CAD للـ Java تم تحميلها. يمكنك الحصول عليها [here](https://releases.aspose.com/cad/java/).  
- ترخيص صالح أو ترخيص مؤقت من [here](https://purchase.aspose.com/temporary-license/).  

## استيراد المساحات الاسمية

أضف الفئات المطلوبة من Aspose.CAD إلى ملف المصدر Java الخاص بك:

```java
import com.aspose.cad.Image;

import com.aspose.cad.fileformats.dgn.DgnImage;
import com.aspose.cad.imageoptions.CadRasterizationOptions;
import com.aspose.cad.fileformats.cad.CadImage;
import com.aspose.cad.imageoptions.CadRasterizationOptions;
import com.aspose.cad.imageoptions.PngOptions;
```

هذه الاستيرادات تمنحك إمكانية الوصول إلى تحميل الصور، عملية التحويل إلى نقطية، وخيارات PNG الخاصة.

## دليل خطوة بخطوة

### الخطوة 1: إعداد مشروعك

أنشئ مشروع Java جديد (IDE حسب اختيارك) وأضف ملف JAR الخاص بـ Aspose.CAD إلى مسار الفئات (classpath) للمشروع.

### الخطوة 2: تحديد ملف STL الخاص بك (كيفية تحميل stl)

حدد المجلد الذي يحتوي على نموذج STL الذي تريد تحويله:

```java
String dataDir = "Your Document Directory" + "ExportingSTL/";
String fileName = dataDir + "example.stl";
```

> **نصيحة احترافية:** احتفظ بملفات STL في مجلد موارد مخصص لتجنب مشاكل المسارات.

### الخطوة 3: تحميل ملف STL (تحويل stl إلى png)

استخدم طريقة `Image.load` لقراءة ملف STL إلى كائن `CadImage`:

```java
CadImage cadImage = (CadImage)Image.load(fileName);
```

في هذه المرحلة تكون الهندسة ثلاثية الأبعاد جاهزة للتحويل إلى نقطية.

### الخطوة 4: تكوين خيارات التحويل إلى نقطية (تحويل 3d stl إلى png)

حدد أبعاد الإخراج وإعدادات التحويل الأخرى. اضبط العرض/الارتفاع لتتناسب مع دقة PNG المطلوبة:

```java
CadRasterizationOptions vectorOptions = new CadRasterizationOptions();
vectorOptions.setPageWidth(1500);
vectorOptions.setPageHeight(1500);
```

يمكنك أيضًا تعديل لون الخلفية، وزن الخط، أو مضاد التعرجات هنا.

### الخطوة 5: تكوين خيارات PNG (تحويل stl إلى png في Java)

أنشئ كائن `PngOptions` و (اختياريًا) اربط به خيارات التحويل إلى نقطية:

```java
PngOptions pngOptions = new PngOptions();
// Uncomment the line below if you want to set vector rasterization options
// pngOptions.setVectorRasterizationOptions(vectorOptions);
```

ترك السطر معلقًا يستخدم الإعدادات الافتراضية للتحويل إلى نقطية، وهي كافية لمعظم الحالات.

### الخطوة 6: حفظ كـ PNG

أخيرًا، احفظ الصورة المرسومة إلى القرص:

```java
String outPath = dataDir + "galeon.stl.png";
cadImage.save(outPath, pngOptions);
```

الآن لديك تمثيل PNG لنموذج STL الأصلي جاهز للاستخدام في مكونات الواجهة، صفحات الويب، أو الوثائق.

## المشكلات الشائعة والحلول

| المشكلة | السبب | الحل |
|-------|-------|-----|
| **إخراج PNG فارغ** | لم يتم ضبط خيارات التحويل إلى نقطية أو الحجم صفر | تأكد من أن `setPageWidth` و `setPageHeight` قيمهما موجبة. |
| **OutOfMemoryError** | ملفات STL كبيرة جدًا | زيادة حجم الذاكرة المخصصة للـ JVM (`-Xmx`) أو تقليل أبعاد الصورة. |
| **License not found** | ملف الترخيص مفقود أو غير صحيح | ضع ملف الترخيص في مسار الفئات (classpath) وحمله قبل أي استدعاءات لـ Aspose. |

## الخلاصة

لقد تعلمت بنجاح كيفية **تصدير stl إلى png** باستخدام Aspose.CAD للـ Java. يسمح لك هذا سير العمل بإنشاء معاينات PNG عالية الجودة من أي نموذج STL، مما يبسط مهام التصور في التطبيقات المبنية على Java.

## الأسئلة المتكررة

### س1: هل Aspose.CAD للـ Java متوافق مع جميع إصدارات ملفات STL؟

ج1: يدعم Aspose.CAD للـ Java إصدارات مختلفة من ملفات STL، مما يضمن التوافق مع معظم الصيغ الشائعة.

### س2: هل يمكنني استخدام Aspose.CAD للـ Java في مشروع تجاري؟

ج2: نعم، يمكنك ذلك. فقط احصل على ترخيص صالح من [here](https://purchase.aspose.com/buy).

### س3: هل أحتاج إلى ترخيص مؤقت للتجربة المجانية؟

ج3: لا، لا يلزم ترخيص مؤقت للتجربة المجانية. يمكنك البدء فورًا بالإصدار التجريبي [here](https://releases.aspose.com/).

### س4: أين يمكنني العثور على دعم إضافي أو طرح أسئلة؟

ج4: زر منتدى Aspose.CAD [here](https://forum.aspose.com/c/cad/19) لأي دعم أو استفسارات.

### س5: هل هناك وثائق شاملة متاحة؟

ج5: نعم، يمكن العثور على الوثائق [here](https://reference.aspose.com/cad/java/).

## الأسئلة المتكررة

**س: كيف يمكنني التحكم في لون خلفية PNG المُصدّر؟**  
ج: استخدم `vectorOptions.setBackgroundColor(Color.getWhite())` قبل تعيين الخيارات إلى `pngOptions`.

**س: هل يمكنني تصدير ملفات STL متعددة في عملية دفعة؟**  
ج: بالتأكيد – ضع منطق التحويل داخل حلقة تتكرر على قائمة مسارات الملفات.

**س: هل يحتفظ PNG بالشفافية؟**  
ج: نعم، يدعم PNG قناة ألفا؛ يمكنك تمكينها عبر `pngOptions.setTransparent(true)` إذا لزم الأمر.

**س: هل من الممكن التصدير إلى صيغ نقطية أخرى (مثل JPEG، BMP)؟**  
ج: يدعم Aspose.CAD العديد من الصيغ النقطية؛ فقط استخدم `JpegOptions`، `BmpOptions`، إلخ، بدلاً من `PngOptions`.

**س: ما هو إصدار Aspose.CAD المطلوب لدعم STL؟**  
ج: دعم STL متاح منذ Aspose.CAD 20.x؛ استخدام أحدث إصدار يضمن التوافق الكامل.

---

**آخر تحديث:** 2025-12-21  
**تم الاختبار مع:** Aspose.CAD للـ Java 24.12  
**المؤلف:** Aspose  

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}