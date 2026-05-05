---
date: 2026-04-06
description: Aspose.CAD を使用して C# で DWF を JPG に変換する方法を学び、DWG ファイルから DWF のレイアウトサイズを抽出する方法を発見しましょう。
keywords:
- convert dwf to jpg
- how to extract dwf
- convert dwg to jpg
linktitle: C#でDWGファイルを扱う - DWFレイアウトのサイズ取得
second_title: Aspose.CAD .NET - CAD and BIM File Format
title: C#でDWFをJPGに変換 – DWGからDWFレイアウトサイズを取得
url: /ja/net/dwg-file-manipulation/get-size-of-dwf-layout/
weight: 10
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# C#でDWFをJPGに変換 – DWGからDWFレイアウトサイズを取得

## はじめに

DWFを**convert DWF to JPG**しながら正確なレイアウト寸法も把握したい場合は、ここが適切です。このチュートリアルでは、Aspose.CAD for .NET を使用して DWG から派生した DWF ファイルを開き、各レイアウトのサイズを読み取り、レイアウトを高品質な JPG 画像として保存する、完全なエンドツーエンドの例を順を追って説明します。最後まで読むと、DWF のレイアウト情報の抽出方法が分かるだけでなく、任意の C# プロジェクトに組み込める再利用可能なコードスニペットも手に入ります。

## クイック回答

- **What does “convert DWF to JPG” mean?** それはベクタ DWF レイアウトをビットマップ JPEG 画像にラスタライズすることを意味します。  
- **Why read layout size first?** 正確な範囲を把握することで、正しいページ寸法を設定でき、伸びたり切れたりする出力を防げます。  
- **Which library handles this?** Aspose.CAD for .NET は DWG、DWF およびラスタ画像変換をフルサポートします。  
- **Do I need a license?** 評価用の一時ライセンスで動作しますが、本番環境ではフルライセンスが必要です。  
- **What .NET versions are supported?** .NET Framework 4.5+、.NET Core 3.1+、.NET 5/6/7。

## 「convert DWF to JPG」とは何か、そしてなぜ重要か

DWF (Design Web Format) ファイルを JPG に変換すると、ブラウザで表示したり、レポートに埋め込んだり、CAD ソフトを持っていないステークホルダーと共有できるポータブルな画像が作成されます。変換により、標準的な画像処理ツールを使用して画像を操作（リサイズ、圧縮、透かし）する柔軟性も得られます。

## なぜ DWF レイアウトサイズを抽出するのか

DWF ファイルは複数のレイアウトを含むことができ、各レイアウトは独自の座標系と単位（インチ、ミリメートルなど）を持ちます。レイアウトサイズを抽出することで、以下が可能になります：

1. ラスタライズ時に元のアスペクト比を保持する。  
2. 高解像度出力に適した DPI を選択する。  
3. 手動調整なしで多数のレイアウトをバッチ処理できる。

## 前提条件

このチュートリアルをシームレスに進めるには、以下の前提条件が整っていることを確認してください。

