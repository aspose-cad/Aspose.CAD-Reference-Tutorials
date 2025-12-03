---
date: 2025-12-03
description: 學習如何使用 Java 將 dxf 檔案匯出為圖像。本分步指南示範如何使用 Aspose.CAD for Java 將 dxf 版面匯出為
  JPEG 或 PNG。
language: zh-hant
linktitle: Export Specific DXF Layout to Image with Java
second_title: Aspose.CAD Java API
title: 如何使用 Aspose.CAD 在 Java 中將 DXF 版面匯出為圖像
url: /java/additional-features/export-specific-layout-to-image/
weight: 16
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# 如何使用 Aspose.CAD 在 Java 中將 DXF 版面匯出為影像

## 簡介

如果您需要了解 **如何匯出 dxf** 檔案為影像（使用 Java），Aspose.CAD 提供簡潔的 API，為您處理繁重的工作。在本教學中，我們將逐步說明整個流程——從載入 DXF（或 DWF）圖紙、選取欲匯出的版面，到最終儲存為點陣圖。無論您是在建置報表工具、CAD 檢視器，或是自動化轉換管線，掌握此工作流程都能為您節省大量時間與精力。

## 快速解答
- **需要的函式庫是什麼？** Aspose.CAD for Java  
- **我可以匯出為 PNG 而不是 JPEG 嗎？** 可以，只要將 `JpegOptions` 改成 `PngOptions`。  
- **在正式環境需要授權嗎？** 商業使用必須擁有有效的 Aspose.CAD 授權。  
- **支援哪些 Java 版本？** 完全支援 Java 8 及更新版本。  
- **是否可以一次匯出多個版面？** 當然可以——遍歷圖層清單，分別儲存每個版面即可。

## 「如何匯出 dxf」在實務上是什麼意思？
匯出 DXF 版面指的是將向量圖形資料轉換為點陣圖（如 JPEG 或 PNG），同時保留所選圖層的視覺忠實度。這在需要將 CAD 圖紙嵌入網頁、產生縮圖，或製作可列印預覽時相當有用。

## 為什麼要使用 Aspose.CAD for Java？
- **不需外部 CAD 軟體** ─ 函式庫內部自行處理解析與點陣化。  
- **細緻的圖層控制** ─ 您可以精確挑選要渲染的圖層（或版面）。  
- **多種輸出格式** ─ JPEG、PNG、BMP、TIFF 等。  
- **跨平台** ─ 只要能執行 Java 的作業系統皆可使用。

## 前置作業

在開始之前，請確保您已具備：

