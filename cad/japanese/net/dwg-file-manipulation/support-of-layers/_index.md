---
date: 2026-04-09
description: C# と Aspose.CAD for .NET を使用して、DWG のレイヤーをエクスポートし、DWG 画像を変換し、DWG JPEG
  を保存する方法を学びましょう。効率的な CAD ファイル操作のためのステップバイステップガイドです。
keywords:
- export dwg layers
- convert dwg image
- dwg layer visibility
- save dwg jpeg
linktitle: C#でDWGファイルのレイヤーを操作する
second_title: Aspose.CAD .NET - CAD and BIM File Format
title: C#でDWGレイヤーをエクスポート – Aspose.CADチュートリアル
url: /ja/net/dwg-file-manipulation/support-of-layers/
weight: 11
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# C# で DWG レイヤーをエクスポート – Aspose.CAD チュートリアル

## はじめに

この包括的なガイドでは、C# と Aspose.CAD ライブラリを使用して **DWG レイヤーのエクスポート方法** を学びます。**DWG 画像を変換** したり、**DWG レイヤーの表示** を制御したり、単に **DWG JPEG を保存** したりする必要がある場合でも、以下の手順で効率的に実行する方法を正確に示します。チュートリアルの最後までに、特定のレイヤーを抽出し高品質 JPEG としてレンダリングする、すぐに実行できるコードスニペットが手に入ります。

## クイック回答

- **「export dwg layers」とは何ですか？** これは、DWG ファイルの選択されたレイヤーを JPEG や PNG などの画像形式にラスタライズすることを意味します。  
- **このタスクに最適なライブラリはどれですか？** Aspose.CAD for .NET は、AutoCAD を必要とせずにフル機能のサポートを提供します。  
- **複数のレイヤーを同時にエクスポートできますか？** はい。レイヤー名の配列をラスタライズオプションに渡すだけです。  
- **本番環境で使用するにはライセンスが必要ですか？** 商用ライセンスが必要です。評価用の無料トライアルも利用可能です。  
- **サポートされている出力形式は何ですか？** JPEG、PNG、BMP、TIFF など、ImageOptions クラスを通じて多数の形式がサポートされています。

## export dwg layers とは何ですか？

DWG レイヤーをエクスポートするとは、DWG 図面内の 1 つまたは複数のレイヤーに属するベクトルデータを取得し、ビットマップ画像にラスタライズすることを意味します。これは、CAD ファイル全体を公開せずに、図面の特定部分のビューを共有したい場合に便利です。

## DWG レイヤーの表示を制御する理由は？

- プレゼンテーションやドキュメント用にクリーンなビジュアル資産を作成する。  
- 必要なジオメトリだけをエクスポートしてファイルサイズを削減する。  
- 機密レイヤーを非表示にすることで、所有する設計詳細を保護する。  

## 前提条件

Before we dive in, verify that you have:

