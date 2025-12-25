---
date: 2025-12-25
description: 了解如何使用 Aspose.CAD for Java 將 DWG 匯出為 BMP。本分步指南說明如何調整 CAD 圖紙尺寸並高效地將 CAD
  轉換為 BMP。
linktitle: Adjusting CAD Drawing Size Using Unit Type
second_title: Aspose.CAD Java API
title: 將 DWG 匯出為 BMP – 使用單位類型調整 CAD 大小 (Java)
url: /zh-hant/java/cad-file-manipulation/adjusting-cad-drawing-size-using-unit-type/
weight: 14
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# 匯出 DWG 為 BMP – 使用 Aspose.CAD for Java 透過單位類型調整 CAD 繪圖尺寸

## 介紹

當您需要 **匯出 DWG 為 BMP** 時，控制輸出尺寸與測量單位對於後續處理或列印至關重要。在本教學中，您將學會如何使用 Aspose.CAD for Java 調整 CAD 繪圖尺寸並將 CAD 轉換為 BMP，透過 `UnitType` 屬性來定義測量單位。步驟以簡明語言說明，即使您是首次使用此函式庫也能輕鬆跟隨。

## 快速回答
- **「匯出 DWG 為 BMP」是什麼意思？** 將 DWG 繪圖轉換為 BMP 點陣圖像。  
- **哪個屬性控制輸出尺寸？** `CadRasterizationOptions.setUnitType()` 用於設定單位（例如公分）。  
- **執行程式碼需要授權嗎？** 免費試用可用於評估；正式環境需購買授權。  
- **可以選擇其他版面配置嗎？** 可以，使用 `setLayouts()` 指定模型空間或紙張空間版面。  
- **支援哪些輸出格式？** 除 BMP 外，亦可透過更換選項類別匯出為 PNG、JPEG、TIFF 等。

## 什麼是 **匯出 DWG 為 BMP**？

匯出 DWG 為 BMP 意指將向量式 DWG 檔案光柵化為位圖圖像（BMP）。當您需要為舊有系統、影像處理流程或簡易顯示情境提供像素精確的圖像時，此功能相當實用。

## 為什麼要使用 **單位類型** 調整 CAD 繪圖尺寸？

設定單位類型可讓您在不必自行計算縮放比例的情況下，直接控制匯出圖像的實體尺寸。這確保位圖與實際測量（例如公分）相符，對工程圖與列印文件尤為重要。

## 前置條件

在開始教學之前，請確保已具備以下前置條件：

- **Java 開發環境** – 已安裝 JDK（8 版或以上）以及 IDE 或建置工具（Maven/Gradle）。  
- **Aspose.CAD for Java 程式庫** – 下載並將 Aspose.CAD 程式庫整合至您的 Java 專案。您可於[此處](https://releases.aspose.com/cad/java/)取得程式庫。

## 匯入命名空間

在 Java 程式碼中，加入必要的匯入以存取 Aspose.CAD 功能。請加入以下 import：

```java
import com.aspose.cad.Image;
import com.aspose.cad.ImageOptionsBase;

import com.aspose.cad.imageoptions.CadRasterizationOptions;
import com.aspose.cad.imageoptions.PngOptions;
```

現在，讓我們將使用單位類型調整 CAD 繪圖尺寸的流程分解為可管理的步驟：

## 步驟 1：定義資料目錄

```java
String dataDir = "Your Document Directory" + "CADConversion/";
```

設定存放 CAD 檔案的目錄路徑。

## 步驟 2：載入 CAD 繪圖

```java
String sourceFilePath = dataDir + "sample.dwg";
Image image = Image.load(sourceFilePath);
```

使用 Aspose.CAD 的 `Image` 類別載入 CAD 繪圖。

## 步驟 3：建立 BMP 選項

```java
BmpOptions bmpOptions = new BmpOptions();
```

實例化 `BmpOptions` 類別，以匯出 CAD 版面為 BMP 格式。

## 步驟 4：設定光柵化選項

```java
CadRasterizationOptions cadRasterizationOptions = new CadRasterizationOptions();
bmpOptions.setVectorRasterizationOptions(cadRasterizationOptions);
```

建立 `CadRasterizationOptions` 實例，並將其關聯至 `BmpOptions` 以執行向量光柵化。

## 步驟 5：設定單位類型

```java
cadRasterizationOptions.setUnitType(UnitType.Centimeter);
```

指定 CAD 繪圖的目標單位類型。本例中，我們將其設為 **Centimeter**，此設定會直接影響在 **調整 CAD 繪圖尺寸** 時匯出圖像的大小。

## 步驟 6：設定版面

```java
cadRasterizationOptions.setLayouts(new String[] { "Model" });
```

定義匯出時要考慮的版面。本例選取 **"Model"** 版面，若需要亦可切換至紙張空間版面。

## 步驟 7：匯出為 BMP

```java
String outPath = sourceFilePath + ".bmp";
image.save(outPath, bmpOptions);
```

最後，將已修改的 CAD 繪圖儲存為 BMP 格式。此步驟完成 **匯出 DWG 為 BMP** 工作流程，同時保留您先前設定的尺寸調整。

## 常見問題與解決方案

| 問題 | 原因 | 解決方式 |
|------|------|----------|
| **輸出圖像太小** | 未設定單位類型或使用預設（像素） | 呼叫 `setUnitType()` 並傳入所需的測量單位（例如 `UnitType.Centimeter`）。 |
| **匯出錯誤的版面** | 版面名稱拼寫錯誤 | 使用 CAD 檢視器確認版面名稱，並在 `setLayouts()` 中使用完全相同的字串。 |
| **授權例外** | 生產環境未使用有效授權 | 如 FAQ 所述，套用臨時或永久授權。 |

## 常見問答（延伸）

**Q: 我可以在其他程式語言中使用 Aspose.CAD for Java 嗎？**  
A: Aspose.CAD 主要支援 Java，但也提供 .NET 等其他語言的版本。

**Q: Aspose.CAD 有哪些授權方案？**  
A: 您可於[此處](https://purchase.aspose.com/buy)探索授權選項並購買 Aspose.CAD。

**Q: 是否提供 Aspose.CAD 的免費試用？**  
A: 當然，您可於[此處](https://releases.aspose.com/)取得免費試用。

**Q: 如何取得 Aspose.CAD for Java 的技術支援？**  
A: 請前往 Aspose.CAD 論壇[此處](https://forum.aspose.com/c/cad/19)取得完整支援。

**Q: 我可以取得臨時授權嗎？**  
A: 可以，請於[此處](https://purchase.aspose.com/temporary-license/)申請臨時授權。

---

**最後更新：** 2025-12-25  
**測試環境：** Aspose.CAD for Java 24.10  
**作者：** Aspose  

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}