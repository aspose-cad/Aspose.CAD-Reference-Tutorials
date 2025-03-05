---
title: Aspose.CAD for .NET での CAD 図面サイズの調整
linktitle: CAD 図面のサイズを調整する
second_title: Aspose.CAD .NET - CAD および BIM ファイル形式
description: Aspose.CAD を使用して .NET で CAD 図面のサイズを簡単に調整する方法を学びます。シームレスにサイズを変更するには、ステップバイステップのガイドに従ってください。
type: docs
weight: 10
url: /ja/net/cad-drawing-manipulation/adjust-cad-drawing-size/
---
## 導入

.NET アプリケーションで CAD 図面のサイズをシームレスに調整したいと考えていますか? Aspose.CAD for .NET は堅牢なソリューションを提供し、CAD 図面のサイズ変更を簡単に処理できるようにします。このチュートリアルでは、Aspose.CAD を使用して CAD 図面のサイズを変更する複雑さを確実に理解できるように、プロセスを各ステップに分けて説明します。

## 前提条件

チュートリアルに入る前に、次の前提条件が満たされていることを確認してください。

- Aspose.CAD for .NET ライブラリ: からライブラリをダウンロードしてインストールします。[Aspose.CAD for .NET ダウンロード ページ](https://releases.aspose.com/cad/net/).
- サンプル CAD 図面: ドキュメント ディレクトリにサンプル CAD 図面ファイル (例: 「sample.dwg」) があることを確認します。

## 名前空間のインポート

まず、必要な名前空間を .NET アプリケーションにインポートします。この手順は、Aspose.CAD for .NET が提供する機能にアクセスするために重要です。

```csharp
using System;
using System.Collections.Generic;
using System.Linq;
using System.Text;
using System.Threading.Tasks;
using Aspose.CAD;
```

## ステップ 1: CAD 図面をロードする

まず、CAD 図面を Aspose.CAD.Image クラスのインスタンスにロードします。サンプル図面の正しいファイル パスがあることを確認してください。

```csharp
string MyDir = "Your Document Directory";
string sourceFilePath = MyDir + "sample.dwg";

// Image のインスタンスに CAD 図面をロードします
using (var image = Aspose.CAD.Image.Load(sourceFilePath))
{
    //コードはここにあります...
}
```

## ステップ 2: BmpOptions を作成する

BmpOptions クラスのインスタンスを作成します。このクラスは、CAD 図面を BMP ファイルとして保存するときにオプションを指定します。

```csharp
Aspose.CAD.ImageOptions.BmpOptions bmpOptions = new Aspose.CAD.ImageOptions.BmpOptions();
```

## ステップ 3: CadRasterizationOptions を設定する

CadRasterizationOptions クラスをインスタンス化し、ベクトル ラスター化用にそのプロパティを構成します。

```csharp
Aspose.CAD.ImageOptions.CadRasterizationOptions cadRasterizationOptions = new Aspose.CAD.ImageOptions.CadRasterizationOptions();
bmpOptions.VectorRasterizationOptions = cadRasterizationOptions;
```

## ステップ 4: UnitType プロパティを設定する

CadRasterizationOptions の UnitType プロパティを設定して、サイズ変更の単位タイプを指定します。この例では、センチメートルに設定されています。

```csharp
cadRasterizationOptions.UnitType = Aspose.CAD.ImageOptions.UnitType.Centimeter;
```

## ステップ 5: レイアウト プロパティを設定する

[レイアウト] プロパティを設定して、サイズ変更した図面に含めるレイアウトを指定します。

```csharp
cadRasterizationOptions.Layouts = new string[] { "Model" };
```

## ステップ 6: BMP にエクスポートする

最後に、Save メソッドを使用して、サイズ変更したレイアウトを BMP ファイルとして保存します。

```csharp
string outPath = sourceFilePath + ".bmp";
image.Save(outPath, bmpOptions);
```

これで、Aspose.CAD for .NET を使用して CAD 図面のサイズが正常に調整されました。

## 結論

このチュートリアルでは、Aspose.CAD を使用して .NET で CAD 図面のサイズを変更するプロセスを説明しました。これらの手順に従うことで、この機能をアプリケーションにシームレスに統合し、スムーズなユーザー エクスペリエンスを提供できます。

## よくある質問

### Q1: Aspose.CAD for .NET はすべての CAD 形式と互換性がありますか?

 A1: Aspose.CAD for .NET は、DWG、DXF、DWF などを含む幅広い CAD 形式をサポートしています。チェックしてください[ドキュメンテーション](https://reference.aspose.com/cad/net/)完全なリストについては、

### Q2: 複数のレイアウトのサイズを同時に変更できますか?

A2: はい、CadRasterizationOptions のレイアウト配列を調整することで、複数のレイアウトのサイズを変更できます。

### Q3: Aspose.CAD for .NET のサポートはどこで受けられますか?

 A3: にアクセスしてください。[Aspose.CAD フォーラム](https://forum.aspose.com/c/cad/19)コミュニティのサポートと支援のために。

### Q4: 無料トライアルはありますか?

 A4: はい、探索できます。[無料トライアル](https://releases.aspose.com/) Aspose.CAD for .NET の機能を評価します。

### Q5: Aspose.CAD for .NET の一時ライセンスを取得するにはどうすればよいですか?

 A5: テスト目的で一時ライセンスを取得します。[ここ](https://purchase.aspose.com/temporary-license/).