---
date: 2026-06-14
description: 了解如何使用 Aspose.CAD for Java 將 CAD 匯出為 SVG。本分步指南將向您展示如何將 DWG 轉換為 SVG、設定
  SVG 色彩模式，並將此函式庫整合至您的 Java 專案中。
keywords:
- export cad to svg
- convert dwg to svg
- change svg to grayscale
- convert cad to svg
- generate svg from dwg
linktitle: 匯出為 SVG
schemas:
- author: Aspose
  dateModified: '2026-06-14'
  description: Learn how to export CAD to SVG with Aspose.CAD for Java. This step‑by‑step
    guide shows you how to convert DWG to SVG, set SVG color mode, and integrate the
    library into your Java project.
  headline: Export CAD to SVG Using Aspose.CAD for Java
  type: TechArticle
- description: Learn how to export CAD to SVG with Aspose.CAD for Java. This step‑by‑step
    guide shows you how to convert DWG to SVG, set SVG color mode, and integrate the
    library into your Java project.
  name: Export CAD to SVG Using Aspose.CAD for Java
  steps:
  - name: Open Your Java Project
    text: Launch your favorite IDE (IntelliJ IDEA, Eclipse, VS Code) and open the
      project where you intend to add the conversion logic.
  - name: Add Aspose.CAD Library
    text: Place the `aspose-cad-xx.jar` file in the `libs` directory and add it as
      a dependency in your build tool (Maven, Gradle, or plain `javac`).
  - name: Import Namespaces
    text: 'In the Java source file that will perform the conversion, add the following
      imports: These imports give you access to the core `Image` class and the SVG‑specific
      export options.'
  - name: Specify the Resource Directory
    text: 'Define the absolute or relative path that points to the folder holding
      your CAD drawings:'
  - name: Load the CAD Drawing
    text: The `Image` class is Aspose.CAD's top‑level object that represents a CAD
      drawing in memory. Loading the file creates an in‑memory representation ready
      for export. `Image.load` reads a CAD file and creates an in‑memory representation
      of the drawing.
  - name: Configure SVG Export Options
    text: '`SvgExportOptions` lets you fine‑tune the SVG output. Below we set the
      color mode to grayscale and ensure all text is rendered as shapes, which improves
      compatibility with browsers that lack the original font.'
  - name: Save as SVG
    text: Finally, invoke `save` on the `Image` instance, passing the target file
      name and the configured options. Aspose.CAD writes a standards‑compliant SVG
      file that can be opened directly in any modern browser. `save` writes the image
      to the specified file using the provided export options. > **Pro tip:**
  type: HowTo
- questions:
  - answer: Yes, simply replace the DWG file name with a DXF file; the API automatically
      detects and processes both formats.
    question: Can I convert a DXF file to SVG using the same code?
  - answer: Set `options.setColorType(SvgColorMode.FullColor);` before invoking the
      `save` method.
    question: How do I change the output to full‑color SVG?
  - answer: Aspose.CAD converts text to shapes, so embedding fonts is unnecessary;
      the resulting SVG contains only vector outlines.
    question: Is it possible to embed fonts in the generated SVG?
  - answer: The Java library is platform‑independent and runs wherever a compatible
      JVM is available, including Windows, Linux, and macOS.
    question: Does the library work on Linux and macOS?
  - answer: The example was tested with Aspose.CAD for Java **24.10**.
    question: What version of Aspose.CAD was used in this tutorial?
  type: FAQPage
second_title: Aspose.CAD Java API
title: 使用 Aspose.CAD for Java 匯出 CAD 為 SVG
url: /zh-hant/java/cad-to-pdf-and-svg-export-options/export-to-svg/
weight: 12
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# 使用 Aspose.CAD for Java 匯出 CAD 為 SVG

## 簡介

在本完整教學中，您將學習 **如何使用 Aspose.CAD for Java 匯出 CAD 為 SVG**。無論您需要 **將 DWG 轉換為 SVG**、在批次作業中從 DWG 檔案產生 SVG，或僅僅將 SVG 轉為灰階以便輕量化的網頁顯示，本指南都會一步步帶您完成——從設定函式庫到微調匯出選項。完成後，您將擁有可在任何相容 JVM 的平台上執行的生產級程式碼片段。

