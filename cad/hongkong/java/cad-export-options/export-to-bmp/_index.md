---
date: 2025-12-21
description: 學習如何使用 Aspose.CAD for Java，透過本一步步指南將 DWG 轉換為 BMP，並將 CAD 匯出為 BMP。
linktitle: Export to BMP
second_title: Aspose.CAD Java API
title: 如何使用 Aspose.CAD for Java 將 DWG 轉換為 BMP
url: /zh-hant/java/cad-export-options/export-to-bmp/
weight: 12
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# 使用 Aspose.CAD for Java 將 DWG 轉換為 BMP

## 簡介

在現代數位設計工作流程中，能夠快速且可靠地 **將 DWG 轉換為 BMP** 是相當重要的。無論您是要建立批次處理服務，或只需要單一檔案的轉換，Aspose.CAD for Java 都提供了功能完整的 API，讓您 **將 CAD 匯出為 BMP**，並可完整掌控光柵化設定。透過本教學，您將一步步了解從載入 DWG 檔案到儲存最終 BMP 圖像的全過程，讓您能自信地將此轉換整合至 Java 應用程式中。

## 快速回答
- **需要哪個函式庫？** Aspose.CAD for Java。
- **可以用單行程式碼完成 DWG 轉 BMP 嗎？** 不行，必須先載入檔案、設定光柵化選項，最後再儲存。
- **正式環境需要授權嗎？** 需要商業授權；亦提供免費試用版。
- **API 支援批次轉換嗎？** 當然可以——只要在迴圈中重複使用相同的選項即可。
- **支援哪個 Java 版本？** Java 8 及以上。

## 什麼是「將 DWG 轉換為 BMP」？

將 DWG（AutoCAD 繪圖）檔案轉為 BMP（點陣圖）會把向量資料光柵化為像素格式。此方式在需要通用圖像（如報告、縮圖或網頁預覽）且不想安裝 CAD 軟體時非常實用。

## 為什麼使用 Aspose.CAD for Java 將 CAD 匯出為 BMP？

- **無外部相依** – 純 Java，無需本機 DLL。
- **細緻的光柵化控制** – 可設定頁面大小、版面配置、抗鋸齒等。
- **高保真度** – 保留線寬、顏色與圖層資訊。
- **可擴充** – 適用於單一檔案或大規模批次作業。

## 先決條件

在開始撰寫程式碼之前，請確保您已具備：

- **Aspose.CAD for Java 函式庫** – 從 [here](https://releases.aspose.com/cad/java/) 下載。
- **Java 開發環境** – JDK 8 以上，搭配您慣用的 IDE。
- **基本的 Java 知識** – 了解類別、方法與檔案 I/O。

## 匯入命名空間

在您的 Java 專案中匯入必要的命名空間，以存取 Aspose.CAD 功能：

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

## 步驟 1：設定資源目錄路徑

定義包含 DWG（或其他 CAD）檔案的資料夾路徑。

```java
String dataDir = "Your Document Directory" + "ExportingCAD/";
```

## 步驟 2：載入 CAD 檔案

使用 `Image` 物件載入來源 DWG 檔案。

```java
String fileName = (dataDir + "site.dwf");
Image image = Image.load(fileName);
```

## 步驟 3：設定 BMP 匯出選項

建立 `BmpOptions`，並附加 `CadRasterizationOptions` 物件，以控制向量資料的光柵化方式。

```java
BmpOptions bmpOptions = new BmpOptions();
CadRasterizationOptions rasterizationOptions = new CadRasterizationOptions();
bmpOptions.setVectorRasterizationOptions(rasterizationOptions);
```

## 步驟 4：設定光柵化參數

調整頁面尺寸並指定要渲染的版面（layout）。這些設定會直接影響最終 BMP 的品質與檔案大小。

```java
rasterizationOptions.setPageHeight(500);
rasterizationOptions.setPageWidth(500);
rasterizationOptions.setLayouts(new String[] { "Model" });
```

## 步驟 5：匯出為 BMP

提供輸出路徑，呼叫 `save` 方法寫入 BMP 檔案。

```java
String outPath = dataDir + "site.bmp";
image.save(outPath, bmpOptions);
```

請對每一個欲 **將 DWG 轉換為 BMP** 的 CAD 檔案，重複上述步驟。

## 常見問題與技巧

- **版面名稱不正確** – 請確保版面字串與 DWG 檔案中定義的版面相符（例如 `"Model"` 或 `"Layout1"`）。
- **輸出解析度過低** – 提升 `PageWidth` 與 `PageHeight` 以取得更高 DPI 的結果。
- **記憶體使用量大** – 若處理極大型圖紙，建議一次只處理一個檔案，並在每次儲存後釋放 `Image` 物件。

## 常見問答

### Q1: Aspose.CAD for Java 是否適合批次處理？

A1: 絕對適合！Aspose.CAD for Java 支援批次處理，讓您能同時高效處理多個 CAD 檔案。

### Q2: 我可以為不同版面自訂光柵化選項嗎？

A2: 可以，您可以依需求自行調整頁面尺寸、版面等光柵化參數。

### Q3: 哪裡可以取得 Aspose.CAD for Java 的其他支援？

A3: 前往 [Aspose.CAD forum](https://forum.aspose.com/c/cad/19) 取得社群支援與討論。

### Q4: 有免費試用版嗎？

A4: 有，您可在 [here](https://releases.aspose.com/) 取得 Aspose.CAD for Java 的免費試用版。

### Q5: 如何取得臨時授權？

A5: 請至 [here](https://purchase.aspose.com/temporary-license/) 取得 Aspose.CAD for Java 的臨時授權。

## 常見問題

**Q: 可以將其他 CAD 格式（例如 DXF、DGN）轉為 BMP 嗎？**  
A: 可以，相同的 API 亦支援 DXF、DGN、DWF 以及其他已支援的格式。

**Q: 轉換過程會保留圖層可見性嗎？**  
A: 預設會光柵化所有可見圖層；若需隱藏圖層，可透過 `CadRasterizationOptions` 進行設定。

**Q: 能否為 BMP 設定背景顏色？**  
A: 能，於儲存前使用 `rasterizationOptions.setBackgroundColor(Color.getWhite());` 設定背景色。

**Q: 如何處理受密碼保護的 CAD 檔案？**  
A: 使用 `Image.load(fileName, loadOptions)` 載入檔案，`loadOptions` 中可包含密碼資訊。

**Q: 大量批次處理時，提升效能的最佳方式是？**  
A: 重複使用同一個 `BmpOptions` 實例，僅在每次迭代時變更輸入檔案路徑。

## 結論

依照本指南操作後，您已具備使用 Aspose.CAD for Java **將 DWG 轉換為 BMP** 以及 **將 CAD 匯出為 BMP** 的完整基礎。將這些步驟整合至您的應用程式，可自動產生圖像、建立縮圖，或為後續處理準備資產。

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}

---

**最後更新：** 2025-12-21  
**測試環境：** Aspose.CAD for Java 24.11  
**作者：** Aspose  

---