---
date: 2026-05-20
description: 了解如何使用 Aspose.CAD for Java 在覆寫自動代碼頁檢測的同時將 DWG 轉換為 PDF。內容包括 DWG 匯出為 PDF
  的步驟、編碼技巧以及故障排除。
keywords:
- convert dwg pdf
- export dwg to pdf
- Aspose.CAD Java
linktitle: 覆寫 DWG 檔案的自動代碼頁檢測
schemas:
- author: Aspose
  dateModified: '2026-05-20'
  description: Learn how to convert DWG to PDF while overriding automatic code page
    detection using Aspose.CAD for Java. Includes export dwg to pdf steps, encoding
    tips, and troubleshooting.
  headline: Convert DWG to PDF – Override Code Page Detection in Java
  type: TechArticle
- description: Learn how to convert DWG to PDF while overriding automatic code page
    detection using Aspose.CAD for Java. Includes export dwg to pdf steps, encoding
    tips, and troubleshooting.
  name: Convert DWG to PDF – Override Code Page Detection in Java
  steps:
  - name: Set Up the Java Project
    text: Create a Maven or Gradle project and add the Aspose.CAD JAR to the classpath.
      This ensures the IDE can resolve the imported classes and that the runtime can
      locate the library.
  - name: Load the DWG File with a Specified Code Page
    text: Tell Aspose.CAD which encoding to use and whether to attempt recovery of
      malformed CIF/MIF data.
  - name: Export the CAD Image to PDF
    text: With the correct code page applied, you can safely export the drawing. The
      `PdfOptions` object lets you fine‑tune the PDF output (compression, rasterization,
      etc.).
  - name: Verify Success
    text: A simple console message confirms that the process completed without exceptions.
      You can repeat these steps for multiple DWG files, adjusting the source path
      and output name as needed.
  type: HowTo
- questions:
  - answer: It forces Aspose.CAD to use a specific character encoding instead of guessing.
    question: What does “override code page” mean?
  - answer: Yes – after setting the correct code page, you can save the CAD image
      as PDF.
    question: Can I export DWG directly to PDF?
  - answer: '`CodePages.Japanese` and `MifCodePages.Japanese` are the right choices.'
    question: Which encoding works for Japanese text?
  - answer: A commercial license is required; a temporary license is available for
      testing.
    question: Do I need a license for production use?
  - answer: Any recent version that supports `LoadOptions` and `PdfOptions`.
    question: What version of Aspose.CAD is needed?
  type: FAQPage
second_title: Aspose.CAD Java API
title: 將 DWG 轉換為 PDF – 在 Java 中覆寫代碼頁檢測
url: /zh-hant/java/dwg-file-operations/override-code-page-detection/
weight: 13
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# 轉換 DWG 為 PDF – 在 Java 中覆寫代碼頁偵測

在本完整教學中，您將學習 **如何將 DWG 轉換為 PDF**，同時覆寫可能導致文字損壞的自動代碼頁偵測。Aspose.CAD for Java 為您提供對字元編碼的精確控制，使您能夠復原格式錯誤的 CIF/MIF 資料並產生可靠的 PDF 輸出。無論您是建立批次轉換器，或是將 CAD 處理加入更大的 Java 服務，以下步驟將帶您走完整個工作流程——從專案設定到驗證。

## 快速解答
- **「override code page」是什麼意思？** 它會強制 Aspose.CAD 使用特定的字元編碼，而不是自行猜測。
- **我可以直接將 DWG 匯出為 PDF 嗎？** 可以 —— 設定正確的代碼頁後，您即可將 CAD 圖像儲存為 PDF。
- **哪種編碼適用於日文文字？** `CodePages.Japanese` 與 `MifCodePages.Japanese` 為正確的選擇。
- **生產環境需要授權嗎？** 需要商業授權；測試用的臨時授權亦可取得。
- **需要哪個版本的 Aspose.CAD？** 任一支援 `LoadOptions` 與 `PdfOptions` 的近期版本皆可。

## 什麼是「export CAD to PDF」？
將 CAD 匯出為 PDF 會將向量式 DWG 圖紙轉換為可普遍檢視、固定版面的 PDF 文件。此轉換會保留所有幾何實體、線條、圖層與嵌入文字，同時將圖紙平面化為易於分享、列印、存檔或嵌入其他應用程式的格式，而無需 CAD 軟體。

## 為什麼要覆寫自動代碼頁偵測？
手動指定代碼頁可確保文字位元正確解讀，消除 Aspose.CAD 自動偵測錯誤舊版編碼時常出現的亂碼。這對於日文、斯拉夫文或阿拉伯文等非拉丁文字尤為重要，亦能確保匯出的 PDF 與原始設計相符。

