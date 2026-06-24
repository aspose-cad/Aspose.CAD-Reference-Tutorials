---
date: 2026-04-23
description: 學習如何使用 Aspose.CAD for Java 自訂 DWG 字型、變更 DWG 文字樣式以及執行 DWG 字型替換。DWG 文字註釋逐步指南。
keywords:
- customize fonts dwg
- change dwg text style
- dwg font substitution
- update dwg text style
- dwg text annotation
linktitle: CAD文字與註釋
second_title: Aspose.CAD Java API
title: 如何在 CAD 文本與註釋中自訂 DWG 字型
url: /zh-hant/java/cad-text-and-annotation/
weight: 21
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# 如何在 CAD 文字與註解中自訂 DWG 字型

## 介紹  

如果您需要快速且以程式方式 **customize fonts dwg** 檔案，您來對地方了。在本教學中，我們將示範如何使用 Aspose.CAD for Java 為 DWG 圖面新增文字、取代現有字型，以及微調字型樣式。無論是潤飾原理圖、準備施工文件，或只是想要更清晰的 **dwg text annotation**，這些步驟都能讓您以最小的麻煩獲得專業的效果。

## 快速解答
- **什麼是自訂 DWG 字型的主要好處？** 提升可讀性，並確保圖面符合公司品牌形象。  
- **哪個函式庫負責這些變更？** Aspose.CAD for Java 提供完整功能的 API。  
- **生產環境使用是否需要授權？** 免費試用版可用於評估；部署時需購買商業授權。  
- **API 能處理大型 DWG 檔案嗎？** 能——它有效率地串流資料，適用於大型圖面。  
- **是否需要額外軟體？** 只需 Java 執行環境（JDK 8 或更新版本）與 Aspose.CAD JAR。  

## 什麼是「customize fonts dwg」？  
「customize fonts dwg」指的是將 DWG 檔案中的預設文字樣式替換為您選擇的字型，並調整其大小、粗細，或對特定圖層或物件套用不同樣式。這可確保在所有檢視器與平台上呈現一致的外觀。

## 為何使用 Aspose.CAD for Java 來自訂字型？  
- **完整程式化控制** — 無需開啟圖形介面編輯器即可修改文字。  
- **批次處理** — 在單一腳本中處理數十個檔案。  
- **跨平台** — 可在 Windows、Linux 與 macOS 上執行。  
- **無外部相依性** — API 內部解析 DWG，無需安裝 AutoCAD。  

## 前置條件
- 已安裝 Java Development Kit 8 或更新版本。  
- 已將 Aspose.CAD for Java JAR 加入專案的 classpath。  
- 欲編輯的 DWG 檔案。  

## 如何在 DWG 中新增文字  
在需要為零件加標籤、加入註解或建立 **dwg text annotation** 時，新增文字資訊是常見需求。請依照以下步驟：

1. 使用 `CadImage` **載入 DWG 檔案**。  
2. **建立 `CadText` 實體**，設定所需的字串、位置與字型。  
3. **將該實體加入** 圖面的實體集合中。  
4. **儲存** 修改後的檔案。  

> *注意：實際程式碼片段與原始教學相同，已包含於連結的子教學中。*  

## 如何在 DWG 中取代字型  
在整個圖面中取代現有字型有助於維持一致性，特別是當原始字型在目標系統上不可用時。

1. 使用 `CadImage` **開啟 DWG**。  
2. **遍歷** 所有 `CadText` 物件。  
3. **設定 `FontName` 屬性** 為您偏好的字型（例如 “Arial”）。  
4. **儲存** 更新後的圖面。  

此方法在「Substitute Font in DWG」子教學中有詳細說明。

## 如何為特定樣式變更 DWG 字型樣式  
有時僅需為特定文字樣式（例如 “Title”）更換字型，而其他樣式保持不變。

1. **辨識** 您想要修改的樣式名稱。  
2. **找到對應的 `CadTextStyle` 物件**。  
3. **更新其 `FontName`** 以及其他樣式屬性。  
4. **儲存檔案** 以永久套用變更。  

逐步指南可在「Substitute Font of a Particular Style in DWG」子教學中取得。

## 常見使用情境
- **建築圖面**：必須使用公司標準字型。  
- **建築平面圖**：需要為客戶提供易讀的註解。  
- **批次轉換**：將舊有 DWG 檔案批量轉換為新的公司字型套件。  

## CAD 文字與註解教學
### [使用 Aspose.CAD for Java 在 DWG 中新增文字](./add-text-in-dwg/)
輕鬆提升您的 DWG 圖面，使用 Aspose.CAD for Java。依循步驟指南無縫新增文字。

### [使用 Aspose.CAD for Java 替換 DWG 中的字型](./substitute-font-in-dwg/)
輕鬆提升您的 CAD 設計。學習如何使用 Aspose.CAD for Java 在 DWG 檔案中替換字型。步驟指南助您達成視覺完美。

### [使用 Aspose.CAD for Java 替換 DWG 中特定樣式的字型](./substitute-font-of-particular-style-in-dwg/)
學習如何使用 Aspose.CAD for Java 在 DWG 檔案中替換特定樣式的字型。精準的步驟指南助您自訂樣式。

## 常見問題

**Q: 我可以在較舊 AutoCAD 版本建立的 DWG 檔案上使用這些方法嗎？**  
**A:** 是的。Aspose.CAD 支援從 R12 到最新版本的 DWG 檔案。

**Q: 如果目標字型未安裝在檢視者的機器上會發生什麼情況？**  
**A:** 圖面會退回使用預設字型，可能會影響版面配置。建議嵌入字型或確保所有機器皆已安裝該字型。

**Q: 能否僅在特定圖層上取代字型？**  
**A:** 絕對可以。在變更 `FontName` 前，先依 `LayerName` 篩選 `CadText` 物件。

**Q: 在字型變更後需要重新建構圖面嗎？**  
**A:** 不需要手動重新建構；儲存 `CadImage` 後會將所有更新寫入檔案。

**Q: 如何驗證字型變更已正確套用？**  
**A:** 在支援該字型的任何檢視器中開啟 DWG，或以程式方式列舉 `CadText` 物件以讀取 `FontName`。

---

**最後更新：** 2026-04-23  
**測試環境：** Aspose.CAD for Java 24.12  
**作者：** Aspose

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}