---
date: 2026-05-04
description: تعلم كيفية تحويل ملفات CAD PDF عن طريق تصدير DGN إلى PDF AutoCAD باستخدام
  Aspose.CAD للغة Java. دليل خطوة بخطوة مع حجم PDF قابل للتخصيص وخيارات.
keywords:
- convert cad pdf
- how to export dgn
- customize pdf size
- aspose cad download
- set pdf options
linktitle: تصدير DGN بصيغة AutoCAD إلى PDF
second_title: Aspose.CAD Java API
title: تحويل CAD PDF – تصدير DGN إلى PDF أوتوكاد بسهولة باستخدام Aspose.CAD للغة جافا
url: /ar/java/dgn-export-options/exporting-dgn-to-pdf/
weight: 12
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# تحويل CAD PDF: تصدير DGN إلى PDF متوافق مع AutoCAD بسهولة باستخدام Aspose.CAD for Java

## المقدمة

إذا كنت بحاجة إلى **convert CAD PDF** ملفات مباشرةً من مصادر DGN، فقد وصلت إلى المكان الصحيح. في هذا الدرس سنرشدك إلى كيفية استخدام Aspose.CAD for Java لتصدير ملفات DGN إلى PDF متوافق مع AutoCAD. ستتعرف على كيفية ضبط أبعاد الصفحة المخصصة، اختيار تخطيطات محددة، وضبط مخرجات PDF بدقة — كل ذلك مع كود واضح خطوة بخطوة يمكنك إدراجه في مشروعك.

## إجابات سريعة
- **What does “convert CAD PDF” mean?** يشير إلى تحويل ملفات CAD المصدرية (مثل DGN) إلى PDF يحافظ على بيانات المتجهات ودقة التخطيط.  
- **Which library handles the conversion?** Aspose.CAD for Java توفر نسخة تجريبية موثوقة مجانية من الترخيص لهذا المهمة.  
- **Do I need a license for development?** النسخة التجريبية المجانية تكفي للاختبار؛ يتطلب الاستخدام في الإنتاج رخصة تجارية.  
- **Can I customize the PDF size?** نعم – تسمح لك `CadRasterizationOptions` بتحديد عرض الصفحة، ارتفاعها، والقياس.  
- **How many lines of code are required?** أقل من 20 سطرًا من كود Java لتحميل، تكوين، وحفظ PDF.

## ما هو “convert CAD PDF”؟
تحويل CAD PDF يعني أخذ رسم CAD أصلي (مثل DGN) وإنتاج PDF يحتفظ بالرسومات المتجهية الأصلية، الطبقات، ومعلومات التخطيط. يمكن عرض PDF الناتج على أي جهاز دون الحاجة إلى برنامج CAD، مما يجعله مثاليًا للمشاركة، الطباعة، أو الأرشفة.

## لماذا تستخدم Aspose.CAD for Java لتحويل CAD PDF؟
- **Full format support** – DGN, DWG, DXF، والعديد غيرها.  
- **No external dependencies** – Java نقي، لا توجد DLLs أصلية.  
- **Fine‑grained control** – يمكنك اختيار أي تخطيطات لتصديرها، ضبط أحجام صفحات مخصصة، والتحكم في جودة التحويل إلى نقطية.  
- **Scalable for batch jobs** – تحميل وحفظ العشرات من الملفات في حلقة مع حد أدنى من الحمل.

## المتطلبات المسبقة
قبل أن نبدأ، تأكد من أن لديك ما يلي:

