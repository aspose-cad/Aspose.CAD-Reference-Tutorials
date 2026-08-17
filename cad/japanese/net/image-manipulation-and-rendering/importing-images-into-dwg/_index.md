---
date: 2026-08-17
description: C# と Aspose.CAD for .NET を使用して DWG ファイルに画像を追加する方法を学びます。このガイドでは、画像のインポート、挿入ポイントの設定、PDF
  へのエクスポートの手順を説明します。
keywords:
- add image to dwg
- convert dwg to pdf
- set insertion point dwg
- embed png in dwg
- save dwg as pdf
lastmod: 2026-08-17
linktitle: C# で DWG ファイルに画像をインポートする方法
og_description: C# を使用して DWG ファイルに画像を追加する方法を学びます。このチュートリアルでは、画像のインポート、挿入ポイントの設定、Aspose.CAD
  を使用した DWG から PDF への変換について解説します。
og_image_alt: Guide showing C# code to embed an image into a DWG file using Aspose.CAD
og_title: C# と Aspose.CAD を使用して DWG ファイルに画像を追加する方法
schemas:
- author: Aspose
  dateModified: '2026-08-17'
  description: Learn how to add image to dwg files using C# and Aspose.CAD for .NET.
    This guide walks you through importing images, setting insertion points, and exporting
    to PDF.
  headline: How to add image to dwg files with C# using Aspose.CAD
  type: TechArticle
- description: Learn how to add image to dwg files using C# and Aspose.CAD for .NET.
    This guide walks you through importing images, setting insertion points, and exporting
    to PDF.
  name: How to add image to dwg files with C# using Aspose.CAD
  steps:
  - name: set up your document directory
    text: Prepare the folder that contains the source DWG and the image you want to
      embed.
  - name: load the dwg file
    text: The `CadImage` class represents a DWG drawing and provides access to its
      entities, layers, and metadata.
  - name: define the image properties
    text: Create an `Image` object that points to the raster file (e.g., PNG) and
      specify its format.
  - name: set insertion point dwg and vectors
    text: Specify where the image should appear inside the drawing and how it should
      be scaled. The insertion point is defined by a 2‑D coordinate, while the vectors
      control width and height.
  - name: create and configure the raster image
    text: Instantiate a `RasterImage` object, assign the image data, and set any additional
      rendering options.
  - name: add image to dwg file
    text: Insert the configured raster image into the DWG’s entities collection so
      it becomes part of the drawing.
  - name: save as pdf (export dwg to pdf)
    text: After embedding the image you can **convert dwg to pdf** or **save dwg as
      pdf** with a single call. This is useful for sharing the drawing with stakeholders
      who don’t have CAD software.
  type: HowTo