- Aspose.CAD for .NET: Aspose.CAD for .NET がインストールされていることを確認してください。ダウンロードは [Aspose.CAD for .NET download page](https://releases.aspose.com/cad/net/) から行えます。

ライブラリが用意できていれば、依存関係を探す手間なくコードに集中できます。

## 名前空間のインポート

コードを書き始める前に、必要な名前空間をインポートします。これらは CAD ファイル、ラスタライズオプション、ファイル I/O を操作するためのクラスを提供します。

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

## ステップ 1: 環境の設定

新しい C# コンソールまたはクラスライブラリ プロジェクトを作成し、**Aspose.CAD.dll** への参照を追加し、プロジェクトが互換性のある .NET バージョンを対象としていることを確認してください。

## ステップ 2: ファイルパスの定義（DWF の抽出方法）

ソース DWF ファイルの場所と、生成された JPG ファイルを書き込む場所を指定します。

```csharp
string MyDir = "Your Document Directory";
string sourceFilePath = MyDir + "blocks_and_tables.dwf";
```

> **Pro tip:** 異なる OS での安全なパス処理のために `Path.Combine(MyDir, "blocks_and_tables.dwf")` を使用してください。

## ステップ 3: DWF 画像のロード

`Aspose.CAD.Image` オブジェクトに DWF ファイルをロードします。ページ固有のプロパティにアクセスする必要があるため、`DwfImage` にキャストします。

```csharp
using (DwfImage image = (DwfImage)Aspose.CAD.Image.Load(sourceFilePath))
{
    // Code for further steps will go here
}
```

## ステップ 4: ページを反復処理

DWF には複数のページ（レイアウト）が含まれることがあります。各ページをループして個別に処理できるようにします。

```csharp
foreach (var page in image.Pages)
{
    // Code for further steps will go here
}
```

## ステップ 5: レイアウト情報の取得

ループ内でレイアウト名を取得します。この名前はログ出力と出力 JPG ファイルの命名の両方に使用されます。

```csharp
var layout = page.Name;
System.Console.WriteLine("Layout= " + layout);
```

## ステップ 6: JPG オプションの設定

`JpegOptions` インスタンスを作成し、ラスタライズオプションを設定します。`Layouts` プロパティで Aspose.CAD にどのレイアウトをレンダリングするか指示します。

```csharp
using (FileStream fs = new FileStream(MyDir + "layout_" + layout + ".jpg", FileMode.Create))
{
    JpegOptions jpegOptions = new JpegOptions();
    CadRasterizationOptions options = new CadRasterizationOptions();
    options.Layouts = new string[] { layout };
    // Code for further steps will go here
}
```

## ステップ 7: ページサイズの決定（convert dwg to jpg）

レイアウトの幅と高さを元の単位で計算します。この情報はラスタページサイズを正確に設定するために不可欠です。

```csharp
double sizeExtX = page.MaxPoint.X - page.MinPoint.X;
double sizeExtY = page.MaxPoint.Y - page.MinPoint.Y;
// Code for further steps will go here
```

## ステップ 8: ページ寸法の設定

Aspose.CAD が提供するヘルパーメソッドを使用して、元の単位（インチまたはミリメートル）をピクセルに変換します。単位タイプがどちらでもない場合は、生の値を使用します。

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

## ステップ 9: JPG ファイルの保存

最後に、ラスタライズオプションを JPEG オプションにバインドし、画像をディスクに保存します。

```csharp
jpegOptions.VectorRasterizationOptions = options;
image.Save(fs, jpegOptions);
}
```

ループが完了すると、各レイアウトごとに JPG ファイルが作成され、元の DWF の寸法と正確に一致するサイズになります。

## 一般的な問題と解決策

| 症状 | 考えられる原因 | 対策 |
|---------|--------------|-----|
| Empty JPG output | `options.Layouts` が正しく設定されていない | レイアウト名が `page.Name` と一致しているか確認してください。 |
| Distorted image | DPI 変換が間違っている | 変換前に `CommonHelper.DPI = 300`（または目標 DPI）を設定してください。 |
| File not found | `MyDir` パスが間違っている | 絶対パスを使用するか `Path.Combine` を使用してください。 |
| License exception | ライセンスが適用されていない | `Image.Load` を呼び出す前に一時または永続ライセンスをロードしてください。 |

## よくある質問

### Q1: Aspose.CAD は最新の DWG ファイル形式と互換性がありますか？

A1: Aspose.CAD はさまざまな DWG ファイル形式をサポートしており、最新バージョンも含まれます。具体的な互換性の詳細は [documentation](https://reference.aspose.com/cad/net/) を参照してください。

### Q2: Aspose.CAD を商用および個人プロジェクトの両方で使用できますか？

A2: はい、Aspose.CAD は商用・個人利用の両方に対応した柔軟なライセンスオプションを提供しています。詳細は [purchase page](https://purchase.aspose.com/buy) をご覧ください。

### Q3: Aspose.CAD の一時ライセンスはどのように取得できますか？

A3: 評価目的での一時ライセンスは [here](https://purchase.aspose.com/temporary-license/) から取得できます。

### Q4: Aspose.CAD のサポートはどこで受けられますか？

A4: ご質問やサポートが必要な場合は、[Aspose.CAD forum](https://forum.aspose.com/c/cad/19) をご利用ください。

### Q5: Aspose.CAD の無料トライアルはありますか？

A5: はい、Aspose.CAD の無料トライアル版は [here](https://releases.aspose.com/) から入手できます。

### Q6: DWF を抽出せずに DWG ファイルを直接 JPG に変換するにはどうすればよいですか？

A6: `Aspose.CAD.Image.Load` で DWG ファイルをロードし、同じラスタライズ手順を使用できます。`options.Layouts` に DWG から取得した目的のレイアウト名を設定するだけです。

### Q7: 変換はベクタ品質を保持しますか？

A7: JPG にラスタライズすると画像はビットマップベースになるため、ベクタの拡大縮小は失われます。ロスレスなスケーリングが必要な場合は、代わりに PNG や SVG へのエクスポートを検討してください。

---

**最終更新日:** 2026-04-06  
**テスト環境:** Aspose.CAD 24.11 for .NET  
**作者:** Aspose  

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}