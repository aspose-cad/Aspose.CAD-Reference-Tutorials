---
title: 使用 Aspose.CAD for Java 將 STL 匯出為 PNG
linktitle: 將 STL 導出為 PNG
second_title: Aspose.CAD Java API
description: 探索使用 Aspose.CAD 在 Java 中將 STL 檔案匯出為 PNG 的無縫過程。簡化您的工作流程並輕鬆增強您的 Java 專案。
type: docs
weight: 20
url: /zh-hant/java/cad-export-options/export-stl-to-png/
---
## 介紹

您是否希望使用 Java 將 STL 檔案匯出為 PNG？ Aspose.CAD for Java 是您需要的解決方案！在本教程中，我們將逐步指導您完成流程。作為一名熟練的 SEO 作家，我將確保內容不僅內容豐富，而且針對搜尋引擎進行了優化。

## 先決條件

在深入學習本教程之前，請確保您具備以下先決條件：

- 您的電腦上安裝了 Java 開發工具包 (JDK)。
- 下載 Aspose.CAD for Java 函式庫。你可以得到它[這裡](https://releases.aspose.com/cad/java/).
- 有效許可證或臨時許可證[這裡](https://purchase.aspose.com/temporary-license/).

## 導入命名空間

在您的 Java 專案中，匯入必要的命名空間：

```java
import com.aspose.cad.Image;

import com.aspose.cad.fileformats.dgn.DgnImage;
import com.aspose.cad.imageoptions.CadRasterizationOptions;
import com.aspose.cad.fileformats.cad.CadImage;
import com.aspose.cad.imageoptions.CadRasterizationOptions;
import com.aspose.cad.imageoptions.PngOptions;
```

現在，讓我們將該範例分解為多個步驟。

## 第 1 步：設定您的項目

建立一個新的 Java 專案並將 Aspose.CAD for Java 庫新增至專案的依賴項。

## 第 2 步：指定您的 STL 文件

定義 STL 檔案的路徑。例如：

```java
String dataDir = "Your Document Directory" + "ExportingSTL/";
String fileName = dataDir + "example.stl";
```

## 第3步：載入STL文件

使用以下命令載入 STL 文件`Image.load`方法：

```java
CadImage cadImage = (CadImage)Image.load(fileName);
```

## 步驟 4：配置光柵化選項

設定向量化的光柵化選項：

```java
CadRasterizationOptions vectorOptions = new CadRasterizationOptions();
vectorOptions.setPageWidth(1500);
vectorOptions.setPageHeight(1500);
```

## 第 5 步：配置 PNG 選項

指定 PNG 匯出選項：

```java
PngOptions pngOptions = new PngOptions();
//如果要設定向量光柵化選項，請取消註解下面的行
//pngOptions.setVectorRasterizationOptions(vectorOptions);
```

## 步驟6：另存為PNG

將 CAD 映像儲存為 PNG 檔案：

```java
String outPath = dataDir + "galeon.stl.png";
cadImage.save(outPath, pngOptions);
```

恭喜！您已使用 Aspose.CAD for Java 成功將 STL 檔案匯出為 PNG。

## 結論

在本教程中，我們探索如何利用 Aspose.CAD for Java 輕鬆將 STL 檔案匯出為 PNG。這個強大的程式庫簡化了複雜的任務，使其成為您的 Java 專案的寶貴資產。

## 常見問題解答

### Q1：Aspose.CAD for Java 是否與所有 STL 檔案版本相容？

A1：Aspose.CAD for Java支援各種STL檔案版本，確保與大多數常見格式的兼容性。

### Q2：我可以在商業專案中使用Aspose.CAD for Java嗎？

 A2: 是的，可以。只需從以下機構取得有效許可證即可[這裡](https://purchase.aspose.com/buy).

### Q3：免費試用需要臨時許可證嗎？

 A3：不需要，免費試用不需要臨時許可證。您可以立即開始使用試用版[這裡](https://releases.aspose.com/).

### Q4：我可以在哪裡找到額外的支援或提出問題？

 A4：造訪 Aspose.CAD 論壇[這裡](https://forum.aspose.com/c/cad/19)如有任何支持或疑問。

### Q5：有完整的文檔嗎？

 A5：是的，可以找到文檔[這裡](https://reference.aspose.com/cad/java/).