---
date: 2025-12-28
description: 學習如何使用 Aspose.CAD for Java 讀取 DWG 檔案，輕鬆列出 DWG 檔案中的圖面。將強大的 CAD 功能整合至您的
  Java 應用程式。
linktitle: List Layouts in DWG
second_title: Aspose.CAD Java API
title: 如何使用 Aspose.CAD for Java 讀取 DWG 並列出 DWG 中的版面配置
url: /zh-hant/java/cad-file-manipulation/list-layouts-in-dwg/
weight: 12
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# 如何使用 Aspose.CAD for Java 讀取 DWG 並列出 DWG 中的版面配置

## 簡介

## 快速回答
- **需要的函式庫是什麼？** Aspose.CAD for Java.
- **我可以在任何作業系統上讀取 DWG 檔案嗎？** 可以 – Java 是跨平台的.
- **執行範例是否需要授權？** 免費試用可用於評估；正式環境需購買授權.
- **支援哪些 CAD 格式？** DWG、DXF、DWF 等.
- **程式碼是否相容於 Java 8 以上？** 絕對相容.

## 在 Java 中「如何讀取 DWG」是什麼？

讀取 DWG 檔案表示將二進位 CAD 資料載入可查詢的物件模型。Aspose.CAD 以簡單的 .NET/Java 類別抽象化複雜的 DWG 結構，讓您專注於所需的資訊——本例中為版面名稱。

## 為什麼要列出 DWG 檔案中的版面？

DWG 可以包含多個版面（紙張空間、模型空間、自訂圖紙）。了解版面名稱可讓您：
- 針對每個版面產生報告。
- 將特定版面匯出為影像或 PDF。
- 自動化圖紙的批次處理。

## 前置條件

在深入程式碼之前，請確認您已具備以下項目：

- **Aspose.CAD for Java Library** – 從 [website](https://releases.aspose.com/cad/java/) 下載最新的 JAR。
- **Java Development Environment** – JDK 8 或更高版本，以及您選擇的 IDE 或建置工具。

## 匯入命名空間

在您的 Java 原始檔案中，匯入所需的 Aspose.CAD 類別：

```java
import com.aspose.cad.Image;

import com.aspose.cad.fileformats.cad.CadImage;
import com.aspose.cad.fileformats.cad.CadLayoutDictionary;
import com.aspose.cad.fileformats.cad.cadobjects.CadLayout;
```

## 步驟 1：設定文件目錄

將 **“Your Document Directory”** 替換為 CAD 檔案所在的絕對路徑。

```java
String dataDir = "Your Document Directory" + "CADConversion/";
```

## 步驟 2：載入 DWG 檔案

`Image.load` 方法會自動偵測檔案格式，因此您可以使用相同的程式碼載入 **DWG** 與 **DXF** 檔案。

```java
String sourceFilePath = dataDir + "conic_pyramid.dxf";
Image image = Image.load(sourceFilePath);
CadImage cadImage = (CadImage)image;
```

## 步驟 3：取得版面並列印名稱

此迴圈會遍歷每個版面物件，並將其名稱列印至主控台——這是一個簡單的方式，驗證您已成功 **讀取 DWG** 並擷取版面資訊。

```java
CadLayoutDictionary layouts = cadImage.getLayouts();
for (CadLayout layout : layouts.getValues())
{
    System.out.println("Layout " + layout.getLayoutName());
}
```

## 常見問題與技巧

- **檔案路徑不正確** – 請再次確認 `dataDir` 以符合作業系統的分隔符 (`/` 或 `\\`) 結尾。
- **不支援的 DWG 版本** – 請確保使用最新的 Aspose.CAD 版本；較舊的 DWG 版本可能需要轉換。
- **記憶體使用量** – 大型圖紙可能佔用大量記憶體。完成後請釋放 `CadImage` 物件：`cadImage.dispose();`.

## 結論

恭喜！您現在已掌握使用 Aspose.CAD for Java **讀取 DWG** 並列出其版面的方式。此技巧是更進階 CAD 自動化的基礎，例如將特定版面匯出為影像或 PDF。欲深入了解，請參考官方 [documentation](https://reference.aspose.com/cad/java/)。

## 常見問答

### Q1：我可以將 Aspose.CAD for Java 與其他 CAD 檔案格式一起使用嗎？

A1：可以，Aspose.CAD 支援多種 CAD 格式，包括 DWG、DXF、DWF 等。

### Q2：Aspose.CAD for Java 有提供免費試用嗎？

A2：有，您可從 [here](https://releases.aspose.com/) 取得免費試用。

### Q3：在哪裡可以取得 Aspose.CAD for Java 的社群支援？

A3：請前往 [Aspose.CAD forum](https://forum.aspose.com/c/cad/19) 獲得社群支援。

### Q4：如何購買 Aspose.CAD for Java 的授權？

A4：您可在 [purchase page](https://purchase.aspose.com/buy) 購買授權。

### Q5：我可以使用臨時授權進行測試嗎？

A5：可以，您可在 [here](https://purchase.aspose.com/temporary-license/) 取得臨時授權。

**額外問題**

**Q: 此方法能在 Linux 上讀取 DWG 檔案嗎？**  
A: 絕對可以。由於解決方案純粹使用 Java，於任何具相容 JDK 的作業系統皆可執行。

**Q: 我可以在不將整個圖紙載入記憶體的情況下讀取 DWG 檔案嗎？**  
A: Aspose.CAD 會將圖紙載入記憶體；若檔案非常大，建議使用多執行緒處理或未來版本可能提供的串流 API。

**Q: 有辦法依名稱篩選版面嗎？**  
A: 有 – 取得 `CadLayoutDictionary` 後，可在處理前檢查 `layout.getLayoutName().equalsIgnoreCase("MyLayout")`。

---

**最後更新：** 2025-12-28  
**測試環境：** Aspose.CAD for Java 24.11  
**作者：** Aspose  

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}