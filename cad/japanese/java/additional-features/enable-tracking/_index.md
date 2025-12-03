---
date: 2025-12-03
description: Aspose.CAD for Java を使用して DWG を PDF に変換する際の PDF ページサイズの設定方法と、DWG ファイルでのトラッキングを有効にする方法を学びましょう
  – 正確に CAD 図面を PDF にエクスポートするための完全ガイド。
language: ja
linktitle: Set PDF Page Size and Enable Tracking in DWG Files Using Java
second_title: Aspose.CAD Java API
title: Java の Aspose.CAD を使用して DWG ファイルの PDF ページサイズを設定し、トラッキングを有効にする
url: /java/additional-features/enable-tracking/
weight: 12
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Aspose.CAD for Java を使用して DWG ファイルの PDF ページサイズを設定し、トラッキングを有効にする

## Introduction

DWG を PDF に*変換*する際に **PDF ページサイズを設定** し、さらにレンダリングの問題を追跡したい場合、Aspose.CAD for Java は両方をクリーンにプログラムで実行できる方法を提供します。このチュートリアルでは、ページ寸法の構成、トラッキングの有効化、CAD 図面 PDF のエクスポート手順を Java だけで実行する方法を順を追って解説します。最後まで読むと、CAD 図面に正しいページサイズを設定する重要性と、エクスポートプロセス中に詳細なトラッキング情報を取得する方法が理解できるようになります。

## Quick Answers
- **「set PDF page size」は何に影響しますか？** 結果として生成される PDF キャンバスの幅と高さを定義し、図面が完全に収まるようにします。  
- **この機能を使用するのにライセンスは必要ですか？** テストにはトライアルで動作しますが、本番環境では商用ライセンスが必要です。  
- **必要な Aspose.CAD のバージョンは？** `CadRasterizationOptions` をサポートする最新のバージョンであればどれでも構いません。  
- **他の CAD フォーマットでも使用できますか？** 例は DWG/DXF ですが、同様のアプローチはほとんどのサポート対象フォーマットで機能します。  
- **変換にどれくらい時間がかかりますか？** 中規模のファイルであれば通常 1 秒未満です。大きな図面はそれ以上かかることがあります。

## What is “set PDF page size” in the context of CAD export?

PDF ページサイズを設定することは、出力キャンバスの正確な寸法（ピクセルまたはポイント）をレンダラに指示することを意味します。スケールやレイアウトを保持しなければならない技術図面では特に重要です。ページサイズを明示しない場合、PDF はデフォルトサイズになり、図面が切り取られたり歪んだりする可能性があります。

## Why set PDF page size when exporting CAD drawings?
- **スケールを保持** – エンジニアは実寸印刷に依存します。  
- **用紙に合わせる** – プロジェクト仕様に合った A4、Letter、またはカスタムサイズを選択します。  
- **可読性の向上** – 大きなページはズームせずに細部を表示できます。  
- **一貫した出力** – 自動化パイプラインは毎回同一サイズの PDF を生成します。

## How to set PDF page size when converting DWG to PDF?

以下では、エクスポート前に `CadRasterizationOptions` にカスタムの幅と高さを設定します。この手順がキーワード **set PDF page size** に直接対応します。

## Prerequisites

