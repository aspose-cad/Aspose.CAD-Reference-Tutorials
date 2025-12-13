---
date: 2025-12-13
description: 學習如何在 Java 中使用 Aspose.CAD 將 CAD 儲存為 JPEG、添加多個圖層，並調整 CAD 尺寸以實現精確的影像轉換。
linktitle: Support of Layers in CAD
second_title: Aspose.CAD Java API
title: 在 Java 中將 CAD 另存為 JPEG 並支援圖層
url: /zh-hant/java/advanced-cad-features/support-of-layers-in-cad/
weight: 18
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# 在 Java 中將 CAD 儲存為 JPEG（支援圖層）

## 簡介

在本教學中，您將學會如何 **將 CAD 儲存為 JPEG**，同時充分利用 Aspose.CAD for Java 的圖層支援。圖層讓您可以將圖紙的特定部分分離，輕鬆匯出只需要的內容。我們將逐步說明，從環境設定到匯出僅包含所選圖層的 JPEG。

## 快速回答
- **「將 CAD 儲存為 JPEG」是什麼意思？** 它會將 CAD 圖紙轉換為點陣 JPEG 圖像。
- **我可以只包含選取的圖層嗎？** 可以 – 使用 `setLayers` 方法指定要渲染的圖層。
- **如何變更圖像尺寸？** 在 `CadRasterizationOptions` 中調整 `setPageWidth` 與 `setPageHeight`。
- **這是僅限 Java 的解決方案嗎？** 範例使用 Aspose.CAD for Java，但相同概念可套用於其他語言。
- **需要授權嗎？** 免費試用可用於測試，正式環境需購買商業授權。

## 先決條件

在開始之前，請確保您已具備以下項目：

1. **Aspose.CAD for Java Library** – 從 [website](https://releases.aspose.com/cad/java/) 下載。依照安裝說明將 JAR 檔加入專案的 classpath。  
2. **Java 開發環境** – 已安裝近期的 JDK（8 或更新版本）。

現在環境已備妥，讓我們探討如何 **將 CAD 儲存為 JPEG** 並選擇性渲染圖層的程式碼。

## 匯入命名空間

開始匯入所需的 Aspose.CAD 類別與標準 Java 工具：

```java
import com.aspose.cad.Image;

import com.aspose.cad.imageoptions.CadRasterizationOptions;
import com.aspose.cad.imageoptions.JpegOptions;
import java.util.ArrayList;
import java.util.Arrays;
import java.util.List;
```

## 逐步指南

### 步驟 1：設定檔案路徑

定義來源 DWF 檔案所在位置以及輸出 JPEG 要寫入的路徑。

```java
String dataDir = "Your Document Directory" + "DWFDrawings/";
String srcFile = dataDir + "for_layers_test.dwf";
String outFile = dataDir + "for_layers_test.jpg";
```

### 步驟 2：載入 DWF 圖像

使用 Aspose.CAD 的 `Image.load` 方法讀取 CAD 圖紙。

```java
Image image = Image.load(srcFile);
```

### 步驟 3：設定光柵化選項（調整 CAD 尺寸）

建立 `CadRasterizationOptions` 實例並設定期望的輸出大小。變更這些值即可 **調整 CAD 尺寸**，以符合最終 JPEG。

```java
CadRasterizationOptions rasterizationOptions = new CadRasterizationOptions();
rasterizationOptions.setPageWidth(1600);
rasterizationOptions.setPageHeight(1600);
```

### 步驟 4：指定圖層（新增多個圖層）

若要渲染多於一個圖層，只需將圖層名稱加入清單。此處以單一圖層 “LayerA” 為例。

```java
List<String> stringList = new ArrayList<>(Arrays.asList("LayerA"));
rasterizationOptions.setLayers(stringList);
```

*小技巧：* 若要 **新增多個圖層**，擴充 `Arrays.asList` 呼叫，例如 `Arrays.asList("LayerA", "LayerB", "LayerC")`。

### 步驟 5：設定 JPEG 選項（Java 轉換 CAD 圖像）

將光柵化設定與 JPEG 輸出格式關聯。

```java
JpegOptions jpegOptions = new JpegOptions();
jpegOptions.setVectorRasterizationOptions(rasterizationOptions);
```

### 步驟 6：匯出為 JPG（將 CAD 儲存為 JPEG）

最後，將圖像寫入磁碟。此步驟 **將 CAD 圖紙儲存為 JPEG**，且僅包含選取的圖層。

```java
image.save(outFile, jpegOptions);
```

依照上述步驟，您已成功 **將 CAD 儲存為 JPEG**，同時掌控圖層顯示與圖像尺寸的自訂。

## 常見問題與解決方案

| 問題 | 解決方案 |
|-------|----------|
| **圖層未顯示** | 確認圖層名稱與 DWF 檔案中儲存的名稱完全相符（區分大小寫）。 |
| **輸出圖像為空白** | 確保 `setPageWidth` 與 `setPageHeight` 足夠容納圖紙的範圍。 |
| **授權例外** | 測試時使用試用授權；正式環境請取得完整授權。 |

## 常見問答

**問：我可以在光柵化選項中加入多個圖層嗎？**  
答：當然可以。將 `stringList` 延伸為更多圖層名稱，例如 `Arrays.asList("LayerA", "LayerB")`。

**問：Aspose.CAD 是否相容其他 CAD 格式？**  
答：是的，支援 DWG、DXF、DWF 等多種格式。

**問：如何變更輸出圖像尺寸？**  
答：在 `CadRasterizationOptions` 實例中修改 `setPageWidth` 與 `setPageHeight`。

**問：在哪裡可以購買 Aspose.CAD 的授權？**  
答：您可以在 [here](https://purchase.aspose.com/buy) 查看授權方案。

**問：哪裡可以取得社群支援？**  
答：加入 Aspose.CAD 社群的 [forum](https://forum.aspose.com/c/cad/19) 取得協助與討論。

---

**最後更新：** 2025-12-13  
**測試環境：** Aspose.CAD for Java 24.11  
**作者：** Aspose  

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}