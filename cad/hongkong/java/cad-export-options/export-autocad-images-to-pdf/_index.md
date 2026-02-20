---
date: 2026-02-20
description: 學習如何使用 Aspose.CAD for Java 匯出 AutoCAD PDF。本分步指南將向您展示如何 **將 DWG 轉換為 PDF**、**將
  CAD 儲存為 PDF**，以及如何處理授權。
linktitle: Export AutoCAD Images to PDF
second_title: Aspose.CAD Java API
title: 將 DWG 轉換為 PDF - 使用 Aspose.CAD for Java 將 AutoCAD 圖像匯出為 PDF
url: /zh-hant/java/cad-export-options/export-autocad-images-to-pdf/
weight: 10
---

 code blocks, shortcodes, links, etc. Keep them.

Make sure to preserve markdown formatting.

Proceed to output.{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# 匯出 AutoCAD PDF - 使用 Aspose.CAD for Java 匯出 AutoCAD 圖像為 PDF

## 介紹

您是否正在尋找使用 Java **convert DWG to PDF**？不必再找了！在本教學中，我們將帶您一步步使用 Aspose.CAD for Java 將 AutoCAD 圖像轉換為 PDF，這是一個強大的函式庫，可讓 **convert DWG to PDF** 的過程變得輕鬆。最後，您將了解如何 **save CAD as PDF**、套用自訂光柵化設定，並在生產環境中使用 Aspose.CAD 授權。

## 快速解答
- **Can I convert DWG to PDF with Java?** 是的，Aspose.CAD for Java 能處理 DWG、DXF 以及許多其他格式。  
- **Do I need a license?** 需要 **Aspose CAD license** 才能無限制使用；亦提供臨時授權供評估使用。  
- **What Java version is supported?** 支援 Java 8+（此函式庫相容於所有現代 JDK）。  
- **Can I customize PDF page size?** 當然可以 – 在光柵化選項中調整 `pageWidth` 與 `pageHeight`。  
- **Is 3‑D rasterization possible?** 是的，啟用 `TypeOfEntities.Entities3D` 即可完成完整的 3‑D 渲染。

## 什麼是 **export autocad pdf**？

匯出 AutoCAD PDF 指的是將向量式 CAD 圖紙（DWG、DXF、DWF 等）轉換為可攜式 PDF 文件，同時保留圖層、線寬，並可選擇保留 3‑D 幾何。此功能適用於與客戶共享設計、存檔或在不需 CAD 軟體的情況下列印。

## 為什麼要使用 Aspose.CAD for Java 轉換 DWG 為 PDF？

- **Full format support** – 支援 DWG、DXF、DWF 以及更多格式。  
- **No external dependencies** – 純 Java 函式庫，無需原生 DLL。  
- **High‑quality rasterization** – 可控制 DPI、頁面大小與版面配置，讓您能 **customize PDF page size** 以符合專案需求。  
- **License flexibility** – 可先使用免費試用版，之後升級為永久 **Aspose CAD license**。  

## 前置條件

- **Java Development Environment** – 已安裝 JDK 8 或更新版本。  
- **Aspose.CAD for Java Library** – 從 [download link](https://releases.aspose.com/cad/java/) 下載。  
- **Document Directory** – 您機器上的資料夾，用於存放來源 CAD 檔案與產生的 PDF。  

## 匯入命名空間

在您的 Java 專案中，匯入使用 Aspose.CAD 所需的類別：

```java
import com.aspose.cad.Image;

import com.aspose.cad.imageoptions.CadRasterizationOptions;
import com.aspose.cad.imageoptions.PdfOptions;
//import com.aspose.cad.imageoptions.TypeOfEntities;
```

現在讓我們一步步走過程式碼。

## 如何使用 Aspose.CAD for Java 轉換 DWG 為 PDF

### 步驟 1：設定資源目錄路徑

```java
String dataDir = "Your Document Directory" + "ExportingCAD/";
```

> **Pro tip:** 將 `"Your Document Directory"` 替換為您在前置條件中建立的資料夾之絕對路徑。

### 步驟 2：載入 CAD 圖像

```java
String srcFile = dataDir + "conic_pyramid.dxf";
Image cadImage = Image.load(srcFile);
```

> **Why this matters:** 將 CAD 檔載入 `Image` 物件，即可完整存取 Aspose.CAD 的光柵化引擎。

### 步驟 3：設定光柵化選項

```java
CadRasterizationOptions rasterizationOptions = new CadRasterizationOptions();
rasterizationOptions.setPageWidth(500);
rasterizationOptions.setPageHeight(500);
// rasterizationOptions.setTypeOfEntities(TypeOfEntities.Entities3D);

rasterizationOptions.setLayouts(new String[] {"Model"});
```

- 調整 `pageWidth` 與 `pageHeight` 以 **customize PDF page size**。  
- 若需 3‑D 實體的 **java convert cad pdf**，請取消註解 `setTypeOfEntities` 行。  
- `setLayouts` 呼叫會選擇要渲染的版面（Model、Layout1 等）。

### 步驟 4：設定 PDF 選項

```java
PdfOptions pdfOptions = new PdfOptions();
pdfOptions.setVectorRasterizationOptions(rasterizationOptions);
```

此設定將光柵化選項與 PDF 輸出關聯，確保向量資料正確轉換。

### 步驟 5：儲存 PDF

```java
cadImage.save(dataDir + "Export3DImagestoPDF_out_.pdf", pdfOptions);
```

產生的檔案 `Export3DImagestoPDF_out_.pdf` 為您原始 AutoCAD 圖紙的 **save cad as pdf** 表現。

## 常見問題與解決方案

| 症狀 | 可能原因 | 解決方案 |
|------|----------|----------|
| 空白 PDF 輸出 | 未設定光柵化選項或版面不匹配 | 確認 `setLayouts` 與 CAD 檔中的版面名稱相符。 |
| 低解析度影像 | `pageWidth`/`pageHeight` 設定過小 | 增加尺寸或透過 `rasterizationOptions.setResolution(...)` 設定更高 DPI。 |
| 授權例外 | 未套用有效授權 | 套用 **Aspose CAD license** 或使用臨時授權進行測試。 |

## 常見問答

### Q1：我可以在 Aspose.CAD for Java 中使用其他 CAD 檔案格式嗎？

A1：是的，Aspose.CAD 支援包括 DWG、DWF、DGN 等在內的多種格式，為您的專案提供彈性。

### Q2：我該如何取得 Aspose.CAD for Java 的臨時授權？

A2：請前往 [here](https://purchase.aspose.com/temporary-license/) 取得評估用的臨時授權。

### Q3：光柵化是否有版面選項？

A3：是的，您可以透過 `setLayouts` 方法自訂版面（例如 `"Model"`、`"Layout1"`），以控制要渲染的視圖。

### Q4：我可以自訂輸出 PDF 檔的大小嗎？

A4：當然可以！在光柵化選項中調整 `pageWidth` 與 `pageHeight` 參數，即可符合您想要的尺寸。

### Q5：我可以在哪裡尋求協助或討論 Aspose.CAD for Java 相關問題？

A5：請前往 [Aspose.CAD forum](https://forum.aspose.com/c/cad/19) 獲得專屬支援與社群討論。

**最後更新：** 2026-02-20  
**測試環境：** Aspose.CAD for Java 24.10  
**作者：** Aspose  

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}