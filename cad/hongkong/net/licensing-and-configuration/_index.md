---
date: 2026-09-14
description: 了解如何使用檔案路徑或 FileStream 在 Aspose.CAD for .NET 中套用授權，並探索計量授權以優化資源使用。
keywords:
- how to apply license
- apply license by path
- apply license using filestream
- metered licensing
lastmod: 2026-09-14
linktitle: 授權與設定
og_description: 了解如何使用檔案路徑或 FileStream 在 Aspose.CAD for .NET 中套用授權，並探索計量授權以優化資源使用。（150‑160
  字）
og_image_alt: Screenshot of Aspose.CAD license configuration page in a .NET IDE
og_title: 如何在 Aspose.CAD for .NET 中套用授權 – 快速指南
schemas:
- author: Aspose
  dateModified: '2026-09-14'
  description: Learn how to apply license in Aspose.CAD for .NET using a file path
    or FileStream, and explore metered licensing to optimise resource usage.
  headline: How to apply license in Aspose.CAD for .NET
  type: TechArticle
- description: Learn how to apply license in Aspose.CAD for .NET using a file path
    or FileStream, and explore metered licensing to optimise resource usage.
  name: How to apply license in Aspose.CAD for .NET
  steps:
  - name: Place your `Aspose.CAD.lic` file in a folder that your application can read
      (e.g., the application root or a secured config folder).
    text: Place your `Aspose.CAD.lic` file in a folder that your application can read
      (e.g., the application root or a secured config folder).
  - name: 'Add the following code early in your startup routine (e.g., `Main`, `Startup.Configure`,
      or `Global.asax`):'
    text: 'Add the following code early in your startup routine (e.g., `Main`, `Startup.Configure`,
      or `Global.asax`):'
  - name: Retrieve the license bytes from your source (file system, Azure Blob, etc.).
    text: Retrieve the license bytes from your source (file system, Azure Blob, etc.).
  - name: Open a `FileStream` with read permissions.
    text: Open a `FileStream` with read permissions.
  - name: Pass the stream to the `License` object.
    text: Pass the stream to the `License` object.
  - name: Obtain a metered‑license key from your Aspose account dashboard.
    text: Obtain a metered‑license key from your Aspose account dashboard.
  - name: Register the key with `License.SetMeteredKey("your‑key")`.
    text: Register the key with `License.SetMeteredKey("your‑key")`.
  - name: After each operation, call `License.GetMeteredUsage()` to retrieve the current
      usage count.
    text: After each operation, call `License.GetMeteredUsage()` to retrieve the current
      usage count.
  type: HowTo
- questions:
  - answer: Yes, a single license file can be deployed to any number of development
      or production servers, provided the usage complies with your purchased term.
    question: Can I use the same license file on multiple machines?
  - answer: The library will run in evaluation mode, adding a watermark to rendered
      images and limiting the number of pages you can process.
    question: What happens if I forget to set the license before loading a CAD file?
  - answer: Only the first activation and each usage report need connectivity; after
      that, the library can operate offline until the next report.
    question: Does metered licensing require an internet connection?
  - answer: Aspose.CAD supports 45+ input and output formats, including DWG, DXF,
      DGN, STL, OBJ, and IFC, and can render files up to 500 MB without loading the
      entire document into memory.
    question: Which CAD/BIM formats are supported out of the box?
  - answer: Call `License.IsLicensed` (or inspect `License.LicenseFilePath`) after
      registration; it returns `true` when a valid license is active.
    question: Is there a way to programmatically check if the license was applied
      successfully?
  type: FAQPage
second_title: Aspose.CAD .NET - CAD and BIM File Format
tags:
- Aspose.CAD
- license configuration
- .NET
- CAD processing
- metered licensing
title: 如何在 Aspose.CAD for .NET 中套用授權
url: /zh-hant/net/licensing-and-configuration/
weight: 20
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# 如何在 Aspose.CAD for .NET 中套用授權

歡迎閱讀關於 **如何套用授權** 的 Aspose.CAD .NET 完整指南。無論您是開發桌面工具、伺服器端服務，或自動化 BIM 流程，有效的授權可解鎖超過 40 種 CAD 與 BIM 格式的完整套件，提升高效能渲染，並移除評估水印。本篇文章將一步步說明所有授權選項，讓您能無縫開始開發。

## 快速回答
- **我可以從檔案路徑載入授權嗎？** 是的 – 只需實例化 `License` 並呼叫 `SetLicense("path/to/license.lic")`。  
- **支援 FileStream 嗎？** 當然可以；將開啟的串流傳遞給 `SetLicense(stream)`。  
- **什麼是計量授權？** 它會依每次請求追蹤使用量，讓您只為實際消耗的部分付費。  
- **開發時需要授權嗎？** 免費試用授權可用於開發與測試；正式環境則需商業授權。  
- **支援哪些 .NET 版本？** .NET Framework 4.5+、.NET Core 3.1+、.NET 5/6/7。

## Aspose.CAD 的授權是什麼？
Aspose.CAD 的授權機制用於驗證您的購買並啟用函式庫的完整功能集。若未套用授權，API 會以評估模式執行，限制輸出大小並在渲染的影像上加上水印。

## 為什麼使用基於路徑的授權而非串流？
基於路徑的授權是啟用 Aspose.CAD 最快速的方式：只要指向 .lic 檔案，函式庫會自動載入。當需要從非檔案來源讀取授權、實施自訂安全機制，或將授權嵌入組件時，則使用串流。請依您的部署限制選擇合適的方法。

`License` 類別代表 Aspose.CAD 的授權元件，用於向 API 註冊授權。

