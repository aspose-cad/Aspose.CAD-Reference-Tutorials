---
title: C# での座標を含む DWG から PDF への変換 - Aspose.CAD チュートリアル
linktitle: C# で座標を含む DWG を PDF に変換する
second_title: Aspose.CAD .NET - CAD および BIM ファイル形式
description: Aspose.CAD を使用して、C# で特定の座標を含む DWG を PDF に変換する方法を学習します。正確かつ効率的に CAD ファイルを変換するには、ステップバイステップのガイドに従ってください。
type: docs
weight: 11
url: /ja/net/conversion-and-export/converting-dwg-to-pdf-with-coordinates/
---
## 導入

Aspose.CAD for .NET を使用して、指定された座標を持つ DWG ファイルを PDF に変換するためのこの包括的なチュートリアルへようこそ。 Aspose.CAD は、開発者が .NET アプリケーションで CAD ファイル形式をシームレスに操作できるようにする強力なライブラリです。このチュートリアルでは、精度を高めるために特定の座標を指定しながら、DWG ファイルを PDF に変換するプロセスを説明します。

## 前提条件

始める前に、次の前提条件を満たしていることを確認してください。

- Aspose.CAD ライブラリ: .NET 用の Aspose.CAD ライブラリをダウンロードしてインストールします。図書館を見つけることができます[ここ](https://releases.aspose.com/cad/net/).

- 開発環境: Visual Studio またはその他の優先 IDE を含む、互換性のある開発環境がセットアップされていることを確認します。

- DWG ファイル: 変換できる DWG ファイルを用意します。提供されているサンプル ファイルまたはカスタム DWG ファイルを使用できます。

## 名前空間のインポート

C# プロジェクトで、必要な名前空間をインポートします。

```csharp
using System;
using System.Collections.Generic;
using System.Linq;
using System.Text;
using System.Threading.Tasks;
using Aspose.CAD;
using Aspose.CAD.FileFormats.Cad;
using Aspose.CAD.FileFormats.Cad.CadParameters;
using Aspose.CAD.FileFormats.Cad.CadTables;
using Aspose.CAD.ImageOptions;
```

理解を深めるために、コードをステップバイステップのガイドに分解してみましょう。

## ステップ 1: ドキュメント ディレクトリを定義する

```csharp
string MyDir = "Your Document Directory";
```

## ステップ 2: ソース DWG ファイルのパスを設定する

```csharp
string sourceFilePath = MyDir + "visualization_-_conference_room.dwg";
```

## ステップ 3: DWG ファイルをロードし、ラスタライズ オプションを構成する

```csharp
using (CadImage cadImage = (CadImage)Image.Load(sourceFilePath))
{
    CadRasterizationOptions rasterizationOptions = new CadRasterizationOptions();
    rasterizationOptions.Layouts = new string[] { "Model" };
    rasterizationOptions.NoScaling = true;
```

## ステップ 4: 座標とビューポートを定義する

```csharp
    Point topLeft = new Point(500, 1000);
    double width = 3108;
    double height = 2489;

    CadVportTableObject newView = new CadVportTableObject();
    newView.Name = new CadStringParameter();
    newView.Name.Init("*Active");
    newView.CenterPoint.X = topLeft.X + width / 2f;
    newView.CenterPoint.Y = topLeft.Y - height / 2f;
    newView.ViewHeight.Value = height;
    newView.ViewAspectRatio.Value = width / height;
```

## ステップ 5: ビューポート設定を適用する

```csharp
    for (int i = 0; i < cadImage.ViewPorts.Count; i++)
    {
        CadVportTableObject currentView = (CadVportTableObject)(cadImage.ViewPorts[i]);
        if (cadImage.ViewPorts.Count == 1 || string.Equals(currentView.Name.Value.ToLowerInvariant(), "*active"))
        {
            cadImage.ViewPorts[i] = newView;
            break;
        }
    }
```

## ステップ 6: PDF オプションを構成してエクスポートする

```csharp
    Aspose.CAD.ImageOptions.PdfOptions pdfOptions = new Aspose.CAD.ImageOptions.PdfOptions();
    pdfOptions.VectorRasterizationOptions = rasterizationOptions;

    MyDir = MyDir + "ConvertDWGToPDFBySupplyingCoordinates_out.pdf";
    cadImage.Save(MyDir, pdfOptions);
}
```

## ステップ 7: 成功メッセージを表示する

```csharp
Console.WriteLine("\nThe DWG file exported successfully to PDF.\nFile saved at " + MyDir);
```

## 結論

おめでとう！ Aspose.CAD for .NET を使用して、指定した座標を持つ DWG ファイルを PDF に変換することができました。このチュートリアルでは重要な手順を説明し、開発者に明確なガイドを提供しました。

## よくある質問

### Q1: Aspose.CAD を他の CAD ファイル形式で使用できますか?

A1: はい、Aspose.CAD は、DWG、DXF、DWF などを含むさまざまな CAD 形式をサポートしています。

### Q2: 変換プロセス中のエラーはどのように処理すればよいですか?

A2: try-catch ブロックを使用してエラー処理メカニズムを実装し、例外をキャプチャして管理します。

### Q3: Aspose.CAD は Windows 環境と Linux 環境の両方に適していますか?

A3: はい、Aspose.CAD は Windows と Linux の両方のプラットフォームと互換性があります。

### Q4: PDF 出力をさらにカスタマイズできますか?

A4：確かに！ Aspose.CAD が提供する広範なオプションを調べて、PDF 出力を特定の要件に合わせて調整します。

### Q5: 追加のサポートやコミュニティのディスカッションはどこで見つけられますか?

A5: にアクセスしてください。[Aspose.CAD フォーラム](https://forum.aspose.com/c/cad/19)コミュニティのサポートとディスカッションのために。