- **Aspose.CAD for Java** ─ 從 [Aspose 官方網站](https://releases.aspose.com/cad/java/) 下載最新 JAR。  
- **Java Development Kit (JDK) 8+** 已安裝並在 IDE 或建置工具中設定好。  
- 一個包含欲匯出版面的 DXF（或 DWF）檔案。

## 匯入命名空間

要開始使用，請在 Java 專案中匯入必要的類別：

```java
import com.aspose.cad.Image;

import com.aspose.cad.imageoptions.CadRasterizationOptions;
import com.aspose.cad.imageoptions.PdfOptions;
import com.aspose.cad.fileformats.dwf.whip.objects.DwfWhipLayer;
import com.aspose.cad.fileformats.cad.CadImage;
import com.aspose.cad.fileformats.dwf.DwfImage;
import com.aspose.cad.imageoptions.JpegOptions;
import java.util.ArrayList;
import java.util.Arrays;
import java.util.List;
```

現在讓我們詳細說明每個步驟。

## 如何匯出 DXF 版面為影像 ─ 步驟說明

### 步驟 1：設定資源目錄  
定義存放來源 DXF/DWF 檔案的資料夾。

```java
String dataDir = "Your Document Directory" + "DXFDrawings\\";
```

> **專業提示：** 請將 `"Your Document Directory"` 替換為您機器上的絕對路徑，或使用相對於專案根目錄的路徑。

### 步驟 2：載入 DXF（或 DWF）影像  
Aspose.CAD 能讀取 DXF 與 DWF 兩種格式。此範例載入一個包含多個圖層的 DWF 檔案。

```java
String srcFile = dataDir + "for_layers_test.dwf";
DwfImage image = (DwfImage) Image.load(srcFile);
```

> 若您使用純 DXF 檔案，只需將副檔名改為 `.dxf`，並轉型為 `CadImage`。

### 步驟 3：取得圖層名稱  
取得所有可用的圖層（版面）名稱，以便決定要匯出哪一個。

```java
List<String> layersNames = image.getLayers().getLayersNames();
```

現在您會得到一個 `List<String>`，其中包含如 `"Layer_0"`、`"Layer_1"` 等名稱。

### 步驟 4：設定點陣化選項  
配置輸出影像的尺寸與其他點陣化參數。

```java
CadRasterizationOptions rasterizationOptions = new CadRasterizationOptions();
rasterizationOptions.setPageWidth(1600);
rasterizationOptions.setPageHeight(1600);
```

可自行調整 `PageWidth` 與 `PageHeight` 以符合所需解析度。

### 步驟 5：指定要匯出的圖層（或版面）  
選取確切的版面。此範例匯出 **全部** 圖層，您亦可自行篩選只保留單一版面。

```java
String[] stringArray = Arrays.copyOf(layersNames.toArray(), layersNames.toArray().length, String[].class);
List<String> stringList = Arrays.asList(stringArray);
rasterizationOptions.setLayers(stringList);
```

> **為什麼這很重要：** 限制 `Layers` 集合可減少檔案大小並加快渲染速度。

### 步驟 6：設定 JPEG 選項（或 PNG）  
建立欲輸出格式的選項物件。範例使用 JPEG，若要 **java convert dxf png** 只需將 `JpegOptions` 換成 `PngOptions`。

```java
JpegOptions jpegOptions = new JpegOptions();
jpegOptions.setVectorRasterizationOptions(rasterizationOptions);
```

### 步驟 7：匯出 DXF 為影像  
最後，將點陣化後的版面儲存至磁碟。

```java
String output = dataDir + "for_layers_test.jpg";
image.save(output, jpegOptions);
```

若想輸出 PNG，只需將檔案副檔名改為 `.png`，並在前一步使用 `PngOptions`。

> **結果：** 指定的 DXF 版面已成功儲存為高品質影像，可供顯示、分享或進一步處理。

## 常見問題與解決方案

| 問題 | 原因 | 解決方式 |
|------|------|----------|
| **在 `image.getLayers()` 上拋出 NullPointerException** | 檔案不是 DWF/DXF 或已損毀。 | 確認來源檔案路徑正確，且檔案為支援的 CAD 格式。 |
| **輸出影像為空白** | `rasterizationOptions.setLayers()` 未選取任何圖層。 | 確認圖層清單中包含欲匯出的版面名稱。 |
| **影像解析度過低** | `PageWidth`/`PageHeight` 設定過小。 | 增大尺寸，或使用 `rasterizationOptions.setResolution(300)` 提升 DPI。 |
| **LicenseException** | 未使用有效的 Aspose.CAD 授權。 | 在載入影像前使用 `License license = new License(); license.setLicense("Aspose.CAD.lic");` 申請授權。 |

## 常見問答

**Q: 我可以一次匯出多個 DXF 版面嗎？**  
A: 可以。遍歷 `layersNames` 清單，於 `CadRasterizationOptions` 中設定每個圖層（或圖層群組），然後對每次迭代呼叫 `image.save()`。

**Q: Aspose.CAD for Java 是否相容於 Java 11 及更新版本？**  
A: 完全相容。此函式庫基於 .NET Standard，適用於任何支援相應 JAR 相依性的 Java 版本。

**Q: 如何處理轉換過程中的錯誤？**  
A: 將載入與儲存程式碼包在 `try‑catch` 區塊中，捕捉 `Exception` 或更具體的 Aspose 例外，以便記錄或重新拋出。

**Q: 除了 JPEG，還有其他輸出格式嗎？**  
A: 有。Aspose.CAD 支援 PNG、BMP、TIFF、GIF 以及 PDF。只需對應更換選項類別（`JpegOptions`、`PngOptions` 等）。

**Q: 能否自訂背景顏色或線條粗細？**  
A: `CadRasterizationOptions` 提供 `setBackgroundColor()`、`setLineWidth()` 等屬性，可微調點陣化輸出。

## 結論

現在您已掌握使用 Aspose.CAD for Java **如何匯出 dxf** 版面為點陣圖的完整、可投入生產的作法。透過調整點陣化選項與輸出格式，您可以因應縮圖、高解析度列印或網頁 PNG 等不同需求。歡迎自行嘗試圖層篩選、DPI 設定與多種影像格式，以符合專案的精確需求。

---

**最後更新：** 2025-12-03  
**測試環境：** Aspose.CAD for Java 24.12  
**作者：** Aspose  

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}