---
date: 2026-03-07
description: 學習如何使用 Aspose.CAD for Java 替換 DWG 檔案中的字型。此一步一步的指南精確展示如何替換特定樣式的字型。
linktitle: Substitute Font of a Particular Style in DWG
second_title: Aspose.CAD Java API
title: 如何使用 Aspose.CAD for Java 在 DWG 中替換特定樣式的字型
url: /zh-hant/java/cad-text-and-annotation/substitute-font-of-particular-style-in-dwg/
weight: 12
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# 如何使用 Aspose.CAD for Java 替換 DWG 中特定樣式的字體

## 介紹

在 CAD（Computer‑Aided Design）領域，精確度與細節至關重要，而 **了解如何替換字體** 能為您節省無數次的重工時間。Aspose.CAD for Java 為開發者提供了一種乾淨、程式化的方式來修改 DWG 檔案，包括變更特定文字樣式的字體。本教學將逐步說明如何在 DWG 檔案中替換特定樣式的字體、說明為何需要這麼做，並示範如何驗證結果。

## 快速答覆
- **「replace font」在 DWG 中是什麼意思？** 更改與文字樣式定義相關聯的主要字體。  
- **哪個函式庫負責此功能？** Aspose.CAD for Java。  
- **需要授權嗎？** 免費試用可用於測試；正式上線需購買商業授權。  
- **可以一次變更多個樣式嗎？** 可以——遍歷樣式集合並為每個樣式設定字體。  
- **程式碼是否相容於 Java 8+？** 完全相容，API 目標為 Java 8 及以上版本。

## 什麼是 DWG 中的字體替換？
字體替換是指更新文字樣式（在 DWG 詞彙中亦稱為「style」）的 *主要字體* 屬性。當圖面引用該樣式時，所有文字會自動採用新字體，確保整個檔案的外觀一致。

## 為什麼要修改 DWG 文字樣式？
- **維持品牌一致性：** 在所有圖面中使用公司字體。  
- **修復缺少字體的問題：** 將無法使用的字體替換為目標系統已安裝的字體。  
- **為列印/繪圖作準備：** 某些繪圖機需要特定字體才能正確輸出。  

## 前置條件

在開始本教學之前，請確保已完成以下設定：

1. **Aspose.CAD for Java Library：** 下載並安裝 Aspose.CAD 函式庫。您可以在此處取得函式庫與文件說明 [here](https://releases.aspose.com/cad/java/)。  
2. **Java Development Kit (JDK)：** 確認您的機器已安裝 Java。

現在您已具備必要工具，讓我們繼續下一節。

## 匯入命名空間（修改 DWG 文字樣式所需）

在 Java 中，匯入正確的命名空間對於使用外部函式庫至關重要。此處請確保匯入必要的 Aspose.CAD 命名空間。以下為範例：

```java
import com.aspose.cad.Image;

import com.aspose.cad.fileformats.cad.CadImage;
```

現在，讓我們將範例程式碼拆解為多個步驟。

## 步驟 1：設定資源目錄

```java
// The path to the resource directory.
String dataDir = "Your Document Directory" + "CADConversion/";
```

將 `"Your Document Directory"` 替換為實際文件目錄的路徑。

## 步驟 2：載入 CAD 圖紙

```java
String srcFile = dataDir + "conic_pyramid.dxf";

// Load a CAD drawing in an instance of CadImage
CadImage cadImage = (CadImage)Image.load(srcFile);
```

請將 `"conic_pyramid.dxf"` 替換為您 CAD 圖紙的實際名稱。

## 步驟 3：為樣式指定字體（變更 DWG 樣式字體）

```java
// Specify the font for one particular style
((CadStyleTableObject)cadImage.getStyles().get_Item(0)).setPrimaryFontName("Arial");
```

根據需求調整字體名稱（本例為 "Arial"）。此行 **設定 DWG 樣式的主要字體**，從而取代舊字體。

## 常見問題與解決方案

| 問題 | 原因 | 解決方案 |
|------|------|----------|
| 儲存後字體未變更 | 修改後未儲存圖紙 | 在設定字體後呼叫 `cadImage.save(outputPath);`。 |
| 字體名稱未被識別 | 執行程式的系統未安裝該字體 | 安裝該字體或使用通用字體名稱（例如 "Tahoma"）。 |
| `ClassCastException` | 從 `get_Item` 取得的物件類型錯誤 | 確保索引指向 `CadStyleTableObject`。 |

## 常見問答

### Q1：我可以在同一個 DWG 檔案中替換多個字體嗎？

A1：可以，您可以遍歷不同的樣式，並為每個樣式分別設定主要字體。

### Q2：我可以使用的字體名稱有沒有上限？

A2：沒有，您可以使用系統上任何有效的字體名稱。

### Q3：我可以撤銷字體替換嗎？

A3：Aspose.CAD 提供彈性；您可以還原變更或將 DWG 檔案另存為不同版本。

### Q4：本教學適用於其他 CAD 格式嗎？

A4：雖然範例以 DWG 為主，但相同原理可套用於其他支援的 CAD 格式。

### Q5：如何取得 Aspose.CAD for Java 的支援？

A5：請前往 [Aspose.CAD 論壇](https://forum.aspose.com/c/cad/19) 取得社群支援與討論。

## 其他常見問題

**Q：如何儲存已修改的圖紙？**  
A：在設定新字體後，呼叫 `cadImage.save(dataDir + "output.dwg");` 將變更寫入新檔案。

**Q：我只能替換註解物件的字體嗎？**  
A：可以，先篩選出與註解相關的樣式，再套用 `setPrimaryFontName`。

**Q：是否可以在不儲存的情況下預覽字體變更？**  
A：可以使用 `cadImage.save(outputStream, new ImageOptions());` 將影像渲染為位圖，於記憶體中預覽。

**Q：Aspose.CAD 是否支援 TrueType 與 OpenType 字體？**  
A：只要字體已安裝於主機作業系統，TrueType（.ttf）與 OpenType（.otf）皆完全支援。

## 常見問答

**Q：此程式碼需要哪個版本的 Aspose.CAD？**  
A：本教學使用的 API 在 Aspose.CAD for Java 24.11 及更新版本中皆可使用。

**Q：我可以在 Linux 伺服器上執行此程式碼嗎？**  
A：可以，只要伺服器上已安裝所需字體且具備 Java 8+ 環境。

**Q：在變更字體前，如何列出所有可用的文字樣式？**  
A：遍歷 `cadImage.getStyles()`，並印出每個樣式的名稱與目前的主要字體。

**Q：是否有辦法批次處理多個 DWG 檔案？**  
A：將邏輯包在迴圈中，依序載入每個檔案、更新目標樣式，最後儲存輸出。

**Q：變更主要字體會影響尺寸或間距嗎？**  
A：字體度量可能不同，變更後可能需要調整文字高度或位置。

## 結論

Aspose.CAD for Java 為 CAD 操作開啟了強大的可能性，而 **如何替換字體** 只是其中一項功能。您可以嘗試不同樣式，使用 *modify DWG text style* 或 *set primary font dwg* 等關鍵詞微調圖面，並將程式碼整合至更大型的自動化流程中，以實現批次處理。

---

**最後更新：** 2026-03-07  
**測試環境：** Aspose.CAD for Java 24.11  
**作者：** Aspose  

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}