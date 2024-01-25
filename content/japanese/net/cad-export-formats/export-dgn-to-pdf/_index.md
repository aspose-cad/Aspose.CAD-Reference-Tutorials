---
title: Aspose.CAD for .NET で DGN を PDF にエクスポート
linktitle: DGN を PDF にエクスポート
second_title: Aspose.CAD .NET - CAD および BIM ファイル形式
description: Aspose.CAD for .NET を使用して、DGN ファイルを PDF に簡単にエクスポートする方法を学びます。シームレスな CAD ファイル操作のためのステップバイステップのガイド。
type: docs
weight: 12
url: /ja/net/cad-export-formats/export-dgn-to-pdf/
---
## 導入

.NET 開発の世界では、Aspose.CAD は CAD ファイルの操作と変換を容易にする強力なライブラリです。開発者がよく遭遇する一般的なタスクの 1 つは、DGN ファイルを PDF 形式にエクスポートすることです。このチュートリアルでは、Aspose.CAD for .NET を使用してプロセスを段階的に説明します。

## 前提条件

チュートリアルに入る前に、次のものが整っていることを確認してください。

- C# と .NET Framework に関する実践的な知識。
-  Aspose.CAD for .NET ライブラリがインストールされています。ダウンロードできます[ここ](https://releases.aspose.com/cad/net/).
- このチュートリアルのサンプル DGN ファイル (たとえば、「Nikon_D90_Camera.dgn」)。

## 名前空間のインポート

C# プロジェクトで、必要な名前空間をインポートすることから始めます。

```csharp
using System;
using System.Collections.Generic;
using System.Linq;
using System.Text;
using System.Threading.Tasks;
using Aspose.CAD;
```

## ステップ 1: DGN ファイルをロードする

```csharp
string MyDir = "Your Document Directory";
string sourceFilePath = MyDir + "Nikon_D90_Camera.dgn";

using (DgnImage cadImage = (DgnImage)Image.Load(sourceFilePath))
{
    //コードはここにあります...
}
```

## ステップ 2: ラスタライズ オプションを構成する

```csharp
CadRasterizationOptions rasterizationOptions = new CadRasterizationOptions();
rasterizationOptions.PageWidth = 600;
rasterizationOptions.PageHeight = 300;
rasterizationOptions.NoScaling = true;
rasterizationOptions.AutomaticLayoutsScaling = false;
```

## ステップ 3: PDF オプションの作成

```csharp
PdfOptions pdfOptions = new PdfOptions();
pdfOptions.VectorRasterizationOptions = rasterizationOptions;
```

## ステップ 4: PDF として保存

```csharp
cadImage.Save(MyDir + "ExportDGNToPdf_out.pdf", pdfOptions);
```

## 結論

おめでとう！ Aspose.CAD for .NET を使用して DGN ファイルを PDF にエクスポートできました。このチュートリアルでは、DGN ファイルのロードからラスタライズ オプションの構成、出力の PDF としての保存まで、重要な手順を説明しました。

## よくある質問

### Q1: CAD の予備知識がなくても、Aspose.CAD for .NET を使用できますか?

A1: もちろんです！ Aspose.CAD は複雑な CAD タスクを簡素化し、さまざまな背景を持つ開発者がアクセスできるようにします。

### Q2: Aspose.CAD のその他の例やドキュメントはどこで入手できますか?

 A2: を探索してください。[ドキュメンテーション](https://reference.aspose.com/cad/net/)包括的なガイドと例を参照してください。

### Q3: Aspose.CAD の無料トライアルはありますか?

A3: はい、無料トライアルを利用できます。[ここ](https://releases.aspose.com/).

### Q4: Aspose.CAD の一時ライセンスを取得するにはどうすればよいですか?

 A4: 一時ライセンスを取得する[ここ](https://purchase.aspose.com/temporary-license/).

### Q5: サポートが必要ですか、それとも質問がありますか?

A5: にアクセスしてください。[Aspose.CAD フォーラム](https://forum.aspose.com/c/cad/19)コミュニティサポートのために。