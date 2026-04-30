---
date: 2026-01-12
description: تعلم كيفية تصدير ملفات CAD إلى PDF مع تجاوز الكشف التلقائي عن صفحة الترميز
  في ملفات DWG باستخدام Aspose.CAD للغة Java. يتعامل مع الترميز وملفات CIF/MIF المشوهة.
linktitle: Override Automatic Code Page Detection in DWG Files
second_title: Aspose.CAD Java API
title: تصدير CAD إلى PDF – تجاوز الكشف التلقائي عن صفحة الترميز في ملفات DWG باستخدام
  Java
url: /ar/java/dwg-file-operations/override-code-page-detection/
weight: 13
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# تصدير CAD إلى PDF – تجاوز الكشف التلقائي عن صفحة الترميز في ملفات DWG باستخدام Java

## مقدمة

في هذا الدليل الشامل ستكتشف **كيفية تصدير CAD إلى PDF** مع تجاوز الكشف التلقائي عن صفحة الترميز الذي يمكن أن يفسد النص في ملفات DWG. يمنحك Aspose.CAD for Java تحكمًا دقيقًا في الترميز، مما يتيح لك استعادة بيانات CIF/MIF المشوهة وإنتاج مخرجات PDF موثوقة. سواءً كنت تبني محولًا دفعيًا أو تدمج معالجة CAD في تطبيق Java أكبر، فإن الخطوات أدناه ستقودك عبر سير العمل بالكامل.

## إجابات سريعة
- **ماذا يعني “تجاوز صفحة الترميز”?** إنه يجبر Aspose.CAD على استخدام ترميز أحرف محدد بدلاً من التخمين.
- **هل يمكنني تصدير DWG مباشرة إلى PDF؟** نعم – بعد ضبط صفحة الترميز الصحيحة، يمكنك حفظ صورة CAD كملف PDF.
- **ما هو الترميز المناسب للنص الياباني؟** `CodePages.Japanese` و `MifCodePages.Japanese` هما الاختياران الصحيحان.
- **هل أحتاج إلى رخصة للاستخدام الإنتاجي؟** يلزم الحصول على رخصة تجارية؛ تتوفر رخصة مؤقتة للاختبار.
- **ما هو إصدار Aspose.CAD المطلوب؟** أي إصدار حديث يدعم `LoadOptions` و `PdfOptions`.

## ما هو “تصدير CAD إلى PDF”؟
تحويل CAD إلى PDF يحول الرسومات الهندسية القائمة على المتجهات إلى تنسيق مستند ثابت يدعم على نطاق واسع. يحافظ ملف PDF الناتج على الخطوط، الطبقات، والنص مع جعل الرسم سهل المشاركة، الطباعة، أو الإدراج في تطبيقات أخرى.

## لماذا يتم تجاوز الكشف التلقائي عن صفحة الترميز؟
غالبًا ما تخزن ملفات DWG النص باستخدام صفحات ترميز قديمة. يمكن أن يفسر الكشف التلقائي في Aspose.CAD هذه البايتات بشكل خاطئ، مما يؤدي إلى ظهور أحرف مشوشة. من خلال تحديد صفحة الترميز يدويًا، تضمن ظهور النص بالضبط كما هو مقصود في ملف PDF المصدر، خاصةً للخطوط غير اللاتينية مثل اليابانية، السيريالية، أو العربية.

