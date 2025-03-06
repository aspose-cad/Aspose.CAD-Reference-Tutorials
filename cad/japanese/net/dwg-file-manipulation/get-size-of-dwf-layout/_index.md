---
title: C# での DWG ファイルの操作 - DWF レイアウトのサイズの取得
linktitle: C# での DWG ファイルの操作 - DWF レイアウトのサイズの取得
second_title: Aspose.CAD .NET - CAD および BIM ファイル形式
description: DWG ファイルの処理における Aspose.CAD for .NET の機能を試してください。 C# を使用して DWF レイアウト サイズを簡単に抽出する方法を学びます。
weight: 10
url: /ja/net/dwg-file-manipulation/get-size-of-dwf-layout/
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# C# での DWG ファイルの操作 - DWF レイアウトのサイズの取得

## 導入

コンピュータ支援設計 (CAD) および .NET 開発の分野では、Aspose.CAD は DWG ファイルを処理するための強力なツールとして機能します。このチュートリアルでは、C# で DWG ファイルを操作し、DWF レイアウトのサイズを抽出するプロセスを説明します。コードに入る前に、この旅に乗り出すためのすべての設定が完了していることを確認してください。

## 前提条件

このチュートリアルをスムーズに進めるには、次の前提条件が満たされていることを確認してください。

-  Aspose.CAD for .NET: Aspose.CAD for .NET がインストールされていることを確認します。からダウンロードできます。[Aspose.CAD for .NET ダウンロード ページ](https://releases.aspose.com/cad/net/).

必要なツールが揃ったので、コーディングの分野に飛び込みましょう。

## 名前空間のインポート

コードの作業を始める前に、必要な名前空間をインポートしましょう。

```csharp
using Aspose.CAD.FileFormats.Cad;
using Aspose.CAD.FileFormats.Dwf;
using Aspose.CAD.ImageOptions;
using System;
using System.Collections.Generic;
using System.IO;
using System.Linq;
using System.Text;
```

これらの名前空間は、C# アプリケーションで Aspose.CAD を使用して CAD ファイルを処理するための必須のクラスとメソッドを提供します。

## ステップ 1: 環境をセットアップする

まず、プロジェクトに適切な環境が設定されていることを確認します。 C# プロジェクトで Aspose.CAD ライブラリを参照します。

## ステップ 2: ファイル パスを定義する

DWG ファイルのパスと、生成された JPG ファイルの出力ディレクトリを定義します。

```csharp
string MyDir = "Your Document Directory";
string sourceFilePath = MyDir + "blocks_and_tables.dwf";
```

## ステップ 3: DWF イメージをロードする

Aspose.CAD を使用して DWF イメージをロードします。

```csharp
using (DwfImage image = (DwfImage)Aspose.CAD.Image.Load(sourceFilePath))
{
    //さらなるステップのコードはここにあります
}
```

## ステップ 4: ページを反復処理する

DWF イメージのページを繰り返し処理します。

```csharp
foreach (var page in image.Pages)
{
    //さらなるステップのコードはここにあります
}
```

## ステップ 5: レイアウト情報を取得する

各ページからレイアウト情報を取得します。

```csharp
var layout = page.Name;
System.Console.WriteLine("Layout= " + layout);
```

## ステップ 6: JPG オプションを設定する

レイアウトを JPG ファイルとして保存するためのオプションを設定します。

```csharp
using (FileStream fs = new FileStream(MyDir + "layout_" + layout + ".jpg", FileMode.Create))
{
    JpegOptions jpegOptions = new JpegOptions();
    CadRasterizationOptions options = new CadRasterizationOptions();
    options.Layouts = new string[] { layout };
    //さらなるステップのコードはここにあります
}
```

## ステップ 7: ページ サイズを決定する

DWF レイアウトのサイズを決定します。

```csharp
double sizeExtX = page.MaxPoint.X - page.MinPoint.X;
double sizeExtY = page.MaxPoint.Y - page.MinPoint.Y;
//さらなるステップのコードはここにあります
```

## ステップ 8: ページのサイズを設定する

ユニットタイプに基づいてページサイズを設定します。

```csharp
if (page.UnitType == UnitType.Inch)
{
    options.PageHeight = CommonHelper.INtoPixels(sizeExtY, CommonHelper.DPI);
    options.PageWidth = CommonHelper.INtoPixels(sizeExtX, CommonHelper.DPI);
}
else if (page.UnitType == UnitType.Millimeter)
{
    options.PageHeight = CommonHelper.MMtoPixels(sizeExtY, CommonHelper.DPI);
    options.PageWidth = CommonHelper.MMtoPixels(sizeExtX, CommonHelper.DPI);
}
else
{
    options.PageHeight = (float)sizeExtY;
    options.PageWidth = (float)sizeExtX;
}
```

## ステップ 9: JPG ファイルを保存する

指定したオプションを使用して JPG ファイルを保存します。

```csharp
jpegOptions.VectorRasterizationOptions = options;
image.Save(fs, jpegOptions);
}
```

これで、C# の Aspose.CAD を使用して DWG ファイルから DWF レイアウトのサイズが正常に抽出されました。 Aspose.CAD が .NET 開発に提供するその他の機能を自由に探索してください。

## 結論

このチュートリアルでは、Aspose.CAD を使用して C# で DWG ファイルを操作するプロセスを説明しました。これらの手順に従うと、DWF レイアウトのサイズを取得できるだけでなく、.NET プロジェクトでのさまざまな CAD 関連タスクに Aspose.CAD の機能を利用することもできます。

## よくある質問

### Q1: Aspose.CAD は最新の DWG ファイル形式と互換性がありますか?

 A1: Aspose.CAD は、最新バージョンを含むさまざまな DWG ファイル形式をサポートしています。を参照してください。[ドキュメンテーション](https://reference.aspose.com/cad/net/)特定の互換性の詳細については、

### Q2: Aspose.CAD は商用プロジェクトと個人プロジェクトの両方に使用できますか?

 A2: はい、Aspose.CAD は商用利用と個人利用の両方に柔軟なライセンス オプションを提供しています。訪問[購入ページ](https://purchase.aspose.com/buy)詳細については。

### Q3: Aspose.CAD の一時ライセンスを取得するにはどうすればよいですか?

A3: 一時ライセンスは以下から取得できます。[ここ](https://purchase.aspose.com/temporary-license/)評価目的のため。

### Q4: Aspose.CAD のサポートはどこで見つけられますか?

A4: ご質問やサポートが必要な場合は、次のサイトにアクセスしてください。[Aspose.CAD フォーラム](https://forum.aspose.com/c/cad/19).

### Q5: Aspose.CAD の無料トライアルはありますか?

 A5: はい、Aspose.CAD の無料試用版にアクセスできます。[ここ](https://releases.aspose.com/).
{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}
