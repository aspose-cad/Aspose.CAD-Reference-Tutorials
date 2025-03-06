---
title: BMP 形式へのエクスポート - Aspose.CAD チュートリアル
linktitle: BMP 形式へのエクスポート
second_title: Aspose.CAD .NET - CAD および BIM ファイル形式
description: Aspose.CAD for .NET を使用して、3D 画像を BMP にエクスポートするシームレスな世界を体験してください。チュートリアルに従って、手間のかからない体験をしてください。
weight: 11
url: /ja/net/file-format-conversion/exporting-to-bmp-format/
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# BMP 形式へのエクスポート - Aspose.CAD チュートリアル

## 導入

ソフトウェア開発のダイナミックな世界では、Aspose.CAD for .NET はコンピュータ支援設計 (CAD) ファイルを処理するための強力なツールとして際立っています。 CAD イメージを広く使用されている BMP 形式にエクスポートしたい場合は、このチュートリアルが頼りになるガイドです。この段階的なウォークスルーでは、Aspose.CAD for .NET を使用して 3D 画像を BMP にエクスポートするプロセスについて説明します。飛び込んでみましょう！

## 前提条件

このチュートリアルを開始する前に、次の前提条件が満たされていることを確認してください。

-  Aspose.CAD for .NET:Aspose.CAD ライブラリを次からダウンロードしてインストールします。[ここ](https://releases.aspose.com/cad/net/).
- 開発環境: .NET 開発環境をセットアップします。
- CAD ファイル: エクスポートできる CAD ファイルを用意します。この例では、「18-12-11 9644 - site.dwf」を使用します。

## 名前空間のインポート

.NET プロジェクトで、必要な名前空間を必ずインポートしてください。

```csharp
using System;
using System.Collections.Generic;
using System.Linq;
using System.Text;
using System.Threading.Tasks;
using Aspose.CAD;
using Aspose.CAD.ImageOptions;
```

## ステップ 1: CAD イメージをロードする

まず、CAD イメージをプロジェクトにロードします。 「Your Document Directory」を実際のディレクトリ パスに置き換えます。

```csharp
string MyDir = "Your Document Directory";
string inputFile = MyDir + "18-12-11 9644 - site.dwf";

using (Image image = Image.Load(inputFile))
{
    //画像をロードするためのコードはここにあります
}
```

## ステップ 2: BMP エクスポート オプションを構成する

CAD ファイルのベクトル ラスタライズ オプションを含む、BMP エクスポート オプションを設定します。

```csharp
BmpOptions bmpOptions = new BmpOptions();
var dwfRasterizationOptions = new CadRasterizationOptions();
bmpOptions.VectorRasterizationOptions = dwfRasterizationOptions;

dwfRasterizationOptions.PageHeight = 500;
dwfRasterizationOptions.PageWidth = 500;
```

## ステップ 3: BMP にエクスポートする

BMPファイルの出力パスを指定してエクスポート処理を実行します。

```csharp
string outPath = MyDir + "18-12-11 9644 - site.bmp";
image.Save(outPath, bmpOptions);
```

## 結論

おめでとう！ Aspose.CAD for .NET を使用して 3D イメージを BMP に正常にエクスポートしました。このチュートリアルでは、複雑なタスクを簡単に行えるようにする Aspose.CAD の多用途性を垣間見ることができます。

## よくある質問

### Q1: Aspose.CAD for .NET はどの CAD ファイル形式でも使用できますか?

A1: はい、Aspose.CAD はさまざまな CAD ファイル形式をサポートしており、プロジェクトに柔軟性をもたらします。

### Q2: 一時ライセンスはテスト目的で利用できますか?

 A2：確かに！仮免許を取得できます[ここ](https://purchase.aspose.com/temporary-license/)評価用に。

### Q3: Aspose.CAD の包括的なドキュメントはどこで入手できますか?

 A3: ドキュメントを参照してください。[ここ](https://reference.aspose.com/cad/net/)詳細な情報と例については、

### Q4: サポートを求めたり、コミュニティとつながったりするにはどうすればよいですか?

 A4: Aspose.CAD フォーラムにアクセスしてください。[ここ](https://forum.aspose.com/c/cad/19)質問したり、コミュニティと交流したりするためです。

### Q5: Aspose.CAD for .NET を購入できますか?

 A5: はい、Aspose.CAD を購入できます。[ここ](https://purchase.aspose.com/buy)プロジェクトの可能性を最大限に引き出します。

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}
