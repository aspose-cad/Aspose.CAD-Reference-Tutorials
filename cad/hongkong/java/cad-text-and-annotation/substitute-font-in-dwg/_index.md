---
date: 2025-12-28
description: 學習如何在 Java 專案中載入 DWG 檔案，並使用 Aspose.CAD for Java 設定主要字型名稱。一步一步的指南，打造完美的
  CAD 視覺效果。
linktitle: Substitute Font in DWG
second_title: Aspose.CAD Java API
title: 如何在 Java 中載入 DWG 檔案並使用 Aspose.CAD 替換字型
url: /zh-hant/java/cad-text-and-annotation/substitute-font-in-dwg/
weight: 11
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# 如何在 Java 中載入 DWG 檔案並使用 Aspose.CAD 替換字型

## 簡介

如果您需要 **load DWG file Java** 應用程式並為圖紙增添精緻外觀，替換字型是一個快速且有效的做法。使用 Aspose.CAD for Java，您可以將預設文字樣式替換為任何已安裝於系統的字型，確保每個註解都如您所預期地正確顯示。在本教學中，我們將逐步說明整個流程——從在 Java 中載入 DWG 檔案到使用 `setPrimaryFontName` 方法變更字型。

## 快速解答
- **需要什麼函式庫？** Aspose.CAD for Java.
- **可以在 Java 中載入 DWG 檔案嗎？** Yes, simply call `Image.load()` on the DWG path.
- **哪個方法會變更字型？** `setPrimaryFontName`.
- **在正式環境需要授權嗎？** Yes, a commercial license is required.
- **是否支援批次處理？** Absolutely – loop through multiple files with the same code.

## 什麼是「load dwg file java」？

在 Java 環境中載入 DWG 檔案，即是將二進位 CAD 資料讀取至 Aspose.CAD 可操作的 `Image` 物件中。檔案載入後，您即可透過程式完整存取圖層、樣式與文字實體。

## 為什麼要在 DWG 檔案中替換字型？

- **一致性：** 確保所有協作者看到相同的字型，不受本機字型設定影響。  
- **可讀性：** 某些預設 CAD 字型在螢幕上難以辨識，換成如 Arial 這類清晰字型可提升可讀性。  
- **品牌形象：** 使技術圖紙符合企業的風格指南。

## 先決條件

- **Java Development Kit (JDK)** – 任意較新的版本（建議 8 以上）。  
- **Aspose.CAD for Java** – 從 [website](https://releases.aspose.com/cad/java/) 下載。  
- **Sample DWG file** – 您想要修改的圖紙（測試時可使用任何 DWG 或 DXF 檔案）。

## 匯入命名空間

在您的 Java 專案中，匯入使用 Aspose.CAD 所需的類別。這些匯入讓您能存取影像載入、CAD 專屬物件以及樣式操作功能。

```java
import com.aspose.cad.Image;

import com.aspose.cad.fileformats.cad.CadImage;
import com.aspose.cad.fileformats.cad.cadtables.CadStyleTableObject;
```

## 逐步指南：替換字型

### 步驟 1：載入您的 DWG 檔案（load dwg file java）

首先，將 API 指向您的 DWG（或 DXF）檔案所在位置，並將其載入至 `CadImage` 物件中。

```java
// The path to the resource directory.
String dataDir = "Your Document Directory" + "CADConversion/";

String srcFile = dataDir + "conic_pyramid.dxf";
CadImage cadImage = (CadImage) Image.load(srcFile);
```

> **小技巧：** 如果直接處理 DWG 檔案，請在 `srcFile` 變數中將 `.dxf` 副檔名改為 `.dwg`。

### 步驟 2：遍歷樣式表並設定主要字型名稱

每個 CAD 圖紙都包含一系列樣式物件。遍歷這些物件，並使用 `setPrimaryFontName` 方法（即 **設定主要字型名稱** 的 API 呼叫）來替換字型。

```java
for(Object style : cadImage.getStyles())
{
    // Set the font name
    ((com.aspose.cad.fileformats.cad.cadtables.CadStyleTableObject)style).setPrimaryFontName("Arial");
}
```

您可以將 `"Arial"` 更改為執行程式的機器上已安裝的任何字型。

### 步驟 3：儲存已修改的圖紙

更新字型後，將變更寫回新的 DWG 檔案（或覆寫原始檔案）。

```java
cadImage.save(dataDir + "output.dwg", new DwgOptions());
```

儲存後的檔案將使用您指定的字型，所有文字註解皆會以該字型呈現。

## 常見問題與解決方案

| 問題 | 解決方案 |
|-------|----------|
| **字型未套用** | 確認該字型已安裝於主機作業系統，且字型名稱拼寫完全正確。 |
| **`Image.load` 拋出例外** | 確保檔案路徑正確，且檔案為支援的 DWG/DXF 格式。 |
| **大型檔案效能下降** | 將檔案於獨立執行緒處理或批次執行，以避免 UI 被阻塞。 |

## 常見問答

### Q1: 我可以還原 DWG 檔案中的字型替換嗎？

A1: 是的，您可以透過重新載入原始 DWG 檔案或使用 CAD 軟體內的復原功能來還原字型替換。

### Q2: 在 Aspose.CAD for Java 中字型替換有任何限制嗎？

A2: 字型替換功能取決於系統中可用的字型。請確保所需字型可存取，或考慮將其嵌入 DWG 檔案中。

### Q3: 在替換過程中，我該如何處理字型大小的調整？

A3: 您可以透過存取 Aspose.CAD 中的樣式屬性，並相應地修改字型大小來調整字型尺寸。

### Q4: 我可以在批次處理中自動化字型替換嗎？

A4: 可以，Aspose.CAD for Java 支援批次處理。您可以使用腳本或程式碼在多個 DWG 檔案間自動化字型替換。

### Q5: Aspose.CAD for Java 是否相容於最新的 CAD 檔案格式？

A5: 是的，Aspose.CAD for Java 會定期更新，以支援最新的 CAD 檔案格式，確保與業界標準相容。

## 常見問題

**Q: `setPrimaryFontName` 方法是否僅影響文字實體？**  
A: 它會更新樣式表的主要字型，進而影響所有引用該樣式的文字物件。

**Q: 我可以使用未安裝於系統的自訂字型嗎？**  
A: Aspose.CAD 依賴作業系統的字型註冊表。若要使用自訂字型，需先將其安裝在執行程式的機器上。

**Q: 是否可以僅為單一圖層變更字型？**  
A: 可以，在呼叫 `setPrimaryFontName` 前，先依圖層名稱篩選樣式。

**Q: 需要哪個版本的 Aspose.CAD 才能支援 DWG 2022 檔案？**  
A: 最新發行版（截至 2025 年）完整支援 DWG 2022。請隨時查閱發行說明以確認特定格式支援情況。

**Q: 在開發環境中如何處理授權？**  
A: 可使用臨時評估授權進行測試。正式環境則需使用 `License.setLicense("Aspose.Total.Java.lic");` 嵌入已購買的授權檔案。

---

**最後更新：** 2025-12-28  
**測試環境：** Aspose.CAD for Java 24.11  
**作者：** Aspose  

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}