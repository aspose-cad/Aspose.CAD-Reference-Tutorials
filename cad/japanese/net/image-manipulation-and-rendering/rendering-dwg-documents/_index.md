---
title: C# での DWG ドキュメントのレンダリング - Aspose.CAD ガイド
linktitle: C# での DWG ドキュメントのレンダリング
second_title: Aspose.CAD .NET - CAD および BIM ファイル形式
description: Aspose.CAD を使用して C# で DWG ドキュメントをレンダリングする方法を学びます。このステップバイステップのガイドでは、コード例を使用してインポート、構成、保存について説明します。
weight: 17
url: /ja/net/image-manipulation-and-rendering/rendering-dwg-documents/
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# C# での DWG ドキュメントのレンダリング - Aspose.CAD ガイド

## 導入

Aspose.CAD を使用して C# で DWG ドキュメントをレンダリングするための包括的なガイドへようこそ。経験豊富な開発者でも、.NET を始めたばかりでも、このチュートリアルでは、Aspose.CAD を活用して DWG ファイルを効率的にレンダリングするプロセスを説明します。 Aspose.CAD は、CAD ファイル形式を操作するための堅牢な機能を提供する強力な API であり、DWG ファイルを扱う開発者にとって頼りになる選択肢となっています。

## 前提条件

チュートリアルに進む前に、次の前提条件を満たしていることを確認してください。

- C# プログラミング言語の基本的な知識。
- Visual Studio がマシンにインストールされていること。
-  Aspose.CAD ライブラリがプロジェクトに統合されました。からダウンロードできます[ここ](https://releases.aspose.com/cad/net/).
- 例に従うサンプル DWG ファイル (「Bottom_plate.dwg」など)。

## 名前空間のインポート

まず、C# コードの先頭で必要な名前空間をインポートしてください。

```csharp
using System;
using System.Collections.Generic;
using System.Linq;
using System.Text;
using System.Threading.Tasks;
using Aspose.CAD;
using Aspose.CAD.ImageOptions;
using Aspose.CAD.FileFormats.Cad.CadTables;
using Aspose.CAD.FileFormats.Cad;
```

ここで、提供された例を複数のステップに分解してみましょう。

## ステップ 1: DWG ファイルをロードする

```csharp
string MyDir = "Your Document Directory";
string sourceFilePath = MyDir + "Bottom_plate.dwg";
using (CadImage cadImage = (CadImage)Image.Load(sourceFilePath))
{
    // DWG ファイルをロードするためのコードはここに記述されます。
}
```

## ステップ 2: ラスタライズ オプションを構成する

```csharp
CadRasterizationOptions rasterizationOptions = new CadRasterizationOptions();
rasterizationOptions.Layouts = new string[] { "Model" };
rasterizationOptions.NoScaling = true;
//追加のラスタライズ構成をここに追加できます。
```

## ステップ 3: 描画する領域を定義する

```csharp
Point topLeft = new Point(6156, 7053);
double width = 3108;
double height = 2489;
```

## ステップ 4: 新しいビューポートを作成する

```csharp
CadVportTableObject newView = new CadVportTableObject();
newView.Name.Value = "*Active";
newView.CenterPoint.X = topLeft.X + width / 2f;
newView.CenterPoint.Y = topLeft.Y - height / 2f;
newView.ViewHeight.Value = height;
newView.ViewAspectRatio.Value = width / height;
```

## ステップ 5: アクティブなビューポートを置き換える

```csharp
for (int i = 0; i < cadImage.ViewPorts.Count; i++)
{
    CadVportTableObject currentView = (CadVportTableObject)(cadImage.ViewPorts[i]);
    if ((currentView.Name.Value == null && cadImage.ViewPorts.Count == 1) ||
    string.Equals(currentView.Name.Value.ToLowerInvariant(), "*active"))
    {
        cadImage.ViewPorts[i] = newView;
        break;
    }
}
```

## ステップ 6: PDF オプションを構成する

```csharp
PdfOptions pdfOptions = new PdfOptions();
pdfOptions.VectorRasterizationOptions = rasterizationOptions;
```

## ステップ 7: レンダリングされた DWG を PDF として保存する

```csharp
cadImage.Save(MyDir, pdfOptions);
```

## 結論

おめでとう！ C# の Aspose.CAD を使用して、DWG ドキュメントを PDF にレンダリングすることに成功しました。自由にさらに多くの機能を探索し、特定の要件に基づいてコードをカスタマイズしてください。

## よくある質問

### Q1: Aspose.CAD を他の CAD ファイル形式で使用できますか?

A1: はい、Aspose.CAD は、DWG、DXF、DWF などを含むさまざまな CAD 形式をサポートしています。

### Q2: Aspose.CAD は .NET Core と互換性がありますか?

A2: はい、Aspose.CAD は .NET Framework と .NET Core の両方と互換性があります。

### Q3: DWG ファイル内のさまざまなレイアウトを処理するにはどうすればよいですか?

 A3: 希望のレイアウトを指定できます。`Layouts`の財産`CadRasterizationOptions`.

### Q4: Aspose.CAD を使用する場合、ライセンスに関する考慮事項はありますか?

 A4: ライセンスの詳細については、次のサイトをご覧ください。[ここ](https://purchase.aspose.com/buy).

### Q5: 追加のサポートはどこで入手できますか?

A5: にアクセスしてください。[Aspose.CAD フォーラム](https://forum.aspose.com/c/cad/19)コミュニティのサポートとディスカッションのために。
{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}
