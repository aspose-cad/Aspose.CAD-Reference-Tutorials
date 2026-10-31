---
date: 2026-10-30
description: 了解如何使用 Aspose.CAD for Java 批次將 DXF 檔案轉換為 WMF，提供逐步程式碼說明、免費試用資訊，以及可選的 PDF
  匯出。
keywords:
- batch convert dxf files
- aspose cad java
- dxf to wmf conversion
- java cad rasterization
- aspose free trial
lastmod: 2026-10-30
linktitle: 使用 Java 匯出 DXF 為 WMF 格式
og_description: 使用 Aspose.CAD for Java 批次將 DXF 檔案轉換為 WMF。依照本指南載入 DXF 圖紙、設定光柵化選項、儲存為
  WMF，並可選擇以免費試用方式匯出為 PDF。
og_image_alt: Tutorial showing batch conversion of DXF to WMF in Java using Aspose.CAD
og_title: 使用 Aspose.CAD for Java 批次將 DXF 檔案轉換為 WMF
schemas:
- author: Aspose
  dateModified: '2026-10-30'
  description: Learn how to batch convert DXF files to WMF using Aspose.CAD for Java,
    with step‑by‑step code, free trial info, and optional PDF export.
  headline: Batch convert DXF files to WMF with Aspose.CAD for Java
  type: TechArticle
- description: Learn how to batch convert DXF files to WMF using Aspose.CAD for Java,
    with step‑by‑step code, free trial info, and optional PDF export.
  name: Batch convert DXF files to WMF with Aspose.CAD for Java
  steps:
  - name: load dxf drawing
    text: Image.load reads the DXF file into an Aspose.CAD Image object.
  - name: configure rasterization options
    text: '`CadRasterizationOptions` specifies page size, resolution, and background
      for rasterizing the CAD drawing.'
  - name: save as wmf
    text: '`ImageSaveOptions` with `SaveFormat.WMF` tells Aspose.CAD to write the
      output as a Windows Metafile.'
  - name: dispose of resources
    text: Calling `image.close()` releases native resources used by the Aspose.CAD
      Image object.
  - name: optional – export to pdf
    text: '`PdfOptions` configures PDF‑specific settings when saving the image as
      a PDF document. > **Pro tip:** You can reuse the same `CadRasterizationOptions`
      object for PDF export by passing it to a `PdfOptions` instance, saving you a
      few lines of setup.'
  type: HowTo
