---
date: 2026-06-19
description: 了解如何使用 Aspose.CAD for Java 在儲存 CAD 圖紙時設定逾時。提升效能、避免卡頓，並有效率地將 CAD 匯出為 PDF。
keywords:
- how to set timeout
- convert dwg to pdf
- export cad to pdf
linktitle: 設定儲存逾時
schemas:
- author: Aspose
  dateModified: '2026-06-19'
  description: Learn how to set timeout on saving CAD drawings with Aspose.CAD for
    Java. Boost performance, avoid hangs, and export CAD to PDF efficiently.
  headline: How to Set Timeout on Save for CAD with Aspose.CAD
  type: TechArticle
- description: Learn how to set timeout on saving CAD drawings with Aspose.CAD for
    Java. Boost performance, avoid hangs, and export CAD to PDF efficiently.
  name: How to Set Timeout on Save for CAD with Aspose.CAD
  steps:
  - name: Set Source and Output Directories
    text: Ensure you have the correct source and output directories for your CAD drawings.
  - name: Create Interruption Token Source
    text: Initialize an interruption token source to manage interruptions during the
      save operation.
  - name: Load CAD Drawing
    text: The `CadImage` class is Aspose.CAD's core object that represents a CAD drawing
      in memory, offering methods for rendering and conversion.
  - name: Configure Rasterization Options
    text: '`CadRasterizationOptions` specifies how the CAD drawing is rasterized into
      an image. Configure rasterization options for the CAD drawing.'
  - name: Configure PDF Options
    text: '`PdfOptions` defines settings for saving a CAD drawing as a PDF document.
      Set up PDF options with vector rasterization options and the interruption token.'
  - name: Save Drawing with Timeout
    text: Save the CAD drawing to a PDF file with the specified timeout.
  - name: Handle Interruption
    text: '`OperationCanceledException` is thrown when a save operation exceeds the
      specified timeout. Create a thread to handle the save operation and interrupt
      it after a specified timeout.'
  type: HowTo
- questions:
  - answer: Yes, wrap each conversion in its own thread with a separate interruption
      token to enforce per‑file time limits.
    question: Can I use this feature to convert DWG to PDF in a batch job?
  - answer: The timeout mechanism is tied to the `InterruptionTokenSource` and works
      with any format that respects the token, including PDF, PNG, and SVG.
    question: Does the timeout work on all output formats?
  - answer: Aspose.CAD automatically discards incomplete output, so you won’t end
      up with corrupted PDFs.
    question: What happens to partially written files after a timeout?
  - answer: Yes, a valid Aspose.CAD license is required for commercial deployments;
      a free trial is available for evaluation.
    question: Is a license required for production use?
  - answer: The official Aspose.CAD documentation provides additional code snippets
      and best‑practice guidelines.
    question: Where can I find more examples of using interruption tokens?
  type: FAQPage
second_title: Aspose.CAD Java API
title: 如何使用 Aspose.CAD 為 CAD 設定儲存逾時
url: /zh-hant/java/other-cad-operations/put-timeout-on-save/
weight: 15
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# 設定 Aspose.CAD 儲存 CAD 時的逾時

## 介紹

在本完整指南中，您將學習 **如何設定逾時**，在使用 Aspose.CAD for Java 儲存 CAD 圖面時套用逾時機制。設定逾時可防止長時間執行的儲存操作卡住您的應用程式，這在需要 **將 CAD 匯出為 PDF** 或 **將 DWG 轉換為 PDF** 的批次處理情境中特別重要。Aspose.CAD for Java 支援超過 50 種 CAD 格式，且能在不將整個文件載入記憶體的情況下處理數百頁的檔案，為您提供可預測的效能與資源使用。

## 快速解答
- **逾時的作用是什麼？** 它會在指定時間後中止儲存操作，釋放執行緒並防止資源洩漏。  
- **哪個類別控制逾時？** `InterruptionTokenSource` 提供儲存例程使用的取消令牌。  
- **逾時後仍能匯出 CAD 為 PDF 嗎？** 可以 – 您可以捕獲中斷例外並重新嘗試或記錄失敗。  
- **需要特別的授權嗎？** 一般的 Aspose.CAD 授權即可，逾時功能已內建。  
- **此方法是執行緒安全的嗎？** 是的，只要每個儲存操作在各自的執行緒中使用各自的令牌即可。

