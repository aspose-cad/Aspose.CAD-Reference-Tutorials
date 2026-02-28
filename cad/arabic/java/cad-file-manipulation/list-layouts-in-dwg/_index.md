---
date: 2026-02-28
description: تعرّف على كيفية قراءة ملفات DWG باستخدام Aspose.CAD للـ Java وقم بسرد
  التخطيطات في ملفات DWG بسهولة. دمج وظائف CAD القوية في تطبيقات Java الخاصة بك.
linktitle: List Layouts in DWG
second_title: Aspose.CAD Java API
title: كيفية قراءة ملفات DWG وإدراج التخطيطات في DWG باستخدام Aspose.CAD للـ Java
url: /ar/java/cad-file-manipulation/list-layouts-in-dwg/
weight: 12
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# كيفية قراءة ملفات DWG وإدراج التخطيطات في DWG باستخدام Aspose.CAD للـ Java

## مقدمة

إذا كنت تبحث عن طريقة موثوقة **كيفية قراءة dwg** برمجياً، فإن Aspose.CAD للـ Java يوفر واجهة برمجة تطبيقات نظيفة ومتعددة المنصات تتيح لك تحميل الرسم واستخراج أي معلومات تحتاجها—مثل أسماء جميع التخطيطات داخل الملف. في هذا الدرس خطوة بخطوة سنوضح لك **كيفية قراءة DWG** وإدراج كل تخطيط موجود في ملف DWG (أو DXF)، حتى تتمكن من دمج هذه القدرة في أي تطبيق Java يتعامل مع بيانات CAD.

## إجابات سريعة
- **ما المكتبة المطلوبة؟** Aspose.CAD للـ Java.  
- **هل يمكنني قراءة ملفات DWG على أي نظام تشغيل؟** نعم – Java متعددة المنصات، لذا يمكنك **قراءة dwg على لينكس** بسهولة كما على Windows.  
- **هل أحتاج إلى ترخيص لتشغيل العينة؟** النسخة التجريبية المجانية تكفي للتقييم؛ الترخيص مطلوب للإنتاج.  
- **ما صيغ CAD المدعومة؟** DWG، DXF، DWF، وغيرها.  
- **هل الكود متوافق مع Java 8+؟** بالتأكيد.

## ما هو “how to read dwg” في Java؟

قراءة ملف DWG تعني تحميل بيانات CAD الثنائية إلى نموذج كائن يمكنك الاستعلام عنه. تقوم Aspose.CAD بتجريد بنية DWG المعقدة خلف فئات Java بسيطة، مما يسمح لك بالتركيز على المعلومات التي تحتاجها – في هذه الحالة، أسماء التخطيطات.

## لماذا ندرج التخطيطات في ملف DWG؟

يمكن أن يحتوي DWG على عدة تخطيطات (مساحة الورق، مساحة النموذج، أوراق مخصصة). معرفة أسماء التخطيطات تمكنك من:

- إنشاء تقارير لكل تخطيط.  
- تصدير تخطيطات محددة إلى صور أو ملفات PDF.  
- أتمتة معالجة الرسومات على دفعات.  

## المتطلبات المسبقة

قبل الغوص في الكود، تأكد من توفر ما يلي:

- **مكتبة Aspose.CAD للـ Java** – حمّل أحدث ملف JAR من [الموقع](https://releases.aspose.com/cad/java/).  
- **بيئة تطوير Java** – JDK 8 أو أعلى، وIDE أو أداة بناء من اختيارك.

## استيراد المساحات الاسمية

في ملف المصدر Java الخاص بك، استورد فئات Aspose.CAD المطلوبة:

```java
import com.aspose.cad.Image;

import com.aspose.cad.fileformats.cad.CadImage;
import com.aspose.cad.fileformats.cad.CadLayoutDictionary;
import com.aspose.cad.fileformats.cad.cadobjects.CadLayout;
```

## الخطوة 1: إعداد دليل المستندات الخاص بك

```java
String dataDir = "Your Document Directory" + "CADConversion/";
```

استبدل **“Your Document Directory”** بالمسار المطلق حيث توجد ملفات CAD الخاصة بك. على Linux قد تستخدم مسارًا مثل `/home/user/cad/`.

## الخطوة 2: تحميل ملف DWG

```java
String sourceFilePath = dataDir + "conic_pyramid.dxf";
Image image = Image.load(sourceFilePath);
CadImage cadImage = (CadImage)image;
```

طريقة `Image.load` تكتشف صيغة الملف تلقائيًا، لذا يعمل نفس الكود لكل من ملفات **DWG** و**DXF**.

## الخطوة 3: الحصول على التخطيطات وطباعة الأسماء

```java
CadLayoutDictionary layouts = cadImage.getLayouts();
for (CadLayout layout : layouts.getValues())
{
    System.out.println("Layout " + layout.getLayoutName());
}
```

تتكرر الحلقة فوق كل كائن تخطيط وتطبع اسمه إلى وحدة التحكم – طريقة بسيطة للتحقق من أنك نجحت في **قراءة DWG** واستخراج معلومات التخطيط.

## كيفية تحويل DWG إلى PDF على Linux

إذا احتجت لاحقًا إلى تحويل تخطيط محدد إلى PDF، يمكن لـ Aspose.CAD عرض التخطيط كصورة ثم يمكنك استخدام Aspose.PDF (أو أي مكتبة PDF أخرى) لإدراج تلك الصورة في مستند PDF. كود التحويل هو نفسه على Linux لأن الواجهة برمجة التطبيقات هي Java صافية.

## المشكلات الشائعة والنصائح

- **مسار الملف غير صحيح** – تأكد من أن `dataDir` ينتهي بفاصل (`/` أو `\\`) مناسب لنظام التشغيل الخاص بك.  
- **إصدار DWG غير مدعوم** – تأكد من استخدام نسخة حديثة من Aspose.CAD؛ قد تحتاج إصدارات DWG القديمة إلى تحويل.  
- **استهلاك الذاكرة** – الرسومات الكبيرة قد تستهلك ذاكرة كبيرة. حرّر كائن `CadImage` عند الانتهاء: `cadImage.dispose();`.  
- **التشغيل على خوادم بدون واجهة** – لا تتطلب مكونات UI، لذا يعمل الكود على خوادم Linux بدون بيئة رسومية.

## الخلاصة

تهانينا! الآن تعرف **كيفية قراءة dwg** وإدراج تخطيطاتها باستخدام Aspose.CAD للـ Java. تشكل هذه التقنية الأساس لأتمتة CAD أكثر تقدماً، مثل تصدير تخطيطات محددة إلى صور، ملفات PDF، أو حتى تحويل DWG إلى PDF على Linux. للمزيد من الاستكشاف، راجع [التوثيق الرسمي](https://reference.aspose.com/cad/java/).

## الأسئلة المتكررة

**س1: هل يمكنني استخدام Aspose.CAD للـ Java مع صيغ CAD أخرى؟**  
ج1: نعم، يدعم Aspose.CAD صيغ CAD متعددة، بما في ذلك DWG، DXF، DWF، وأكثر.

**س2: هل هناك نسخة تجريبية مجانية متاحة لـ Aspose.CAD للـ Java؟**  
ج2: نعم، يمكنك الحصول على نسخة تجريبية مجانية من [هنا](https://releases.aspose.com/).

**س3: أين يمكنني الحصول على دعم المجتمع لـ Aspose.CAD للـ Java؟**  
ج3: زر [منتدى Aspose.CAD](https://forum.aspose.com/c/cad/19) للحصول على دعم المجتمع.

**س4: كيف أشتري ترخيصًا لـ Aspose.CAD للـ Java؟**  
ج4: يمكنك شراء ترخيص من [صفحة الشراء](https://purchase.aspose.com/buy).

**س5: هل يمكنني استخدام ترخيص مؤقت لأغراض الاختبار؟**  
ج5: نعم، يمكنك الحصول على ترخيص مؤقت [من هنا](https://purchase.aspose.com/temporary-license/).

**أسئلة إضافية**

**س: هل يعمل هذا النهج لقراءة ملفات DWG على Linux؟**  
ج: بالتأكيد. بما أن الحل مكتوب بالكامل بلغة Java، فهو يعمل على أي نظام تشغيل يحتوي على JDK متوافق.

**س: هل يمكنني قراءة ملف DWG دون تحميل الرسم بالكامل في الذاكرة؟**  
ج: يقوم Aspose.CAD بتحميل الرسم في الذاكرة؛ للملفات الكبيرة جدًا قد تحتاج إلى معالجتها في خيوط منفصلة أو استخدام واجهات تدفق إذا توفرت في إصدارات مستقبلية.

**س: هل هناك طريقة لتصفية التخطيطات حسب الاسم؟**  
ج: نعم – بعد استرجاع `CadLayoutDictionary`، يمكنك فحص `layout.getLayoutName().equalsIgnoreCase("MyLayout")` قبل المعالجة.

---

**آخر تحديث:** 2026-02-28  
**تم الاختبار مع:** Aspose.CAD للـ Java 24.11  
**المؤلف:** Aspose  

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}