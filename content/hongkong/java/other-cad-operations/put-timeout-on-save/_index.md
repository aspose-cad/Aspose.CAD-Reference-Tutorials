---
title: 使用 Aspose.CAD 儲存 CAD 時逾時
linktitle: 儲存超時
second_title: Aspose.CAD Java API
description: 了解如何使用 Aspose.CAD 來提高 Java 應用程式的效能。為 CAD 工程圖的儲存設定逾時。請遵循我們的逐步指南。
type: docs
weight: 15
url: /zh-hant/java/other-cad-operations/put-timeout-on-save/
---
## 介紹

歡迎閱讀有關使用 Aspose.CAD for Java 設定儲存逾時的教學課程。在本指南中，我們將引導您完成設定儲存 CAD 繪圖逾時的過程，以提高應用程式的效能。 Aspose.CAD for Java 是一個功能強大的程式庫，可讓您在 Java 應用程式中無縫地使用 CAD 檔案。

## 先決條件

在深入學習本教程之前，請確保您具備以下先決條件：
-  Aspose.CAD for Java 程式庫：確保您已將 Aspose.CAD for Java 程式庫整合到您的專案中。您可以從以下位置下載該程式庫[網站](https://releases.aspose.com/cad/java/).
- 開發環境：使用所有必要的工具和相依性設定 Java 開發環境。

## 導入包

首先，將所需的套件匯入到您的 Java 專案中。在 Java 檔案的開頭新增以下行：

```java
import com.aspose.cad.Image;
import com.aspose.cad.InterruptionTokenSource;
import com.aspose.cad.fileformats.cad.CadImage;
import com.aspose.cad.imageoptions.CadRasterizationOptions;
import com.aspose.cad.imageoptions.PdfOptions;
import java.util.concurrent.TimeUnit;
```

現在，讓我們將範例程式碼分解為逐步說明：

## 第 1 步：設定來源目錄和輸出目錄

```java
final String SourceDir = Utils.getDataDir_DWGDrawings();
final String OutputDir = Utils.getDataDir_Output();
```

確保您的 CAD 工程圖具有正確的來源目錄和輸出目錄。

## 步驟2：建立中斷令牌來源

```java
final InterruptionTokenSource source = new com.aspose.cad.InterruptionTokenSource();
```

初始化中斷令牌來源以管理保存作業期間的中斷。

## 第 3 步：載入 CAD 圖紙

```java
final CadImage cadImageBig = (CadImage)Image.load(SourceDir + "Drawing11.dwg");
```

將 CAD 圖紙加載到`CadImage`目的。

## 步驟 4：配置光柵化選項

```java
CadRasterizationOptions rasterizationOptionsBig = new CadRasterizationOptions();
rasterizationOptionsBig.setPageWidth(cadImageBig.getSize().getWidth() / 2);
rasterizationOptionsBig.setPageHeight(cadImageBig.getSize().getHeight() / 2);
```

配置 CAD 繪圖的光柵化選項。

## 步驟 5：配置 PDF 選項

```java
final PdfOptions CADfBig = new PdfOptions();
CADfBig.setVectorRasterizationOptions(rasterizationOptionsBig);
CADfBig.setInterruptionToken(source.getToken());
```

使用向量光柵化選項和中斷標記來設定 PDF 選項。

## 第 6 步：超時儲存繪圖

```java
cadImageBig.save(OutputDir + "PutTimeoutOnSave_out.pdf", CADfBig);
```

使用指定的超時將 CAD 繪圖儲存到 PDF 檔案。

## 第 7 步：處理中斷

```java
java.lang.Thread thread = new java.lang.Thread(new Runnable() {
    @Override
    public void run() {
        try {
            cadImageBig.save(OutputDir + "PutTimeoutOnSave_out.pdf", CADfBig);
        } catch (Throwable th) {
            System.out.println("interrupted !!!");
        }
    }
});
thread.start();
TimeUnit.SECONDS.sleep(3);
source.interrupt();
thread.join();
```

創建一個線程來處理保存操作並在指定的超時後中斷它。

## 結論

恭喜！您已經成功學習如何使用 Aspose.CAD for Java 設定儲存逾時。此功能可以大大提高您的 CAD 相關應用程式的效率。

## 常見問題解答

### Q1: 如何下載 Aspose.CAD for Java？

 A1：您可以從[發布頁面](https://releases.aspose.com/cad/java/).

### Q2：在哪裡可以找到 Aspose.CAD for Java 的文檔？

 A2：請參閱[文件](https://reference.aspose.com/cad/java/)以獲得全面的資訊。

### Q3：有免費試用嗎？

A3：是的，您可以從以下位置獲得免費試用[這個連結](https://releases.aspose.com/).

### Q4：如何取得臨時駕照？

 A4：參觀[這裡](https://purchase.aspose.com/temporary-license/)了解臨時許可證詳細資訊。

### Q5: 需要協助或有疑問嗎？

 A5：前往[Aspose.CAD論壇](https://forum.aspose.com/c/cad/19)以獲得社區支持。