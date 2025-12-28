---
date: 2025-12-28
description: تعلم كيفية قراءة ملفات DWG باستخدام Aspose.CAD للغة Java وقم بسرد تخطيطات
  ملفات DWG بسهولة. دمج وظائف CAD القوية في تطبيقات Java الخاصة بك.
linktitle: List Layouts in DWG
second_title: Aspose.CAD Java API
title: كيفية قراءة ملفات DWG وعرض التخطيطات في DWG باستخدام Aspose.CAD للـ Java
url: /ar/java/cad-file-manipulation/list-layouts-in-dwg/
weight: 12
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# كيفية قراءة ملفات DWG وإدراج التخطيطات في DWG باستخدام Aspose.CAD للـ Java

## المقدمة

إذا كنت بحاجة إلى **قراءة DWG** برمجيًا واستخراج معلومات مثل أسماء التخطيطات، فإن Aspose.CAD للـ Java يجعل ذلك سهلًا. في هذا الدرس خطوة بخطوة سنوضح لك **كيفية قراءة DWG** وإدراج جميع التخطيطات الموجودة في ملف DWG (أو DXF). في نهاية الدليل ستكون قادرًا على إضافة هذه القدرة إلى أي تطبيق Java يعمل مع بيانات CAD.

## إجابات سريعة
- **ما المكتبة المطلوبة؟** Aspose.CAD للـ Java.
- **هل يمكنني قراءة ملفات DWG على أي نظام تشغيل؟** نعم – Java متعدد المنصات.
- **هل أحتاج إلى ترخيص لتشغيل العينة؟** النسخة التجريبية المجانية تكفي للتقييم؛ الترخيص مطلوب للإنتاج.
- **ما صيغ CAD المدعومة؟** DWG، DXF، DWF، وغيرها.
- **هل الكود متوافق مع Java 8+؟** بالتأكيد.

## ما هو “كيفية قراءة dwg” في Java؟

قراءة ملف DWG يعني تحميل بيانات CAD الثنائية إلى نموذج كائن يمكنك الاستعلام منه. Aspose.CAD يُجرد بنية DWG المعقدة خلف فئات .NET/Java بسيطة، مما يتيح لك التركيز على المعلومات التي تحتاجها – في هذه الحالة، أسماء التخطيطات.

## لماذا يتم إدراج التخطيطات في ملف DWG؟

يمكن أن يحتوي DWG على عدة تخطيطات (مساحة الورق، مساحة النموذج، أوراق مخصصة). معرفة أسماء التخطيطات تمكنك من:
- إنشاء تقارير لكل تخطيط.
- تصدير تخطيطات محددة إلى صور أو ملفات PDF.
- أتمتة معالجة دفعات من الرسومات.

## المتطلبات المسبقة

قبل الغوص في الكود، تأكد من أن لديك ما يلي:

- **مكتبة Aspose.CAD للـ Java** – قم بتنزيل أحدث JAR من [الموقع](https://releases.aspose.com/cad/java/).
- **بيئة تطوير Java** – JDK 8 أو أعلى، وIDE أو أداة بناء من اختيارك.

## استيراد المساحات الاسمية

في ملف Java المصدر الخاص بك، استورد الفئات المطلوبة من Aspose.CAD:

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

استبدل **“Your Document Directory”** بالمسار المطلق حيث توجد ملفات CAD الخاصة بك.

## الخطوة 2: تحميل ملف DWG

```java
String sourceFilePath = dataDir + "conic_pyramid.dxf";
Image image = Image.load(sourceFilePath);
CadImage cadImage = (CadImage)image;
```

طريقة `Image.load` تكتشف تنسيق الملف تلقائيًا، لذا يمكنك استخدام نفس الكود لكل من ملفات **DWG** و **DXF**.

## الخطوة 3: الحصول على التخطيطات وطباعة الأسماء

```java
CadLayoutDictionary layouts = cadImage.getLayouts();
for (CadLayout layout : layouts.getValues())
{
    System.out.println("Layout " + layout.getLayoutName());
}
```

الحلقة تتكرر على كل كائن تخطيط وتطبع اسمه إلى وحدة التحكم – طريقة بسيطة للتحقق من أنك نجحت في **قراءة DWG** واستخراج معلومات التخطيط.

## المشكلات الشائعة والنصائح

- **مسار ملف غير صحيح** – تحقق مرة أخرى من أن `dataDir` ينتهي بفاصل (`/` أو `\\`) المناسب لنظام التشغيل الخاص بك.
- **إصدار DWG غير مدعوم** – تأكد من أنك تستخدم نسخة حديثة من Aspose.CAD؛ قد تحتاج الإصدارات القديمة من DWG إلى تحويل.
- **استخدام الذاكرة** – الرسومات الكبيرة قد تستهلك ذاكرة كبيرة. قم بتحرير كائن `CadImage` عند الانتهاء: `cadImage.dispose();`.

## الخاتمة

تهانينا! الآن تعرف **كيفية قراءة DWG** وإدراج تخطيطاتها باستخدام Aspose.CAD للـ Java. تشكل هذه التقنية الأساس لأتمتة CAD المتقدمة، مثل تصدير تخطيطات محددة إلى صور أو ملفات PDF. للمزيد من الاستكشاف، راجع [الوثائق](https://reference.aspose.com/cad/java/) الرسمية.

## الأسئلة المتكررة

### س1: هل يمكنني استخدام Aspose.CAD للـ Java مع صيغ CAD أخرى؟

نعم، يدعم Aspose.CAD صيغ CAD متعددة، بما في ذلك DWG، DXF، DWF، وغيرها.

### س2: هل تتوفر نسخة تجريبية مجانية لـ Aspose.CAD للـ Java؟

نعم، يمكنك الحصول على نسخة تجريبية مجانية من [هنا](https://releases.aspose.com/).

### س3: أين يمكنني الحصول على دعم المجتمع لـ Aspose.CAD للـ Java؟

قم بزيارة [منتدى Aspose.CAD](https://forum.aspose.com/c/cad/19) للحصول على دعم المجتمع.

### س4: كيف يمكنني شراء ترخيص لـ Aspose.CAD للـ Java؟

يمكنك شراء ترخيص من [صفحة الشراء](https://purchase.aspose.com/buy).

### س5: هل يمكنني استخدام ترخيص مؤقت لأغراض الاختبار؟

نعم، يمكنك الحصول على ترخيص مؤقت من [هنا](https://purchase.aspose.com/temporary-license/).

**أسئلة إضافية**

**س: هل يعمل هذا النهج لقراءة ملفات DWG على لينكس؟**  
**ج:** بالتأكيد. بما أن الحل مكتوب بالكامل بلغة Java، فهو يعمل على أي نظام تشغيل يحتوي على JDK متوافق.

**س: هل يمكنني قراءة ملف DWG دون تحميل الرسم بالكامل في الذاكرة؟**  
**ج:** Aspose.CAD يحمل الرسم في الذاكرة؛ بالنسبة للملفات الكبيرة جدًا، فكر في معالجتها في خيوط منفصلة أو استخدام واجهات برمجة تطبيقات البث إذا كانت متاحة في الإصدارات المستقبلية.

**س: هل هناك طريقة لتصفية التخطيطات حسب الاسم؟**  
**ج:** نعم – بعد استرجاع `CadLayoutDictionary`، يمكنك التحقق من `layout.getLayoutName().equalsIgnoreCase("MyLayout")` قبل المعالجة.

---

**آخر تحديث:** 2025-12-28  
**تم الاختبار مع:** Aspose.CAD للـ Java 24.11  
**المؤلف:** Aspose  

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}