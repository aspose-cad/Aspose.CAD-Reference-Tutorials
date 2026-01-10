---
date: 2026-01-10
description: 學習如何使用 Aspose.CAD for Java 讀取 DWG 檔案並建立多重標註 DWG 實體，透過本分步教學。
linktitle: Support MLeader Entity for DWG Format with Java
second_title: Aspose.CAD Java API
title: 如何使用 Aspose.CAD for Java 讀取 DWG 並支援 MLeader
url: /zh-hant/java/cad-text-and-formatting/support-mleader-entity/
weight: 12
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# 如何使用 Aspose.CAD for Java 讀取 DWG 並支援 MLeader

## 簡介

如果您需要在 Java 應用程式中 **讀取 DWG** 檔案並處理 **multileader DWG** 實體，您來對地方了。Aspose.CAD for Java 為您提供一個簡潔的程式化方式來開啟 DWG 圖面、檢查 MLeader 物件，並驗證其屬性——全部不需完整的 CAD 工作站。在本教學中，我們將逐步說明從載入 DWG 檔案到確認 multileader 資料符合預期樣式的每個步驟。

## 快速解答

- **「如何讀取 dwg」涉及什麼？** 使用 `Image.load()` 載入 DWG，然後轉型為 `CadImage`。
- **我可以建立 multileader dwg 實體嗎？** 是的——您可以使用 CadMLeader API 新增、編輯和驗證 MLeader 物件。
- **需要哪個函式庫版本？** 任意近期的 Aspose.CAD for Java 版本（示範的 API 可在 2024 以上的版本中使用）。
- **開發時需要授權嗎？** 測試時可使用臨時授權，正式環境則需完整授權。
- **程式碼是否跨平台？** 絕對可以——Java 可在 Windows、Linux 與 macOS 上執行。

## 什麼是使用 Aspose.CAD 的「如何讀取 dwg」？

讀取 DWG 檔案即是將二進位圖面轉換為記憶體中的 `CadImage` 物件。取得該物件後，您可以列舉其實體（線條、圓形、文字、**MLeader** 物件等），並檢查其屬性。

## 為什麼要支援 MLeader 實體？

MLeader（multileader）物件將引線與附加的文字或圖塊結合，是工程圖註解的關鍵。支援它們可讓您：

- 驗證註解是否符合公司標準。
- 提取文字以供後續處理（例如物料清單產生）。
- 以程式方式修改引線樣式或取代圖塊內容。

## 先決條件

