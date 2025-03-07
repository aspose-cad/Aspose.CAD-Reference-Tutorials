---
title: CAD 図面を SVG 形式にエクスポート - Aspose.CAD ガイド
linktitle: CAD 図面を SVG 形式にエクスポートする
second_title: Aspose.CAD .NET - CAD および BIM ファイル形式
description: Aspose.CAD for .NET を使用して CAD 図面を SVG にエクスポートするシームレスなプロセスを確認してください。柔軟性とカスタマイズにより CAD 開発を強化します。
weight: 15
url: /ja/net/advanced-export-techniques/exporting-cad-drawings-to-svg/
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# CAD 図面を SVG 形式にエクスポート - Aspose.CAD ガイド

## 導入

CAD (コンピューター支援設計) のダイナミックな世界では、図面をさまざまな形式にエクスポートする機能が重要なスキルです。 SVG (Scalable Vector Graphics) は、そのスケーラビリティと多用途性により人気を集めているフォーマットの 1 つです。このチュートリアルでは、強力な Aspose.CAD for .NET ライブラリを使用して CAD 図面を SVG にエクスポートする方法を説明します。

## 前提条件

チュートリアルに入る前に、次の前提条件が満たされていることを確認してください。

-  Aspose.CAD for .NET ライブラリ: Aspose.CAD for .NET ライブラリをダウンロードしてインストールします。図書館を見つけることができます[ここ](https://releases.aspose.com/cad/net/).

- 開発環境: Visual Studio またはその他の .NET 開発ツールを使用して、適切な開発環境をセットアップします。

## 名前空間のインポート

まず、必要な名前空間をプロジェクトにインポートします。

```csharp
using Aspose.CAD.ImageOptions;
using System;
using System.Collections.Generic;
using System.Linq;
using System.Text;
```

## ステップ 1: ドキュメント ディレクトリを設定する

```csharp
//ドキュメントディレクトリへのパス。
string MyDir = "Your Document Directory";
```

## ステップ 2: CAD 図面をロードする

```csharp
using (Image image = Image.Load(MyDir + "sample.dwg"))
{
```

## ステップ 3: SVG エクスポート オプションを構成する

```csharp
    var options = new SvgOptions();
    options.ColorType = SvgColorMode.Grayscale;
    options.TextAsShapes = true;
```

## ステップ 4: SVG ファイルを保存する

```csharp
    image.Save(MyDir + "sample.svg", options);
}
```

これらの簡単な手順に従うことで、Aspose.CAD for .NET を使用して CAD 図面を SVG にシームレスにエクスポートできます。このライブラリには柔軟性とカスタマイズ オプションが用意されており、要件に応じて出力を調整できます。

## 結論

結論として、Aspose.CAD for .NET は、CAD 図面を SVG にエクスポートするプロセスを簡素化します。その直観的な API と堅牢な機能により、CAD アプリケーションを使用する開発者にとって貴重なツールになります。

## よくある質問

### Q1: Aspose.CAD はすべての CAD 形式と互換性がありますか?

A1: Aspose.CAD は、DWG や DXF を含むさまざまな CAD 形式をサポートし、幅広い互換性を保証します。

### Q2: SVG にエクスポートするときにカラー モードをカスタマイズできますか?

A2: はい、Aspose.CAD ではカラー モードを選択できるため、出力に柔軟性が得られます。

### Q3: 一時ライセンスはテスト目的で利用できますか?

 A3: はい、一時ライセンスを取得できます。[ここ](https://purchase.aspose.com/temporary-license/)評価用に。

### Q4: Aspose.CAD の詳細なドキュメントはどこで入手できますか?

 A4: ドキュメントは入手可能です[ここ](https://reference.aspose.com/cad/net/).

### Q5: Aspose.CAD に関するサポートを受けたり、質問したりするにはどうすればよいですか?

 A5: コミュニティフォーラムにアクセスしてください[ここ](https://forum.aspose.com/c/cad/19)サポートとディスカッションのため。
{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}