## CAD 儲存作業中的逾時是什麼？
逾時是一個可設定的時間上限，當超過此上限時，會強制停止儲存程序並拋出中斷例外。這可保護您的 Java 應用程式免於因複雜圖面或 I/O 瓶頸而無限卡住。

## 為何在儲存 CAD 檔案時設定逾時？
Aspose.CAD 能在一般圖面下於一秒內 **將 DWG 轉換為 PDF** 或 **將 CAD 匯出為 PDF**，但極大或損毀的檔案可能需要數分鐘。透過設定逾時，您可保證任何單一儲存不會超過，例如 30 秒，從而維持批次吞吐量穩定，避免執行緒資源耗盡。

## 前置條件

在開始教學之前，請確保您已具備以下前置條件：
- **Aspose.CAD for Java Library** – 確認已將 Aspose.CAD for Java 函式庫整合至您的專案中。您可從 [website](https://releases.aspose.com/cad/java/) 下載函式庫。
- **開發環境** – 設定好 Java 開發環境，並安裝所有必要的工具與相依性。

## 匯入套件

要開始使用，請在 Java 專案中匯入所需的套件。於 Java 檔案的開頭加入以下程式碼：

```java
import com.aspose.cad.Image;
import com.aspose.cad.InterruptionTokenSource;
import com.aspose.cad.fileformats.cad.CadImage;
import com.aspose.cad.imageoptions.CadRasterizationOptions;
import com.aspose.cad.imageoptions.PdfOptions;
import java.util.concurrent.TimeUnit;
```

現在，讓我們將範例程式碼拆解為逐步說明：

## 如何在儲存 CAD 圖面時設定逾時？

載入 CAD 檔案，建立具備所需逾時的 `InterruptionTokenSource`，並將該令牌傳遞給 PDF 儲存選項。若操作超過逾時，Aspose.CAD 會拋出 `OperationCanceledException`，您可以捕獲此例外以優雅地處理失敗。

### 步驟 1：設定來源與輸出目錄

```java
final String SourceDir = Utils.getDataDir_DWGDrawings();
final String OutputDir = Utils.getDataDir_Output();
```

確保您為 CAD 圖面設定了正確的來源與輸出目錄。

### 步驟 2：建立 Interruption Token Source

```java
final InterruptionTokenSource source = new com.aspose.cad.InterruptionTokenSource();
```

初始化一個中斷令牌來源，以在儲存操作期間管理中斷。

### 步驟 3：載入 CAD 圖面

`CadImage` 類別是 Aspose.CAD 的核心物件，代表記憶體中的 CAD 圖面，提供渲染與轉換的方法。

```java
final CadImage cadImageBig = (CadImage)Image.load(SourceDir + "Drawing11.dwg");
```

### 步驟 4：設定光柵化選項

`CadRasterizationOptions` 指定 CAD 圖面如何光柵化為影像。

```java
CadRasterizationOptions rasterizationOptionsBig = new CadRasterizationOptions();
rasterizationOptionsBig.setPageWidth(cadImageBig.getSize().getWidth() / 2);
rasterizationOptionsBig.setPageHeight(cadImageBig.getSize().getHeight() / 2);
```

為 CAD 圖面配置光柵化選項。

### 步驟 5：設定 PDF 選項

`PdfOptions` 定義將 CAD 圖面儲存為 PDF 文件的設定。

```java
final PdfOptions CADfBig = new PdfOptions();
CADfBig.setVectorRasterizationOptions(rasterizationOptionsBig);
CADfBig.setInterruptionToken(source.getToken());
```

使用向量光柵化選項與中斷令牌設定 PDF 選項。

### 步驟 6：使用逾時儲存圖面

```java
cadImageBig.save(OutputDir + "PutTimeoutOnSave_out.pdf", CADfBig);
```

將 CAD 圖面以指定的逾時儲存為 PDF 檔案。

### 步驟 7：處理中斷

`OperationCanceledException` 會在儲存操作超過指定逾時時拋出。

```java
java.lang.Thread thread = new java.lang.Thread(new Runnable() {
    @Override
    public void run() {
        try {
            cadImageBig.save(OutputDir + "PutTimeoutOnSave_out.pdf", CADfBig);
        } catch (Throwable th) {
            System.out.println("interrupted !!!");
        }
    }
});
thread.start();
TimeUnit.SECONDS.sleep(3);
source.interrupt();
thread.join();
```

建立執行緒以處理儲存操作，並在指定的逾時後中斷該執行緒。

## 常見問題與解決方案

- **逾時設定過短** – 若頻繁收到中斷，請增加逾時值以容納較大的圖面。  
- **未捕獲 InterruptedException** – 請務必在儲存呼叫外層使用 `try‑catch` 包住 `OperationCanceledException`，以防止應用程式崩潰。  
- **記憶體消耗** – 使用 `PdfOptions.setVectorRasterizationOptions` 以串流輸出，而非一次載入整個檔案至記憶體。

## 常見問答

**Q: 我可以在批次工作中使用此功能將 DWG 轉換為 PDF 嗎？**  
A: 可以，將每個轉換放在各自的執行緒中，並使用獨立的中斷令牌，以強制每個檔案的時間限制。

**Q: 逾時機制適用於所有輸出格式嗎？**  
A: 逾時機制與 `InterruptionTokenSource` 相關，適用於任何支援該令牌的格式，包括 PDF、PNG 與 SVG。

**Q: 逾時後會發生什麼事，部分寫入的檔案怎麼處理？**  
A: Aspose.CAD 會自動捨棄未完成的輸出，您不會得到損毀的 PDF。

**Q: 生產環境需要授權嗎？**  
A: 需要，商業部署必須使用有效的 Aspose.CAD 授權；亦提供免費試用版供評估使用。

**Q: 哪裡可以找到更多使用中斷令牌的範例？**  
A: 官方 Aspose.CAD 文件提供更多程式碼片段與最佳實踐指南。

## 其他資源

- [releases page](https://releases.aspose.com/cad/java/) – 最新 Aspose.CAD for Java 版本的直接下載頁面。  
- [documentation](https://reference.aspose.com/cad/java/) – 完整 API 參考與開發者指南。  
- [this link](https://releases.aspose.com/) – Aspose 產品的一般發布資訊。  
- [here](https://purchase.aspose.com/temporary-license/) – 取得測試用的臨時授權。  
- [Aspose.CAD forum](https://forum.aspose.com/c/cad/19) – 社群支援與討論區。

## 結論

您現在已掌握 **如何設定逾時**，以在使用 Aspose.CAD for Java 儲存 CAD 圖面時保證安全。將 `InterruptionTokenSource` 整合至工作流程後，您即可可靠地 **將 CAD 匯出為 PDF** 或 **將 DWG 轉換為 PDF**，而不必擔心長時間卡住，確保應用程式保持回應且具可擴展性。

---

**Last Updated:** 2026-06-19  
**Tested With:** Aspose.CAD for Java 24.12  
**Author:** Aspose  

{{< blocks/products/products-backtop-button >}}

## 相關教學

- [使用 Aspose.CAD for Java 匯出 DWG 為 PDF 或光柵圖像](/cad/java/cad-drawing-conversion/export-dwg-to-pdf-or-raster/)
- [使用 Aspose.CAD for Java 匯出特定 DWG 版面為 PDF](/cad/java/cad-drawing-conversion/export-specific-dwg-layout-to-pdf/)
- [使用 Aspose.CAD for Java 將 DWG 轉換為 PNG 及其他光柵格式](/cad/java/cad-drawing-conversion/convert-cad-layout-to-raster-image/)


{{< /blocks/products/pf/tutorial-page-section >}}
{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}