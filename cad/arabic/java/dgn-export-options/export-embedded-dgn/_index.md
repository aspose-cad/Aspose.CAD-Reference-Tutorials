---
date: 2026-01-07
description: تعلم كيفية تصدير ملفات CAD إلى PDF وتحويل DGN إلى PDF باستخدام Aspose.CAD
  للغة Java. دليل خطوة بخطوة لمطوري Java.
linktitle: Export Embedded DGN
second_title: Aspose.CAD Java API
title: تصدير CAD إلى PDF – تصدير DGN المدمج باستخدام Aspose.CAD للغة Java
url: /ar/java/dgn-export-options/export-embedded-dgn/
weight: 11
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# تصدير CAD إلى PDF – تصدير DGN المضمن باستخدام Aspose.CAD for Java

## مقدمة

## إجابات سريعة
- **ماذا يعني “export CAD to PDF”?** يقوم بتحويل رسومات CAD (DWG، DGN، إلخ) إلى ملفات PDF مع الحفاظ على جودة المتجهات.  
- **ما المكتبة المستخدمة؟** Aspose.CAD for Java.  
- **هل أحتاج إلى ترخيص؟** يتطلب الترخيص للاستخدام في الإنتاج؛ يتوفر نسخة تجريبية مجانية.  
- **ما المتطلبات الأساسية؟** بيئة تطوير Java وحزمة Aspose.CAD for Java JAR.  
- **هل يمكنني تخصيص المخرجات؟** نعم – يمكنك اختيار التخطيطات، ضبط خيارات الرستر، والتحكم في إعدادات PDF.

## ما هو “export CAD to PDF”؟
يعني تصدير CAD إلى PDF أخذ ملف CAD أصلي (مثل DWG أو DGN) وإنشاء مستند PDF يمثل بدقة الهندسة الأصلية. يمكن عرض ملف PDF على أي منصة دون الحاجة إلى برنامج CAD، مما يجعله مثالياً للمشاركة أو الطباعة أو الأرشفة.

## لماذا نستخدم Aspose.CAD for Java لتحويل DGN إلى PDF؟
- **بدون تبعيات خارجية** – يعمل بالكامل في Java.  
- **يحافظ على بيانات المتجهات** – تبقى ملفات PDF واضحة عند أي مستوى تكبير.  
- **تحكم دقيق** – اختر تخطيطات محددة، اضبط DPI للرستر، وضمن الخطوط.  
- **جاهز للمؤسسات** – يدعم الملفات الكبيرة، المعالجة الدفعية، وخيارات الترخيص.

## المتطلبات الأساسية

قبل أن نبدأ، تأكد من توفر ما يلي:

- **بيئة تطوير Java** – JDK 8 أو أعلى مثبتة ومُكوَّنة.  
- **Aspose.CAD for Java** – قم بتنزيل أحدث JAR من [here](https://releases.aspose.com/cad/java/).

## استيراد الحزم

للبدء، تحتاج إلى استيراد الفئات الضرورية في مشروع Java الخاص بك. أضف عبارات الاستيراد التالية إلى ملف المصدر الخاص بك:

```java
import java.io.FileNotFoundException;
import java.io.FileOutputStream;
import java.io.OutputStream;
import com.aspose.cad.Image;
import com.aspose.cad.ImageOptionsBase;
import com.aspose.cad.fileformats.cad.CadImage;
import com.aspose.cad.fileformats.dgn.DgnImage;
import com.aspose.cad.imageoptions.CadRasterizationOptions;
import com.aspose.cad.imageoptions.JpegOptions;
import com.aspose.cad.imageoptions.PdfOptions;
```

## كيفية تصدير DGN إلى PDF باستخدام Aspose.CAD for Java؟

فيما يلي دليل واضح مرقم يوضح بالضبط كيفية تحويل ملف DGN مضمّن (مخزن داخل DWG) إلى PDF.

### الخطوة 1: إعداد مسارات الإدخال والإخراج

حدد الدليل الذي يحتوي على ملف المصدر الخاص بك وحدد ملف DWG الذي يحتوي على DGN المضمّن.

```java
String dataDir = "Your Document Directory" + "ExportingDGN/";
String fileName = dataDir + "BlockRefDgn.dwg";
```

### الخطوة 2: تحميل ملف DWG

حمّل ملف DWG في كائن `Image`. يكتشف Aspose.CAD تلقائيًا بيانات DGN المضمّنة.

```java
Image objImage = Image.load(fileName);
```

### الخطوة 3: تكوين خيارات الرستر

اختر التخطيط (التخطيطات) التي تريد تضمينها في PDF. في هذا المثال نقوم بتصدير تخطيط **Model** فقط.

```java
CadRasterizationOptions rasterizationOptions = new CadRasterizationOptions();
rasterizationOptions.setLayouts(new String[] {"Model"});
```

### الخطوة 4: تكوين خيارات PDF

اربط إعدادات الرستر بخيارات تصدير PDF.

```java
PdfOptions pdfOptions = new PdfOptions();
pdfOptions.setVectorRasterizationOptions(rasterizationOptions);
```

### الخطوة 5: حفظ ملف PDF

أخيرًا، احفظ ملف PDF على القرص باستخدام الخيارات المكوَّنة.

```java
objImage.save(dataDir + "BlockRefDgn.pdf", pdfOptions);
```

## تحويل DWG إلى PDF – نصيحة إضافية

إذا كان ملف المصدر الخاص بك هو DWG عادي (بدون DGN مضمّن)، يمكنك إعادة استخدام نفس الكود – فقط غيّر قيمة `fileName` لتشير إلى ملف DWG الذي تريد تحويله. تبقى خيارات الرستر وPDF متطابقة، مما يمنحك سير عمل ثابت لـ **convert DWG to PDF**.

## المشكلات الشائعة والحلول

| المشكلة | السبب | الحل |
|-------|--------|----------|
| **إخراج PDF فارغ** | عدم تطابق اسم التخطيط | تحقق من أن اسم التخطيط الممرّر إلى `setLayouts` يطابق تمامًا اسم التخطيط في ملف المصدر (حسّاس لحالة الأحرف). |
| **استثناء الترخيص** | استخدام النسخة التجريبية بدون ترخيص | قم بتطبيق ترخيص Aspose.CAD صالح قبل تحميل الصورة (`License license = new License(); license.setLicense("Aspose.CAD.lic");`). |
| **الملف غير موجود** | مسار `dataDir` غير صحيح | استخدم مسارًا مطلقًا أو تأكد من صحة المسار النسبي بالنسبة إلى دليل عمل المشروع. |
| **رسومات منخفضة الدقة** | قيمة DPI الافتراضية للرستر منخفضة | قم بتعيين `rasterizationOptions.setPageWidth/Height` أو `setResolution` لزيادة DPI. |

## الأسئلة المتكررة

**س: هل يمكنني استخدام Aspose.CAD for Java في مشروع تجاري؟**  
ج: نعم، Aspose.CAD for Java هي مكتبة تجارية. يمكنك الحصول على ترخيص من [here](https://purchase.aspose.com/buy).

**س: هل تتوفر نسخة تجريبية مجانية؟**  
ج: نعم، يمكنك الوصول إلى نسخة تجريبية مجانية من Aspose.CAD for Java [here](https://releases.aspose.com/).

**س: كيف يمكنني الحصول على دعم Aspose.CAD for Java؟**  
ج: يمكنك طلب الدعم من مجتمع Aspose.CAD على [forum](https://forum.aspose.com/c/cad/19).

**س: ماذا لو احتجت إلى ترخيص مؤقت؟**  
ج: يمكنك الحصول على ترخيص مؤقت من [here](https://purchase.aspose.com/temporary-license/).

**س: أين يمكنني العثور على الوثائق؟**  
ج: الوثائق متاحة [here](https://reference.aspose.com/cad/java/).

## الخلاصة

لقد تعلمت الآن كيفية **export CAD to PDF**، وتحديدًا كيفية **convert DGN to PDF** وحتى **convert DWG to PDF** باستخدام Aspose.CAD for Java. باتباع الخطوات أعلاه، يمكنك دمج تحويل CAD إلى PDF بسلاسة في أي حل مبني على Java، وتقديم ملفات PDF عالية الجودة لمستخدميك دون الحاجة إلى برنامج CAD إضافي.

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}

---

**آخر تحديث:** 2026-01-07  
**تم الاختبار باستخدام:** Aspose.CAD for Java 24.12  
**المؤلف:** Aspose