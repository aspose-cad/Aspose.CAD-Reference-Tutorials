---
date: 2026-10-19
description: 了解如何僅用幾行程式碼，即可使用 Aspose.CAD for Java 建立 PNG 縮圖 IFC 檔案。
keywords:
- create png thumbnail ifc
- ifc to png conversion
- aspose cad java
- java image processing
- bIM visualization
lastmod: 2026-10-19
linktitle: 匯出 IFC 為 PNG
og_description: 使用 Aspose.CAD for Java 輕鬆建立 PNG 縮圖 IFC 檔案。本分步指南將示範如何載入、rasterize 並將
  IFC 模型儲存為高品質 PNG 圖像。
og_image_alt: Developer guide showing Java code that converts IFC files to PNG thumbnails
  using Aspose.CAD
og_title: 使用 Aspose.CAD for Java 建立 PNG 縮圖 IFC
schemas:
- author: Aspose
  dateModified: '2026-10-19'
  description: Learn how to create PNG thumbnail IFC files with Aspose.CAD for Java
    in just a few lines of code.
  headline: How to create PNG thumbnail IFC with Aspose.CAD for Java
  type: TechArticle
- description: Learn how to create PNG thumbnail IFC files with Aspose.CAD for Java
    in just a few lines of code.
  name: How to create PNG thumbnail IFC with Aspose.CAD for Java
  steps:
  - name: load the IFC file
    text: First, point to the folder where your IFC file lives and load it with `CadImage.load`.
      `CadImage.load` reads a CAD file and returns an image object that can be rasterized.
      > **Why this matters:** Loading the file as a `CadImage` gives you access to
      vector‑raster conversion options that control resol
  - name: set rasterization options
    text: Define the output dimensions and any other vector‑related settings through
      `VectorRasterizationOptions`. `VectorRasterizationOptions` lets you specify
      output size, background color, and other rasterization parameters. > Adjust
      `PageWidth` and `PageHeight` to control the final PNG resolution, which i
  - name: configure PNG options
    text: Link the rasterization options to the PNG exporter by creating a `PngOptions`
      instance.
  - name: save the image as PNG
    text: Finally, write the rasterized image to disk using the `save` method. `save`
      writes the rasterized image to the specified file path in the chosen format.
      > After this step you have successfully **created a PNG thumbnail IFC** and
      can use the resulting `example.png` anywhere you need a raster image.
  type: HowTo
- questions:
  - answer: Yes, Aspose.CAD supports many formats (DWG, DXF, DGN, etc.). Simply change
      the file extension and load the appropriate image class.
    question: Can I use this approach to convert other CAD formats to PNG?
  - answer: DPI is controlled indirectly via `PageWidth`/`PageHeight`. Adjust these
      values relative to the desired physical size to achieve the required DPI.
    question: Does the library let me set a custom DPI?
  - answer: PNG is a lossless format, so the rasterized image retains the full visual
      fidelity of the original vector data.
    question: Is the PNG output loss‑less?
  type: FAQPage
second_title: Aspose.CAD Java API
tags:
- ifc conversion
- png thumbnail
- aspose.cad
- java image processing
- bim visualization
title: 如何使用 Aspose.CAD for Java 建立 PNG 縮圖 IFC
url: /zh-hant/java/cad-export-options/export-ifc-to-png/
weight: 18
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# 使用 Aspose.CAD for Java 將 IFC 匯出為 PNG

## 簡介

在本教學中，您將學習如何使用 Aspose.CAD for Java **create PNG thumbnail IFC** 檔案。無論您需要為 BIM 入口網站快速預覽、為文件管理系統產生縮圖，或是自動批次轉換，以下步驟都能讓您在幾行 Java 程式碼中將 3‑D IFC 模型光柵化為清晰的 2‑D PNG 圖像。

## 快速問答
- **需要哪個程式庫？** Aspose.CAD for Java。  
- **我可以用幾行程式碼建立 PNG 縮圖 IFC 嗎？** 是 – 整個工作流程可在 20 行以內完成。  
- **生產環境需要授權嗎？** 臨時授權可用於測試；商業部署則需要正式授權。  
- **輸出是否可伸縮？** 您可以設定任意像素尺寸，PNG 會依需求縮放至任何大小。  
- **支援哪個 Java 版本？** Java 8 或更高。

## 什麼是「將 IFC 轉換為 PNG」？

將 IFC（Industry Foundation Classes）轉換為 PNG 代表將 3‑D 建築模型光柵化為 2‑D 位圖圖像。此過程會產生可在瀏覽器、報告或行動應用程式中顯示的視覺縮圖，無需完整的 CAD 檢視器。

## 為什麼要使用 Aspose.CAD for Java？

Aspose.CAD 支援 **30+ CAD and BIM formats**，包括 IFC、DWG、DXF 和 DGN，且可處理高達 **2 GB** 的檔案而無需將整個文件載入記憶體。此程式庫為純 Java，具有 **zero external dependencies**，可在 Windows、Linux 與 macOS 上執行，十分適合伺服器端影像產生。  
它提供高效能的光柵化、廣泛的格式支援，且易於整合至 Java 應用程式中。

## 先決條件

