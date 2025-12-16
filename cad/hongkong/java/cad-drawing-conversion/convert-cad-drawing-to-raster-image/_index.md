---
date: 2025-12-16
description: 了解如何使用 Aspose.CAD for Java 將 CAD 轉換為 PNG，涵蓋匯出 DWG 為圖像、將 CAD 儲存為 PNG，以及
  CAD 轉換為點陣圖的選項。
linktitle: Convert CAD Drawing to Raster Image Format
second_title: Aspose.CAD Java API
title: 如何使用 Aspose.CAD for Java 將 CAD 轉換為 PNG
url: /zh-hant/java/cad-drawing-conversion/convert-cad-drawing-to-raster-image/
weight: 10
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# 如何使用 Aspose.CAD for Java 將 CAD 轉換為 PNG

在現代工程工作流程中，您常常需要 **將 CAD 轉換為 PNG**，以便在瀏覽器中顯示圖紙、嵌入文件，或與沒有 CAD 軟體的利害關係人共享。本教學將帶您完整了解從載入 CAD 檔案到匯出高品質 PNG 點陣圖的每一步，使用功能強大的 Aspose.CAD for Java 函式庫。

## 快速解答
- **主要目的為何？** 將 CAD 圖紙轉換為 PNG 點陣圖。  
- **使用哪個函式庫？** Aspose.CAD for Java。  
- **需要授權嗎？** 提供免費試用版；正式環境需購買授權。  
- **可以自訂影像尺寸嗎？** 可以，使用 `CadRasterizationOptions` 設定寬度與高度。  
- **支援哪些 CAD 格式？** DWG、DXF、DWF 等多種格式。

## 什麼是「將 CAD 轉換為 PNG」？
將 CAD 轉換為 PNG 意指將向量式 CAD 內容（DWG、DXF 等）光柵化為像素式影像格式。PNG 支援透明度且為無損壓縮，非常適合用於網頁預覽、文件說明與報告。

## 為什麼要將 CAD 轉換為 PNG（CAD 轉點陣圖）？
- **通用檢視：** PNG 可在任何裝置上開啟，無需特別的 CAD 檢視器。  
- **載入快速：** 點陣圖在網頁上即時顯示。  
- **易於嵌入：** 可將 PNG 插入 PDF、Word 文件或簡報。  
- **外觀一致：** 完全保留線寬、顏色與圖層的原始設計。

## 前置條件
在開始之前，請確保您已具備：

1. **Java 開發環境** – 已安裝並設定 JDK 8 或更新版本。  
2. **Aspose.CAD 函式庫** – 下載並將函式庫加入專案。您可以在 **[此處](https://releases.aspose.com/cad/java/)** 取得。

## 匯入命名空間
在 Java 類別中加入必要的匯入，以便使用 Aspose.CAD 物件。

```java
import com.aspose.cad.Image;
import com.aspose.cad.ImageOptionsBase;

import com.aspose.cad.imageoptions.CadRasterizationOptions;
import com.aspose.cad.imageoptions.PngOptions;
```

## 步驟說明：將 CAD 轉換為 PNG

### 步驟 1：載入 CAD 圖紙
使用 `Image.load()` 載入來源 CAD 檔案（DXF、DWG 等）。

```java
String dataDir = "Your Document Directory" + "CADConversion/";
String srcFile = dataDir + "conic_pyramid.dxf";
Image image = Image.load(srcFile);
```

> **小技巧：** 將 CAD 檔案放在專屬資料夾（例如 `CADConversion`）中，可避免路徑問題。

### 步驟 2：設定光柵化選項（將 dwg 匯出為影像）
定義輸出影像的尺寸與其他光柵化設定。

```java
CadRasterizationOptions rasterizationOptions = new CadRasterizationOptions();
rasterizationOptions.setPageWidth(1200);
rasterizationOptions.setPageHeight(1200);
```

您亦可在此控制背景顏色、線條渲染模式與 DPI 等參數。

### 步驟 3：建立影像選項（將 cad 儲存為 png）
建立 `PngOptions` 實例，並將光柵化設定套用上去。

```java
ImageOptionsBase options = new PngOptions();
options.setVectorRasterizationOptions(rasterizationOptions);
```

### 步驟 4：儲存點陣圖（cad 檔案轉 png）
最後，將 PNG 檔寫入磁碟。

```java
image.save(dataDir + "conic_pyramid_raster_image_out.png", options);
```

產生的檔案 `conic_pyramid_raster_image_out.png` 為原始 CAD 圖紙的高解析度 PNG 版本。

### 針對其他檔案重複執行
只需將 `srcFile` 改為其他 CAD 檔案路徑，重新執行相同步驟。相同程式碼同樣適用於 DWG、DWF 以及其他支援格式。

## 常見問題與解決方案
| 問題 | 解決方案 |
|------|----------|
| **PNG 輸出為空白** | 確認來源 CAD 檔案正確載入（`Image.load()` 不應拋出例外）。 |
| **尺寸不正確** | 調整 `PageWidth` / `PageHeight`，或透過 `rasterizationOptions.setResolution(...)` 設定 DPI。 |
| **圖層遺失** | 確認 CAD 檔的圖層未被隱藏；可使用 `CadRasterizationOptions.setDrawType(CadDrawTypeMode.Vector);`。 |
| **授權錯誤** | 使用有效的 Aspose.CAD 授權檔案（`License license = new License(); license.setLicense("Aspose.CAD.lic");`）。 |

## 常見問答

**Q1：Aspose.CAD 是否支援所有 CAD 格式？**  
A1：Aspose.CAD 支援多種 CAD 格式，包括 DWG、DXF、DWF 等。完整列表請參閱 **[文件說明](https://reference.aspose.com/cad/java/)**。

**Q2：我可以依需求自訂光柵化選項嗎？**  
A2：可以，Aspose.CAD 提供彈性設定光柵化參數，讓您依尺寸、DPI、背景色等需求調整輸出。

**Q3：在哪裡可以取得 Aspose.CAD 相關支援？**  
A3：請前往 **[Aspose.CAD 論壇](https://forum.aspose.com/c/cad/19)** 尋求協助，並與社群互動。

**Q4：Aspose.CAD for Java 有免費試用版嗎？**  
A4：有，您可在 **[此處](https://releases.aspose.com/)** 取得免費試用。

**Q5：如何購買 Aspose.CAD for Java？**  
A5：前往 **[購買頁面](https://purchase.aspose.com/buy)** 完成購買。

---

**最後更新：** 2025-12-16  
**測試環境：** Aspose.CAD for Java 24.11（撰寫時最新版本）  
**作者：** Aspose  

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}