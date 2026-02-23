---
date: 2026-02-23
description: 學習如何使用 Aspose CAD DWG for Java 載入 DWG 檔案並提取底圖標誌 — 為開發人員提供的逐步指南。
linktitle: Accessing Underlay Flags of DWG
second_title: Aspose.CAD Java API
title: aspose cad dwg – 載入 DWG 並存取底圖旗標 (Java)
url: /zh-hant/java/cad-file-manipulation/accessing-underlay-flags-of-dwg/
weight: 11
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# 載入 DWG 檔案並存取底圖旗標 – Aspose.CAD for Java

在現代 CAD 工作流程中，**使用 aspose cad dwg 您可以快速載入 DWG 檔案**，並提取通常對一般檢視者隱藏的底圖細節。無論您是要建立 Java DWG 檢視器、自動化批次處理 dwg 管線，或是為 GIS 整合提取中繼資料，Aspose.CAD for Java 都提供乾淨、以程式碼為先的解決方案。本教學將一步步說明如何**載入 DWG 檔案**、遍歷其實體，並讀取許多開發者常忽略的底圖旗標。

## 快速答覆
- **開啟 DWG 的主要類別是什麼？** `com.aspose.cad.Image.load()` 會回傳 `CadImage`。
- **哪個物件保存底圖資訊？** `CadUnderlay`（或其衍生類型，如 `CadDgnUnderlay`）。
- **開發時需要授權嗎？** 免費試用可用於測試；正式上線需購買商業授權。
- **可以在迴圈中處理多個 DWG 檔案嗎？** 可以，只要重複載入與遍歷的模式即可。
- **此方法相容於 Java 11+ 嗎？** 完全相容，Aspose.CAD 支援 Java 8 直至最新 LTS 版本。

## aspose cad dwg – 載入 DWG 檔案 (Java)

`Image.load()` 會讀取 DWG 的二進位內容，並在記憶體中建立 `CadImage` 物件。之後您即可探索圖層、區塊與底圖實體，而不必自行處理 DWG 檔案格式。

## 為什麼要從 DWG 中提取底圖旗標？

底圖旗標說明外部參照（例如 DGN 或 PDF 底圖）在圖面中的位置、縮放與旋轉方式。取得這些值可讓您：

- 在自訂 **java dwg viewer** 中**重新建立**完全相同的視覺版面。
- 將底圖轉換為原生 CAD 實體以便進一步編輯。
- 產生包含底圖中繼資料的報告，以符合合規或文件需求。
- **批次處理 dwg** 檔案，並將底圖中繼資料儲存至資料庫以供日後分析。

## 前置需求
- **Aspose.CAD Library** – 從 [releases](https://releases.aspose.com/cad/java/) 頁面下載。  
- **Java Development Kit** – JDK 8 或更新版本。  
- **一個資料夾**，內含您要分析的 DWG 檔案。請將程式碼中的 `"Your Document Directory"` 替換為實際路徑。

## 匯入命名空間

```java
import com.aspose.cad.Image;

import com.aspose.cad.fileformats.cad.CadImage;
import com.aspose.cad.fileformats.cad.cadobjects.CadBaseEntity;
import com.aspose.cad.fileformats.cad.cadobjects.CadDgnUnderlay;
import com.aspose.cad.fileformats.cad.cadobjects.CadUnderlay;
import com.aspose.cad.fileformats.cad.cadobjects.UnderlayFlags;
```

## 步驟說明

### 步驟 1：設定資源目錄
```java
// The path to the resource directory.
String dataDir = "Your Document Directory" + "DWGDrawings/";
```
定義 DWG 檔案所在的位置。使用專屬資料夾可讓範例保持簡潔且易於搬移。

### 步驟 2：載入 DWG 檔案
```java
// Input file name and path
String fileName = dataDir + "BlockRefDgn.dwg";

// Load an existing DWG file and convert it into CadImage 
CadImage image = (CadImage)Image.load(fileName);
```
此處**載入 dwg 檔案** `BlockRefDgn.dwg` 成為 `CadImage` 實例，準備進行檢查。

### 步驟 3：遍歷 DWG 實體
```java
// Go through each entity inside the DWG file
for(CadBaseEntity entity : image.getEntities())
```
此迴圈會走訪每一個實體──線條、圓形、區塊與底圖──以便挑選出需要的項目。

### 步驟 4：識別 CadDgnUnderlay 實體
```java
// Check if entity is of CadDgnUnderlay type
if (entity instanceof CadDgnUnderlay)
```
只有 `CadDgnUnderlay` 物件包含我們想要的底圖旗標，因此在此過濾出它們。

### 步驟 5：存取底圖資訊
```java
// Access different underlay flags 
CadUnderlay underlay = (CadUnderlay) entity;
System.out.println(underlay.getUnderlayPath());
System.out.println(underlay.getUnderlayName());
// ... (Additional underlay properties)
break;
```
取得 `CadUnderlay` 後，即可讀取其路徑、名稱、插入點、旋轉角度、縮放比例，以及 `UnderlayFlags` 列舉（顯示、裁切等渲染選項）。

## 如何在批次程序中載入 dwg 檔案

若需**批次處理 dwg** 檔案，只要將上述步驟包在簡單的 `for` 迴圈中，遍歷 `dataDir` 內的所有檔案。每個檔案皆使用相同的 `Image.load()` 呼叫，並可將擷取的旗標寫入 CSV 或資料庫，以供後續報表使用。

## 常見問題與技巧
- **底圖路徑為 null** – 確認 DWG 確實參照了外部檔案，否則路徑會是空的。
- **不支援的底圖類型** – Aspose.CAD 目前僅支援 DGN 底圖，PDF 底圖尚未透過 API 暴露。
- **授權例外** – 未使用有效授權執行程式時，所有匯出影像會加上浮水印。
- **效能技巧**：在批次處理大量檔案時，重複使用同一個 `Image` 實例，可減少 GC 壓力。

## 常見問答

**Q: 可以在 Java 中使用 Aspose.CAD 處理其他 CAD 檔案格式嗎？**  
A: Aspose.CAD 主要聚焦於 DWG 格式，但亦支援 DXF、DWF 及其他 CAD 格式。

**Q: 有提供 Aspose.CAD for Java 的試用版嗎？**  
A: 有，您可從 [here](https://releases.aspose.com/) 取得免費試用。

**Q: 如何取得 Aspose.CAD for Java 的支援或協助？**  
A: 前往 [Aspose.CAD forum](https://forum.aspose.com/c/cad/19) 取得社群支援與討論。

**Q: 是否有臨時授權可供 Aspose.CAD for Java 使用？**  
A: 有，您可在 [here](https://purchase.aspose.com/temporary-license/) 取得臨時授權。

**Q: 哪裡可以找到 Aspose.CAD for Java 的完整文件？**  
A: 請參考 [documentation](https://reference.aspose.com/cad/java/) 取得詳細資訊。

---

**最後更新：** 2026-02-23  
**測試環境：** Aspose.CAD 24.12 for Java  
**作者：** Aspose  

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}