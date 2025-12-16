---
date: 2025-12-12
description: تعلم كيفية تعيين لون الخلفية في Java باستخدام Aspose.CAD for Java أثناء
  تحويل ملفات CAD إلى PDF وTIFF. خصّص لون الرسم للحصول على نتائج احترافية.
linktitle: Setting Background and Drawing Color
second_title: Aspose.CAD Java API
title: تعيين لون الخلفية في جافا باستخدام Aspose.CAD للـ Java
url: /ar/java/advanced-cad-features/setting-background-and-drawing-color/
weight: 15
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# تعيين لون الخلفية في Java باستخدام Aspose.CAD for Java

## المقدمة

في سير عمل CAD الحديث، القدرة على **تعيين لون الخلفية في Java** أثناء التحويل أمر أساسي لإنتاج مستندات واضحة وجاهزة للعرض. تجعل Aspose.CAD for Java عملية تحويل ملفات CAD إلى PDF أو TIFF سهلة مع منحك التحكم الكامل في ألوان الخلفية والرسم. في هذا البرنامج التعليمي سنستعرض العملية بالكامل — من تحميل ملف DXF إلى تصدير ملفات PDF وTIFF بالألوان التي تختارها.

## إجابات سريعة
- **ما المكتبة التي تتعامل مع تحويل CAD في Java؟** Aspose.CAD for Java.  
- **هل يمكنني تغيير لون الخلفية أثناء التحويل؟** نعم، باستخدام `CadRasterizationOptions.setBackgroundColor`.  
- **ما صيغ الإخراج التي يغطيها؟** PDF وTIFF (كلاهما rasterized).  
- **هل أحتاج إلى ترخيص للاستخدام الإنتاجي؟** الترخيص التجاري مطلوب؛ يتوفر نسخة تجريبية مجانية.  
- **هل يدعم التحويل الجماعي؟** بالتأكيد — يمكن معالجة ملفات متعددة في حلقة باستخدام نفس الإعدادات.

## ما هو “set background color java” في سياق تحويل CAD؟
تعيين لون الخلفية في Java يعني تكوين خيارات الـ rasterization بحيث يستخدم اللون الذي تحدده بدلاً من القماش الأبيض الافتراضي عند إنشاء الصورة (PDF أو TIFF). هذا يحسن التباين البصري، خاصةً عندما يحتوي الرسم على خطوط فاتحة.

## لماذا نستخدم Aspose.CAD for Java لتحويل CAD إلى PDF أو TIFF؟
- **دقة عالية** – يحافظ على وزن الخطوط، الطبقات، والألوان.  
- **بدون تبعيات خارجية** – جافا صافية، لا مكتبات أصلية.  
- **مرونة في العرض** – التحكم في حجم الصفحة، DPI، الخلفية، وألوان الرسم.  
- **معالجة دفعات** – مثالية لأنابيب الأتمتة.

## المتطلبات المسبقة

قبل أن نبدأ، تأكد من وجود ما يلي:

