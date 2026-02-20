---
date: 2026-02-20
description: 了解如何使用 Aspose.CAD for Java 高效地將 DWG 轉換為 BMP，並將 CAD 匯出為 BMP。請參考我們的逐步指南，獲得精確的轉換。
linktitle: Export to BMP
second_title: Aspose.CAD Java API
title: 使用 Aspose.CAD for Java 將 DWG 轉換為 BMP
url: /zh-hant/java/cad-export-options/export-to-bmp/
weight: 12
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# 使用 Aspose.CAD for Java 將 DWG 轉換為 BMP

## 介紹

在現代工程工作流程中，能夠 **快速且可靠地將 DWG 轉換為 BMP** 對於產生縮圖、文件或將 CAD 視覺效果整合到 Web 應用程式中至關重要。Aspose.CAD for Java 提供簡單的 API，讓您 **將 CAD 匯出為 BMP**，同時完整掌控光柵化設定。本教學將一步步說明從環境設定到儲存最終 BMP 圖片的全過程，讓您能自信地在 Java 專案中加入此功能。

## 快速解答
- **需要哪個函式庫？** Aspose.CAD for Java（提供免費試用）。  
- **支援哪些檔案格式進行轉換？** DWG、DWF、DXF 以及其他多種 CAD 格式皆可轉換為 BMP。  
- **開發時需要授權嗎？** 測試階段使用臨時或評估授權即可；正式上線需購買正式授權。  
- **轉換需要多長時間？** 在現代硬體上，標準尺寸圖紙通常在一秒內完成。  
- **可以批次處理多個檔案嗎？** 可以——只要將轉換程式碼放入迴圈即可。

## 什麼是將 DWG 轉換為 BMP？
將 DWG 轉換為 BMP 會把向量式 CAD 圖面轉換成點陣圖位圖。當您需要在瀏覽器顯示、嵌入文件，或使用不支援原生 CAD 檔案的影像編輯工具時，這種格式非常實用。

## 為什麼要使用 Aspose.CAD 匯出 CAD 為 BMP？
- **無外部相依** – 純 Java，無需本機 DLL。  
- **高保真** – 保留線寬、顏色與圖層。  
- **可自訂光柵化** – 可控制頁面尺寸、解析度與渲染品質。  
- **支援批次** – 易於整合至自動化流水線。

## 前置條件

在開始教學之前，請確保已具備以下條件：

