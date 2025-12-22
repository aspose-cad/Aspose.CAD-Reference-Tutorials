---
date: 2025-12-22
description: 學習如何使用 Aspose.CAD for Java 載入 DWG 檔案並提取底圖資訊——一步一步的指南，涵蓋底圖旗標。
linktitle: Accessing Underlay Flags of DWG
second_title: Aspose.CAD Java API
title: 載入 DWG 檔案並存取底圖標誌 – Aspose.CAD for Java
url: /zh-hant/java/cad-file-manipulation/accessing-underlay-flags-of-dwg/
weight: 11
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# 載入 DWG 檔案與存取底圖旗標 – Aspose.CAD for Java

在現代 CAD 工作流程中，快速 **載入 DWG 檔案** 並提取底圖細節是一項常見需求。無論您是建立檢視器、自动化批次處理，或是為 GIS 整合提取中繼資料，Aspose.CAD for Java 都提供乾淨、以程式碼為先的方式來完成。於本教學中，我們將逐步說明 **載入 DWG 檔案**、遍歷其實體，並讀取許多開發者常忽略的底圖旗標。

## 快速解答
- **開啟 DWG 的主要類別是什麼？** `com.aspose.cad.Image.load()` 會回傳 `CadImage`。
- **哪個物件保存底圖資訊？** `CadUnderlay`（或其衍生類型，如 `CadDgnUnderlay`）。
- **開發是否需要授權？** 免費試用版可用於測試；正式環境需購買商業授權。
- **可以在迴圈中處理多個 DWG 檔案嗎？** 可以，只要重複載入與遍歷的模式即可。
- **此方法是否相容於 Java 11 以上？** 完全相容，Aspose.CAD 支援 Java 8 直至最新的 LTS 版本。

## 在 Aspose.CAD 中「載入 DWG 檔案」是什麼？
`Image.load()` 會讀取 DWG 的二進位內容，並建立一個記憶體中的 `CadImage` 物件。之後您可以探索圖層、區塊與底圖實體，而不必自行處理 DWG 檔案格式。

## 為何要從 DWG 中提取底圖旗標？
底圖旗標說明外部參考（例如 DGN 或 PDF 底圖）在圖面中的位置、縮放與旋轉方式。了解這些數值可讓您：
- 在自訂檢視器中重新建立完全相同的視覺版面。
- 將底圖轉換為原生 CAD 實體，以便進一步編輯。
- 產生包含底圖中繼資料的報告，以符合合規或文件需求。

## 前置條件
- **Aspose.CAD Library** – 從 [releases](https://releases.aspose.com/cad/java/) 頁面下載。
- **Java Development Kit** – JDK 8 或更新版本。
- **資料夾**，內含您要分析的 DWG 檔案。請在程式碼中將 `"Your Document Directory"` 替換為實際路徑。

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
定義 DWG 檔案所在的位置。使用專屬資料夾可讓範例保持整潔且易於搬移。

### 步驟 2：載入 DWG 檔案
```java
// Input file name and path
String fileName = dataDir + "BlockRefDgn.dwg";

// Load an existing DWG file and convert it into CadImage 
CadImage image = (CadImage)Image.load(fileName);
```
此處我們 **載入 dwg 檔案** `BlockRefDgn.dwg` 成為 `CadImage` 實例，準備進行檢查。

### 步驟 3：遍歷 DWG 實體
```java
// Go through each entity inside the DWG file
for(CadBaseEntity entity : image.getEntities())
```
此迴圈會走訪每個實體──線條、圓形、區塊與底圖──以便挑選出我們需要的項目。

### 步驟 4：識別 CadDgnUnderlay 實體
```java
// Check if entity is of CadDgnUnderlay type
if (entity instanceof CadDgnUnderlay)
```
只有 `CadDgnUnderlay` 物件包含我們想要的底圖旗標，因此我們會過濾出這類物件。

### 步驟 5：存取底圖資訊
```java
// Access different underlay flags 
CadUnderlay underlay = (CadUnderlay) entity;
System.out.println(underlay.getUnderlayPath());
System.out.println(underlay.getUnderlayName());
// ... (Additional underlay properties)
break;
```
取得 `CadUnderlay` 後，我們即可讀取其路徑、名稱、插入點、旋轉角度、縮放係數，以及表示可見性、裁切與其他渲染選項的 `UnderlayFlags` 列舉。

## 常見問題與技巧
- **底圖路徑為 null** – 確認 DWG 確實參考了外部檔案；否則路徑會是空的。
- **不支援的底圖類型** – 目前 Aspose.CAD 僅支援 DGN 底圖；PDF 底圖尚未透過 API 暴露。
- **授權例外** – 若未使用有效授權執行程式，所有匯出的影像都會加上浮水印。

## 常見問答

**Q: 我可以在 Java 中使用 Aspose.CAD 處理其他 CAD 檔案格式嗎？**  
A: Aspose.CAD 主要聚焦於 DWG 格式，但也支援 DXF、DWF 以及其他 CAD 格式。

**Q: 是否提供 Aspose.CAD for Java 的試用版？**  
A: 有的，您可從 [此處](https://releases.aspose.com/) 取得免費試用版以探索功能。

**Q: 如何取得 Aspose.CAD for Java 的支援或協助？**  
A: 請前往 [Aspose.CAD 論壇](https://forum.aspose.com/c/cad/19) 獲取社群支援與討論。

**Q: 是否提供 Aspose.CAD for Java 的臨時授權？**  
A: 有的，您可在 [此處](https://purchase.aspose.com/temporary-license/) 取得臨時授權。

**Q: 在哪裡可以找到 Aspose.CAD for Java 的完整文件？**  
A: 請參考 [文件說明](https://reference.aspose.com/cad/java/) 以取得詳細資訊。

---

**最後更新：** 2025-12-22  
**測試版本：** Aspose.CAD 24.12 for Java  
**作者：** Aspose  

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}