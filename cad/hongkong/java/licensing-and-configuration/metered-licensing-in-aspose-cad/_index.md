---
date: 2026-05-25
description: 了解如何在 Aspose.CAD for Java 中設定計量授權，以優化 CAD 處理、降低成本，並有效追蹤使用情況。
keywords:
- how to set metered
- Aspose.CAD licensing
- Java metered licensing
linktitle: 如何在 Aspose.CAD 中設定計量授權
schemas:
- author: Aspose
  dateModified: '2026-05-25'
  description: Learn how to set metered licensing in Aspose.CAD for Java to optimize
    CAD processing, reduce costs, and track usage efficiently.
  headline: How to Set Metered Licensing in Aspose.CAD
  type: TechArticle
- questions:
  - answer: A usage‑based model that tracks API calls and charges per consumption
      unit.
    question: What is metered licensing?
  - answer: Two keys – a public and a private key – generated from your Aspose account.
    question: How many keys are required?
  - answer: Yes, call `License.getConsumptionQuantity()` before and after processing.
    question: Can I check usage programmatically?
  - answer: A free trial license can be obtained from the Aspose website.
    question: Is a trial available?
  - answer: Java 8 through 17 are fully supported.
    question: Which Java version is supported?
  type: FAQPage
second_title: Aspose.CAD Java API
title: 如何在 Aspose.CAD 中設定計量授權
url: /zh-hant/java/licensing-and-configuration/metered-licensing-in-aspose-cad/
weight: 10
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Aspose.CAD 的計量授權

## 介紹

釋放 Aspose.CAD for Java 的全部潛能，使用 **如何設定計量** 授權！本一步一步的指南將帶領您完成每個階段——從安裝前置條件、匯入正確的套件，到在處理前後測量消耗量。完成後，您將確切了解 **如何設定計量** 金鑰、讀取使用指標，並保持 CAD 工作流程的成本效益。

## 快速解答
- **什麼是計量授權？** 一種基於使用量的模型，會追蹤 API 呼叫並依消耗單位收費。  
- **需要多少把金鑰？** 兩把金鑰——一把公鑰和一把私鑰——由您的 Aspose 帳戶產生。  
- **我可以程式化檢查使用情況嗎？** 可以，在處理前後呼叫 `License.getConsumptionQuantity()`。  
- **是否提供試用版？** 可從 Aspose 官方網站取得免費試用授權。  
- **支援哪個 Java 版本？** 完全支援 Java 8 至 17。

## Aspose.CAD 的計量授權是什麼？
計量授權是 Aspose.CAD 的即付即用模型，會將每一次 API 呼叫記錄為一個消耗單位。它讓您能精確監控使用量、避免過度配置，且僅為實際消耗付費。

## 為何在 CAD 處理上使用計量授權？
Aspose.CAD 支援 **50+** 種輸入與輸出格式——包括 DWG、DXF、DGN 與 SVG，且可處理高達 **2 GB** 的檔案而無需將整個文件載入記憶體。此效率可降低伺服器成本，尤其在處理大量圖紙時更為顯著。

## 前置條件

在深入 Aspose.CAD 計量授權的世界之前，請確保已具備以下條件：

### Java Development Kit (JDK) 安裝