- questions:
  - answer: The core library is .NET‑specific, but Aspose offers equivalent APIs for
      Java, Python and other platforms.
    question: Can I use Aspose.CAD for .NET with other programming languages?
  - answer: Yes, you can explore a free trial on the [Aspose free trial page](https://releases.aspose.com/).
    question: Is a free trial available for Aspose.CAD?
  - answer: The documentation is available in the [Aspose.CAD .NET API reference](https://reference.aspose.com/cad/net/).
    question: Where can I find detailed documentation for Aspose.CAD?
  - answer: Visit the [temporary license page](https://purchase.aspose.com/temporary-license/)
      to get a temporary license.
    question: How do I obtain a temporary license for Aspose.CAD?
  - answer: Yes, you can seek support and engage with the community in the [Aspose.CAD
      community forum](https://forum.aspose.com/c/cad/19).
    question: Are there community forums for Aspose.CAD support?
  type: FAQPage
second_title: Aspose.CAD .NET - CAD and BIM File Format
tags:
- CAD
- Aspose.CAD
- C# image processing
- DWG manipulation
title: C# と Aspose.CAD を使用して DWG ファイルに画像を追加する方法
url: /ja/net/image-manipulation-and-rendering/importing-images-into-dwg/
weight: 11
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# C# と Aspose.CAD を使用して DWG ファイルに画像を追加する方法

## はじめに

DWG ファイルに画像を追加することは、ロゴや写真、ラスタ画像で CAD 図面を強化する必要がある場合の一般的な要件です。このチュートリアルでは、C# と Aspose.CAD for .NET を使用してプログラムで **add image to dwg** を行い、必要に応じて結果を PDF に変換する方法を学びます。手順は分割されているので、各セクションを自分のプロジェクトにコピー＆ペーストできます。

## クイック回答
- **どのライブラリがこの作業を処理しますか？** Aspose.CAD for .NET.
- **PNG ファイルを埋め込めますか？** Yes – PNG, JPEG, BMP and other raster formats are supported.
- **開発にライセンスは必要ですか？** A free trial works for testing; a commercial license is required for production.
- **PDF エクスポートはサポートされていますか？** Absolutely – you can convert the updated DWG to PDF in one line.
- **対応している .NET バージョンは何ですか？** .NET Framework 4.6+, .NET Core 3.1+, .NET 5/6/7.

## DWG ファイルとは？

DWG ファイルは Autodesk AutoCAD 図面のネイティブバイナリ形式で、ベクトルジオメトリ、レイヤー、メタデータを格納します。建築、エンジニアリング、建設の分野で広く使用されており、Aspose.CAD は AutoCAD をインストールせずにこの形式の読み書きが可能です。

## なぜ Aspose.CAD で DWG に画像を追加するのか？

Aspose.CAD は **50 以上の入力および出力形式** をサポートし、500 MB を超えるファイルでも全体をメモリに読み込まずに処理でき、ヘッドレスサーバー環境でも動作する決定的な API を提供します。これにより、DWG 図面の大量処理が高速かつ信頼性の高いものになります。

## 前提条件
- C# プログラミングの基本知識。
- Aspose.CAD for .NET がインストール済み。[Aspose.CAD for .NET ダウンロードページ](https://releases.aspose.com/cad/net/) からダウンロードできます。また、[Aspose リリースページ](https://releases.aspose.com/) で他の Aspose 製品も確認できます。
- Visual Studio 2022 以降の開発環境。

## Aspose.CAD を使用して DWG に画像を追加する方法

対象の DWG を読み込み、埋め込みたい画像を表すラスタ画像オブジェクトを作成し、挿入ポイントとスケーリングベクトルを設定してから画像を図面に添付します。最後に変更した DWG を保存するか、直接 PDF にエクスポートします。典型的な 2 ページ図面であれば、数秒未満で完了します。

### 名前空間のインポート
必要な CAD クラスを公開する名前空間をインクルードします。

```csharp
using Aspose.CAD.FileFormats.Cad;
using Aspose.CAD.FileFormats.Cad.CadObjects;
using Aspose.CAD.ImageOptions;
using System;
using System.Collections.Generic;
using System.Linq;
using System.Text;
```

### 手順 1: ドキュメントディレクトリの設定
ソース DWG と埋め込みたい画像が格納されているフォルダーを用意します。

```csharp
string MyDir = "Your Document Directory";
```

### 手順 2: DWG ファイルの読み込み
`CadImage` クラスは DWG 図面を表し、エンティティ、レイヤー、メタデータへのアクセスを提供します。

```csharp
string dwgPathToFile = MyDir + "Drawing11.dwg";
CadImage cadImage1 = (CadImage)Image.Load(dwgPathToFile);
```

### 手順 3: 画像プロパティの定義
ラスタファイル（例: PNG）を指す `Image` オブジェクトを作成し、その形式を指定します。

```csharp
CadRasterImageDef cadRasterImageDef = new CadRasterImageDef("road-sign-custom.png", 640, 562);
cadRasterImageDef.ObjectHandle = "A3B4";
```

### 手順 4: 挿入ポイントとベクトルの設定
画像を図面内のどこに表示し、どのように拡大縮小するかを指定します。挿入ポイントは 2 次元座標で定義され、ベクトルは幅と高さを制御します。

```csharp
Cad3DPoint insertionPoint = new Cad3DPoint(26.77, 22.35);
Cad3DPoint uVector = new Cad3DPoint(0.0061565450840500831, 0);
Cad3DPoint vVector = new Cad3DPoint(0, 0.0061565450840500822);
```

### 手順 5: ラスター画像の作成と設定
`RasterImage` オブジェクトをインスタンス化し、画像データを割り当て、必要に応じて追加のレンダリングオプションを設定します。

```csharp
CadRasterImage cadRasterImage = new CadRasterImage(cadRasterImageDef, insertionPoint, uVector, vVector);
cadRasterImage.ImageDefReference = "A3B4";
cadRasterImage.DisplayFlags = 7;
cadRasterImage.ClippingState = 0;
cadRasterImage.ClipBoundaryVertexList.Add(new Cad2DPoint(-0.5, 0.5));
cadRasterImage.ClipBoundaryVertexList.Add(new Cad2DPoint(639.5, 561.5));
```

### 手順 6: DWG ファイルに画像を追加
設定したラスタ画像を DWG のエンティティコレクションに挿入し、図面の一部として組み込みます。

```csharp
CadImage cadImage = (CadImage)cadImage1;
cadImage.BlockEntities["*Model_Space"].AddEntity(cadRasterImage);

List<CadBaseObject> list = new List<CadBaseObject>(cadImage.Objects);
list.Add(cadRasterImageDef);
cadImage.Objects = list.ToArray();
```

### 手順 7: PDF として保存 (DWG を PDF にエクスポート)
画像を埋め込んだ後、**convert dwg to pdf** または **save dwg as pdf** をワンコールで実行できます。CAD ソフトが無いステークホルダーと図面を共有する際に便利です。

```csharp
PdfOptions pdfOptions = new PdfOptions();
CadRasterizationOptions cadRasterizationOptions = new CadRasterizationOptions();
pdfOptions.VectorRasterizationOptions = cadRasterizationOptions;
cadRasterizationOptions.DrawType = CadDrawTypeMode.UseObjectColor;

cadRasterizationOptions.PageHeight = 1600;
cadRasterizationOptions.PageWidth = 1600;
cadRasterizationOptions.Layouts = new string[] { "Model" };
cadImage1.Save(MyDir + "export2.pdf", pdfOptions);
```

## 画像を埋め込んだ後に DWG を PDF に変換する方法

`CadImage` インスタンスの `Save` メソッドに `SaveFormat.Pdf` と、必要に応じてページサイズやラスタライズ、メタデータを制御する `PdfOptions` オブジェクトを渡します。Aspose.CAD は埋め込まれたラスタ画像、レイヤー、線幅を保持した忠実な PDF を生成し、任意のビューアで開くことができます。この変換はコード 1 行で実行されます。

## よくある問題と解決策
- **画像が誤った位置に表示される** – 挿入ポイント座標と方向ベクトルを再確認してください。これらは図面の原点に対して相対的です。
- **大きな画像でメモリが急増する** – 挿入前にラスタ画像の `Resize` オプションを使用するか、解像度の低いコピーで作業してください。
- **PDF エクスポートでベクトル品質が失われる** – ベクトルデータを保持する `PdfOptions` で保存していることを確認してください。ラスタ画像はそのまま埋め込まれます。

## よくある質問

**Q: Aspose.CAD for .NET を他のプログラミング言語で使用できますか？**  
A: コアライブラリは .NET 固有ですが、Aspose は Java、Python など他のプラットフォーム向けに同等の API を提供しています。

**Q: Aspose.CAD の無料トライアルは利用可能ですか？**  
A: はい、[Aspose 無料トライアルページ](https://releases.aspose.com/) で無料トライアルをお試しできます。

**Q: Aspose.CAD の詳細なドキュメントはどこで見つけられますか？**  
A: ドキュメントは [Aspose.CAD .NET API リファレンス](https://reference.aspose.com/cad/net/) にあります。

**Q: Aspose.CAD の一時ライセンスはどう取得しますか？**  
A: [一時ライセンスページ](https://purchase.aspose.com/temporary-license/) から取得できます。

**Q: Aspose.CAD のサポート用コミュニティフォーラムはありますか？**  
A: はい、[Aspose.CAD コミュニティフォーラム](https://forum.aspose.com/c/cad/19) でサポートや情報交換が可能です。

---

**Last Updated:** 2026-08-17  
**Tested With:** Aspose.CAD 24.11 for .NET  
**Author:** Aspose

## 関連チュートリアル

- [DWG を PDF またはラスタ画像にエクスポート - Aspose.CAD ガイド](/cad/net/advanced-export-techniques/exporting-dwg-to-pdf-or-raster-images/)
- [C# で DWG を DXF 形式にエクスポート - Aspose.CAD チュートリアル](/cad/net/advanced-export-techniques/exporting-dwg-to-dxf/)
- [特定レイアウトを PDF にエクスポート - Aspose.CAD ガイド](/cad/net/advanced-export-techniques/exporting-specific-layouts-to-pdf/)

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}