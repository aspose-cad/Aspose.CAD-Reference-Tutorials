---
date: 2025-12-22
description: تعرّف على كيفية تحميل ملف DWG واستخراج معلومات الطبقة السفلية باستخدام
  Aspose.CAD للغة Java – دليل خطوة بخطوة يغطي علامات الطبقة السفلية.
linktitle: Accessing Underlay Flags of DWG
second_title: Aspose.CAD Java API
title: تحميل ملف DWG والوصول إلى أعلام الطبقة السفلية – Aspose.CAD للـ Java
url: /ar/java/cad-file-manipulation/accessing-underlay-flags-of-dwg/
weight: 11
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# تحميل ملف DWG والوصول إلى أعلام Underlay – Aspose.CAD للـ Java

في سير عمل CAD الحديث، **تحميل ملف DWG** بسرعة واستخراج تفاصيل الـ underlay هو مطلب شائع. سواءً كنت تبني عارضًا، أو تقوم بأتمتة معالجة دفعات، أو تستخرج البيانات الوصفية لتكامل GIS، فإن Aspose.CAD للـ Java يوفّر لك طريقة نظيفة تعتمد على الكود للقيام بذلك. في هذا الدرس سنستعرض الخطوات الدقيقة لـ **تحميل ملف DWG**، وتكرار الكيانات الخاصة به، وقراءة أعلام الـ underlay التي يتغاضى عنها العديد من المطورين.

## إجابات سريعة
- **ما هو الصنف الأساسي لفتح ملف DWG؟** `com.aspose.cad.Image.load()` يُعيد `CadImage`.
- **أي كائن يحمل معلومات الـ underlay؟** `CadUnderlay` (أو الأنواع المشتقة مثل `CadDgnUnderlay`).
- **هل أحتاج إلى ترخيص للتطوير؟** نسخة تجريبية مجانية تعمل للاختبار؛ الترخيص التجاري مطلوب للإنتاج.
- **هل يمكنني معالجة ملفات DWG متعددة في حلقة؟** نعم – فقط كرّر نمط التحميل‑والتكرار.
- **هل هذا النهج متوافق مع Java 11+؟** بالتأكيد، Aspose.CAD يدعم Java 8 وحتى أحدث إصدارات LTS.

## ما هو “load dwg file” في Aspose.CAD؟
`Image.load()` يقرأ محتوى DWG الثنائي ويُنشئ كائن `CadImage` في الذاكرة. من هناك يمكنك استكشاف الطبقات، الكتل، وكيانات الـ underlay دون الحاجة للتعامل مع تنسيق ملف DWG بنفسك.

## لماذا استخراج أعلام الـ underlay من ملف DWG؟
تخبرك أعلام الـ underlay كيف يتم وضع مرجع خارجي (مثل DGN أو PDF underlay) وتكبيره وتدويره داخل الرسم. معرفة هذه القيم تتيح لك:
- إعادة إنشاء التخطيط البصري الدقيق في عارض مخصص.
- تحويل الـ underlays إلى كيانات CAD أصلية للمزيد من التحرير.
- إنشاء تقارير تتضمن بيانات الـ underlay الوصفية للامتثال أو التوثيق.

## المتطلبات المسبقة
- **مكتبة Aspose.CAD** – حمّلها من صفحة [الإصدارات](https://releases.aspose.com/cad/java/).
- **مجموعة تطوير Java** – JDK 8 أو أحدث.
- **مجلد** يحتوي على ملفات DWG التي تريد تحليلها. استبدل `"Your Document Directory"` في الشيفرة بالمسار الفعلي الخاص بك.

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
حدد مكان وجود ملفات DWG الخاصة بك. استخدام مجلد مخصص يحافظ على العينة نظيفة وقابلة للنقل.

### الخطوة 2: تحميل ملف DWG
```java
// Input file name and path
String fileName = dataDir + "BlockRefDgn.dwg";

// Load an existing DWG file and convert it into CadImage 
CadImage image = (CadImage)Image.load(fileName);
```
هنا نقوم **بتحميل ملف DWG** `BlockRefDgn.dwg` إلى كائن `CadImage`، جاهز للفحص.

### الخطوة 3: تكرار كيانـات DWG
```java
// Go through each entity inside the DWG file
for(CadBaseEntity entity : image.getEntities())
```
تقوم الحلقة بزيارة كل كيان — خطوط، دوائر، كتل، وunderlays — حتى نتمكن من اختيار ما نحتاجه.

### الخطوة 4: تحديد كيانـات CadDgnUnderlay
```java
// Check if entity is of CadDgnUnderlay type
if (entity instanceof CadDgnUnderlay)
```
فقط كائنات `CadDgnUnderlay` تحتوي على أعلام الـ underlay التي نبحث عنها، لذا نقوم بفلترتها.

### الخطوة 5: الوصول إلى معلومات الـ Underlay
```java
// Access different underlay flags 
CadUnderlay underlay = (CadUnderlay) entity;
System.out.println(underlay.getUnderlayPath());
System.out.println(underlay.getUnderlayName());
// ... (Additional underlay properties)
break;
```
بمجرد حصولنا على كائن `CadUnderlay`، يمكننا قراءة مساره، اسمه، نقطة الإدراج، الدوران، عوامل القياس، وتعداد `UnderlayFlags` الذي يحدد الرؤية، القص، وغيرها من خيارات العرض.

## المشكلات الشائعة والنصائح
- **مسار underlay فارغ** – تأكد من أن ملف DWG يشير فعليًا إلى ملف خارجي؛ وإلا سيكون المسار فارغًا.
- **نوع underlay غير مدعوم** – Aspose.CAD يدعم حاليًا underlays من نوع DGN؛ تحتـيات PDF لم تُعرَض بعد عبر الـ API.
- **استثناءات الترخيص** – تشغيل الشيفرة بدون ترخيص صالح سيضيف علامة مائية إلى أي صور مُصدَّرة.

## الأسئلة المتكررة

**س: هل يمكنني استخدام Aspose.CAD للـ Java مع صيغ CAD أخرى؟**  
ج: يركز Aspose.CAD أساسًا على صيغة DWG، لكنه يدعم أيضًا DXF، DWF، وصيغ CAD أخرى.

**س: هل هناك نسخة تجريبية متاحة لـ Aspose.CAD للـ Java؟**  
ج: نعم، يمكنك استكشاف الميزات عبر نسخة تجريبية مجانية من [هنا](https://releases.aspose.com/).

**س: كيف يمكنني الحصول على الدعم أو طلب المساعدة بخصوص Aspose.CAD للـ Java؟**  
ج: زر [منتدى Aspose.CAD](https://forum.aspose.com/c/cad/19) للحصول على دعم المجتمع والنقاشات.

**س: هل تتوفر تراخيص مؤقتة لـ Aspose.CAD للـ Java؟**  
ج: نعم، يمكنك الحصول على ترخيص مؤقت [من هنا](https://purchase.aspose.com/temporary-license/).

**س: أين يمكنني العثور على الوثائق الشاملة لـ Aspose.CAD للـ Java؟**  
ج: راجع [الوثائق](https://reference.aspose.com/cad/) للحصول على معلومات مفصلة.

---

**آخر تحديث:** 2025-12-22  
**تم الاختبار مع:** Aspose.CAD 24.12 للـ Java  
**المؤلف:** Aspose  

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}