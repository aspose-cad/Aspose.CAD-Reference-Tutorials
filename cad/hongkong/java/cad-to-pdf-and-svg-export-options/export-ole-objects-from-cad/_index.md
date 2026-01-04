---
date: 2026-01-04
description: 學習如何將 CAD 另存為 PNG，並使用 Aspose.CAD for Java 輕鬆匯出 CAD 檔案中的 OLE 物件。快速設定、完整程式碼範例與最佳實踐技巧。
linktitle: Export OLE Objects from CAD
second_title: Aspose.CAD Java API
title: 使用 Aspose.CAD for Java 將 CAD 儲存為 PNG 並匯出 OLE 物件
url: /zh-hant/java/cad-to-pdf-and-svg-export-options/export-ole-objects-from-cad/
weight: 10
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# 將 CAD 儲存為 PNG 並匯出 OLE 物件（使用 Aspose.CAD for Java）

## 介紹

在快速變化的電腦輔助設計（CAD）領域，能夠 **將 CAD 儲存為 PNG** 同時擷取內嵌的 OLE（Object Linking and Embedding）物件，能大幅簡化工作流程。無論您是要建立批次轉換工具、為網站入口產生縮圖，或只是需要歸檔 OLE 內容，Aspose.CAD for Java 都提供乾淨且程式化的解決方案。本教學將從專案設定一步步說明，直到將每個 OLE 物件匯出為 PNG 圖片。

## 快速答覆
- **可以直接將 OLE 物件匯出為 PNG 嗎？** 可以 – Aspose.CAD 會載入 CAD 檔案，並讓您將每個版面光柵化為 PNG。  
- **需要哪個版本的 Java？** Java 8 或更新版本。  
- **此功能需要授權嗎？** 評估可使用免費試用版；正式環境需購買授權。  
- **向量資料會被保留嗎？** PNG 光柵化保留視覺相似度，但輸出為點陣圖，非向量。  
- **支援批次處理嗎？** 完全支援 – 如程式碼範例所示，可遍歷檔案陣列。

## 前置條件

在開始之前，請確保您已具備以下項目：

- **Java Development Kit (JDK)** – 已安裝並設定 Java 8 以上。  
- **Aspose.CAD for Java** – 從[下載連結](https://releases.aspose.com/cad/java/)取得最新程式庫。  
- **CAD 原始檔** – 任意包含 OLE 物件的 DWG/DXF/DGN 檔案。

## 匯入命名空間

使用 CAD 檔案前，需要匯入 Aspose.CAD 的核心類別。請保持以下匯入區塊原樣不變，因為稍後的教學會用到這些類別。

```java
import com.aspose.cad.Image;

import com.aspose.cad.fileformats.cad.CadImage;
import com.aspose.cad.imageoptions.CadRasterizationOptions;
import com.aspose.cad.imageoptions.PngOptions;
```

## 如何將 CAD 儲存為 PNG

以下提供簡潔的逐步指南，說明 **如何匯出 OLE 物件並將 CAD 儲存為 PNG**。每一步都有簡短說明，並附上可直接複製到專案中的程式碼。

### 步驟 1：設定文件目錄

指定存放 CAD 圖紙的資料夾。將佔位字串替換為您機器上的實際路徑。

```java
String dataDir = "Your Document Directory" + "DWGDrawings/";
```

### 步驟 2：定義 CAD 檔案名稱

列出所有要處理的 CAD 檔案。可依需求自行增減項目。

```java
String[] files = new String[] { "D ZD junior D10m H2m.dwg", "ZD - Senior D6m H2m45.dwg" };
```

### 步驟 3：設定 PNG 匯出選項

配置光柵化設定。此範例以特定版面 (`Layout1`) 為目標，並使用預設的 PNG 選項。

```java
PngOptions pngOptions = new PngOptions();
CadRasterizationOptions rasterizationOptions = new CadRasterizationOptions();
pngOptions.setVectorRasterizationOptions(rasterizationOptions);
rasterizationOptions.setLayouts(new String[] { "Layout1" });
```

### 步驟 4：遍歷 CAD 檔案並儲存為 PNG

載入每個 CAD 檔案、光柵化 OLE 物件，並寫入 PNG 檔案。`_out.png` 後綴可協助辨識產生的圖像。

```java
for(String file : files)
{
    CadImage cadImage = (CadImage)Image.load(dataDir + file);
    cadImage.save(dataDir + file + "_out.png", pngOptions);
}
```

## 常見問題與解決方案

| 問題 | 為何會發生 | 解決方式 |
|------|------------|----------|
| **`Image.load` 拋出 `FileNotFoundException`** | `dataDir` 路徑錯誤或檔名拼寫有誤。 | 再次確認目錄字串，並確保檔名完全相符（含空格）。 |
| **輸出的 PNG 為空白** | 版面名稱在來源 CAD 檔案中不存在。 | 使用 `cadImage.getLayouts()` 列出可用版面，然後更新 `rasterizationOptions.setLayouts(...)`。 |
| **大型 CAD 檔案導致 OutOfMemoryError** | 高解析度光柵化會消耗大量堆積記憶體。 | 增加 JVM 堆積 (`-Xmx2g`) 或降低解析度，方法是 `rasterizationOptions.setResolution(...)`。 |

## 常見問答

### Q1：Aspose.CAD 是否相容所有 CAD 檔案格式？

A1：Aspose.CAD 支援多種 CAD 格式，包括 DWG、DXF 與 DGN。完整支援清單請參閱[文件說明](https://reference.aspose.com/cad/java/)。

### Q2：我可以自訂 OLE 物件的匯出設定嗎？

A2：可以，Aspose.CAD 提供豐富的選項讓您依需求調整匯出設定。

### Q3：Aspose.CAD 有提供免費試用嗎？

A3：有，您可從[此處](https://releases.aspose.com/)取得免費試用版，體驗其功能。

### Q4：哪裡可以取得 Aspose.CAD 的社群支援？

A4：請前往[Aspose.CAD 論壇](https://forum.aspose.com/c/cad/19)加入討論，尋求協助或分享經驗。

### Q5：如何購買 Aspose.CAD 的授權？

A5：請造訪[購買頁面](https://purchase.aspose.com/buy)選擇符合您開發需求的授權方案。

## 結論

依照上述五個簡單步驟，您即可 **將 CAD 儲存為 PNG** 並以少量 Java 程式碼擷取所有內嵌 OLE 物件。此方法特別適合批次轉換、自動化報表或任何需要 CAD 內容點陣圖而不想手動匯出的情境。歡迎自行嘗試不同的光柵化參數，以符合品質與效能需求。

---

**最後更新：** 2026-01-04  
**測試環境：** Aspose.CAD for Java 24.12（撰寫時的最新版本）  
**作者：** Aspose  

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}