## 前置條件
- **Java 開發環境** – JDK 8+ 以及您偏好的 IDE。  
- **Aspose.CAD for Java** – 從官方網站下載程式庫 [here](https://releases.aspose.com/cad/java/)。  
- **DWG 範例檔案** – 使用提供的 `SimpleEntities.dwg` 或任何您需要轉換的 DWG。

## 匯入套件
`Document`、`LoadOptions` 與 `PdfOptions` 類別是轉換流程的核心。

`Document` 類別代表記憶體中的 CAD 圖紙，提供載入、操作與以各種格式儲存檔案的方法。  
`LoadOptions` 類別允許您在載入 DWG 檔案時指定代碼頁與復原選項。  
`PdfOptions` 類別控制 PDF 專屬設定，例如壓縮、光柵化與中繼資料。

在您的 Java 專案中，匯入必要的 Aspose.CAD 類別：

```java
import com.aspose.cad.CodePages;
import com.aspose.cad.Image;
import com.aspose.cad.LoadOptions;
import com.aspose.cad.MifCodePages;
import com.aspose.cad.fileformats.cad.CadImage;
```

## 如何在覆寫代碼頁的情況下將 DWG 轉換為 PDF？
使用 `LoadOptions` 載入 DWG 檔案以指定精確的代碼頁，然後以配置好的 `PdfOptions` 實例呼叫產生的 `CadImage` 的 `save` 方法。此兩步驟流程確保文字正確解讀，且產生的 PDF 保留原始圖紙的忠實度、圖層與向量品質。

### 步驟 1：設定 Java 專案
建立 Maven 或 Gradle 專案，並將 Aspose.CAD JAR 加入 classpath。這可確保 IDE 能解析匯入的類別，且執行時能找到程式庫。

### 步驟 2：以指定代碼頁載入 DWG 檔案
告訴 Aspose.CAD 使用哪種編碼，以及是否嘗試復原格式錯誤的 CIF/MIF 資料。

```java
String SourceDir = "Your Document Directory";
String dwgPathToFile = SourceDir + "SimpleEntites.dwg";
LoadOptions opts = new LoadOptions();
opts.setSpecifiedEncoding(CodePages.Japanese);
opts.setSpecifiedMifEncoding(MifCodePages.Japanese);
opts.setRecoverMalformedCifMif(false);
CadImage cadImage = (CadImage) Image.load(dwgPathToFile, opts);
```

### 步驟 3：將 CAD 圖像匯出為 PDF
套用正確的代碼頁後，您即可安全匯出圖紙。`PdfOptions` 物件讓您微調 PDF 輸出（壓縮、光柵化等）。

```java
// Perform export or other operations with cadImage
// For example, exporting to PDF
PdfOptions pdfOptions = new PdfOptions();
cadImage.save("output.pdf", pdfOptions);
```

### 步驟 4：驗證成功
簡單的主控台訊息可確認流程已順利完成且未拋出例外。

```java
System.out.println("OverrideAutomaticCodePageDetectionDwg executed successfully");
```

您可以對多個 DWG 檔案重複上述步驟，依需求調整來源路徑與輸出名稱。

## 常見問題與解決方案
- **仍出現亂碼：** 再次確認 `specifiedEncoding` 與原始 DWG 的代碼頁相符。如有需要，請使用不同的 `CodePages` 列舉值。  
- **`cadImage.save` 發生 `NullPointerException`：** 確認 DWG 檔案已正確載入；檢查路徑與檔案權限。  
- **PDF 檔案過大：** 在 `PdfOptions` 中啟用壓縮（例如 `pdfOptions.setCompress(true)`），以減少檔案大小而不失去品質。

## 常見問答

**Q1: Aspose.CAD 是否相容所有版本的 DWG 檔案？**  
A1: Aspose.CAD 支援超過 30 種 DWG 版本，包括 AutoCAD 2018 及更早的版本。

**Q2: 我可以在商業專案中使用 Aspose.CAD 嗎？**  
A2: 可以，生產環境需要商業授權。您可於此取得授權 [here](https://purchase.aspose.com/buy)。

**Q3: 免費試用版有任何限制嗎？**  
A1: 試用版會限制檔案大小與功能；詳情請參考官方文件。

**Q4: 我該如何取得 Aspose.CAD 的支援？**  
A4: 前往社群 [Aspose.CAD forum](https://forum.aspose.com/c/cad/19) 取得協助與討論。

**Q5: 是否提供測試用的臨時授權？**  
A5: 有，您可在此申請臨時授權 [here](https://purchase.aspose.com/temporary-license/)。

---

**最後更新：** 2026-05-20  
**測試環境：** Aspose.CAD for Java 24.11 (latest at time of writing)  
**作者：** Aspose

## 相關教學

- [匯出 DWG 為 PDF 並轉換 CAD 圖紙 – Aspose.CAD Java 教學](/cad/java/cad-drawing-conversion/)
- [使用 Aspose.CAD for Java 匯出特定 DWG 版面為 PDF](/cad/java/cad-drawing-conversion/export-specific-dwg-layout-to-pdf/)
- [使用 Aspose.CAD for Java 匯出 DWG 為 PDF 或光柵圖像](/cad/java/cad-drawing-conversion/export-dwg-to-pdf-or-raster/)

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}

{{< blocks/products/products-backtop-button >}}

{{< /blocks/products/pf/main-wrap-class >}}