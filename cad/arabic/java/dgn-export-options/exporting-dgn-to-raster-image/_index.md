---
date: 2026-01-10
description: تعلم كيفية إنشاء ملفات JPEG من ملفات DGN باستخدام Aspose.CAD للغة Java.
  يوضح لك هذا الدليل خطوة بخطوة كيفية تحويل DGN إلى JPEG بكفاءة.
linktitle: Exporting DGN in AutoCAD Format to Raster Image Format
second_title: Aspose.CAD Java API
title: كيفية إنشاء JPEG من DGN باستخدام Aspose.CAD للـ Java
url: /ar/java/dgn-export-options/exporting-dgn-to-raster-image/
weight: 13
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# إنشاء JPEG من DGN باستخدام Aspose.CAD للـ Java

## مقدمة

في هذا الدليل الشامل ستقوم **بإنشاء JPEG من DGN** باستخدام بضع أسطر فقط من كود Java. سواءً كنت تبني أداة تحويل دفعات أو تحتاج إلى عرض رسومات CAD كصور صديقة للويب، فإن تحويل DGN إلى JPEG هو طلب شائع في العديد من سير عمل الهندسة والتصميم. سنستعرض كل خطوة — من إعداد مكتبة Aspose.CAD إلى حفظ الصورة النقطية النهائية — حتى تتمكن من دمج الحل في تطبيقاتك فورًا.

## إجابات سريعة
- **ما المكتبة المطلوبة؟** Aspose.CAD للـ Java  
- **هل يمكنني تحويل صيغ CAD أخرى إلى JPEG؟** نعم، يدعم Aspose.CAD العديد من الصيغ (انظر الكلمة المفتاحية الثانوية *convert cad to jpeg*)  
- **هل أحتاج إلى ترخيص للإنتاج؟** الترخيص التجاري مطلوب للاستخدام غير التجريبي  
- **ما نسخة Java المدعومة؟** Java 8 أو أحدث  
- **كم يستغرق التحويل النموذجي؟** عادةً أقل من ثانية للرسومات ذات الحجم القياسي  

## ما هو “إنشاء JPEG من DGN”؟
إنشاء JPEG من ملف DGN يعني تحويل الرسم القائم على المتجهات DGN إلى صورة مبنية على البكسل (JPEG). تحافظ هذه العملية على الدقة البصرية مع إنتاج ملف خفيف يمكن عرضه في المتصفحات أو البريد الإلكتروني أو التقارير دون الحاجة إلى برنامج CAD.

## لماذا تحويل DGN إلى JPEG؟
- **سهولة المشاركة:** يمكن عرض ملفات JPEG على أي جهاز.  
- **الأداء:** الصور النقطية تُحمَّل أسرع في صفحات الويب مقارنةً بملفات CAD المتجهية.  
- **التوافق:** العديد من الأدوات اللاحقة (مثل محركات التقارير) تقبل فقط الصيغ النقطية.  

## المتطلبات المسبقة

قبل البدء، تأكد من وجود ما يلي:

1. **Aspose.CAD Library** – قم بتنزيلها من الموقع الرسمي **[here](https://releases.aspose.com/cad/java/)**.  
2. **Java Development Kit (JDK)** – Java 8 أو أحدث مثبت على جهازك.  
3. **IDE** – أي بيئة تطوير متوافقة مع Java مثل IntelliJ IDEA أو Eclipse.

## استيراد الحزم

أضف الاستيرادات المطلوبة إلى فئة Java الخاصة بك:

```java
import java.io.FileNotFoundException;
import java.io.FileOutputStream;
import java.io.OutputStream;
import com.aspose.cad.Image;
import com.aspose.cad.ImageOptionsBase;
import com.aspose.cad.fileformats.dgn.DgnImage;
import com.aspose.cad.imageoptions.CadRasterizationOptions;
import com.aspose.cad.imageoptions.JpegOptions;
```

## دليل خطوة بخطوة

### الخطوة 1: تحميل ملف DGN

```java
String dataDir = "Your Document Directory" + "ExportingDGN/";
DgnImage dgnImage = (DgnImage) Image.load(dataDir + "Nikon_D90_Camera.dgn");
```

*شرح:* طريقة `Image.load` تقرأ ملف DGN المصدر وتعيد كائن `DgnImage` يمكننا تحويله إلى نقطية لاحقًا.

### الخطوة 2: إنشاء كائن JpegOptions

```java
ImageOptionsBase options = new JpegOptions();
```

*شرح:* `JpegOptions` تخبر Aspose.CAD أن صيغة الإخراج يجب أن تكون JPEG. كما تسمح لنا بإرفاق إعدادات التحويل إلى نقطية.

### الخطوة 3: تكوين إعدادات التحويل إلى نقطية

```java
CadRasterizationOptions vectorOptions = new CadRasterizationOptions();
vectorOptions.setPageWidth(600);
vectorOptions.setPageHeight(400);
vectorOptions.setNoScaling(true);
vectorOptions.setAutomaticLayoutsScaling(false);
options.setVectorRasterizationOptions(vectorOptions);
```

*شرح:* هذه الخيارات تحدد حجم الصورة الناتجة وتتحكم في سلوك التحجيم. عدّل `PageWidth` و `PageHeight` لتتناسب مع الدقة المستهدفة.

### الخطوة 4: حفظ الصورة المحوّلة

```java
OutputStream outStream = new FileOutputStream(dataDir + "ExportDGNToRasterImage_Out.jpg");
dgnImage.save(outStream, options);
```

*شرح:* طريقة `save` تكتب ملف JPEG النقطي إلى تدفق الإخراج المحدد. بعد هذه الخطوة ستحصل على ملف JPEG جاهز للاستخدام.

> **نصيحة احترافية:** ضع كود التحويل داخل كتلة `try‑with‑resources` لضمان إغلاق التدفقات تلقائيًا.

## حالات الاستخدام الشائعة

- **إنشاء صور مصغرة** لمتصفحات ملفات CAD.  
- **إدراج الرسومات** في تقارير PDF أو صفحات HTML.  
- **معالجة دفعات تلقائية** لأرشيفات التصميم.

## استكشاف الأخطاء وإصلاحها والمشكلات الشائعة

| المشكلة | السبب | الحل |
|--------|-------|------|
| صورة ناتجة فارغة أو بيضاء | إعدادات التحويل إلى نقطية غير صحيحة (مثل تعيين `NoScaling` إلى true مع حجم صفحة غير متطابق) | عدّل `PageWidth`/`PageHeight` أو اضبط `NoScaling` إلى false |
| خطأ نفاد الذاكرة للملفات الكبيرة DGN | تحميل ملفات ضخمة جدًا دون تدفق | زد حجم heap لـ JVM (`-Xmx`) أو عالج الملفات على أجزاء أصغر |
| جودة JPEG غير كافية | جودة JPEG الافتراضية منخفضة | استخدم `((JpegOptions)options).setQuality(100);` قبل الحفظ |

## الأسئلة المتكررة

### س1: هل يمكنني استخدام Aspose.CAD للـ Java مع صيغ ملفات CAD أخرى؟

نعم، يدعم Aspose.CAD مجموعة واسعة من الصيغ، مما يتيح لك **تحويل CAD إلى JPEG** والعديد من المخرجات النقطية أو المتجهة الأخرى.

### س2: هل هناك نسخة تجريبية مجانية متاحة لـ Aspose.CAD للـ Java؟

نعم، يمكنك الوصول إلى نسخة تجريبية مجانية **[هنا](https://releases.aspose.com/)**.

### س3: أين يمكنني العثور على الوثائق الخاصة بـ Aspose.CAD للـ Java؟

راجع الوثائق **[هنا](https://reference.aspose.com/cad/java/)**.

### س4: كيف يمكنني الحصول على الدعم لـ Aspose.CAD للـ Java؟

قم بزيارة منتدى الدعم **[هنا](https://forum.aspose.com/c/cad/19)**.

### س5: أين يمكنني شراء ترخيص لـ Aspose.CAD للـ Java؟

يمكنك شراء الترخيص **[هنا](https://purchase.aspose.com/buy)**.

## الخلاصة

لقد تعلمت الآن كيفية **إنشاء JPEG من DGN** باستخدام Aspose.CAD للـ Java. باتباع الخطوات أعلاه، يمكنك دمج تحويل DGN إلى JPEG بسلاسة في أي تطبيق Java، سواءً لأدوات سطح المكتب أو خدمات الويب أو خطوط الأنابيب الآلية.

---

**آخر تحديث:** 2026-01-10  
**تم الاختبار مع:** Aspose.CAD للـ Java 24.11 (أحدث نسخة وقت الكتابة)  
**المؤلف:** Aspose  

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}