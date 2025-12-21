---
date: 2025-12-21
description: تعلم كيفية تحويل DWG إلى PDF عن طريق تصدير تخطيط DWG محدد إلى PDF باستخدام
  Aspose.CAD للغة Java. اتبع هذا الدليل خطوة بخطوة لتحويل DWG إلى PDF لتبسيط سير عمل
  CAD الخاص بك.
linktitle: Export Specific DWG Layout to PDF
second_title: Aspose.CAD Java API
title: تحويل DWG إلى PDF – تصدير التخطيط باستخدام Aspose.CAD للغة Java
url: /ar/java/cad-drawing-conversion/export-specific-dwg-layout-to-pdf/
weight: 14
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# تحويل DWG إلى PDF – تصدير تخطيط محدد باستخدام Aspose.CAD للـ Java

## المقدمة

في عالم التصميم بمساعدة الحاسوب (CAD) المتطور، يُعد **convert DWG to PDF** مطلبًا شائعًا عند مشاركة الرسومات مع العملاء أو المقاولين أو أصحاب المصلحة غير التقنيين. تجعل Aspose.CAD للـ Java هذا التحويل سهلًا، وتتيح لك أيضًا اختيار تخطيط واحد من ملف DWG يحتوي على عدة تخطيطات. في هذا الدرس سنستعرض **كيفية تصدير تخطيطات DWG** المحددة إلى PDF، حتى تتمكن من تقديم ما يحتاجه مشروعك بالضبط دون صفحات إضافية أو قص يدوي.

## إجابات سريعة
- **ماذا يعني “convert DWG to PDF”?** إنه يحول رسم DWG إلى مستند PDF، مع الحفاظ على بيانات المتجهات ودقة التخطيط.  
- **ما المكتبة التي تتعامل مع التحويل؟** توفر Aspose.CAD للـ Java واجهة برمجة تطبيقات جاهزة للاستخدام.  
- **هل أحتاج إلى ترخيص للإنتاج؟** نعم، يلزم الحصول على ترخيص تجاري؛ نسخة التجربة المجانية تكفي للتقييم.  
- **هل يمكنني اختيار تخطيط واحد؟** بالتأكيد – قم بتعيين خاصية `Layouts` إلى اسم التخطيط المطلوب.  
- **ما نسخة Java المدعومة؟** Java 8 وما بعدها متوافقة تمامًا.

## المتطلبات المسبقة

