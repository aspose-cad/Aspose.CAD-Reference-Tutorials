---
title: 使用 Aspose.CAD for Java 支援 DWG 格式的 MLeader 實體
linktitle: 使用 Java 支援 DWG 格式的 MLeader 實體
second_title: Aspose.CAD Java API
description: 透過我們有關支援 DWG 格式的 MLeader 實體的逐步教程，釋放 Aspose.CAD for Java 的強大功能。
weight: 12
url: /zh-hant/java/cad-text-and-formatting/support-mleader-entity/
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# 使用 Aspose.CAD for Java 支援 DWG 格式的 MLeader 實體

## 介紹

在使用 Java 的電腦輔助設計 (CAD) 領域，理解和實現對 DWG 格式的 MLeader 實體的支援是一項寶貴的技能。 Aspose.CAD for Java 為此類任務提供了強大的解決方案，提供了一組強大的工具和功能。本教學將引導您完成使用 Java 和 Aspose.CAD 支援 DWG 檔案中的 MLeader 實體的過程。

## 先決條件

在我們深入研究本教程之前，請確保您具備以下先決條件：

1. Java 開發環境：確保您的系統上設定了 Java 開發環境。

2.  Aspose.CAD 函式庫：從下列位置下載並安裝 Java 的 Aspose.CAD 函式庫：[下載連結](https://releases.aspose.com/cad/java/).

## 導入命名空間

在您的 Java 專案中，匯入必要的命名空間以有效利用 Aspose.CAD 的功能。在您的程式碼中包含以下行：

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

現在，讓我們將程式碼分解為逐步指南，以使用 Java 和 Aspose.CAD 支援 DWG 格式的 MLeader 實體。

## 1.載入DWG檔並存取CadImage

```java
String dataDir = "Your Document Directory" + "DWGDrawings/";
String file = dataDir + "Multileaders.dwg";
Image image = Image.load(file);
CadImage cadImage = (CadImage) image;
```

## 2. 驗證 MLeader 實體

```java
Assert.areNotEqual(cadImage.getEntities().length, 0);
CadMLeader cadMLeader = (CadMLeader) cadImage.getEntities()[2];
```

### 3. 驗證 MLeader 樣式和屬性

```java
Assert.areEqual(cadMLeader.getStyleDescription(), "Standard");
Assert.areEqual(cadMLeader.getLeaderStyleId(), "12E");
Assert.areEqual(cadMLeader.getArrowHeadId1(), "639");
Assert.areEqual(cadMLeader.getLeaderLineTypeID(), "14");
```

## 4. 存取 MLeader 上下文數據

```java
CadMLeaderContextData context = cadMLeader.getContextData();
```

## 5. 驗證上下文屬性

```java
Assert.areEqual(context.getArrowHeadSize(), 30.0, 0.1);
Assert.areEqual(context.getBasePoint().getX(), 481, 1);
Assert.areEqual(context.getContentScale(), 1.0, 0.01);
Assert.areEqual(context.getDefaultText().getValue(), "This is multileader with huge text\\P{\\H1.5x;6666666666666666666666666666\\P}bbbbbbbbbbbbbbbbbbbbbbbbbbbbbbbbbbb");
Assert.areEqual(context.hasMText(), true);
```

## 6. 訪問MLeader節點和Leader Line

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

## 7. 驗證其他 MLeader 屬性

```java
Assert.areEqual(Integer.toString(mleaderNode.getBranchIndex()), Integer.toString(0));
Assert.areEqual(mleaderNode.getDogLegLength(), 8.0, 0.1);
Assert.areEqual(context.hasMText(), true);
```

## 8. 驗證文字屬性

```java
Assert.areEqual(context.getTextAttachmentType().getValue(), (short) 1);
Assert.areEqual(context.getTextBackgroundColor().getValue(), 18);
Assert.areEqual(context.getTextHeight(), 20.0, 0.1);
Assert.areEqual(context.getTextStyleID().getValue(), "11");
Assert.areEqual(context.getTextRotation().getValue(), 0.0, 0.01);
```

## 9. MLleader 的附加屬性

```java
Assert.areEqual(cadMLeader.getArrowHeadId1(), "639");
Assert.areEqual(cadMLeader.getLeaderType(), 1);
Assert.areEqual(cadMLeader.getBlockContentColor(), 0);
Assert.areEqual(cadMLeader.getLeaderLineColor(), 0);
Assert.areEqual(cadMLeader.getTextHeight(), 1.0, 0.01);
```

## 結論

恭喜！您已成功瀏覽了有關使用 Java 和 Aspose.CAD 支援 DWG 格式的 MLeader 實體的綜合指南。此功能為進階 CAD 操作打開了大門，並增強了您的 Java 開發工具包。

## 常見問題解答

### Q1：我可以將 Aspose.CAD for Java 與其他 CAD 格式一起使用嗎？

A1：是的，Aspose.CAD 支援 DWG 以外的各種 CAD 格式，為您的專案提供多功能性。

### Q2：在哪裡可以找到 Aspose.CAD for Java 的詳細文件？

 A2：請參閱[文件](https://reference.aspose.com/cad/java/)深入了解 Aspose.CAD 的功能。

### Q3：有免費試用嗎？

 A3：是的，直接探索功能[免費試用](https://releases.aspose.com/).

### 問題 4：如何取得 Aspose.CAD 的臨時許可？

A4：透過以下方式取得臨時許可證[這個連結](https://purchase.aspose.com/temporary-license/).

### Q5：我可以在哪裡尋求社區支持和協助？

A5：訪問[Aspose.CAD論壇](https://forum.aspose.com/c/cad/19)與社區聯繫並獲得協助。
{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}