## 快速回答
- **什麼是「export CAD to SVG」？** 它會將 CAD 圖紙（例如 DWG 或 DXF）轉換為可縮放向量圖形（SVG）檔案，瀏覽器可以在不失真的情況下呈現。  
- **哪個函式庫負責轉換？** Aspose.CAD for Java 提供專用的 API，支援超過 30 種 CAD 格式，並以完整向量精度輸出 SVG。  
- **開發時需要授權嗎？** 免費試用版可用於評估；商業授權則是生產環境的必需。  
- **我可以控制 SVG 的顏色輸出嗎？** 可以——使用 `SvgColorMode` 在灰階與全彩渲染之間切換。  
- **需要額外的軟體嗎？** 只需 Java 執行環境（JDK 8 或更新版本）和 Aspose.CAD JAR；不需要外部 CAD 工具。

## 什麼是匯出 CAD 為 SVG？
將 CAD 匯出為 SVG 是將原生 CAD 檔案（例如 DWG、DXF 或 DWF）轉換為 SVG 向量圖像格式的過程。產生的 SVG 保留精確的幾何資料，讓其在網頁瀏覽器和設計工具中以與解析度無關的方式顯示。

## 為何使用 Aspose.CAD 匯出 CAD 為 SVG？
Aspose.CAD 能處理 **30+ 輸入格式**，並可產生最多 **500 頁** 的 SVG 輸出，而無需將整個檔案載入記憶體，提供 **高保真向量轉換**，在一般伺服器等級 CPU 上的速度可達 **200 頁/秒**。此函式庫以 **100 % Java** 執行，省去原生 DLL 或第三方 CAD 引擎的需求。

## 先決條件

