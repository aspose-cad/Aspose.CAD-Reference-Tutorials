---
date: 2026-02-25
description: 學習如何將 DWG 轉換為 PNG、讀取 XREF 元資料，並使用 Aspose.CAD for Java 將 DWG 文件渲染為圖像——終極
  Java CAD 教學。
linktitle: CAD Meta Data and Rendering
second_title: Aspose.CAD Java API
title: 將 DWG 轉換為 PNG 及 CAD 元資料渲染
url: /zh-hant/java/cad-meta-data-and-rendering/
weight: 27
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# 將 DWG 轉換為 PNG 及 CAD 元資料渲染

## 介紹

如果您需要 **快速將 DWG 轉換為 PNG** 並同時擷取 XREF 元資料，您來對地方了。在本教學中，我們將說明如何從 DWG 檔案讀取 XREF 資訊，然後使用 Aspose.CAD for Java 將這些圖紙渲染為高品質的 PNG 圖片。無論您是要建置可視化 CAD 平面圖的 Web 服務，或是自動化批次轉換，以下步驟都能為您提供穩固、可投入生產環境的基礎。

## 快速回答
- **Aspose.CAD 能將 DWG 轉換為 PNG 嗎？** 可以 – 函式庫直接將 DWG 渲染為 PNG，無需中間步驟。  
- **需要哪個版本的 Java？** 支援 Java 8 以上。  
- **生產環境需要授權嗎？** 需要商業授權；亦提供免費試用版供評估。  
- **XREF 元資料可以取得嗎？** 當然可以 – Aspose.CAD 透過其 CADImage API 暴露 XREF 參照。  
- **可以控制影像解析度嗎？** 可以 – 在渲染時可指定寬度、高度或 DPI。

## 什麼是「將 DWG 轉換為 PNG」？
將 DWG 轉換為 PNG 意指將原生的 AutoCAD 圖紙（DWG）產生為可在瀏覽器、行動應用或文件中顯示的點陣圖（PNG），無需 CAD 軟體。PNG 支援透明度且提供無損品質，非常適合技術插圖。

## 為什麼使用 Aspose.CAD for Java 來轉換 DWG 為 PNG？
- **無外部相依性** – 純 Java，無需本機 DLL。  
- **完整的 DWG 支援** – 能處理複雜實體、圖層與 XREF。  
- **細緻的控制** – 可程式化設定輸出尺寸、DPI 與渲染選項。  
- **執行緒安全** – 適合高吞吐量服務。

## 前置條件
- Java Development Kit (JDK) 8 或更新版本。  
- Aspose.CAD for Java 函式庫（將 JAR 加入專案 classpath）。  
- 正式環境的有效 Aspose.CAD 授權（試用版為選擇性）。  
- 含有 XREF 參照的範例 DWG 檔案以供測試。

## 從 DWG 檔案讀取 XREF 元資料

### 為什麼 XREF 元資料很重要
外部參照（XREF）讓 DWG 檔案連結其他圖紙，實現模組化設計。擷取 XREF 元資料可協助您建立相依圖、驗證檔案完整性，或動態載入被參照的圖紙。

### 步驟說明
1. **載入 DWG 檔案** – 使用 `CadImage.load()` 開啟圖紙。  
2. **遍歷 XREF 集合** – `CadImage.Xrefs` 屬性會回傳每個參照的檔案路徑、插入點與比例。  
3. **收集資訊** – 將元資料存入清單或資料庫，以便後續處理。  
4. **關閉影像** – 使用 `close()` 釋放資源。

> *小技巧：* 處理大型組件時，可依圖層或區塊名稱過濾 XREF，以降低記憶體使用。

## 將 DWG 文件渲染為影像

### 從 DWG 到 PNG 的概觀
渲染是將向量實體轉換為像素的過程。Aspose.CAD 提供 `CadRasterizationOptions` 物件，您可在其中設定寬度、高度、DPI 與輸出格式（`ImageFormat.Png`）。函式庫會在一次呼叫中將整個圖紙（含 XREF）光柵化。

### 步驟說明
1. **建立光柵化選項** – 設定 `setImageFormat(ImageFormat.Png)` 並指定所需解析度。  
2. **實例化 `PngOptions` 物件** – 將其與光柵化選項關聯。  
3. **呼叫 `save()`** – 傳入輸出檔案路徑；Aspose.CAD 會寫入 PNG 檔。  
4. **驗證結果** – 用任何影像檢視器開啟 PNG，確認圖層與顏色均已保留。

> *常見陷阱：* 若未啟用 `setRenderXref(true)`，輸出影像將不會包含 XREF。需要完整視覺呈現時，務必設定此旗標。

## CAD 元資料與渲染教學
我們對您成功的承諾不僅止於上述教學。探索我們完整的 Aspose.CAD for Java 教學列表，涵蓋多元主題以滿足您的學習需求。從基礎概念到進階技巧，我們的教學將協助您在 CAD 開發旅程中發揮 Aspose.CAD for Java 的全部潛能。

### [使用 Aspose.CAD for Java 讀取 DWG 檔案的 XREF 元資料](./read-xref-meta-data/)
深入了解 Aspose.CAD for Java，輕鬆掌握從 DWG 檔案讀取 XREF 元資料的技巧，提升您的 CAD 開發效率。

### [使用 Aspose.CAD for Java 將 DWG 文件渲染為影像](./render-dwg-to-image/)
探索 Aspose.CAD for Java 在將 DWG 文件渲染為影像方面的無縫整合，依循步驟指南即可快速取得成效。

## 常見問題

**Q: 我可以一次批次轉換多個 DWG 為 PNG 嗎？**  
A: 可以 – 只要遍歷 DWG 檔案目錄，對每個檔案套用相同的光柵化選項即可。

**Q: 渲染時會保留線寬與顏色嗎？**  
A: 會的。Aspose.CAD 會遵循原始 CAD 的樣式設定，包括線型、線寬與真實顏色。

**Q: 如何處理受密碼保護的 DWG 檔案？**  
A: 在 `CadImage.load()` 時透過 `LoadOptions` 物件傳入密碼，函式庫會自動解密檔案。

**Q: 能只渲染特定版面或視口嗎？**  
A: 可以，在 `CadRasterizationOptions.setLayoutName()` 中指定版面名稱，即可只渲染單一版面。

**Q: 若需要透明背景該怎麼做？**  
A: 在保存為 PNG 前，呼叫 `CadRasterizationOptions.setBackgroundColor(Color.getTransparent())` 設定透明背景。

---

**最後更新：** 2026-02-25  
**測試環境：** Aspose.CAD for Java 24.12  
**作者：** Aspose  

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}