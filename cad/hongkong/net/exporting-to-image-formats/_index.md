---
date: 2026-07-18
description: Aspose CAD 轉換讓您輕鬆將 IFC 匯出為 PNG、將 IGES 匯出為 PDF。了解如何在數分鐘內使用 Aspose.CAD
  for .NET 逐步轉換 CAD 檔案。
keywords:
- aspose cad conversion
- export cad to png
- convert iges to pdf
lastmod: 2026-07-18
linktitle: 匯出至影像格式
og_description: Aspose CAD 轉換可快速將 IFC 匯出為 PNG、將 IGES 匯出為 PDF。遵循本指南，使用 Aspose.CAD for
  .NET 無縫處理 CAD 檔案。
og_image_alt: Guide showing Aspose CAD conversion from CAD files to PNG and PDF
og_title: Aspose CAD 轉換：匯出至影像格式
schemas:
- author: Aspose
  dateModified: '2026-07-18'
  description: Aspose CAD conversion lets you effortlessly export IFC to PNG and IGES
    to PDF. Learn step‑by‑step how to convert CAD files with Aspose.CAD for .NET in
    minutes.
  headline: 'Aspose CAD Conversion: Exporting to Image Formats'
  type: TechArticle
- questions:
  - answer: Yes, iterate over a folder with `foreach (var file in Directory.GetFiles(path,
      "*.ifc")) { var img = new Image(file); img.Save(Path.ChangeExtension(file, ".png"),
      ImageFormat.Png); }`. The `Directory.GetFiles` method returns the names of files
      (including their paths) that match a specified pattern in a directory.
    question: Can I convert multiple CAD files in one batch?
  - answer: Layer visibility is respected; you can toggle layers via `LoadOptions`
      before saving, ensuring only selected layers appear in the output.
    question: Does Aspose.CAD preserve layer information in the exported image?
  - answer: The library comfortably processes files up to **2 GB**; larger files should
      be split or streamed using `LoadOptions.MemoryLimit`.
    question: What is the maximum file size Aspose.CAD can handle?
  - answer: Yes—by saving as `ImageFormat.Pdf` the output retains vector data, allowing
      infinite scaling without quality loss.
    question: Is there support for converting CAD to vector‑based PDFs?
  - answer: A single Aspose.CAD license covers all supported .NET runtimes (Framework,
      Core, and .NET 5+).
    question: Do I need a separate license for each .NET platform?
  type: FAQPage
second_title: Aspose.CAD .NET - CAD and BIM File Format
tags:
- aspose cad
- cad conversion
- export cad to png
- iges to pdf
- ifc to png
title: Aspose CAD 轉換：匯出至影像格式
url: /zh-hant/net/exporting-to-image-formats/
weight: 39
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Aspose CAD 轉換：匯出至影像格式

在現代工程與設計工作流程中，**aspose cad conversion** 是將複雜的 CAD 與 BIM 檔案轉換為通用可檢視影像格式的關鍵。無論您需要分享 IFC 模型的快速預覽，或是從 IGES 圖紙產生可列印的 PDF，本教學將逐步說明如何使用 Aspose.CAD for .NET。您將看到如何在匯出至 PNG、PDF 及其他點陣格式時，保持幾何形狀、顏色與圖層的完整性。

## 快速解答
- **Aspose.CAD 可以匯出哪些格式？** 超過 30 種 CAD/BIM 格式，超過 20 種影像類型，包括 PNG、JPEG、PDF 與 TIFF。  
- **開發是否需要授權？** 免費試用可用於評估；正式上線需購買商業授權。  
- **支援哪些 .NET 版本？** .NET Framework 4.6+、.NET Core 3.1+、.NET 5/6/7。  
- **能處理大型檔案嗎？** 可以 — Aspose.CAD 可處理高達 2 GB 的檔案，且不需將整個文件載入記憶體。  
- **需要額外軟體嗎？** 不需要外部 CAD 工具；此函式庫在內部完成所有轉換。

## 什麼是 Aspose CAD 轉換？
`Image` 類別代表載入記憶體中的 CAD 文件，提供將其儲存為各種格式的方法。Aspose CAD 轉換使用 Aspose.CAD for .NET 將 CAD/BIM 檔案轉換為其他格式。先以 `Image` 載入來源，選擇目標格式，然後呼叫 `Save`。這種兩步驟模式可保留圖層、線寬與紋理，符合原始設計意圖。

