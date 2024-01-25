---
title: Aspose.CAD for .NET での DGN V7 の 3D のサポート
linktitle: DGN V7 の 3D のサポート
second_title: Aspose.CAD .NET - CAD および BIM ファイル形式
description: Aspose.CAD for .NET の DGN V7 の 3D サポートのパワーを解放します。ステップバイステップのチュートリアルに従ってください。
type: docs
weight: 20
url: /ja/net/cad-features-and-support/support-of-3d-for-dgn-v7/
---
## 導入

Aspose.CAD for .NET での DGN V7 の 3D サポートの活用に関する包括的なチュートリアルへようこそ。 Aspose.CAD は、開発者が .NET アプリケーションで CAD ファイルをシームレスに操作できるようにする強力なライブラリです。このチュートリアルでは、DGN V7 の 3D サポートを利用する手順を検討し、CAD 関連プロジェクトを強化するための知識を提供します。

## 前提条件

チュートリアルに入る前に、次の前提条件が満たされていることを確認してください。

-  Aspose.CAD for .NET: Aspose.CAD for .NET がインストールされていることを確認します。そうでない場合は、からダウンロードできます[ここ](https://releases.aspose.com/cad/net/).

- 開発環境: .NET アプリケーション開発に適した開発環境 (Visual Studio など) をセットアップします。

- サンプル DGN ファイル: テスト用にサンプル DGN ファイルを用意します。付属のサンプルファイル「Nikon_D90_Camera.dgn」をご利用いただけます。

それでは、Aspose.CAD for .NET を使用して DGN V7 の 3D サポートを実現する手順に移りましょう。

## 名前空間のインポート

.NET アプリケーションで、必要な名前空間をインポートすることから始めます。

```csharp
using System;
using System.Collections.Generic;
using System.Linq;
using System.Text;
using System.Threading.Tasks;
using Aspose.CAD;
using Aspose.CAD.FileFormats.Dgn;
using Aspose.CAD.ImageOptions;
```

## ステップ 1: ドキュメント ディレクトリを設定する

プロジェクト内にドキュメント ディレクトリが設定されていることを確認してください。交換する`"Your Document Directory"`ドキュメントディレクトリへの実際のパスを置き換えます。

```csharp
string MyDir = "Your Document Directory";
```

## ステップ 2: DGN ファイルをロードする

次のコードを使用して、既存の DGN ファイルを CadImage としてロードします。

```csharp
string sourceFilePath = MyDir + "Nikon_D90_Camera.dgn";
string outFile = MyDir + "Nikon_D90_Camera.dgn";

using (DgnImage dgnImage = (DgnImage)Image.Load(sourceFilePath))
{
    //さらに処理するためのコードはここにあります
}
```

## ステップ 3: PDF エクスポート オプションを構成する

PDF にエクスポートするためのオプションを設定し、ページ寸法、自動レイアウト スケーリング、背景色、エクスポートするレイアウトなどのベクトル ラスタライズ オプションを指定します。

```csharp
var options = new PdfOptions
{
    VectorRasterizationOptions = new CadRasterizationOptions
    {
        PageWidth = 1500,
        PageHeight = 1500,
        AutomaticLayoutsScaling = true,
        BackgroundColor = Color.Black,
        Layouts = new string[] { "1", "2", "3", "9" } //指定されたビューのみをエクスポートする
    }
};
```

## ステップ 4: ラスター画像を保存する

構成されたオプションを使用して、DGN ファイルをラスター イメージとして保存します。

```csharp
dgnImage.Save(outFile, options);
```

## 結論

おめでとう！ Aspose.CAD for .NET を利用して、3D サポート付きの DGN ファイルをラスター イメージにエクスポートすることに成功しました。このチュートリアルでは、この機能を CAD プロジェクトに統合するための重要な手順を説明しました。

## よくある質問

### Q1: Aspose.CAD for .NET を他の CAD ファイル形式で使用できますか?

A1: はい、Aspose.CAD は、DWG や DXF などのさまざまな CAD ファイル形式をサポートしています。

### Q2: Aspose.CAD を使用するときに例外を処理するにはどうすればよいですか?

A2: 例外を適切に処理するには、提供された例に示されているように、コードを try-catch ブロックで囲みます。

### Q3: Aspose.CAD は商用プロジェクトに適していますか?

 A3：もちろんです！ Aspose.CAD for .NET を購入できます[ここ](https://purchase.aspose.com/buy).

### Q4: 購入する前に Aspose.CAD for .NET を試すことはできますか?

A4：確かに！無料トライアルを試してみる[ここ](https://releases.aspose.com/).

### Q5: Aspose.CAD for .NET のコミュニティ サポートはどこで見つけられますか?

 A5: コミュニティフォーラムにアクセスしてください[ここ](https://forum.aspose.com/c/cad/19).