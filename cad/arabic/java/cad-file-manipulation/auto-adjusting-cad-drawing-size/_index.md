---
date: 2025-12-22
description: تعلم كيفية تصدير رسومات CAD وتحويل DWG إلى BMP في Java باستخدام Aspose.CAD.
  اتبع هذا الدليل خطوة بخطوة للتعامل الفعال مع ملفات CAD.
linktitle: Auto Adjusting CAD Drawing Size
second_title: Aspose.CAD Java API
title: كيفية تصدير رسم CAD إلى BMP باستخدام Aspose.CAD للـ Java
url: /ar/java/cad-file-manipulation/auto-adjusting-cad-drawing-size/
weight: 13
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# كيفية تصدير رسم CAD إلى BMP باستخدام Aspose.CAD للـ Java

## المقدمة

إذا كنت تبحث عن طريقة واضحة وموثوقة **كيفية تصدير cad** من Java، فقد وجدت المكان المناسب. مع Aspose.CAD للـ Java يمكنك ليس فقط تعديل أحجام الرسومات تلقائيًا بل أيضًا **تحويل DWG إلى BMP** ببضع أسطر من الشيفرة. يشرح هذا الدليل العملية بالكامل، من إعداد بيئتك إلى إنشاء صورة BMP تحافظ على تخطيط CAD الأصلي.

## إجابات سريعة
- **ماذا يعني “كيفية تصدير cad”؟** يشير إلى تحويل ملفات CAD (DWG، DXF، إلخ) إلى صيغة أخرى مثل BMP أو PNG أو PDF.  
- **أي مكتبة تتولى التحويل؟** Aspose.CAD للـ Java توفر واجهة برمجة تطبيقات بسيطة لهذا الغرض.  
- **هل أحتاج إلى ترخيص؟** الترخيص المؤقت يكفي للاختبار؛ الترخيص الكامل مطلوب للإنتاج.  
- **هل يمكنني تصدير عدة تخطيطات مرة واحدة؟** نعم – عن طريق ضبط خاصية `Layouts` يمكنك تحديد التخطيطات التي تريد رسمها.  
- **هل BMP هو الصيغة الوحيدة المتاحة؟** لا – يمكنك أيضًا التصدير إلى PNG، JPEG، TIFF، وغيرها.

## ما هو “كيفية تصدير cad” باستخدام Aspose.CAD؟
يعني تصدير CAD أخذ رسم CAD أصلي (مثل ملف DWG) وتحويله إلى صورة نقطية أو صيغة متجهة أخرى. تتولى Aspose.CAD كل الأعمال الصعبة: تحليل بنية CAD، تحويل الكيانات المتجهة إلى نقطية، وكتابة النتيجة إلى صيغة الصورة التي تختارها.

## لماذا نستخدم Aspose.CAD للـ Java **لتحويل DWG إلى BMP**؟
- **بدون تبعيات خارجية** – جافا صافية، لا ملفات DLL أصلية.  
- **دعم كامل لـ DWG، DXF، DGN، وغيرها من الصيغ**.  
- **تحكم دقيق** في خيارات التحويل مثل اختيار التخطيط، التحجيم، ولون الخلفية.  
- **أداء عالي** مناسب للمعالجة الدفعة على الخوادم.

## المتطلبات المسبقة

قبل أن تبدأ، تأكد من توفر ما يلي:

