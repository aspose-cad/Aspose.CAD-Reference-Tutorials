---
title: Aspose.CAD for .NET でのキャンバス サイズとモードの設定
linktitle: キャンバスのサイズとモードの設定
second_title: Aspose.CAD .NET - CAD および BIM ファイル形式
description: Aspose.CAD for .NET でのキャンバス サイズとモードの設定に関するステップバイステップ ガイドをご覧ください。この包括的なチュートリアルを使用して、CAD レンダリングを簡単に最適化します。
type: docs
weight: 16
url: /ja/net/cad-features-and-support/setting-canvas-size-and-mode/
---
## 導入

Aspose.CAD for .NET の可能性を最大限に引き出し、CAD レンダリング エクスペリエンスに革命を起こす準備はできていますか?このステップバイステップのチュートリアルでは、強力な Aspose.CAD ライブラリを使用してキャンバスのサイズとモードを設定する複雑な手順を詳しく説明します。経験豊富な開発者でも、初心者でも、このガイドではプロセスを順を追って説明し、Aspose.CAD の機能を効果的に活用できるようにします。

## 前提条件

チュートリアルに入る前に、次の前提条件が満たされていることを確認してください。

-  Aspose.CAD ライブラリ: Aspose.CAD ライブラリを次の場所からダウンロードしてインストールします。[Aspose.CAD Web サイト](https://releases.aspose.com/cad/net/).

- 開発環境: マシン上に .NET 開発環境がセットアップされていることを確認します。

- サンプル CAD ファイル: このチュートリアルでは、サンプル DXF ファイルを使用します。で見つけることができます。[Aspose.CAD ドキュメント](https://reference.aspose.com/cad/net/).

## 名前空間のインポート

まず、.NET アプリケーションの先頭で必要な名前空間をインポートします。

```csharp
using System;
using System.Collections.Generic;
using System.Linq;
using System.Text;
using System.Threading.Tasks;
using Aspose.CAD;
```

## ステップ 1: CAD ファイルをロードする

次のコードを使用して CAD ファイルをロードすることから始めます。

```csharp
string MyDir = "Your Document Directory";
string sourceFilePath = MyDir + "conic_pyramid.dxf";

using (Image image = Image.Load(sourceFilePath))
{
    //さらなるステップのコードはここにあります
}
```

## ステップ 2: CadRasterizationOptions を作成する

のインスタンスを作成します`CadRasterizationOptions`そしてそのプロパティを設定します。

```csharp
CadRasterizationOptions rasterizationOptions = new CadRasterizationOptions();
rasterizationOptions.PageWidth = 1600;
rasterizationOptions.PageHeight = 1600;
rasterizationOptions.AutomaticLayoutsScaling = true;
rasterizationOptions.NoScaling = false;
```

## ステップ 3: PdfOptions を作成する

のインスタンスを作成します`PdfOptions`そしてそれを設定します`VectorRasterizationOptions`財産：

```csharp
PdfOptions pdfOptions = new PdfOptions();
pdfOptions.VectorRasterizationOptions = rasterizationOptions;
```

## ステップ 4: PDF にエクスポートする

構成されたオプションを使用して、CAD ファイルを PDF にエクスポートします。

```csharp
image.Save(MyDir + "result_out.pdf", pdfOptions);
```

## ステップ 5: TiffOptions を作成する

のインスタンスを作成します`TiffOptions`そしてそれを設定します`VectorRasterizationOptions`財産：

```csharp
TiffOptions tiffOptions = new TiffOptions(TiffExpectedFormat.Default);
tiffOptions.VectorRasterizationOptions = rasterizationOptions;
```

## ステップ 6: TIFF にエクスポートする

構成されたオプションを使用して、CAD ファイルを TIFF にエクスポートします。

```csharp
image.Save(MyDir + "result_out.tiff", tiffOptions);
```

## 結論

おめでとう！ Aspose.CAD for .NET でキャンバスのサイズとモードが正常に設定されました。この強力な機能は、CAD レンダリングの可能性の世界を開きます。さまざまなオプションを試して、.NET アプリケーションにおける Aspose.CAD の可能性を最大限に引き出してください。

## よくある質問

### Q1: Aspose.CAD を他の .NET ライブラリと一緒に使用できますか?

A1: はい、Aspose.CAD は他の .NET ライブラリとシームレスに統合し、CAD 操作の拡張機能を提供します。

### Q2: Aspose.CAD の無料トライアルは利用できますか?

 A2: はい、無料トライアルで Aspose.CAD の機能を試すことができます。訪問[ここ](https://releases.aspose.com/)始めるために。

### Q3: Aspose.CAD のサポートを受けるにはどうすればよいですか?

A3: サポートとディスカッションについては、次のサイトにアクセスしてください。[Aspose.CAD フォーラム](https://forum.aspose.com/c/cad/19).

### Q4: Aspose.CAD の包括的なドキュメントはどこで見つけられますか?

 A4: を参照してください。[Aspose.CAD ドキュメント](https://reference.aspose.com/cad/net/)詳細な情報と例については、

### Q5: Aspose.CAD for .NET を購入するにはどうすればよいですか?

 A5: Aspose.CAD を購入するには、次のサイトにアクセスしてください。[購入ページ](https://purchase.aspose.com/buy).