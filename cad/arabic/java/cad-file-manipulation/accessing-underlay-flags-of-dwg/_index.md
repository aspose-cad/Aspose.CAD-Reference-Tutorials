---
date: 2026-02-23
description: تعلم كيفية تحميل ملفات DWG باستخدام Aspose.CAD DWG للغة Java واستخراج
  أعلام التحتية – دليل خطوة بخطوة للمطورين.
linktitle: Accessing Underlay Flags of DWG
second_title: Aspose.CAD Java API
title: aspose cad dwg – تحميل DWG والوصول إلى علامات Underlay (Java)
url: /ar/java/cad-file-manipulation/accessing-underlay-flags-of-dwg/
weight: 11
---

 to keep shortcodes unchanged.

Now produce final content.{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# تحميل ملف DWG والوصول إلى علامات التحتية – Aspose.CAD للـ Java

في سير عمل CAD الحديث، **مع aspose cad dwg يمكنك بسرعة تحميل ملف DWG** واستخراج تفاصيل التحتية التي غالبًا ما تكون مخفية عن المشاهدين العاديين. سواء كنت تبني عارض DWG للـ Java، أو تقوم بأتمتة عملية دفعة dwg، أو تستخرج البيانات الوصفية لتكامل GIS، فإن Aspose.CAD للـ Java يمنحك طريقة نظيفة تعتمد على الكود للقيام بذلك. في هذا البرنامج التعليمي سنستعرض الخطوات الدقيقة **لتحميل ملف DWG**، وتكرار كياناته، وقراءة علامات التحتية التي يتغافل عنها العديد من المطورين.

## إجابات سريعة
- **ما هو الصنف الأساسي لفتح ملف DWG؟** `com.aspose.cad.Image.load()` يُعيد `CadImage`.
- **أي كائن يحمل معلومات التحتية؟** `CadUnderlay` (أو الأنواع المشتقة مثل `CadDgnUnderlay`).
- **هل أحتاج إلى ترخيص للتطوير؟** النسخة التجريبية المجانية تعمل للاختبار؛ يلزم ترخيص تجاري للإنتاج.
- **هل يمكنني معالجة ملفات DWG متعددة في حلقة؟** نعم – فقط كرّر نمط التحميل‑والتكرار.
- **هل هذه الطريقة متوافقة مع Java 11+؟** بالتأكيد، Aspose.CAD يدعم Java 8 وحتى أحدث إصدارات LTS.

## aspose cad dwg – تحميل ملف DWG (Java)

`Image.load()` يقرأ محتوى DWG الثنائي ويُنشئ كائن `CadImage` في الذاكرة. من هناك يمكنك استكشاف الطبقات، الكتل، وكيانات التحتية دون الحاجة للتعامل مع تنسيق ملف DWG بنفسك.

## لماذا استخراج علامات التحتية من ملف DWG؟

علامات التحتية تخبرك كيف يتم وضع مرجع خارجي (مثل تحتية DGN أو PDF) وتكبيره وتدويره داخل الرسم. معرفة هذه القيم تتيح لك:
- إعادة إنشاء التخطيط البصري الدقيق في **عارض java dwg** مخصص.
- تحويل التحتيات إلى كيانات CAD أصلية لمزيد من التحرير.
- إنشاء تقارير تتضمن بيانات التحتية للامتثال أو التوثيق.
- **معالجة دفعة dwg** للملفات وتخزين بيانات التحتية في قاعدة بيانات للتحليل لاحقًا.

## المتطلبات المسبقة
- **مكتبة Aspose.CAD** – حمّلها من صفحة [الإصدارات](https://releases.aspose.com/cad/java/).  
- **مجموعة تطوير Java** – JDK 8 أو أحدث.  
- **مجلد** يحتوي على ملفات DWG التي تريد تحليلها. استبدل `"Your Document Directory"` في الكود بالمسار الفعلي الخاص بك.

## استيراد المساحات الاسمية

```java
import com.aspose.cad.Image;

import com.aspose.cad.fileformats.cad.CadImage;
import com.aspose.cad.fileformats.cad.cadobjects.CadBaseEntity;
import com.aspose.cad.fileformats.cad.cadobjects.CadDgnUnderlay;
import com.aspose.cad.fileformats.cad.cadobjects.CadUnderlay;
import com.aspose.cad.fileformats.cad.cadobjects.UnderlayFlags;
```

## دليل خطوة بخطوة

### الخطوة 1: تعيين دليل الموارد
```java
// The path to the resource directory.
String dataDir = "Your Document Directory" + "DWGDrawings/";
```
حدد موقع ملفات DWG الخاصة بك. استخدام مجلد مخصص يحافظ على العينة نظيفة وقابلة للنقل.

### الخطوة 2: تحميل ملف DWG
```java
// Input file name and path
String fileName = dataDir + "BlockRefDgn.dwg";

// Load an existing DWG file and convert it into CadImage 
CadImage image = (CadImage)Image.load(fileName);
```
هنا نقوم **بتحميل ملف dwg** `BlockRefDgn.dwg` إلى كائن `CadImage`، جاهز للفحص.

### الخطوة 3: تكرار كيانات DWG
```java
// Go through each entity inside the DWG file
for(CadBaseEntity entity : image.getEntities())
```
تقوم الحلقة بزيارة كل كائن—خطوط، دوائر، كتل، وتحتيات—حتى نتمكن من اختيار ما نحتاجه.

### الخطوة 4: تحديد كائنات CadDgnUnderlay
```java
// Check if entity is of CadDgnUnderlay type
if (entity instanceof CadDgnUnderlay)
```
فقط كائنات `CadDgnUnderlay` تحتوي على علامات التحتية التي نبحث عنها، لذا نقوم بفلترتها.

### الخطوة 5: الوصول إلى معلومات التحتية
```java
// Access different underlay flags 
CadUnderlay underlay = (CadUnderlay) entity;
System.out.println(underlay.getUnderlayPath());
System.out.println(underlay.getUnderlayName());
// ... (Additional underlay properties)
break;
```
بمجرد حصولنا على `CadUnderlay`، يمكننا قراءة مساره، اسمه، نقطة الإدراج، الدوران، عوامل المقياس، وتعداد `UnderlayFlags` الذي يحدد الرؤية، القص، وغيرها من خيارات العرض.

## كيفية تحميل ملفات dwg في عملية دفعة

إذا كنت بحاجة إلى **معالجة دفعة dwg** للملفات، غلف الخطوات السابقة في حلقة `for` بسيطة تتكرر على جميع الملفات في `dataDir`. نفس استدعاء `Image.load()` يعمل لكل ملف، ويمكنك تخزين العلامات المستخرجة في ملف CSV أو قاعدة بيانات للتقارير اللاحقة.

## المشكلات الشائعة والنصائح
- **مسار التحتية فارغ** – تأكد من أن ملف DWG يشير فعليًا إلى ملف خارجي؛ وإلا سيكون المسار فارغًا.
- **نوع التحتية غير مدعوم** – Aspose.CAD يدعم حاليًا تحتيات DGN؛ تحتيات PDF لم تُعرض بعد عبر الـ API.
- **استثناءات الترخيص** – تشغيل الكود بدون ترخيص صالح سيضيف علامة مائية على أي صور مُصدرة.
- **نصيحة الأداء:** أعد استخدام كائن `Image` واحد عند معالجة العديد من الملفات في دفعة لتقليل ضغط الـ GC.

## الأسئلة المتكررة

**س: هل يمكنني استخدام Aspose.CAD للـ Java مع صيغ CAD أخرى؟**  
ج: يركز Aspose.CAD أساسًا على صيغة DWG، لكنه يدعم أيضًا DXF، DWF، وصيغ CAD أخرى.

**س: هل هناك نسخة تجريبية متاحة لـ Aspose.CAD للـ Java؟**  
ج: نعم، يمكنك استكشاف الميزات من خلال نسخة تجريبية مجانية من [هنا](https://releases.aspose.com/).

**س: كيف يمكنني الحصول على الدعم أو المساعدة بخصوص Aspose.CAD للـ Java؟**  
ج: زر [منتدى Aspose.CAD](https://forum.aspose.com/c/cad/19) للحصول على دعم المجتمع والنقاشات.

**س: هل تتوفر تراخيص مؤقتة لـ Aspose.CAD للـ Java؟**  
ج: نعم، يمكنك الحصول على ترخيص مؤقت من [هنا](https://purchase.aspose.com/temporary-license/).

**س: أين يمكنني العثور على الوثائق الشاملة لـ Aspose.CAD للـ Java؟**  
ج: راجع [الوثائق](https://reference.aspose.com/cad/java/) للحصول على معلومات مفصلة.

---

**آخر تحديث:** 2026-02-23  
**تم الاختبار مع:** Aspose.CAD 24.12 للـ Java  
**المؤلف:** Aspose  

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}