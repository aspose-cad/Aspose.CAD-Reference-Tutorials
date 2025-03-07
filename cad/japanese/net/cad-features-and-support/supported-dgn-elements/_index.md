---
title: Aspose.CAD for .NET でサポートされる DGN 要素
linktitle: サポートされている DGN 要素
second_title: Aspose.CAD .NET - CAD および BIM ファイル形式
description: DGN ファイルを処理するための Aspose.CAD for .NET の強力な機能を調べてください。ステップバイステップのガイドに従って、2D 要素と 3D 要素をシームレスに操作します。
weight: 18
url: /ja/net/cad-features-and-support/supported-dgn-elements/
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Aspose.CAD for .NET でサポートされる DGN 要素

## 導入

あなたは、DGN ファイルをシームレスに操作したいと考えている .NET 開発者ですか? Aspose.CAD for .NET は、DGN ファイルを効率的に処理するための堅牢なソリューションを提供します。このチュートリアルでは、サポートされている DGN 要素について詳しく説明し、Aspose.CAD for .NET を使用するプロセスをガイドします。

## 前提条件

始める前に、以下のものがあることを確認してください。

- .NET プログラミングの基本的な知識。
- Visual Studio がマシンにインストールされていること。
- ダウンロードできる Aspose.CAD for .NET ライブラリ[ここ](https://releases.aspose.com/cad/net/).

## 名前空間のインポート

プロジェクトを開始するには、必要な名前空間を .NET アプリケーションにインポートします。この手順により、Aspose.CAD for .NET によって提供される機能に確実にアクセスできるようになります。

```csharp
using System;
using System.Collections.Generic;
using System.Linq;
using System.Text;
using System.Threading.Tasks;
using Aspose.CAD;
using Aspose.CAD.FileFormats.Dgn;
using Aspose.CAD.FileFormats.Dgn.DgnElements;
```

## ステップ 1: DGN ファイルをロードする

まず、既存の DGN ファイルを .NET アプリケーションに CadImage としてロードします。

```csharp
string MyDir = "Your Document Directory";
string sourceFilePath = MyDir + "Nikon_D90_Camera.dgn";

using (DgnImage dgnImage = (DgnImage)Image.Load(sourceFilePath))
{
    //コードはここにあります
}
```

## ステップ 2: DGN 要素を反復処理する

foreach ループを使用して DGN 要素を反復処理します。 Aspose.CAD for .NET は、操作できるさまざまな DGN 要素タイプを提供します。

```csharp
foreach (DgnDrawingElementBase element in dgnImage.Elements)
{
    //コードはここにあります
}
```

## ステップ 3: 以前にサポートされていたエンティティを処理する

以前にサポートされていた 2D エンティティを処理しますが、現在は 3D でもサポートされています。

```csharp
switch (element.Metadata.Type)
{
    case DgnElementType.Line:
    case DgnElementType.Ellipse:
    case DgnElementType.Curve:
    //追加のケース
        {
            //コードはここにあります
            break;
        }
}
```

## ステップ 4: サポートされている 3D エンティティを処理する

Aspose.CAD for .NET によって提供されるサポートされている 3D エンティティを処理します。

```csharp
switch (element.Metadata.Type)
{
    case DgnElementType.SolidHeader3D:
    case DgnElementType.Cone:
    case DgnElementType.CellHeader:
        {
            //コードはここにあります
            break;
        }
}
```

## ステップ 5: エクスポートして保存する

最後に、変更した DGN ファイルをラスター イメージにエクスポートし、指定したディレクトリに保存します。

```csharp
Console.WriteLine("\nThe DGN file exported successfully to raster image.\nFile saved at " + MyDir);
```

## 結論

このチュートリアルでは、DGN ファイルの処理および操作における Aspose.CAD for .NET の機能を検討しました。ステップバイステップのガイドに従うことで、2D エンティティでも 3D エンティティでも、サポートされている DGN 要素を効率的に操作できます。 Aspose.CAD for .NET を使用すると、DGN ファイル処理を .NET アプリケーションにシームレスに統合できます。

## よくある質問

### Q1: Aspose.CAD for .NET のドキュメントはどこで見つけられますか?

 A1: ドキュメントは見つかります。[ここ](https://reference.aspose.com/cad/net/).

### Q2: Aspose.CAD for .NET をダウンロードするにはどうすればよいですか?

 A2: ライブラリをダウンロードできます。[ここ](https://releases.aspose.com/cad/net/).

### Q3: Aspose.CAD for .NET の無料トライアルはありますか?

A3: はい、無料トライアルにアクセスできます。[ここ](https://releases.aspose.com/).

### Q4: Aspose.CAD for .NET の一時ライセンスはどこで入手できますか?

 A4: 一時ライセンスが利用可能です[ここ](https://purchase.aspose.com/temporary-license/).

### Q5: サポートが必要ですか、それとも質問がありますか?

A5: Aspose.CAD for .NET コミュニティにアクセスしてください。[サポートフォーラム](https://forum.aspose.com/c/cad/19).
{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}