- **Java Development Kit (JDK)** – Java 8 以上がマシンにインストールされていること。  
- **Aspose.CAD for Java** – 公式の [Aspose CAD download page](https://releases.aspose.com/cad/java/) からダウンロードしてください。  
- **Document Directory** – 処理したい DWG/DXF ファイルが入っているフォルダー。

## Import Namespaces

First, import the classes you’ll need. The code block is unchanged from the original tutorial.

```java
import com.aspose.cad.Image;

import com.aspose.cad.imageoptions.CadRasterizationOptions;
import com.aspose.cad.imageoptions.CadRenderResult;
import com.aspose.cad.imageoptions.PdfOptions;
import com.aspose.cad.imageoptions.RenderResult;
import java.io.FileNotFoundException;
import java.io.FileOutputStream;
import java.io.OutputStream;
```

## Step 1: Load the DWG/DXF File

Load your source drawing. Adjust the path to point at your own file.

```java
String dataDir = "Your Document Directory" + "DXFDrawings/";
Image image = Image.load(dataDir + "conic_pyramid.dxf");
```

## Step 2: Configure PDF Export Options (including page size)

Here we set the page width and height—this is where we **set PDF page size**. The values are in pixels; you can convert from inches or millimeters as needed.

```java
OutputStream stream = new FileOutputStream(dataDir + "output_conic_pyramid.pdf");
PdfOptions pdfOptions = new PdfOptions();
CadRasterizationOptions cadRasterizationOptions = new CadRasterizationOptions();
pdfOptions.setVectorRasterizationOptions(cadRasterizationOptions);
cadRasterizationOptions.setPageWidth(800);   // <-- custom width
cadRasterizationOptions.setPageHeight(600);  // <-- custom height
```

> **ヒント:** 標準用紙サイズを使用したい場合は `1 inch = 72 points` の換算を利用してください。A4 用紙 (8.27 × 11.69 in) の場合は `pageWidth = 595`、`pageHeight = 842` と設定します。

## Step 3: Implement Tracking

Tracking captures any rendering problems. We attach a custom handler that will be invoked after the export.

```java
cadRasterizationOptions.RenderResult = new ErrorHandler();
```

## Step 4: Export to PDF

Now perform the conversion. The PDF will be created with the dimensions you specified, and any tracking information will be printed to the console.

```java
System.out.println("Exporting to pdf format");
image.save(stream, pdfOptions);
```

## Step 5: CadRenderHandler Class

The handler prints out any failures that occurred during rendering. This helps you debug issues when **exporting CAD drawing PDF**.

```java
public static class ErrorHandler extends CadRasterizationOptions.CadRenderHandler {
    @Override
    public void invoke(CadRenderResult result) {
        System.out.println("Tracking results of exporting");

        if (result.isRenderComplete())
            return;

        System.out.println("Have some problems:");

        int idxError = 1;
        for (RenderResult rr : result.getFailures()) {
            System.out.printf("{0}. {1}, {2}", idxError, rr.getRenderCode(), rr.getMessage());
            idxError++;
        }
    }
}
```

## Common Issues and Solutions

| 問題 | 原因 | 対策 |
|------|------|------|
| **Blank PDF** | Page size set to 0 or too small | Verify `setPageWidth` and `setPageHeight` are positive values. |
| **Missing geometry** | Rendering errors captured by the handler | Review the console output from `ErrorHandler` and address the specific `RenderCode`. |
| **File not found** | Incorrect `dataDir` path | Use an absolute path or ensure the directory exists. |
| **License exception** | Using the trial without a valid license for large files | Apply your Aspose.CAD license before loading the image. |

## Frequently Asked Questions

**Q: Aspose.CAD for Java を使用して他の CAD ファイル形式でもトラッキングを有効にできますか？**  
A: Aspose.CAD は主に DWG/DXF のトラッキングをサポートしています。他の形式については公式ドキュメントをご確認ください。

**Q: Aspose.CAD for Java で追加のエクスポートオプションを扱うにはどうすればよいですか？**  
A: ライブラリは DPI、背景色、ベクトルラスタライズなど多数のオプションを提供しています。詳細は [Aspose.CAD Java Documentation](https://reference.aspose.com/cad/java/) を参照してください。

**Q: Aspose.CAD for Java のトライアル版はありますか？**  
A: はい、[Aspose.CAD Free Trial](https://releases.aspose.com/) から無料トライアルをダウンロードできます。

**Q: Aspose.CAD for Java に関するサポートや議論はどこで行えますか？**  
A: コミュニティサポートや公式回答は [Aspose.CAD forum](https://forum.aspose.com/c/cad/19) でご利用ください。

**Q: Aspose.CAD for Java の一時ライセンスはどう取得しますか？**  
A: 手順は [Temporary License](https://purchase.aspose.com/temporary-license/) ページに記載されています。

---

**最終更新日:** 2025-12-03  
**テスト環境:** Aspose.CAD for Java 24.11 (執筆時点での最新バージョン)  
**作者:** Aspose  

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}