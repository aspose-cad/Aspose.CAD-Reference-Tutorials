---
date: 2025-11-30
description: 學習如何使用 Aspose.CAD for Java 從 DXF 檔案建立 PDF 並匯出特定圖層。本分步指南將向您展示如何快速且可靠地將
  DXF 轉換為 PDF。
language: zh-hant
linktitle: Export Specific Layer of DXF Drawing to PDF with Java
second_title: Aspose.CAD Java API
title: 從 DXF 建立 PDF：使用 Aspose.CAD for Java 匯出圖層
url: /java/additional-features/export-specific-layer-to-pdf/
weight: 18
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# 從 DXF 建立 PDF：使用 Aspose.CAD for Java 匯出圖層

## 簡介

如果您需要 **從 DXF 建立 PDF** 圖紙，同時只保留您關心的圖層，Aspose.CAD for Java 可讓此過程變得輕鬆。在本教學中，我們將示範一個真實情境：將 DXF 檔案的單一圖層匯出為 PDF 文件。您將了解此方法為何適合產生輕量圖紙、與非 CAD 使用者分享設計細節，或建構自動化報告流程。

## 快速答覆
- **本教學涵蓋什麼內容？** 使用 Aspose.CAD for Java 將特定 DXF 圖層匯出為 PDF。  
- **主要好處？** 只保留所需的幾何圖形，減少檔案大小與視覺雜訊。  
- **先決條件？** Java SDK、Aspose.CAD for Java 函式庫，以及一個 DXF 檔案。  
- **實作需要多長時間？** 基本設定大約需要 10‑15 分鐘。  
- **可以匯出多個圖層嗎？** 可以 – 只要調整圖層清單（見 Step 3）。

## 什麼是「從 DXF 建立 PDF」？

將 DXF（Drawing Exchange Format）檔案轉換為 PDF 文件是常見需求，尤其在需要與沒有 CAD 軟體的利害關係人分享 CAD 資料時。PDF 格式能保留視覺精度，且可在任何平台上檢視。

## 為何使用 Aspose.CAD for Java 轉換 DXF 為 PDF？

- **無外部相依性** – 純 Java，無需本機 DLL。  
- **細緻的圖層控制** – 精確選擇要在輸出中顯示的圖層。  
- **高品質光柵化** – 可設定 DPI、頁面尺寸與渲染選項。  
- **跨平台** – 可在 Windows、Linux 及 macOS 上執行。

## 先決條件

- **Aspose.CAD for Java 函式庫** – 從 [Aspose.CAD Java 文件](https://reference.aspose.com/cad/java/) 下載。  
- **Java 開發環境** – JDK 8 或以上，並使用您偏好的 IDE 或建置工具。

## 匯入命名空間

首先，匯入您需要的類別。將 import 整合在一起有助於可讀性，也方便未來的更新。

```java
import com.aspose.cad.Image;

import com.aspose.cad.imageoptions.CadRasterizationOptions;
import com.aspose.cad.imageoptions.PdfOptions;
import java.util.ArrayList;
import java.util.Arrays;
import java.util.List;
```

## 步驟 1：設定資源目錄

定義包含 DXF 原始檔案的資料夾。將佔位符替換為您機器上的實際路徑。

```java
String dataDir = "Your Document Directory" + "DXFDrawings/";
```

## 步驟 2：載入 DXF 圖紙

將 DXF 檔案載入至 `Image` 物件。Aspose.CAD 會自動偵測檔案格式。

```java
String srcFile = dataDir + "conic_pyramid.dxf";
Image image = Image.load(srcFile);
```

## 步驟 3：設定光柵化選項（選擇圖層）

在此告訴 Aspose.CAD 要渲染哪些圖層。範例僅保留預設圖層 `"0"`。若要匯出其他圖層，請將 `"0"` 替換為圖紙中實際的圖層名稱。

```java
CadRasterizationOptions rasterizationOptions = new CadRasterizationOptions();
rasterizationOptions.setPageWidth(1600);
rasterizationOptions.setPageHeight(1600);

List<String> stringList = new ArrayList<>(Arrays.asList("0"));
rasterizationOptions.setLayers(stringList);
```

**專業提示：** 您可以在 `stringList` 中加入多個圖層名稱（例如 `Arrays.asList("Layer1", "Layer2")`），一次匯出多個圖層。

## 步驟 4：建立 PDF 選項

將光柵化設定連結至 PDF 輸出配置。

```java
PdfOptions pdfOptions = new PdfOptions();
pdfOptions.setVectorRasterizationOptions(rasterizationOptions);
```

## 步驟 5：匯出為 PDF（從 DXF 建立 PDF）

最後，將選取的圖層儲存為 PDF 檔案。產生的 PDF 只會包含您指定的圖層之幾何圖形。

```java
image.save(dataDir + "conic_pyramid_layer_out_.pdf", pdfOptions);
```

## 常見問題與解決方案

| Issue | Reason | Fix |
|-------|--------|-----|
| **沒有輸出或空白 PDF** | 圖層名稱不匹配或大小寫敏感 | 確認 DXF 中的圖層名稱正確（可使用 CAD 檢視器），並在 `setLayers` 中使用相同名稱。 |
| **縮放不正確** | 頁面寬度/高度與圖紙單位不匹配 | 調整 `setPageWidth` / `setPageHeight`，或在 `CadRasterizationOptions` 上設定 `setResolution`。 |
| **授權例外** | 使用試用版卻未套用授權 | 使用以下程式碼載入授權檔案：`License license = new License(); license.setLicense("Aspose.CAD.Java.lic");`。 |

## 常見問與答

**Q: 我可以同時匯出多個圖層嗎？**  
A: 可以。修改 Step 3 中的 `stringList`，將所有想要的圖層名稱加入，例如 `Arrays.asList("LayerA", "LayerB")`。

**Q: Aspose.CAD 是否相容所有 DXF 版本？**  
A: Aspose.CAD 支援廣泛的 DXF 版本，從早期的 R12 到最新的發行版，確保高度相容性。

**Q: 匯出過程中發生錯誤時該如何處理？**  
A:載入與儲存程式碼包在 `try‑catch` 區塊中，並記錄 `Exception` 詳細資訊。這樣可優雅地處理檔案損毀或權限問題。

**Q: 生產環境是否需要商業授權？**  
A: 需要。臨時授權可用於評估，但購買授權可移除評估水印並解鎖全部功能。

**Q: 我可以在哪裡取得更多協助或範例？**  
A: 前往 [Aspose.CAD 論壇](https://forum.aspose.com/c/cad/19) 獲得社群支援，或查閱官方 API 文件取得更多程式碼範例。

## 結論

您現在已學會 **如何使用 Aspose.CAD for Java 匯出特定圖層以從 DXF 建立 PDF**。此技術讓您完整掌控產生 PDF 的視覺內容，非常適合輕量分享、自動化報告，或將 CAD 資料整合至更大型的 Java 應用程式。歡迎依專案需求試驗不同的光柵化設定、圖層選擇與 PDF 選項。

---

**最後更新：** 2025-11-30  
**測試環境：** Aspose.CAD for Java 24.11  
**作者：** Aspose  

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}