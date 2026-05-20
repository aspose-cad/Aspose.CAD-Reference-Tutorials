---
date: 2026-05-20
description: 了解如何使用 Aspose.CAD for Java 將圖像加入 DWG 檔案，並將 DWG 轉換為 PDF。請遵循我們的逐步指南，以提升開發效率。
keywords:
- add image to dwg
- convert dwg to pdf
- import image into dwg
- embed raster image dwg
- dwg file operations
linktitle: 使用 Java 將圖像匯入 DWG 檔案
schemas:
- author: Aspose
  dateModified: '2026-05-20'
  description: Learn how to add image to DWG files using Aspose.CAD for Java and also
    convert DWG to PDF. Follow our step-by-step guide for efficient development.
  headline: Add Image to DWG Files Effortlessly Using Aspose.CAD Java
  type: TechArticle
- description: Learn how to add image to DWG files using Aspose.CAD for Java and also
    convert DWG to PDF. Follow our step-by-step guide for efficient development.
  name: Add Image to DWG Files Effortlessly Using Aspose.CAD Java
  steps:
  - name: Load the DWG File
    text: First, point to the folder that contains your DWG drawing and load it with
      `Image.load`.
  - name: Define the Raster Image Definition
    text: The `CadRasterImageDef` class defines the external raster image resource
      to be embedded in the drawing.
  - name: Set Insertion Point and Scaling Vectors
    text: The insertion point determines where the lower‑left corner of the image
      will appear. The **U** and **V** vectors control horizontal and vertical scaling.
  - name: Create the CadRasterImage Object
    text: The `CadRasterImage` entity represents a raster picture placed in the DWG
      model space.
  - name: Add the Image to Model Space
    text: Insert the raster image into the `*Model_Space` block, then update the drawing’s
      object collection so the definition is saved.
  - name: Configure PDF Export Options (Optional)
    text: '`PdfOptions` specifies settings for saving a CAD drawing as a PDF file.
      `CadRasterizationOptions` defines how the CAD content is rasterized during PDF
      conversion.'
  - name: Save the Resulting PDF
    text: 'Finally, export the modified drawing as a PDF file. The same `image` instance
      is used, so the PDF reflects the newly added raster image. By following these
      steps, you can **add image to dwg** files quickly and also **save dwg as pdf**
      when needed, covering the most common **dwg file operations** in '
  type: HowTo
