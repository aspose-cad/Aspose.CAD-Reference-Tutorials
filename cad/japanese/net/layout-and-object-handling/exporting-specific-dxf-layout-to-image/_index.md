---
date: 2026-09-09
description: .NETで特定のDXFレイアウトをJPEGまたはPNGに変換するために、Aspose CAD exportの使用方法を学びましょう。迅速な結果を得るためのステップバイステップの手順をご案内します。
keywords:
- aspose cad export
- how to export dxf
- convert dxf to jpeg
- batch export dxf
- convert dwf to jpeg
lastmod: 2026-09-09
linktitle: 特定のDXFレイアウトを画像にエクスポート
og_description: .NETで特定のDXFレイアウトをJPEGまたはPNGに変換するために、Aspose CAD exportの使用方法を学びましょう。迅速な結果を得るためのステップバイステップの手順をご案内します。
og_image_alt: Tutorial showing Aspose CAD export of DXF layout to JPEG image in .NET
og_title: Aspose CAD export – 特定のDXFレイアウトを画像にエクスポート
schemas:
- author: Aspose
  dateModified: '2026-09-09'
  description: Learn how to use Aspose CAD export to convert a specific DXF layout
    to JPEG or PNG in .NET. Follow step‑by‑step instructions for fast results.
  headline: Aspose CAD export – exporting a specific DXF layout to an image
  type: TechArticle
- description: Learn how to use Aspose CAD export to convert a specific DXF layout
    to JPEG or PNG in .NET. Follow step‑by‑step instructions for fast results.
  name: Aspose CAD export – exporting a specific DXF layout to an image
  steps:
  - name: set up your project
    text: Create a new .NET project or open an existing one where you plan to implement
      the Aspose.CAD functionality.
  - name: load CAD image
    text: 'Use the following code to load a CAD image from your specified file path:'
  - name: configure rasterization options
    text: 'Set up the rasterization options, specifying the page width and height:'
  - name: iterate over layers
    text: 'Retrieve the layers from the CAD image and iterate through them:'
  - name: export layers to images
    text: For each layer, export it to a JPEG image using the configured options.
      The `JpegOptions` class defines JPEG‑specific settings such as quality and compression
      level. Repeat these steps for each layer in the CAD image.
  type: HowTo
- questions:
  - answer: Yes – you can script a folder scan and call the same export routine for
      each file; the library is optimized for high‑throughput scenarios.
    question: Does Aspose CAD export support batch processing of thousands of files?
  - answer: Absolutely – set the `JpegQuality` property in `RasterizationOptions`
      to a value between 0 and 100.
    question: Can I control the JPEG quality level?
  - answer: Yes – change the `Save` format to `SaveFormat.Png` and adjust any transparency
      settings as needed.
    question: Is it possible to export a layout as a PNG instead of JPEG?
  - answer: Aspose.CAD supports .NET Framework 4.5+, .NET Core 3.1+, .NET 5, .NET
      6 and later.
    question: What .NET versions are officially supported?
  - answer: The engine streams pages to disk and never loads the full document into
      memory, allowing processing of multi‑gigabyte files on modest hardware.
    question: How does Aspose CAD export handle very large drawings?
  type: FAQPage
second_title: Aspose.CAD .NET - CAD and BIM File Format
tags:
- aspose cad
- dxf export
- cad to image
- c# cad processing
- cad conversion
title: Aspose CAD export – 特定のDXFレイアウトを画像にエクスポート
url: /ja/net/layout-and-object-handling/exporting-specific-dxf-layout-to-image/
weight: 10
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Aspose CAD エクスポート – 特定の DXF レイアウトを画像にエクスポート

## はじめに

Aspose CAD エクスポートを使用すると、個々の DXF レイアウトを含む CAD 図面を、サードパーティの CAD ソフトウェアを必要とせずに JPEG や PNG などのラスタ画像に直接変換できます。このチュートリアルでは、DXF ファイルを読み込み、必要なレイアウトを選択し、数行の .NET コードで画像にエクスポートする方法を学びます。

