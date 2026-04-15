---
date: 2026-01-07
description: 學習如何使用 Aspose.CAD for Java 將 CAD 匯出為 SVG。此一步步指南將示範如何將 DWG 轉換為 SVG、設定
  SVG 顏色模式，並將函式庫整合至您的 Java 專案。
linktitle: Export to SVG
second_title: Aspose.CAD Java API
title: 使用 Aspose.CAD for Java 將 CAD 匯出為 SVG
url: /zh-hant/java/cad-to-pdf-and-svg-export-options/export-to-svg/
weight: 12
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# 使用 Aspose.CAD for Java 匯出 CAD 為 SVG

## 簡介

歡迎來到 Aspose.CAD for Java 的世界，這是一個功能強大的函式庫，讓開發人員能輕鬆操作 CAD 圖面。無論您是資深開發者或是 CAD 領域的新手，本完整指南將一步步帶您完成 **export CAD to SVG**，示範如何將 DWG 轉換為 SVG、設定 SVG 色彩模式，並將 API 整合至您的 Java 專案。

## 快速解答
- **「export CAD to SVG」是什麼意思？** 它會將 CAD 圖面（例如 DWG）轉換成可在瀏覽器中顯示的可縮放向量圖形（Scalable Vector Graphics）檔案。  
- **哪個函式庫負責轉換？** Aspose.CAD for Java 提供簡易的 API 完成此任務。  
- **開發時需要授權嗎？** 免費試用可用於測試；正式上線需購買商業授權。  
- **我可以控制 SVG 的顏色輸出嗎？** 可以，您可以設定 SVG 色彩模式（例如灰階）。  
- **還需要其他軟體嗎？** 只需 Java 執行環境與 Aspose.CAD JAR 檔案。

## 先決條件

在開始教學之前，請確保您已具備以下條件：

- **Java 開發環境**：確保系統已安裝 Java。  
- **Aspose.CAD 函式庫**：從 [download link](https://releases.aspose.com/cad/java/) 下載並安裝 Aspose.CAD for Java。  
- **文件目錄**：為您的 CAD 圖面建立一個資料夾，並記下其路徑。

## 匯入命名空間

在此步驟中，我們將匯入必要的命名空間，以展開 Aspose.CAD 的旅程。請依照下列步驟操作：

### 步驟 1：開啟您的 Java 項目
在您選擇的 IDE 中開啟 Java 專案。

### 步驟 2：新增 Aspose.CAD 庫
將 Aspose.CAD 函式庫加入專案。您可以透過將 JAR 檔案加入專案的相依性來完成。

### 步驟 3：匯入命名空間
在 Java 類別中匯入所需的命名空間：

```java
import com.aspose.cad.Image;
import com.aspose.cad.imageoptions.SvgOptions;
import com.aspose.cad.imageoptions.SvgColorMode;
```

## 匯出 CAD 為 SVG

既然已完成前置作業，現在讓我們一步步執行 **export CAD to SVG**，使用 Aspose.CAD for Java。

### 步驟 1：指定資源目錄
定義資源目錄的路徑，即存放 CAD 圖面的資料夾：

```java
String dataDir = "Your Document Directory" + "DWGDrawings/";
```

### 步驟 2：載入 CAD 圖形
使用 Aspose.CAD 函式庫載入 CAD 圖面：

```java
Image image = Image.load(dataDir + "meshes.dwg");
```

### 步驟 3：設定 SVG 匯出選項
設定 SVG 匯出選項以自訂輸出內容。此處我們 **set SVG color mode** 為灰階，並指示匯出器將文字轉換為圖形：

```java
SvgOptions options = new SvgOptions();
options.setColorType(SvgColorMode.Grayscale);
options.setTextAsShapes(true);
```

### 步驟 4：另存為 SVG
將 CAD 圖面儲存為 SVG 檔案：

```java
image.save(dataDir + "meshes.svg");
```

> **Pro tip:** 若需 **convert DWG to SVG** 且保留顏色，請將 `SvgColorMode.Grayscale` 改為 `SvgColorMode.FullColor`。

恭喜！您已成功使用 Aspose.CAD for Java 將 CAD 圖面匯出為 SVG。

## 為何使用 Aspose.CAD 匯出 CAD 為 SVG？
- **高保真度**：向量資料完整保留，確保 SVG 與原始 CAD 圖面外觀完全相同。  
- **無外部相依**：轉換全程於 Java 內部執行，無需額外工具。  
- **可自訂輸出**：如 `setColorType` 等選項讓您決定 SVG 為灰階或全彩。

## 常見問題與解決方案
- **找不到檔案**：確認 `dataDir` 指向正確資料夾，且 DWG 檔名正確。  
- **SVG 輸出空白**：若圖面含文字需以圖形呈現，請確定已設定 `options.setTextAsShapes(true)`。  
- **不支援的 CAD 格式**：Aspose.CAD 支援 DWG、DXF、DWF 等多種格式，請參閱文件取得完整清單。

## 結論

在本教學中，我們探討了使用 Aspose.CAD for Java **export CAD to SVG** 的完整流程。憑藉直觀的 API 與強大的功能，Aspose.CAD 讓複雜的 CAD 操作變得簡單，為開發者提供了多元且可靠的工具。

## 常見問題解答

**Q: 可以使用相同程式碼將 DXF 檔案轉換為 SVG 嗎？**  
A: 可以，只要將檔名換成 DXF，即可由 API 處理兩種格式。

**Q: 如何將輸出改為全彩 SVG？**  
A: 在儲存前設定 `options.setColorType(SvgColorMode.FullColor);`。

**Q: 能否在產生的 SVG 中嵌入字型？**  
A: Aspose.CAD 目前會將文字轉換為圖形，無需嵌入字型。

**Q: 此函式庫能在 Linux 與 macOS 上執行嗎？**  
A: Java 函式庫與平台無關，只要有相容的 JVM 即可執行。

**Q: 本教學使用的 Aspose.CAD 版本為何？**  
A: 本範例測試於 Aspose.CAD for Java 24.10。

---

**Last Updated:** 2026-01-07  
**Tested With:** Aspose.CAD for Java 24.10  
**Author:** Aspose  

---

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}
