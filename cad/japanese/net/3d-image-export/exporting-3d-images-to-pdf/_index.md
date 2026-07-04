---
date: 2026-07-04
description: Aspose.CAD for .NET を使用して、3D CAD画像から PDF ページサイズを設定し、PDF をエクスポートする方法を学びます
  – DWG を PDF に変換し、CAD を PDF として保存するステップバイステップガイドです。
keywords:
- set pdf page size
- export pdf from cad
- convert dwg to pdf
- save cad as pdf
- cad to pdf tutorial
linktitle: 3D画像のPDFエクスポート
schemas:
- author: Aspose
  dateModified: '2026-07-04'
  description: Learn how to set PDF page size and export PDF from 3D CAD images using
    Aspose.CAD for .NET – a step‑by‑step guide to convert DWG to PDF and save CAD
    as PDF.
  headline: Set PDF page size – Export 3D Images to PDF with Aspose.CAD
  type: TechArticle
- description: Learn how to set PDF page size and export PDF from 3D CAD images using
    Aspose.CAD for .NET – a step‑by‑step guide to convert DWG to PDF and save CAD
    as PDF.
  name: Set PDF page size – Export 3D Images to PDF with Aspose.CAD
  steps:
  - name: Load the CAD Image
    text: '`Image` class represents a CAD drawing loaded into memory, ready for rasterization.'
  - name: Configure Rasterization Options (Save CAD as PDF)
    text: '`RasterizationOptions` class defines how the CAD data is rasterized, including
      page size, DPI, and whether 3‑D entities are rendered.'
  - name: Set PDF Options (Create PDF from CAD)
    text: '`PdfOptions` class holds the output format settings and links the rasterization
      options to PDF generation.'
  - name: Save as PDF (Generate PDF from 3D Model)
    text: '`Save` method on the `Image` object writes the rasterized content to the
      specified PDF file, producing a ready‑to‑share document.'
  type: HowTo