- **بيئة تطوير Java** – JDK 8+ ومحرّك التطوير المفضل لديك.  
- **مكتبة Aspose.CAD** – حمّل أحدث ملف JAR من الموقع الرسمي **[هنا](https://releases.aspose.com/cad/java/)**.  
- **ملف DWG** – رسم يحتوي على تخطيط واحد على الأقل (مثال: *visualization_-_conference_room.dwg*).  

## لماذا تصدير تخطيط DWG محدد إلى PDF؟

تحتوي العديد من ملفات DWG على مساحات ورقية متعددة (تخطيطات). قد يؤدي تصدير الملف بالكامل إلى إنشاء PDF كبير يحتوي على صفحات غير مرغوب فيها. اختيار تخطيط واحد:

- يقلل من حجم الملف.  
- يركز انتباه المشاهد على ورقة الرسم ذات الصلة.  
- يتماشى مع معايير توثيق المشروع.  

## دليل خطوة بخطوة

### الخطوة 1: إعداد بيئة المشروع

أنشئ مشروع Java جديد (Maven أو Gradle أو IDE عادي) وأضف ملف JAR الخاص بـ Aspose.CAD إلى مسار الفئات (classpath). يمكنك تحميله **[هنا](https://releases.aspose.com/cad/java/)**.

### الخطوة 2: استيراد الحزم الضرورية

أضف مساحات الأسماء المطلوبة من Aspose.CAD إلى فئة Java الخاصة بك.

```java
import com.aspose.cad.Image;
import com.aspose.cad.imageoptions.CadRasterizationOptions;
import com.aspose.cad.imageoptions.PdfOptions;
```

### الخطوة 3: تحميل ملف DWG

حدد موقع ملف DWG الذي تريد تحويله وحمّله في كائن `Image`.

```java
String srcFile = dataDir + "visualization_-_conference_room.dwg";
Image image = Image.load(srcFile);
```

### الخطوة 4: تكوين خيارات التحويل إلى نقطية

حدد حجم الصفحة، وبشكل أساسي، التخطيط الذي ترغب في تصديره.

```java
CadRasterizationOptions rasterizationOptions = new CadRasterizationOptions();
rasterizationOptions.setPageWidth(1600);
rasterizationOptions.setPageHeight(1600);
// Specify desired layout name
rasterizationOptions.setLayouts(new String[] {"Layout1"});
```

### الخطوة 5: تعيين خيارات تصدير PDF

ربط إعدادات التحويل إلى نقطية بمصدّر PDF.

```java
PdfOptions pdfOptions = new PdfOptions();
pdfOptions.setVectorRasterizationOptions(rasterizationOptions);
```

### الخطوة 6: تصدير DWG إلى PDF

احفظ النتيجة كملف PDF. سيحتوي الناتج على **Layout1** فقط، محققًا عملية **convert DWG to PDF** نظيفة.

```java
image.save(dataDir + "ExportSpecificLayoutToPDF_out_.pdf", pdfOptions);
```

## المشكلات الشائعة والحلول

| المشكلة | لماذا يحدث | الحل |
|-------|----------------|-----|
| **التخطيط غير موجود** | اسم التخطيط مكتوب بشكل خاطئ أو غير موجود في ملف DWG. | استخدم `image.getLayoutNames()` لسرد التخطيطات المتاحة، ثم اختر الصحيح. |
| **PDF بدقة منخفضة** | `PageWidth`/`PageHeight` صغيرة جدًا. | قم بزيادة الأبعاد (مثال: 2000 × 2000) أو اضبط `rasterizationOptions.setResolution(300);`. |
| **استثناء الترخيص** | التشغيل بدون ترخيص صالح في بيئة غير تجريبية. | قم بتطبيق ترخيص Aspose.CAD قبل تحميل الصورة: `License license = new License(); license.setLicense("Aspose.CAD.lic");`. |

## الأسئلة المتكررة

**س1: هل يمكنني استخدام Aspose.CAD للـ Java مع مكتبات CAD أخرى مبنية على Java؟**  
ج: Aspose.CAD للـ Java مكتبة مستقلة لكنها يمكن دمجها مع مكتبات Java أخرى لتوسيع الوظائف.

**س2: هل هناك خيارات ترخيص لـ Aspose.CAD؟**  
ج: نعم، يمكنك استكشاف خيارات الترخيص وتفاصيل الشراء **[هنا](https://purchase.aspose.com/buy)**.

**س3: كيف يمكنني الحصول على ترخيص مؤقت لـ Aspose.CAD؟**  
ج: زر **[هذا الرابط](https://purchase.aspose.com/temporary-license/)** لطلب ترخيص مؤقت.

**س4: أين يمكنني العثور على دعم لـ Aspose.CAD؟**  
ج: لأي استفسارات أو مساعدة، زر **[منتدى Aspose.CAD](https://forum.aspose.com/c/cad/19)**.

**س5: هل هناك نسخة تجريبية مجانية متاحة لـ Aspose.CAD؟**  
ج: نعم، يمكنك الوصول إلى نسخة تجريبية مجانية **[هنا](https://releases.aspose.com/)**.

## الخلاصة

باتباعك لهذا **dwg to pdf tutorial**، لديك الآن طريقة موثوقة لـ **convert DWG to PDF** مع استهداف تخطيط واحد. هذه الطريقة توفر مساحة التخزين، وتسرّع مشاركة المستندات، وتحافظ على تنظيم سير عمل CAD الخاص بك. لا تتردد في تجربة إعدادات التحويل إلى نقطية المختلفة أو دمج عدة تخطيطات في ملف PDF واحد مع تطور مشروعك.

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}

---

**آخر تحديث:** 2025-12-21  
**تم الاختبار مع:** Aspose.CAD for Java 24.12  
**المؤلف:** Aspose