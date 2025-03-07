---
title: 3D 画像を PDF にエクスポート - Aspose.CAD チュートリアル
linktitle: 3D 画像を PDF にエクスポートする
second_title: Aspose.CAD .NET - CAD および BIM ファイル形式
description: Aspose.CAD for .NET を使用すると、3D CAD イメージを PDF に簡単に変換できます。シームレスな PDF エクスポートについては、段階的なチュートリアルに従ってください。
weight: 10
url: /ja/net/3d-image-export/exporting-3d-images-to-pdf/
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# 3D 画像を PDF にエクスポート - Aspose.CAD チュートリアル

## 導入

Aspose.CAD for .NET を使用して 3D 画像を PDF にシームレスにエクスポートしたいと考えていますか?このステップバイステップのチュートリアルでは、Aspose.CAD の機能を利用して 3D 画像を PDF 形式に簡単に変換できるように、プロセスをガイドします。

## 前提条件

チュートリアルに入る前に、次の前提条件が満たされていることを確認してください。

-  Aspose.CAD for .NET: .NET 用の Aspose.CAD ライブラリがインストールされていることを確認します。そうでない場合は、からダウンロードできます。[Aspose.CAD for .NET ダウンロード ページ](https://releases.aspose.com/cad/net/).

- ドキュメント ディレクトリ: CAD ファイルを保存するディレクトリを設定し、そのパスを書き留めます。

## 名前空間のインポート

.NET プロジェクトで、Aspose.CAD を操作するために必要な名前空間をインポートします。コード ファイルの先頭に次の行を追加します。

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

まず、PDF にエクスポートする CAD イメージをロードします。使用`Load`Aspose.CAD ライブラリのメソッド。交換する`"conic_pyramid.dxf"`CAD ファイルへのパスを含めます。

```csharp
string MyDir = "Your Document Directory";
string sourceFilePath = MyDir + "conic_pyramid.dxf";
using (Image cadImage = Image.Load(sourceFilePath))
{
    //CAD イメージをロードするためのコードはここにあります
}
```

## ステップ 2: ラスタライズ オプションを構成する

CAD イメージのラスタライズ オプションを構成します。ページ幅、ページ高さ、レイアウトなどのパラメータを設定します。に関連する行のコメントを解除します`TypeOfEntities`エンティティが 3D の場合。

```csharp
CadRasterizationOptions rasterizationOptions = new CadRasterizationOptions();
rasterizationOptions.PageWidth = 500;
rasterizationOptions.PageHeight = 500;
// rasterizationOptions.TypeOfEntities = TypeOfEntities.Entities3D;

rasterizationOptions.Layouts = new string[] { "Model" };
```

## ステップ 3: PDF オプションを設定する

PDF オプションを作成し、ラスタライズ オプションに関連付けます。

```csharp
PdfOptions pdfOptions = new PdfOptions();
pdfOptions.VectorRasterizationOptions = rasterizationOptions;
```

## ステップ 4: PDF として保存

構成されたオプションを使用して、CAD イメージを PDF ファイルとして保存します。 PDFファイルの出力パスを指定します。

```csharp
MyDir = MyDir + "Export3DImagestoPDF_out.pdf";
cadImage.Save(MyDir, pdfOptions);
```

## 結論

おめでとう！ Aspose.CAD for .NET を使用して 3D 画像を PDF にエクスポートできました。この簡単なチュートリアルにより、CAD ファイルをよりアクセスしやすい形式に簡単に変換できます。

## よくある質問

### Q1: Aspose.CAD はすべての CAD ファイル形式と互換性がありますか?

A1: はい、Aspose.CAD は幅広い CAD 形式をサポートしており、さまざまなファイル タイプを柔軟に処理できます。

### Q2: PDF にエクスポートするときにページの寸法をカスタマイズできますか?

A2: もちろんです。このチュートリアルでは、要件に応じてページの幅と高さを構成する方法を示します。

### Q3: Aspose.CAD の一時ライセンスは利用できますか?

 A3: はい、次のサイトにアクセスして、Aspose.CAD の一時ライセンスを取得できます。[仮免許](https://purchase.aspose.com/temporary-license/).

### Q4: 追加のサポートやコミュニティのディスカッションはどこで見つけられますか?

 A4: へ向かいます。[Aspose.CAD フォーラム](https://forum.aspose.com/c/cad/19)サポートとコミュニティとの関わりのために。

### Q5: Aspose.CAD の無料試用版はありますか?

 A5: はい、Aspose.CAD の機能を調べるには、[無料トライアル](https://releases.aspose.com/).
{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}