- Aspose.CAD for Java 函式庫：從 [此處](https://releases.aspose.com/cad/java/) 下載並安裝 Aspose.CAD for Java 函式庫。  
- Java 開發環境：確保系統已設定好 Java 開發環境。  
- 基礎 Java 知識：熟悉基本的 Java 程式概念。

## 匯入命名空間

在您的 Java 專案中，匯入必要的命名空間以存取 Aspose.CAD 功能：

```java
import com.aspose.cad.Image;
import com.aspose.cad.InterpolationMode;
import com.aspose.cad.SmoothingMode;
import com.aspose.cad.TextRenderingHint;

import com.aspose.cad.imageoptions.BmpOptions;
import com.aspose.cad.imageoptions.CadRasterizationOptions;
import com.aspose.cad.imageoptions.PdfOptions;
//import com.aspose.cad.imageoptions.TypeOfEntities;
```

## 如何使用 Aspose.CAD for Java 將 DWG 轉換為 BMP

以下是與原始工作流程相同的逐步指南，並加入說明與最佳實踐提示。

### 步驟 1：設定資源目錄路徑

先定義 CAD 檔案所在的資源目錄路徑。

```java
String dataDir = "Your Document Directory" + "ExportingCAD/";
```

> **專業提示：** 使用 `System.getProperty("user.dir")` 來建立跨環境皆可使用的絕對路徑。

### 步驟 2：載入 CAD 檔案

將 CAD 檔案載入 Aspose.CAD 的 `Image` 物件。

```java
String fileName = (dataDir + "site.dwf");
Image image = Image.load(fileName);
```

> **為什麼這很重要：** 只載入一次檔案，即可在需要時重複使用同一個 `Image` 實例匯出不同格式。

### 步驟 3：設定 BMP 匯出選項

建立並設定 BMP 匯出選項，包括光柵化設定。

```java
BmpOptions bmpOptions = new BmpOptions();
CadRasterizationOptions rasterizationOptions = new CadRasterizationOptions();
bmpOptions.setVectorRasterizationOptions(rasterizationOptions);
```

> **提示：** 您也可以使用 `bmpOptions.setBitsPerPixel(24);` 來控制顏色深度。

### 步驟 4：設定光柵化參數

定義頁面高度、頁面寬度與版面配置等光柵化參數。

```java
rasterizationOptions.setPageHeight(500);
rasterizationOptions.setPageWidth(500);
rasterizationOptions.setLayouts(new String[] { "Model" });
```

> **常見陷阱：** 忘記指定版面配置可能導致多版面圖紙產生空白影像。

### 步驟 5：匯出為 BMP

指定輸出路徑並儲存 BMP 檔案。

```java
String outPath = dataDir + "site.bmp";
image.save(outPath, bmpOptions);
```

> **結果：** `site.bmp` 會出現在 `ExportingCAD` 資料夾中，可直接用於報告、網頁或進一步的影像處理。

對每個想要匯出為 BMP 的 CAD 檔案，重複上述步驟即可。

## 常見問題與解決方案

| 問題 | 原因 | 解決方案 |
|------|------|----------|
| BMP 輸出為空白 | 版面名稱錯誤或未指定版面 | 確認版面名稱與來源 CAD 檔案相符（例如 `"Model"`）。 |
| 影像解析度低 | 預設光柵化 DPI 較低 | 使用 `rasterizationOptions.setResolution(300);` 提升品質。 |
| 大檔案發生 OutOfMemoryError | JVM 堆積空間不足 | 增加 JVM 堆積 (`-Xmx2g`) 或將檔案分批處理。 |

## 結論

使用 Aspose.CAD for Java 匯出 CAD 為 BMP 非常簡單。依循本步驟指南，您即可在 Java 應用程式中無縫整合 **DWG 轉 BMP** 功能，為任何工程工作流程提供高效且精確的轉換。

## 常見問答

### Q1：Aspose.CAD for Java 是否適合批次處理？

A1：絕對適合！Aspose.CAD for Java 支援批次處理，讓您能同時高效處理多個 CAD 檔案。

### Q2：我可以為不同版面自訂光柵化選項嗎？

A2：可以，您可以依需求自訂頁面尺寸、版面配置等光柵化參數。

### Q3：在哪裡可以取得 Aspose.CAD for Java 的其他支援？

A3：請前往 [Aspose.CAD 論壇](https://forum.aspose.com/c/cad/19) 取得社群支援與討論。

### Q4：是否提供免費試用？

A4：有，您可在 [此處](https://releases.aspose.com/) 取得 Aspose.CAD for Java 的免費試用版。

### Q5：如何取得臨時授權？

A5：請至 [此處](https://purchase.aspose.com/temporary-license/) 取得 Aspose.CAD for Java 的臨時授權。

## 常見問題

**Q：可以使用相同程式碼將其他 CAD 格式（例如 DXF）轉換為 BMP 嗎？**  
A：可以。只要在 `fileName` 中更改副檔名，Aspose.CAD 會自動完成轉換。

**Q：BMP 能設定透明背景嗎？**  
A：BMP 本身不支援透明度；若需要 alpha 通道，建議匯出為 PNG。

**Q：如何將產生的 BMP 嵌入 PDF 報告？**  
A：使用標準影像函式庫（例如 iText）載入 BMP，然後將其作為圖像物件加入 PDF。

**Q：此函式庫支援高解析度列印嗎？**  
A：支援。將 `rasterizationOptions.setResolution()` 設為 600 DPI 或更高，即可取得列印品質的輸出。

**Q：商業使用有哪些授權方案？**  
A：Aspose 提供永久授權、訂閱授權與臨時授權。請聯絡業務取得客製化報價。

---

**最後更新：** 2026-02-20  
**測試環境：** Aspose.CAD for Java 24.11（撰寫時的最新版本）  
**作者：** Aspose  

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}