---
date: 2025-12-08
description: 了解如何使用 Aspose.CAD for Java 將 IGES 轉換為 PDF。請遵循本分步指南，將 IGES 格式整合並產生高品質的
  PDF 檔案。
language: zh-hant
linktitle: Integrate IGES Format
second_title: Aspose.CAD Java API
title: 如何使用 Aspose.CAD for Java 將 IGES 轉換為 PDF
url: /java/advanced-cad-features/integrate-iges-format/
weight: 11
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# 如何使用 Aspose.CAD for Java 將 IGES 轉換為 PDF

## Introduction

在現代 CAD 開發中，能夠 **將 IGES 轉換為 PDF** 快速且可靠是常見需求。無論您需要與非技術持份者分享設計，或是將圖紙存檔為可攜式格式，Aspose.CAD for Java 都能讓轉換過程變得簡單。在本教學中，我們將逐步示範完整的實作範例，說明如何載入 IGES 檔案、設定光柵化選項，並將結果儲存為 PDF 文件。

## Quick Answers
- **此教學涵蓋什麼內容？** 使用 Aspose.CAD for Java 將 IGES 檔案轉換為 PDF。  
- **實作需要多長時間？** 基本設定大約需要 10‑15 分鐘。  
- **先決條件是什麼？** 已安裝 JDK、已將 Aspose.CAD 函式庫加入專案，以及一個用於 CAD 檔案的資料夾。  
- **需要授權嗎？** 測試時可使用臨時授權；正式環境需購買正式授權。  
- **可以自訂 PDF 大小嗎？** 可以——光柵化選項允許設定頁面寬度、高度及其他參數。

## What is “convert IGES to PDF”?

「將 IGES 轉換為 PDF」這個說法描述的是將以 IGES（Initial Graphics Exchange Specification，初始圖形交換規範）格式儲存的設計——一種中立的 CAD 交換格式——轉換為 PDF 檔案的過程。PDF 可在任何裝置上檢視，無需專業 CAD 軟體。Aspose.CAD 透過解析 IGES 幾何資訊並將其光柵化為高解析度 PDF，完成繁重的工作。

## Why Convert IGES to PDF with Aspose.CAD?

- **平台獨立性：** PDF 檔案幾乎可在任何作業系統上開啟。  
- **保留視覺忠實度：** Aspose.CAD 的光柵化引擎能維持原始 IGES 圖紙的精確外觀。  
- **自動化就緒：** 可從 Java 服務、批次工作或桌面應用程式呼叫 API，實現全自動工作流程。  
- **無外部相依性：** 不需額外的 CAD 檢視器或轉換器，所有功能皆在 Java 程序內執行。

## Prerequisites

在開始之前，請確保您具備以下項目：

- **Java Development Kit (JDK)：** 已在電腦上安裝 Java 8 或更新版本。  
- **Aspose.CAD for Java：** 從官方 [Aspose.CAD 下載頁面](https://releases.aspose.com/cad/java/) 下載最新 JAR。  
- **文件目錄：** 建立一個資料夾（例如 `data/`），用來放置來源 IGES 檔案以及儲存產生的 PDF。請在程式碼中將 `dataDir` 變數調整指向此資料夾。

## Import Namespaces

以下匯入語句是轉換程式碼所必需的，請放在 Java 原始檔的最上方：

```java
import com.aspose.cad.Image;
import com.aspose.cad.Image;

import com.aspose.cad.imageoptions.CadRasterizationOptions;
import com.aspose.cad.imageoptions.PdfOptions;
```

> **專業提示：** 重複的 `import com.aspose.cad.Image;` 行不會造成問題，但可移除以讓檔案更整潔。

## Step 1: Load the IGES File

```java
String sourceFilePath = dataDir + "figa2.igs";
Image igesImage = Image.load(sourceFilePath);
```

此處我們將 IGES 檔案 (`figa2.igs`) 載入為 `Image` 物件。該物件現在在記憶體中代表 CAD 圖紙，可供後續處理。

## Step 2: Set Up Output Path and PDF Options

```java
String outPath = dataDir + "meshes.pdf";
PdfOptions pdf = new PdfOptions();
CadRasterizationOptions vectorOptions = new CadRasterizationOptions();
vectorOptions.setPageHeight(1000);
vectorOptions.setPageWidth(1000);
pdf.setVectorRasterizationOptions(vectorOptions);
```

我們定義輸出路徑 (`meshes.pdf`) 並設定光柵化選項。透過設定 `PageHeight` 與 `PageWidth`，即可控制產生 PDF 頁面的尺寸，這在需要特定版面或 DPI 時相當有用。

## Step 3: Save the Resulting PDF

```java
igesImage.save(outPath, pdf);
```

`save` 方法執行實際的 **將 IGES 轉換為 PDF** 操作。呼叫完成後，您會在 `dataDir` 資料夾中看到完整渲染的 PDF 檔案。

## Common Use Cases

- **專案文件化：** 將設計檔案轉換為 PDF，以納入技術手冊。  
- **客戶審閱：** 與沒有 CAD 軟體的客戶分享唯讀 PDF。  
- **批次處理：** 自動將大量 IGES 資料庫轉換為 PDF，以便存檔。

## Troubleshooting & Tips

| 問題 | 解決方案 |
|-------|----------|
| **File not found** | 確認 `dataDir` 指向正確的資料夾，且 `figa2.igs` 確實存在。 |
| **Blank PDF output** | 確認 IGES 檔案包含可見的幾何圖形，且光柵化選項設定了足夠的頁面大小。 |
| **Performance bottleneck on large files** | 增加 JVM 堆積大小 (`-Xmx`) 或將檔案分批處理。 |

## Frequently Asked Questions

**問：Aspose.CAD 是否相容其他 CAD 格式？**  
答：是的，Aspose.CAD 支援 DWG、DXF、DGN、STL 等多種格式，除了 IGES 之外。

**問：我可以自訂向量圖像的光柵化選項嗎？**  
答：當然可以！您可以透過 `CadRasterizationOptions` 調整頁面尺寸、背景顏色，甚至線條粗細。

**問：Aspose.CAD 有提供臨時授權嗎？**  
答：有，您可在此取得試用授權 [here](https://purchase.aspose.com/temporary-license/)。

**問：我可以在哪裡尋求 Aspose.CAD 的協助或社群支援？**  
答：Aspose.CAD 社群論壇是提問的好去處——請前往 [here](https://forum.aspose.com/c/cad/19)。

**問：如何購買 Aspose.CAD 授權？**  
答：您可在此購買完整授權 [here](https://purchase.aspose.com/buy)，解鎖全部功能並移除評估限制。

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}

---

**最後更新時間：** 2025-12-08  
**測試環境：** Aspose.CAD for Java 24.12 (latest at time of writing)  
**作者：** Aspose  

---