## クイック回答
- **必要なライブラリは何ですか？** Aspose.CAD for .NET (the Aspose CAD export component).  
- **1つのレイアウトだけをエクスポートできますか？** Yes – you can select a specific layout before rasterizing.  
- **サポートされている出力形式は？** JPEG, PNG, BMP, TIFF and more.  
- **本番環境でライセンスは必要ですか？** A valid Aspose.CAD license is required for non‑trial use.  
- **.NET 6+ で動作しますか？** Absolutely – the library targets .NET Framework 4.5+, .NET Core 3.1+, .NET 5/6/7.

## Aspose CAD エクスポートとは？

Aspose CAD エクスポートは、CAD および BIM ファイルをラスタまたはベクタ画像に変換する Aspose.CAD ライブラリの一部です。AutoCAD をインストールせずに、任意のレイアウト、ページ、レイヤーを単一呼び出し API でレンダリングできます。このコンポーネントはバッチ処理、高解像度出力、アンチエイリアシングや背景色制御などの高度なレンダリングオプションもサポートします。

## DXF 変換に Aspose CAD エクスポートを使用する理由

Aspose CAD エクスポートは **30 以上の CAD/BIM フォーマット** をサポートし、**10 000 ページ** までのファイルをメモリ使用量 **50 MB 未満** に抑えながらストリーミングで処理できます。エンジンは線の太さ、色、ハッチパターンを保持し、元の図面と一致するピクセルパーフェクトな JPEG 出力を提供します。また、高価なデスクトップ CAD のインストールが不要になるため、自動変換パイプラインをシンプルかつコスト効率的に実現できます。

## 前提条件

