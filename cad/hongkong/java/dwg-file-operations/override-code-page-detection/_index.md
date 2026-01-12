---
date: 2026-01-12
description: 了解如何使用 Aspose.CAD for Java 在將 CAD 匯出為 PDF 時覆寫 DWG 檔案的自動代碼頁偵測。支援編碼與錯誤的
  CIF/MIF。
linktitle: Override Automatic Code Page Detection in DWG Files
second_title: Aspose.CAD Java API
title: 將 CAD 匯出為 PDF – 使用 Java 覆寫 DWG 檔案的自動代碼頁偵測
url: /zh-hant/java/dwg-file-operations/override-code-page-detection/
weight: 13
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# 匯出 CAD 為 PDF – 在 DWG 檔案中以 Java 覆寫自動代碼頁偵測

## 介紹

在本完整指南中，您將了解 **如何將 CAD 匯出為 PDF**，同時覆寫可能導致 DWG 檔案文字損壞的自動代碼頁偵測。Aspose.CAD for Java 提供精細的編碼控制，讓您恢復錯誤的 CIF/MIF 資料，並產生可靠的 PDF 輸出。無論您是建立批次轉換工具，或是將 CAD 處理整合至更大的 Java 應用程式，以下步驟將帶您完成整個工作流程。

## 快速答覆
- **「覆寫代碼頁」是什麼意思？** 它會強制 Aspose.CAD 使用特定的字元編碼，而非自行猜測。
- **我可以直接將 DWG 匯出為 PDF 嗎？** 可以 – 設定正確的代碼頁後，即可將 CAD 圖像儲存為 PDF。
- **哪種編碼適用於日文文字？** `CodePages.Japanese` 與 `MifCodePages.Japanese` 為正確選擇。
- **正式環境需要授權嗎？** 需要商業授權；測試時可使用臨時授權。
- **需要哪個版本的 Aspose.CAD？** 任一支援 `LoadOptions` 與 `PdfOptions` 的近期版本。

## 什麼是「匯出 CAD 為 PDF」？
將 CAD 匯出為 PDF 會把向量式 CAD 圖紙轉換成廣受支援的固定版面文件格式。產生的 PDF 能保留線條、圖層與文字，同時讓圖紙易於分享、列印或嵌入其他應用程式。

## 為什麼要覆寫自動代碼頁偵測？
DWG 檔案常使用舊式代碼頁儲存文字。Aspose.CAD 的自動偵測可能會誤判這些位元，導致字元亂碼。手動指定代碼頁即可確保匯出 PDF 時文字正確顯示，特別是日文、斯拉夫文或阿拉伯文等非拉丁文字。

## 前置條件
- **Java 開發環境** – JDK 8 以上，搭配您喜愛的 IDE。
- **Aspose.CAD for Java** – 從官方網站下載程式庫 [此處](https://releases.aspose.com/cad/java/)。
- **DWG 範例檔** – 使用提供的 `SimpleEntities.dwg` 或任何您需要轉換的 DWG 檔。

## 匯入套件
在您的 Java 專案中匯入必要的 Aspose.CAD 類別：

```java
import com.aspose.cad.CodePages;
import com.aspose.cad.Image;
import com.aspose.cad.LoadOptions;
import com.aspose.cad.MifCodePages;
import com.aspose.cad.fileformats.cad.CadImage;
```

## 步驟說明

### 步驟 1：設定 Java 專案
建立新的 Maven 或 Gradle 專案，並將 Aspose.CAD JAR 加入 classpath。此步驟確保 IDE 能解析匯入的類別。

### 步驟 2：以指定代碼頁載入 DWG 檔案
告訴 Aspose.CAD 使用哪種編碼，並決定是否嘗試恢復錯誤的 CIF/MIF 資料。

```java
String SourceDir = "Your Document Directory";
String dwgPathToFile = SourceDir + "SimpleEntites.dwg";
LoadOptions opts = new LoadOptions();
opts.setSpecifiedEncoding(CodePages.Japanese);
opts.setSpecifiedMifEncoding(MifCodePages.Japanese);
opts.setRecoverMalformedCifMif(false);
CadImage cadImage = (CadImage) Image.load(dwgPathToFile, opts);
```

### 步驟 3：將 CAD 圖像匯出為 PDF
在正確的代碼頁套用後，即可安全匯出圖紙。`PdfOptions` 物件允許您微調 PDF 輸出（壓縮、光柵化等）。

```java
// Perform export or other operations with cadImage
// For example, exporting to PDF
PdfOptions pdfOptions = new PdfOptions();
cadImage.save("output.pdf", pdfOptions);
```

### 步驟 4：驗證成功
簡單的主控台訊息會確認流程已順利完成且未拋出例外。

```java
System.out.println("OverrideAutomaticCodePageDetectionDwg executed successfully");
```

您可以針對多個 DWG 檔案重複上述步驟，僅需調整來源路徑與輸出檔名。

## 常見問題與解決方案
- **仍出現亂碼：** 再次確認 `specifiedEncoding` 與原始 DWG 的代碼頁相符，必要時使用其他 `CodePages` 列舉值。
- **`cadImage.save` 發生 `NullPointerException`：** 確認 DWG 檔案已正確載入；檢查路徑與檔案權限。
- **PDF 檔案過大：** 在 `PdfOptions` 中啟用壓縮，例如 `pdfOptions.setCompress(true)`。

## 常見問答

**Q1：Aspose.CAD 是否相容所有 DWG 版本？**  
A1：Aspose.CAD 支援多種 DWG 版本，包括 AutoCAD 2018 及更早的版本。

**Q2：我可以在商業專案中使用 Aspose.CAD 嗎？**  
A2：可以，正式環境須取得商業授權。您可於 [此處](https://purchase.aspose.com/buy) 取得授權。

**Q3：免費試用版有什麼限制？**  
A3：試用版會限制檔案大小與功能，詳情請參考官方文件。

**Q4：如何取得 Aspose.CAD 的技術支援？**  
A4：請前往社群 [Aspose.CAD 論壇](https://forum.aspose.com/c/cad/19) 取得協助與討論。

**Q5：是否提供測試用的臨時授權？**  
A5：有，您可於 [此處](https://purchase.aspose.com/temporary-license/) 申請臨時授權。

---

**最後更新：** 2026-01-12  
**測試環境：** Aspose.CAD for Java 24.11（撰寫時最新版本）  
**作者：** Aspose  

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}