確保您的系統已安裝最新版本的 Java Development Kit。您可以從 [here](https://www.oracle.com/java/technologies/javase-downloads.html) 下載。

### Aspose.CAD for Java 函式庫

請下載並設定 Aspose.CAD for Java 函式庫。您可以在 [here](https://releases.aspose.com/cad/java/) 找到該函式庫。亦可在 [here](https://releases.aspose.com/) 瀏覽其他 Aspose 版本。

## 如何在 Aspose.CAD for Java 中設定計量授權？

載入您的公鑰與私鑰，呼叫 `License.setMeteredKey(publicKey, privateKey)`，函式庫即會立即切換至計量模式。此單一呼叫會為之後的每個 API 操作啟用使用量追蹤，讓您能在任何處理步驟前後查詢消耗情況。

## 匯入套件

為了使用函式庫，請匯入其核心套件：

`import com.aspose.cad.*;` 會將 Aspose.CAD 類別帶入您的專案。

```java
import com.aspose.cad;
```

## 步驟 1：設定計量金鑰

`setMeteredKey` 會將您的公鑰與私鑰註冊至 Aspose.CAD 函式庫。

首先，使用 `setMeteredKey` 方法設定計量金鑰。將 `<valid public key>` 與 `<valid private key>` 替換為您實際的公鑰與私鑰。

```java
Metered.setMeteredKey("<valid public key>", "<valid private key>");
```

## 步驟 2：在處理前取得消耗量

`getConsumptionQuantity` 會回傳迄今為止記錄的總消耗單位數。

在存取 Aspose.CAD API 之前取得已消耗的數量，以獲得初步了解。

```java
BigDecimal quantityOld = Metered.getConsumptionQuantity();
System.out.println("Consumption quantity before processing: " + quantityOld);
```

## 步驟 3：處理

使用 Aspose.CAD 功能執行您想要的 CAD 處理。取消註解與您特定任務相關的程式碼片段，例如載入 CAD 圖像。

```java
// Example:
// com.aspose.cad.fileformats.cad.CadImage image =
// (com.aspose.cad.fileformats.cad.CadImage)com.aspose.cad.Image.load("BlockRefDgn.dwg");
```

## 步驟 4：在處理後取得消耗量

處理完成後，再次取得已消耗的數量，以評估影響。

```java
BigDecimal quantity = Metered.getConsumptionQuantity();
System.out.println("Consumption quantity after processing: " + quantity);
```

如有需要，請重複上述步驟以執行其他處理或任務。

## 常見問題與解決方案

- **Invalid key error:** 請再次確認兩把金鑰已完全照 Aspose 帳戶中顯示的內容複製；多餘的空格會導致驗證失敗。  
- **Zero consumption reported:** 請確保在第一次 API 使用 *之後* 呼叫 `License.getConsumptionQuantity()`；首次呼叫會初始化計數器。  
- **Performance slowdown on large files:** 使用 `CadImage.load(..., LoadOptions)` 搭配 `LoadOptions.setLoadMode(LoadMode.Stream)`，以避免將整個檔案載入記憶體。

## 常見問與答

**Q1：我可以將計量授權用於評估目的嗎？**  
A1: 可以，您可在 [here](https://releases.aspose.com/) 取得免費試用授權。

**Q2：在哪裡可以找到 Aspose.CAD for Java 的詳細文件？**  
A2: 請參考文件 [here](https://reference.aspose.com/cad/java/)。

**Q3：如何購買 Aspose.CAD for Java 的授權？**  
A3: 前往購買頁面 [here](https://purchase.aspose.com/buy)。

**Q4：是否提供臨時授權選項？**  
A5: 是的，您可在 [here](https://purchase.aspose.com/temporary-license/) 探索臨時授權。

**Q5：需要社群支援或有特定問題？**  
A5: 前往 Aspose.CAD 論壇 [here](https://forum.aspose.com/c/cad/19)。

**Q6：計量授權能在雲端部署中使用嗎？**  
A6: 當然可以。相同的 `setMeteredKey` 呼叫在 Docker、Kubernetes 或無伺服器環境中皆可運作。

**Q7：我可以重設消耗計數器嗎？**  
A7: 計數器會在每個新計費週期開始時自動重設，無法手動重設。

## 結論

恭喜！您已成功掌握 **如何設定計量** 授權於 Aspose.CAD for Java。透過本指南，您已順利在 Java 專案中設定並整合計量授權，確保有效使用 Aspose.CAD 功能，同時讓成本透明化。

---

**最後更新：** 2026-05-25  
**測試環境：** Aspose.CAD for Java 24.10  
**作者：** Aspose  

{{< blocks/products/products-backtop-button >}}

## 相關教學

- [使用 Aspose.CAD for Java 將 CAD 轉換為 PDF – 完整教學](/cad/java/)
- [從 CAD 建立 PDF – 使用 Aspose.CAD for Java 匯出 DXF 為 PDF](/cad/java/additional-features/export-dxf-to-pdf/)
- [設定畫布大小 – 使用 Aspose.CAD for Java 的進階 CAD 功能](/cad/java/advanced-cad-features/)


{{< /blocks/products/pf/tutorial-page-section >}}
{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}