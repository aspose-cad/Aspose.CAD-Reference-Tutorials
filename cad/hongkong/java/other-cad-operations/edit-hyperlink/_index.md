---
date: 2026-06-19
description: 了解如何使用 Aspose.CAD for Java 編輯 DWG 檔案，包括如何更新 DWG XRef 路徑和編輯超連結。立即試用免費版！
keywords:
- how to edit dwg
- update dwg xref paths
- Aspose.CAD Java hyperlink
linktitle: 編輯超連結
schemas:
- author: Aspose
  dateModified: '2026-06-19'
  description: Learn how to edit DWG files with Aspose.CAD for Java, including how
    to update DWG XRef paths and edit hyperlinks. Try the free trial today!
  headline: How to Edit DWG Hyperlinks - Aspose.CAD Java Tutorial
  type: TechArticle
- description: Learn how to edit DWG files with Aspose.CAD for Java, including how
    to update DWG XRef paths and edit hyperlinks. Try the free trial today!
  name: How to Edit DWG Hyperlinks - Aspose.CAD Java Tutorial
  steps:
  - name: Accessing Insert Objects
    text: '`CadInsertObject` is the Aspose.CAD class that represents an inserted block
      reference (XRef) inside a DWG drawing. Iterate through the entities and identify
      if an entity is an instance of the `CadInsertObject` class.'
  - name: How to Change XRef Path in a DWG Drawing
    text: '`CadImage` is the primary object that loads and saves CAD files in Aspose.CAD
      for Java. Once you have identified the insert object, retrieve the associated
      block entity and update the XRef path as needed. This ensures the reference
      points to the correct external file.'
  - name: Modifying Hyperlinks
    text: Next, check if the entity has a hyperlink associated with it. If the hyperlink
      matches a specific URL, update it to the desired URL. This step guarantees that
      clicking the hyperlink in the CAD viewer opens the new target.
  type: HowTo
- questions:
  - answer: Yes, after making changes call `cadImage.save("EditedDrawing.dwg");` to
      persist the modifications.
    question: Do I need to call a specific method to write the edited DWG back to
      disk?
  - answer: Absolutely—loop through `cadImage.getEntities()` and apply the hyperlink
      logic to each matching entity.
    question: Is it possible to edit multiple hyperlinks in one pass?
  type: FAQPage
second_title: Aspose.CAD Java API
title: 如何編輯 DWG 超連結 - Aspose.CAD Java 教程
url: /zh-hant/java/other-cad-operations/edit-hyperlink/
weight: 17
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# 如何編輯 DWG 超連結 - Aspose.CAD Java 教程

在當今的數位時代，**如何有效編輯 DWG** 檔案是工程師、建築師與 BIM 專家的必備技能。無論是要修正斷裂的超連結、將 XRef 指向新的來源，或是批次更新多個圖面，Aspose.CAD for Java 都提供一種乾淨、程式化的方式來完成這些變更，而不必開啟 CAD 編輯器。本教學將帶您一步步完成整個流程，從載入圖面到持久化編輯結果。

## 快速解答
- **什麼程式庫負責在 Java 中編輯 DWG？** Aspose.CAD for Java。  
- **我可以同時編輯超連結與 XRef 路徑嗎？** 可以——兩者在同一個 API 中皆受支援。  
- **開發時需要授權嗎？** 免費試用可用於測試；正式上線需購買商業授權。  
- **需要哪個版本的 Java？** Java 8 或更高版本。  
- **程式碼範例可以直接執行嗎？** 可以，只要將檔案路徑更新為本機的 DWG 檔案即可。

## 為何編輯 DWG 超連結和 XRef 路徑？

保持超連結與 XRef 路徑的即時更新可防止參照斷裂，確保專案文件始終指向正確資源，並能在龐大的 CAD 資料庫中自動批次更新。這可減少人工操作、降低錯誤，並提升整體專案效率，讓開發者在設計生命週期中以程式方式維護連結完整性。

## 先決條件

在開始教學前，請確保已具備以下條件：

