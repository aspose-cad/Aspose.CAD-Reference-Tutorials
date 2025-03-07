---
title: DWG からコンプライアンス PDF への変換 - Aspose.CAD チュートリアル
linktitle: DWG からコンプライアンス PDF への変換
second_title: Aspose.CAD .NET - CAD および BIM ファイル形式
description: Aspose.CAD for .NET を使用して DWG を Compliance PDF に変換します。ステップバイステップのガイダンスについては、チュートリアルに従ってください。
weight: 13
url: /ja/net/conversion-and-export/converting-dwg-to-compliance-pdf/
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# DWG からコンプライアンス PDF への変換 - Aspose.CAD チュートリアル

## 導入

Aspose.CAD for .NET を使用して DWG ファイルをコンプライアンス PDF に変換するためのステップバイステップのチュートリアルへようこそ。 Aspose.CAD は、開発者が CAD ファイル形式を簡単に操作できるようにする強力な .NET API です。このチュートリアルでは、詳細な例と説明を使用して、DWG ファイルをコンプライアンス PDF に変換するプロセスを説明します。

## 前提条件

始める前に、次の前提条件が満たされていることを確認してください。

-  Aspose.CAD for .NET: Aspose.CAD ライブラリが .NET プロジェクトに統合されていることを確認してください。ダウンロードできます[ここ](https://releases.aspose.com/cad/net/).

- 開発環境: 動作する .NET 開発環境がインストールされており、それが正しく構成されていることを確認します。

- サンプル DWG ファイル: コンプライアンス PDF に変換するサンプル DWG ファイルをダウンロードします。

## 名前空間のインポート

.NET プロジェクトで、Aspose.CAD 機能を利用するために必要な名前空間をインポートします。

```csharp
using System;
using System.Collections.Generic;
using System.Linq;
using System.Text;
using System.Threading.Tasks;
using Aspose.CAD;
using Aspose.CAD.ImageOptions;
```

ここで、DWG ファイルをコンプライアンス PDF に変換するプロセスを複数のステップに分けて見てみましょう。

## ステップ 1: DWG ファイルをロードする

```csharp
string MyDir = "Your Document Directory";
string sourceFilePath = MyDir + "Bottom_plate.dwg";

Aspose.CAD.Image cadImage = Aspose.CAD.Image.Load(sourceFilePath);
```

## ステップ 2: ラスタライズ オプションを設定する

のインスタンスを作成します`CadRasterizationOptions`背景色、ページ幅、ページ高さなどのプロパティを設定します。

```csharp
CadRasterizationOptions rasterizationOptions = new CadRasterizationOptions
{
    BackgroundColor = Aspose.CAD.Color.White,
    PageWidth = 1600,
    PageHeight = 1600
};
```

## ステップ 3: PDF オプションの作成

のインスタンスを作成します`PdfOptions`ベクトル ラスタライズ オプションを設定します。

```csharp
PdfOptions pdfOptions = new PdfOptions
{
    VectorRasterizationOptions = rasterizationOptions,
    CorePdfOptions = new PdfDocumentOptions { Compliance = PdfCompliance.PdfA1a }
};
```

## ステップ 4: PDF として保存 (A1a 準拠)

CAD イメージを A1a 準拠のコンプライアンス PDF として保存します。

```csharp
cadImage.Save(MyDir + "PDFA1_A.pdf", pdfOptions);
```

## ステップ 5: PDF として保存 (A1b 準拠)

コンプライアンス タイプを A1b に変更し、CAD イメージをコンプライアンス PDF として保存します。

```csharp
pdfOptions.CorePdfOptions.Compliance = PdfCompliance.PdfA1b;
cadImage.Save(MyDir + "PDFA1_B.pdf", pdfOptions);
```

## 結論

おめでとう！ Aspose.CAD for .NET を使用して、DWG ファイルを Compliance PDF に正常に変換しました。このチュートリアルは、CAD 変換機能をアプリケーションに統合しようとしている開発者向けの包括的なガイドを提供します。

## よくある質問

### Q1: Aspose.CAD を使用して、他の CAD 形式をコンプライアンス PDF に変換できますか?

A1: はい、Aspose.CAD はさまざまな CAD 形式をサポートしており、コンプライアンス PDF への変換が可能です。

### Q2: Aspose.CAD は .NET Core と互換性がありますか?

A2: はい、Aspose.CAD は .NET Framework と .NET Core の両方と互換性があります。

### Q3: Aspose.CAD のライセンス オプションはありますか?

 A3: はい、ライセンス オプションを検討できます。[ここ](https://purchase.aspose.com/buy).

### Q4: 無料トライアルはありますか?

 A4: はい、無料トライアルが可能です[ここ](https://releases.aspose.com/).

### Q5: Aspose.CAD のサポートはどこで受けられますか?

A5: にアクセスしてください。[Aspose.CAD フォーラム](https://forum.aspose.com/c/cad/19)サポート関連の質問については、
{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}
