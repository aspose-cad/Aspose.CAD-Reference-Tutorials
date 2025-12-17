---
date: 2025-12-10
description: 學習如何在 Java 中使用 Aspose.CAD 從 DXF 產生 PDF。此一步一步的指南向您展示如何輕鬆將 DXF 匯出為 PDF。
linktitle: Render DXF as PDF Using Java
second_title: Aspose.CAD Java API
title: 使用 Aspose.CAD for Java 從 DXF 產生 PDF
url: /zh-hant/java/additional-features/render-dxf-as-pdf/
weight: 19
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# 使用 Aspose.CAD for Java 從 DXF 建立 PDF

## 簡介

## 快速回答
- **使用的函式庫是什麼？** Aspose.CAD for Java  
- **主要目標？** 從 DXF 圖紙建立 PDF  
- **關鍵前置條件？** Java 開發環境 + Aspose.CAD JAR  
- **典型轉換時間？** 在現代硬件上每頁數毫秒  
- **可以自訂頁面大小嗎？** 可以 – 在匯出前調整光柵化選項  

## 先決條件

在開始之前，請確保您已具備：

- 基本的 Java 程式設計知識。  
- 已安裝 Aspose.CAD for Java 函式庫。如未安裝，可在此下載 [here](https://releases.aspose.com/cad/java/)。  
- 用於測試的 DXF 圖紙檔案。  

## 匯入命名空間

在 Java 程式碼中，首先匯入必要的命名空間以利用 Aspose.CAD 的功能。使用以下程式碼片段：

```java
import com.aspose.cad.Color;
import com.aspose.cad.Image;

import com.aspose.cad.imageoptions.CadRasterizationOptions;
import com.aspose.cad.imageoptions.PdfOptions;
```

## 如何使用 Aspose.CAD 從 DXF 建立 PDF

以下是一個逐步指南，帶您完成轉換過程。每一步都包含簡短說明以及需要貼入專案的完整程式碼。

### 步驟 1：設定資源目錄

定義 DXF 圖紙所在的資源目錄路徑。此設定對程式碼的正確運作至關重要。 

```java
String dataDir = "Your Document Directory" + "DXFDrawings/";
```

### 步驟 2：載入 DXF 檔案

使用以下程式碼片段將 DXF 檔案載入程式中：

```java
String srcFile = dataDir + "conic_pyramid.dxf";
Image image = Image.load(srcFile);
```

### 步驟 3：設定光柵化選項

建立 `CadRasterizationOptions` 的實例，並設定背景顏色、頁寬、頁高等多項屬性。這些選項決定向量圖在放入 PDF 前的光柵化方式。

```java
CadRasterizationOptions rasterizationOptions = new CadRasterizationOptions();
rasterizationOptions.setBackgroundColor(Color.getWhite());
rasterizationOptions.setPageWidth(1600);
rasterizationOptions.setPageHeight(1600);
```

### 步驟 4：建立 PDF 選項

建立 `PdfOptions`，並將先前設定好的 `rasterizationOptions` 指派給 `VectorRasterizationOptions` 屬性。此動作將光柵化設定與最終 PDF 輸出關聯起來。

```java
PdfOptions pdfOptions = new PdfOptions();
pdfOptions.setVectorRasterizationOptions(rasterizationOptions);
```

### 步驟 5：將 DXF 匯出為 PDF

最後，使用 `save` 方法將 DXF 檔案匯出為 PDF。這一步會 **export dxf to pdf**，並套用所有自訂設定。

```java
image.save(dataDir + "conic_pyramid_out_.pdf", pdfOptions);
```

此時，您已成功使用 Aspose.CAD for Java 將 DXF 檔案渲染為 PDF！

## 常見問題與解決方案

| 問題 | 原因 | 解決方法 |
|------|------|----------|
| **空白 PDF 輸出** | 未設定光柵化選項或背景顏色為透明 | 確保已套用 `setBackgroundColor(Color.getWhite())` |
| **頁面尺寸不正確** | 頁寬/頁高值過小或過大 | 調整 `setPageWidth` 和 `setPageHeight` 以符合所需的 PDF 大小 |
| **大型 DXF 發生 OutOfMemoryError** | 大型圖紙在光柵化時佔用過多記憶體 | 增加 JVM 堆積大小 (`-Xmx`) 或將檔案分成較小區段處理 |

## 常見問與答

**Q: Aspose.CAD for Java 是否相容所有 DXF 版本？**  
A: Aspose.CAD for Java 支援廣泛的 DXF 版本，確保與您可能遇到的大多數檔案相容。

**Q: 我可以進一步自訂 PDF 輸出嗎？**  
A: 可以，您可透過調整光柵化選項（色深、線寬等）來符合特定的視覺需求。

**Q: 是否提供試用版？**  
A: 有，您可透過下載免費試用版 [here](https://releases.aspose.com/) 來體驗 Aspose.CAD for Java 的功能。

**Q: 如何取得 Aspose.CAD for Java 的支援？**  
A: 請前往 [Aspose.CAD forum](https://forum.aspose.com/c/cad/19) 尋求協助並與社群互動。

**Q: 測試是否需要臨時授權？**  
A: 需要，您可在此取得臨時授權 [here](https://purchase.aspose.com/temporary-license/) 供測試使用。

## 結論

在本教學中，我們示範了如何使用 Aspose.CAD for Java **從 DXF 圖紙建立 PDF**。依照上述步驟，您即可將 DXF 轉 PDF 的功能整合至任何基於 Java 的解決方案，無論是桌面工具、Web 服務或自動批次處理程序。歡迎自行試驗光柵化設定，以在品質與檔案大小之間取得最佳平衡，符合您的特定需求。

---

**最後更新：** 2025-12-10  
**測試環境：** Aspose.CAD for Java 24.11  
**作者：** Aspose  

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}