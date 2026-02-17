---
date: 2026-02-17
description: 學習如何在 Java 中使用 Aspose.CAD 將 DWG 另存為 JPEG，添加多個圖層，並調整 CAD 尺寸以實現精確的圖像轉換。
linktitle: Support of Layers in CAD
second_title: Aspose.CAD Java API
title: 在 Java 中將 DWG 另存為 JPEG（支援圖層）
url: /zh-hant/java/advanced-cad-features/support-of-layers-in-cad/
weight: 18
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# 在 Java 中將 DWG 另存為 JPEG（支援圖層）

## 介紹

在本教學中，您將了解如何 **將 DWG 另存為 JPEG**，同時充分利用 Aspose.CAD for Java 的圖層支援。圖層可讓您將圖紙的特定部分分離，輕鬆只匯出所需的內容。我們將逐步說明，從環境設定到匯出僅包含您選擇圖層的 JPEG。

## 快速解答
- **「將 DWG 另存為 JPEG」是什麼意思？** 它會將 DWG（或其他 CAD）圖紙轉換為點陣 JPEG 圖像。  
- **我可以只包含選取的圖層嗎？** 可以 – 使用 `setLayers` 方法指定要渲染的圖層。  
- **如何變更圖像尺寸？** 在 `CadRasterizationOptions` 中調整 `setPageWidth` 和 `setPageHeight`。  
- **這是僅限 Java 的解決方案嗎？** 範例使用 Aspose.CAD for Java，但相同概念適用於其他語言。  
- **我需要授權嗎？** 免費試用可用於測試；正式環境需購買商業授權。

## 「將 DWG 另存為 JPEG」是什麼？

將 DWG 另存為 JPEG 意指將向量式 CAD 檔案（DWG、DWF、DXF 等）光柵化為標準的 JPEG 位圖。當您需要在僅支援點陣圖的網頁、電子郵件或報告中嵌入 CAD 圖紙時，此功能相當有用。

## 為何使用支援圖層的 JPEG 轉換？

- **聚焦相關資料：** 只匯出所需的圖層，減少檔案大小與視覺雜訊。  
- **保留設計意圖：** 圖層保留物件的邏輯分組，讓您可使用相同來源檔案產生不同輸出。  
- **完整控制尺寸：** 透過調整光柵化選項，可產生符合出版需求的高解析度圖像。

## 前置條件

在開始之前，請確保您已具備以下項目：

1. **Aspose.CAD for Java Library** – 從[網站](https://releases.aspose.com/cad/java/)下載。依照安裝指南將 JAR 檔案加入專案的 classpath。  
2. **Java 開發環境** – 在您的機器上安裝近期的 JDK（8 版或更新）。

現在環境已備妥，讓我們來探討如何使用選擇性圖層渲染 **將 DWG 另存為 JPEG** 所需的程式碼。

## 匯入命名空間

首先匯入所需的 Aspose.CAD 類別與標準 Java 工具類別：

```java
import com.aspose.cad.Image;

import com.aspose.cad.imageoptions.CadRasterizationOptions;
import com.aspose.cad.imageoptions.JpegOptions;
import java.util.ArrayList;
import java.util.Arrays;
import java.util.List;
```

## 步驟說明

### 步驟 1：設定檔案路徑

定義來源 DWF 檔案所在位置以及輸出 JPEG 的寫入路徑。

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

建立 `CadRasterizationOptions` 實例並設定所需的輸出尺寸。變更這些數值即可 **調整 CAD 尺寸**，以產生最終的 JPEG。

```java
CadRasterizationOptions rasterizationOptions = new CadRasterizationOptions();
rasterizationOptions.setPageWidth(1600);
rasterizationOptions.setPageHeight(1600);
```

### 步驟 4：指定圖層（新增多個圖層）

若要渲染多個圖層，只需將它們的名稱加入清單。本例以單一圖層 “LayerA” 為起點。

```java
List<String> stringList = new ArrayList<>(Arrays.asList("LayerA"));
rasterizationOptions.setLayers(stringList);
```

*小技巧：* 若要 **新增多個圖層**，可擴充 `Arrays.asList` 呼叫，例如 `Arrays.asList("LayerA", "LayerB", "LayerC")`。這讓您在轉換時 **選取特定的 CAD 圖層**。

### 步驟 5：設定 JPEG 選項（Java 轉換 CAD 圖像）

將光柵化設定與 JPEG 輸出格式關聯起來。

```java
JpegOptions jpegOptions = new JpegOptions();
jpegOptions.setVectorRasterizationOptions(rasterizationOptions);
```

### 步驟 6：匯出為 JPG（將 DWG 另存為 JPEG）

最後，將圖像寫入磁碟。此步驟 **將 CAD 圖紙另存為 JPEG** 檔案，且僅包含選取的圖層。

```java
image.save(outFile, jpegOptions);
```

依照上述步驟，您已成功 **將 DWG 另存為 JPEG**，同時掌控顯示的圖層並自訂圖像尺寸。

## 如何在選擇圖層的情況下將 DWF 轉換為 JPEG

雖然範例使用 DWF 作為來源，但相同的光柵化流程適用於任何支援的 CAD 格式（DWG、DXF、DGN 等）。只要在 `srcFile` 中更改檔案副檔名，函式庫便會自動執行 **將 DWF 轉換為 JPEG**（或其他格式）的操作。

## 常見問題與解決方案

| 問題 | 解決方案 |
|-------|----------|
| **圖層未顯示** | 確認圖層名稱與 DWF 檔案中儲存的名稱完全相符（區分大小寫）。 |
| **輸出圖像為空白** | 確保 `setPageWidth` 與 `setPageHeight` 足夠大，以涵蓋圖紙的範圍。 |
| **授權例外** | 測試時使用試用授權；正式環境請取得完整授權。 |

## 常見問答

**Q: 我可以在光柵化選項中加入多個圖層嗎？**  
A: 當然可以。將 `stringList` 延伸加入其他圖層名稱，例如 `Arrays.asList("LayerA", "LayerB")`。

**Q: Aspose.CAD 是否相容其他 CAD 格式？**  
A: 是的，它支援 DWG、DXF、DWF 以及許多其他格式。

**Q: 我該如何變更輸出圖像的尺寸？**  
A: 在 `CadRasterizationOptions` 實例中修改 `setPageWidth` 與 `setPageHeight`。

**Q: 我可以從哪裡購買 Aspose.CAD 的授權？**  
A: 您可在[此處](https://purchase.aspose.com/buy)了解授權方案。

**Q: 我可以在哪裡取得社群支援？**  
A: 加入 Aspose.CAD 社群的[論壇](https://forum.aspose.com/c/cad/19)以獲得協助與討論。

---

**最後更新：** 2026-02-17  
**測試環境：** Aspose.CAD for Java 24.11  
**作者：** Aspose  

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}