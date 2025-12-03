---
date: 2025-12-03
description: 學習如何在將 DWG 轉換為 PDF 時設定 PDF 頁面尺寸，並使用 Aspose.CAD for Java 在 DWG 檔案中啟用追蹤功能——完整指南，精準匯出
  CAD 圖紙為 PDF。
language: zh-hant
linktitle: Set PDF Page Size and Enable Tracking in DWG Files Using Java
second_title: Aspose.CAD Java API
title: 使用 Aspose.CAD (Java) 設定 PDF 頁面大小並在 DWG 檔案中啟用追蹤
url: /java/additional-features/enable-tracking/
weight: 12
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# 在 Java 中使用 Aspose.CAD 設定 PDF 頁面大小並啟用 DWG 檔案追蹤

## 介紹

如果您在*將 DWG 轉換為 PDF*時需要**設定 PDF 頁面大小**，同時想追蹤任何渲染問題，Aspose.CAD for Java 提供了一個乾淨且可程式化的方式一次完成。本文將逐步說明如何設定頁面尺寸、啟用追蹤，並從 Java 匯出 CAD 繪圖 PDF。完成後，您將了解為何正確的頁面大小對 CAD 繪圖很重要，以及如何在匯出過程中取得詳細的追蹤資訊。

## 快速解答
- **「設定 PDF 頁面大小」會影響什麼？** 它決定最終 PDF 畫布的寬度與高度，確保您的圖紙完整呈現。  
- **使用此功能需要授權嗎？** 試用版可用於測試；正式環境需購買商業授權。  
- **需要哪個版本的 Aspose.CAD？** 任何支援 `CadRasterizationOptions` 的近期版本皆可。  
- **可以套用於其他 CAD 格式嗎？** 範例以 DWG/DXF 為例，相同做法亦適用於大多數支援的格式。  
- **轉換需要多長時間？** 一般檔案在一秒以內完成；較大的圖紙可能需要更久。

## 在 CAD 匯出情境下，「設定 PDF 頁面大小」是什麼意思？
設定 PDF 頁面大小即告訴渲染器輸出畫布的精確尺寸（以像素或點為單位）。對於必須保留比例與版面配置的技術圖紙而言，這點尤為重要。若未明確設定頁面大小，PDF 可能會使用預設尺寸，導致圖紙被裁切或變形。

## 為何在匯出 CAD 圖紙時要設定 PDF 頁面大小？
- **保留比例** – 工程師依賴真實比例的列印。  
- **符合紙張** – 可選擇 A4、Letter 或自訂尺寸，以符合專案規範。  
- **提升可讀性** – 較大的頁面能在不放大的情況下顯示細節。  
- **輸出一致** – 自動化流程每次產生的 PDF 都具有相同尺寸。

## 如何在將 DWG 轉換為 PDF 時設定 PDF 頁面大小？
以下示範在匯出前以自訂寬度與高度設定 `CadRasterizationOptions`。此步驟直接回應關鍵字 **設定 PDF 頁面大小**。

## 前置條件

- **Java Development Kit (JDK)** – 已安裝 Java 8 或更新版本。  
- **Aspose.CAD for Java** – 從官方 [Aspose CAD 下載頁面](https://releases.aspose.com/cad/java/) 取得。  
- **文件目錄** – 放置欲處理的 DWG/DXF 檔案的資料夾。

## 匯入命名空間

首先匯入所需的類別。程式碼區塊保持原樣。

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

## 步驟 1：載入 DWG/DXF 檔案

載入來源圖紙。請自行調整路徑指向您的檔案。

```java
String dataDir = "Your Document Directory" + "DXFDrawings/";
Image image = Image.load(dataDir + "conic_pyramid.dxf");
```

## 步驟 2：設定 PDF 匯出選項（含頁面大小）

在此設定頁面寬度與高度——這就是 **設定 PDF 頁面大小** 的地方。數值以像素為單位，您也可以自行從英吋或毫米換算。

```java
OutputStream stream = new FileOutputStream(dataDir + "output_conic_pyramid.pdf");
PdfOptions pdfOptions = new PdfOptions();
CadRasterizationOptions cadRasterizationOptions = new CadRasterizationOptions();
pdfOptions.setVectorRasterizationOptions(cadRasterizationOptions);
cadRasterizationOptions.setPageWidth(800);   // <-- custom width
cadRasterizationOptions.setPageHeight(600);  // <-- custom height
```

> **小技巧：** 若您偏好標準紙張尺寸，可使用換算式 `1 英吋 = 72 點`。以 A4 紙（8.27 × 11.69 英吋）為例，設定 `pageWidth = 595`、`pageHeight = 842`。

## 步驟 3：實作追蹤

追蹤會捕捉任何渲染問題。我們會掛接一個自訂處理程式，在匯出完成後被呼叫。

```java
cadRasterizationOptions.RenderResult = new ErrorHandler();
```

## 步驟 4：匯出為 PDF

執行轉換。PDF 會依您指定的尺寸產生，且追蹤資訊會印出至主控台。

```java
System.out.println("Exporting to pdf format");
image.save(stream, pdfOptions);
```

## 步驟 5：CadRenderHandler 類別

此處理程式會列印在渲染過程中發生的任何失敗，協助您在**匯出 CAD 圖紙 PDF**時除錯。

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

| 問題 | 原因 | 解決方式 |
|------|------|----------|
| **PDF 為空白** | 頁面大小設定為 0 或過小 | 確認 `setPageWidth` 與 `setPageHeight` 為正值。 |
| **缺少圖形** | 由處理程式捕捉到的渲染錯誤 | 查看 `ErrorHandler` 在主控台的輸出，針對特定 `RenderCode` 進行修正。 |
| **找不到檔案** | `dataDir` 路徑不正確 | 使用絕對路徑或確保目錄已存在。 |
| **授權例外** | 使用試用版且未為大型檔案設定有效授權 | 在載入影像前套用您的 Aspose.CAD 授權。 |

## 常見問答

**Q：我可以在 Aspose.CAD for Java 中為其他 CAD 檔案格式啟用追蹤嗎？**  
A：Aspose.CAD 主要在 DWG/DXF 上提供追蹤支援。其他格式請參考官方文件。

**Q：如何在 Aspose.CAD for Java 中處理其他匯出選項？**  
A：此函式庫提供多種選項，如 DPI、背景色、向量光柵化等。詳情請見 [Aspose.CAD Java 文件](https://reference.aspose.com/cad/java/)。

**Q：Aspose.CAD for Java 有提供試用版嗎？**  
A：有，您可從 [Aspose.CAD 免費試用](https://releases.aspose.com/) 下載。

**Q：我可以到哪裡取得 Aspose.CAD for Java 的支援或討論區？**  
A：請前往 [Aspose.CAD 論壇](https://forum.aspose.com/c/cad/19) 取得社群支援與官方回覆。

**Q：如何取得 Aspose.CAD for Java 的臨時授權？**  
A：請依照 [臨時授權](https://purchase.aspose.com/temporary-license/) 頁面上的說明操作。

---

**最後更新：** 2025-12-03  
**測試環境：** Aspose.CAD for Java 24.11（撰寫時最新版本）  
**作者：** Aspose  

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}