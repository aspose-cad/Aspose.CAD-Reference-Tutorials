---
title: Aspose.CAD for .NET での背景と描画色の設定
linktitle: 背景と描画色の設定
second_title: Aspose.CAD .NET - CAD および BIM ファイル形式
description: Aspose.CAD for .NET をマスターします。背景と描画色を簡単に設定できます。ステップバイステップのガイドに従ってください。
type: docs
weight: 15
url: /ja/net/cad-features-and-support/setting-background-and-drawing-colors/
---
## 導入

.NET 開発の動的な世界では、Aspose.CAD がコンピュータ支援設計 (CAD) ファイルを処理するための強力なツールとして登場します。 CAD 図面の操作スキルを向上させたい場合は、このチュートリアルが入り口となります。 Aspose.CAD for .NET を使用した背景の設定と描画色の複雑さを詳しく掘り下げ、明確さと有効性を保証するステップバイステップのガイドを提供します。

## 前提条件

この作業を開始する前に、次の前提条件が満たされていることを確認してください。

- .NET 開発の基本的な理解。
-  Aspose.CAD for .NET のインストール。まだダウンロードしていない場合は、ダウンロードしてください[ここ](https://releases.aspose.com/cad/net/).
- 実験用のサンプル CAD ファイル。ドキュメント ディレクトリで見つかります。

## 名前空間のインポート

.NET プロジェクトで、必要な名前空間をインポートすることから始めます。

```csharp
using System;
using System.Collections.Generic;
using System.Linq;
using System.Text;
using System.Threading.Tasks;
using Aspose.CAD;
```

## ステップ 1: CAD ファイルをロードする

まず、次のコード スニペットを使用して、作業する CAD ファイルをロードします。

```csharp
string MyDir = "Your Document Directory";
string sourceFilePath = MyDir + "conic_pyramid.dxf";

using (Image image = Image.Load(sourceFilePath))
{
    //さらに処理するためのコードはここにあります
}
```

## ステップ 2: ラスタライズ オプションを構成する

のインスタンスを作成します`CadRasterizationOptions`そして背景と描画色の設定のプロパティを設定します。

```csharp
CadRasterizationOptions rasterizationOptions = new CadRasterizationOptions();
rasterizationOptions.PageWidth = 1600;
rasterizationOptions.PageHeight = 1600;
rasterizationOptions.BackgroundColor = Color.Beige;
rasterizationOptions.DrawType = CadDrawTypeMode.UseDrawColor;
rasterizationOptions.DrawColor = Color.Blue;
```

## ステップ 3: PDF にエクスポートする

のインスタンスを作成します`PdfOptions`そして、`VectorRasterizationOptions`財産：

```csharp
PdfOptions pdfOptions = new PdfOptions();
pdfOptions.VectorRasterizationOptions = rasterizationOptions;

//CAD を PDF にエクスポート
image.Save(MyDir + "result_out.pdf", pdfOptions);
```

## ステップ 4: TIFF にエクスポートする

のインスタンスを作成します`TiffOptions`そして、`VectorRasterizationOptions`財産：

```csharp
TiffOptions tiffOptions = new TiffOptions(TiffExpectedFormat.Default);
tiffOptions.VectorRasterizationOptions = rasterizationOptions;

//CAD を TIFF にエクスポート
image.Save(MyDir + "result_out.tiff", tiffOptions);
```

## 結論

おめでとう！ Aspose.CAD for .NET で背景色と描画色を設定する方法を学習しました。このチュートリアルでは、CAD ファイルを簡単に操作するスキルを習得します。

## よくある質問

### Q1: Aspose.CAD for .NET はどの種類の CAD ファイルでも使用できますか?

A1: はい、Aspose.CAD は、DWG、DXF、DGN などのさまざまな CAD 形式をサポートしています。

### Q2: Aspose.CAD for .NET の無料トライアルは利用できますか?

 A2: はい、無料トライアルを試すことができます[ここ](https://releases.aspose.com/).

### Q3: Aspose.CAD for .NET の詳細なドキュメントはどこで入手できますか?

 A3: ドキュメントを参照してください。[ここ](https://reference.aspose.com/cad/net/).

### Q4: Aspose.CAD の一時ライセンスを取得するにはどうすればよいですか?

 A4: 仮免許は取得可能です[ここ](https://purchase.aspose.com/temporary-license/).

### Q5: サポートが必要ですか、それともコミュニティとつながりたいですか?

 A5: サポート フォーラムにアクセスしてください。[ここ](https://forum.aspose.com/c/cad/19).