- C# プログラミング言語の基本的な知識。  
- マシンに Visual Studio がインストールされていること。  
- Aspose.CAD for .NET ライブラリ、[Aspose.CAD website](https://releases.aspose.com/cad/net/) からダウンロードできます。

## 名前空間のインポート

まず、ラスタライズおよび画像エクスポート機能にアクセスできる名前空間をインポートします。

```csharp
using Aspose.CAD.ImageOptions;
using System;
using System.Collections.Generic;
using System.IO;
using System.Linq;
using System.Text;
```

## ステップ 1: DWG ファイルの読み込み

ソースの DWG（または DWF）ファイルを `Image` オブジェクトに読み込みます。このオブジェクトはメモリ内で図面全体を表します。

```csharp
string MyDir = "Your Document Directory";
string sourceFilePath = MyDir + "for_layers_test.dwf";

using (Aspose.CAD.Image image = Aspose.CAD.Image.Load(sourceFilePath))
{
    // Your code for subsequent steps goes here
}
```

*この点が重要な理由:* ファイルを一度だけ読み込むことで、同じ `image` インスタンスを複数のレイヤー固有のエクスポートに再利用でき、パフォーマンスが向上します。

## ステップ 2: ラスタライズオプションの設定

`CadRasterizationOptions` インスタンスを作成し、Aspose.CAD に図面の描画方法を指示します。ここでは、エクスポートされた JPEG が鮮明になるように高解像度（1600 × 1600）を設定しています。

```csharp
Aspose.CAD.ImageOptions.CadRasterizationOptions rasterizationOptions = new Aspose.CAD.ImageOptions.CadRasterizationOptions();
rasterizationOptions.PageWidth = 1600;
rasterizationOptions.PageHeight = 1600;
```

必要に応じて、背景色、線幅のスケーリング、アンチエイリアス設定なども調整できます。

## ステップ 3: レイヤーの指定（DWG レイヤーの表示）

**DWG レイヤーをエクスポート** 用にエクスポートしたいレイヤーを追加します。この例では「LayerA」だけをエクスポートしています。複数のレイヤーをエクスポートする場合は、配列に列挙するだけです。

```csharp
rasterizationOptions.Layers = new string[] { "LayerA" };
```

*プロのコツ:* 図面に表示されている正確なレイヤー名を使用してください。レイヤー名は大文字小文字を区別します。

## ステップ 4: 画像エクスポートオプションの設定

作成したい画像形式を選択します。ここでは `JpegOptions` を使用します。JPEG は品質とファイルサイズのバランスが良く、Web プレビュー用に **DWG JPEG を保存** ファイルが必要な場合に最適です。

```csharp
JpegOptions jpegOptions = new JpegOptions();
jpegOptions.VectorRasterizationOptions = rasterizationOptions;
```

**DWG 画像を変換** を PNG や TIFF に変換する必要がある場合は、`JpegOptions` を対応するオプションクラスに置き換えてください。

## ステップ 5: エクスポート画像の保存

出力ファイルパスを定義し、`Save` を呼び出します。ラスタライズエンジンは指定したレイヤーリストを尊重するため、最終的な JPEG には「LayerA」のみが表示されます。

```csharp
MyDir = MyDir + "for_layers_test.jpg";
image.Save(MyDir, jpegOptions);
```

この行が実行された後、`for_layers_test.jpg` がドキュメントディレクトリに作成され、選択したレイヤーのみが含まれます。

## 一般的な問題と解決策

| Issue | Resolution |
|-------|------------|
| **レイヤー名が見つかりません** | 元の DWG でのレイヤー名の正確な綴りと大文字小文字を確認してください。CAD ビューアでレイヤー名を一覧表示できます。 |
| **空白の出力画像** | ラスタライズオプションで背景が透明でないこと、選択したレイヤーに実際にジオメトリが含まれていることを確認してください。 |
| **低解像度の出力** | `PageWidth` と `PageHeight` を増やすか、`CadRasterizationOptions` の `Resolution` を設定してください。 |
| **サポートされていない DWG バージョン** | 最新の Aspose.CAD バージョンに更新してください。これにより、最新の AutoCAD リリースがサポートされます。 |

## よくある質問

### Q1: 複数のレイヤーを同時に処理できますか？

A1: はい、可能です。レイヤー名を `rasterizationOptions.Layers` 配列に追加するだけです。

### Q2: Aspose.CAD のトライアル版は利用可能ですか？

A2: はい、[here](https://releases.aspose.com/) から無料トライアル版を入手できます。

### Q3: ドキュメントはどこで見つけられますか？

A3: ドキュメントは[here](https://reference.aspose.com/cad/net/) で利用可能です。

### Q4: Aspose.CAD のサポートはどこで受けられますか？

A4: [Aspose.CAD forum](https://forum.aspose.com/c/cad/19) でサポートを受けられます。

### Q5: Aspose.CAD のライセンスオプションは何ですか？

A5: ライセンスオプションや購入詳細は[here](https://purchase.aspose.com/buy) で確認できます。

**追加の Q&A**

**Q: PNG にエクスポートできますか？**  
A: もちろんです。`JpegOptions` を `PngOptions` に置き換え、ファイル拡張子もそれに合わせて変更してください。

**Q: ライブラリは線のスタイルや色を保持しますか？**  
A: はい。すべてのベクトル属性はラスタライズ時に忠実に描画されます。

---

**最終更新日:** 2026-04-09  
**テスト環境:** Aspose.CAD for .NET (latest release)  
**作者:** Aspose  

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}