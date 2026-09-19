---
date: 2026-09-19
description: 了解如何在 .NET 中實作 Aspose CAD 計量授權，以有效監控 .NET 應用程式的資源使用情況。請跟隨我們的逐步指南。
keywords:
- aspose cad metered licensing
- monitor resource usage .net
- aspose cad licensing
lastmod: 2026-09-19
linktitle: 計量授權
og_description: 了解如何在 .NET 中實作 Aspose CAD 計量授權，以有效監控 .NET 應用程式的資源使用情況。請跟隨我們的逐步指南。
og_image_alt: Guide to Aspose CAD metered licensing for .NET developers
og_title: 如何在 .NET 中使用 Aspose CAD 計量授權
schemas:
- author: Aspose
  dateModified: '2026-09-19'
  description: Learn how to implement Aspose CAD metered licensing in .NET to monitor
    resource usage .NET applications efficiently. Follow our step‑by‑step guide.
  headline: How to use Aspose CAD metered licensing in .NET
  type: TechArticle
- description: Learn how to implement Aspose CAD metered licensing in .NET to monitor
    resource usage .NET applications efficiently. Follow our step‑by‑step guide.
  name: How to use Aspose CAD metered licensing in .NET
  steps:
  - name: '**Aspose.CAD installed** – download the latest package from the [Aspose.CAD
      website](https://releases.aspose.com/cad/net/).'
    text: '**Aspose.CAD installed** – download the latest package from the [Aspose.CAD
      website](https://releases.aspose.com/cad/net/).'
  - name: '**Public and private keys** – obtain them from the [Aspose.CAD purchase
      page](https://purchase.aspose.com/buy).'
    text: '**Public and private keys** – obtain them from the [Aspose.CAD purchase
      page](https://purchase.aspose.com/buy).'
  - name: '**Basic .NET knowledge** – the guide assumes you are comfortable with C#
      projects targeting .NET 6 or later.'
    text: '**Basic .NET knowledge** – the guide assumes you are comfortable with C#
      projects targeting .NET 6 or later.'
  type: HowTo
- questions:
  - answer: Yes, the free trial version available from the [free trial version](https://releases.aspose.com/)
      supports metered licensing.
    question: Can I use metered licensing with a free trial?
  - answer: Monitoring before and after each major operation gives the most accurate
      insight, but you can also poll at regular intervals for long‑running services.
    question: How often should I check consumption quantities?
  - answer: Yes, the same public/private key pair can be reused across multiple projects
      and environments.
    question: Are metered keys reusable?
  - answer: The library will throw a licensing exception. You can either purchase
      additional credits or contact support via the [Aspose.CAD support](https://forum.aspose.com/c/cad/19)
      forum.
    question: What happens if I exceed my metered limit?
  - answer: Absolutely – explore [temporary licensing options](https://purchase.aspose.com/temporary-license/)
      for limited‑duration needs.
    question: Can I temporarily license Aspose.CAD for a short‑term project?
  type: FAQPage
second_title: Aspose.CAD .NET - CAD and BIM File Format
tags:
- aspose cad
- metered licensing
- .net resource monitoring
title: 如何在 .NET 中使用 Aspose CAD 計量授權
url: /zh-hant/net/licensing-and-configuration/metered-licensing/
weight: 12
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Aspose CAD 計量授權於 .NET

## 簡介

Aspose CAD 計量授權讓您能控制 .NET 應用程式消耗多少 CAD/BIM API 呼叫，提供精確的計費與使用情況洞察。透過整合此授權模式，您可以 **監測 .NET 資源使用** 應用程式，而無需硬編碼限制，使擴展與成本管理變得簡單。以下指南將逐步說明，從匯入命名空間到在處理前後讀取消耗資料。

## 快速回答
- **什麼是計量授權？** 一種基於使用量的模式，每次 API 呼叫會消耗預先定義的點數。
- **我需要試用授權嗎？** 是 – 免費試用版可與計量金鑰一起使用。
- **如何查看消耗量？** 在操作前後呼叫 `License.GetConsumptionQuantity()`。
- **它是執行緒安全的嗎？** 是，授權引擎設計為可支援並行的 .NET 工作負載。
- **我可以重複使用相同的金鑰嗎？** 當然可以 – 相同的公私鑰組合可在多個專案間共享。

## 什麼是 Aspose CAD 計量授權？

Aspose CAD 計量授權是一種基於使用量的授權方案，會追蹤 Aspose.CAD for .NET 函式庫所發出的每一次 API 呼叫。它讓開發人員只為實際消耗的資源付費，而不必購買永久授權。

## 為何在 Aspose CAD 中使用計量授權？

計量授權透過僅對實際 API 使用量收費，讓您精確掌控成本。它免除預先購買授權座位的需求，且會隨工作負載自動擴展，非常適合使用量波動的間歇性或雲端處理。

## 前置條件

1. **已安裝 Aspose.CAD** – 從 [Aspose.CAD 官方網站](https://releases.aspose.com/cad/net/) 下載最新套件。  
2. **公私鑰** – 從 [Aspose.CAD 購買頁面](https://purchase.aspose.com/buy) 取得。  
3. **基本 .NET 知識** – 本指南假設您熟悉目標為 .NET 6 或更高版本的 C# 專案。

## 匯入命名空間

在 C# 檔案的頂部加入所需的 `using` 指示，以便編譯器能找到 Aspose.CAD 類別。

```csharp
using Aspose.CAD;
using Aspose.CAD.ImageOptions;
using Aspose.CAD.License;
```

`License` 命名空間包含計量授權所需的類別。

## 如何設定計量金鑰？

`SetMeteredKey` 會將您的公私計量授權金鑰註冊至 Aspose.CAD 引擎。請在應用程式啟動時呼叫此方法一次，並傳入從 Aspose 取得的金鑰。這可確保所有後續的 API 呼叫皆被計入您的計量帳戶。

```csharp
using System;
using System.Collections.Generic;
using System.Linq;
using System.Text;
```

## 如何在 API 呼叫前取得消耗數量？

`GetConsumptionQuantity` 會回傳函式庫截至呼叫點為止已消耗的總點數。請在執行任何 CAD 操作前取得此值，以建立基準。將其與處理後的值比較，即可確定特定任務的實際點數使用量。

```csharp
//ExStart:MeteredLicensing
// Access the setMeteredKey property and pass public and private keys as parameters
Aspose.CAD.Metered.SetMeteredKey("PublicKey", "PrivateKey");
```

## 如何使用 Aspose.CAD 處理 CAD 資料？

`CadImage` 代表已載入的 CAD 檔案，並提供渲染或轉換的方法。設定計量金鑰後，將 CAD 檔案載入 `CadImage` 實例。之後您可以渲染為點陣圖格式、轉換為其他 CAD 類型，或擷取中繼資料，所有操作皆會計入您的計量配額。

```csharp
// Get metered data amount before calling API
decimal amountbefore = Aspose.CAD.Metered.GetConsumptionQuantity();
// Display information
Console.WriteLine("Amount Consumed Before: " + amountbefore.ToString());
```

## 如何在 API 呼叫後取得消耗數量？

處理完畢後可再次呼叫 `GetConsumptionQuantity` 以取得更新後的點數總計。將先前記錄的基準值減去，即可計算最近一次操作消耗了多少點數。此資訊有助於您監控使用模式，並優化程式碼以降低成本。

```csharp
// Do processing
//Aspose.CAD.FileFormats.Cad.CadImage image = (Aspose.CAD.FileFormats.Cad.CadImage)Aspose.CAD.Image.load("BlockRefDgn.dwg");
```

## 常見問題與疑難排解

- **未設定授權錯誤：** 確保在任何 Aspose.CAD API 使用前已呼叫 `SetMeteredKey`。  
- **意外的高消耗量：** 確認未在迴圈中不小心載入大量檔案；每次載入皆算一次呼叫。  
- **執行緒安全性疑慮：** 授權引擎是執行緒安全的，但請避免同時多次呼叫 `SetMeteredKey`。

## 常見問答

**Q: 我可以在免費試用版中使用計量授權嗎？**  
A: 可以，從 [免費試用版](https://releases.aspose.com/) 取得的免費試用版本支援計量授權。

**Q: 我應該多久檢查一次消耗數量？**  
A: 在每個主要操作前後監測可提供最精確的洞察，但對於長時間執行的服務，也可以定期輪詢。

**Q: 計量金鑰可以重複使用嗎？**  
A: 可以，相同的公私金鑰組合可在多個專案與環境中重複使用。

**Q: 若超出計量上限會發生什麼事？**  
A: 函式庫會拋出授權例外。您可以購買額外點數，或透過 [Aspose.CAD 支援論壇](https://forum.aspose.com/c/cad/19) 聯絡支援。

**Q: 我可以為短期專案暫時授權 Aspose.CAD 嗎？**  
A: 當然可以 – 可參考 [臨時授權選項](https://purchase.aspose.com/temporary-license/) 以滿足有限期限的需求。

---

**最後更新：** 2026-09-19  
**測試環境：** Aspose.CAD 24.11 for .NET  
**作者：** Aspose  

```csharp
// Get metered data amount after calling API
decimal amountafter = Aspose.CAD.Metered.GetConsumptionQuantity();
// Display information
Console.WriteLine("Amount Consumed After: " + amountafter.ToString());
//ExEnd:MeteredLicensing 
```

## 相關教學

- [在 Aspose.CAD for .NET 中套用授權 – 步驟教學](/cad/net/)
- [如何使用 Aspose.CAD for .NET 將 CAD 圖紙轉換並匯出為 PDF – 教學](/cad/net/advanced-export-techniques/exporting-cad-drawings-to-pdf/)
- [在 Aspose.CAD for .NET 中將 CAD 轉換為 PNG](/cad/net/cad-drawing-manipulation/convert-cad-drawing-to-raster-image/)


{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}