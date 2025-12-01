---
date: 2025-12-01
description: 了解如何設定 PDF 頁面大小、將 DWG 轉換為 PDF，並使用 Aspose.CAD for Java 啟用 DWG 變更追蹤。
language: zh-hant
linktitle: Set PDF Page Size and Track DWG with Java
second_title: Aspose.CAD Java API
title: 使用 Aspose.CAD Java 設定 PDF 頁面大小並追蹤 DWG
url: /java/additional-features/enable-tracking/
weight: 12
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# 設定 PDF 頁面尺寸並追蹤 DWG 使用 Aspose.CAD Java

## 簡介

在 CAD 專案協作時，您常常需要 **設定 PDF 頁面尺寸** 以確保版面一致、**將 DWG 轉換為 PDF**，以及追蹤圖紙的每一次變更。Aspose.CAD for Java 讓這一切在單一、流暢的工作流程中得以實現。本教學將逐步說明如何 **設定 PDF 頁面尺寸**、啟用 **DWG 變更追蹤**，並將圖紙匯出為 PDF——全部使用 Java 完成。

## 快速解答
- **我如何設定 PDF 頁面尺寸？** 在匯出前使用 `CadRasterizationOptions.setPageWidth()` 與 `setPageHeight()`。  
- **匯出時可以追蹤變更嗎？** 可以——實作自訂的 `CadRenderHandler` 以取得追蹤結果。  
- **哪個方法可將 DWG 轉換為 PDF？** 在設定好選項後呼叫 `image.save(stream, pdfOptions)`。  
- **主要的先決條件是什麼？** JDK、Aspose.CAD for Java，以及包含 DWG/DXF 檔案的資料夾。  
- **正式環境需要授權嗎？** 需要，非試用部署必須使用有效的 Aspose.CAD 授權。

## 在 DWG 匯出情境中，「設定 PDF 頁面尺寸」是什麼？

設定 PDF 頁面尺寸即決定最終 PDF 畫布的寬高（以像素為單位）。當您希望匯出的圖紙符合特定紙張尺寸或螢幕佈局時，這項設定相當重要，能確保所有元件精確出現在預期位置。

## 為什麼在匯出 DWG 檔案時要啟用追蹤？

追蹤（或變更追蹤）會記錄轉換過程中出現的渲染問題、缺少字型或不支援的實體。取得這些資訊後，您可以：

- 快速找出需在最終交付前修正的問題。  
- 向團隊成員提供明確的變更或遺漏說明。  
- 為受規範限制的產業保留稽核痕跡。

## 先決條件

