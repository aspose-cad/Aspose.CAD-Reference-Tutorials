---
title: Aspose.CAD for .NET で CAD レイアウトをラスター イメージ形式にエクスポートする
linktitle: CAD レイアウトをラスター イメージ形式にエクスポート
second_title: Aspose.CAD .NET - CAD および BIM ファイル形式
description: Aspose.CAD for .NET を使用して CAD レイアウトをラスター イメージにエクスポートする方法を学びます。シームレスな変換については、ステップバイステップのガイドに従ってください。
type: docs
weight: 10
url: /ja/net/cad-export-formats/export-cad-layouts-to-raster-image-formats/
---
## 導入

Aspose.CAD for .NET を使用して、CAD レイアウトをラスター イメージ形式に効率的に変換したいと考えていますか?このステップバイステップのガイドでは、プロセスを順を追って説明し、タスクをシームレスにするための詳細な手順とコード スニペットを提供します。経験豊富な開発者でも、Aspose.CAD の初心者でも、このチュートリアルはあらゆるレベルの専門知識に対応します。

## 前提条件

チュートリアルに入る前に、次のものが揃っていることを確認してください。

- Aspose.CAD for .NET ライブラリ: Aspose.CAD ライブラリがインストールされていることを確認します。そうでない場合は、からダウンロードできます。[Aspose.CAD Web サイト](https://releases.aspose.com/cad/net/).

- CAD 図面ファイル: ラスター イメージ形式に変換する CAD 図面ファイル (conic_pyramid.dxf など) を準備します。

## 名前空間のインポート

.NET プロジェクトで、Aspose.CAD 機能を利用するために必要な名前空間をインポートします。コードの先頭に次の名前空間を含めます。

```csharp
using System;
using System.Collections.Generic;
using System.Linq;
using System.Text;
using System.Threading.Tasks;
using Aspose.CAD;
```

## ステップ 1: CAD 図面をロードする

```csharp
string MyDir = "Your Document Directory";
string sourceFilePath = MyDir + "conic_pyramid.dxf";

// Image のインスタンスに CAD 図面をロードします
using (var image = Image.Load(sourceFilePath))
{
    // CAD 図面をロードするためのコードはここにあります
}
```

## ステップ 2: CadRasterizationOptions を作成する

```csharp
// CadRasterizationOptions のインスタンスを作成する
var rasterizationOptions = new CadRasterizationOptions();
rasterizationOptions.PageWidth = 500;
rasterizationOptions.PageHeight = 500;
```

## ステップ 3: レイヤーを指定する

```csharp
//CadRasterizationOptions のレイヤー リストにレイヤー名を追加します。
rasterizationOptions.Layers = new string[] { "LayerA" };
```

## ステップ 4: JpegOptions を作成する

```csharp
//JpegOptions (またはラスター形式の任意の ImageOptions) のインスタンスを作成します。
var options = new JpegOptions();
options.VectorRasterizationOptions = rasterizationOptions;
```

## ステップ 5: Jpeg 形式にエクスポートする

```csharp
//各レイヤーをJpeg形式でエクスポート
MyDir = MyDir + "CADLayersToRasterImageFormats_out.jpg";
image.Save(MyDir, options);
```

## 追加ステップ: すべてのレイヤーを変換する

すべてのレイヤーを変換する場合は、次の方法を使用します。

```csharp
ConvertAllLayersToRasterImageFormats();
```

このメソッドは、CAD 図面内のすべてのレイヤーを反復処理し、各レイヤーを個別の Jpeg ファイルにエクスポートします。

## 結論

おめでとう！ Aspose.CAD for .NET を使用して CAD レイアウトをラスター イメージ形式にエクスポートする方法を学習しました。このチュートリアルは、CAD 変換のための効率的で信頼性の高いソリューションを求める開発者向けの包括的なガイドを提供します。

## よくある質問

### Q1: 他の画像形式をエクスポートに使用できますか?

 A1: はい、可能です。単純に交換するだけ`JpegOptions`必要な形式のオプションを使用して、`PngOptions`または`BmpOptions`.

### Q2: 体験版はありますか?

A2: はい、試用版をダウンロードすると、Aspose.CAD の機能を試すことができます。[ここ](https://releases.aspose.com/).

### Q3: Aspose.CAD のサポートを受けるにはどうすればよいですか?

 A3: Aspose.CAD にアクセスしてください。[フォーラム](https://forum.aspose.com/c/cad/19)コミュニティ サポートを利用するか、専用サポートのライセンスの購入を検討してください。

### Q4: 一時ライセンスは利用できますか?

 A4: はい、一時ライセンスを取得できます。[ここ](https://purchase.aspose.com/temporary-license/).

### Q5: ドキュメントはどこで入手できますか?

 A5: 詳細ドキュメントを参照してください。[ここ](https://reference.aspose.com/cad/net/).