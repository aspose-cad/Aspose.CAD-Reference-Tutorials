---
title: 異なるレイアウトで単一の PDF を作成する - Aspose.CAD ガイド
linktitle: 異なるレイアウトで単一の PDF を作成する
second_title: Aspose.CAD .NET - CAD および BIM ファイル形式
description: Aspose.CAD for .NET を使用して、異なるレイアウトを持つ単一の PDF を作成します。シームレスな統合と効率的な PDF 生成については、ステップバイステップのガイドに従ってください。
type: docs
weight: 13
url: /ja/net/advanced-cad-techniques/creating-single-pdf-with-different-layouts/
---
## 導入

Aspose.CAD for .NET を使用して、さまざまなレイアウトを持つ CAD 図面から単一の PDF ドキュメントを生成したいと考えていますか?このステップバイステップのガイドでは、プロセスを順を追って説明し、シームレスな統合と効率的な PDF 作成を実現するのに役立ちます。 Aspose.CAD for .NET は、CAD 図面をプログラムで操作するための強力な機能を提供します。このチュートリアルでは、異なるレイアウトを持つ単一の PDF を作成することに焦点を当てます。

## 前提条件

チュートリアルに進む前に、次の前提条件を満たしていることを確認してください。

-  Aspose.CAD for .NET: Aspose.CAD for .NET がインストールされていることを確認してください。からダウンロードできます[ここ](https://releases.aspose.com/cad/net/).

- 開発環境: .NET 開発環境をセットアップし、C# プログラミングの基本を理解します。

## 名前空間のインポート

C# プロジェクトに、Aspose.CAD for .NET の機能を活用するために必要な名前空間を含めます。

```csharp
using Aspose.CAD.FileFormats.Cad;
using Aspose.CAD.ImageOptions;
using System;
using System.Collections.Generic;
using System.Linq;
using System.Text;
```

## ステップ 1: CAD イメージをロードする

```csharp
//ドキュメントディレクトリへのパス。
string MyDir = "Your Document Directory";

using (CadImage cadImage = (CadImage)Image.Load(MyDir + "City skyway map.dwg"))
{
    //ステップ 1 のコードはここにあります
}
```

## ステップ 2: ラスタライズ オプションをカスタマイズする

```csharp
CadRasterizationOptions rasterizationOptions = new CadRasterizationOptions();
rasterizationOptions.PageWidth = 1000;
rasterizationOptions.PageHeight = 1000;

//複数のレイアウトのカスタム サイズ
rasterizationOptions.LayoutPageSizes.Add("ANSI C Plot", new SizeF(500, 1000));
rasterizationOptions.LayoutPageSizes.Add("8.5 x 11 Plot", new SizeF(1000, 100));
```

## ステップ 3: PDF オプションを定義する

```csharp
PdfOptions pdfOptions = new PdfOptions() { VectorRasterizationOptions = rasterizationOptions };
```

## ステップ 4: PDF として保存

```csharp
cadImage.Save(MyDir + "singlePDF_out.pdf", pdfOptions);
```

これで、Aspose.CAD for .NET を使用して、さまざまなレイアウトを持つ単一の PDF ドキュメントが正常に作成されました。自由にさらに多くの機能を探索し、特定の要件に応じてコードをカスタマイズしてください。

## 結論

このチュートリアルでは、Aspose.CAD for .NET を使用して、さまざまなレイアウトを持つ CAD 図面から単一の PDF を作成するプロセスについて説明しました。この強力なライブラリは、CAD 操作タスクを簡素化し、さまざまなシナリオに柔軟性を提供します。

## よくある質問

### Q1: Aspose.CAD for .NET を他の CAD 形式で使用できますか?

A1: はい、Aspose.CAD for .NET は、DWG、DXF、DGN などのさまざまな CAD 形式をサポートしています。

### Q2: 無料トライアルはありますか?

 A2: はい、無料トライアルを試すことができます[ここ](https://releases.aspose.com/).

### Q3: Aspose.CAD for .NET のサポートを受けるにはどうすればよいですか?

 A3: にアクセスしてください。[Aspose.CAD フォーラム](https://forum.aspose.com/c/cad/19)コミュニティサポートのために。

### Q4: 詳細なドキュメントはどこで入手できますか?

 A4: ドキュメントを参照してください。[ここ](https://reference.aspose.com/cad/net/).

### Q5: Aspose.CAD for .NET のライセンスを購入できますか?

 A5: はい、ライセンスを購入できます。[ここ](https://purchase.aspose.com/buy).