1. **Java 開發環境** – JDK 11 以上以及您喜愛的 IDE（IntelliJ、Eclipse、VS Code）。  
2. **Aspose.CAD for Java** – 從 [download link](https://releases.aspose.com/cad/java/) 下載最新的 JAR。

## 匯入命名空間

在您的 Java 類別中加入以下匯入，以便使用 DWG 實體與光柵化選項：

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

## 如何使用 Aspose.CAD for Java 讀取 DWG 檔案

### 步驟 1：載入 DWG 檔案並取得 `CadImage`

```java
String dataDir = "Your Document Directory" + "DWGDrawings/";
String file = dataDir + "Multileaders.dwg";
Image image = Image.load(file);
CadImage cadImage = (CadImage) image;
```

### 步驟 2：驗證圖面是否包含 MLeader 實體

```java
Assert.areNotEqual(cadImage.getEntities().length, 0);
CadMLeader cadMLeader = (CadMLeader) cadImage.getEntities()[2];
```

### 步驟 3：驗證 MLeader 樣式與基本屬性

```java
Assert.areEqual(cadMLeader.getStyleDescription(), "Standard");
Assert.areEqual(cadMLeader.getLeaderStyleId(), "12E");
Assert.areEqual(cadMLeader.getArrowHeadId1(), "639");
Assert.areEqual(cadMLeader.getLeaderLineTypeID(), "14");
```

### 步驟 4：存取 MLeader 上下文資料（multileader 的核心）

```java
CadMLeaderContextData context = cadMLeader.getContextData();
```

### 步驟 5：驗證上下文層級屬性

```java
Assert.areEqual(context.getArrowHeadSize(), 30.0, 0.1);
Assert.areEqual(context.getBasePoint().getX(), 481, 1);
Assert.areEqual(context.getContentScale(), 1.0, 0.01);
Assert.areEqual(context.getDefaultText().getValue(),
    "This is multileader with huge text\\P{\\H1.5x;6666666666666666666666666666\\P}bbbbbbbbbbbbbbbbbbbbbbbbbbbbbbbbbbb");
Assert.areEqual(context.hasMText(), true);
```

### 步驟 6：操作 MLeader 節點及其引線

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

### 步驟 7：驗證其他 MLeader 節點屬性

```java
Assert.areEqual(Integer.toString(mleaderNode.getBranchIndex()), Integer.toString(0));
Assert.areEqual(mleaderNode.getDogLegLength(), 8.0, 0.1);
Assert.areEqual(context.hasMText(), true);
```

### 步驟 8：檢查文字相關屬性

```java
Assert.areEqual(context.getTextAttachmentType().getValue(), (short) 1);
Assert.areEqual(context.getTextBackgroundColor().getValue(), 18);
Assert.areEqual(context.getTextHeight(), 20.0, 0.1);
Assert.areEqual(context.getTextStyleID().getValue(), "11");
Assert.areEqual(context.getTextRotation().getValue(), 0.0, 0.01);
```

### 步驟 9：檢查其他 MLeader 屬性以確保完整性

```java
Assert.areEqual(cadMLeader.getArrowHeadId1(), "639");
Assert.areEqual(cadMLeader.getLeaderType(), 1);
Assert.areEqual(cadMLeader.getBlockContentColor(), 0);
Assert.areEqual(cadMLeader.getLeaderLineColor(), 0);
Assert.areEqual(cadMLeader.getTextHeight(), 1.0, 0.01);
```

## 常見問題與解決方案

| 問題 | 發生原因 | 解決方法 |
|-------|----------------|-----|
| `ClassCastException` 在轉型實體時發生 | 所選索引並非 MLeader 物件。 | 在轉型前先確認 `cadImage.getEntities()[i] instanceof CadMLeader`。 |
| `null` 值的引線點 | 圖面使用了未完全支援的自訂引線樣式。 | 使用最新的 Aspose.CAD 版本，或在測試時回退至預設樣式。 |
| 數值斷言失敗 | 不同 CAD 版本之間的微小四捨五入差異。 | 如範例所示，調整 `Assert.areEqual(..., delta)` 中的容差。 |

## 常見問答

**Q: 我可以在 Aspose.CAD for Java 中使用其他 CAD 格式嗎？**  
A: 可以，Aspose.CAD 除了支援 DWG，亦支援 DXF、DWF、DGN 以及多種光柵格式。

**Q: 我可以在哪裡找到 Aspose.CAD for Java 的詳細文件？**  
A: 請參考官方的 [documentation](https://reference.aspose.com/cad/java/) 以取得 API 細節與程式碼範例。

**Q: 是否提供免費試用？**  
A: 當然可以——您可從 [free trial](https://releases.aspose.com/) 頁面下載試用版。

**Q: 如何取得測試用的臨時授權？**  
A: 可透過 [temporary license link](https://purchase.aspose.com/temporary-license/) 取得臨時授權。

**Q: 我可以在哪裡向社群尋求協助？**  
A: [Aspose.CAD forum](https://forum.aspose.com/c/cad/19) 是分享問題與解決方案的最佳場所。

## 結論

您現在已擁有完整的端對端教學，說明如何使用 Aspose.CAD for Java **讀取 DWG** 檔案以及 **建立 multileader DWG** 實體。依循上述步驟，您即可驗證 MLeader 樣式、提取註解資料，並將 DWG 處理整合至任何基於 Java 的工作流程中。

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}

---

**最後更新：** 2026-01-10  
**測試環境：** Aspose.CAD 24.11 for Java  
**作者：** Aspose