## المتطلبات المسبقة
- **بيئة تطوير Java** – JDK 8+ وIDE المفضلة لديك.
- **Aspose.CAD for Java** – قم بتنزيل المكتبة من الموقع الرسمي [هنا](https://releases.aspose.com/cad/java/).
- **ملف DWG تجريبي** – استخدم الملف `SimpleEntities.dwg` المرفق أو أي ملف DWG تحتاج إلى تحويله.

## استيراد الحزم
في مشروع Java الخاص بك، استورد الفئات الضرورية من Aspose.CAD:

```java
import com.aspose.cad.CodePages;
import com.aspose.cad.Image;
import com.aspose.cad.LoadOptions;
import com.aspose.cad.MifCodePages;
import com.aspose.cad.fileformats.cad.CadImage;
```

## دليل خطوة بخطوة

### الخطوة 1: إعداد مشروع Java
أنشئ مشروع Maven أو Gradle جديد وأضف ملف JAR الخاص بـ Aspose.CAD إلى مسار الفئة. تضمن هذه الخطوة أن IDE يمكنه حل الفئات المستوردة.

### الخطوة 2: تحميل ملف DWG بصفحة ترميز محددة
أخبر Aspose.CAD أي ترميز يجب استخدامه وما إذا كان يجب محاولة استعادة بيانات CIF/MIF المشوهة.

```java
String SourceDir = "Your Document Directory";
String dwgPathToFile = SourceDir + "SimpleEntites.dwg";
LoadOptions opts = new LoadOptions();
opts.setSpecifiedEncoding(CodePages.Japanese);
opts.setSpecifiedMifEncoding(MifCodePages.Japanese);
opts.setRecoverMalformedCifMif(false);
CadImage cadImage = (CadImage) Image.load(dwgPathToFile, opts);
```

### الخطوة 3: تصدير صورة CAD إلى PDF
مع تطبيق صفحة الترميز الصحيحة، يمكنك تصدير الرسم بأمان. يتيح لك كائن `PdfOptions` ضبط مخرجات PDF بدقة (الضغط، التحويل إلى نقطية، إلخ).

```java
// Perform export or other operations with cadImage
// For example, exporting to PDF
PdfOptions pdfOptions = new PdfOptions();
cadImage.save("output.pdf", pdfOptions);
```

### الخطوة 4: التحقق من النجاح
رسالة بسيطة في وحدة التحكم تؤكد أن العملية اكتملت دون استثناءات.

```java
System.out.println("OverrideAutomaticCodePageDetectionDwg executed successfully");
```

يمكنك تكرار هذه الخطوات لعدة ملفات DWG، مع تعديل مسار المصدر واسم الإخراج حسب الحاجة.

## المشكلات الشائعة والحلول
- **ما زالت الأحرف غير المفهومة تظهر:** تحقق مرة أخرى من أن `specifiedEncoding` يطابق صفحة الترميز الأصلية لملف DWG. استخدم تعداد `CodePages` مختلف إذا لزم الأمر.
- **`NullPointerException` عند `cadImage.save`:** تأكد من تحميل ملف DWG بشكل صحيح؛ تحقق من المسار وأذونات الملف.
- **حجم PDF كبير:** فعّل الضغط في `PdfOptions` (مثال: `pdfOptions.setCompress(true)`).

## الأسئلة المتكررة

**س1: هل Aspose.CAD متوافق مع جميع إصدارات ملفات DWG؟**  
ج1: يدعم Aspose.CAD مجموعة واسعة من إصدارات DWG، بما في ذلك AutoCAD 2018 والإصدارات السابقة.

**س2: هل يمكنني استخدام Aspose.CAD للمشاريع التجارية؟**  
ج2: نعم، يلزم الحصول على رخصة تجارية للاستخدام الإنتاجي. يمكنك الحصول على رخصة [هنا](https://purchase.aspose.com/buy).

**س3: هل هناك أي قيود في نسخة التجربة المجانية؟**  
ج3: النسخة التجريبية تفرض قيودًا على الحجم والميزات؛ راجع الوثائق الرسمية للحصول على التفاصيل.

**س4: كيف يمكنني الحصول على دعم لـ Aspose.CAD؟**  
ج4: زر مجتمع [منتدى Aspose.CAD](https://forum.aspose.com/c/cad/19) للحصول على المساعدة والنقاشات.

**س5: هل تتوفر رخصة مؤقتة لأغراض الاختبار؟**  
ج5: نعم، يمكن طلب رخصة مؤقتة [هنا](https://purchase.aspose.com/temporary-license/).

**آخر تحديث:** 2026-01-12  
**تم الاختبار مع:** Aspose.CAD for Java 24.11 (latest at time of writing)  
**المؤلف:** Aspose  

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}