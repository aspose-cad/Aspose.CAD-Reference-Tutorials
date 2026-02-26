---
date: 2026-01-10
description: 學習如何使用 Aspose.CAD for Java 從 DGN 檔案建立 JPEG。此逐步教學示範如何有效地將 DGN 轉換為 JPEG。
linktitle: Exporting DGN in AutoCAD Format to Raster Image Format
second_title: Aspose.CAD Java API
title: 如何使用 Aspose.CAD for Java 從 DGN 生成 JPEG
url: /zh-hant/java/dgn-export-options/exporting-dgn-to-raster-image/
weight: 13
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# 使用 Aspose.CAD for Java 從 DGN 建立 JPEG

## 介紹

在本完整指南中，您只需幾行 Java 程式碼即可 **從 DGN 建立 JPEG**。無論是打造批次轉換工具，或是需要將 CAD 圖面以網頁友善的影像方式顯示，將 DGN 轉換為 JPEG 是許多工程與設計工作流程的常見需求。我們將一步步說明——從設定 Aspose.CAD 函式庫到儲存最終的點陣圖——讓您立即將此解決方案整合至自己的應用程式中。

## 快速回答
- **需要的程式庫是什麼？** Aspose.CAD for Java  
- **我可以將其他 CAD 格式轉換為 JPEG 嗎？** 可以，Aspose.CAD 支援多種格式（請參考次要關鍵字 *convert cad to jpeg*）  
- **生產環境需要授權嗎？** 非試用版使用需購買商業授權  
- **支援的 Java 版本為何？** Java 8 或更新版本  
- **一般轉換需要多長時間？** 標準尺寸圖面通常在一秒內完成  

## “從 DGN 建立 JPEG” 是什麼？

從 DGN 檔案建立 JPEG 意指將向量式的 DGN 圖面光柵化為像素式的 JPEG 影像。此過程在保留視覺忠實度的同時，產生可在瀏覽器、電子郵件或報告中直接顯示的輕量檔案，無需 CAD 軟體。

## 為什麼要將 DGN 轉換為 JPEG？

- **易於分享：** JPEG 可在任何裝置上通用檢視。  
- **效能提升：** 點陣圖在網頁載入速度快於向量 CAD 檔案。  
- **相容性：** 許多下游工具（例如報表引擎）僅接受點陣格式。  

## 前置條件

在開始之前，請確保您具備以下項目：

1. **Aspose.CAD 程式庫** – 從官方網站 **[此處](https://releases.aspose.com/cad/java/)** 下載。  
2. **Java Development Kit (JDK)** – 已安裝 Java 8 或更新版本。  
3. **IDE** – 任意支援 Java 的開發環境，如 IntelliJ IDEA 或 Eclipse。  

## 匯入套件

將必要的匯入語句加入您的 Java 類別：

```java
import java.io.FileNotFoundException;
import java.io.FileOutputStream;
import java.io.OutputStream;
import com.aspose.cad.Image;
import com.aspose.cad.ImageOptionsBase;
import com.aspose.cad.fileformats.dgn.DgnImage;
import com.aspose.cad.imageoptions.CadRasterizationOptions;
import com.aspose.cad.imageoptions.JpegOptions;
```

## 步驟說明

### 步驟 1：載入 DGN 檔案

```java
String dataDir = "Your Document Directory" + "ExportingDGN/";
DgnImage dgnImage = (DgnImage) Image.load(dataDir + "Nikon_D90_Camera.dgn");
```

*說明：* `Image.load` 方法會讀取來源 DGN 檔案，並回傳可供後續光柵化的 `DgnImage` 物件。

### 步驟 2：建立 JpegOptions 物件

```java
ImageOptionsBase options = new JpegOptions();
```

*說明：* `JpegOptions` 告訴 Aspose.CAD 輸出格式為 JPEG，亦可在此附加光柵化設定。

### 步驟 3：設定光柵化參數

```java
CadRasterizationOptions vectorOptions = new CadRasterizationOptions();
vectorOptions.setPageWidth(600);
vectorOptions.setPageHeight(400);
vectorOptions.setNoScaling(true);
vectorOptions.setAutomaticLayoutsScaling(false);
options.setVectorRasterizationOptions(vectorOptions);
```

*說明：* 這些選項定義最終影像的尺寸與縮放行為。請依目標解析度調整 `PageWidth` 與 `PageHeight`。

### 步驟 4：儲存轉換後的影像

```java
OutputStream outStream = new FileOutputStream(dataDir + "ExportDGNToRasterImage_Out.jpg");
dgnImage.save(outStream, options);
```

*說明：* `save` 方法會將光柵化後的 JPEG 寫入指定的輸出串流。完成此步驟後，即可取得可直接使用的 JPEG 檔案。

> **專業提示：** 將轉換程式碼包在 try‑with‑resources 區塊中，以確保串流自動關閉。

## 常見使用情境

- **產生縮圖** 供 CAD 檔案瀏覽器使用。  
- **將圖面嵌入** PDF 報告或 HTML 頁面。  
- **自動化批次處理** 設計檔案庫。  

## 疑難排解與常見陷阱

| 問題 | 原因 | 解決方式 |
|------|------|----------|
| 輸出影像全白或空白 | 光柵化參數不正確（例如 `NoScaling` 為 true 且頁面尺寸不匹配） | 調整 `PageWidth`/`PageHeight` 或將 `NoScaling` 設為 false |
| 大型 DGN 檔案記憶體不足 | 未使用串流直接載入過大檔案 | 增加 JVM 堆積大小 (`-Xmx`) 或將檔案分段處理 |
| JPEG 品質不佳 | 預設 JPEG 品質偏低 | 在儲存前使用 `((JpegOptions)options).setQuality(100);` 來提升品質 |

## 常見問題

### Q1：我可以在 Java 中使用 Aspose.CAD 處理其他 CAD 檔案格式嗎？

A1：可以，Aspose.CAD 支援多種格式，讓您 **convert CAD to JPEG** 以及其他點陣或向量輸出。

### Q2：Aspose.CAD for Java 有提供免費試用嗎？

A2：有，您可前往 **[此處](https://releases.aspose.com/)** 取得免費試用版。

### Q3：在哪裡可以找到 Aspose.CAD for Java 的文件說明？

A3：請參考文件 **[此處](https://reference.aspose.com/cad/java/)**。

### Q4：如何取得 Aspose.CAD for Java 的技術支援？

A4：請造訪支援論壇 **[此處](https://forum.aspose.com/c/cad/19)**。

### Q5：在哪裡可以購買 Aspose.CAD for Java 的授權？

A5：您可在 **[此處](https://purchase.aspose.com/buy)** 購買授權。

## 結論

您現在已學會如何使用 Aspose.CAD for Java **從 DGN 建立 JPEG**。依照上述步驟，您可以輕鬆將 DGN 轉 JPEG 的功能整合至任何 Java 應用程式，無論是桌面工具、Web 服務或自動化工作流程。

---

**最後更新：** 2026-01-10  
**測試環境：** Aspose.CAD for Java 24.11（撰寫時的最新版本）  
**作者：** Aspose  

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}