---
date: 2026-02-12
description: 學習如何在使用 Aspose.CAD for Java 將 CAD 轉換為 PDF 時設定 PDF 頁面大小。請依照此一步一步的指南啟用追蹤、將
  CAD 轉換為 PDF，並高效地將 CAD 儲存為 PDF。
linktitle: Set PDF Page Size – Enable Tracking for CAD Rendering
second_title: Aspose.CAD Java API
title: 如何設定 PDF 頁面大小並啟用 CAD 渲染流程的追蹤
url: /zh-hant/java/advanced-cad-features/enable-tracking-for-cad-rendering-process/
weight: 10
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# 啟用 CAD 渲染流程的追蹤

## 簡介

在本教學中，您將學會在使用 **Aspose.CAD for Java** **將 CAD 轉換為 PDF** 時 **設定 PDF 頁面大小**。啟用追蹤可讓您完整掌握渲染管線，讓除錯與優化 CAD 檔案（例如 DXF）轉 PDF 的過程變得更簡單。無論您是需要 **將 CAD 儲存為 PDF**、從 DXF 產生 PDF，或僅是控制輸出尺寸，以下步驟都會帶您完成整個流程。

## 快速解答
- **「設定 PDF 頁面大小」的作用是什麼？** 它在 CAD 渲染過程中定義最終 PDF 頁面的寬度與高度。  
- **為什麼要啟用追蹤？** 追蹤會記錄轉換的每個階段，協助您發現效能瓶頸或錯誤。  
- **我需要授權嗎？** 免費試用可用於評估；正式環境需購買商業授權。  
- **支援哪些 CAD 格式？** 包括 DWG、DXF、DGN 等多種格式——完整列表請參閱 Aspose.CAD 文件。  
- **可以即時變更頁面尺寸嗎？** 可以——只要在 `CadRasterizationOptions` 中調整 `PageWidth` 與 `PageHeight` 即可。  

## 什麼是 CAD 渲染中的「設定 PDF 頁面大小」？

設定 PDF 頁面大小告訴光柵化器在將向量 CAD 資料光柵化成 PDF 頁面時，畫布應該有多大。這對於維持視覺忠實度至關重要，尤其是在處理細部工程圖時。

## 為什麼要為 CAD 渲染啟用追蹤？

啟用追蹤會提供每個步驟的詳細日誌——從載入來源檔案到寫入 PDF 輸出。它能協助您：

- 診斷特定圖紙為何渲染不正確。  
- 測量每個階段所花費的時間，對效能調校很有幫助。  
- 驗證您設定的頁面大小是否真的被套用。  

## 先決條件

在設定追蹤之前，請確保您具備以下條件：

1. **Java 開發環境** – 在您的機器上已安裝 Java 8 或更新版本。  
2. **Aspose.CAD 程式庫** – 下載並整合 Aspose.CAD 程式庫至您的 Java 專案。下載連結請見 [here](https://releases.aspose.com/cad/java/)。  
3. **文件目錄** – 準備一個目錄，用於存放 CAD 檔案與產生的 PDF。  

## 匯入命名空間

在您的 Java 專案中，匯入必要的命名空間以使用 Aspose.CAD 功能。請在程式碼開頭加入以下程式碼：

```java
import java.io.FileNotFoundException;
import java.io.FileOutputStream;
import java.io.OutputStream;

import com.aspose.cad.Image;

import com.aspose.cad.imageoptions.CadRasterizationOptions;
import com.aspose.cad.imageoptions.PdfOptions;
```

## 設定資源目錄路徑

將 `"Your Document Directory"` 替換為實際的文件目錄路徑。

```java
String dataDir = "Your Document Directory" + "CADConversion/";
```

## 載入 CAD 檔案

指定 CAD 檔案的路徑，確保它位於先前設定的文件目錄內。

```java
String srcFile = dataDir + "conic_pyramid.dxf";
Image image = Image.load(srcFile);
```

## 設定 PDF 輸出選項

建立輸出串流並設定 PDF 轉換的相關選項。

```java
OutputStream stream = new FileOutputStream(dataDir + "conic_pyramid.pdf");
PdfOptions pdfOptions = new PdfOptions();
```

## 設定 CadRasterizationOptions（設定 PDF 頁面大小）

此處我們透過定義 `PageWidth` 與 `PageHeight` **設定 PDF 頁面大小**。請依照您的工程圖需求調整這些數值。這是回答 **如何在 java cad to pdf 時設定 PDF 大小** 的核心步驟。

```java
CadRasterizationOptions cadRasterizationOptions = new CadRasterizationOptions();
pdfOptions.setVectorRasterizationOptions(cadRasterizationOptions);
cadRasterizationOptions.setPageWidth(800);
cadRasterizationOptions.setPageHeight(600);
```

## 儲存 PDF 檔案

使用先前設定的選項將渲染好的 PDF 檔案儲存。

```java
image.save(stream, pdfOptions);
```

## 驗證追蹤已啟用

確認追蹤已成功於 CAD 渲染流程中啟用。

```java
System.out.println("Tracking enabled successfully for CAD rendering process.");
```

## 常見問題與疑難排解

| 症狀 | 可能原因 | 解決方法 |
|---------|--------------|-----|
| PDF 頁面顯示空白 | `PageWidth`/`PageHeight` 設為 0 | 請確保提供非零的尺寸。 |
| 輸出檔案損毀 | 輸出串流未關閉 | 在 `image.save(...)` 後呼叫 `stream.close()`。 |
| PDF 中缺少圖層 | CAD 檔案使用不受支援的實體 | 確認該檔案格式已被 Aspose.CAD 完全支援。 |

## 常見問答

### Q1：Aspose.CAD 是否相容所有 CAD 檔案格式？

A1：Aspose.CAD 支援多種 CAD 格式，包括 DWG、DXF、DGN 等。完整列表請參考 [documentation](https://reference.aspose.com/cad/java/)。

### Q2：我可以自訂 PDF 檔案的輸出尺寸嗎？

A2：當然可以！在 `CadRasterizationOptions` 中調整 `PageWidth` 與 `PageHeight` 參數，即可自訂輸出尺寸。

### Q3：Aspose.CAD for Java 是否提供免費試用？

A3：是的，您可透過此處的免費試用 [here](https://releases.aspose.com/) 來體驗 Aspose.CAD 的功能。

### Q4：我該如何取得 Aspose.CAD 相關問題的社群支援？

A4：請前往 [Aspose.CAD forum](https://forum.aspose.com/c/cad/19) 與社群互動並尋求協助。

### Q5：Aspose.CAD 是否提供臨時授權？

A5：是的，若需要臨時授權，可於此處取得 [here](https://purchase.aspose.com/temporary-license/)。

## 結論

恭喜！您已學會如何 **設定 PDF 頁面大小** 並在使用 **Aspose.CAD for Java** 進行 CAD 渲染時啟用追蹤。此指南讓您能 **將 CAD 轉換為 PDF**、**將 CAD 儲存為 PDF**，以及從 DXF 產生 PDF，並完整掌控頁面尺寸與詳細執行日誌。歡迎自行嘗試不同的頁面大小，並探索其他光柵化選項，以符合您的特定工程工作流程。

---

**最後更新:** 2026-02-12  
**測試環境:** Aspose.CAD for Java 24.12 (latest at time of writing)  
**作者:** Aspose  

---

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}