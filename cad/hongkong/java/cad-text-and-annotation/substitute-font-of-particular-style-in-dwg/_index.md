---
date: 2026-01-02
description: 學習如何使用 Aspose.CAD for Java 替換 DWG 檔案中的字型。一步一步的指南，精準自訂樣式。
linktitle: Substitute Font of a Particular Style in DWG
second_title: Aspose.CAD Java API
title: 如何在 DWG 中使用 Aspose.CAD for Java 替換特定樣式的字體
url: /zh-hant/java/cad-text-and-annotation/substitute-font-of-particular-style-in-dwg/
weight: 12
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# 如何在 DWG 中使用 Aspose.CAD for Java 替換特定樣式的字體

## 簡介

在 CAD（Computer-Aided Design）領域，精確與細節至關重要，**了解如何替換字體** 能為您節省大量重新製作的時間。Aspose.CAD for Java 為開發者提供一種乾淨、程式化的方式來修改 DWG 檔案，包括變更特定文字樣式的字體。本教學將逐步說明如何在 DWG 檔案中替換特定樣式的字體、說明為何需要這麼做，並示範如何驗證結果。

## 快速解答
- **「replace font」在 DWG 中是什麼意思？** 更改與文字樣式定義相關聯的主要字體。  
- **哪個函式庫負責此功能？** Aspose.CAD for Java。  
- **我需要授權嗎？** 免費試用可用於測試；正式上線需購買商業授權。  
- **可以一次變更多個樣式嗎？** 可以——遍歷樣式集合並為每個樣式設定字體。  
- **程式碼是否相容於 Java 8 以上？** 完全相容，API 目標為 Java 8 及更新版本。

## 什麼是 DWG 中的字體替換？
字體替換指的是更新文字樣式（在 DWG 詞彙中亦稱為「style」）的*主要字體*屬性。當圖面引用該樣式時，所有文字會自動套用新字體，確保整個檔案的外觀保持一致。

## 為什麼要修改 DWG 文字樣式？
- **維持品牌一致性：** 在所有圖面中使用公司字體。  
- **修復缺失字體：** 將無法使用的字體替換為目標系統已安裝的字體。  
- **為列印/繪圖做準備：** 某些繪圖機需要特定字體才能正確輸出。  

## 前提條件

在開始本教學之前，請先確保已完成以下設定：

1. **Aspose.CAD for Java Library：** 下載並安裝 Aspose.CAD 函式庫。您可以在 [此處](https://releases.aspose.com/cad/java/) 找到函式庫與相關文件。  
2. **Java Development Kit (JDK)：** 確認您的機器已安裝 Java。

現在您已具備必要工具，請繼續下一節。

## 匯入命名空間（修改 DWG 文字樣式的必要步驟）

在 Java 中，正確匯入命名空間對於使用外部函式庫至關重要。此處請確保匯入所需的 Aspose.CAD 命名空間。以下為範例程式碼：

```java
import com.aspose.cad.Image;

import com.aspose.cad.fileformats.cad.CadImage;
```

現在，我們將範例程式碼拆解為多個步驟。

## 步驟 1：設定資源目錄

```java
// The path to the resource directory.
String dataDir = "Your Document Directory" + "CADConversion/";
```

將 `"Your Document Directory"` 替換為您實際的文件目錄路徑。

## 步驟 2：載入 CAD 圖紙

```java
String srcFile = dataDir + "conic_pyramid.dxf";

// Load a CAD drawing in an instance of CadImage
CadImage cadImage = (CadImage)Image.load(srcFile);
```

請將 `"conic_pyramid.dxf"` 替換為您 CAD 圖面的實際檔名。

## 步驟 3：指定樣式字體（變更 DWG 樣式字體）

```java
// Specify the font for one particular style
((CadStyleTableObject)cadImage.getStyles().get_Item(0)).setPrimaryFontName("Arial");
```

依需求調整字體名稱（本例為 "Arial"）。此行 **設定 DWG 樣式的主要字體**，即完成舊字體的替換。

## 常見問題及解決方案

| 問題 | 原因 | 解決方案 |

|-------|-------|----------|

| 儲存後字型未更改 | 修改後圖形未儲存 | 設定字型後呼叫 `cadImage.save(outputPath);`。 |

| 字體名稱無法辨識 | 程式碼運作所在的系統未安裝該字體 | 安裝該字體或使用通用字體名稱（例如，「Tahoma」）。 |

| `ClassCastException` | `get_Item` 傳回的物件類型錯誤 | 確保索引指向 `CadStyleTableObject`。 |

## 常見問題解答

### 問題 1：我可以在一個 DWG 檔案中替換多種字體嗎？

回答 1：可以，您可以遍歷不同的樣式，並分別設定每種樣式的主字體。

### 問題 2：我可以使用的字體名稱有限制嗎？

A2：不，您可以使用系統上任何有效的字體名稱。

### Q3：我可以撤銷字型替換嗎？

A3：Aspose.CAD 提供了彈性；您可以撤銷更改或儲存不同版本的 DWG 檔案。

### Q4：本教學是否適用於其他 CAD 格式？

A4：雖然範例著重於 DWG，但類似的原理也適用於其他支援的 CAD 格式。

### Q5：如何獲得 Aspose.CAD for Java 的支援？

A5：請造訪 [Aspose.CAD 論壇](https://forum.aspose.com/c/cad/19) 以取得社群支持與討論。

## 其他常見問題

**問：如何儲存修改後的圖形？ ** 答：設定新字型後，呼叫 `cadImage.save(dataDir + "output.dwg");` 將變更寫入新檔案。

**問：我能否只替換註解物件的字體？ ** 答：可以，在套用 `setPrimaryFontName` 之前，請先篩選樣式集合中與註解相關的樣式。

**問：能否在不儲存的情況下預覽字體變更？ ** 答：您可以使用 `cadImage.save(outputStream, new ImageOptions());` 將影像渲染為點陣圖，以便在記憶體中預覽。

**問：Aspose.CAD 是否支援 TrueType 和 OpenType 字型？ ** 答：只要主機作業系統上安裝了 TrueType (.ttf) 和 OpenType (.otf) 字體，Aspose.CAD 都完全支援它們。

＃＃ 結論

Aspose.CAD for Java 為 CAD 操作開啟了強大的可能性，而 **如何取代字體** 只是其中一項功能。您可以嘗試不同的樣式，使用次要關鍵字如 *修改 DWG 文字樣式* 或 *設定主字體 dwg* 進一步進一步圖面，把程式流程整合至更大的自動化，以實現批次處理。

---

**最後更新：** 2026-01-02
**測試使用：** Aspose.CAD for Java 24.11
**作者：** 阿斯普斯  

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}