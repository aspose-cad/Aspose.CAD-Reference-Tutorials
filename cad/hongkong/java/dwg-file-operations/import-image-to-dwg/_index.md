---
date: 2026-01-12
description: 學習如何使用 Aspose.CAD for Java 為 DWG 檔案加入圖像，並將 DWG 轉換為 PDF。請跟隨我們的逐步指南，以提升開發效率。
linktitle: Import Image to DWG File Using Java
second_title: Aspose.CAD Java API
title: 使用 Aspose.CAD Java 輕鬆將圖像加入 DWG 檔案
url: /zh-hant/java/dwg-file-operations/import-image-to-dwg/
weight: 10
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# 輕鬆使用 Aspose.CAD Java 為 DWG 檔案加入影像

在現代 Java 應用程式中，**將影像加入 DWG** 檔案是一項常見需求——無論您是建立 CAD 檢視器、自動化圖紙更新，或是產生文件。Aspose.CAD for Java 為您提供一種直接、效能高的方式，將點陣圖直接嵌入 DWG 繪圖中，無需完整的 CAD 引擎。本教學將帶您完整走過從載入 DWG 到匯出結果為 PDF 的全過程。

## 快速解答
- **需要哪個函式庫？** Aspose.CAD for Java  
- **我也可以匯出成 PDF 嗎？** Yes – use `PdfOptions` with `CadRasterizationOptions`  
- **開發時需要授權嗎？** A free trial works for testing; a commercial license is required for production  
- **支援哪個 Java 版本？** Java 8 and higher  
- **實作需要多久時間？** About 10‑15 minutes for a basic image import

## 什麼是「將影像加入 dwg」？
將影像加入 DWG 檔案是指在圖紙的模型空間中插入一個點陣圖（PNG、JPEG 等）作為 `CadRasterImage` 物件。該影像成為 CAD 實體樹的一部份，且可像其他 CAD 物件一樣進行定位、縮放與裁剪。

## 為什麼使用 Aspose.CAD for Java 來將影像加入 dwg？
- **不需要 CAD 軟體** – API 於內部處理 DWG 解析。  
- **細緻的控制** 插入點、縮放向量與裁剪。  
- **內建 PDF 轉換**，讓您在同一工作流程中產生可列印的 PDF。  
- **跨平台** – 可在 Windows、Linux 與 macOS 上執行。

