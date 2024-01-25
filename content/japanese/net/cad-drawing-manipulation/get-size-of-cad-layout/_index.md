---
title: Aspose.CAD for .NET で CAD レイアウトのサイズを取得する
linktitle: CADレイアウトのサイズを取得
second_title: Aspose.CAD .NET - CAD および BIM ファイル形式
description: Aspose.CAD を使用して .NET で CAD レイアウト サイズを取得する方法を学習します。 CAD ファイルを効率的に操作するには、ステップバイステップのガイドに従ってください。
type: docs
weight: 14
url: /ja/net/cad-drawing-manipulation/get-size-of-cad-layout/
---
## 導入

Aspose.CAD for .NET を使用して CAD レイアウトのサイズを取得するためのこの包括的なガイドへようこそ。 Aspose.CAD は、開発者が CAD ファイルをシームレスに操作できるようにする強力なライブラリです。このチュートリアルでは、実際の例と段階的な手順を使用して、CAD レイアウトのサイズを取得するプロセスを説明します。

## 前提条件

チュートリアルに入る前に、次の前提条件が満たされていることを確認してください。

-  Aspose.CAD for .NET: Aspose.CAD ライブラリがインストールされていることを確認してください。からダウンロードできます。[Aspose.CAD for .NET ダウンロード ページ](https://releases.aspose.com/cad/net/).

- ドキュメント ファイル: 使用する CAD ファイルを準備します。このチュートリアルでは、例として「conic_pyramid.dxf」と「Bottom_plate.dwg」を使用します。

さあ、始めましょう！

## 名前空間のインポート

.NET プロジェクトで、必要な名前空間をインポートすることから始めます。

```csharp
using System;
using System.Collections.Generic;
using System.IO;
using System.Linq;
using System.Text;
using Aspose.CAD;
using Aspose.CAD.FileFormats.Cad;
using Aspose.CAD.FileFormats.Cad.CadConsts;
using Aspose.CAD.FileFormats.Cad.CadObjects;
using Aspose.CAD.FileFormats.Cad.CadTables;
using Aspose.CAD.ImageOptions;
```

## ステップ 1: ドキュメント ディレクトリを設定する

ドキュメント ディレクトリへのパスを設定します。交換する`"Your Document Directory"`実際のパスを使用します。

```csharp
string MyDir = "Your Document Directory";
```

## ステップ 2: CAD ファイルのパスを指定する

分析する CAD ファイル パスの配列を定義します。この例では、「conic_pyramid.dxf」と「Bottom_plate.dwg」を使用します。

```csharp
string[] sourceFilePaths = new[]
{
    MyDir + "conic_pyramid.dxf",
    MyDir + "Bottom_plate.dwg"
};
```

## ステップ 3: CAD ファイルを反復処理する

各 CAD ファイルを反復処理して、レイアウト情報を取得します。

```csharp
foreach (var sourceFilePath in sourceFilePaths)
{
    string extension = Path.GetExtension(sourceFilePath);
    using (CadImage cadImage = (CadImage)Aspose.CAD.Image.Load(sourceFilePath))
    {
        // ... (次のステップに進みます)
    }
}
```

## ステップ 4: 空ではないレイアウトを取得する

CAD ファイル タイプに基づいて空ではないレイアウトを取得するヘルパー メソッドを定義します。

```csharp
private static List<string> GetNotEmptyLayouts(Image cadImage, string extension)
{
    // ... (次のステップに進みます)
}
```

## ステップ 5: DWG ファイルのレイアウトを取得する

DWG ファイルの空ではないレイアウトを取得するロジックを実装します。

```csharp
private static List<string> GetNotEmptyLayoutsForDwg(CadImage cadImage)
{
    // ... (次のステップに進みます)
}
```

## ステップ 6: DXF ファイルのレイアウトを取得する

DXF ファイルの空ではないレイアウトを取得するロジックを実装します。

```csharp
private static List<string> GetNotEmptyLayoutsForDxf(CadImage cadImage)
{
    // ... (次のステップに進みます)
}
```

## ステップ 7: レイアウト サイズを取得し、画像として保存する

レイアウト サイズを取得して画像として保存するプロセスを完了します。

```csharp
foreach (string layout in layouts)
{
    // ... (次のステップに進みます)
}
```

## 結論

おめでとう！ Aspose.CAD for .NET を使用して CAD レイアウトのサイズを取得する方法を学習しました。このチュートリアルでは、プロジェクトのセットアップからレイアウト情報の取得、画像としての保存までの重要な手順を説明しました。この知識を .NET アプリケーションに組み込んで、CAD ファイルを効率的に操作できるようになりました。

## よくある質問

### Q1: Aspose.CAD はすべての CAD ファイル形式と互換性がありますか?

A1: はい、Aspose.CAD は、DWG や DXF などのさまざまな CAD ファイル形式をサポートしています。

### Q2: 画像保存オプションをカスタマイズできますか?

A2: もちろんです！特定の要件に合わせて、形式や解像度などの画像オプションを調整できます。

### Q3: 追加のドキュメントはどこで入手できますか?

 A3: を参照してください。[Aspose.CAD ドキュメント](https://reference.aspose.com/cad/net/)詳細な情報と例については、

### Q4: 無料トライアルはありますか?

A4: はい、Aspose.CAD を使用して探索できます。[無料トライアル](https://releases.aspose.com/).

### Q5;技術サポートを受けるにはどうすればよいですか?

 A5: 技術サポートについては、次のサイトにアクセスしてください。[Aspose.CAD フォーラム](https://forum.aspose.com/c/cad/19).