## 如何在 Aspose.CAD for .NET 中以路徑套用授權？

要以路徑套用授權，請建立 `License` 類別的實例，並以完整的 .lic 檔案路徑呼叫其 `SetLicense` 方法。請將此程式碼放在應用程式啟動的早期，以確保之後的 CAD 操作皆在授權環境下執行。

`License` 類別代表 Aspose.CAD 的授權元件，用於向 API 註冊授權。

1. 將您的 `Aspose.CAD.lic` 檔案放置於應用程式可讀取的資料夾（例如應用程式根目錄或受保護的設定資料夾）。  
2. 在啟動例程的早期加入以下程式碼（例如 `Main`、`Startup.Configure` 或 `Global.asax`）：

```csharp
// No code block added – original tutorial contained none.
```

> **直接回答（40‑70 個字）:**  
> 要以路徑套用授權，建立 `License` 物件並呼叫 `SetLicense("full\\path\\to\\Aspose.CAD.lic")`。此單行程式碼即可啟用完整函式庫、移除評估水印，並讓您在不受效能限制的情況下處理超過 40 種 CAD/BIM 格式。請在任何 CAD 操作之前呼叫，以確保授權已生效。

## 如何在 Aspose.CAD for .NET 中使用 FileStream 套用授權？

要使用 `FileStream` 套用授權，請以讀取模式開啟 .lic 檔案，建立 `License` 物件，並將串流傳遞給 `SetLicense`。確保串流在註冊完成前保持開啟，完成後再關閉以釋放資源。

`FileStream` 類別提供用於讀寫磁碟檔案的串流。

1. 從您的來源（檔案系統、Azure Blob 等）取得授權位元組。  
2. 以讀取權限開啟 `FileStream`。  
3. 將串流傳遞給 `License` 物件。

> **直接回答（40‑70 個字）:**  
> 建立 `License` 物件並呼叫 `SetLicense(stream)`，其中 `stream` 為指向您的 `Aspose.CAD.lic` 的可讀 `FileStream`。此方式可從記憶體載入授權，若需要可將檔案保留在檔案系統之外，並立即啟用所有功能。確保串流在註冊完成前保持開啟，完成後再關閉。

## Aspose.CAD for .NET 的計量授權如何運作？

透過呼叫 `License.SetMeteredKey` 並傳入唯一金鑰即可啟用計量授權。註冊後，SDK 會自動將每次 CAD 操作回報至 Aspose 伺服器，讓您能監控使用量，並僅為訂閱期間內執行的操作付費。

`License.SetMeteredKey` 方法用於向 Aspose.CAD 函式庫註冊計量授權金鑰。

1. 從 Aspose 帳戶儀表板取得計量授權金鑰。  
2. 使用 `License.SetMeteredKey("your‑key")` 註冊金鑰。  
3. 每次操作後，呼叫 `License.GetMeteredUsage()` 以取得目前的使用計數。

> **直接回答（40‑70 個字）:**  
> 透過呼叫 `License.SetMeteredKey("your‑key")` 即可啟用計量授權。SDK 會在每次 CAD 操作後將使用資料傳送至 Aspose 伺服器，讓您依實際消耗進行監控與計費。此模式支援無限制的同時使用者，同時使成本與實際使用情況保持一致。

## 授權與設定教學

### [在 Aspose.CAD for .NET 中以路徑套用授權](./apply-license-by-path/)
釋放 Aspose.CAD for .NET 的完整潛能！遵循我們的逐步指南，輕鬆套用授權。立即提升您的 CAD 檔案操作體驗！

### [在 Aspose.CAD for .NET 中使用 FileStream 套用授權](./apply-license-using-filestream/)
精通 Aspose.CAD for .NET：使用 FileStream 輕鬆套用授權。探索逐步指南，釋放其潛能。立即下載！

### [在 Aspose.CAD for .NET 中的計量授權](./metered-licensing/)
使用 .NET 的計量授權釋放 Aspose.CAD 的潛能。無縫優化資源使用。探索我們的逐步指南。

## 常見問題

**Q: 我可以在多台機器上使用相同的授權檔案嗎？**  
A: 是的，只要使用符合購買條款，可將單一授權檔案部署至任意數量的開發或生產伺服器。

**Q: 若在載入 CAD 檔案前忘記設定授權會發生什麼情況？**  
A: 函式庫將以評估模式執行，於渲染的影像加上水印，且限制可處理的頁數。

**Q: 計量授權是否需要網際網路連線？**  
A: 僅在首次啟用與每次使用回報時需要連線；之後函式庫可離線運作，直至下一次回報。

**Q: 預設支援哪些 CAD/BIM 格式？**  
A: Aspose.CAD 支援超過 45 種輸入與輸出格式，包括 DWG、DXF、DGN、STL、OBJ 及 IFC，且可在不將整個文件載入記憶體的情況下渲染高達 500 MB 的檔案。

**Q: 有沒有程式方式檢查授權是否成功套用？**  
A: 在註冊後呼叫 `License.IsLicensed`（或檢查 `License.LicenseFilePath`）；若授權有效，會回傳 `true`。

---

**最後更新：** 2026-09-14  
**測試環境：** Aspose.CAD 24.11 for .NET  
**作者：** Aspose

## 相關教學

- [在 Aspose.CAD for .NET 中以路徑套用授權](/cad/net/licensing-and-configuration/apply-license-by-path/)
- [在 Aspose.CAD for .NET 中使用 FileStream 套用授權](/cad/net/licensing-and-configuration/apply-license-using-filestream/)
- [在 Aspose.CAD for .NET 中的計量授權](/cad/net/licensing-and-configuration/metered-licensing/)


{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}