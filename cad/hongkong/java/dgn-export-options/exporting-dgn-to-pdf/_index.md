---
date: 2026-05-04
description: 學習如何使用 Aspose.CAD for Java，將 DGN 匯出為 AutoCAD PDF，以轉換 CAD PDF 檔案。提供可自訂
  PDF 大小與選項的逐步指南。
keywords:
- convert cad pdf
- how to export dgn
- customize pdf size
- aspose cad download
- set pdf options
linktitle: 將 DGN（AutoCAD 格式）匯出為 PDF
second_title: Aspose.CAD Java API
title: 轉換 CAD PDF – 使用 Aspose.CAD for Java 輕鬆將 DGN 匯出為 AutoCAD PDF
url: /zh-hant/java/dgn-export-options/exporting-dgn-to-pdf/
weight: 12
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# 轉換 CAD PDF：使用 Aspose.CAD for Java 輕鬆將 DGN 匯出為 AutoCAD PDF

## 介紹

如果您需要直接從 DGN 來源 **convert CAD PDF** 檔案，就來對地方了。在本教學中，我們將示範如何使用 Aspose.CAD for Java 將 DGN 檔案匯出為相容於 AutoCAD 的 PDF。您將看到如何設定自訂頁面尺寸、挑選特定版面配置，並微調 PDF 輸出——全部以清晰的逐步程式碼呈現，您可以直接套用到自己的專案中。

## 快速解答
- **「convert CAD PDF」是什麼意思？** 它指的是將 CAD 原始檔案（如 DGN）轉換成保留向量資料與版面忠實度的 PDF。  
- **哪個函式庫負責轉換？** Aspose.CAD for Java 提供可靠且免授權費的試用版來完成此任務。  
- **開發時需要授權嗎？** 免費試用可用於測試；正式上線則需購買商業授權。  
- **可以自訂 PDF 大小嗎？** 可以 – `CadRasterizationOptions` 允許設定頁面寬度、高度與縮放比例。  
- **需要多少行程式碼？** 不到 20 行 Java 程式碼即可載入、設定並儲存 PDF。

## 什麼是「convert CAD PDF」？
將 CAD PDF 轉換指的是將原生 CAD 繪圖（例如 DGN）產生一個保留原始向量圖形、圖層與版面資訊的 PDF。產出的 PDF 可在任何裝置上檢視，無需 CAD 軟體，非常適合分享、列印或存檔。

## 為什麼使用 Aspose.CAD for Java 來轉換 CAD PDF？
- **完整格式支援** – 支援 DGN、DWG、DXF 等多種格式。  
- **無外部相依性** – 純 Java 實作，無需本機 DLL。  
- **細緻控制** – 可選擇要匯出的版面、設定自訂頁面大小，並控制光柵化品質。  
- **適合批次作業** – 在迴圈中載入與儲存大量檔案，開銷極低。

## 前置條件
在開始之前，請確保您已具備以下項目：

