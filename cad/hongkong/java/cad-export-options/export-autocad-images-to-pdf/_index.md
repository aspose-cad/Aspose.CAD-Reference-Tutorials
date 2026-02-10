---
date: 2025-12-19
description: 學習如何使用 Aspose.CAD for Java 匯出 AutoCAD PDF。此一步一步的指南將向您展示如何將 DWG 轉換為 PDF、將
  CAD 儲存為 PDF，以及處理授權。
linktitle: Export AutoCAD Images to PDF
second_title: Aspose.CAD Java API
title: 匯出 AutoCAD PDF - 使用 Aspose.CAD for Java 教程將 AutoCAD 圖像匯出為 PDF
url: /zh-hant/java/cad-export-options/export-autocad-images-to-pdf/
weight: 10
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# 匯出 AutoCAD PDF - 使用 Aspose.CAD for Java 匯出 AutoCAD 圖像為 PDF

## 介紹

您是否想要在 Java 中無縫 **匯出 AutoCAD PDF**？不必再尋找！本教學將帶您使用 Aspose.CAD for Java 這個強大的函式庫，將 AutoCAD 圖像轉換為 PDF，讓 **convert DWG to PDF** 的流程變得輕鬆。完成後，您將了解如何 **save CAD as PDF**、套用自訂光柵化設定，並在正式環境中使用 Aspose.CAD 授權。

## 快速回答
- **可以使用 Java 轉換 DWG 為 PDF 嗎？** 可以，Aspose.CAD for Java 支援 DWG、DXF 以及許多其他格式。  
- **需要授權嗎？** 需要 **Aspose CAD license** 才能無限制使用；亦提供暫時授權供評估使用。  
- **支援哪個 Java 版本？** Java 8 以上（函式庫相容於所有現代 JDK）。  
- **可以自訂 PDF 頁面大小嗎？** 當然可以——在光柵化選項中調整 `pageWidth` 與 `pageHeight`。  
- **支援 3‑D 光柵化嗎？** 支援，啟用 `TypeOfEntities.Entities3D` 即可完成完整的 3‑D 渲染。

## 什麼是 **export autocad pdf**？
匯出 AutoCAD PDF 指的是將向量式 CAD 圖紙（DWG、DXF、DWF 等）轉換為可攜式 PDF 文件，同時保留圖層、線寬，並可選擇保留 3‑D 幾何。此功能適用於與客戶共享設計、歸檔或在不安裝 CAD 軟體的情況下列印。

## 為什麼使用 Aspose.CAD for Java 來 **export autocad pdf**？
- **完整格式支援** – 可處理 DWG、DXF、DWF 等多種格式。  
- **無外部相依** – 純 Java 函式庫，無需原生 DLL。  
- **高品質光柵化** – 可控制 DPI、頁面大小與版面配置。  
- **授權彈性** – 先使用免費試用版，之後升級為永久 **Aspose CAD license**。

## 前置條件

在開始之前，請確保您已具備：

- **Java 開發環境** – 已安裝 JDK 8 或更新版本。  
- **Aspose.CAD for Java 函式庫** – 從[下載連結](https://releases.aspose.com/cad/java/)取得。  
- **文件目錄** – 在本機建立一個資料夾，用於放置來源 CAD 檔案與產生的 PDF。

## 匯入命名空間

在您的 Java 專案中，匯入使用 Aspose.CAD 所需的類別：

```java
import com.aspose.cad.Image;

import com.aspose.cad.imageoptions.CadRasterizationOptions;
import com.aspose.cad.imageoptions.PdfOptions;
//import com.aspose.cad.imageoptions.TypeOfEntities;
```

接下來，我們將一步一步說明程式碼。

## 步驟說明

### 步驟 1：設定資源目錄路徑

```java
String dataDir = "Your Document Directory" + "ExportingCAD/";
```

> **小技巧：** 將 `"Your Document Directory"` 替換為您在前置條件中建立的資料夾的絕對路徑。

### 步驟 2：載入 CAD 圖像

```java
String srcFile = dataDir + "conic_pyramid.dxf";
Image cadImage = Image.load(srcFile);
```

> **為什麼重要：** 將 CAD 檔案載入 `Image` 物件，可完整存取 Aspose.CAD 的光柵化引擎。

### 步驟 3：設定光柵化選項

```java
CadRasterizationOptions rasterizationOptions = new CadRasterizationOptions();
rasterizationOptions.setPageWidth(500);
rasterizationOptions.setPageHeight(500);
// rasterizationOptions.setTypeOfEntities(TypeOfEntities.Entities3D);

rasterizationOptions.setLayouts(new String[] {"Model"});
```

- 調整 `pageWidth` 與 `pageHeight` 以改變輸出 PDF 的尺寸。  
- 若需 **java convert cad pdf** 的 3‑D 實體，取消註解 `setTypeOfEntities` 那一行。  
- `setLayouts` 呼叫可選擇要渲染的版面（Model、Layout1 等）。

### 步驟 4：設定 PDF 選項

```java
PdfOptions pdfOptions = new PdfOptions();
pdfOptions.setVectorRasterizationOptions(rasterizationOptions);
```

此步驟將光柵化設定與 PDF 輸出關聯，確保向量資料正確轉換。

### 步驟 5：儲存 PDF

```java
cadImage.save(dataDir + "Export3DImagestoPDF_out_.pdf", pdfOptions);
```

產生的檔案 `Export3DImagestoPDF_out_.pdf` 即為您原始 AutoCAD 圖紙的 **save cad as pdf** 版本。

## 常見問題與解決方案

| 症狀 | 可能原因 | 解決方式 |
|------|----------|----------|
| PDF 為空白 | 未設定光柵化選項或版面不符 | 確認 `setLayouts` 與 CAD 檔案中的版面名稱相符。 |
| 影像解析度低 | `pageWidth`/`pageHeight` 設定過小 | 增大尺寸或透過 `rasterizationOptions.setResolution(...)` 設定更高 DPI。 |
| 授權例外 | 未套用有效授權 | 套用 **Aspose CAD license**，或使用暫時授權進行測試。 |

## 常見問答

### Q1：可以在 Java 中使用 Aspose.CAD 處理其他 CAD 檔案格式嗎？
A1：可以，Aspose.CAD 支援包括 DWG、DWF、DGN 等多種格式，讓您的專案更具彈性。

### Q2：如何取得 Aspose.CAD for Java 的暫時授權？
A2：請前往[此處](https://purchase.aspose.com/temporary-license/)取得評估用的暫時授權。

### Q3：光柵化有提供版面選項嗎？
A3：有，您可透過 `setLayouts` 方法自訂版面（例如 `"Model"`、`"Layout1"`），決定要渲染哪個視圖。

### Q4：可以自訂輸出 PDF 檔案的大小嗎？
A4：當然可以！只要在光柵化選項中調整 `pageWidth` 與 `pageHeight` 即可符合需求。

### Q5：若需要協助或討論 Aspose.CAD for Java 的相關問題，該去哪裡？
A5：請前往 [Aspose.CAD 論壇](https://forum.aspose.com/c/cad/19) 尋求專屬支援與社群討論。

---

**最後更新：** 2025-12-19  
**測試環境：** Aspose.CAD for Java 24.10  
**作者：** Aspose  

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}