1. **مجموعة تطوير جافا (JDK)** – حمّلها [من هنا](https://www.java.com/en/download/).  
2. **مكتبة Aspose.CAD للـ Java** – احصل على أحدث ملف JAR من [هنا](https://releases.aspose.com/cad/java/).  
3. **ملف CAD تجريبي** – ملف DWG (مثال: `sample.dwg`) موجود في دليل المستندات داخل مشروعك.

## استيراد المساحات الاسمية

في تطبيق Java الخاص بك، أدرج المساحات الاسمية اللازمة لاستخدام وظائف Aspose.CAD. إليك مثالاً:

```java

import com.aspose.cad.Image;
import com.aspose.cad.ImageOptionsBase;

import com.aspose.cad.imageoptions.CadRasterizationOptions;
import com.aspose.cad.imageoptions.PngOptions;
```

الآن، لنقسّم عملية **كيفية تصدير cad** إلى خطوات يمكن التحكم فيها.

## دليل خطوة بخطوة

### الخطوة 1: تحميل رسم CAD

```java
String dataDir = "Your Document Directory" + "CADConversion/";
String sourceFilePath = dataDir + "sample.dwg";
Image objImage = Image.load(sourceFilePath);
```

نحمّل ملف DWG المصدر إلى كائن `Image`، وهو نقطة الدخول لجميع العمليات اللاحقة.

### الخطوة 2: إنشاء `BmpOptions`

```java
BmpOptions bmpOptions = new BmpOptions();
```

ستحتوي `BmpOptions` على إعدادات التحويل الخاصة بإخراج BMP.

### الخطوة 3: ضبط إعدادات التحويل

```java
CadRasterizationOptions cadRasterizationOptions = new CadRasterizationOptions();
bmpOptions.setVectorRasterizationOptions(cadRasterizationOptions);
```

هنا نربط خيارات التحويل بخيارات BMP، مما يتيح لنا التحكم في طريقة رسم كيانات CAD.

### الخطوة 4: تحديد التخطيط(ات) للتصدير

```java
cadRasterizationOptions.setLayouts(new String[]{"Model"});
```

خاصية `Layouts` تخبر Aspose.CAD أي تخطيطات الرسم يجب تضمينها. في معظم الحالات، يكون `"Model"` هو التخطيط الأساسي الذي تريد تحويله.

### الخطوة 5: التصدير إلى صيغة BMP

```java
String outPath = sourceFilePath + ".bmp";
objImage.save(outPath, bmpOptions);
```

استدعاء `save` مع `BmpOptions` المضبوطة يكتب ملف BMP إلى القرص. هذا يكمل سير عمل **تحويل DWG إلى BMP**.

## المشكلات الشائعة والحلول

| المشكلة | السبب | الحل |
|--------|-------|------|
| صورة الإخراج فارغة | اسم التخطيط غير صحيح أو التخطيط مفقود | تأكد من أن اسم التخطيط يطابق ملف CAD (مثال: `"Model"`). |
| دقة منخفضة | DPI الافتراضي منخفض | اضبط `cadRasterizationOptions.setResolution(300);` قبل الحفظ. |
| خطأ نفاد الذاكرة للملفات الكبيرة | الرسومات الكبيرة تحتاج مساحة heap أكبر | زد حجم heap للـ JVM (`-Xmx2g`) أو عالج الصفحات بشكل منفصل. |

## الأسئلة المتكررة

**س: هل Aspose.CAD متوافق مع صيغ CAD المختلفة؟**  
ج: نعم، يدعم Aspose.CAD صيغ DWG، DXF، DGN، والعديد من الصيغ الأخرى.

**س: هل يمكنني استخدام Aspose.CAD في مشاريع تجارية؟**  
ج: بالطبع. يمكنك شراء ترخيص [من هنا](https://purchase.aspose.com/buy) للاستخدام في الإنتاج.

**س: كيف أحصل على ترخيص مؤقت للاختبار؟**  
ج: يمكنك الحصول على ترخيص مؤقت [من هنا](https://purchase.aspose.com/temporary-license/).

**س: أين يمكنني العثور على دعم المجتمع؟**  
ج: انضم إلى منتدى مجتمع Aspose.CAD على [forum](https://forum.aspose.com/c/cad/19).

**س: هل هناك نسخة تجريبية مجانية متاحة لـ Aspose.CAD للـ Java؟**  
ج: نعم، حمّل النسخة التجريبية المجانية [من هنا](https://releases.aspose.com/).

## الخاتمة

في هذا الدليل أظهرنا **كيفية تصدير cad** من Java و**تحويل DWG إلى BMP** باستخدام Aspose.CAD. باتباع الخطوات الخمس أعلاه، يمكنك دمج تحويل CAD إلى صورة في أي تطبيق Java، سواء كان أداة سطح مكتب، خدمة ويب، أو خط معالجة دفعي. استكشف صيغ إخراج أخرى (PNG، JPEG، PDF) بتغيير فئة الخيارات، واستفد من مجموعة الميزات الغنية في Aspose.CAD لتلبية جميع احتياجاتك في معالجة CAD.

---

**آخر تحديث:** 2025-12-22  
**تم الاختبار مع:** Aspose.CAD للـ Java 24.12  
**المؤلف:** Aspose  

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}