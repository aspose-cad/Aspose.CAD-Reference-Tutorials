---
date: 2026-07-18
description: Aspose.CAD for .NET を使用して CAD を PNG にエクスポートする方法。IFC ファイルを high‑quality
  PNG 画像に迅速かつ確実に変換します。
keywords:
- how to export cad to png
- Aspose.CAD IFC conversion
- CAD to PNG .NET
lastmod: 2026-07-18
linktitle: IFC ファイルを PNG にエクスポート
og_description: Aspose.CAD for .NET を使用して CAD を PNG にエクスポートする方法。コード不要のセットアップで、IFC
  ファイルを PNG 画像に step‑by‑step で変換する方法を学びます。
og_image_alt: Guide showing IFC to PNG conversion with Aspose.CAD for .NET
og_title: CAD を PNG にエクスポートする方法 – Aspose.CAD .NET ガイド
schemas:
- author: Aspose
  dateModified: '2026-07-18'
  description: How to export CAD to PNG using Aspose.CAD for .NET. Convert IFC files
    to high‑quality PNG images quickly and reliably.
  headline: How to Export CAD to PNG – Exporting IFC Files with Aspose.CAD
  type: TechArticle
- questions:
  - answer: No, Aspose.CAD for .NET is specifically designed for Windows environments.
    question: Can I use Aspose.CAD for .NET on macOS or Linux?
  - answer: Yes, you can obtain a temporary license from [here](https://purchase.aspose.com/temporary-license/)
      for evaluation.
    question: Is a temporary license available for testing purposes?
  - answer: Visit the [Aspose.CAD forum](https://forum.aspose.com/c/cad/19) for community
      support and discussions.
    question: How can I get support for Aspose.CAD?
  - answer: Refer to the [Aspose.CAD documentation](https://reference.aspose.com/cad/net/)
      for detailed information and examples.
    question: Where can I find comprehensive documentation?
  - answer: Check the documentation or seek assistance on the [Aspose.CAD forum](https://forum.aspose.com/c/cad/19).
    question: What if I encounter issues during installation?
  type: FAQPage
second_title: Aspose.CAD .NET - CAD and BIM File Format
tags:
- export cad
- Aspose.CAD
- IFC to PNG
- .NET image conversion
title: CAD を PNG にエクスポートする方法 – Aspose.CAD を使用した IFC ファイルのエクスポート
url: /ja/net/exporting-to-image-formats/exporting-ifc-files-to-png/
weight: 10
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# CADをPNGにエクスポートする方法 – Aspose.CADでIFCファイルをエクスポート

## はじめに

If you need to **how to export cad to png**, Aspose.CAD for .NET offers a reliable, code‑free way to turn IFC (Industry Foundation Classes) models into crisp PNG raster images. In this tutorial we’ll walk through the entire workflow—from installing the library to saving the final PNG—so you can integrate the conversion into any .NET application with confidence.

## クイック回答
- **変換を処理するライブラリは何ですか？** Aspose.CAD for .NET.
- **サポートされているソース形式は？** IFC (Industry Foundation Classes) ファイル.
- **ターゲット画像形式は？** PNG、サイズと解像度を完全に制御できます.
- **最低 .NET バージョンは？** .NET Framework 4.5+ または .NET Core 3.1+.
- **ライセンス要件は？** 本番使用のための有効な Aspose.CAD ライセンス.

## “CADをPNGにエクスポートする方法”とは何ですか？

このフレーズは、IFC などの CAD ベースのファイル形式を Portable Network Graphics (PNG) ラスタ画像に変換するプロセスを指します。この変換により、CAD ビジュアルをウェブページ、ドキュメント、レポートに簡単に表示、共有、埋め込むことができ、軽量で広くサポートされているフォーマットで視覚的忠実度を保ち、専用の CAD ビューアは不要です。

## なぜこの変換に Aspose.CAD を使用するのか？

Aspose.CAD は **50 以上の CAD および BIM フォーマット** をサポートし、ファイル全体をメモリにロードせずに数百ページに及ぶ IFC モデルを処理できます。標準的なサーバーハードウェア上で高速かつメモリ効率の良い変換を実現し、レイヤー、線幅、カラー マッピングを自動的に処理するとともに、出力品質やサイズに関する豊富な設定オプションを提供します。

## 前提条件

### 1. Aspose.CAD のインストール
Aspose.CAD for .NET がインストールされていることを確認してください。リリースページから[こちら](https://releases.aspose.com/cad/net/)でダウンロードできます。

### 2. ドキュメント ディレクトリ
ドキュメント用の指定ディレクトリを作成します。提供された例では、変数 `MyDir` がドキュメントディレクトリを表します。

## 名前空間のインポート
前提条件が整ったので、.NET プロジェクトで Aspose.CAD を使用するために必要な名前空間をインポートします。

```csharp
using Aspose.CAD.ImageOptions;
using System;
using System.Collections.Generic;
using System.Linq;
using System.Text;
using Aspose.CAD.FileFormats.Ifc;
```

## CAD を PNG にエクスポートする方法は？

`IfcImage` は、PNG などのラスタ形式にラスタライズできる IFC CAD 画像を表します。`new IfcImage("source.ifc")` で IFC ファイルをロードし、`RasterizationOptions` でラスタライズを設定し、`PngOptions` で PNG 固有の設定を行い、最後に `Save(outputPath, pngOptions)` を呼び出します。このエンドツーエンドのフローにより、数行のコードで CAD モデルを高解像度 PNG に変換し、レイヤー、カラー、線幅を自動的に処理します。

## 手順 1: IFC ファイルのロード
`IfcImage` クラスは IFC モデルをロードし、ラスタライズの準備を行います。

```csharp
string MyDir = "Your Document Directory";
string sourceFilePath = MyDir + "example.ifc";
using (IfcImage cadImage = (IfcImage)Image.Load(sourceFilePath))
{
```

この手順では、Aspose.CAD の `IfcImage` オブジェクトを初期化し、IFC ファイルをロードします。

## 手順 2: ラスタライズ オプションの設定
`RasterizationOptions` クラスは、ベクトル データをラスタ画像に変換する方法を定義し、ページ幅、高さ、背景色などを設定できます。

```csharp
    CadRasterizationOptions rasterizationOptions = new CadRasterizationOptions();
   
    rasterizationOptions.PageWidth = 100;
    rasterizationOptions.PageHeight = 100;
```

PNG 出力のページ幅と高さを設定するために、ラスタライズ オプションを定義します。

## 手順 3: PNG オプションの設定
`PngOptions` クラスは、圧縮レベルやカラー深度など、PNG 出力に特有の設定を保持します。

```csharp
    PngOptions pngOptions = new PngOptions();
    pngOptions.VectorRasterizationOptions = rasterizationOptions;
```

PNG オプションを作成し、先に定義したラスタライズ オプションと関連付けます。

## 手順 4: 出力パスの指定
出力パスは、生成された PNG ファイルの保存先を決定します。

```csharp
    // Set output path as well
    string outPath = sourceFilePath + ".png";
    cadImage.Save(outPath, pngOptions);
}
```

PNG ファイルの出力パスを定義し、ソースファイルと同じ名前で拡張子が ".png" になるようにします。最後に、変換された画像を保存します。

## よくある問題と解決策
- **フォントや線スタイルが欠如している場合:** ソース IFC がすべての必要なリソースを参照していることを確認してください。Aspose.CAD は可能な限り欠損したアセットを埋め込みます。
- **大きなファイルでメモリ使用量が急増する場合:** `RasterizationOptions` の `MemoryLimit` プロパティを使用してメモリ使用量を上限設定します。
- **色が正しくない場合:** ソース IFC のカラー定義が IFC スキーマに準拠しているか確認してください。Aspose.CAD は標準のカラー マッピングを尊重します。

## よくある質問

**Q: Aspose.CAD for .NET を macOS や Linux で使用できますか？**  
**A:** いいえ、Aspose.CAD for .NET は Windows 環境向けに設計されています。

**Q: テスト目的で一時ライセンスは利用できますか？**  
**A:** はい、評価用に[こちら](https://purchase.aspose.com/temporary-license/)から一時ライセンスを取得できます。

**Q: Aspose.CAD のサポートはどのように受けられますか？**  
**A:** コミュニティサポートやディスカッションは[ Aspose.CAD フォーラム](https://forum.aspose.com/c/cad/19)をご覧ください。

**Q: 包括的なドキュメントはどこで見つけられますか？**  
**A:** 詳細情報やサンプルは[ Aspose.CAD ドキュメント](https://reference.aspose.com/cad/net/)をご参照ください。

**Q: インストール中に問題が発生した場合はどうすればよいですか？**  
**A:** ドキュメントを確認するか、[Aspose.CAD フォーラム](https://forum.aspose.com/c/cad/19)で支援を求めてください。

---

**最終更新日:** 2026-07-18  
**テスト済みバージョン:** Aspose.CAD 24.11 for .NET  
**作者:** Aspose

## 関連チュートリアル

- [Aspose.CAD for .NET で CAD 図面をラスタ画像に変換](/cad/net/cad-drawing-manipulation/convert-cad-drawing-to-raster-image/)
- [Aspose.CAD for .NET で STL から PNG への変換を簡単に](/cad/net/stl-file-export/exporting-stl-files-to-png/)
- [Aspose.CAD for .NET で CAD レイアウトをラスタ画像形式にエクスポート](/cad/net/cad-export-formats/export-cad-layouts-to-raster-image-formats/)


{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}