- questions:
  - answer: Yes, Aspose.CAD for Java works with any IDE that supports JDK 8+, including
      IntelliJ IDEA, Eclipse, and VS Code.
    question: Is Aspose.CAD for Java compatible with all Java development environments?
  - answer: Yes, you can use Aspose.CAD for Java for commercial projects. Visit **[here](https://purchase.aspose.com/buy)**
      for licensing details.
    question: Can I use Aspose.CAD for Java for commercial projects?
  - answer: Yes, you can access the free trial **[here](https://releases.aspose.com/)**.
    question: Is there a free trial available for Aspose.CAD for Java?
  - answer: You can seek support on the **[Aspose.CAD forum](https://forum.aspose.com/c/cad/19)**.
    question: How can I get support for Aspose.CAD for Java?
  - answer: Yes, you can get a temporary license **[here](https://purchase.aspose.com/temporary-license/)**.
    question: Can I obtain a temporary license for Aspose.CAD for Java?
  type: FAQPage
second_title: Aspose.CAD Java API
title: 使用 Aspose.CAD Java 輕鬆將圖像加入 DWG 檔案
url: /zh-hant/java/dwg-file-operations/import-image-to-dwg/
weight: 10
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# 使用 Aspose.CAD Java 輕鬆將圖像添加至 DWG 檔案

在現代 Java 應用程式中，**將圖像添加至 DWG** 檔案是一項常見需求——無論您是建立 CAD 檢視器、自動化圖紙更新，或是產生文件說明。Aspose.CAD for Java 為您提供一種簡單且高效能的方式，直接將點陣圖嵌入 DWG 繪圖中，無需完整的 CAD 引擎。本教學將帶您完整走過流程，從載入 DWG 到匯出為 PDF，並同時說明如何 **import image into dwg** 以及 **convert dwg to pdf** 於單一工作流程中。

## 快速解答
- **需要什麼函式庫？** Aspose.CAD for Java  
- **可以同時匯出為 PDF 嗎？** 可以 – 使用 `PdfOptions` 搭配 `CadRasterizationOptions`  
- **開發時需要授權嗎？** 免費試用可用於測試；正式上線需購買商業授權  
- **支援哪個 Java 版本？** Java 8 及以上  
- **實作需要多久？** 基本圖像匯入約需 10‑15 分鐘  

## 什麼是「將圖像添加至 dwg」？

將圖像添加至 DWG 檔案是指將點陣圖（PNG、JPEG 等）作為 **CadRasterImage** 實體嵌入繪圖的模型空間中，您可以為其設定位置、縮放，甚至裁切，就像其他 CAD 物件一樣。它會儲存在繪圖的物件表中，並由標準 CAD 檢視器顯示。

## 為何使用 Aspose.CAD for Java 來將圖像添加至 dwg？

您可以在不安裝任何第三方 CAD 軟體的情況下，將點陣圖嵌入 DWG 檔案，且 API 提供像素級的插入點、縮放向量與裁切邊界控制。Aspose.CAD 可處理高達 2 GB 的檔案，支援 **50+ 輸入與輸出格式**，且可在 Windows、Linux、macOS 上執行，讓您輕鬆將 CAD 操作整合至任何基於 Java 的後端。

## 前置條件
- **Aspose.CAD for Java** – 從官方網站 **[here](https://releases.aspose.com/cad/java/)** 下載最新 JAR。  
- **Java Development Kit** – JDK 8 或更新版本，搭配您慣用的 IDE（IntelliJ IDEA、Eclipse、VS Code 等）。  
- 有效的 **Aspose.CAD 授權** 用於正式環境（試用版可供實驗使用）。  

## 匯入套件
以下匯入語句帶入了用於圖像操作與 PDF 轉換的核心 Aspose.CAD 類別。  
```java
import com.aspose.cad.Image;
import com.aspose.cad.fileformats.cad.CadDrawTypeMode;
import com.aspose.cad.fileformats.cad.CadImage;
import com.aspose.cad.fileformats.cad.cadobjects.*;
import com.aspose.cad.imageoptions.CadRasterizationOptions;
import com.aspose.cad.imageoptions.PdfOptions;
```

## 步驟指南

### 步驟 1：載入 DWG 檔案
首先，指向包含 DWG 繪圖的資料夾，並使用 `Image.load` 載入檔案。  
```java
String dataDir = "Your Document Directory" + "DWGDrawings/";
String srcFile = dataDir + "Drawing11.dwg";
Image image = Image.load(srcFile);
```

### 步驟 2：定義光柵圖像定義
`CadRasterImageDef` 類別用於定義要嵌入繪圖的外部光柵圖像資源。  
```java
CadRasterImageDef cadRasterImageDef = new CadRasterImageDef("road-sign-custom.png", 640, 562);
cadRasterImageDef.setObjectHandle("A3B4");
```

### 步驟 3：設定插入點與縮放向量
插入點決定圖像左下角出現的位置。**U** 與 **V** 向量控制水平與垂直縮放。  
```java
Cad3DPoint insertionPoint = new Cad3DPoint(26.77, 22.35);
Cad3DPoint uVector = new Cad3DPoint(0.0061565450840500831, 0);
Cad3DPoint vVector = new Cad3DPoint(0, 0.0061565450840500822);
```

### 步驟 4：建立 CadRasterImage 物件
`CadRasterImage` 實體代表放置於 DWG 模型空間的光柵圖像。  
```java
CadRasterImage cadRasterImage = new CadRasterImage(cadRasterImageDef, insertionPoint, uVector, vVector);
cadRasterImage.setImageDefReference("A3B4");
cadRasterImage.setDisplayFlags((short)7);
cadRasterImage.setClippingState((short)0);
cadRasterImage.getClipBoundaryVertexList().add(new Cad2DPoint(-0.5, 0.5));
cadRasterImage.getClipBoundaryVertexList().add(new Cad2DPoint(639.5, 561.5));
```

### 步驟 5：將圖像加入模型空間
將光柵圖像插入 `*Model_Space` 區塊，然後更新繪圖的物件集合，使定義得以儲存。  
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
`PdfOptions` 指定將 CAD 繪圖儲存為 PDF 檔案的設定。`CadRasterizationOptions` 定義 PDF 轉換過程中的光柵化方式。  
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
最後，將修改後的繪圖匯出為 PDF 檔案。使用相同的 `image` 實例，確保 PDF 反映新加入的光柵圖像。  
```java
image.save((srcFile + "_generated.pdf"), pdfOptions);
```

透過上述步驟，您可以快速 **add image to dwg** 檔案，並在需要時 **save dwg as pdf**，一次完成最常見的 **dwg file operations**。

## 常見問題與解決方案
- **圖像未顯示** – 請確認圖像檔案路徑 (`road-sign-custom.png`) 正確，且圖像尺寸與傳入 `CadRasterImageDef` 的參數相符。  
- **縮放不正確** – 調整 U 與 V 向量；它們代表每個像素對應的繪圖單位。  
- **PDF 為空白** – 確認 `CadRasterizationOptions.setDrawType` 設為 `UseObjectColor` 或其他適當模式。  

## 常見問答

**Q: Aspose.CAD for Java 是否相容所有 Java 開發環境？**  
A: 是，Aspose.CAD for Java 可在任何支援 JDK 8+ 的 IDE 中使用，包括 IntelliJ IDEA、Eclipse 與 VS Code。

**Q: 我可以在商業專案中使用 Aspose.CAD for Java 嗎？**  
A: 可以，您可在商業專案中使用 Aspose.CAD for Java。授權細節請參閱 **[here](https://purchase.aspose.com/buy)**。

**Q: Aspose.CAD for Java 是否提供免費試用？**  
A: 有，您可在 **[here](https://releases.aspose.com/)** 取得免費試用版。

**Q: 如何取得 Aspose.CAD for Java 的支援？**  
A: 您可前往 **[Aspose.CAD forum](https://forum.aspose.com/c/cad/19)** 尋求協助。

**Q: 我可以取得 Aspose.CAD for Java 的臨時授權嗎？**  
A: 可以，請至 **[here](https://purchase.aspose.com/temporary-license/)** 取得臨時授權。

---

**最後更新：** 2026-05-20  
**測試環境：** Aspose.CAD for Java 24.11  
**作者：** Aspose  

{{< blocks/products/products-backtop-button >}}

## 相關教學

- [Export DWG to PDF or Raster Using Aspose.CAD for Java](/cad/java/cad-drawing-conversion/export-dwg-to-pdf-or-raster/)
- [Add Custom Properties DWG Files Using Aspose.CAD for Java](/cad/java/additional-features/add-custom-properties/)
- [Save CAD as PNG – Convert CAD Drawing to Raster Image Format Using Aspose.CAD for Java](/cad/java/cad-drawing-conversion/convert-cad-drawing-to-raster-image/)


{{< /blocks/products/pf/tutorial-page-section >}}
{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}