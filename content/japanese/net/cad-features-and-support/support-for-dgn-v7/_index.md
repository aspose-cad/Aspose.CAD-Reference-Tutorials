---
title: Aspose.CAD for .NET での DGN V7 のサポート
linktitle: DGN V7 のサポート
second_title: Aspose.CAD .NET - CAD および BIM ファイル形式
description: Aspose.CAD for .NET の DGN V7 のシームレスなサポートを調べてください。ステップバイステップのガイダンスに従って、DGN ファイルをラスター イメージに簡単に変換できます。
type: docs
weight: 19
url: /ja/net/cad-features-and-support/support-for-dgn-v7/
---
## 導入

.NET 開発の分野では、Aspose.CAD はコンピュータ支援設計 (CAD) ファイルを処理するための強力なライブラリとして際立っています。このチュートリアルでは、Aspose.CAD for .NET の特定の機能、つまり DGN V7 ファイルのサポートについて詳しく説明します。 DGN (Design の略) は、CAD ドメインで広く使用されているファイル形式です。 Aspose.CAD は、DGN V7 ファイルを操作するプロセスを簡素化し、開発者にシームレスなエクスペリエンスを提供します。

## 前提条件

実装に入る前に、次の前提条件が満たされていることを確認してください。

-  Aspose.CAD for .NET: Aspose.CAD ライブラリがインストールされていることを確認してください。からダウンロードできます。[Webサイト](https://releases.aspose.com/cad/net/).

- 開発環境: Visual Studio またはその他の優先 IDE を含む、動作する .NET 開発環境をセットアップします。

前提条件が整理されたので、Aspose.CAD for .NET での DGN V7 のサポートを活用する方法を見てみましょう。

## 名前空間のインポート

まず、Aspose.CAD の機能にアクセスするために必要な名前空間をインポートします。

```csharp
using System;
using System.Collections.Generic;
using System.Linq;
using System.Text;
using System.Threading.Tasks;
using Aspose.CAD;
```

## ステップ 1: DGN ファイルをロードする

まず、既存の DGN ファイルを`CadImage`。交換する`"Your Document Directory"`そして`"Nikon_D90_Camera.dgn"`適切なディレクトリ パスとファイル名を使用します。

```csharp
string MyDir = "Your Document Directory";
string sourceFilePath = MyDir + "Nikon_D90_Camera.dgn";

using (CadImage cadImage = (CadImage)Image.Load(sourceFilePath))
{
    //さらなるステップのコードはここにあります...
}
```

## ステップ 2: ラスタライズ オプションを構成する

を作成します`CadRasterizationOptions`オブジェクトを使用して、ラスタライズに関連するさまざまなプロパティを定義および設定します。

```csharp
CadRasterizationOptions rasterizationOptions = new CadRasterizationOptions
{
    PageWidth = 600,
    PageHeight = 300,
    NoScaling = true,
    AutomaticLayoutsScaling = false
};
```

## ステップ 3: ベクトル ラスタライズ オプションを設定する

を作成します`JpegOptions`DGN ファイルを JPEG に変換するつもりなので、オブジェクトを作成します。以前に作成したものを割り当てます`CadRasterizationOptions`それに反対します。

```csharp
ImageOptionsBase options = new JpegOptions
{
    VectorRasterizationOptions = rasterizationOptions
};
```

## ステップ 4: ラスタライズされた画像を保存する

電話してください`Save`の方法`CadImage`クラス オブジェクトを使用して、DGN ファイルをラスター イメージ (この場合は JPEG) にエクスポートします。

```csharp
cadImage.Save(MyDir + "ExportDGNToRasterImage_out.jpeg", options);
```

これらの手順が完了すると、DGN ファイルがラスター イメージに正常にエクスポートされます。

## 結論

このチュートリアルでは、Aspose.CAD for .NET での DGN V7 のシームレスなサポートについて調べました。段階的なガイドに従うことで、開発者は DGN ファイルをラスター イメージに簡単に変換し、.NET アプリケーションの機能を拡張できます。

## よくある質問

### Q1: Aspose.CAD は最新の DGN V7 仕様と互換性がありますか?

A1: はい、Aspose.CAD は DGN V7 ファイルをシームレスに処理できるように設計されており、最新の仕様との互換性が保証されています。

### Q2: DGN ファイル変換のラスタライズ オプションをカスタマイズできますか?

 A2: もちろんです。このチュートリアルでは、作成および構成する方法を示します。`CadRasterizationOptions`変換プロセスを調整します。

### Q3: JPEG 以外にサポートされている出力形式はありますか?

A3: はい、Aspose.CAD はさまざまな出力形式をサポートしています。包括的なリストについてはドキュメントを参照してください。

### Q4: Aspose.CAD 関連のクエリのサポートを受けるにはどうすればよいですか?

 A4: にアクセスしてください。[Aspose.CAD フォーラム](https://forum.aspose.com/c/cad/19)コミュニティのサポートとディスカッションのために。

### Q5: Aspose.CAD for .NET の無料トライアルはありますか?

 A5: はい、無料トライアルにアクセスできます。[ここ](https://releases.aspose.com/).