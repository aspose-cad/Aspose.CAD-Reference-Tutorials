---
date: 2025-12-28
description: 學習如何使用 Aspose.CAD for Java 在 DWG 圖紙中自訂字型。一步一步的指南，教您加入文字、替換字型，並完善 CAD
  註解。
linktitle: CAD Text and Annotation
second_title: Aspose.CAD Java API
title: 如何在 CAD 文字與註釋中自訂字型
url: /zh-hant/java/cad-text-and-annotation/
weight: 21
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# 如何在 CAD 文字與註釋中自訂字型

## 簡介

如果你想在 DWG 圖紙中 **how to customize fonts**，你來對地方了。在本教學中，我們將逐步說明如何使用 Aspose.CAD for Java 新增文字、取代字型，以及微調字型樣式。無論你是在潤飾原理圖、準備施工文件，或只是想要更清晰的 **dwg text annotation**，這些步驟都能協助你快速且可靠地達成專業的效果。

## 快速答覆
- **在 DWG 中自訂字型的主要目的為何？** 提升可讀性，並符合品牌或專案標準。  
- **哪個函式庫負責處理變更？** Aspose.CAD for Java。  
- **我需要授權嗎？** 免費試用可用於評估；正式上線需購買商業授權。  
- **我可以處理大型 DWG 檔案嗎？** 可以 — API 會有效率地串流資料，適用於大型圖紙。  
- **需要額外的軟體嗎？** 只需 Java 執行環境 (JDK 8 或更新版) 以及 Aspose.CAD JAR。  

## 什麼是 CAD 中的 “how to customize fonts”？
自訂字型是指將 DWG 檔案中的預設文字樣式替換為您選擇的字型，並調整其大小、粗細，或對特定圖層或物件套用不同的樣式。這可確保圖紙在所有檢視器中皆呈現您預期的外觀。

## 為何使用 Aspose.CAD for Java 來自訂字型？
- **完整控制** 文字物件，而無需在 GUI 編輯器中開啟圖紙。  
- **批次處理** — 在單一腳本中處理數十個檔案。  
- **跨平台** — 可在 Windows、Linux 與 macOS 上執行。  
- **無外部相依性** — API 內部管理 DWG 解析。  

## 先決條件
- 已安裝 Java Development Kit 8 或更新版本。  
- 已將 Aspose.CAD for Java JAR 加入專案的 classpath。  
- 一個您想編輯的 DWG 檔案。  

## 如何在 DWG 中新增文字
在需要為零件加標籤、加入說明或建立 **dwg text annotation** 時，新增文字資訊是常見需求。請依照以下步驟操作：

1. **載入 DWG 檔案** using `CadImage`。  
2. **建立 `CadText` 實體** with the desired string, location, and font.  
3. **將實體加入** to the drawing’s entities collection。  
4. **儲存** the modified file。

> *注意：實際程式碼片段與原始教學相同，已包含於連結的子教學中。*  

## 如何在 DWG 中取代字型
在整個圖紙中取代既有字型有助於保持一致性特別是當原始字型在目標系統上不可用時。

1. **開啟 DWG** with `CadImage`。  
2. **遍歷** over all `CadText` objects。  
3. **設定 `FontName` 屬性** to your preferred font (e.g., “Arial”)。  
4. **儲存** the updated drawing。

此方法於「Substitute Font in DWG」子教學中有詳細說明。

## 如何變更特定樣式的 DWG 字型樣式
有時僅有特定文字樣式（例如「Title」）需要新字型，而其他樣式保持不變。

1. **識別欲修改的樣式名稱** you want to modify。  
2. **找到相對應的 `CadTextStyle` 物件**。  
3. **更新其 `FontName`** and any additional style attributes。  
4. **持久化變更** by saving the file。

步驟說明可於「Substitute Font of a Particular Style in DWG」子教學中取得。

## 常見使用情境
- **施工圖紙** where company‑standard fonts are mandatory。  
- **建築平面圖** that need legible annotations for clients。  
- **批次轉換** of legacy DWG files to a new corporate font set。  

## CAD 文字與註釋教學
### [使用 Aspose.CAD for Java 在 DWG 中新增文字](./add-text-in-dwg/)
使用 Aspose.CAD for Java 輕鬆提升您的 DWG 圖紙。透過我們的步驟指南無縫新增文字。

### [使用 Aspose.CAD for Java 在 DWG 中取代字型](./substitute-font-in-dwg/)
輕鬆提升您的 CAD 設計。學習使用 Aspose.CAD for Java 在 DWG 檔案中取代字型。提供視覺完美的步驟指南。

### [使用 Aspose.CAD for Java 在 DWG 中取代特定樣式的字型](./substitute-font-of-particular-style-in-dwg/)
了解如何使用 Aspose.CAD for Java 在 DWG 檔案中取代字型。提供精確自訂樣式的步驟指南。

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}

## 常見問題

**Q: 我可以將這些方法用於較舊 AutoCAD 版本所建立的 DWG 檔案嗎？**  
A: 可以。Aspose.CAD 支援從 R12 到最新版本的 DWG。

**Q: 如果目標字型未安裝在檢視者的機器上會發生什麼情況？**  
A: 圖紙會回退至預設字型，可能影響版面配置。建議嵌入字型或確保所有機器皆已安裝該字型。

**Q: 是否只能在特定圖層上取代字型？**  
A: 當然可以。在變更 `FontName` 前，先依 `LayerName` 篩選 `CadText` 物件。

**Q: 在字型變更後需要重新建構圖紙嗎？**  
A: 不需要手動重新建構；儲存 `CadImage` 即會寫入所有更新至檔案。

**Q: 如何驗證字型變更已正確套用？**  
A: 在任何支援該字型的檢視器中開啟 DWG，或以程式方式列舉 `CadText` 物件以讀取 `FontName`。

---

**最後更新：** 2025-12-28  
**測試環境：** Aspose.CAD for Java 24.12  
**作者：** Aspose