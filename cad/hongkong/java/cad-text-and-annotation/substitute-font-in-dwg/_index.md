---
date: 2026-05-04
description: 學習如何使用 Aspose.CAD 在 Java 中將 DXF 轉換為 DWG 並設定主要字型。一步一步的指南，打造完美的 CAD 視覺效果。
keywords:
- convert dxf to dwg
- set primary font
- change dwg text style
- how to substitute font
- aspose cad licensing
linktitle: 在 DWG 中替換字型
second_title: Aspose.CAD Java API
title: 將 dxf 轉換為 dwg 並在 DWG 中更改字型 – Aspose.CAD Java
url: /zh-hant/java/cad-text-and-annotation/substitute-font-in-dwg/
weight: 11
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# 如何在 Java 中載入 DWG 檔案並使用 Aspose.CAD 替換字型

## 介紹

如果您需要在 Java 應用程式中 **convert dxf to dwg**，並讓圖紙呈現更精緻的外觀，替換字型是一個快速且有效的做法。使用 Aspose.CAD for Java，您可以將預設文字樣式替換為任何已安裝於系統的字型，確保每個註解都如您所預期的那樣顯示。在本教學中，我們將一步步說明從在 Java 中載入 DWG 檔案，到使用 `setPrimaryFontName` 方法變更字型的完整流程。

## 快速解答
- **需要哪個函式庫？** Aspose.CAD for Java。  
- **可以在 Java 中載入 DWG 檔案嗎？** 可以，只要對 DWG 路徑呼叫 `Image.load()` 即可。  
- **哪個方法可以變更字型？** `setPrimaryFontName`。  
- **正式環境需要授權嗎？** 需要，必須購買商業授權。  
- **可以批次處理嗎？** 當然可以——使用相同程式碼在迴圈中處理多個檔案。

## 什麼是 **convert dxf to dwg**？

「Convert dxf to dwg」指的是將 DXF（Drawing Exchange Format）檔案轉換為許多 CAD 應用程式使用的原生 DWG 格式。透過轉換，您可以將廣受支援的 DXF 圖紙帶入 DWG 工作流程，並利用 Aspose.CAD 套用進階樣式，例如字型替換。

## 為何在 DWG 檔案中替換字型？

- **一致性：** 確保所有協作者看到相同的字型，不受本機字型設定影響。  
- **可讀性：** 某些預設 CAD 字型在螢幕上難以辨識，換成如 Arial 這類清晰字型可提升可讀性。  
- **品牌形象：** 讓技術圖紙符合公司風格指南。

## 常見使用情境

| 情境 | 為何重要 |
|----------|----------------|
| **批次轉換舊有 DXF 圖紙** | 可一次將它們轉為 DWG 並套用公司字型。 |
| **為客戶簡報準備圖紙** | 統一且易讀的字型讓文件更顯專業。 |
| **自動化 CAD 流程** | 內嵌字型替換可省去手動後處理步驟。 |

## 前置條件

- **Java Development Kit (JDK)** – 任意近期版本（建議 8 以上）。  
- **Aspose.CAD for Java** – 從[官方網站](https://releases.aspose.com/cad/java/)下載。  
- **範例 DWG/DXF 檔案** – 您想要修改的圖紙（測試時可使用任意 DWG 或 DXF 檔案）。

## 匯入命名空間

在您的 Java 專案中，匯入使用 Aspose.CAD 所需的類別。這些匯入讓您能存取圖像載入、CAD 專屬物件與樣式操作。

```java
import com.aspose.cad.Image;

import com.aspose.cad.fileformats.cad.CadImage;
import com.aspose.cad.fileformats.cad.cadtables.CadStyleTableObject;
```

## 替換字型的逐步指南

### 步驟 1：載入 DWG 檔案 (load dwg file java)

首先，將 API 指向 DWG（或 DXF）檔案所在位置，並將其載入至 `CadImage` 物件。

```java
// The path to the resource directory.
String dataDir = "Your Document Directory" + "CADConversion/";

String srcFile = dataDir + "conic_pyramid.dxf";
CadImage cadImage = (CadImage) Image.load(srcFile);
```

> **小技巧：** 若直接處理 DWG 檔案，請將 `srcFile` 變數中的 `.dxf` 副檔名改為 `.dwg`。

### 步驟 2：遍歷樣式表並設定主要字型名稱

每個 CAD 圖紙都包含一系列樣式物件。遍歷這些樣式，使用 `setPrimaryFontName` 方法（**設定主要字型名稱**）來替換字型。

```java
for(Object style : cadImage.getStyles())
{
    // Set the font name
    ((com.aspose.cad.fileformats.cad.cadtables.CadStyleTableObject)style).setPrimaryFontName("Arial");
}
```

您可以將 `"Arial"` 改為執行程式的機器上已安裝的任何字型。

### 步驟 3：儲存已修改的圖紙

更新字型後，將變更寫回新的 DWG 檔案（或覆寫原檔）。

```java
cadImage.save(dataDir + "output.dwg", new DwgOptions());
```

儲存後的檔案將使用您指定的字型，所有文字註解皆會以該字型呈現。

## 常見問題與解決方案

| 問題 | 解決方案 |
|-------|----------|
| **字型未套用** | 確認該字型已安裝於主機作業系統，且拼寫完全相符。 |
| **`Image.load` 拋出例外** | 確認檔案路徑正確，且檔案為支援的 DWG/DXF 格式。 |
| **大型檔案效能下降** | 將檔案於獨立執行緒處理，或分批執行以避免 UI 卡頓。 |

## 常見問答

**Q: `setPrimaryFontName` 方法只會影響文字實體嗎？**  
A: 它會更新樣式表的主要字型，進而影響所有參考該樣式的文字物件。

**Q: 可以使用未安裝於系統的自訂字型嗎？**  
A: Aspose.CAD 依賴作業系統的字型註冊表。若要使用自訂字型，必須先將其安裝於執行程式的機器上。

**Q: 能否只為單一圖層變更字型？**  
A: 可以，在呼叫 `setPrimaryFontName` 前，先依圖層名稱過濾樣式。

**Q: 需要哪個版本的 Aspose.CAD 才能支援 DWG 2022 檔案？**  
A: 截至 2025 年的最新版本已完整支援 DWG 2022。請隨時查閱發行說明以確認特定格式支援情況。

**Q: 在開發環境如何處理授權？**  
A: 測試時可使用臨時評估授權。正式環境請使用 `License.setLicense("Aspose.Total.Java.lic");` 內嵌您購買的授權檔。

---

**最後更新：** 2026-05-04  
**測試環境：** Aspose.CAD for Java 24.11  
**作者：** Aspose  

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}