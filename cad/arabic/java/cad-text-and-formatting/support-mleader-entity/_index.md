---
date: 2026-01-10
description: تعلم كيفية قراءة ملفات DWG وإنشاء كيانات DWG متعددة القادة باستخدام Aspose.CAD
  للغة Java في هذا الدرس خطوة بخطوة.
linktitle: Support MLeader Entity for DWG Format with Java
second_title: Aspose.CAD Java API
title: كيفية قراءة DWG ودعم MLeader باستخدام Aspose.CAD للـ Java
url: /ar/java/cad-text-and-formatting/support-mleader-entity/
weight: 12
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# كيفية قراءة ملفات DWG ودعم MLeader باستخدام Aspose.CAD للـ Java

## المقدمة

إذا كنت بحاجة إلى **قراءة ملفات DWG** والعمل مع **كائنات multileader DWG** في تطبيق Java، فقد وصلت إلى المكان الصحيح. يوفر لك Aspose.CAD للـ Java طريقة برمجية نظيفة لفتح رسومات DWG، وفحص كائنات MLeader، والتحقق من خصائصها—كل ذلك دون الحاجة إلى محطة CAD متكاملة. في هذا البرنامج التعليمي سنستعرض كل خطوة، من تحميل ملف DWG إلى التأكد من أن بيانات الـ multileader تتطابق مع النمط المتوقع.

## إجابات سريعة
- **ما الذي يتضمنه “كيفية قراءة DWG”؟** تحميل الـ DWG باستخدام `Image.load()` وتحويله إلى `CadImage`.
- **هل يمكنني إنشاء كائنات multileader DWG؟** نعم – يمكنك إضافة، تعديل، والتحقق من كائنات MLeader باستخدام واجهة CadMLeader API.
- **ما نسخة المكتبة المطلوبة؟** أي إصدار حديث من Aspose.CAD للـ Java (الواجهة البرمجية المعروضة تعمل مع الإصدارات 2024+).
- **هل أحتاج إلى ترخيص للتطوير؟** ترخيص مؤقت يكفي للاختبار؛ الترخيص الكامل مطلوب للإنتاج.
- **هل الشيفرة متعددة المنصات؟** بالتأكيد – Java تعمل على Windows وLinux وmacOS.

## ما هو “كيفية قراءة DWG” باستخدام Aspose.CAD؟

قراءة ملف DWG تعني تحويل الرسم الثنائي إلى كائن `CadImage` في الذاكرة. بمجرد حصولك على هذا الكائن، يمكنك تعداد الكيانات (خطوط، دوائر، نص، كائنات **MLeader**، إلخ) وفحص خصائصها.

## لماذا دعم كائنات MLeader؟

كائنات MLeader (multileader) تجمع بين خطوط القائد والنص أو الكتل المرفقة، مما يجعلها أساسية للتعليقات التوضيحية في الرسومات الهندسية. دعمها يتيح لك:

- التحقق من أن التعليقات التوضيحية تتوافق مع معايير الشركة.
- استخراج النص للمعالجة اللاحقة (مثل إنشاء قوائم المواد).
- تعديل أنماط القائد برمجياً أو استبدال محتوى الكتل.

## المتطلبات المسبقة

قبل البدء، تأكد من وجود ما يلي:

1. **بيئة تطوير Java** – JDK 11+ وأي IDE مفضلة (IntelliJ, Eclipse, VS Code).  
2. **Aspose.CAD للـ Java** – حمّل أحدث ملف JAR من [رابط التحميل](https://releases.aspose.com/cad/java/).  

## استيراد الحزم

أضف الاستيرادات التالية إلى فئة Java الخاصة بك لتتمكن من العمل مع كائنات DWG وخيارات الرستر:

```java
import com.aspose.cad.Image;

import com.aspose.cad.fileformats.cad.CadImage;
import com.aspose.cad.fileformats.cad.cadobjects.CadMLeader;
import com.aspose.cad.fileformats.cad.cadobjects.CadMLeaderContextData;
import com.aspose.cad.fileformats.cad.cadobjects.CadMLeaderLine;
import com.aspose.cad.fileformats.cad.cadobjects.CadMLeaderNode;
import com.aspose.cad.imageoptions.CadRasterizationOptions;
import com.aspose.cad.imageoptions.PdfOptions;
```

## كيفية قراءة ملفات DWG باستخدام Aspose.CAD للـ Java

### الخطوة 1: تحميل ملف DWG والحصول على `CadImage`

```java
String dataDir = "Your Document Directory" + "DWGDrawings/";
String file = dataDir + "Multileaders.dwg";
Image image = Image.load(file);
CadImage cadImage = (CadImage) image;
```

### الخطوة 2: التحقق من أن الرسم يحتوي على كائنات MLeader

```java
Assert.areNotEqual(cadImage.getEntities().length, 0);
CadMLeader cadMLeader = (CadMLeader) cadImage.getEntities()[2];
```

### الخطوة 3: التحقق من نمط MLeader والخصائص الأساسية

```java
Assert.areEqual(cadMLeader.getStyleDescription(), "Standard");
Assert.areEqual(cadMLeader.getLeaderStyleId(), "12E");
Assert.areEqual(cadMLeader.getArrowHeadId1(), "639");
Assert.areEqual(cadMLeader.getLeaderLineTypeID(), "14");
```

### الخطوة 4: الوصول إلى بيانات سياق MLeader (قلب الـ multileader)

```java
CadMLeaderContextData context = cadMLeader.getContextData();
```

### الخطوة 5: التحقق من خصائص المستوى السياقي

```java
Assert.areEqual(context.getArrowHeadSize(), 30.0, 0.1);
Assert.areEqual(context.getBasePoint().getX(), 481, 1);
Assert.areEqual(context.getContentScale(), 1.0, 0.01);
Assert.areEqual(context.getDefaultText().getValue(),
    "This is multileader with huge text\\P{\\H1.5x;6666666666666666666666666666\\P}bbbbbbbbbbbbbbbbbbbbbbbbbbbbbbbbbbb");
Assert.areEqual(context.hasMText(), true);
```

### الخطوة 6: العمل مع عقدة MLeader وخط القائد الخاص بها

```java
CadMLeaderNode mleaderNode = context.getLeaderNode();
Assert.areEqual(mleaderNode.getLastLeaderLinePoint().getX(), 473, 1);

CadMLeaderLine leaderLine = mleaderNode.getLeaderLine();
Assert.areEqual(leaderLine.getBreakEndPoint().toString(), null);
Assert.areEqual(Integer.toString(leaderLine.getBreakPointIndex().getValue()), Integer.toString(0));
Assert.areEqual(leaderLine.getBreakStartPoint().toString(), null);
Assert.areEqual(Integer.toString(leaderLine.getLeaderLineIndex().getValue()), Integer.toString(0));
Assert.areEqual(Integer.toString(leaderLine.getLeaderPoints().size()), Integer.toString(4));
```

### الخطوة 7: التحقق من خصائص إضافية لعقدة MLeader

```java
Assert.areEqual(Integer.toString(mleaderNode.getBranchIndex()), Integer.toString(0));
Assert.areEqual(mleaderNode.getDogLegLength(), 8.0, 0.1);
Assert.areEqual(context.hasMText(), true);
```

### الخطوة 8: فحص الخصائص المتعلقة بالنص

```java
Assert.areEqual(context.getTextAttachmentType().getValue(), (short) 1);
Assert.areEqual(context.getTextBackgroundColor().getValue(), 18);
Assert.areEqual(context.getTextHeight(), 20.0, 0.1);
Assert.areEqual(context.getTextStyleID().getValue(), "11");
Assert.areEqual(context.getTextRotation().getValue(), 0.0, 0.01);
```

### الخطوة 9: مراجعة خصائص MLeader الأخرى للتأكد من الاكتمال

```java
Assert.areEqual(cadMLeader.getArrowHeadId1(), "639");
Assert.areEqual(cadMLeader.getLeaderType(), 1);
Assert.areEqual(cadMLeader.getBlockContentColor(), 0);
Assert.areEqual(cadMLeader.getLeaderLineColor(), 0);
Assert.areEqual(cadMLeader.getTextHeight(), 1.0, 0.01);
```

## المشكلات الشائعة والحلول

| المشكلة | سبب حدوثها | الحل |
|---------|------------|------|
| `ClassCastException` عند تحويل الكيان | الفهرس المختار ليس كائن MLeader. | تحقق من `cadImage.getEntities()[i] instanceof CadMLeader` قبل التحويل. |
| قيم `null` لنقاط خط القائد | الرسم يستخدم نمط قائد مخصص غير مدعوم بالكامل. | استخدم أحدث نسخة من Aspose.CAD أو عُد إلى النمط الافتراضي للاختبار. |
| فشل التأكيدات على القيم الرقمية | اختلافات طفيفة في التقريب بين إصدارات CAD. | عدّل التسامح في `Assert.areEqual(..., delta)` كما هو موضح في الأمثلة. |

## الأسئلة المتكررة

**س: هل يمكنني استخدام Aspose.CAD للـ Java مع صيغ CAD أخرى؟**  
ج: نعم، يدعم Aspose.CAD صيغ DXF، DWF، DGN، وعدة صيغ رسترية بالإضافة إلى DWG.

**س: أين يمكنني العثور على الوثائق التفصيلية لـ Aspose.CAD للـ Java؟**  
ج: راجع [الوثائق الرسمية](https://reference.aspose.com/cad/java/) للحصول على تفاصيل API وعينات الشيفرة.

**س: هل هناك نسخة تجريبية مجانية متاحة؟**  
ج: بالتأكيد – يمكنك تنزيل نسخة تجريبية من صفحة [التجربة المجانية](https://releases.aspose.com/).

**س: كيف أحصل على ترخيص مؤقت للاختبار؟**  
ج: احصل على ترخيص مؤقت عبر [رابط الترخيص المؤقت](https://purchase.aspose.com/temporary-license/).

**س: أين يمكنني طلب المساعدة من المجتمع؟**  
ج: منتدى [Aspose.CAD](https://forum.aspose.com/c/cad/19) هو أفضل مكان لمشاركة الأسئلة والحلول.

## الخاتمة

الآن لديك دليل شامل من البداية إلى النهاية حول **كيفية قراءة ملفات DWG** و**إنشاء كائنات multileader DWG** باستخدام Aspose.CAD للـ Java. باتباع الخطوات أعلاه، يمكنك التحقق من أنماط MLeader، استخراج بيانات التعليقات التوضيحية، ودمج معالجة DWG في أي سير عمل مبني على Java.

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}

---

**آخر تحديث:** 2026-01-10  
**تم الاختبار مع:** Aspose.CAD 24.11 للـ Java  
**المؤلف:** Aspose