- questions:
  - answer: Yes, Aspose.CAD supports more than 50 input and output formats, including
      DWG, DXF, DGN, STL, and IFC, ensuring flexibility for any project.
    question: Is Aspose.CAD compatible with all CAD file formats?
  - answer: Absolutely. Set `PageWidth` and `PageHeight` in `RasterizationOptions`
      to any size in points, inches, or millimetres before calling `Save`.
    question: Can I customize the page dimensions when exporting to PDF?
  - answer: Yes, you can obtain temporary licenses for Aspose.CAD by visiting [Temporary
      License](https://purchase.aspose.com/temporary-license/).
    question: Are temporary licenses available for Aspose.CAD?
  - answer: Head to the [Aspose.CAD Forum](https://forum.aspose.com/c/cad/19) for
      expert help and peer‑to‑peer advice.
    question: Where can I find additional support or community discussions?
  - answer: Yes, you can explore the features of Aspose.CAD by accessing the [free
      trial](https://releases.aspose.com/).
    question: Is there a free trial version of Aspose.CAD?
  type: FAQPage
second_title: Aspose.CAD .NET - CAD and BIM File Format
title: PDFページサイズの設定 – Aspose.CADで3D画像をPDFにエクスポート
url: /ja/net/3d-image-export/exporting-3d-images-to-pdf/
weight: 10
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# 3D画像をPDFにエクスポート - Aspose.CAD チュートリアル

## はじめに

3‑D CAD 図面を PDF に変換する際に **PDF ページサイズを設定** したい場合は、ここが適切な場所です。このチュートリアルでは、CAD ファイルの読み込み、ラスタライズオプションの設定（カスタムページ寸法を含む）をステップバイステップで示し、Aspose.CAD for .NET を使用して高忠実度の PDF を生成する方法を解説します。最後まで読むと、**CAD から PDF をエクスポート**、**CAD を PDF として保存** ができ、AutoCAD をインストールせずにレイアウトの詳細をすべて制御できるようになります。

## クイック回答

- **「CAD から PDF をエクスポート」とは何ですか？** CAD 図面（DWG、DXF、DGN など）を、任意のデバイスで開くことができる PDF に変換します。  
- **どのライブラリが変換を実行しますか？** Aspose.CAD for .NET は、外部依存関係なしでラスタライズと PDF エクスポートを提供します。  
- **ライセンスは必要ですか？** 本番環境では一時ライセンスまたはフルライセンスが必要です。無料トライアルも利用可能です。  
- **カスタムページ寸法を設定できますか？** はい。`RasterizationOptions` の `PageWidth` と `PageHeight` を使用します。  
- **3‑D ジオメトリは保持されますか？** 3‑D エンティティはラスタライズされます。完全な 3‑D サポートを有効にするには `TypeOfEntities.Entities3D` を設定してください。  

## CAD のコンテキストで「PDF をエクスポート」とは何ですか？

CAD から PDF をエクスポートするとは、CAD 図面（DWG、DXF、DGN など）を PDF ファイルに変換することで、ベクターグラフィック、ラスタライズされた 3‑D ビュー、正確なページレイアウト情報を含めることができ、CAD ソフトウェアを持っていない人とも簡単に共有できるようにすることです。

## なぜ Aspose.CAD を使用して PDF をエクスポートするのか？

Aspose.CAD を使用すると、**PDF ページサイズを設定** でき、完全にマネージドな .NET コードだけで PDF をエクスポートできます。50 以上の CAD フォーマットに対応し、ファイル全体をメモリに読み込まずに最大 2 GB のファイルを処理でき、線幅や色、オプションの 3‑D エンティティのレンダリングを最大 1200 DPI のラスタライズで保持します。このライブラリは Windows、Linux、macOS 上で動作するため、生成された PDF はあらゆるプラットフォームで利用可能です。

## 前提条件

- **Aspose.CAD for .NET** がインストールされていること。以下の [Aspose.CAD for .NET ダウンロードページ](https://releases.aspose.com/cad/net/) からダウンロードしてください。  
- 変換したい CAD ファイルが入っているフォルダー（例: `C:\CAD\`）  
- .NET 6.0 以降（または .NET Framework 4.7.2）  

## 名前空間のインポート

`using` ステートメントは、ラスタライズと PDF オプションの操作に必要な Aspose.CAD 名前空間をインポートします。  

```csharp
using System;
using System.Collections.Generic;
using System.Linq;
using System.Text;
using System.Threading.Tasks;
using Aspose.CAD;
using Aspose.CAD.ImageOptions;
```

## ステップバイステップガイド

### CAD を PDF にエクスポートする際に PDF ページサイズを設定する方法

CAD ファイルを読み込み、`RasterizationOptions` でページ寸法を設定し、そのオプションを `PdfOptions` インスタンスに添付して `Save` を呼び出します。この 4 ステップのフローにより、出力サイズと品質を完全に制御でき、コードを簡潔に保つことができます。

### 手順 1: CAD 画像の読み込み

`Image` クラスは、メモリに読み込まれた CAD 図面を表し、ラスタライズの準備ができています。  

```csharp
string MyDir = "Your Document Directory";
string sourceFilePath = MyDir + "conic_pyramid.dxf";
using (Image cadImage = Image.Load(sourceFilePath))
{
    // Your code for loading the CAD image goes here
}
```

### 手順 2: ラスタライズオプションの設定（CAD を PDF として保存）

`RasterizationOptions` クラスは、ページサイズ、DPI、3‑D エンティティのレンダリング有無など、CAD データのラスタライズ方法を定義します。  

```csharp
CadRasterizationOptions rasterizationOptions = new CadRasterizationOptions();
rasterizationOptions.PageWidth = 500;
rasterizationOptions.PageHeight = 500;
// rasterizationOptions.TypeOfEntities = TypeOfEntities.Entities3D;

rasterizationOptions.Layouts = new string[] { "Model" };
```

### 手順 3: PDF オプションの設定（CAD から PDF を作成）

`PdfOptions` クラスは、出力フォーマット設定を保持し、ラスタライズオプションを PDF 生成に結び付けます。  

```csharp
PdfOptions pdfOptions = new PdfOptions();
pdfOptions.VectorRasterizationOptions = rasterizationOptions;
```

### 手順 4: PDF として保存（3D モデルから PDF を生成）

`Image` オブジェクトの `Save` メソッドは、ラスタライズされたコンテンツを指定された PDF ファイルに書き込み、共有可能なドキュメントを生成します。  

```csharp
MyDir = MyDir + "Export3DImagestoPDF_out.pdf";
cadImage.Save(MyDir, pdfOptions);
```

## よくある問題と解決策

| 問題 | 原因 | 対策 |
|-------|--------|-----|
| **出力 PDF が空白** | レイアウト名が間違っているか、`Model` レイアウトが存在しません。 | `rasterizationOptions.Layouts` が CAD ファイル内に存在するレイアウトと一致しているか確認してください。 |
| **解像度が低い** | デフォルトのラスタライズ DPI が低く設定されています。 | 保存前に `rasterizationOptions.Resolution = 300;` を設定してください。 |
| **3‑D エンティティが表示されない** | `TypeOfEntities` がコメントアウトされています。 | `rasterizationOptions.TypeOfEntities = TypeOfEntities.Entities3D;` のコメントを解除してください。 |
| **ライセンス例外** | ライセンスなしでトライアル版を使用しています。 | `License license = new License(); license.SetLicense("Aspose.CAD.lic");` を使用して一時または永続ライセンスを適用してください。 |

## よくある質問

**Q: Aspose.CAD はすべての CAD ファイル形式に対応していますか？**  
A: はい、Aspose.CAD は DWG、DXF、DGN、STL、IFC などを含む 50 以上の入力・出力形式をサポートしており、あらゆるプロジェクトに柔軟に対応できます。

**Q: PDF にエクスポートする際にページ寸法をカスタマイズできますか？**  
A: もちろんです。`Save` を呼び出す前に、`RasterizationOptions` の `PageWidth` と `PageHeight` をポイント、インチ、ミリメートルのいずれかの単位で任意のサイズに設定してください。

**Q: Aspose.CAD の一時ライセンスは利用可能ですか？**  
A: はい、[Temporary License](https://purchase.aspose.com/temporary-license/) にアクセスして Aspose.CAD の一時ライセンスを取得できます。

**Q: 追加のサポートやコミュニティディスカッションはどこで見つけられますか？**  
A: 専門家の支援やピアツーピアのアドバイスは、[Aspose.CAD Forum](https://forum.aspose.com/c/cad/19) にてご確認ください。

**Q: Aspose.CAD の無料トライアル版はありますか？**  
A: はい、[free trial](https://releases.aspose.com/) にアクセスして Aspose.CAD の機能をお試しいただけます。

## 結論

Aspose.CAD for .NET を使用して **PDF ページサイズを設定** し、**3D CAD 画像から PDF をエクスポート** する完全な本番対応手法が手に入りました。ラスタライズオプションを調整することで、解像度、ページレイアウト、3‑D エンティティのレンダリングを細かく調整し、あらゆる文書要件に対応できます。さまざまな DPI 設定やページ寸法を試して、ファイルサイズと視覚的忠実度の最適なバランスを実現してください。

{{< blocks/products/products-backtop-button >}}

## 関連チュートリアル

- [特定レイアウトを PDF にエクスポート - Aspose.CAD ガイド](/cad/net/advanced-export-techniques/exporting-specific-layouts-to-pdf/)
- [DWG を PDF またはラスタ画像にエクスポート - Aspose.CAD ガイド](/cad/net/advanced-export-techniques/exporting-dwg-to-pdf-or-raster-images/)
- [Aspose.CAD for .NET で DGN を PDF にエクスポート](/cad/net/cad-export-formats/export-dgn-to-pdf/)


{{< /blocks/products/pf/tutorial-page-section >}}
{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

--- 

**最終更新日:** 2026-07-04  
**テスト環境:** Aspose.CAD 24.11 for .NET  
**作者:** Aspose