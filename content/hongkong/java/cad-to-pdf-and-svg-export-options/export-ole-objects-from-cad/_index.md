---
title: 使用 Aspose.CAD for Java 從 CAD 匯出 OLE 對象
linktitle: 從 CAD 匯出 OLE 對象
second_title: Aspose.CAD Java API
description: 釋放 Aspose.CAD for Java 的潛力。輕鬆從 CAD 檔案匯出 OLE 物件。立即下載以實現無縫 CAD 資料管理。
type: docs
weight: 10
url: /zh-hant/java/cad-to-pdf-and-svg-export-options/export-ole-objects-from-cad/
---
## 介紹

在電腦輔助設計 (CAD) 的動態世界中，有效管理和提取 OLE（物件連結和嵌入）物件至關重要。 Aspose.CAD for Java 提供了從 CAD 檔案匯出 OLE 物件的強大解決方案。本逐步指南將引導您完成整個過程，確保您充分利用工具的潛力。

## 先決條件

在深入學習本教程之前，請確保您具備以下先決條件：

- Java 環境：確保您的電腦上設定了 Java 開發環境。
-  Aspose.CAD for Java：下載並安裝 Aspose.CAD for Java 函式庫。您可以在以下位置找到該圖書館：[下載連結](https://releases.aspose.com/cad/java/).
- CAD 檔案：準備包含要匯出的 OLE 物件的 CAD 檔案。

## 導入命名空間

首先，將必要的名稱空間匯入到您的 Java 專案中。這些命名空間提供了使用 Aspose.CAD 處理 CAD 檔案所需的基本類別和功能。

```java
import com.aspose.cad.Image;

import com.aspose.cad.fileformats.cad.CadImage;
import com.aspose.cad.imageoptions.CadRasterizationOptions;
import com.aspose.cad.imageoptions.PngOptions;
```

現在，讓我們將從 CAD 匯出 OLE 物件的過程分解為多個步驟：

## 第 1 步：設定您的文件目錄

```java
String dataDir = "Your Document Directory" + "DWGDrawings/";
```

確保將“您的文件目錄”替換為包含 CAD 檔案的目錄路徑。

## 步驟 2：定義 CAD 檔名

```java
String[] files = new String[] { "D ZD junior D10m H2m.dwg", "ZD - Senior D6m H2m45.dwg" };
```

指定要處理的 CAD 檔案的名稱`files`大批。

## 第 3 步：設定 PNG 匯出選項

```java
PngOptions pngOptions = new PngOptions();
CadRasterizationOptions rasterizationOptions = new CadRasterizationOptions();
pngOptions.setVectorRasterizationOptions(rasterizationOptions);
rasterizationOptions.setLayouts(new String[] { "Layout1" });
```

配置 PNG 匯出選項，包括向量光柵化和佈局設定。

## 第 4 步：迭代 CAD 文件

```java
for(String file : files)
{
    CadImage cadImage = (CadImage)Image.load(dataDir + file);
    cadImage.save(dataDir + file + "_out.png", pngOptions);
}
```

迭代每個指定的 CAD 文件，使用 Aspose.CAD 載入它，並將 OLE 物件儲存為 PNG 映像。

## 結論

透過這些簡單但功能強大的步驟，您可以使用 Aspose.CAD for Java 從 CAD 檔案無縫匯出 OLE 物件。這種多功能工具使開發人員能夠有效管理 CAD 數據，為 CAD 應用程式開發開闢了新的可能性。

## 常見問題解答

### Q1：Aspose.CAD 是否相容於所有 CAD 檔案格式？

 A1：Aspose.CAD支援多種CAD格式，包括DWG、DXF和DGN。請參閱[文件](https://reference.aspose.com/cad/java/)取得完整清單。

### Q2：我可以自訂 OLE 物件的匯出設定嗎？

A2：是的，Aspose.CAD 提供了廣泛的自訂匯出設定選項，可讓您根據您的特定要求自訂輸出。

### Q3：Aspose.CAD 有免費試用版嗎？

 A3：是的，您可以透過取得免費試用版來探索 Aspose.CAD 的功能[這裡](https://releases.aspose.com/).

### 問題 4：我可以在哪裡獲得 Aspose.CAD 的社群支持？

 A4：加入 Aspose.CAD 社群：[論壇](https://forum.aspose.com/c/cad/19)尋求協助並分享您的經驗。

### Q5: 如何購買 Aspose.CAD 的授權？

A5：訪問[購買頁面](https://purchase.aspose.com/buy)取得適合您的開發需求的授權。