- **مكتبة Aspose.CAD for Java** – قم بتنزيلها [هنا](https://releases.aspose.com/cad/java/).  
- **مجلد لملفات CAD** – استبدل `"Your Document Directory" + "CADConversion/"` بالمسار الفعلي على جهازك.

## استيراد المساحات الاسمية

أولاً، استورد الفئات التي ستحتاجها. هذه الاستيرادات تمنحك إمكانية التعامل مع الألوان، خيارات الـ rasterization، وصيغ الإخراج.

```java
import java.awt.Color;
import java.awt.Image;

import com.aspose.cad.fileformats.cad.CadDrawTypeMode;
import com.aspose.cad.fileformats.tiff.enums.TiffExpectedFormat;
import com.aspose.cad.imageoptions.CadRasterizationOptions;
import com.aspose.cad.imageoptions.PdfOptions;
import com.aspose.cad.imageoptions.TiffOptions;
```

## دليل خطوة بخطوة

### الخطوة 1: تحميل ملف CAD

نقوم بتحميل ملف DXF (أو أي صيغة CAD مدعومة) إلى كائن `Image`.

```java
String dataDir = "Your Document Directory" + "CADConversion/";
String srcFile = dataDir + "conic_pyramid.dxf";
Image objImage = Image.load(srcFile);
```

### الخطوة 2: تكوين لون الخلفية ولون الرسم

هنا نحدد أبعاد الصفحة، نختار لون الخلفية، ونخبر الـ renderer باستخدام لون رسم محدد بدلاً من ألوان CAD الأصلية.

```java
CadRasterizationOptions rasterizationOptions = new CadRasterizationOptions();
rasterizationOptions.setPageWidth(1600);
rasterizationOptions.setPageHeight(1600);
rasterizationOptions.setBackgroundColor(com.aspose.cad.Color.getBeige());   // example background
rasterizationOptions.setDrawType(CadDrawTypeMode.UseDrawColor);
rasterizationOptions.setBackgroundColor(com.aspose.cad.Color.getBlue());   // overwrite with blue if needed
```

> **نصيحة احترافية:** جرّب `CadDrawTypeMode.UseOriginalColors` إذا أردت الحفاظ على ألوان CAD الأصلية مع تطبيق خلفية مخصصة.

### الخطوة 3: إنشاء PDF وحفظه

نربط خيارات الـ rasterization بـ `PdfOptions` ونحفظ النتيجة كملف PDF.

```java
PdfOptions pdfOptions = new PdfOptions();
pdfOptions.setVectorRasterizationOptions(rasterizationOptions);
objImage.save(dataDir + "result_out_.pdf", pdfOptions);
```

### الخطوة 4: إنشاء TIFF وحفظه

يمكن إعادة استخدام نفس إعدادات الـ rasterization لإخراج TIFF.

```java
TiffOptions tiffOptions = new TiffOptions(TiffExpectedFormat.Default);
tiffOptions.setVectorRasterizationOptions(rasterizationOptions);
objImage.save(dataDir + "result_out_.tiff", tiffOptions);
```

## المشكلات الشائعة والحلول

| المشكلة | الحل |
|-------|----------|
| **لون الخلفية لا يتغير** | تأكد من استدعاء `setBackgroundColor` *بعد* ضبط نوع الرسم. الاستدعاء الثاني يكتب فوق الأول، لذا احتفظ باللون المطلوب كآخر استدعاء. |
| **الإخراج غير واضح** | زد من `PageWidth`/`PageHeight` أو اضبط DPI أعلى عبر `rasterizationOptions.setResolution(...)`. |
| **استثناء ملف غير موجود** | تحقق من أن مسار `dataDir` ينتهي بفاصل (`/` أو `\\`) وأن الملف موجود فعلاً. |

## الأسئلة المتكررة

**س: هل Aspose.CAD for Java مناسبة للتحويلات الجماعية؟**  
ج: بالتأكيد. يمكنك وضع الكود داخل حلقة ومعالجة عشرات الملفات بنفس إعدادات الـ rasterization.

**س: هل يمكنني تخصيص لون الخلفية في الملفات المولدة؟**  
ج: نعم. يوضح البرنامج التعليمي كيفية تعيين أي `com.aspose.cad.Color` تحتاجه لكل من مخرجات PDF وTIFF.

**س: أين يمكنني العثور على وثائق شاملة لـ Aspose.CAD for Java؟**  
ج: راجع [الوثائق](https://reference.aspose.com/cad/java/) للحصول على تفاصيل متعمقة وأمثلة إضافية.

**س: هل تتوفر نسخة تجريبية مجانية؟**  
ج: نعم، استكشف الميزات عبر [النسخة التجريبية المجانية](https://releases.aspose.com/).

**س: كيف يمكنني الحصول على دعم لـ Aspose.CAD for Java؟**  
ج: زر [منتدى Aspose.CAD](https://forum.aspose.com/c/cad/19) لطرح الأسئلة ومشاركة التجارب مع المجتمع.

---

**آخر تحديث:** 2025-12-12  
**تم الاختبار مع:** Aspose.CAD for Java 24.11  
**المؤلف:** Aspose  

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}