## 如何將 IFC 檔案匯出為 PNG？
`Image` 類別代表載入記憶體中的 CAD 文件，提供將其儲存為各種格式的方法。使用 `new Image("model.ifc")` 載入 IFC 檔案，然後呼叫 `image.Save("model.png", ImageFormat.Png)`。Aspose.CAD 讀取 3‑D 幾何形狀，將其平面化為點陣圖，並輸出保留色彩深度與透明度的高解析度 PNG。若需批次處理，可遍歷資料夾並逐一儲存每個檔案。

## 如何將 IGES 檔案匯出為 PDF？
`Image` 類別代表載入記憶體中的 CAD 文件，提供將其儲存為各種格式的方法。從 IGES 檔案建立 `Image` 實例，然後呼叫 `image.Save("drawing.pdf", ImageFormat.Pdf)`。此轉換保留向量資訊、線條樣式與註解，產生可在任何檢視器開啟且不失細節的 PDF。可使用可選的 `Resolution` 屬性提升 DPI，以產生列印品質的 PDF。

## 為何使用 Aspose.CAD for .NET？
Aspose.CAD 支援 **30+ 輸入格式**（包括 IFC、IGES、DWG、DWF 與 STL），並可輸出 **20+ 影像類型**。在一般伺服器上可於 5 秒內處理數百頁的圖紙，且完全離線運作——不需安裝原生 CAD。這些可量化的優勢使其成為企業與自由開發者皆具成本效益且高效能的選擇。

## 常見陷阱與專業提示
`LoadOptions` 類別讓您自訂 CAD 檔案的載入方式，例如設定記憶體限制或指定圖層。  
`FontSettings` 物件定義在轉換過程中使用的字型替代與嵌入規則。

- **陷阱：** 忽略預設 DPI 會產生低解析度影像。  
  **專業提示：** 將 `image.DpiX` 與 `image.DpiY` 設為 300，以獲得列印品質的 PNG。  
- **陷阱：** 大型 IGES 檔案可能超出記憶體限制。  
  **專業提示：** 使用帶有 `MemoryLimit` 的 `LoadOptions` 以分塊串流檔案。  
- **陷阱：** IFC 模型缺少字型會導致佔位文字。  
  **專業提示：** 在轉換前使用 `FontSettings` 物件嵌入所需字型。

## 匯出至影像格式教學
### [匯出 IFC 檔案至 PNG - Aspose.CAD 教學](./exporting-ifc-files-to-png/)
探索 Aspose.CAD for .NET，這是一個強大的解決方案，可無縫將 IFC 轉換為 PNG。立即下載以提升 CAD 檔案處理效率。

### [匯出 IGES 檔案至 PDF - Aspose.CAD 指南](./exporting-iges-files-to-pdf/)
了解如何使用 Aspose.CAD for .NET 輕鬆將 IGES 檔案匯出為 PDF。遵循我們的逐步指南，精確操作 CAD 檔案。

## 常見問與答

**Q: 我可以一次批次轉換多個 CAD 檔案嗎？**  
A: 可以，使用 `foreach (var file in Directory.GetFiles(path, "*.ifc")) { var img = new Image(file); img.Save(Path.ChangeExtension(file, ".png"), ImageFormat.Png); }` 迭代資料夾。`Directory.GetFiles` 方法會回傳符合指定模式的檔案名稱（含路徑）。

**Q: Aspose.CAD 會在匯出的影像中保留圖層資訊嗎？**  
A: 會尊重圖層可見性；您可在儲存前透過 `LoadOptions` 切換圖層，確保僅顯示選取的圖層於輸出結果。

**Q: Aspose.CAD 能處理的最大檔案大小是多少？**  
A: 此函式庫可輕鬆處理高達 **2 GB** 的檔案；較大的檔案應使用 `LoadOptions.MemoryLimit` 進行分割或串流。

**Q: 是否支援將 CAD 轉換為向量式 PDF？**  
A: 有 — 透過以 `ImageFormat.Pdf` 儲存，輸出會保留向量資料，允許無限制縮放且不失真。

**Q: 每個 .NET 平台是否需要單獨的授權？**  
A: 單一 Aspose.CAD 授權即可涵蓋所有支援的 .NET 執行環境（Framework、Core 以及 .NET 5+）。

---

**最後更新：** 2026-07-18  
**測試版本：** Aspose.CAD 24.12 for .NET  
**作者：** Aspose

## 相關教學

- [匯出 IFC 檔案至 PNG - Aspose.CAD 教學](/cad/net/exporting-to-image-formats/exporting-ifc-files-to-png/)
- [匯出 IGES 檔案至 PDF - Aspose.CAD 指南](/cad/net/exporting-to-image-formats/exporting-iges-files-to-pdf/)
- [匯出 CAD 版面至點陣影像格式 (Aspose.CAD for .NET)](/cad/net/cad-export-formats/export-cad-layouts-to-raster-image-formats/)

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}