---
title: Aspose.CAD for .NET で DGN をラスター イメージにエクスポートする
linktitle: DGN をラスター イメージにエクスポート
second_title: Aspose.CAD .NET - CAD および BIM ファイル形式
description: Aspose.CAD for .NET を使用して、DGN をラスター イメージに簡単に変換します。ステップバイステップのガイドを参照して、CAD ファイル操作で .NET のパワーを解放してください。
weight: 13
url: /ja/net/cad-export-formats/export-dgn-to-raster-image/
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Aspose.CAD for .NET で DGN をラスター イメージにエクスポートする

## 導入

.NET 開発の動的な領域では、Aspose.CAD がコンピュータ支援設計 (CAD) ファイルを処理するための強力なツールとして登場します。このチュートリアルでは、Aspose.CAD for .NET を使用して DGN ファイルをラスター イメージにエクスポートするプロセスについて詳しく説明します。 DGN ファイルを視覚的に魅力的なラスター イメージにシームレスに変換したい場合は、ここが最適な場所です。

## 前提条件

この作業を開始する前に、次の前提条件が満たされていることを確認してください。

-  Aspose.CAD for .NET: Aspose.CAD ライブラリが .NET プロジェクトにインストールされていることを確認します。ライブラリと関連ドキュメントは、[Webサイト](https://reference.aspose.com/cad/net/).

- サンプル DGN ファイル: 変換できる DGN ファイルを用意します。この例では、「Nikon_D90_Camera.dgn」を使用します。

それでは、ステップバイステップのガイドを見てみましょう。

## 名前空間のインポート

.NET プロジェクトで、Aspose.CAD に必要な名前空間をインポートすることから始めます。この手順により、DGN からラスター イメージへの変換に必要なクラスとメソッドにアクセスできるようになります。

```csharp
using System;
using System.Collections.Generic;
using System.Linq;
using System.Text;
using System.Threading.Tasks;
using Aspose.CAD;
```

## ステップ 1: DGN ファイルをロードする

まず、DGN ファイルを`CadImage`物体。これにより、その後の操作の基盤が提供されます。

```csharp
string MyDir = "Your Document Directory";
string sourceFilePath = MyDir + "Nikon_D90_Camera.dgn";

using (CadImage cadImage = (CadImage)Image.Load(sourceFilePath))
{
    //さらに処理するためのコードはここにあります
}
```

## ステップ 2: ラスタライズ オプションを定義する

を作成します`CadRasterizationOptions`オブジェクトを作成し、さまざまなプロパティを設定して、要件に応じてラスタライズ プロセスをカスタマイズします。

```csharp
CadRasterizationOptions rasterizationOptions = new CadRasterizationOptions();
rasterizationOptions.PageWidth = 600;
rasterizationOptions.PageHeight = 300;
rasterizationOptions.NoScaling = true;
rasterizationOptions.AutomaticLayoutsScaling = false;
```

## ステップ 3: JpegOptions オブジェクトを作成する

DGN ファイルを JPEG に変換することが目的なので、`JpegOptions`オブジェクトを作成し、以前に定義したものを割り当てます`CadRasterizationOptions`それに。

```csharp
ImageOptionsBase options = new JpegOptions();
options.VectorRasterizationOptions = rasterizationOptions;
```

## ステップ 4: ラスター画像を保存する

を活用してください。`Save`の方法`CadImage`クラスを使用して、DGN ファイルを目的の形式 (この場合は JPEG) のラスター イメージにエクスポートします。

```csharp
cadImage.Save(MyDir + "ExportDGNToRasterImage_out.jpg", options);
```

## 結論

おめでとう！ Aspose.CAD for .NET を使用して DGN ファイルをラスター イメージにエクスポートする手順を完了しました。このチュートリアルでは、この機能を .NET プロジェクトに簡単に統合するための重要な知識を習得しました。

## よくある質問

### Q1: DGN ファイルを JPEG 以外の形式にエクスポートできますか?

A1: はい、Aspose.CAD for .NET はさまざまな出力形式をサポートしています。ステップ 3 でオプションを適宜変更できます。

### Q2 変換プロセス中に例外を処理するにはどうすればよいですか?

A2: 潜在的な問題に対処するために、提供されたコードに示されているように、適切な例外処理があることを確認してください。

### Q3: Aspose.CAD for .NET の試用版はありますか?

 A3: はい、無料トライアルで製品を試すことができます。訪問[ここ](https://releases.aspose.com/)詳細については。

### Q4: Aspose.CAD for .NET に関連する問題について支援を求めたり、議論したりするにはどこに行けばよいですか?

 A4: に向かってください。[Aspose.CAD フォーラム](https://forum.aspose.com/c/cad/19)コミュニティのサポートとディスカッションのために。

### Q5: Aspose.CAD for .NET の一時ライセンスを取得するにはどうすればよいですか?

 A5: 訪問[このリンク](https://purchase.aspose.com/temporary-license/)開発ニーズに応じて一時ライセンスを取得します。
{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}