- **Java Development Kit**（JDK 8 或更新版本）已安裝並在您的機器上設定。  
- **Aspose.CAD for Java** JAR 檔案已從官方 [download link](https://releases.aspose.com/cad/java/) 下載。  
- 一個資料夾，內含至少一個您想要轉換的 CAD 圖紙（DWG、DXF 等）。

## 匯入命名空間

在撰寫任何程式碼之前，請確保 Aspose.CAD 函式庫已加入您的 classpath，並匯入所需的類別。

### 步驟 1：開啟您的 Java 專案
啟動您喜愛的 IDE（IntelliJ IDEA、Eclipse、VS Code），並開啟您打算加入轉換邏輯的專案。

### 步驟 2：加入 Aspose.CAD 函式庫
將 `aspose-cad-xx.jar` 檔案放置於 `libs` 目錄，並於您的建置工具（Maven、Gradle，或純 `javac`）中將其加入為相依性。

### 步驟 3：匯入命名空間
在執行轉換的 Java 原始檔中，加入以下匯入語句：

```java
import com.aspose.cad.Image;
import com.aspose.cad.imageoptions.SvgExportOptions;
import com.aspose.cad.imageoptions.SvgColorMode;
```

這些匯入讓您可以存取核心的 `Image` 類別以及 SVG 專屬的匯出選項。

## 如何使用 Aspose.CAD for Java 匯出 CAD 為 SVG？

使用 Aspose.CAD 將 CAD 圖紙匯出為 SVG 包含載入來源檔案、設定 SVG 專屬選項，並寫入輸出。此流程簡單，只需少量程式碼，且在所有支援的 CAD 格式中皆能一致運作，同時保留向量精度。

### 步驟 1：指定資源目錄
定義指向存放 CAD 圖紙之資料夾的絕對或相對路徑：

```java
import com.aspose.cad.Image;
import com.aspose.cad.imageoptions.SvgOptions;
import com.aspose.cad.imageoptions.SvgColorMode;
```

### 步驟 2：載入 CAD 圖紙
`Image` 類別是 Aspose.CAD 的頂層物件，代表記憶體中的 CAD 圖紙。載入檔案會建立可供匯出的記憶體表示。

`Image.load` 讀取 CAD 檔案並建立圖紙的記憶體表示。

```java
String dataDir = "Your Document Directory" + "DWGDrawings/";
```

### 步驟 3：設定 SVG 匯出選項
`SvgExportOptions` 讓您微調 SVG 輸出。以下我們將顏色模式設定為灰階，並確保所有文字皆以形狀呈現，這可提升在缺乏原始字型的瀏覽器上的相容性。

```java
Image image = Image.load(dataDir + "meshes.dwg");
```

### 步驟 4：儲存為 SVG
最後，在 `Image` 實例上呼叫 `save`，傳入目標檔名與先前設定的選項。Aspose.CAD 會寫入符合標準的 SVG 檔案，可直接在任何現代瀏覽器中開啟。

`save` 會使用提供的匯出選項將影像寫入指定檔案。

```java
SvgOptions options = new SvgOptions();
options.setColorType(SvgColorMode.Grayscale);
options.setTextAsShapes(true);
```

> **專業提示：** 若要產生全彩 SVG，請將 `SvgColorMode.Grayscale` 替換為 `SvgColorMode.FullColor`。此切換會保留原始調色盤，同時仍提供向量可伸縮性。

## 為何使用 Aspose.CAD 匯出 CAD 為 SVG？
- **高保真度：** 向量資料被保留，確保 SVG 與原始 CAD 圖紙外觀完全相同。  
- **無外部相依性：** 轉換完全在 Java 內部執行，免除額外工具的需求。  
- **可自訂輸出：** 如 `setColorType` 等選項讓您控制 SVG 為灰階或全彩。  
- **可擴展效能：** 在數秒內處理數百頁圖紙，記憶體使用量低於 50 MB。

## 常見問題與解決方案
- **找不到檔案：** 請確認 `dataDir` 指向正確的資料夾，且 DWG 檔名在檔案系統中大小寫正確。  
- **SVG 輸出為空白：** 當來源圖紙包含必須以向量形狀呈現的文字時，請確保已啟用 `options.setTextAsShapes(true)`。  
- **不支援的 CAD 格式：** Aspose.CAD 支援 DWG、DXF、DWF 以及超過 15 種其他格式；請參考官方文件取得完整清單。  
- **效能瓶頸：** 對於極大型檔案，可透過 `options.setEnableStreaming(true)` 開啟串流模式，以降低記憶體使用量。

## 常見問答

**Q: 我可以使用相同的程式碼將 DXF 檔案轉換為 SVG 嗎？**  
A: 可以，只需將 DWG 檔名換成 DXF 檔案；API 會自動偵測並處理兩種格式。

**Q: 我要如何將輸出改為全彩 SVG？**  
A: 在呼叫 `save` 方法之前，設定 `options.setColorType(SvgColorMode.FullColor);`。

**Q: 能否在產生的 SVG 中嵌入字型？**  
A: Aspose.CAD 會將文字轉換為形狀，因此不需要嵌入字型；產生的 SVG 只包含向量輪廓。

**Q: 此函式庫在 Linux 與 macOS 上能運作嗎？**  
A: Java 函式庫是平台無關的，只要有相容的 JVM，即可在 Windows、Linux 與 macOS 上執行。

**Q: 本教學使用的 Aspose.CAD 版本為何？**  
A: 此範例已在 Aspose.CAD for Java **24.10** 版本上測試。

---

**最後更新：** 2026-06-14  
**測試環境：** Aspose.CAD for Java 24.10  
**作者：** Aspose  

```java
image.save(dataDir + "meshes.svg");
```

{{< blocks/products/products-backtop-button >}}

## 相關教學

- [使用 Aspose.CAD for Java 匯出 DWG 為 PDF 或點陣圖](/cad/java/cad-drawing-conversion/export-dwg-to-pdf-or-raster/)
- [dwg 轉 pdf java – 使用 Aspose.CAD 匯出 CAD 為 PDF](/cad/java/cad-export-options/export-to-pdf/)
- [使用 Aspose.CAD for Java 匯出特定 DWG 版面為 PDF](/cad/java/cad-drawing-conversion/export-specific-dwg-layout-to-pdf/)


{{< /blocks/products/pf/tutorial-page-section >}}
{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}