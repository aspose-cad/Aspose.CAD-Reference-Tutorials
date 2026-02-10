---
date: 2025-12-19
description: 了解如何使用 Aspose.CAD for Java 將 CAD 儲存為 PNG，將 DWG、DXF 及其他 CAD 檔案高效轉換為點陣圖像。
linktitle: Convert CAD Drawing to Raster Image Format
second_title: Aspose.CAD Java API
title: 將 CAD 另存為 PNG – 使用 Aspose.CAD for Java 將 CAD 圖紙轉換為點陣圖格式
url: /zh-hant/java/cad-drawing-conversion/convert-cad-drawing-to-raster-image/
weight: 10
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# 將 CAD 儲存為 PNG – 使用 Aspose.CAD for Java 轉換 CAD 圖紙為點陣圖格式

## 簡介

在本教學中，您將學習如何使用 Aspose.CAD for Java **將 CAD 儲存為 PNG**。將 CAD 圖紙轉換為 PNG 等點陣圖格式是網頁預覽、文件編寫與報告中常見的需求。Aspose.CAD 提供可靠且高效能的方式，執行 **cad to png conversion**（CAD 轉 PNG）以支援 DWG、DXF、DWF 以及其他多種 CAD 檔案類型。

## 快速答覆
- **什麼程式庫負責轉換？** Aspose.CAD for Java.  
- **我可以將 DWG 轉換為 PNG 嗎？** 可以 – 同一個 API 可用於 DWG、DXF 以及其他格式。  
- **在正式環境需要授權嗎？** 非評估使用須購買商業授權。  
- **點陣圖尺寸可否自訂？** 當然可以 – 您可以透過 rasterization options 設定頁寬、頁高與 DPI。  
- **轉換需要多長時間？** 一般標準圖紙通常在一秒內完成；較大的檔案可能需要更長時間。

## 什麼是「將 CAD 儲存為 PNG」？

將 CAD 儲存為 PNG 代表將向量式 CAD 資料光柵化為像素圖像（PNG）。此過程常稱為 **convert cad to raster**，在保留視覺精度的同時，產生易於嵌入網頁、電子郵件或報告的格式。

## 為什麼使用 Aspose.CAD for Java？

- **廣泛的格式支援** – 可處理 DWG、DXF、DWF 等多種格式。  
- **無外部相依性** – 純 Java，無需本機 DLL。  
- **細緻的控制** – 可自訂解析度、背景顏色與渲染品質。  
- **可擴展的效能** – 適用於批次處理或即時轉換。

## 先決條件

在開始本教學之前，請確保已具備以下先決條件：

1. **Java 開發環境**：確保您的機器上已安裝並設定好可運作的 Java 開發環境。  
2. **Aspose.CAD 程式庫**：下載並將 Aspose.CAD for Java 程式庫整合至您的專案中。您可於[此處](https://releases.aspose.com/cad/java/)取得程式庫。

## 匯入命名空間

在 Java 程式碼中，匯入必要的命名空間以有效使用 Aspose.CAD for Java 的功能。此步驟對於存取所需的類別與方法至關重要。

```java
import com.aspose.cad.Image;
import com.aspose.cad.ImageOptionsBase;

import com.aspose.cad.imageoptions.CadRasterizationOptions;
import com.aspose.cad.imageoptions.PngOptions;
```

現在，讓我們將將 CAD 圖紙轉換為點陣圖的過程分解為以下詳細步驟：

## 步驟 1：載入 CAD 圖紙

```java
String dataDir = "Your Document Directory" + "CADConversion/";
String srcFile = dataDir + "conic_pyramid.dxf";
Image image = Image.load(srcFile);
```

在此步驟中，我們使用 `Image.load()` 方法從指定的檔案路徑載入 CAD 圖紙。

## 步驟 2：設定光柵化選項

```java
CadRasterizationOptions rasterizationOptions = new CadRasterizationOptions();
rasterizationOptions.setPageWidth(1200);
rasterizationOptions.setPageHeight(1200);
```

建立 `CadRasterizationOptions` 的實例，並為光柵化圖像設定頁寬與頁高。

## 步驟 3：建立影像選項

```java
ImageOptionsBase options = new PngOptions();
options.setVectorRasterizationOptions(rasterizationOptions);
```

為最終圖像建立 `PngOptions` 的實例，並設定向量光柵化選項。

## 步驟 4：儲存光柵圖像

```java
image.save(dataDir + "conic_pyramid_raster_image_out.png", options);
```

使用 `image.save()` 方法將產生的光柵圖像儲存至指定目錄。

對您的每個 CAD 檔案重複上述步驟，即可成功 **將 CAD 圖紙影像** 轉換為 PNG。

## 常見使用情境與技巧

- **網頁預覽產生** – 將大型 DWG 檔案轉換為輕量的 PNG 縮圖，以快速在瀏覽器中顯示。  
- **報告嵌入** – 在不支援向量 CAD 檔案的 PDF 或 Word 報告中使用 PNG 輸出。  
- **批次轉換** – 迭代資料夾中的 CAD 檔案，套用相同的光柵化設定以產生一致的輸出。  
- **專業提示**：調整 `rasterizationOptions.setResolution()` 以提升 DPI，獲得高解析度列印效果。

## 結論

總結來說，使用 Aspose.CAD for Java 將 CAD 圖紙轉換為點陣圖是一個簡單的流程。依循本教學所列步驟，您即可有效將此功能整合至 Java 應用程式中，執行 **convert dwg to png**、**export cad as png** 或其他任何 **cad to png conversion**。

## 常見問題

**Q: 如何在轉換 DWG 為 PNG 時設定自訂背景顏色？**  
A: 在建立 `PngOptions` 實例之前，於 `CadRasterizationOptions` 上設定 `backgroundColor` 屬性。

**Q: 能否一次批次轉換多個 CAD 檔案？**  
A: 可以——將載入、光柵化與儲存步驟包在迴圈中，遍歷您的檔案集合。

**Q: 預設設定下的影像品質如何？**  
A: 預設 DPI 為 96，產生螢幕品質的 PNG；若需列印品質，請提升 DPI。

**Q: Aspose.CAD 是否支援 PNG 輸出的透明背景？**  
A: 完全支援。預設情況下 PNG 會保存 alpha 通道，您亦可在光柵化選項中指定透明背景。

**Q: 我可以將 CAD 檔案轉換為其他點陣格式，如 JPEG 或 BMP 嗎？**  
A: 可以——將 `PngOptions` 替換為 `JpegOptions` 或 `BmpOptions`，其餘光柵化設定保持不變。

---

**最後更新：** 2025-12-19  
**測試環境：** Aspose.CAD for Java 24.12（最新）  
**作者：** Aspose  

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}