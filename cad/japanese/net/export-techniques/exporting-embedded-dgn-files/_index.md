---
title: 埋め込み DGN ファイルのエクスポート - Aspose.CAD チュートリアル
linktitle: 埋め込みDGNファイルのエクスポート
second_title: Aspose.CAD .NET - CAD および BIM ファイル形式
description: Aspose.CAD for .NET の機能を試してください。このステップバイステップのチュートリアルで、埋め込まれた DGN ファイルを PDF に簡単にエクスポートする方法を学びましょう。
type: docs
weight: 14
url: /ja/net/export-techniques/exporting-embedded-dgn-files/
---
## 導入

ソフトウェア開発のダイナミックな世界では、Aspose.CAD for .NET はコンピュータ支援設計 (CAD) ファイルを処理するための強力なツールとして際立っています。このチュートリアルでは、Aspose.CAD for .NET を使用して埋め込み DGN ファイルをエクスポートするプロセスについて説明します。経験豊富な開発者であっても、好奇心旺盛な初心者であっても、このステップバイステップのガイドは、Aspose.CAD の機能を効果的に活用するのに役立ちます。

## 前提条件

チュートリアルに入る前に、次の前提条件が満たされていることを確認してください。

1.  .NET 用 Aspose.CAD: からライブラリをダウンロードしてインストールします。[Aspose.CAD for .NET](https://releases.aspose.com/cad/net/).

2. 開発環境: Visual Studio またはその他の優先 IDE を使用して .NET 開発環境をセットアップします。

3. サンプル DXF ファイル: このチュートリアルでは、「conic_pyramid.dxf」ファイルを使用します。指定したドキュメント ディレクトリにそれが存在することを確認してください。

## 名前空間のインポート

C# コードで、必要な名前空間を必ずインポートしてください。

```csharp
using System;
using System.Collections.Generic;
using System.Linq;
using System.Text;
using System.Threading.Tasks;
using Aspose.CAD;
using Aspose.CAD.FileFormats.Cad;
using Aspose.CAD.ImageOptions;
```

## ステップ 1: DXF ファイルをロードする

```csharp
string MyDir = "Your Document Directory";
string sourceFilePath = MyDir + "conic_pyramid.dxf";
using (CadImage cadImage = (CadImage)Image.Load(sourceFilePath))
{
    //さらなるステップのコードはここにあります
}
```

## ステップ 2: ラスタライズ オプションを設定する

```csharp
CadRasterizationOptions rasterizationOptions = new CadRasterizationOptions();
rasterizationOptions.Layouts = new[] { "Model" };
```

## ステップ 3: PDF オプションを設定する

```csharp
PdfOptions pdfOptions = new PdfOptions();
pdfOptions.VectorRasterizationOptions = rasterizationOptions;
```

## ステップ 4: PDF として保存

```csharp
cadImage.Save(MyDir + "conic_pyramid.pdf", pdfOptions);
```

## ステップ 5: 成功メッセージを表示する

```csharp
Console.WriteLine("\nThe DXF drawing exported successfully to PDF.\nFile saved at " + MyDir);
```

## 結論

おめでとう！ Aspose.CAD for .NET を使用して、埋め込み DGN ファイルを PDF にエクスポートすることができました。このチュートリアルでは重要な手順を説明し、Aspose.CAD が提供するより高度な機能を探索するための基礎を提供します。

## よくある質問

### Q1: Aspose.CAD for .NET を他のプログラミング言語で使用できますか?

A1: Aspose.CAD は主に .NET をサポートしますが、Aspose は Java や Python などのさまざまな言語のライブラリを提供します。

### Q2: Aspose.CAD for .NET の無料トライアルはありますか?

 A2: はい、以下から無料トライアルを利用できます。[ここ](https://releases.aspose.com/).

### Q3: Aspose.CAD for .NET の包括的なドキュメントはどこで見つけられますか?

 A3: ドキュメントを参照してください。[ここ](https://reference.aspose.com/cad/net/).

### Q4: Aspose.CAD for .NET の一時ライセンスを取得するにはどうすればよいですか?

 A4: 仮免許を取得する[ここ](https://purchase.aspose.com/temporary-license/).

### Q5: サポートが必要ですか、それともコミュニティと関わりたいですか?

A5: にアクセスしてください。[Aspose.CAD フォーラム](https://forum.aspose.com/c/cad/19)サポートとディスカッションのため。