- **Aspose.CAD Library** – 從 [download link](https://releases.aspose.com/cad/java/) 下載最新的 JAR。  
- **Java Development Kit** – 在您的機器上安裝 JDK 8 或更新版本。  
- **IFC source file** – 將檔案放置於可在程式碼中引用的資料夾中。

## 匯入命名空間

`com.aspose.cad` 套件提供您所需的所有類別。`CadImage` 是載入 CAD 檔案的入口點，而 `PngOptions` 用於設定光柵化參數。

```java
import com.aspose.cad.Image;

import com.aspose.cad.fileformats.ifc.IfcImage;
import com.aspose.cad.imageoptions.CadRasterizationOptions;
import com.aspose.cad.imageoptions.PngOptions;
```

## 如何在 Java 中建立 PNG 縮圖 IFC？

載入 IFC 檔案、定義光柵化選項，並將結果儲存為 PNG 圖像——這就是完整的轉換工作流程。以下各節將逐步說明每個步驟，讓您可以直接複製貼上程式碼片段到專案中並立即執行。

### 步驟 1：載入 IFC 檔案
首先，指向 IFC 檔案所在的資料夾，並使用 `CadImage.load` 載入。  
`CadImage.load` 讀取 CAD 檔案並回傳可供光柵化的影像物件。

```java
String dataDir = "Your Document Directory" + "ExportingIFC/";
String fileName = dataDir + "example.ifc";
IfcImage cadImage = (IfcImage)Image.load(fileName);
```

> **為什麼這很重要：** 將檔案載入為 `CadImage` 可讓您存取向量‑光柵轉換選項，控制解析度、背景顏色與線條粗細。

### 步驟 2：設定光柵化選項
透過 `VectorRasterizationOptions` 定義輸出尺寸及其他向量相關設定。  
`VectorRasterizationOptions` 允許您指定輸出大小、背景顏色以及其他光柵化參數。

```java
CadRasterizationOptions vectorOptions = new CadRasterizationOptions();
vectorOptions.setPageWidth(1500);
vectorOptions.setPageHeight(1500);
```

> 調整 `PageWidth` 和 `PageHeight` 以控制最終 PNG 解析度，這在您 **save PNG java** 檔案以供高品質列印或網頁縮圖時尤為重要。

### 步驟 3：設定 PNG 選項
透過建立 `PngOptions` 實例，將光柵化選項連結至 PNG 匯出器。

```java
PngOptions pngOptions = new PngOptions();
pngOptions.setVectorRasterizationOptions(vectorOptions);
```

### 步驟 4：將影像儲存為 PNG
最後，使用 `save` 方法將光柵化影像寫入磁碟。  
`save` 會將光柵化影像寫入指定路徑的選定格式檔案。

```java
String outPath = dataDir + "example.png";
cadImage.save(outPath, pngOptions);
```

> 完成此步驟後，您已成功 **created a PNG thumbnail IFC**，並可在任何需要光柵圖像的地方使用產生的 `example.png`。

## 常見使用情境

- **產生縮圖** 用於網路入口網站的 BIM 模型。  
- **嵌入平面圖快照** 至 PDF 或 Word 報告中。  
- **自動批次轉換** 大型 IFC 資料庫，用於存檔或遷移專案。

## 疑難排解與技巧

- **記憶體問題：** 對於非常大的 IFC 檔案，請增加 JVM 堆積大小（`-Xmx2g` 或更高）。  
- **缺少紋理：** 確保 IFC 檔案的外部資源可從 `dataDir` 取得。  
- **專業提示：** 若您偏好白色背景而非預設的透明 PNG，請使用 `vectorOptions.setBackgroundColor(Color.getWhite())`。

## 常見問答

### Q1：Aspose.CAD 是否相容所有版本的 IFC 檔案？

A1：Aspose.CAD 支援多種 IFC 版本。請參閱 [文件說明](https://reference.aspose.com/cad/java/) 以取得詳細相容性資訊。

### Q2：我可以進一步自訂光柵化選項嗎？

A2：當然可以！請參閱 [文件說明](https://reference.aspose.com/cad/java/) 以了解進階設定，如 DPI 控制、抗鋸齒與線條粗細。

### Q3：是否提供試用版？

A3：是的，您可從 [Aspose.CAD 免費試用](https://releases.aspose.com/) 下載免費試用版。

### Q4：如何取得測試用的臨時授權？

A4：請從 [Aspose.CAD 臨時授權頁面](https://purchase.aspose.com/temporary-license/) 取得臨時授權。

### Q5：我可以在哪裡提問或回報問題？

A5：請加入 [Aspose.CAD 論壇](https://forum.aspose.com/c/cad/19) 社群，以獲得 Aspose 工程師與其他開發者的支援。

## 常見問題

**Q: 我可以使用此方法將其他 CAD 格式轉換為 PNG 嗎？**  
A: 是的，Aspose.CAD 支援多種格式（DWG、DXF、DGN 等）。只需更改檔案副檔名並載入相應的影像類別。

**Q: 程式庫是否允許我設定自訂 DPI？**  
A: DPI 透過 `PageWidth`/`PageHeight` 間接控制。調整這些值相對於目標實體尺寸，即可達到所需的 DPI。

**Q: PNG 輸出是否無損？**  
A: PNG 為無損格式，光柵化影像會保留原始向量資料的完整視覺忠實度。

## 結論

您現在擁有一套完整、可投入生產的方式，使用 Aspose.CAD for Java **create PNG thumbnail IFC** 檔案。將這些步驟整合至桌面工具、伺服器端服務或雲端函式，以自動化 BIM 可視化流程，為最終使用者提供快速且高品質的縮圖。

---

**最後更新：** 2026-10-19  
**測試環境：** Aspose.CAD for Java 24.11  
**作者：** Aspose

## 相關教學

- [如何使用 Aspose.CAD for Java 將 STL 轉換為 PNG](/cad/java/cad-export-options/export-stl-to-png/)
- [將 DWG 轉換為 PNG – 使用 Aspose.CAD for Java 將 CAD 儲存為 PNG](/cad/java/cad-drawing-conversion/convert-cad-drawing-to-raster-image/)
- [在 Java 中將 DWG 匯出為 PDF – 使用 Aspose.CAD 設定 PDF 頁面大小](/cad/java/cad-export-options/export-to-pdf/)


{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}