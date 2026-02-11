---
date: 2026-01-02
description: 學習如何將 DWG 匯出為 PDF、啟用隱藏線，並使用 Aspose.CAD for Java 將 DWG 轉換為 PDF，這是一個一步一步的教學。
linktitle: Export DWG as PDF with Hidden Lines Using Java
second_title: Aspose.CAD Java API
title: 匯出 DWG 為 PDF（含隱藏線） – Aspose.CAD for Java
url: /zh-hant/java/cad-text-and-formatting/support-hidden-lines-in-dwg/
weight: 11
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# 匯出 DWG 為 PDF（含隱藏線） – Aspose.CAD for Java

## 介紹

在本教學中，您將學會如何使用 Aspose.CAD for Java **匯出 DWG 為 PDF**，同時保留隱藏線。無論您需要 **將 DWG 轉換為 PDF**、製作 **dwg to pdf 教學** 風格的指南，或只是 **將 DWG 儲存為 PDF** 並支援隱藏線，我們都會一步步帶您完成。完成後，您將擁有一個可直接套用於任何 Java 專案的即用解決方案。

## 快速回答
- **本教學涵蓋什麼內容？** 使用 Aspose.CAD for Java 在匯出 DWG 為 PDF 時啟用隱藏線渲染。  
- **主要執行的操作是什麼？** `export dwg as pdf`。  
- **需要授權嗎？** 免費試用可用於測試；正式環境需購買商業授權。  
- **先決條件是什麼？** Java 開發環境、Aspose.CAD for Java 程式庫，以及 DWG 檔案。  
- **實作需要多長時間？** 基本設定約需 10‑15 分鐘。

## 什麼是「export dwg as pdf」？
將 DWG 檔案匯出為 PDF 會將向量式 CAD 圖面轉換為可攜式文件格式，同時保留圖層、線型以及可選的隱藏線渲染。這讓您能輕鬆與可能沒有 CAD 軟體的利害關係人分享設計。

## 為什麼在匯出時要啟用隱藏線？
隱藏線能在 2‑D 頁面上提供更清晰的複雜 3D 模型視覺呈現，只強調可見邊緣，提升可讀性，且常為工程文件的必要要求。

## 先決條件

1. **Aspose.CAD for Java** – 從官方網站下載程式庫，點擊[此處](https://releases.aspose.com/cad/java/)。  
2. **DWG 檔案** – 將來源 DWG 圖紙存放於已知目錄。  
3. **Java 開發環境** – JDK 8 以上以及您偏好的 IDE（Eclipse、IntelliJ 等）。  

現在環境已備妥，讓我們深入程式碼。

## 匯入命名空間

先匯入必要的類別，以便操作 CAD 圖像與 PDF 選項。

```java
import com.aspose.cad.Image;

import com.aspose.cad.fileformats.cad.CadImage;
import com.aspose.cad.imageoptions.CadRasterizationOptions;
import com.aspose.cad.imageoptions.PdfOptions;
import java.util.Arrays;
import java.util.List;
```

## 步驟 1：設定專案

建立 Java 專案並將 Aspose.CAD JAR 加入建置路徑。接著定義存放 DWG 檔案的目錄。

```java
String dataDir = "Your Document Directory" + "DWGDrawings/";
```

> **小技巧：** 使用絕對路徑或根據專案的 resources 資料夾設定相對路徑。

## 步驟 2：載入 DWG 檔案

將來源 DWG 檔案載入 `CadImage` 物件，以便後續操作。

```java
String sourceFilePath = dataDir + "Bottom_plate.dwg";
String outPath = dataDir + "Bottom_plate.pdf";
CadImage cadImage = (CadImage)Image.load(sourceFilePath);
```

## 步驟 3：設定光柵化選項

選取要包含的圖層，並將頁面大小設為與原始圖紙相同。此處透過指定版面來啟用隱藏線渲染。

```java
List<String> list = Arrays.asList("Print","L1_RegMark","L2_RegMark");
CadRasterizationOptions rasterizationOptions = new CadRasterizationOptions();
rasterizationOptions.setPageHeight(cadImage.getHeight());
rasterizationOptions.setPageWidth(cadImage.getWidth()) ;
rasterizationOptions.setLayers(list);
```

## 步驟 4：設定 PDF 選項

告訴 Aspose.CAD 將向量資料光柵化為 PDF，使用 “Model” 版面以保持隱藏線隱蔽。

```java
PdfOptions pdfOptions = new PdfOptions();
rasterizationOptions.setLayouts(new String[] { "Model" });
pdfOptions.setVectorRasterizationOptions(rasterizationOptions);
```

## 步驟 5：儲存結果

最後，將 DWG 匯出為 PDF 檔案。隱藏線會依您設定的版面正確呈現。

```java
cadImage.save(outPath, pdfOptions);
System.out.println("\nThe DWG file exported successfully to PDF.\nFile saved at " + dataDir);
```

> **常見陷阱：** 若忘記將版面設定為 `"Model"`，所有線條（包括隱藏線）都會在 PDF 中呈現為實線。

## 結論

您現在已掌握使用 Aspose.CAD for Java 以隱藏線支援 **匯出 DWG 為 PDF** 的完整生產就緒方法。此方式可整合至批次處理工具、Web 服務或桌面應用程式，以自動化 CAD 轉 PDF 的工作流程。

## 常見問題

### Q1：我可以在 Aspose.CAD for Java 中使用其他 CAD 檔案格式嗎？
A1：可以，Aspose.CAD 支援多種 CAD 格式，例如 DWG、DXF、DWF 等。

### Q2：Aspose.CAD for Java 有提供免費試用嗎？
A2：有，您可於[此處](https://releases.aspose.com/)取得免費試用。

### Q3：如何取得 Aspose.CAD for Java 的支援？
A3：請前往 Aspose.CAD 論壇[此處](https://forum.aspose.com/c/cad/19)取得社群支援。

### Q4：在哪裡可以找到 Aspose.CAD for Java 的詳細文件？
A4：請參考文件[此處](https://reference.aspose.com/cad/java/)。

### Q5：我可以購買 Aspose.CAD for Java 的臨時授權嗎？
A5：可以，您可於[此處](https://purchase.aspose.com/temporary-license/)取得臨時授權。

### Q6：此方法是否也適用於在無頭伺服器環境中將 DWG 轉換為 PDF？
A6：絕對可以。由於程式碼僅使用 Aspose.CAD API，無需任何 UI 相依，適合伺服器端自動化。

---

**最後更新:** 2026-01-02  
**測試環境:** Aspose.CAD for Java 24.12  
**作者:** Aspose  

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}