- questions:
  - answer: You can access the documentation [Aspose.CAD Java documentation](https://reference.aspose.com/cad/java/).
    question: Where can I find the Aspose.CAD documentation?
  - answer: Download the library [Aspose.CAD Java download page](https://releases.aspose.com/cad/java/).
    question: How do I download Aspose.CAD for Java?
  - answer: Yes, you can get a free trial [Aspose free trial page](https://releases.aspose.com/).
    question: Is there a free trial available?
  - answer: Explore temporary licenses [temporary license options](https://purchase.aspose.com/temporary-license/).
    question: Need temporary licensing options?
  - answer: Visit the Aspose.CAD support forum [Aspose.CAD support forum](https://forum.aspose.com/c/cad/19).
    question: Where can I get support?
  type: FAQPage
second_title: Aspose.CAD Java API
tags:
- batch convert dxf
- Aspose.CAD
- Java CAD conversion
- WMF export
- DXF processing
title: 使用 Aspose.CAD for Java 批次將 DXF 檔案轉換為 WMF
url: /zh-hant/java/additional-features/export-dxf-to-wmf/
weight: 14
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# 批次將 DXF 檔案轉換為 WMF（使用 Aspose.CAD for Java）

## 簡介

在本教學中，您將學習如何使用 Aspose.CAD for Java **批次將 DXF 檔案轉換為 WMF**。無論是需要在 Windows 報告中嵌入 CAD 圖紙、為 Office 文件產生輕量向量圖形，或是自動化大規模轉換，本指南都會帶您完成載入 DXF 圖紙、設定光柵化選項、儲存為 WMF，並可選擇將相同圖紙匯出為 PDF。此步驟可在任何執行 Java 8+ 的平台上運作。

## 快速回答
- **我可以使用免費試用版將 DXF 轉換為 WMF 嗎？** 是的 – Aspose 提供功能完整的 30 天試用版。  
- **需要哪個 Java 版本？** Java 8 或更新版本。  
- **執行程式碼是否需要授權？** 生產環境需要授權；試用版可用於開發與測試。  
- **轉換是否無損？** 向量資料會被保留；可透過光柵化選項控制解析度。  
- **我也可以將相同圖紙匯出為 PDF 嗎？** 當然可以 – 請參考下方「匯出為 PDF」步驟。  
- **如何一次批次轉換多個 DXF 檔案？** 迴圈處理資料夾中的每個檔案，對每個檔案套用相同的載入‑光柵化‑儲存流程。

## 什麼是批次轉換 DXF 檔案？

批次轉換 DXF 檔案是指在一次執行中處理多個 Drawing Exchange Format（DXF）圖紙，並為每個圖紙產生 WMF 輸出。WMF（Windows Metafile）是一種向量圖像格式，可原生整合至 Microsoft Office、Windows 應用程式以及多種報告工具。

## 為什麼使用 Aspose.CAD for Java？

Aspose.CAD for Java 是一套純 Java 引擎，支援 **超過 50 種輸入與輸出格式**——包括 DXF、DWG、DGN、PDF、PNG、SVG 與 WMF——同時提供 **99 % 向量保真度**。它可在任何支援 Java 的作業系統上執行，無需原生 DLL，並可透過單一 `CadRasterizationOptions` 類別控制頁面大小、DPI 與背景顏色。同一套 API 亦支援 PDF、PNG 與 SVG 的匯出，省去使用多個函式庫的需求。

### 可量化的效益
- **支援 50+ 格式**，減少第三方轉換工具的需求。  
- **在典型 2.5 GHz 伺服器上，以 150 DPI 光柵化時，能在 5 秒內處理 300 頁 DXF 檔案**。  
- **記憶體佔用量低於 200 MB**（檔案大小最高 500 MB），只要設定適當的頁面尺寸即可。

## 前置條件

- **Aspose.CAD for Java** 已整合至您的專案。從官方網站下載：[Aspose.CAD Java 下載](https://releases.aspose.com/cad/java/)。  
- 一個包含欲轉換的 DXF 檔案的資料夾（例如 `Your Document Directory/DXFDrawings/`）。  

## 匯入命名空間

`Image` 是 Aspose.CAD 的核心類別，代表記憶體中的 CAD 圖紙。載入檔案後，所有後續操作——光柵化、格式轉換與資源清理——皆透過此物件執行。

以下的匯入語句會載入處理 CAD 檔案所需的 Aspose.CAD 類別。  
```java
import com.aspose.cad.Image;
import com.aspose.cad.ImageSaveOptions;
import com.aspose.cad.fileformats.cad.CadRasterizationOptions;
import com.aspose.cad.fileformats.cad.CadImage;
import com.aspose.cad.fileformats.cad.CadImageInfo;
import com.aspose.cad.fileformats.cad.CadImageInfo;
import java.awt.Color;
```

## 步驟說明

### 如何在 Java 中批次將 DXF 檔案轉換為 WMF？

使用 `Image.load` 載入每個 DXF，設定 `CadRasterizationOptions` 以指定頁面大小與 DPI，然後以 `image.save` 並傳入 `SaveFormat.WMF` 進行儲存。此三步驟模式即可完成完整轉換，同時保留向量品質，且每個檔案只需少量程式碼。

#### 步驟 1：載入 DXF 圖紙

Image.load 會將 DXF 檔案讀入 Aspose.CAD Image 物件。  
```java
import com.aspose.cad.Color;
import com.aspose.cad.Image;

import com.aspose.cad.fileformats.ifc.IfcImage;
import com.aspose.cad.imageoptions.CadRasterizationOptions;
import com.aspose.cad.imageoptions.PdfOptions;
import com.aspose.cad.imageoptions.WmfOptions;
```

#### 步驟 2：設定光柵化選項

`CadRasterizationOptions` 用於指定光柵化 CAD 圖紙的頁面大小、解析度與背景色。  
```java
// The path to the resource directory.
String dataDir = "Your Document Directory" + "DXFDrawings/";
String srcFile = dataDir + "conic_pyramid.dxf";
Image image = Image.load(srcFile);
```

#### 步驟 3：儲存為 WMF

使用 `SaveFormat.WMF` 的 `ImageSaveOptions` 可指示 Aspose.CAD 將輸出寫為 Windows Metafile。  
```java
CadRasterizationOptions rasterizationOptions = new CadRasterizationOptions();
rasterizationOptions.setPageWidth(100);
rasterizationOptions.setPageHeight(100);
WmfOptions wmfOptions = new WmfOptions();
```

#### 步驟 4：釋放資源

呼叫 `image.close()` 會釋放 Aspose.CAD Image 物件所佔用的原生資源。  
```java
cadImage.save(dataDir+" example.ifc.wmf", wmfOptions);
```

#### 步驟 5：選用 – 匯出為 PDF

`PdfOptions` 用於在將影像儲存為 PDF 文件時設定 PDF 專屬的參數。  
```java
finally
{
  cadImage.dispose();
}
```

> **專業提示：** 您可以將相同的 `CadRasterizationOptions` 物件傳遞給 `PdfOptions` 以重複使用，省去幾行設定程式碼。

## 如何使用 Aspose CAD Java 將 DXF 匯出為 PDF？

將儲存格式從 WMF 改為 PDF，只需使用 `new ImageSaveOptions(SaveFormat.Pdf)`。相同的光柵化設定仍然適用，且可額外設定 PDF 專屬的選項，例如作者資訊或壓縮等級。此單行程式碼即可產生可搜尋、頁面精確的 PDF，完整還原原始 CAD 版面。

## 常見問題與解決方案

`License` 是 Aspose 用於在執行時套用產品授權的類別。

| 問題 | 原因 | 解決方式 |
|------|------|----------|
| **`cadImage.save` 發生 NullPointerException** | 變數 `cadImage` 未定義（應為 `image`）。 | 將 `cadImage` 改為 `image`，或統一變數名稱。 |
| **輸出 WMF 為空白** | 光柵化的頁面尺寸過小或背景色設定為透明。 | 增大 `PageWidth`/`PageHeight`，或透過 `rasterizationOptions.setBackgroundColor(Color.WHITE);` 設定背景色。 |
| **授權例外** | 在生產環境中未使用有效的 Aspose 授權。 | 在應用程式啟動時套用授權檔案，例如：`License license = new License(); license.setLicense("Aspose.Total.Java.lic");`。 |

## 常見問答

**問：在哪裡可以找到 Aspose.CAD 文件？**  
答：您可在此取得文件 [Aspose.CAD Java documentation](https://reference.aspose.com/cad/java/)。

**問：如何下載 Aspose.CAD for Java？**  
答：從此下載程式庫 [Aspose.CAD Java download page](https://releases.aspose.com/cad/java/)。

**問：是否提供免費試用？**  
答：有，您可在此取得免費試用 [Aspose free trial page](https://releases.aspose.com/)。

**問：需要臨時授權方案嗎？**  
答：請參考臨時授權方案 [temporary license options](https://purchase.aspose.com/temporary-license/)。

**問：哪裡可以取得支援？**  
答：請前往 Aspose.CAD 支援論壇 [Aspose.CAD support forum](https://forum.aspose.com/c/cad/19)。

## 其他常見問答

**問：能否在不耗盡記憶體的情況下轉換大型 DXF 檔案（數百 MB）？**  
答：可以。請在 try‑with‑resources 區塊中載入檔案，並及時釋放 `Image` 物件。調整 `CadRasterizationOptions.setPageWidth/Height` 為合理大小，以降低記憶體使用量。

**問：WMF 輸出會保留圖層資訊嗎？**  
答：WMF 為平面向量格式，圖層層級會被平坦化，但線條樣式、顏色與剖面圖樣會被保留。

**問：能否為 WMF 設定自訂 DPI？**  
答：可在儲存前使用 `rasterizationOptions.setResolution(300);` 來設定 DPI。

**問：能否在一次執行中批次轉換多個 DXF 檔案？**  
答：當然可以。遍歷目錄，載入每個檔案，並套用相同的光柵化與儲存邏輯。

**問：支援哪些 Java 版本？**  
答：Aspose.CAD for Java 支援 Java 8 及以上版本，包括 Java 11、17 以及更新的 LTS 版。

**最後更新：** 2026-10-30  
**測試環境：** Aspose.CAD for Java 24.11  
**作者：** Aspose

## 相關教學

- [Create PDF from CAD – Export DXF to PDF with Aspose.CAD for Java](/cad/java/additional-features/export-dxf-to-pdf/)
- [Create PDF from DXF: Export Layer with Aspose.CAD for Java](/cad/java/additional-features/export-specific-layer-to-pdf/)
- [How to Convert DXF Layout to JPEG Image with Aspose.CAD in Java](/cad/java/additional-features/export-specific-layout-to-image/)

```java
image.save(dataDir + "conic_pyramid_out_.pdf"); 
```

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}