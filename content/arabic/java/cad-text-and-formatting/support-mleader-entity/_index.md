---
title: دعم كيان MLeader لتنسيق DWG مع Aspose.CAD لـ Java
linktitle: دعم كيان MLeader لتنسيق DWG مع Java
second_title: Aspose.CAD جافا API
description: أطلق العنان لقوة Aspose.CAD لـ Java من خلال برنامجنا التعليمي خطوة بخطوة حول دعم كيانات MLeader بتنسيق DWG.
type: docs
weight: 12
url: /ar/java/cad-text-and-formatting/support-mleader-entity/
---
## مقدمة

في مجال التصميم بمساعدة الكمبيوتر (CAD) باستخدام Java، يعد فهم وتنفيذ الدعم لكيانات MLeader بتنسيق DWG مهارة قيمة. يوفر Aspose.CAD for Java حلاً قويًا لمثل هذه المهام، حيث يقدم مجموعة من الأدوات والوظائف القوية. سيرشدك هذا البرنامج التعليمي خلال عملية دعم كيانات MLeader داخل ملفات DWG باستخدام Java مع Aspose.CAD.

## المتطلبات الأساسية

قبل أن نتعمق في البرنامج التعليمي، تأكد من توفر المتطلبات الأساسية التالية:

1. بيئة تطوير Java: تأكد من إعداد بيئة تطوير Java على نظامك.

2.  مكتبة Aspose.CAD: قم بتنزيل وتثبيت مكتبة Aspose.CAD لـ Java من[رابط التحميل](https://releases.aspose.com/cad/java/).

## استيراد مساحات الأسماء

في مشروع Java الخاص بك، قم باستيراد مساحات الأسماء اللازمة للاستفادة من إمكانيات Aspose.CAD بشكل فعال. قم بتضمين الأسطر التالية في التعليمات البرمجية الخاصة بك:

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

الآن، دعنا نقسم التعليمات البرمجية إلى دليل خطوة بخطوة لدعم كيانات MLeader لتنسيق DWG باستخدام Java مع Aspose.CAD.

## 1. قم بتحميل ملف DWG والوصول إلى CadImage

```java
String dataDir = "Your Document Directory" + "DWGDrawings/";
String file = dataDir + "Multileaders.dwg";
Image image = Image.load(file);
CadImage cadImage = (CadImage) image;
```

## 2. التحقق من صحة كيانات MLeader

```java
Assert.areNotEqual(cadImage.getEntities().length, 0);
CadMLeader cadMLeader = (CadMLeader) cadImage.getEntities()[2];
```

### 3. تحقق من نمط وسمات MLeader

```java
Assert.areEqual(cadMLeader.getStyleDescription(), "Standard");
Assert.areEqual(cadMLeader.getLeaderStyleId(), "12E");
Assert.areEqual(cadMLeader.getArrowHeadId1(), "639");
Assert.areEqual(cadMLeader.getLeaderLineTypeID(), "14");
```

## 4. الوصول إلى بيانات سياق MLeader

```java
CadMLeaderContextData context = cadMLeader.getContextData();
```

## 5. التحقق من صحة سمات السياق

```java
Assert.areEqual(context.getArrowHeadSize(), 30.0, 0.1);
Assert.areEqual(context.getBasePoint().getX(), 481, 1);
Assert.areEqual(context.getContentScale(), 1.0, 0.01);
Assert.areEqual(context.getDefaultText().getValue(), "This is multileader with huge text\\P{\\H1.5x;6666666666666666666666666666\\P}bbbbbbbbbbbbbbbbbbbbbbbbbbbbbbbbbbb");
Assert.areEqual(context.hasMText(), true);
```

## 6. الوصول إلى عقدة MLeader وخط القائد

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

## 7. التحقق من صحة سمات MLleader الإضافية

```java
Assert.areEqual(Integer.toString(mleaderNode.getBranchIndex()), Integer.toString(0));
Assert.areEqual(mleaderNode.getDogLegLength(), 8.0, 0.1);
Assert.areEqual(context.hasMText(), true);
```

## 8. التحقق من صحة سمات النص

```java
Assert.areEqual(context.getTextAttachmentType().getValue(), (short) 1);
Assert.areEqual(context.getTextBackgroundColor().getValue(), 18);
Assert.areEqual(context.getTextHeight(), 20.0, 0.1);
Assert.areEqual(context.getTextStyleID().getValue(), "11");
Assert.areEqual(context.getTextRotation().getValue(), 0.0, 0.01);
```

## 9. سمات MLleader الإضافية

```java
Assert.areEqual(cadMLeader.getArrowHeadId1(), "639");
Assert.areEqual(cadMLeader.getLeaderType(), 1);
Assert.areEqual(cadMLeader.getBlockContentColor(), 0);
Assert.areEqual(cadMLeader.getLeaderLineColor(), 0);
Assert.areEqual(cadMLeader.getTextHeight(), 1.0, 0.01);
```

## خاتمة

تهانينا! لقد نجحت في التنقل عبر الدليل الشامل حول دعم كيانات MLeader لتنسيق DWG باستخدام Java وAspose.CAD. تفتح هذه الإمكانية الأبواب أمام معالجات CAD المتقدمة وتعزز مجموعة أدوات تطوير Java لديك.

## الأسئلة الشائعة

### س1: هل يمكنني استخدام Aspose.CAD لـ Java مع تنسيقات CAD الأخرى؟

ج1: نعم، يدعم Aspose.CAD تنسيقات CAD المتنوعة بخلاف DWG، مما يوفر تنوعًا في مشروعاتك.

### س2: أين يمكنني العثور على الوثائق التفصيلية الخاصة بـ Aspose.CAD لـ Java؟

 ج2: راجع[توثيق](https://reference.aspose.com/cad/java/) للحصول على رؤى متعمقة حول قدرات Aspose.CAD.

### س3: هل هناك نسخة تجريبية مجانية متاحة؟

 ج3: نعم، استكشف الوظائف بشكل مباشر باستخدام[تجربة مجانية](https://releases.aspose.com/).

### س4: كيف يمكنني الحصول على ترخيص مؤقت لـ Aspose.CAD؟

ج4: الحصول على ترخيص مؤقت من خلال[هذا الرابط](https://purchase.aspose.com/temporary-license/).

### س5: أين يمكنني طلب الدعم والمساعدة المجتمعية؟

ج5: قم بزيارة[منتدى Aspose.CAD](https://forum.aspose.com/c/cad/19) للتواصل مع المجتمع والحصول على المساعدة.