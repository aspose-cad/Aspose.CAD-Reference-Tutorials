---
title: CAD 図面に透かしを追加する - Aspose.CAD ガイド
linktitle: CAD 図面に透かしを追加する
second_title: Aspose.CAD .NET - CAD および BIM ファイル形式
description: Aspose.CAD for .NET を使用して、プロフェッショナルなウォーターマークで CAD 図面を強化します。パーソナライズされた魅力的なデザインについては、ステップバイステップのガイドに従ってください。
weight: 11
url: /ja/net/plt-and-watermarking/adding-watermarks-to-cad-drawings/
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# CAD 図面に透かしを追加する - Aspose.CAD ガイド

## 導入

プロの透かしを追加して CAD 図面を強化したいと考えていますか? Aspose.CAD for .NET は、透かしを CAD ファイルにシームレスに統合するための堅牢なソリューションを提供します。このステップバイステップのガイドでは、Aspose.CAD を使用して透かしを追加するプロセスを説明し、図面に重要な情報を伝えるだけでなく、独自のマークも確実に伝えることができます。

## 前提条件

チュートリアルに入る前に、次のものが揃っていることを確認してください。
-  Aspose.CAD for .NET: Aspose.CAD ライブラリがインストールされていることを確認してください。ダウンロードできます[ここ](https://releases.aspose.com/cad/net/).
- ドキュメント ディレクトリ: CAD 図面を保存するディレクトリを設定します。
それでは、CAD 図面に透かしを追加してみましょう。

## 名前空間のインポート

まず、必要な名前空間を .NET プロジェクトにインポートします。

```csharp
using Aspose.CAD.FileFormats.Cad;
using Aspose.CAD.FileFormats.Cad.CadObjects;
using Aspose.CAD.ImageOptions;
using System;
using System.Collections.Generic;
using System.Linq;
using System.Text;
```

## ステップ 1: CAD 図面をロードする

```csharp
//ドキュメントディレクトリへのパス。
string MyDir = "Your Document Directory";
using (CadImage cadImage = (CadImage)Image.Load(MyDir + "Drawing11.dwg")) {
```

## ステップ 2: 透かしをマルチテキストとして追加する

```csharp
//新しいマルチテキストを追加
CadMText watermark = new CadMText();
watermark.Text = "Watermark message";
watermark.InitialTextHeight = 40;
watermark.InsertionPoint = new Cad3DPoint(300, 40);
watermark.LayerName = "0";
cadImage.BlockEntities["*Model_Space"].AddEntity(watermark);
```

## ステップ 3: または透かしをテキストとして追加する

```csharp
//あるいは、Text のような単純なエンティティを追加します。
CadText text = new CadText();
text.DefaultValue = "Watermark text";
text.TextHeight = 40;
text.FirstAlignment = new Cad3DPoint(300, 40);
text.LayerName = "0";
cadImage.BlockEntities["*Model_Space"].AddEntity(text);
```

## ステップ 4: PDF にエクスポートする

```csharp
//ウォーターマーク付きの CAD 図面を PDF にエクスポート
CadRasterizationOptions rasterizationOptions = new CadRasterizationOptions();
rasterizationOptions.PageWidth = 1600;
rasterizationOptions.PageHeight = 1600;
rasterizationOptions.Layouts = new[] { "Model" };
PdfOptions pdfOptions = new PdfOptions();
pdfOptions.VectorRasterizationOptions = rasterizationOptions;
cadImage.Save(MyDir + "AddWatermark_out.pdf", pdfOptions);
```

さまざまな図面に対してこれらの手順を繰り返すと、すぐに本格的な透かし入りの CAD ファイルが完成します。

## 結論

おめでとう！ Aspose.CAD for .NET を使用して CAD 図面に透かしを追加する方法を学習しました。このシンプルかつ強力なプロセスにより、技術図面の整合性を維持しながらデザインをカスタマイズできます。

## よくある質問

### Q1: 透かしの外観をカスタマイズできますか?

A1: はい、好みに応じて透かしのテキスト、フォント、サイズ、位置をカスタマイズできます。

### Q2: Aspose.CAD はさまざまな CAD ファイル形式と互換性がありますか?

A2: Aspose.CAD は、DWG や DXF などのさまざまな CAD ファイル形式をサポートしており、幅広い互換性を確保しています。

### Q3: 単一の CAD 図面に複数の透かしを追加できますか?

A3：もちろんです！必要に応じてウォーターマークを追加できるため、さまざまなユースケースに柔軟に対応できます。

### Q4: Aspose.CAD は無料トライアルを提供していますか?

A4: はい、無料トライアルで Aspose.CAD の機能を試すことができます。それを得る[ここ](https://releases.aspose.com/).

### Q5: Aspose.CAD のサポートはどこで見つけられますか?

 A5: ご質問やサポートが必要な場合は、次のサイトにアクセスしてください。[Aspose.CAD フォーラム](https://forum.aspose.com/c/cad/19).
{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}
