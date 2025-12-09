---
date: 2025-12-09
description: 學習如何在 Java 中啟用 DWG 追蹤，並了解如何使用 Aspose.CAD 在 Java 中將 DXF 轉換為 PDF。本分步指南展示了協作
  CAD 專案的完整工作流程。
linktitle: Enable Tracking in DWG Files Using Java
second_title: Aspose.CAD Java API
title: 在 Java 中使用 Aspose.CAD 啟用 DWG 檔案追蹤
url: /zh-hant/java/additional-features/enable-tracking/
weight: 12
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# 在 Java 中使用 Aspose.CAD 為 DWG 檔案啟用追蹤

## 介紹

在現代 CAD 工作流程中，**啟用 dwg 追蹤 java** 對於需要監控變更、提前發現錯誤、並讓所有相關人員保持同步的團隊而言是必不可少的。本教學將逐步說明如何使用 Aspose.CAD for Java 為 DWG 檔案開啟追蹤，同時也會示範如何在匯出過程中 **java 轉換 dxf 為 pdf**。完成後，您將擁有一段可直接執行的程式碼，不僅能完成轉換，還會回報任何渲染問題。

## 快速回答
- **「enable dwg tracking java」的功能是什麼？** 它會啟動 Aspose.CAD 的錯誤回呼機制，讓您在匯出時看到渲染問題。  
- **需要授權嗎？** 試用版可用於測試；正式環境需購買商業授權。  
- **我也可以將 DXF 轉成 PDF 嗎？** 可以——相同的 `PdfOptions` 也適用於 DXF，滿足 *java convert dxf pdf* 的情境。  
- **需要哪個版本的 JDK？** Java 8 或以上。  
- **哪裡可以找到更多範例？** 請參考下方的 Aspose.CAD Java 文件連結。

## 什麼是 enable dwg tracking java？
在 Java 應用程式中啟用 DWG 追蹤，即是掛接自訂的渲染處理程式，以捕捉警告、錯誤及其他診斷資訊，這些資訊會在 CAD 檔案被光柵化或匯出時產生。此可視化機制有助於開發者除錯轉換流程，提升交付品質。

## 為什麼選擇 Aspose.CAD for Java？
- **完整的 CAD 支援** – 包括 DWG、DXF、DGN 等。  
- **無外部相依** – 純 Java 函式庫，適合伺服器端自動化。  
- **內建追蹤功能** – 透過 `CadRenderHandler` 取得詳細渲染結果。  
- **簡易 PDF 匯出** – 單行程式即可完成轉換，同時保留向量資料。

## 前置條件

在開始實作之前，請先確保以下條件已備妥：

- Java Development Kit (JDK)：確認系統已安裝 Java。  
- Aspose.CAD for Java：從 [download link](https://releases.aspose.com/cad/java/) 下載並安裝。  
- 文件目錄：準備好存放 DWG 檔案的資料夾。

## 匯入命名空間

在 Java 專案中，先匯入使用 Aspose.CAD 所需的命名空間：

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

## 步驟 1：載入 DWG 檔案

先將 DWG（或 DXF）檔案載入 Java 應用程式，請依實際路徑調整檔案路徑：

```java
String dataDir = "Your Document Directory" + "DXFDrawings/";
Image image = Image.load(dataDir + "conic_pyramid.dxf");
```

## 步驟 2：設定 PDF 匯出選項

設定 PDF 匯出選項，並指定 CAD 向量光柵化參數，同時示範 *java convert dxf pdf* 的功能：

```java
OutputStream stream = new FileOutputStream(dataDir + "output_conic_pyramid.pdf");
PdfOptions pdfOptions = new PdfOptions();
CadRasterizationOptions cadRasterizationOptions = new CadRasterizationOptions();
pdfOptions.setVectorRasterizationOptions(cadRasterizationOptions);
cadRasterizationOptions.setPageWidth(800);
cadRasterizationOptions.setPageHeight(600);
```

## 步驟 3：實作追蹤

使用自訂錯誤處理類別實作追蹤，此類別會捕捉渲染問題並在主控台顯示：

```java
cadRasterizationOptions.RenderResult = new ErrorHandler();
```

## 步驟 4：匯出為 PDF

啟動匯出程序，將 DWG/DXF 檔案轉換為 PDF，並開啟追蹤功能：

```java
System.out.println("Exporting to pdf format");
image.save(stream, pdfOptions);
```

## 步驟 5：CadRenderHandler 類別

定義 `ErrorHandler` 類別（繼承自 `CadRenderHandler`），用以處理渲染結果並輸出追蹤資訊：

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

## 常見問題與解決方案

- **`NullPointerException` 發生於 `RenderResult`** – 請確認使用 Aspose.CAD 23.10 以上版本；較舊版本未提供 `RenderResult` API。  
- **找不到檔案** – 請檢查 `dataDir` 是否指向正確資料夾，且檔名大小寫完全相符。  
- **沒有產生追蹤輸出** – 請確認自訂的 `ErrorHandler` 已正確指派給 `cadRasterizationOptions.RenderResult`。

## 常見問答

**Q:** 我可以為其他 CAD 檔案格式啟用追蹤嗎？  
**A:** Aspose.CAD 主要支援 DWG 追蹤。其他格式請參考官方文件。

**Q:** 如何在 Aspose.CAD for Java 中處理其他匯出選項？  
**A:** 請參閱 [Aspose.CAD Java Documentation](https://reference.aspose.com/cad/java/) 內的完整說明。

**Q:** 是否提供 Aspose.CAD for Java 的試用版？  
**A:** 有，您可前往 [Aspose.CAD Free Trial](https://releases.aspose.com/) 下載。

**Q:** 若有問題或想討論，該去哪裡尋求協助？  
**A:** 請造訪 [Aspose.CAD forum](https://forum.aspose.com/c/cad/19) 與社群互動。

**Q:** 如何取得 Aspose.CAD for Java 的臨時授權？  
**A:** 請依照 [Temporary License](https://purchase.aspose.com/temporary-license/) 的說明操作。

## 結論

在 Java 中使用 Aspose.CAD 啟用 DWG 追蹤，不僅能讓您即時掌握轉換問題，亦能提升協同設計流程的效率。依照上述步驟，您即可 **enable dwg tracking java**、將 DXF 轉為 PDF，並優雅地處理任何渲染錯誤。

---

**最後更新：** 2025-12-09  
**測試環境：** Aspose.CAD for Java 24.12  
**作者：** Aspose  

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}