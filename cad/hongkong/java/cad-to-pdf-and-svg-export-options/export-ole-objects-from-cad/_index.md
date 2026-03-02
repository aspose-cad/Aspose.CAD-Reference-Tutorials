---
date: 2026-03-02
description: 解鎖 Aspose.CAD for Java 的潛能。輕鬆匯出 OLE 物件並 **將 CAD 儲存為 PNG**。立即下載，實現無縫的
  CAD 資料管理。
linktitle: Export OLE Objects from CAD
second_title: Aspose.CAD Java API
title: 將 CAD 儲存為 PNG – 使用 Aspose.CAD for Java 匯出 OLE 物件
url: /zh-hant/java/cad-to-pdf-and-svg-export-options/export-ole-objects-from-cad/
weight: 10
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# 將 CAD 另存為 PNG – 使用 Aspose.CAD for Java 匯出 OLE 物件

## Introduction

在快速變化的電腦輔助設計（CAD）領域中，高效管理與擷取 OLE（Object Linking and Embedding）物件——以及能夠 **將 CAD 另存為 PNG**——對於報告、網頁預覽或歸檔等下游工作流程至關重要。Aspose.CAD for Java 提供一個強大的、以程式碼為先的解決方案，讓您只需幾行程式碼即可同時匯出 OLE 物件並將 CAD 圖紙轉換為高品質的 PNG 圖像。

## Quick Answers
- **Aspose.CAD 的功能是什麼？** 它能讀取、操作並轉換 CAD 檔案（DWG、DXF、DGN 等），無需安裝原生 CAD 軟體。  
- **我可以將 CAD 另存為 PNG 嗎？** 可以——使用 `PngOptions` 搭配 `CadRasterizationOptions` 來光柵化任何版面。  
- **如何匯出 OLE 物件？** 使用 `Image.load` 載入 CAD 檔案，然後將每個含有 OLE 的版面另存為 PNG。  
- **我需要授權嗎？** 有免費試用版；商業授權可移除評估限制。  
- **需要哪個 Java 版本？** 完全支援 Java 8 及以上版本。

## What is **save CAD as PNG**?
將 CAD 另存為 PNG 意指將向量式 CAD 圖紙光柵化為像素式的 PNG 圖像。當您需要輕量且在任何平台皆可檢視的格式（如網頁、行動應用程式或文件）時，此轉換非常實用。

## Why use Aspose.CAD for Java to **convert CAD to PNG**?
- **不需安裝 CAD** – 此函式庫完全在 Java 中運作。  
- **保留版面精確度** – 您可以選擇特定版面、控制 DPI，並保持線條品質。  
- **批次處理** – 只需簡單迴圈即可遍歷多個檔案。  
- **匯出 OLE 物件** – 嵌入於 DWG/DXF 檔案的 OLE 內容會自動渲染至 PNG 輸出。

## Prerequisites

Before diving into the tutorial, make sure you have the following prerequisites in place:

- **Java 環境** – 確保您的機器已設定 Java 開發環境。  
- **Aspose.CAD for Java** – 下載並安裝 Aspose.CAD for Java 函式庫。您可於 [download link](https://releases.aspose.com/cad/java/) 取得。  
- **CAD 檔案** – 準備包含您想匯出的 OLE 物件的 CAD 檔案。

## Import Namespaces

首先，將必要的命名空間匯入您的 Java 專案。這些命名空間提供使用 Aspose.CAD 處理 CAD 檔案所需的核心類別與功能。

```java
import com.aspose.cad.Image;

import com.aspose.cad.fileformats.cad.CadImage;
import com.aspose.cad.imageoptions.CadRasterizationOptions;
import com.aspose.cad.imageoptions.PngOptions;
```

現在，讓我們將從 CAD 匯出 OLE 物件的流程分解為多個步驟：

## How to **save CAD as PNG** and export OLE objects

### Step 1: Set Your Document Directory

```java
String dataDir = "Your Document Directory" + "DWGDrawings/";
```

請將 `"Your Document Directory"` 替換為包含 CAD 檔案之目錄的實際路徑。

### Step 2: Define CAD File Names

```java
String[] files = new String[] { "D ZD junior D10m H2m.dwg", "ZD - Senior D6m H2m45.dwg" };
```

指定您想在 `files` 陣列中處理的 CAD 檔案名稱。

### Step 3: Set PNG Export Options

```java
PngOptions pngOptions = new PngOptions();
CadRasterizationOptions rasterizationOptions = new CadRasterizationOptions();
pngOptions.setVectorRasterizationOptions(rasterizationOptions);
rasterizationOptions.setLayouts(new String[] { "Layout1" });
```

設定 PNG 匯出選項，包括向量光柵化與版面設定。這些選項即是讓您 **convert CAD to PNG** 並取得期望品質的關鍵。

### Step 4: Iterate Through CAD Files

```java
for(String file : files)
{
    CadImage cadImage = (CadImage)Image.load(dataDir + file);
    cadImage.save(dataDir + file + "_out.png", pngOptions);
}
```

遍歷每個指定的 CAD 檔案，使用 Aspose.CAD 載入，並將 OLE 物件另存為 PNG 圖像。此迴圈示範了以批次方式 **convert DWG to PNG** 的簡易方法。

## Common Issues and Solutions

| 問題 | 原因 | 解決方案 |
|-------|-------|----------|
| **空白 PNG 輸出** | 版面名稱不匹配 | 確認來源 DWG 中存在版面名稱 (`"Layout1"`)。 |
| **缺少 OLE 圖形** | OLE 物件儲存在其他版面 | 在 `rasterizationOptions.setLayouts(...)` 中加入所有相關版面。 |
| **大型檔案記憶體不足錯誤** | DPI 設定過高 | 透過 `rasterizationOptions.setResolution(...)` 降低 DPI，或一次處理單一檔案。 |

## Frequently Asked Questions

**Q: Aspose.CAD 是否相容所有 CAD 檔案格式？**  
A: Aspose.CAD 支援多種 CAD 格式，包括 DWG、DXF 與 DGN。完整列表請參考 [documentation](https://reference.aspose.com/cad/java/)。

**Q: 我可以自訂 OLE 物件的匯出設定嗎？**  
A: 可以，Aspose.CAD 提供廣泛的選項讓您自訂匯出設定，以符合特定需求。

**Q: 是否提供 Aspose.CAD 的免費試用？**  
A: 有，您可從 [here](https://releases.aspose.com/) 取得免費試用版以探索其功能。

**Q: 在哪裡可以取得 Aspose.CAD 的社群支援？**  
A: 加入 Aspose.CAD 社群於 [forum](https://forum.aspose.com/c/cad/19) 取得協助並分享使用經驗。

**Q: 如何購買 Aspose.CAD 的授權？**  
A: 前往 [purchase page](https://purchase.aspose.com/buy) 取得符合開發需求的授權。

## Conclusion

透過這些簡單卻功能強大的步驟，您即可使用 Aspose.CAD for Java 無縫 **將 CAD 另存為 PNG**，同時匯出 CAD 檔案中的 OLE 物件。此多功能工具讓開發者能有效管理 CAD 資料，為 CAD 應用程式開發與下游影像工作流程開啟全新可能。

---

**Last Updated:** 2026-03-02  
**Tested With:** Aspose.CAD for Java 24.12  
**Author:** Aspose  

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}