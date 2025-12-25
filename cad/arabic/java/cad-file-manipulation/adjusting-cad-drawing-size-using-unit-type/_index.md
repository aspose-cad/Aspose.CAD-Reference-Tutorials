---
date: 2025-12-25
description: تعلم كيفية تصدير DWG إلى BMP باستخدام Aspose.CAD للغة Java. يوضح هذا
  الدليل خطوة بخطوة تعديل حجم الرسم الهندسي وتحويل CAD إلى BMP بكفاءة.
linktitle: Adjusting CAD Drawing Size Using Unit Type
second_title: Aspose.CAD Java API
title: تصدير DWG إلى BMP – تعديل حجم CAD باستخدام نوع الوحدة (Java)
url: /ar/java/cad-file-manipulation/adjusting-cad-drawing-size-using-unit-type/
weight: 14
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# تصدير DWG إلى BMP – تعديل حجم رسم CAD باستخدام نوع الوحدة مع Aspose.CAD للـ Java

## المقدمة

عند الحاجة إلى **export DWG to BMP**، يكون التحكم في حجم الإخراج ووحدة القياس أمرًا أساسيًا للمعالجة اللاحقة أو الطباعة. في هذا الدرس ستتعلم كيفية تعديل حجم رسم CAD وتحويل CAD إلى BMP باستخدام Aspose.CAD للـ Java، عبر خاصية `UnitType` لتحديد وحدة القياس. تم شرح الخطوات بلغة بسيطة لتتمكن من المتابعة حتى وإن كنت جديدًا على المكتبة.

## إجابات سريعة
- **ماذا يعني “export DWG to BMP”؟** تحويل رسم DWG إلى صورة نقطية BMP.  
- **أي خاصية تتحكم في حجم الإخراج؟** `CadRasterizationOptions.setUnitType()` تحدد الوحدة (مثل السنتيمتر).  
- **هل أحتاج إلى ترخيص لتشغيل الكود؟** النسخة التجريبية المجانية تكفي للتقييم؛ الترخيص مطلوب للإنتاج.  
- **هل يمكنني اختيار تخطيطات أخرى؟** نعم، استخدم `setLayouts()` لتحديد تخطيطات النموذج أو مساحة الورق.  
- **ما هي صيغ الإخراج المدعومة؟** بالإضافة إلى BMP، يمكنك التصدير إلى PNG، JPEG، TIFF، إلخ، عبر تغيير فئة الخيارات.

## ما هو **export DWG to BMP**؟

تصدير DWG إلى BMP يعني تحويل ملف DWG المستند إلى المتجهات إلى صورة نقطية (BMP). هذا مفيد عندما تحتاج إلى تمثيل بدقة البكسل للأنظمة القديمة، أو خطوط معالجة الصور، أو سيناريوهات العرض البسيطة.

## لماذا تعديل حجم رسم CAD باستخدام **Unit Type**؟

تعيين نوع الوحدة يتيح لك التحكم في الأبعاد الفعلية للصورة المصدرة دون الحاجة لحساب عوامل التحجيم يدويًا. هذا يضمن أن الصورة النقطية تتطابق مع القياسات الواقعية (مثل السنتيمترات)، وهو أمر حاسم للرسومات الهندسية والوثائق المطبوعة.

## المتطلبات المسبقة

قبل الغوص في الدرس، تأكد من توفر المتطلبات التالية:

- **بيئة تطوير جافا** – JDK فعال (8 أو أحدث) وIDE أو أداة بناء (Maven/Gradle).  
- **مكتبة Aspose.CAD للـ Java** – قم بتحميل وتكامل مكتبة Aspose.CAD في مشروعك الجافا. يمكنك الحصول على المكتبة [هنا](https://releases.aspose.com/cad/java/).

## استيراد المساحات الاسمية

في كود الجا الخاص بك، أدرج المساحات الاسمية اللازمة للوصول إلى وظائف Aspose.CAD. أضف الاستيرادات التالية:

```java
import com.aspose.cad.Image;
import com.aspose.cad.ImageOptionsBase;

import com.aspose.cad.imageoptions.CadRasterizationOptions;
import com.aspose.cad.imageoptions.PngOptions;
```

الآن، لنقسم عملية تعديل حجم رسم CAD باستخدام نوع الوحدة إلى خطوات قابلة للإدارة:

## الخطوة 1: تعريف دليل البيانات

```java
String dataDir = "Your Document Directory" + "CADConversion/";
```

حدد المسار للدليل الذي توجد فيه ملفات CAD الخاصة بك.

## الخطوة 2: تحميل رسم CAD

```java
String sourceFilePath = dataDir + "sample.dwg";
Image image = Image.load(sourceFilePath);
```

حمّل رسم CAD باستخدام فئة `Image` من Aspose.CAD.

## الخطوة 3: إنشاء خيارات BMP

```java
BmpOptions bmpOptions = new BmpOptions();
```

أنشئ كائنًا من فئة `BmpOptions` لتصدير تخطيط CAD إلى صيغة BMP.

## الخطوة 4: تكوين خيارات التحويل إلى نقطية

```java
CadRasterizationOptions cadRasterizationOptions = new CadRasterizationOptions();
bmpOptions.setVectorRasterizationOptions(cadRasterizationOptions);
```

أنشئ مثيلًا من `CadRasterizationOptions` واربطه بـ `BmpOptions` للتحويل من المتجه إلى نقطية.

## الخطوة 5: تعيين نوع الوحدة

```java
cadRasterizationOptions.setUnitType(UnitType.Centimeter);
```

حدد نوع الوحدة المطلوب لرسم CAD. في هذا المثال، تم تعيينه إلى **Centimeter**، مما يؤثر مباشرة على حجم الصورة المصدرة عند **adjust CAD drawing size**.

## الخطوة 6: تعيين التخطيطات

```java
cadRasterizationOptions.setLayouts(new String[] { "Model" });
```

عرّف التخطيطات التي ستؤخذ في الاعتبار أثناء التصدير. في هذه الحالة، اخترنا التخطيط **"Model"**، لكن يمكنك التبديل إلى تخطيطات مساحة الورق إذا لزم الأمر.

## الخطوة 7: التصدير إلى BMP

```java
String outPath = sourceFilePath + ".bmp";
image.save(outPath, bmpOptions);
```

أخيرًا، احفظ رسم CAD المعدل بصيغة BMP. تكمل هذه الخطوة سير عمل **export DWG to BMP** مع الحفاظ على تعديلات الحجم التي قمت بتكوينها.

## المشكلات الشائعة والحلول

| المشكلة | السبب | الحل |
|-------|--------|-----|
| **Output image is too small** | لم يتم تعيين نوع الوحدة أو تم استخدام الافتراضي (بكسل) | استدعِ `setUnitType()` مع الوحدة المطلوبة (مثال: `UnitType.Centimeter`). |
| **Wrong layout exported** | خطأ إملائي في اسم التخطيط | تحقق من أسماء التخطيطات باستخدام عارض CAD؛ استخدم السلسلة الدقيقة في `setLayouts()`. |
| **License exception** | تشغيل بدون ترخيص صالح في بيئة الإنتاج | طبق ترخيصًا مؤقتًا أو دائمًا كما هو موضح في الأسئلة المتكررة. |

## الأسئلة المتكررة (موسعة)

**س: هل يمكنني استخدام Aspose.CAD للـ Java مع لغات برمجة أخرى؟**  
ج: Aspose.CAD يدعم أساسًا Java، لكن هناك إصدارات متاحة للغات أخرى مثل .NET.

**س: هل هناك خيارات ترخيص لـ Aspose.CAD؟**  
ج: نعم، يمكنك استكشاف خيارات الترخيص وشراء Aspose.CAD [هنا](https://purchase.aspose.com/buy).

**س: هل تتوفر نسخة تجريبية مجانية لـ Aspose.CAD؟**  
ج: بالتأكيد، يمكنك الوصول إلى نسخة تجريبية مجانية [هنا](https://releases.aspose.com/).

**س: كيف يمكنني الحصول على دعم لـ Aspose.CAD للـ Java؟**  
ج: زر منتدى Aspose.CAD [هنا](https://forum.aspose.com/c/cad/19) للحصول على دعم شامل.

**س: هل يمكنني الحصول على ترخيص مؤقت لـ Aspose.CAD؟**  
ج: نعم، يمكنك الحصول على ترخيص مؤقت [هنا](https://purchase.aspose.com/temporary-license/).

**آخر تحديث:** 2025-12-25  
**تم الاختبار مع:** Aspose.CAD للـ Java 24.10  
**المؤلف:** Aspose  

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}