- **Aspose.CAD Library** – قم بتنزيله [here](https://releases.aspose.com/cad/java/).  
- **Document Directory** – مجلد على جهازك حيث ستوجد ملفات DGN المدخلة وملفات PDF الناتجة.

## استيراد الحزم

في مشروع Java الخاص بك، استورد الحزم اللازمة للوصول إلى وظائف Aspose.CAD:

```java
import java.io.FileNotFoundException;
import java.io.FileOutputStream;
import java.io.OutputStream;
import com.aspose.cad.Image;
import com.aspose.cad.fileformats.dgn.DgnImage;
import com.aspose.cad.imageoptions.CadRasterizationOptions;
import com.aspose.cad.imageoptions.PdfOptions;
```

الآن، لنقسم كود المثال إلى خطوات متعددة:

## الخطوة 1: تعريف مسارات الملفات (كيفية تصدير dgn)

```java
String dataDir = "Your Document Directory" + "ExportingDGN/";
String fileName = dataDir + "Nikon_D90_Camera.dgn";
String outFile  = dataDir + "Nikon_D90_Camera.pdf";
```

تأكد من استبدال `"Your Document Directory"` بالمسار الفعلي حيث توجد ملفاتك.

## الخطوة 2: تحميل صورة DGN

```java
DgnImage objImage = (DgnImage) Image.load(fileName);
```

حمّل ملف DGN باستخدام Aspose.CAD.

## الخطوة 3: ضبط خيارات تصدير PDF (تخصيص حجم PDF، ضبط خيارات PDF)

```java
PdfOptions options = new PdfOptions();
CadRasterizationOptions vectorOptions = new CadRasterizationOptions();
vectorOptions.setPageWidth(1500);
vectorOptions.setPageHeight(1500);
vectorOptions.setAutomaticLayoutsScaling(true);
vectorOptions.setLayouts(new String[] { "1", "2", "3", "9" }); // Export specific views
options.setVectorRasterizationOptions(vectorOptions);
```

هنا نحدد خيارات تصدير PDF، بما في ذلك أبعاد الصفحة، التحجيم التلقائي، وتخطيطات DGN المحددة (المناظير) التي تريد تضمينها في PDF النهائي.

## الخطوة 4: حفظ ملف PDF

```java
objImage.save(outFile, options);
```

احفظ ملف PDF المُصدّر. طريقة `save` تطبق جميع الخيارات التي قمت بتكوينها في الخطوة السابقة.

كرر هذه الخطوات لأي ملفات DGN إضافية تريد تحويلها. تهانينا! لقد نجحت في **convert CAD PDF** عن طريق تصدير ملفات DGN إلى تنسيق AutoCAD بصيغة PDF باستخدام Aspose.CAD for Java.

## المشكلات الشائعة والحلول
| المشكلة | السبب | الحل |
|-------|----------------|-----|
| **File not found** | مسار `dataDir` غير صحيح | تحقق مرة أخرى من مسار المجلد وتأكد من وجود ملف DGN. |
| **Blank pages in PDF** | تم ضبط `AutomaticLayoutsScaling` على `false` أو معرفات التخطيطات مفقودة | احتفظ بـ `setAutomaticLayoutsScaling(true)` وتحقق من أسماء التخطيطات (`"1","2",…`). |
| **Low‑resolution output** | DPI الافتراضي للتحويل إلى نقطية منخفض | استخدم `vectorOptions.setResolution(300);` لزيادة الجودة (أضفه قبل `setVectorRasterizationOptions`). |
| **License exception** | تشغيل بدون رخصة صالحة في بيئة الإنتاج | طبق رخصة مؤقتة أو مُشتراة كما هو موضح في وثائق Aspose. |

## الأسئلة المتكررة (إضافية)

**س: هل يمكنني تصدير تخطيط واحد فقط من ملف DGN متعدد التخطيطات؟**  
ج: نعم – حدد معرفات التخطيطات المطلوبة في `vectorOptions.setLayouts(new String[] { "2" });`.

**س: هل يمكن تضمين الخطوط في PDF الناتج؟**  
ج: Aspose.CAD يضمّن الخطوط اللازمة تلقائيًا عند تحويل البيانات المتجهية إلى نقطية؛ يمكنك أيضًا التحكم في تضمين الخطوط عبر `PdfOptions` إذا لزم الأمر.

**س: كيف يمكنني معالجة العديد من ملفات DGN دفعة واحدة؟**  
ج: ضع الخطوات داخل حلقة `for` التي تتكرر على قائمة أسماء الملفات، مع إعادة استخدام نفس كائن `PdfOptions` في كل تكرار.

**س: هل تدعم المكتبة ملفات PDF محمية بكلمة مرور؟**  
ج: نعم – يمكنك تعيين كلمة مرور على كائن `PdfOptions` عبر `options.setPassword("yourPassword");`.

**س: أين يمكنني العثور على المزيد من الأمثلة؟**  
ج: وثائق Aspose.CAD الرسمية ومستودع العينات يحتويان على العديد من السيناريوهات الإضافية.

## الأسئلة الشائعة (الأصلية)

### س1: هل Aspose.CAD متوافق مع جميع صيغ ملفات CAD؟

A1: نعم، Aspose.CAD يدعم مجموعة واسعة من صيغ CAD، مما يضمن مرونة في التعامل مع أنواع الملفات المختلفة.

### س2: هل يمكنني تخصيص إعدادات تصدير PDF؟

A2: بالتأكيد. كما هو موضح في الدرس، يمكنك تعديل الخيارات مثل أبعاد الصفحة والتخطيطات لتناسب متطلباتك.

### س3: أين يمكنني العثور على دعم أو مساعدة إضافية؟

A3: زر [Aspose.CAD forum](https://forum.aspose.com/c/cad/19) للحصول على دعم المجتمع والنقاشات.

### س4: هل تتوفر نسخة تجريبية مجانية؟

A4: نعم، يمكنك الوصول إلى النسخة التجريبية المجانية [here](https://releases.aspose.com/).

### س5: كيف يمكنني الحصول على رخصة مؤقتة؟

A5: احصل على رخصة مؤقتة [here](https://purchase.aspose.com/temporary-license/).

## الخاتمة

في هذا الدرس استكشفنا كيفية **convert CAD PDF** الملفات باستخدام Aspose.CAD for Java. ببضع أسطر من الكود يمكنك تحميل رسم DGN، ضبط خيارات تصدير PDF بدقة، وإنشاء ملفات PDF عالية الجودة جاهزة للمشاركة أو الأرشفة. لا تتردد في تجربة أحجام صفحات مختلفة، تخطيطات، أو معالجة دفعات لتناسب احتياجات مشروعك.

---

**آخر تحديث:** 2026-05-04  
**تم الاختبار مع:** Aspose.CAD for Java 24.12  
**المؤلف:** Aspose  

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}