## 前置條件
- Aspose.CAD for Java: 確認已安裝 Aspose.CAD 函式庫。您可在此下載 [here](https://releases.aspose.com/cad/java/)。  
- Java Development Environment: JDK 8+ 與您喜愛的 IDE（IntelliJ、Eclipse、VS Code 等）。

## 匯入套件
```java
import com.aspose.cad.Image;
import com.aspose.cad.fileformats.cad.CadDrawTypeMode;
import com.aspose.cad.fileformats.cad.CadImage;
import com.aspose.cad.fileformats.cad.cadobjects.*;
import com.aspose.cad.imageoptions.CadRasterizationOptions;
import com.aspose.cad.imageoptions.PdfOptions;
```

## 步驟說明

### 步驟 1：載入 DWG 檔案
首先，指向包含 DWG 圖紙的資料夾，並使用 `Image.load` 載入。
```java
String dataDir = "Your Document Directory" + "DWGDrawings/";
String srcFile = dataDir + "Drawing11.dwg";
Image image = Image.load(srcFile);
```

### 步驟 2：定義點陣圖定義
建立一個 `CadRasterImageDef`，用以參照您欲嵌入的外部 PNG。建構子接受影像檔名與其像素尺寸。
```java
CadRasterImageDef cadRasterImageDef = new CadRasterImageDef("road-sign-custom.png", 640, 562);
cadRasterImageDef.setObjectHandle("A3B4");
```

### 步驟 3：設定插入點與縮放向量
插入點決定影像左下角出現的位置。**U** 與 **V** 向量分別控制水平與垂直縮放。
```java
Cad3DPoint insertionPoint = new Cad3DPoint(26.77, 22.35);
Cad3DPoint uVector = new Cad3DPoint(0.0061565450840500831, 0);
Cad3DPoint vVector = new Cad3DPoint(0, 0.0061565450840500822);
```

### 步驟 4：建立 CadRasterImage 物件
將定義、插入點與向量結合成 `CadRasterImage`。若只想顯示圖片的部分區域，亦可設定裁剪邊界。
```java
CadRasterImage cadRasterImage = new CadRasterImage(cadRasterImageDef, insertionPoint, uVector, vVector);
cadRasterImage.setImageDefReference("A3B4");
cadRasterImage.setDisplayFlags((short)7);
cadRasterImage.setClippingState((short)0);
cadRasterImage.getClipBoundaryVertexList().add(new Cad2DPoint(-0.5, 0.5));
cadRasterImage.getClipBoundaryVertexList().add(new Cad2DPoint(639.5, 561.5));
```

### 步驟 5：將影像加入模型空間
將點陣圖插入 `*Model_Space` 區塊，接著更新圖紙的物件集合，使定義得以儲存。
```java
CadImage cadImage = ((CadImage)(image));
cadImage.getBlockEntities().get_Item("*Model_Space").addEntity(cadRasterImage);
CadBaseObject[] objs = cadImage.getObjects();
CadBaseObject[] arr = new CadBaseObject[objs.length + 1];
int ind = 0;
for (CadBaseObject obj : objs)
{
    arr[ind] = obj;
    ind++;
}
arr[ind] = cadRasterImageDef;
cadImage.setObjects(arr);
```

### 步驟 6：設定 PDF 匯出選項（可選）
若您也需要圖紙的 PDF 版，請同時設定 `PdfOptions` 與 `CadRasterizationOptions`。此步驟示範如何在同一流程中 **將 dwg 轉換為 pdf**。
```java
PdfOptions pdfOptions = new PdfOptions();
CadRasterizationOptions cadRasterizationOptions = new CadRasterizationOptions();
pdfOptions.setVectorRasterizationOptions(cadRasterizationOptions);
cadRasterizationOptions.setDrawType(CadDrawTypeMode.UseObjectColor);
cadRasterizationOptions.setPageHeight(1600);
cadRasterizationOptions.setPageWidth(1600);
cadRasterizationOptions.setLayouts(new String[] {"Model"});
```

### 步驟 7：儲存產生的 PDF
最後，將修改後的圖紙匯出為 PDF 檔案。使用相同的 `image` 實例，因此 PDF 會呈現新加入的點陣圖。
```java
image.save((srcFile + "_generated.pdf"), pdfOptions);
```

依照上述步驟，您即可快速 **將影像加入 dwg** 檔案，並在需要時 **將 dwg 儲存為 pdf**。

## 常見問題與解決方案
- **影像未顯示** – 請確認影像檔案路徑 (`road-sign-custom.png`) 正確，且影像尺寸與傳入 `CadRasterImageDef` 的值相符。  
- **縮放不正確** – 調整 U 與 V 向量；它們代表每個像素的圖紙單位。  
- **PDF 為空白** – 確認 `CadRasterizationOptions.setDrawType` 設為 `UseObjectColor` 或其他適當模式。

## 常見問答

**Q: Aspose.CAD for Java 是否相容於所有 Java 開發環境？**  
A: 是的，Aspose.CAD for Java 相容於大多數 Java 開發環境。

**Q: 我可以在商業專案中使用 Aspose.CAD for Java 嗎？**  
A: 可以，您可在商業專案中使用 Aspose.CAD for Java。請前往 [here](https://purchase.aspose.com/buy) 了解授權細節。

**Q: 是否提供 Aspose.CAD for Java 的免費試用？**  
A: 有，您可在 [here](https://releases.aspose.com/) 取得免費試用。

**Q: 如何取得 Aspose.CAD for Java 的支援？**  
A: 您可在 [Aspose.CAD forum](https://forum.aspose.com/c/cad/19) 尋求支援。

**Q: 我可以取得 Aspose.CAD for Java 的臨時授權嗎？**  
A: 可以，您可在 [here](https://purchase.aspose.com/temporary-license/) 取得臨時授權。

---

**最後更新：** 2026-01-12  
**測試環境：** Aspose.CAD for Java 24.11  
**作者：** Aspose  

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}