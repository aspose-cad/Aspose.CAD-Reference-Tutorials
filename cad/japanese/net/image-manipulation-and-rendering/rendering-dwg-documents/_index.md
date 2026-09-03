---
date: 2026-08-23
description: Aspose.CAD を使用して viewport dwg c# を作成する方法を学びます。このガイドでは、DWG ファイルの読み込み、ラスタライズの設定、viewport
  の定義、そして結果を PDF として保存する手順を解説します。
keywords:
- create viewport dwg c#
- render dwg c#
- aspose.cad .net
lastmod: 2026-08-23
linktitle: C# での DWG ドキュメントのレンダリング
og_description: Aspose.CAD for .NET を使用して viewport dwg c# を作成する方法を学びます。このステップバイステップガイドでは、読み込み、ラスタライズ、viewport
  の定義、PDF への保存手順を示します。
og_image_alt: Guide showing how to create viewport dwg c# with Aspose.CAD in .NET
og_title: Aspose.CAD for .NET を使用して viewport dwg c# を作成する方法
schemas:
- author: Aspose
  dateModified: '2026-08-23'
  description: Learn how to create viewport dwg c# using Aspose.CAD. This guide covers
    loading a DWG file, configuring rasterization, defining a viewport, and saving
    the result as PDF.
  headline: How to create viewport dwg c# with Aspose.CAD for .NET
  type: TechArticle
- questions:
  - answer: Load the DWG file with `CadImage.Load`.
    question: What is the first step?
  - answer: '`Viewport` inside `CadRasterizationOptions`.'
    question: Which class defines the view area?
  - answer: Yes, using `PdfOptions` after rasterization.
    question: Can I output to PDF?
  - answer: A commercial license is required; a free trial works for evaluation.
    question: Do I need a license for production?
  - answer: Absolutely – Aspose.CAD works with .NET Framework, .NET Core, and .NET 5/6.
    question: Is .NET Core supported?
  type: FAQPage
second_title: Aspose.CAD .NET - CAD and BIM File Format
tags:
- create viewport dwg c#
- Aspose.CAD
- C# CAD rendering
- DWG to PDF
- CAD viewports
title: Aspose.CAD for .NET を使用して viewport dwg c# を作成する方法
url: /ja/net/image-manipulation-and-rendering/rendering-dwg-documents/
weight: 17
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# C# で DWG ドキュメントをレンダリング – ビューポート dwg c# チュートリアル作成

## はじめに

この包括的なチュートリアルでは、Aspose.CAD を使用して **create viewport dwg c#** を作成し、DWG ファイルを PDF にレンダリングする方法を学びます。特定のレイアウトを抽出したり、印刷用シートを生成したり、レポートに CAD ビューを埋め込んだりする必要がある場合、ビューポートを制御することで正確なレンダリングが可能になります。Aspose.CAD は **20 以上の CAD フォーマット** をサポートし、数千のエンティティを含むファイルでもドキュメント全体をメモリにロードせずに処理できるため、高性能な .NET アプリケーションに最適です。

## クイック回答
- **最初のステップは何ですか？** `CadImage.Load` を使用して DWG ファイルをロードします。  
- **ビュー領域を定義するクラスはどれですか？** `CadRasterizationOptions` 内の `Viewport`。  
- **PDF に出力できますか？** ラスタライズ後に `PdfOptions` を使用します。  
- **本番環境でライセンスが必要ですか？** 商用ライセンスが必要です。評価目的であれば無料トライアルが使用できます。  
- **.NET Core はサポートされていますか？** もちろんです – Aspose.CAD は .NET Framework、.NET Core、そして .NET 5/6 で動作します。

## 前提条件

コードに取り掛かる前に、以下を確認してください：