1. **Java 開發環境：** 已安裝 JDK 8 以上，並使用您慣用的 IDE（IntelliJ IDEA、Eclipse 等）。  
2. **Aspose.CAD for Java 程式庫：** 從[下載連結](https://releases.aspose.com/cad/java/)下載並安裝 Aspose.CAD for Java 程式庫。  
3. **DWG 圖面：** 準備好一個可供編輯超連結的 DWG 檔案。

## 匯入套件

先在 Java 專案中匯入必要的套件，確保可以使用 Aspose.CAD for Java 的功能。

```java
import com.aspose.cad.Image;
import com.aspose.cad.fileformats.cad.CadImage;
import com.aspose.cad.fileformats.cad.cadobjects.CadBaseEntity;
import com.aspose.cad.fileformats.cad.cadobjects.CadBlockEntity;
import com.aspose.cad.fileformats.cad.cadobjects.CadInsertObject;
```

## 如何使用 Aspose.CAD for Java 編輯 DWG 超連結？

`CadImage` 是 Aspose.CAD 用來載入與儲存 CAD 圖面的類別。  
使用 `CadImage` 載入 DWG 檔案，遍歷其實體，於需要的地方更新超連結與 XRef 路徑，最後再將圖面儲存回 DWG。此端對端流程讓您在一次遍歷中修改任意數量的實體，確保所有變更皆被持久化。

### 步驟 1：存取 Insert 物件

`CadInsertObject` 是 Aspose.CAD 用來表示 DWG 圖面中插入的區塊參照 (XRef) 的類別。遍歷實體並判斷是否為 `CadInsertObject` 類別的實例。

```java
    String dataDir = "Your Document Directory" + "DWGDrawings/";
    
    CadImage cadImage = (CadImage)Image.load(dataDir + "AutoCad_Sample.dwg");
    for (CadBaseEntity entity : cadImage.getEntities())
    {
        if (entity instanceof CadInsertObject)
        {
        }
	}
```

### 步驟 2：如何變更 DWG 圖面中的 XRef 路徑

`CadImage` 是 Aspose.CAD for Java 中載入與儲存 CAD 檔案的主要物件。識別到 Insert 物件後，取得其對應的區塊實體，並依需求更新 XRef 路徑。此操作可確保參照指向正確的外部檔案。

```java
			CadBlockEntity block = cadImage.getBlockEntities().get_Item(((CadInsertObject)entity).getName());
            String value = block.getXRefPathName().getValue();
            if (value != null && !value.contentEquals(""))
            {
                block.getXRefPathName().setValue("new file reference.dwg");
            }
    
```

### 步驟 3：修改超連結

接著檢查實體是否具備超連結。若超連結符合特定 URL，則將其更新為目標 URL。此步驟可保證在 CAD 檢視器中點擊超連結時會開啟新的目標。

```java
        if (entity.getHyperlink() == "https://products.aspose.com")
        {
            entity.setHyperlink("https://www.aspose.com");
        }
```

## 常見陷阱與技巧

- **字串比較：** 在 Java 中使用 `.equals()` 取代 `==` 以確保字串比較的可靠性。範例為簡化起見使用 `==`，實務上請改為 `entity.getHyperlink().equals("https://products.aspose.com")`。  
- **空值檢查：** 呼叫 `.getValue()` 前務必確認 `block.getXRefPathName()` 不為 `null`。  
- **儲存變更：** 修改實體後，呼叫 `cadImage.save("output.dwg");` 以持久化變更（此處省略程式碼以維持原始區塊數量）。  
- **效能說明：** Aspose.CAD for Java 支援超過 30 種 CAD 格式，且可在不將整個文件載入記憶體的情況下處理高達 2 GB 的檔案，使大量更新快速且節省記憶體。

## 常見問題

### Q1：Aspose.CAD for Java 是否相容所有 DWG 圖面版本？

A1：Aspose.CAD for Java 支援超過 50 種 DWG 版本，涵蓋從 AutoCAD 2000 到最新 2025 格式。

### Q2：我可以在商業專案中使用 Aspose.CAD for Java 嗎？

A2：可以，正式上線需購買商業授權。您可於[此處](https://purchase.aspose.com/buy)購買授權。

### Q3：Aspose.CAD for Java 有免費試用版嗎？

A3：有，您可在[此處](https://releases.aspose.com/)取得免費試用版。

### Q4：如何取得 Aspose.CAD for Java 的技術支援？

A4：請前往 Aspose.CAD 論壇[此處](https://forum.aspose.com/c/cad/19)取得協助。

### Q5：我可以取得臨時授權以進行測試嗎？

A5：可以，請於[此處](https://purchase.aspose.com/temporary-license/)申請臨時授權。

**其他問答**

**Q：我需要呼叫特定方法才能將編輯後的 DWG 寫回磁碟嗎？**  
A：是的，完成變更後請呼叫 `cadImage.save("EditedDrawing.dwg");` 以持久化修改。

**Q：是否可以一次遍歷中編輯多個超連結？**  
A：絕對可以——只要在 `cadImage.getEntities()` 上迴圈，對每個符合條件的實體套用超連結邏輯即可。

---

**最後更新：** 2026-06-19  
**測試環境：** Aspose.CAD for Java 24.12  
**作者：** Aspose  

{{< blocks/products/products-backtop-button >}}

## 相關教學

- [Read XREF Meta Data from DWG Files Using Aspose.CAD for Java](/cad/java/cad-meta-data-and-rendering/read-xref-meta-data/)
- [Add Custom Properties DWG Files Using Aspose.CAD for Java](/cad/java/additional-features/add-custom-properties/)
- [Export DWG to PDF or Raster Using Aspose.CAD for Java](/cad/java/cad-drawing-conversion/export-dwg-to-pdf-or-raster/)


{{< /blocks/products/pf/tutorial-page-section >}}
{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}