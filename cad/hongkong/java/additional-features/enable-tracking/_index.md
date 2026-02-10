---
date: 2026-02-10
description: 逐步說明如何使用 Aspose.CAD for Java 在 DWG 檔案中啟用追蹤，並使用自訂錯誤處理程式將 DXF 轉換為 PDF。
linktitle: Enable Tracking in DWG Files Using Java
second_title: Aspose.CAD Java API
title: 如何在 Java 中使用 Aspose.CAD 為 DWG 檔案啟用追蹤功能
url: /zh-hant/java/additional-features/enable-tracking/
weight: 12
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# 如何在 Java 中使用 Aspose.CAD 為 DWG 檔案啟用追蹤

## Introduction

如果您正在從事協同 CAD 專案，了解 **如何啟用追蹤** 在 DWG 工作流程中是個改變遊戲規則的功能。它讓您即時掌握渲染問題，提前捕捉轉換錯誤，並讓所有相關人員保持資訊同步。在本教學中，我們將逐步說明如何使用 Aspose.CAD for Java 啟用追蹤，並示範 **如何將 DXF 轉換為 PDF** 作為同一流程的一部分。完成後，您將擁有一段完整、可投入生產的程式碼片段，透過 **自訂錯誤處理程式 Java** 類別在匯出圖紙時回報錯誤。

## Quick Answers
- **「enable dwg tracking java」的功能是什麼？** 它會啟動 Aspose.CAD 的錯誤處理回呼，使您在匯出時能看到渲染問題。  
- **我需要授權嗎？** 試用版可用於測試；正式環境需購買商業授權。  
- **我也可以將 DXF 轉換為 PDF 嗎？** 可以——與 DWG 相同的 `PdfOptions` 也適用於 DXF，滿足 *java convert dxf pdf* 的情境。  
- **需要哪個 JDK 版本？** Java 8 或更高版本。  
- **在哪裡可以找到更多範例？** 請參閱下方連結的 Aspose.CAD Java 文件。

## How to Enable Tracking in DWG Files Using Aspose.CAD

在 Java 應用程式中啟用 DWG 追蹤意味著附加自訂的渲染處理程式，以捕獲警告、錯誤及其他診斷資訊，於 CAD 檔案光柵化或匯出時取得可見性。此可見性協助開發者除錯轉換流程，並確保交付品質更高。

## Why Use Aspose.CAD for Java?

- **完整的 CAD 支援** – 包含 DWG、DXF、DGN 等。  
- **無外部相依性** – 純 Java 函式庫，適合伺服器端自動化。  
- **內建追蹤** – 透過 `CadRenderHandler` 獲得詳細渲染結果。  
- **簡易 PDF 匯出** – 單行程式碼即可完成轉換，同時保留向量資料。  

## Prerequisites

在開始實作之前，請確保已具備以下前置條件：

- Java Development Kit (JDK)：確保系統已安裝 Java。  
- Aspose.CAD for Java：從 [download link](https://releases.aspose.com/cad/java/) 下載並安裝 Aspose.CAD for Java。  
- Document Directory：準備放置 DWG 檔案的資料夾。  

## Import Namespaces

在 Java 專案中，首先匯入必要的命名空間以使用 Aspose.CAD 功能：

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

## Step 1: Load the DWG File

載入 DWG（或 DXF）檔案至 Java 應用程式。請依實際情況調整檔案路徑：

```java
String dataDir = "Your Document Directory" + "DXFDrawings/";
Image image = Image.load(dataDir + "conic_pyramid.dxf");
```

## Step 2: Configure PDF Export Options (How to Convert DXF to PDF)

設定 PDF 匯出選項，指定 CAD 的向量光柵化設定。此亦示範 *java convert dxf pdf* 功能：

```java
OutputStream stream = new FileOutputStream(dataDir + "output_conic_pyramid.pdf");
PdfOptions pdfOptions = new PdfOptions();
CadRasterizationOptions cadRasterizationOptions = new CadRasterizationOptions();
pdfOptions.setVectorRasterizationOptions(cadRasterizationOptions);
cadRasterizationOptions.setPageWidth(800);
cadRasterizationOptions.setPageHeight(600);
```

## Step 3: Implement Tracking (Custom Error Handler Java)

使用自訂錯誤處理程式類別實作追蹤。此類別會捕獲渲染問題並在主控台顯示：

```java
cadRasterizationOptions.RenderResult = new ErrorHandler();
```

## Step 4: Export to PDF

啟動匯出程序，將 DWG/DXF 檔案轉換為 PDF，並啟用追蹤：

```java
System.out.println("Exporting to pdf format");
image.save(stream, pdfOptions);
```

## Step 5: CadRenderHandler Class

定義 `ErrorHandler` 類別（繼承自 `CadRenderHandler`），以處理渲染結果並輸出追蹤資訊：

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

## Why This Matters

啟用追蹤可為每一步轉換留下清晰的稽核紀錄。這在受規範限制的產業（建築、工程、建設）中特別重要，因為需要提供準確渲染的證明以符合合規稽核。自訂錯誤處理程式亦提供掛鉤，可將問題記錄至監控系統或觸發自動重試。

## Common Issues and Solutions

- **`RenderResult` 上的 `NullPointerException`** – 請確認使用 Aspose.CAD 23.10 以上版本；較舊版本不支援 `RenderResult` API。  
- **找不到檔案** – 請確認 `dataDir` 指向正確資料夾，且檔名完全相符（包括大小寫）。  
- **缺少追蹤輸出** – 請確認自訂的 `ErrorHandler` 已正確指派給 `cadRasterizationOptions.RenderResult`。  

## Frequently Asked Questions

**Q:** 我可以使用 Aspose.CAD for Java 為其他 CAD 檔案格式啟用追蹤嗎？  
A: Aspose.CAD 主要支援 DWG 追蹤。其他格式請參考官方文件。  

**Q:** 我該如何處理 Aspose.CAD for Java 中的其他匯出選項？  
A: 請參閱 [Aspose.CAD Java Documentation](https://reference.aspose.com/cad/java/) 的完整說明。  

**Q:** 是否提供 Aspose.CAD for Java 的試用版？  
A: 有，您可於 [Aspose.CAD Free Trial](https://releases.aspose.com/) 取得。  

**Q:** 我該去哪裡尋求協助或討論 Aspose.CAD for Java 相關問題？  
A: 請前往 [Aspose.CAD forum](https://forum.aspose.com/c/cad/19) 取得社群支援。  

**Q:** 我要如何取得 Aspose.CAD for Java 的臨時授權？  
A: 請依照 [Temporary License](https://purchase.aspose.com/temporary-license/) 所示流程操作。  

## Conclusion

在 Java 中使用 Aspose.CAD 啟用 DWG 追蹤，不僅讓您掌握轉換問題，也能簡化協同設計流程。依照上述步驟，您即可 **啟用追蹤**、將 DXF 轉換為 PDF，並優雅地處理任何渲染問題。

---

**最後更新：** 2026-02-10  
**測試環境：** Aspose.CAD for Java 24.12  
**作者：** Aspose  

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}