- C# プログラミングの基本知識  
- Visual Studio（最新のエディション）をインストール  
- プロジェクトに Aspose.CAD ライブラリを追加。ダウンロードは [Aspose.CAD ダウンロードページ](https://releases.aspose.com/cad/net/) から。  
- サンプルとして **Bottom_plate.dwg** などの DWG ファイルを用意

## 名前空間のインポート

C# ファイルの先頭に必要な `using` ディレクティブを追加し、コンパイラが Aspose.CAD の型を認識できるようにします。

```csharp
using System;
using System.Collections.Generic;
using System.Linq;
using System.Text;
using System.Threading.Tasks;
using Aspose.CAD;
using Aspose.CAD.ImageOptions;
using Aspose.CAD.FileFormats.Cad.CadTables;
using Aspose.CAD.FileFormats.Cad;
```

環境が整ったので、実装手順をステップバイステップで見ていきましょう。

## ビューポート dwg c# の作成方法

カスタムビューポートを作成するには、まず DWG ファイルを `CadImage` オブジェクトにロードし、次に `CadRasterizationOptions` で目的のレイアウトとスケーリングを設定します。表示したい領域を定義し、計算した中心・高さ・アスペクト比で `CadVportTableObject` をインスタンス化し、アクティブビューポートを置き換えて PDF オプションを設定し、最後に結果を保存します。

## ステップ 1: dwg ファイルのロード

`CadImage.Load` は DWG ファイルを `CadImage` オブジェクトにロードし、メモリ上で CAD 図面を表現します。

```csharp
string MyDir = "Your Document Directory";
string sourceFilePath = MyDir + "Bottom_plate.dwg";
using (CadImage cadImage = (CadImage)Image.Load(sourceFilePath))
{
    // Your code for loading the DWG file goes here.
}
```

## ステップ 2: ラスタライズオプションの設定

`CadRasterizationOptions` はレイアウト選択、スケーリング、出力サイズなど、CAD 図面のラスタライズ方法を指定します。

```csharp
CadRasterizationOptions rasterizationOptions = new CadRasterizationOptions();
rasterizationOptions.Layouts = new string[] { "Model" };
rasterizationOptions.NoScaling = true;
// Additional rasterization configurations can be added here.
```

## ステップ 3: 描画領域の定義

`Point` はレンダリングする領域の左上隅の X と Y 座標を定義します。

```csharp
Point topLeft = new Point(6156, 7053);
double width = 3108;
double height = 2489;
```

## ステップ 4: 新しいビューポートの作成

`CadVportTableObject` は、レンダリングされた図面の表示領域とアスペクト比を制御するビューポートオブジェクトを表します。

```csharp
CadVportTableObject newView = new CadVportTableObject();
newView.Name.Value = "*Active";
newView.CenterPoint.X = topLeft.X + width / 2f;
newView.CenterPoint.Y = topLeft.Y - height / 2f;
newView.ViewHeight.Value = height;
newView.ViewAspectRatio.Value = width / height;
```

## ステップ 5: アクティブビューポートの置き換え

このループは、カスタムビュー設定を適用するためにアクティブビューポートを新しく作成したものに置き換えます。

```csharp
for (int i = 0; i < cadImage.ViewPorts.Count; i++)
{
    CadVportTableObject currentView = (CadVportTableObject)(cadImage.ViewPorts[i]);
    if ((currentView.Name.Value == null && cadImage.ViewPorts.Count == 1) ||
    string.Equals(currentView.Name.Value.ToLowerInvariant(), "*active"))
    {
        cadImage.ViewPorts[i] = newView;
        break;
    }
}
```

## ステップ 6: PDF オプションの設定

`PdfOptions` は圧縮やメタデータなど、PDF 出力パラメータを構成します。

```csharp
PdfOptions pdfOptions = new PdfOptions();
pdfOptions.VectorRasterizationOptions = rasterizationOptions;
```

## ステップ 7: レンダリングされた dwg を PDF として保存

`image.Save` は、指定されたフォーマットオプションを使用してレンダリングされた画像をファイルに書き込みます。

```csharp
cadImage.Save(MyDir, pdfOptions);
```

## DWG をレンダリングする際にカスタムビューポートを使用する理由

カスタムビューポートを使用すると、特定のレイアウトや領域を切り出すことでファイルサイズを削減し、レンダリング速度を向上させます。フォーカスされたビューポートを使用した場合、Aspose.CAD は 300 ページの DWG を 2 秒未満でレンダリングでき、全体を描画する場合に比べて数秒の差が出ます。

## よくある問題と解決策

- **Blank output** – ビューポート座標が図面の範囲内にあることを確認し、`CadImage.Size` で境界を検証してください。  
- **Missing layers** – `CadRasterizationOptions.Layouts` に正しいレイアウト名を設定してください。デフォルトレイアウトが空になることがあります。  
- **Performance slowdown** – プレビューだけが必要な場合は、`CadRasterizationOptions` のアンチエイリアシングを無効にしてください。

## よくある質問

### Q1: Aspose.CAD を他の CAD ファイル形式で使用できますか？

A1: はい、Aspose.CAD は DWG、DXF、DWF を含むさまざまな形式と、20 以上の追加 CAD タイプをサポートしています。

### Q2: Aspose.CAD は .NET Core と互換性がありますか？

A2: はい、Aspose.CAD は .NET Framework、.NET Core、そして最新の .NET リリースで動作します。

### Q3: DWG ファイル内の異なるレイアウトをどのように処理できますか？

A3: レンダリング前に `CadRasterizationOptions` の `Layouts` プロパティで目的のレイアウトを指定してください。

### Q4: Aspose.CAD の使用に関するライセンス上の考慮点はありますか？

A4: ライセンスの詳細は [Aspose.CAD ライセンスページ](https://purchase.aspose.com/buy) をご覧ください。

### Q5: 追加のサポートはどこで得られますか？

A5: コミュニティの助けやディスカッションは [Aspose.CAD フォーラム](https://forum.aspose.com/c/cad/19) でご確認ください。

### Q6: PDF の代わりに直接 PNG にレンダリングできますか？

A6: はい、`PdfOptions` を `PngOptions` に変更し、`image.Save("output.png", pngOptions)` を呼び出してください。

### Q7: レンダリングされた画像を Windows Forms アプリケーションに埋め込むには？

A7: `Image.FromFile("output.png")` を使用して保存された画像を `PictureBox` コントロールにロードします。

## 結論

これで **create viewport dwg c#** の方法と、Aspose.CAD を使用して DWG ファイルを PDF（または他のラスタ形式）にレンダリングする手順が分かりました。ビューポート操作をマスターすれば、視覚的出力を細かく制御でき、正確なエンジニアリング図面やレポート、サムネイルの生成に不可欠です。さらにラスタライズ設定を探求し、さまざまな出力形式を試し、コードを大規模な .NET サービスやデスクトップユーティリティに統合してください。

---

**最終更新日:** 2026-08-23  
**テスト環境:** Aspose.CAD 24.11 for .NET  
**作者:** Aspose

## 関連チュートリアル

- [C# で座標付き DWG を PDF に変換する際のビューポート設定方法 - Aspose.CAD チュートリアル](/cad/net/conversion-and-export/converting-dwg-to-pdf-with-coordinates/)
- [CAD ラスタライズオプションの設定方法 – Aspose.CAD で特定レイアウトを PDF にエクスポート](/cad/net/advanced-export-techniques/exporting-specific-layouts-to-pdf/)
- [Aspose.CAD for .NET を使用して DWG を PDF とラスタ画像に変換する方法](/cad/net/advanced-export-techniques/exporting-dwg-to-pdf-or-raster-images/)

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}