- **Java Development Kit (JDK)** – 任意近期版本（8 以上）。  
- **Aspose.CAD for Java** – 從官方 [Aspose CAD 下載頁面](https://releases.aspose.com/cad/java/) 取得。  
- **Document Directory** – 放置欲處理的 DWG/DXF 檔案之資料夾。

## 匯入命名空間

先匯入必要的 Aspose.CAD 類別以及標準的 Java I/O 類別。

```java
import com.aspose.cad.Image;

import com.aspose.cad.imageoptions.CadRasterizationOptions;
import com.aspose.cad.imageoptions.CadRenderResult;
import com.aspose.cad.imageoptions.PdfOptions;
import com.aspose.cad.imageoptions.RenderResult;
import java.io.FileNotFoundException;
import java.io.FileOutputStream;
import java.io.OutputStream;
```

## 步驟 1：載入 DWG（或 DXF）檔案

將來源圖紙載入 `Image` 物件。請自行調整路徑指向正確的目錄。

```java
String dataDir = "Your Document Directory" + "DXFDrawings/";
Image image = Image.load(dataDir + "conic_pyramid.dxf");
```

## 步驟 2：設定 PDF 匯出選項（包含頁面尺寸）

在此設定 PDF 選項，並明確 **設定 PDF 頁面尺寸** 為 800 × 600 像素。這裡即是主要關鍵字的應用位置。

```java
OutputStream stream = new FileOutputStream(dataDir + "output_conic_pyramid.pdf");
PdfOptions pdfOptions = new PdfOptions();
CadRasterizationOptions cadRasterizationOptions = new CadRasterizationOptions();
pdfOptions.setVectorRasterizationOptions(cadRasterizationOptions);
cadRasterizationOptions.setPageWidth(800);   // set PDF page width
cadRasterizationOptions.setPageHeight(600);  // set PDF page height
```

## 步驟 3：實作追蹤

建立自訂的錯誤處理程式，以在轉換過程中接收追蹤資訊。

```java
cadRasterizationOptions.RenderResult = new ErrorHandler();
```

## 步驟 4：匯出為 PDF

在完成選項與追蹤處理程式的設定後，將圖紙匯出。此步驟 **將 DWG 轉換為 PDF**（在本例中亦可將 DXF 轉換為 PDF）。

```java
System.out.println("Exporting to pdf format");
image.save(stream, pdfOptions);
```

## 步驟 5：CadRenderHandler 類別 – 捕獲追蹤結果

`ErrorHandler` 類別繼承自 `CadRenderHandler`，並在 **追蹤 DWG 變更** 時列印任何渲染問題。

```java
public static class ErrorHandler extends CadRasterizationOptions.CadRenderHandler {
    @Override
    public void invoke(CadRenderResult result) {
        System.out.println("Tracking results of exporting");

        if (result.isRenderComplete())
            return;

        System.out.println("Have some problems:");

        int idxError = 1;
        for (RenderResult rr : result.getFailures()) {
            System.out.printf("{0}. {1}, {2}", idxError, rr.getRenderCode(), rr.getMessage());
            idxError++;
        }
    }
}
```

## 常見問題與解決方法

| 問題 | 為何會發生 | 解決方式 |
|------|------------|----------|
| **缺少字型** | CAD 檔案引用了伺服器上未安裝的字型。 | 安裝所需字型或將字型嵌入原始圖紙。 |
| **不支援的實體** | 某些 DWG 實體尚未被 Aspose.CAD 支援。 | 使用追蹤輸出找出這些實體，並簡化圖紙。 |
| **頁面尺寸不正確** | 匯出前未呼叫 `setPageWidth/Height`。 | 如上例所示，確保在 `CadRasterizationOptions` 中設定頁面尺寸。 |

## 常見問答

### Q1: 我可以為其他 CAD 檔案格式啟用追蹤嗎？

A1: Aspose.CAD 主要支援 DWG/DXF 檔案的追蹤。其他格式請參考官方文件，了解可用功能。

### Q2: 如何在 Aspose.CAD for Java 中處理其他匯出選項？

A2: 此函式庫提供 DPI、背景色、向量光柵化等多項選項。可於 [Aspose.CAD Java 文件](https://reference.aspose.com/cad/java/) 中深入探索。

### Q3: 是否有 Aspose.CAD for Java 的試用版？

A3: 有，您可從 [Aspose.CAD 免費試用](https://releases.aspose.com/) 下載。

### Q4: 哪裡可以取得支援或討論 Aspose.CAD for Java 的相關問題？

A4: 可前往 [Aspose.CAD 論壇](https://forum.aspose.com/c/cad/19) 提問與交流。

### Q5: 如何取得 Aspose.CAD for Java 的臨時授權？

A5: 請依照 [臨時授權](https://purchase.aspose.com/temporary-license/) 頁面說明，申請限時評估授權。

### Q6: 我能在保留圖層的同時 **將 DWG 轉換為 PDF** 嗎？

A6: 可以。透過設定 `CadRasterizationOptions`，即可在產生的 PDF 中保留圖層資訊。

### Q7: 使用自訂頁面尺寸 **匯出 DWG 為 PDF** 的最佳做法是什麼？

A7: 在呼叫 `image.save()` 前，使用 `setPageWidth` 與 `setPageHeight` 設定所需寬高——如步驟 2 所示。

## 結論

依循上述步驟，您即可 **設定 PDF 頁面尺寸**、**將 DWG 轉換為 PDF**，並 **追蹤 DWG 檔案的變更**，全部透過 Aspose.CAD for Java 完成。此工作流程讓您完整掌控輸出版面，同時提供寶貴的診斷資訊，確保 CAD 協作順暢且無錯。歡迎探索更多渲染選項，並將此程式碼整合至更大型的自動化流程中。

---

**Last Updated:** 2025-12-01  
**Tested With:** Aspose.CAD for Java 24.12 (latest at time of writing)  
**Author:** Aspose  

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}