- Aspose.CAD ライブラリ: Aspose.CAD ライブラリを[リリースページ](https://releases.aspose.com/cad/net/)からダウンロードしてインストールしてください。  
- 開発環境: マシンに .NET 開発環境が設定されていることを確認してください。

## 名前空間のインポート

.NET プロジェクトで、Aspose.CAD が提供する機能にアクセスするために必要な名前空間をインポートします。

```csharp
using System;
```

## 特定の DXF レイアウトを画像にエクスポートする方法？

DXF ファイルを読み込み、目的のレイアウトを選択し、ラスタライズオプションを設定してから画像として保存します。典型的な図面であれば、数回のメソッド呼び出しだけで 1 秒未満で完了します。`CadImage` クラスはメモリにロードされた CAD 図面を表し、レイヤー、レイアウト、レンダリングオプションへのアクセスを提供します。

### 手順 1: プロジェクトの設定

Aspose.CAD 機能を実装する新しい .NET プロジェクトを作成するか、既存のプロジェクトを開きます。

### 手順 2: CAD 画像の読み込み

指定したファイルパスから CAD 画像をロードするコードは次のとおりです。

```csharp
string MyDir = "Your Document Directory";
string sourceFilePath = MyDir + "for_layers_test.dwf";

using (var image = (Aspose.CAD.FileFormats.Cad.CadImage)Aspose.CAD.Image.Load(sourceFilePath))
{
    // Your code for further steps will go here.
}
```

### 手順 3: ラスタライズオプションの設定

ページの幅と高さを指定してラスタライズオプションを設定します。

```csharp
var rasterizationOptions = new Aspose.CAD.ImageOptions.CadRasterizationOptions();
rasterizationOptions.PageWidth = 500;
rasterizationOptions.PageHeight = 500;
```

### 手順 4: レイヤーの反復処理

CAD 画像からレイヤーを取得し、ループで処理します。

```csharp
var layersList = image.Layers;
foreach (var layerName in layersList.GetLayersNames())
{
    // Your code for further steps will go here.
}
```

### 手順 5: レイヤーを画像にエクスポート

各レイヤーについて、設定したオプションを使用して JPEG 画像にエクスポートします。`JpegOptions` クラスは品質や圧縮レベルなど JPEG 固有の設定を定義します。

```csharp
rasterizationOptions.Layers = new string[] { layerName };
var options = new Aspose.CAD.ImageOptions.JpegOptions();
options.VectorRasterizationOptions = rasterizationOptions;
image.Save(layerName + "_out.jpg", options);
```

これらの手順を CAD 画像の各レイヤーに対して繰り返します。

## DXF レイアウトを画像にバッチエクスポートする方法

すべての DXF ファイルをフォルダーに配置し、各ファイルをループで処理して目的のレイアウトを選択し、同じエクスポートロジックを呼び出します。この方法により、数十件の図面を一度に変換でき、自動化パイプラインに最適です。同一のラスタライズおよび保存設定を再利用することで、バッチ全体で一貫した出力品質が保証されます。

## Aspose CAD で DWF を JPEG に変換する方法

Aspose CAD エクスポートは DWF ファイルも扱えます。`CadImage.Load` で DWF を読み込み、同じラスタライズオプションを設定し、JPEG 形式で `Save` を呼び出します。API は DXF のワークフローと同一なので、コードベースを再利用できます。この統一インターフェイスにより、追加のコード分岐なしで混在する CAD ファイルコレクションの変換が簡素化されます。

## よくある問題と解決策
- **レイアウト名が見つからない:** CAD ファイルのレイヤーマネージャに表示されている名前とレイアウト識別子が一致しているか確認してください。  
- **大きなファイルでメモリが急増:** メモリ使用量を抑えるために、ストリーミングを有効にする `LoadOptions` を使用して `CadImage.Load` を呼び出してください。  
- **色が正しくない:** 白いキャンバスが必要な場合は、`RasterizationOptions` の `BackgroundColor` プロパティが `Color.White` に設定されていることを確認してください。

## FAQ

### Q1: Aspose.CAD を他の .NET フレームワークで使用できますか？
A1: はい、Aspose.CAD はさまざまな .NET フレームワークと互換性があり、開発ニーズに柔軟に対応できます。

### Q2: Aspose.CAD 用の一時ライセンスはありますか？
A2: はい、[一時ライセンスページ](https://purchase.aspose.com/temporary-license/)から Aspose.CAD の一時ライセンスを取得できます。

### Q3: Aspose.CAD のサポートはどこで受けられますか？
A3: [Aspose.CAD フォーラム](https://forum.aspose.com/c/cad/19)でコミュニティサポートと支援を受けられます。

### Q4: Aspose.CAD の無料トライアルはありますか？
A4: はい、[Aspose.CAD 無料トライアルページ](https://releases.aspose.com/)で無料トライアルを試すことができます。

### Q5: Aspose.CAD の詳細なドキュメントはどこにありますか？
A5: 詳細は包括的な [Aspose.CAD ドキュメント](https://reference.aspose.com/cad/net/)をご参照ください。

## よくある質問

**Q: Aspose CAD エクスポートは数千ファイルのバッチ処理をサポートしていますか？**  
A: はい、フォルダーをスキャンするスクリプトを作成し、各ファイルに同じエクスポート手順を呼び出すことで実現できます。ライブラリは高スループットシナリオ向けに最適化されています。

**Q: JPEG の品質レベルを制御できますか？**  
A: もちろんです。`RasterizationOptions` の `JpegQuality` プロパティを 0〜100 の値に設定してください。

**Q: レイアウトを JPEG ではなく PNG としてエクスポートできますか？**  
A: はい、`Save` の形式を `SaveFormat.Png` に変更し、必要に応じて透過設定を調整してください。

**Q: 公式にサポートされている .NET バージョンは何ですか？**  
A: Aspose.CAD は .NET Framework 4.5+、.NET Core 3.1+、.NET 5、.NET 6 以降をサポートしています。

**Q: Aspose CAD エクスポートは非常に大きな図面をどのように処理しますか？**  
A: エンジンはページをディスクにストリーミングし、全文書をメモリにロードしないため、数ギガバイトのファイルでも低スペックのハードウェアで処理可能です。

---

**最終更新日:** 2026-09-09  
**テスト環境:** Aspose.CAD 24.12 for .NET  
**作者:** Aspose

## 関連チュートリアル

- [Aspose.CAD for .NET を使用して DXF を PNG に変換](/cad/net/cad-export-formats/export-cad-layouts-to-raster-image-formats/)
- [Aspose CAD の例: .NET でレイアウトをラスタ画像に変換](/cad/net/cad-drawing-manipulation/convert-layouts-to-raster-image/)
- [CAD ラスタライズオプションの設定方法 – Aspose.CAD で特定のレイアウトを PDF にエクスポート](/cad/net/advanced-export-techniques/exporting-specific-layouts-to-pdf/)


{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}