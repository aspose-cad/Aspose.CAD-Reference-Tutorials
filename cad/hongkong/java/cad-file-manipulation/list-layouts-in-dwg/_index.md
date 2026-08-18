---
date: 2026-02-28
description: 學習如何使用 Aspose.CAD for Java 讀取 DWG 檔案，輕鬆列出 DWG 檔案中的版面。將強大的 CAD 功能整合到您的
  Java 應用程式中。
linktitle: List Layouts in DWG
second_title: Aspose.CAD Java API
title: 如何使用 Aspose.CAD for Java 讀取 DWG 並列出 DWG 中的版面
url: /zh-hant/java/cad-file-manipulation/list-layouts-in-dwg/
weight: 12
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# 如何使用 Aspose.CAD for Java 讀取 DWG 並列出 DWG 中的版面配置

## 介紹

如果您正在尋找一種可靠的 **how to read dwg** 檔案的程式化方式，Aspose.CAD for Java 提供了乾淨、跨平台的 API，讓您可以載入圖紙並提取任何所需資訊——例如檔案內所有版面配置的名稱。在本步驟教學中，我們將示範 **how to read DWG** 並列出 DWG（或 DXF）檔案中包含的每個版面，讓您能將此功能整合至任何處理 CAD 資料的 Java 應用程式。

## 快速回答
- **需要哪個函式庫？** Aspose.CAD for Java。  
- **可以在任何作業系統上讀取 DWG 檔案嗎？** 可以——Java 為跨平台語言，您可以 **read dwg on linux** 與在 Windows 上同樣輕鬆。  
- **執行範例是否需要授權？** 免費試用可用於評估；正式環境需購買授權。  
- **支援哪些 CAD 格式？** DWG、DXF、DWF 等。  
- **程式碼是否相容於 Java 8+？** 絕對相容。

## 在 Java 中的 “how to read dwg” 是什麼？

讀取 DWG 檔案即是將二進位 CAD 資料載入可查詢的物件模型。Aspose.CAD 將複雜的 DWG 結構抽象為簡單的 Java 類別，讓您只需關注所需資訊——本例中即版面名稱。

## 為什麼要列出 DWG 檔案中的版面？

DWG 可能包含多個版面（紙張空間、模型空間、自訂圖紙）。取得版面名稱可讓您：

- 依版面產生報表。  
- 將特定版面匯出為影像或 PDF。  
- 自動化批次處理圖紙。  

## 前置條件

在開始撰寫程式碼前，請確認您已具備以下項目：

- **Aspose.CAD for Java Library** – 從[官方網站](https://releases.aspose.com/cad/java/)下載最新 JAR。  
- **Java 開發環境** – JDK 8 以上，並配合您慣用的 IDE 或建置工具。

## 匯入命名空間

在 Java 原始檔中匯入所需的 Aspose.CAD 類別：

```java
import com.aspose.cad.Image;

import com.aspose.cad.fileformats.cad.CadImage;
import com.aspose.cad.fileformats.cad.CadLayoutDictionary;
import com.aspose.cad.fileformats.cad.cadobjects.CadLayout;
```

## 步驟 1：設定文件目錄

```java
String dataDir = "Your Document Directory" + "CADConversion/";
```

將 **“Your Document Directory”** 替換為 CAD 檔案所在的絕對路徑。於 Linux 上可使用類似 `/home/user/cad/` 的路徑。

## 步驟 2：載入 DWG 檔案

```java
String sourceFilePath = dataDir + "conic_pyramid.dxf";
Image image = Image.load(sourceFilePath);
CadImage cadImage = (CadImage)image;
```

`Image.load` 方法會自動偵測檔案格式，因此相同程式碼同時支援 **DWG** 與 **DXF** 檔案。

## 步驟 3：取得版面並列印名稱

```java
CadLayoutDictionary layouts = cadImage.getLayouts();
for (CadLayout layout : layouts.getValues())
{
    System.out.println("Layout " + layout.getLayoutName());
}
```

此迴圈會遍歷每個版面物件，並將名稱印出至主控台——是一個簡單的方式，驗證您已成功 **read DWG** 並擷取版面資訊。

## 在 Linux 上將 DWG 轉換為 PDF 的方法

若日後需要將特定版面轉成 PDF，Aspose.CAD 可先將版面渲染為影像，然後使用 Aspose.PDF（或其他 PDF 函式庫）將影像嵌入 PDF 文件。因為 API 完全基於 Java，轉換程式碼在 Linux 上與其他平台相同。

## 常見問題與技巧

- **檔案路徑不正確** – 請再次確認 `dataDir` 以正確的分隔符（`/` 或 `\\`）結尾，符合您的作業系統。  
- **不支援的 DWG 版本** – 請使用最新的 Aspose.CAD 版本；舊版 DWG 可能需要先轉換。  
- **記憶體使用量** – 大型圖紙會佔用大量記憶體，使用完畢後請釋放 `CadImage` 物件：`cadImage.dispose();`。  
- **在無頭伺服器上執行** – 不需要 UI 元件，程式碼可在沒有圖形環境的 Linux 伺服器上執行。

## 結論

恭喜您！現在您已掌握 **how to read dwg** 並使用 Aspose.CAD for Java 列出其版面配置的技巧。此方法是進階 CAD 自動化的基礎，例如將特定版面匯出為影像、PDF，或在 Linux 上將 DWG 轉為 PDF。欲深入了解，請參考官方[文件](https://reference.aspose.com/cad/java/)。

## 常見問答

**Q1: 可以在 Aspose.CAD for Java 中使用其他 CAD 檔案格式嗎？**  
A1: 可以，Aspose.CAD 支援多種 CAD 格式，包括 DWG、DXF、DWF 等。

**Q2: Aspose.CAD for Java 有免費試用嗎？**  
A2: 有，您可從[此處](https://releases.aspose.com/)取得免費試用。

**Q3: 哪裡可以取得 Aspose.CAD for Java 的社群支援？**  
A3: 請前往[Aspose.CAD 論壇](https://forum.aspose.com/c/cad/19)取得社群協助。

**Q4: 如何購買 Aspose.CAD for Java 的授權？**  
A4: 您可在[購買頁面](https://purchase.aspose.com/buy)購買授權。

**Q5: 可以使用臨時授權進行測試嗎？**  
A5: 可以，請從[此處](https://purchase.aspose.com/temporary-license/)取得臨時授權。

**其他問題**

**Q: 這種做法能在 Linux 上讀取 DWG 檔案嗎？**  
A: 完全可以。因為解決方案純粹使用 Java，能在任何安裝相容 JDK 的作業系統上執行。

**Q: 能否在不將整個圖紙載入記憶體的情況下讀取 DWG 檔案？**  
A: Aspose.CAD 會將圖紙載入記憶體；若檔案極大，可考慮以多執行緒方式處理，或等待未來版本提供串流 API。

**Q: 有辦法依名稱過濾版面嗎？**  
A: 有——取得 `CadLayoutDictionary` 後，可使用 `layout.getLayoutName().equalsIgnoreCase("MyLayout")` 進行篩選。

---

**最後更新：** 2026-02-28  
**測試環境：** Aspose.CAD for Java 24.11  
**作者：** Aspose  

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}