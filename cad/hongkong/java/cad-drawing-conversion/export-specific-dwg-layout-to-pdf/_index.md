---
date: 2025-12-21
description: 學習如何使用 Aspose.CAD for Java，將特定 DWG 佈局匯出為 PDF，將 DWG 轉換為 PDF。請跟隨此一步一步的
  DWG 轉 PDF 教學，簡化您的 CAD 工作流程。
linktitle: Export Specific DWG Layout to PDF
second_title: Aspose.CAD Java API
title: 將 DWG 轉換為 PDF – 使用 Aspose.CAD for Java 匯出版面
url: /zh-hant/java/cad-drawing-conversion/export-specific-dwg-layout-to-pdf/
weight: 14
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# 將 DWG 轉換為 PDF – 使用 Aspose.CAD for Java 匯出特定版面

## 簡介

在不斷變化的電腦輔助設計（CAD）領域，**convert DWG to PDF** 是在與客戶、承建商或非技術持份者共享圖紙時的常見需求。Aspose.CAD for Java 讓此轉換變得輕鬆，甚至可以從多版面 DWG 檔案中挑選單一版面。在本教學中，我們將逐步說明 **如何將 DWG**‑特定版面匯出為 PDF，讓您能精確提供項目所需的內容，而不會產生多餘頁面或需手動裁切。

## 快速解答
- **convert DWG to PDF 是什麼意思？** 它將 DWG 圖紙轉換為 PDF 文件，保留向量資料與版面忠實度。  
- **哪個函式庫負責轉換？** Aspose.CAD for Java 提供即用的 API。  
- **生產環境需要授權嗎？** 是的，需要商業授權；免費試用可用於評估。  
- **可以選擇單一版面嗎？** 當然可以 – 設定 `Layouts` 屬性為目標版面名稱。  
- **支援哪個 Java 版本？** 完全相容於 Java 8 及以上版本。

## 先決條件

在開始之前，請確保您已具備以下條件：

- **Java 開發環境** – JDK 8+ 以及您喜愛的 IDE。  
- **Aspose.CAD 函式庫** – 從官方網站 **[here](https://releases.aspose.com/cad/java/)** 下載最新 JAR。  
- **DWG 檔案** – 包含至少一個版面的圖紙（例如 *visualization_-_conference_room.dwg*）。

## 為什麼要將特定 DWG 版面匯出為 PDF？

許多 DWG 檔案包含多個紙張空間（版面）。匯出整個檔案會產生包含不需要頁面的龐大 PDF。選擇單一版面：

- 減少檔案大小。  
- 將檢視者的注意力聚焦於相關的圖紙。  
- 符合專案文件標準。  

## 逐步指南

### 步驟 1：設定專案環境

建立新的 Java 專案（Maven、Gradle 或純 IDE），並將 Aspose.CAD JAR 加入 classpath。您可以在 **[here](https://releases.aspose.com/cad/java/)** 下載。

### 步驟 2：匯入必要的套件

將所需的 Aspose.CAD 命名空間加入您的 Java 類別中。

```java
import com.aspose.cad.Image;
import com.aspose.cad.imageoptions.CadRasterizationOptions;
import com.aspose.cad.imageoptions.PdfOptions;
```

### 步驟 3：載入 DWG 檔案

指向您想要轉換的 DWG，並將其載入 `Image` 物件。

```java
String srcFile = dataDir + "visualization_-_conference_room.dwg";
Image image = Image.load(srcFile);
```

### 步驟 4：設定光柵化選項

定義頁面尺寸，且關鍵是設定您想要匯出的版面。

```java
CadRasterizationOptions rasterizationOptions = new CadRasterizationOptions();
rasterizationOptions.setPageWidth(1600);
rasterizationOptions.setPageHeight(1600);
// Specify desired layout name
rasterizationOptions.setLayouts(new String[] {"Layout1"});
```

### 步驟 5：設定 PDF 匯出選項

將光柵化設定與 PDF 匯出器關聯。

```java
PdfOptions pdfOptions = new PdfOptions();
pdfOptions.setVectorRasterizationOptions(rasterizationOptions);
```

### 步驟 6：將 DWG 匯出為 PDF

將結果儲存為 PDF 檔案。輸出將僅包含 **Layout1**，實現乾淨的 **convert DWG to PDF** 操作。

```java
image.save(dataDir + "ExportSpecificLayoutToPDF_out_.pdf", pdfOptions);
```

## 常見問題與解決方案

| 問題 | 為何發生 | 解決方式 |
|-------|----------------|-----|
| **找不到版面** | 版面名稱拼寫錯誤或在 DWG 中不存在。 | 使用 `image.getLayoutNames()` 列出可用版面，然後選擇正確的版面。 |
| **PDF 解析度低** | `PageWidth`/`PageHeight` 太小。 | 增大尺寸（例如 2000 × 2000）或設定 `rasterizationOptions.setResolution(300);`。 |
| **授權例外** | 在非試用環境下未使用有效授權執行。 | 在載入影像前套用您的 Aspose.CAD 授權：`License license = new License(); license.setLicense("Aspose.CAD.lic");`。 |

## 常見問答

**Q1：我可以將 Aspose.CAD for Java 與其他基於 Java 的 CAD 函式庫一起使用嗎？**  
A：Aspose.CAD for Java 為獨立函式庫，但可與其他基於 Java 的函式庫整合，以擴充功能。

**Q2：Aspose.CAD 有哪些授權方案？**  
A：有的，您可以在 **[here](https://purchase.aspose.com/buy)** 查看授權方案與購買細節。

**Q3：如何取得 Aspose.CAD 的臨時授權？**  
A：請前往 **[this link](https://purchase.aspose.com/temporary-license/)** 申請臨時授權。

**Q4：在哪裡可以取得 Aspose.CAD 的支援？**  
A：如有任何問題或需要協助，請造訪 **[Aspose.CAD forum](https://forum.aspose.com/c/cad/19)**。

**Q5：Aspose.CAD 是否提供免費試用？**  
A：有的，您可以在 **[here](https://releases.aspose.com/)** 取得免費試用。

## 結論

透過本 **dwg to pdf tutorial**，您現在擁有可靠的方式在針對單一版面時 **convert DWG to PDF**。此方法可節省儲存空間、加快文件共享，並保持 CAD 工作流程整潔。隨著專案發展，您可自由嘗試不同的光柵化設定，或將多個版面合併成單一 PDF。

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}

---

**Last Updated:** 2025-12-21  
**Tested With:** Aspose.CAD for Java 24.12  
**Author:** Aspose