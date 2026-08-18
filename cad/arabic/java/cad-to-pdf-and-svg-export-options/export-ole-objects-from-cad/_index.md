---
date: 2026-03-02
description: اكتشف إمكانات Aspose.CAD للـ Java. صدّر كائنات OLE بسهولة و**احفظ ملفات
  CAD بصيغة PNG**. حمّل الآن لإدارة بيانات CAD بسلاسة.
linktitle: Export OLE Objects from CAD
second_title: Aspose.CAD Java API
title: حفظ ملفات CAD كـ PNG – تصدير كائنات OLE باستخدام Aspose.CAD للغة Java
url: /ar/java/cad-to-pdf-and-svg-export-options/export-ole-objects-from-cad/
weight: 10
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# حفظ CAD بصيغة PNG – تصدير كائنات OLE باستخدام Aspose.CAD for Java

## مقدمة

في عالم التصميم بمساعدة الحاسوب (CAD) المتطور، يعتبر إدارة واستخراج كائنات OLE (الربط والتضمين) بكفاءة—والقدرة على **حفظ CAD بصيغة PNG**—أمرًا حيويًا لتدفقات العمل اللاحقة مثل التقارير، المعاينة على الويب، أو الأرشفة. توفر مكتبة Aspose.CAD for Java حلاً قويًا يعتمد على الكود يتيح لك تصدير كائنات OLE وتحويل رسومات CAD إلى صور PNG عالية الجودة ببضع أسطر من الشيفرة فقط.

## إجابات سريعة
- **ماذا تفعل Aspose.CAD؟** تقرأ وتعدل وتحول ملفات CAD (DWG، DXF، DGN، إلخ) دون الحاجة إلى برنامج CAD أصلي.  
- **هل يمكنني حفظ CAD بصيغة PNG؟** نعم—استخدم `PngOptions` مع `CadRasterizationOptions` لتصيير أي تخطيط.  
- **كيف يتم تصدير كائنات OLE؟** حمّل ملف CAD باستخدام `Image.load` واحفظ كل تخطيط يحتوي على OLE كملف PNG.  
- **هل أحتاج إلى ترخيص؟** يتوفر نسخة تجريبية مجانية؛ الترخيص التجاري يزيل قيود التقييم.  
- **ما نسخة Java المطلوبة؟** Java 8 أو أعلى مدعومة بالكامل.

## ما هو **حفظ CAD بصيغة PNG**؟
يعني حفظ CAD بصيغة PNG تحويل رسومات CAD القائمة على المتجهات إلى صورة PNG قائمة على البكسل. هذا التحويل مفيد عندما تحتاج إلى تنسيق خفيف الوزن، قابل للعرض على جميع المتصفحات، التطبيقات المحمولة، أو الوثائق.

## لماذا نستخدم Aspose.CAD for Java لـ **تحويل CAD إلى PNG**؟
- **لا حاجة لتثبيت CAD** – تعمل المكتبة بالكامل في بيئة Java.  
- **تحافظ على دقة التخطيط** – يمكنك اختيار تخطيطات محددة، التحكم في DPI، والحفاظ على جودة الخطوط.  
- **معالجة دفعات** – تكرار عبر ملفات متعددة باستخدام حلقة بسيطة.  
- **تصدير كائنات OLE** – محتوى OLE المضمّن في ملفات DWG/DXF يُرسم تلقائيًا في ناتج PNG.

## المتطلبات المسبقة

قبل الغوص في الشرح، تأكد من توفر المتطلبات التالية:

- **بيئة Java** – تأكد من إعداد بيئة تطوير Java على جهازك.  
- **Aspose.CAD for Java** – حمّل وثبّت مكتبة Aspose.CAD for Java. يمكنك العثور على المكتبة عبر [رابط التحميل](https://releases.aspose.com/cad/java/).  
- **ملفات CAD** – حضّر ملفات CAD التي تحتوي على كائنات OLE التي تريد تصديرها.

## استيراد المساحات الاسمية

لبدء العمل، استورد المساحات الاسمية الضرورية إلى مشروع Java الخاص بك. توفر هذه المساحات الاسمية الفئات والوظائف الأساسية للعمل مع ملفات CAD باستخدام Aspose.CAD.

```java
import com.aspose.cad.Image;

import com.aspose.cad.fileformats.cad.CadImage;
import com.aspose.cad.imageoptions.CadRasterizationOptions;
import com.aspose.cad.imageoptions.PngOptions;
```

الآن، لنقسم عملية تصدير كائنات OLE من CAD إلى عدة خطوات:

## كيفية **حفظ CAD بصيغة PNG** وتصدير كائنات OLE

### الخطوة 1: تعيين دليل المستند الخاص بك

```java
String dataDir = "Your Document Directory" + "DWGDrawings/";
```

تأكد من استبدال `"Your Document Directory"` بالمسار إلى الدليل الذي يحتوي على ملفات CAD الخاصة بك.

### الخطوة 2: تعريف أسماء ملفات CAD

```java
String[] files = new String[] { "D ZD junior D10m H2m.dwg", "ZD - Senior D6m H2m45.dwg" };
```

حدد أسماء ملفات CAD التي تريد معالجتها في مصفوفة `files`.

### الخطوة 3: تعيين خيارات تصدير PNG

```java
PngOptions pngOptions = new PngOptions();
CadRasterizationOptions rasterizationOptions = new CadRasterizationOptions();
pngOptions.setVectorRasterizationOptions(rasterizationOptions);
rasterizationOptions.setLayouts(new String[] { "Layout1" });
```

قم بتكوين خيارات تصدير PNG، بما في ذلك تصيير المتجهات وإعدادات التخطيط. هذه الخيارات هي ما يتيح لك **تحويل CAD إلى PNG** بالجودة المطلوبة.

### الخطوة 4: التكرار عبر ملفات CAD

```java
for(String file : files)
{
    CadImage cadImage = (CadImage)Image.load(dataDir + file);
    cadImage.save(dataDir + file + "_out.png", pngOptions);
}
```

قم بالتكرار عبر كل ملف CAD محدد، حمّله باستخدام Aspose.CAD، واحفظ كائنات OLE كصور PNG. تُظهر هذه الحلقة طريقة بسيطة لـ **تحويل DWG إلى PNG** على نطاق واسع.

## المشكلات الشائعة والحلول

| المشكلة | السبب | الحل |
|-------|-------|----------|
| **ناتج PNG فارغ** | عدم تطابق اسم التخطيط | تحقق من أن اسم التخطيط (`"Layout1"`) موجود في ملف DWG المصدر. |
| **غياب رسومات OLE** | تخزين كائنات OLE في تخطيط مختلف | أدرج جميع التخطيطات ذات الصلة في `rasterizationOptions.setLayouts(...)`. |
| **خطأ نفاد الذاكرة على ملفات كبيرة** | إعدادات DPI عالية | قلل DPI عبر `rasterizationOptions.setResolution(...)` أو عالج الملفات واحدةً تلو الأخرى. |

## الأسئلة المتكررة

**س: هل Aspose.CAD متوافق مع جميع صيغ ملفات CAD؟**  
ج: تدعم Aspose.CAD صيغ CAD متعددة، بما في ذلك DWG وDXF وDGN. راجع [التوثيق](https://reference.aspose.com/cad/java/) للقائمة الكاملة.

**س: هل يمكنني تخصيص إعدادات التصدير لكائنات OLE؟**  
ج: نعم، توفر Aspose.CAD خيارات واسعة لتخصيص إعدادات التصدير، مما يتيح لك تعديل الناتج وفقًا لمتطلباتك الخاصة.

**س: هل هناك نسخة تجريبية مجانية متاحة لـ Aspose.CAD؟**  
ج: نعم، يمكنك استكشاف قدرات Aspose.CAD بالحصول على نسخة تجريبية مجانية من [هنا](https://releases.aspose.com/).

**س: أين يمكنني الحصول على دعم المجتمع لـ Aspose.CAD؟**  
ج: انضم إلى مجتمع Aspose.CAD عبر [المنتدى](https://forum.aspose.com/c/cad/19) للحصول على المساعدة ومشاركة تجاربك.

**س: كيف يمكنني شراء ترخيص لـ Aspose.CAD؟**  
ج: زر [صفحة الشراء](https://purchase.aspose.com/buy) للحصول على ترخيص يناسب احتياجات التطوير الخاصة بك.

## الخلاصة

باستخدام هذه الخطوات البسيطة والقوية، يمكنك بسهولة **حفظ CAD بصيغة PNG** مع تصدير كائنات OLE من ملفات CAD باستخدام Aspose.CAD for Java. تُعد هذه الأداة المتعددة الاستخدامات وسيلة تمكين للمطورين لإدارة بيانات CAD بفعالية، مما يفتح آفاقًا جديدة في تطوير تطبيقات CAD وتدفقات العمل القائمة على الصور.

---

**آخر تحديث:** 2026-03-02  
**تم الاختبار مع:** Aspose.CAD for Java 24.12  
**المؤلف:** Aspose  

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}