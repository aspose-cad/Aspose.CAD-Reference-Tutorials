---
date: 2026-01-10
description: 學習如何將 DGN 匯出為 DWG，並使用 Aspose.CAD for Java 將 MicroStation DGN 轉換為 AutoCAD
  DWG。逐步指南。
linktitle: Export DGN as Part of DWG
second_title: Aspose.CAD Java API
title: 使用 Aspose.CAD for Java 將 DGN 匯出為 DWG
url: /zh-hant/java/dgn-export-options/export-dgn-as-part-of-dwg/
weight: 10
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# 使用 Aspose.CAD for Java 將 DGN 匯出為 DWG

## 簡介

## 快速解答
- **What does “export dgn to dwg” achieve?** 它會將 DGN 底圖嵌入 DWG 中，讓在 AutoCAD 中能夠無縫檢視。
- **Which format can I export the result to for quick preview?** 您可以使用 `PdfOptions` **export cad file to pdf**。
- **Do I need a license to run the code?** 在正式環境中需要臨時或付費的 Aspose.CAD 授權。
- **What Java version is supported?** Java 8 或更新版本可與最新的 Aspose.CAD for Java 版一起使用。
- **Is there a free trial available?** 有 – 可從 Aspose 官方網站下載試用版。

## 什麼是「export dgn to dwg」？
將 DGN 匯出為 DWG 表示將 MicroStation DGN 設計轉換或嵌入為 AutoCAD DWG 圖紙中的底圖。這讓 CAD 專業人員能夠利用現有的 DGN 資產，而無需從頭重新建立幾何圖形。

## 為什麼要將 MicroStation DGN 轉換為 AutoCAD DWG？
- **Collaboration:** 使用 AutoCAD 的團隊可以直接檢視與編輯 DGN 內容。
- **Standardization:** DWG 是許多後續工作流程的事實上標準格式（例如 PDF 產生、3D 渲染）。
- **Preservation:** 保留原始 DGN 參考，減少資料遺失。

## 先決條件

在開始本教學之前，請確保已具備以下先決條件：
1. **Aspose.CAD Library:** 下載並安裝 Aspose.CAD for Java 函式庫。您可於 [此處](https://releases.aspose.com/cad/java/) 取得函式庫。
2. **Java Development Kit (JDK)：** 確認系統已安裝 Java。
3. **Integrated Development Environment (IDE)：** 選擇如 Eclipse 或 IntelliJ 等 Java IDE，以獲得更順暢的開發體驗。

## 匯入套件

在您的 Java 專案中，匯入必要的 Aspose.CAD 套件以啟用 CAD 檔案操作。以下為範例：

```java
import com.aspose.cad;
import com.aspose.cad.imageoptions;
import com.aspose.cad.fileformats.cad.cadconsts;
import com.aspose.cad.fileformats.cad;
import com.aspose.cad.fileformats.cad.cadobjects;
```

## 步驟 1：設定檔案路徑

為 DWG 檔案定義輸入與輸出路徑。相應地更新 `dataDir`、`fileName` 與 `outPath` 變數。

```java
String dataDir = "Your Document Directory" + "ExportingDGN/";
String fileName = dataDir + "BlockRefDgn.dwg";
String outPath = dataDir + "BlockRefDgn.dwg.pdf";
```

## 步驟 2：建立 PdfOptions 實例

建立 `PdfOptions` 類別的實例，因為我們要 **export the CAD file to PDF** 以快速驗證。

```java
PdfOptions exportOptions = new PdfOptions();
```

## 步驟 3：載入 DWG 檔案

將現有的 DWG 檔案載入為影像，並轉換為 `CadImage` 類型。

```java
CadImage cadImage = (CadImage) Image.load(fileName);
```

## 步驟 4：遍歷實體

逐一檢查 DWG 檔案中的每個實體，判斷其是否為影像定義。若是，則取得對該物件的外部參考。

```java
for (CadBaseEntity baseEntity : cadImage.getEntities()) {
    if (baseEntity.getTypeName() == CadEntityTypeName.DGNUNDERLAY) {
        CadDgnUnderlay dgnFile = (CadDgnUnderlay)baseEntity;
        System.out.println(dgnFile.getUnderlayPath());
    }
}
```

## 步驟 5：定義光柵化選項

為 `CadRasterizationOptions` 物件設定參數，包括頁面寬度、高度、版面配置與背景顏色。

```java
CadRasterizationOptions vectorRasterizationOptions = new CadRasterizationOptions();
vectorRasterizationOptions.setPageWidth(1600);
vectorRasterizationOptions.setPageHeight(1600);
vectorRasterizationOptions.setLayouts(new String[] { "Model" });
vectorRasterizationOptions.setAutomaticLayoutsScaling(false);
vectorRasterizationOptions.setNoScaling(true);
vectorRasterizationOptions.setBackgroundColor(Color.getBlack());
vectorRasterizationOptions.setDrawType(CadDrawTypeMode.UseObjectColor);
```

## 步驟 6：設定向量光柵化選項

為匯出設定向量光柵化選項。

```java
exportOptions.setVectorRasterizationOptions(vectorRasterizationOptions);
```

## 步驟 7：將 DWG 匯出為 PDF

最後，呼叫 `save` 方法將 DWG 匯出為 PDF。

```java
cadImage.save(outPath, exportOptions);
```

## 常見問題與解決方案

| 問題 | 原因 | 解決方案 |
|-------|-------|----------|
| **未出現 DGN 底圖** | DWG 中未包含 `DGNUNDERLAY` 實體。 | 確認來源 DWG 包含 DGN 參考。 |
| **PDF 為空白** | 光柵化選項設定為零尺寸或版面配置錯誤。 | 確保 `setPageWidth`/`setPageHeight` 為正值，且 `setLayouts` 與 DWG 版面名稱相符。 |
| **授權例外** | 未使用有效的 Aspose.CAD 授權執行。 | 在呼叫任何 API 方法前先套用臨時或正式授權。 |

## 常見問答

### Q1：在哪裡可以找到 Aspose.CAD for Java 的文件？
A1：文件可於 [此處](https://reference.aspose.com/cad/java/) 找到。

### Q2：如何下載 Aspose.CAD for Java 函式庫？
A2：您可從 [此連結](https://releases.aspose.com/cad/java/) 下載函式庫。

### Q3：Aspose.CAD for Java 是否提供免費試用？
A3：有，您可於 [此處](https://releases.aspose.com/) 取得免費試用。

### Q4：在哪裡可以取得 Aspose.CAD for Java 的臨時授權？
A4：可於 [此處](https://purchase.aspose.com/temporary-license/) 取得臨時授權。

### Q5：需要協助或有任何問題？
A5：請前往 Aspose.CAD 社群支援論壇 [此處](https://forum.aspose.com/c/cad/19)。

### Q6：我可以將產生的 PDF 轉回 DWG 嗎？
A6：PDF 只是光柵化預覽，若要轉回 DWG 需要使用其他逆向工程工具。

### Q7：此方法是否適用於其他 CAD 格式，如 DWF 或 DXF？
A7：是的，Aspose.CAD 支援多種格式；只需相應調整檔案副檔名與光柵化設定即可。

**最後更新：** 2026-01-10  
**測試環境：** Aspose.CAD for Java 24.11  
**作者：** Aspose  

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}