---
date: 2025-12-21
description: تعلم كيفية تحويل DWG إلى BMP وتصدير CAD إلى BMP باستخدام Aspose.CAD للغة
  Java من خلال هذا الدليل خطوة بخطوة.
linktitle: Export to BMP
second_title: Aspose.CAD Java API
title: كيفية تحويل DWG إلى BMP باستخدام Aspose.CAD للـ Java
url: /ar/java/cad-export-options/export-to-bmp/
weight: 12
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# تحويل DWG إلى BMP باستخدام Aspose.CAD for Java

## المقدمة

في سير عمل التصميم الرقمي الحديث، القدرة على **تحويل DWG إلى BMP** بسرعة وبشكل موثوق أمر أساسي. سواءً كنت تبني خدمة معالجة دفعات أو تحتاج إلى تحويل ملف واحد، توفر لك Aspose.CAD for Java واجهة برمجة تطبيقات قوية لـ **تصدير CAD إلى BMP** مع تحكم كامل في إعدادات التحويل إلى نقطية. في هذا البرنامج التعليمي ستتبع كل خطوة — من تحميل ملف DWG إلى حفظ صورة BMP النهائية — لتتمكن من دمج التحويل في تطبيقات Java الخاصة بك بثقة.

## إجابات سريعة
- **ما المكتبة المطلوبة؟** Aspose.CAD for Java.
- **هل يمكنني تحويل DWG إلى BMP بسطر واحد من الشيفرة؟** لا، تحتاج إلى تحميل الملف، ضبط خيارات التحويل إلى نقطية، ثم الحفظ.
- **هل يلزم وجود ترخيص للإنتاج؟** نعم، يلزم ترخيص تجاري؛ يتوفر نسخة تجريبية مجانية.
- **هل تدعم الواجهة البرمجية التحويل الدفعي؟** بالتأكيد — يمكنك المرور على الملفات وإعادة استخدام نفس الخيارات.
- **ما نسخة Java المدعومة؟** Java 8 وما بعدها.

## ما هو “تحويل DWG إلى BMP”؟

تحويل ملف DWG (رسم AutoCAD) إلى صورة BMP (bitmap) يعني تحويل البيانات المتجهة إلى تنسيق قائم على البكسل. هذا مفيد عندما تحتاج إلى صورة يمكن عرضها عالميًا للتقارير أو المصغرات أو معاينة الويب دون الحاجة إلى برنامج CAD.

## لماذا نستخدم Aspose.CAD for Java لتصدير CAD إلى BMP؟

- **بدون تبعيات خارجية** – جافا صافية، لا ملفات DLL أصلية.
- **تحكم دقيق في التحويل إلى نقطية** – ضبط حجم الصفحة، التخطيط، مضاد التعرج.
- **دقة عالية** – يحافظ على أوزان الخطوط، الألوان، والطبقات.
- **قابلة للتوسع** – تعمل مع ملفات فردية أو دفعات كبيرة.

## المتطلبات المسبقة

قبل الغوص في الشيفرة، تأكد من وجود ما يلي:

- **مكتبة Aspose.CAD for Java** – قم بتنزيلها من [here](https://releases.aspose.com/cad/java/).
- **بيئة تطوير Java** – JDK 8+ وأي IDE تفضله.
- **معرفة أساسية بـ Java** – إلمام بالفئات، الأساليب، وإدخال/إخراج الملفات.

## استيراد المساحات الاسمية

في مشروع Java الخاص بك، استورد المساحات الاسمية اللازمة للوصول إلى وظائف Aspose.CAD:

```java
import com.aspose.cad.Image;
import com.aspose.cad.InterpolationMode;
import com.aspose.cad.SmoothingMode;
import com.aspose.cad.TextRenderingHint;

import com.aspose.cad.imageoptions.BmpOptions;
import com.aspose.cad.imageoptions.CadRasterizationOptions;
import com.aspose.cad.imageoptions.PdfOptions;
//import com.aspose.cad.imageoptions.TypeOfEntities;
```

## الخطوة 1: تعيين مسار دليل الموارد

حدد المجلد الذي يحتوي على ملف DWG (أو أي ملف CAD آخر) الذي تريد تحويله.

```java
String dataDir = "Your Document Directory" + "ExportingCAD/";
```

## الخطوة 2: تحميل ملف CAD

أنشئ كائن `Image` بتحميل ملف DWG المصدر.

```java
String fileName = (dataDir + "site.dwf");
Image image = Image.load(fileName);
```

## الخطوة 3: تكوين خيارات تصدير BMP

أنشئ كائن `BmpOptions` وأرفق كائن `CadRasterizationOptions` الذي يتحكم في طريقة تحويل البيانات المتجهة إلى نقطية.

```java
BmpOptions bmpOptions = new BmpOptions();
CadRasterizationOptions rasterizationOptions = new CadRasterizationOptions();
bmpOptions.setVectorRasterizationOptions(rasterizationOptions);
```

## الخطوة 4: ضبط معلمات التحويل إلى نقطية

عدّل أبعاد الصفحة وحدد أي تخطيط(ات) تريد تصييره. تؤثر هذه الإعدادات مباشرة على جودة وحجم صورة BMP الناتجة.

```java
rasterizationOptions.setPageHeight(500);
rasterizationOptions.setPageWidth(500);
rasterizationOptions.setLayouts(new String[] { "Model" });
```

## الخطوة 5: تصدير إلى BMP

حدد مسار الإخراج واستدعِ `save` لكتابة ملف BMP.

```java
String outPath = dataDir + "site.bmp";
image.save(outPath, bmpOptions);
```

كرر الخطوات السابقة لكل ملف CAD ترغب في **تحويل DWG إلى BMP** باستخدام Aspose.CAD for Java.

## المشكلات الشائعة والنصائح

- **اسم التخطيط غير صحيح** – تأكد من أن سلسلة التخطيط تطابق أحد التخطيطات المعرفة في ملف DWG (مثل `"Model"` أو `"Layout1"`).
- **إخراج منخفض الدقة** – زد من `PageWidth` و `PageHeight` للحصول على نتائج DPI أعلى.
- **استهلاك الذاكرة** – للرسومات الكبيرة جدًا، فكر في معالجة الملفات واحدةً تلو الأخرى وتحرير كائن `Image` بعد كل عملية حفظ.

## الأسئلة المتكررة

### س1: هل Aspose.CAD for Java مناسب للمعالجة الدفعية؟

ج1: بالتأكيد! يدعم Aspose.CAD for Java المعالجة الدفعية، مما يتيح لك التعامل بكفاءة مع ملفات CAD متعددة في آن واحد.

### س2: هل يمكنني تخصيص خيارات التحويل إلى نقطية لتخطيطات مختلفة؟

ج2: نعم، يمكنك تخصيص خيارات التحويل إلى نقطية مثل أبعاد الصفحة والتخطيطات وفقًا لمتطلباتك الخاصة.

### س3: أين يمكنني العثور على دعم إضافي لـ Aspose.CAD for Java؟

ج3: زر [منتدى Aspose.CAD](https://forum.aspose.com/c/cad/19) للحصول على دعم المجتمع والنقاشات.

### س4: هل تتوفر نسخة تجريبية مجانية؟

ج4: نعم، يمكنك تجربة نسخة مجانية من Aspose.CAD for Java [here](https://releases.aspose.com/).

### س5: كيف يمكنني الحصول على ترخيص مؤقت؟

ج5: احصل على ترخيص مؤقت لـ Aspose.CAD for Java [here](https://purchase.aspose.com/temporary-license/).

## أسئلة شائعة أخرى

**س: هل يمكنني تحويل صيغ CAD أخرى (مثل DXF، DGN) إلى BMP؟**  
ج: نعم، تعمل نفس الواجهة البرمجية مع DXF، DGN، DWF، وغيرها من الصيغ المدعومة.

**س: هل يحافظ التحويل على رؤية الطبقات؟**  
ج: بشكل افتراضي تُرسم جميع الطبقات المرئية؛ يمكنك إخفاء طبقات عبر `CadRasterizationOptions` إذا لزم الأمر.

**س: هل يمكن تعيين لون خلفية للـ BMP؟**  
ج: نعم، استخدم `rasterizationOptions.setBackgroundColor(Color.getWhite());` قبل عملية الحفظ.

**س: كيف أتعامل مع ملفات CAD المحمية بكلمة مرور؟**  
ج: حمّل الملف باستخدام `Image.load(fileName, loadOptions)` حيث يحتوي `loadOptions` على كلمة المرور.

**س: ما هي أفضل طريقة لتحسين الأداء للدفعات الكبيرة؟**  
ج: أعد استخدام كائن `BmpOptions` واحد فقط وقم بتغيير مسار ملف الإدخال فقط لكل تكرار.

## الخاتمة

باتباعك لهذا الدليل، أصبحت الآن تمتلك أساسًا قويًا لـ **تحويل DWG إلى BMP** و**تصدير CAD إلى BMP** باستخدام Aspose.CAD for Java. دمج هذه الخطوات في تطبيقاتك سيمكنك من أتمتة إنشاء الصور، إنشاء المصغرات، أو إعداد الأصول للمعالجة اللاحقة.

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}

---

**آخر تحديث:** 2025-12-21  
**تم الاختبار مع:** Aspose.CAD for Java 24.11  
**المؤلف:** Aspose  

---