---
title: DWG を PDF またはラスター イメージにエクスポートする - Aspose.CAD ガイド
linktitle: DWG を PDF またはラスター イメージにエクスポートする
second_title: Aspose.CAD .NET - CAD および BIM ファイル形式
description: Aspose.CAD for .NET を使用して DWG を PDF またはラスター イメージにエクスポートするための包括的なガイドをご覧ください。手順と前提条件を学び、この強力なライブラリを実際に使ってみましょう。
type: docs
weight: 11
url: /ja/net/advanced-export-techniques/exporting-dwg-to-pdf-or-raster-images/
---
## 導入

.NET アプリケーションで DWG ファイルを PDF またはラスター イメージにシームレスに変換したいと考えていますか?これ以上探さない！このステップバイステップ ガイドでは、強力な Aspose.CAD for .NET ライブラリを使用するプロセスを順を追って説明します。経験豊富な開発者であっても、初心者であっても、このチュートリアルはあらゆるスキル レベルに対応しています。

## 前提条件

チュートリアルに入る前に、次のものが整っていることを確認してください。

- .NET プログラミングの基本的な理解。
-  Aspose.CAD for .NET ライブラリがインストールされています。そうでない場合は、ダウンロードしてください[ここ](https://releases.aspose.com/cad/net/).
- .NET 開発用にセットアップされたお気に入りの統合開発環境 (IDE)。

## 名前空間のインポート

必要な名前空間を .NET プロジェクトにインポートすることから始めましょう。これにより、コード内で Aspose.CAD 機能にアクセスできるようになります。

```csharp
using System;
using System.Collections.Generic;
using System.Linq;
using System.Text;
using System.Threading.Tasks;
using Aspose.CAD;
using Aspose.CAD.FileFormats.Cad;
using Aspose.CAD.ImageOptions;
```

## ステップ 1: DWG ファイルをロードする

まず、変換する DWG ファイルをロードします。 「Your Document Directory」を DWG ファイルへのパスに置き換えます。

```csharp
string MyDir = "Your Document Directory";
string sourceFilePath = MyDir + "Bottom_plate.dwg";

using (CadImage cadImage = (CadImage)Image.Load(sourceFilePath))
{
    // DWG をロードするためのコードはここにあります
}
```

## ステップ 2: PDF エクスポートを設定する

次に、PDF エクスポート設定を構成しましょう。この例では、レイアウトを設定し、単位変換を処理する方法を示します。

```csharp
CadRasterizationOptions rasterizationOptions = new CadRasterizationOptions();
rasterizationOptions.Layouts = new string[] { "Model" };

//単位系を確認して定義する
bool currentUnitIsMetric = false;
double currentUnitCoefficient = 1.0;
DefineUnitSystem(cadImage.UnitType, out currentUnitIsMetric, out currentUnitCoefficient);

//PDF エクスポートを設定するコードはここにあります
```

## ステップ 3: PDF にエクスポートする

設定した内容を使用して PDF へのエクスポートを実行します。

```csharp
PdfOptions pdfOptions = new PdfOptions
{
    VectorRasterizationOptions = rasterizationOptions
};

cadImage.Save(outPath, pdfOptions);
```

## ステップ 4: ラスター イメージにエクスポートする

PNG などのラスター イメージにエクスポートする機能を拡張します。

```csharp
// A4 サイズ、300 DPI - 2480 x 3508
rasterizationOptions.PageHeight = 3508;
rasterizationOptions.PageWidth = 2480;

PngOptions pngOptions = new PngOptions
{
    VectorRasterizationOptions = rasterizationOptions
};

cadImage.Save(outPath.Replace("pdf", "png"), pngOptions);
```

## 結論

おめでとう！ Aspose.CAD for .NET を使用して DWG ファイルを PDF とラスター イメージの両方にエクスポートする方法を学習しました。この強力なライブラリはプロセスを合理化し、効率的で開発者にとって使いやすいものにします。

## よくある質問

### Q1: Aspose.CAD for .NET を商用プロジェクトで使用できますか?

 A1: はい、可能です。訪問[購入.aspose.com/購入](https://purchase.aspose.com/buy)ライセンスの詳細については、

### Q2: 無料トライアルはありますか?

A2：確かに！無料トライアルを手に入れましょう[ここ](https://releases.aspose.com/).

### Q3: Aspose.CAD for .NET のサポートを受けるにはどうすればよいですか?

A3: に向かってください。[Aspose.CAD フォーラム](https://forum.aspose.com/c/cad/19)コミュニティサポートのために。

### Q4: テスト目的で一時ライセンスを取得できますか?

 A4: はい、仮免許を取得できます。[ここ](https://purchase.aspose.com/temporary-license/).

### Q5: 詳細なドキュメントはどこで入手できますか?

 A5: ドキュメントは次の場所から入手できます。[Aspose.CAD](https://reference.aspose.com/cad/net/).