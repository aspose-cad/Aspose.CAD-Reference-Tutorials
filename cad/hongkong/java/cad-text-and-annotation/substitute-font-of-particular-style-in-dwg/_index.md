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

## Introduction

在 CAD（Computer-Aided Design）領域，精確與細節至關重要，**了解如何替換字體** 能為您節省大量重新製作的時間。Aspose.CAD for Java 為開發者提供一種乾淨、程式化的方式來修改 DWG 檔案，包括變更特定文字樣式的字體。本教學將逐步說明如何在 DWG 檔案中替換特定樣式的字體、說明為何需要這麼做，並示範如何驗證結果。

## Quick Answers
- **「replace font」在 DWG 中是什麼意思？** 更改與文字樣式定義相關聯的主要字體。  
- **哪個函式庫負責此功能？** Aspose.CAD for Java。  
- **我需要授權嗎？** 免費試用可用於測試；正式上線需購買商業授權。  
- **可以一次變更多個樣式嗎？** 可以——遍歷樣式集合並為每個樣式設定字體。  
- **程式碼是否相容於 Java 8 以上？** 完全相容，API 目標為 Java 8 及更新版本。

## What is Font Replacement in a DWG?
字體替換指的是更新文字樣式（在 DWG 詞彙中亦稱為「style」）的*主要字體*屬性。當圖面引用該樣式時，所有文字會自動套用新字體，確保整個檔案的外觀保持一致。

## Why Modify DWG Text Style?
- **維持品牌一致性：** 在所有圖面中使用公司字體。  
- **修復缺失字體：** 將無法使用的字體替換為目標系統已安裝的字體。  
- **為列印/繪圖做準備：** 某些繪圖機需要特定字體才能正確輸出。  

## Prerequisites

在開始本教學之前，請先確保已完成以下設定：

1. **Aspose.CAD for Java Library：** 下載並安裝 Aspose.CAD 函式庫。您可以在 [此處](https://releases.aspose.com/cad/java/) 找到函式庫與相關文件。  
2. **Java Development Kit (JDK)：** 確認您的機器已安裝 Java。

現在您已具備必要工具，請繼續下一節。

## Import Namespaces (required to modify DWG text style)

在 Java 中，正確匯入命名空間對於使用外部函式庫至關重要。此處請確保匯入所需的 Aspose.CAD 命名空間。以下為範例程式碼：

```java
import com.aspose.cad.Image;

import com.aspose.cad.fileformats.cad.CadImage;
```

現在，我們將範例程式碼拆解為多個步驟。

## Step 1: Set the Resource Directory

```java
// The path to the resource directory.
String dataDir = "Your Document Directory" + "CADConversion/";
```

將 `"Your Document Directory"` 替換為您實際的文件目錄路徑。

## Step 2: Load the CAD Drawing

```java
String srcFile = dataDir + "conic_pyramid.dxf";

// Load a CAD drawing in an instance of CadImage
CadImage cadImage = (CadImage)Image.load(srcFile);
```

請將 `"conic_pyramid.dxf"` 替換為您 CAD 圖面的實際檔名。

## Step 3: Specify Font for a Style (change DWG style font)

```java
// Specify the font for one particular style
((CadStyleTableObject)cadImage.getStyles().get_Item(0)).setPrimaryFontName("Arial");
```

依需求調整字體名稱（本例為 "Arial"）。此行 **設定 DWG 樣式的主要字體**，即完成舊字體的替換。

## Common Issues and Solutions

| 問題 | 原因 | 解決方案 |
|-------|-------|----------|
| Font does not change after saving | The drawing was not saved after modification | Call `cadImage.save(outputPath);` after setting the font. |
| Font name not recognized | Font not installed on the system where the code runs | Install the font or use a generic font name (e.g., "Tahoma"). |
| `ClassCastException` | Wrong object type from `get_Item` | Ensure the index points to a `CadStyleTableObject`. |

## FAQ's

### Q1: Can I substitute multiple fonts in one DWG file?

A1: Yes, you can iterate through different styles and set the primary font for each style individually.

### Q2: Is there a limit to the font names I can use?

A2: No, you can use any valid font name available on your system.

### Q3: Can I undo font substitutions?

A3: Aspose.CAD provides flexibility; you can revert changes or save different versions of your DWG file.

### Q4: Does this tutorial apply to other CAD formats?

A4: While the example focuses on DWG, similar principles can be applied to other supported CAD formats.

### Q5: How can I get support for Aspose.CAD for Java?

A5: Visit the [Aspose.CAD forum](https://forum.aspose.com/c/cad/19) for community support and discussions.

## Additional Frequently Asked Questions

**Q: How do I save the modified drawing?**  
A: After setting the new font, call `cadImage.save(dataDir + "output.dwg");` to write the changes to a new file.

**Q: Can I replace the font of annotation objects only?**  
A: Yes, filter the style collection for annotation‑related styles before applying `setPrimaryFontName`.

**Q: Is it possible to preview the font change without saving?**  
A: You can render the image to a bitmap using `cadImage.save(outputStream, new ImageOptions());` to preview in memory.

**Q: Does Aspose.CAD support TrueType and OpenType fonts?**  
A: Both TrueType (.ttf) and OpenType (.otf) fonts are fully supported as long as they are installed on the host OS.

## Conclusion

Aspose.CAD for Java 為 CAD 操作開啟了強大的可能性，而 **how to replace font** 只是其中一項功能。您可以嘗試不同樣式，使用次要關鍵字如 *modify DWG text style* 或 *set primary font dwg* 進一步微調圖面，並將程式碼整合至更大的自動化流程，以實現批次處理。

---

**Last Updated:** 2026-01-02  
**Tested With:** Aspose.CAD for Java 24.11  
**Author:** Aspose  

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}