- **Aspose.CAD Library** – 前往 [here](https://releases.aspose.com/cad/java/) 下載。  
- **Document Directory** – 您機器上的資料夾，用於存放輸入的 DGN 檔案與輸出的 PDF。

## 匯入套件

在您的 Java 專案中，匯入存取 Aspose.CAD 功能所需的套件：

```java
import java.io.FileNotFoundException;
import java.io.FileOutputStream;
import java.io.OutputStream;
import com.aspose.cad.Image;
import com.aspose.cad.fileformats.dgn.DgnImage;
import com.aspose.cad.imageoptions.CadRasterizationOptions;
import com.aspose.cad.imageoptions.PdfOptions;
```

接下來，我們將範例程式碼分解為多個步驟：

## 步驟 1：定義檔案路徑（如何匯出 dgn）

```java
String dataDir = "Your Document Directory" + "ExportingDGN/";
String fileName = dataDir + "Nikon_D90_Camera.dgn";
String outFile  = dataDir + "Nikon_D90_Camera.pdf";
```

請務必將 `"Your Document Directory"` 替換為實際存放檔案的路徑。

## 步驟 2：載入 DGN 圖像

```java
DgnImage objImage = (DgnImage) Image.load(fileName);
```

使用 Aspose.CAD 載入 DGN 檔案。

## 步驟 3：設定 PDF 匯出選項（自訂 pdf 大小、設定 pdf 選項）

```java
PdfOptions options = new PdfOptions();
CadRasterizationOptions vectorOptions = new CadRasterizationOptions();
vectorOptions.setPageWidth(1500);
vectorOptions.setPageHeight(1500);
vectorOptions.setAutomaticLayoutsScaling(true);
vectorOptions.setLayouts(new String[] { "1", "2", "3", "9" }); // Export specific views
options.setVectorRasterizationOptions(vectorOptions);
```

此處定義 PDF 匯出選項，包括頁面尺寸、自動縮放，以及您希望最終 PDF 包含的特定 DGN 版面（視圖）。

## 步驟 4：儲存 PDF 檔案

```java
objImage.save(outFile, options);
```

儲存匯出的 PDF 檔案。`save` 方法會套用前一步所設定的所有選項。

重複上述步驟即可轉換其他 DGN 檔案。恭喜！您已成功透過 Aspose.CAD for Java 將 DGN 檔案匯出為 AutoCAD 格式的 PDF，完成 **convert CAD PDF**。

## 常見問題與解決方案
| 問題 | 發生原因 | 解決方法 |
|-------|----------------|-----|
| **找不到檔案** | `dataDir` 路徑不正確 | 再次確認資料夾路徑，並確保 DGN 檔案存在。 |
| **PDF 空白頁** | `AutomaticLayoutsScaling` 設為 `false` 或缺少版面配置 ID | 保留 `setAutomaticLayoutsScaling(true)` 並驗證版面名稱 (`"1","2",…`). |
| **低解析度輸出** | 預設光柵化 DPI 較低 | 使用 `vectorOptions.setResolution(300);` 提高品質（在 `setVectorRasterizationOptions` 之前加入）。 |
| **授權例外** | 在生產環境中未使用有效授權執行 | 依照 Aspose 文件說明套用臨時或購買的授權。 |

## 常見問題（其他）

**Q: 我可以只匯出多版面 DGN 檔案中的單一版面嗎？**  
A: 可以 – 在 `vectorOptions.setLayouts(new String[] { "2" });` 中指定欲匯出的版面 ID。

**Q: 能否在產生的 PDF 中嵌入字型？**  
A: Aspose.CAD 會在向量資料光柵化時自動嵌入必要字型；如有需要，也可透過 `PdfOptions` 控制字型嵌入。

**Q: 如何批次處理大量 DGN 檔案？**  
A: 將上述步驟包在 `for` 迴圈中，遍歷檔名清單，對每次迭代重複使用相同的 `PdfOptions` 實例。

**Q: 函式庫是否支援受密碼保護的 PDF？**  
A: 支援 – 可在 `PdfOptions` 物件上使用 `options.setPassword("yourPassword");` 設定密碼。

**Q: 哪裡可以找到更多範例？**  
A: 官方 Aspose.CAD 文件與範例倉庫提供許多其他情境範例。

## 常見問題（原始）

### Q1: Aspose.CAD 是否相容所有 CAD 檔案格式？

A1: 是的，Aspose.CAD 支援廣泛的 CAD 格式，確保在處理各種檔案類型時具備彈性。

### Q2: 我可以自訂 PDF 匯出設定嗎？

A2: 當然可以。如本教學所示，您可以調整頁面尺寸與版面等選項，以符合需求。

### Q3: 我可以在哪裡取得額外支援或協助？

A3: 前往 [Aspose.CAD forum](https://forum.aspose.com/c/cad/19) 取得社群支援與討論。

### Q4: 有免費試用版嗎？

A4: 有，您可在 [here](https://releases.aspose.com/) 取得免費試用。

### Q5: 如何取得臨時授權？

A5: 前往 [here](https://purchase.aspose.com/temporary-license/) 取得臨時授權。

## 結論

在本教學中，我們探討了如何使用 Aspose.CAD for Java **convert CAD PDF**。只需幾行程式碼，即可載入 DGN 繪圖、微調 PDF 匯出選項，並產生高品質的 PDF，適合分享或存檔。歡迎嘗試不同的頁面大小、版面或批次處理，以符合您的專案需求。

---

**最後更新:** 2026-05-04  
**測試環境:** Aspose.CAD for Java 24.12  
**作者:** Aspose  

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}