---
date: 2026-03-24
description: Aspose.CAD for .NET を使用して、DGN V7 の 3D 対応で DGN を PDF（および PNG）に変換する方法をステップバイステップで学ぶ。
linktitle: 3D Support for DGN V7
second_title: Aspose.CAD .NET - CAD and BIM File Format
title: Aspose.CAD for .NET を使用して DGN を PDF に変換（3D 対応）
url: /ja/net/cad-features-and-support/3d-support-for-dgn-v7/
weight: 10
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Aspose.CAD for .NET を使用した DGN から PDF への変換（3D 対応）

## Introduction

最新の CAD ワークフローでは、**DGN を PDF に変換**し、3‑D ジオメトリを保持できることが不可欠です。ドキュメントの作成、CAD 以外の関係者への設計共有、プロジェクトのアーカイブなど、Aspose.CAD for .NET を使用すれば、DGN V7 ファイルを高品質な PDF（場合によっては PNG）に確実に変換できます。このチュートリアルでは、3D 対応を有効にし、DGN ファイルから PDF を生成するための正確な手順を解説します。

## Quick Answers
- **このチュートリアルで扱う内容は？** Aspose.CAD for .NET を使用した 3D 対応の有効化と DGN V7 から PDF への変換。  
- **主に生成される形式は？** PDF（オプションで PNG もエクスポート可能）。  
- **ライセンスは必要ですか？** 無料トライアルでテスト可能です。商用利用には製品ライセンスが必要です。  
- **対応している .NET バージョンは？** .NET Framework 4.5 以上、.NET Core 3.1 以上、.NET 5/6 以上。  
- **実装にかかる時間は？** 基本的な変換で約 10‑15 分。

## What is “convert DGN to PDF”?

DGN を PDF に変換するとは、MicroStation DGN ファイルに保存されたベクターデータを、専用の CAD ソフトウェアがなくても任意のデバイスで閲覧できるポータブルドキュメント形式にレンダリングすることです。Aspose.CAD の 3‑D ラスタライズエンジンにより、レイアウト、カラー、奥行き情報が保持され、忠実なビジュアル表現が実現します。

## Why use Aspose.CAD for this conversion?

- **フル 3‑D ラスタライズ** – 奥行きとレイアウト情報を保持。  
- **外部依存なし** – 純粋な .NET ライブラリで、MicroStation は不要。  
- **複数の出力形式** – PDF、PNG、JPEG、TIFF など（二次キーワード *convert dgn to png* も標準でサポート）。  
- **クロスプラットフォーム** – Windows、Linux、macOS で動作。

## Prerequisites

開始する前に、以下を用意してください。

- Aspose.CAD for .NET がインストール済みであること。ダウンロードは [Aspose.CAD for .NET ダウンロードページ](https://releases.aspose.com/cad/net/) から取得できます。  
- 処理対象の有効な DGN V7 ファイル。  
- .NET 開発環境（Visual Studio、VS Code、または CLI）。インストール手順は [.NET ドキュメント](https://docs.microsoft.com/en-us/dotnet/core/install/) にあります。

## Import Namespaces

```csharp
using System;
using System.Collections.Generic;
using System.Linq;
using System.Text;
using System.Threading.Tasks;
using Aspose.CAD;
```

これらの名前空間により、Aspose.CAD のコアクラスと標準 .NET ユーティリティにアクセスできます。

## Step 1: Set up the Environment

ソース DGN ファイルの場所と、出力 PDF を保存する場所を定義します。

```csharp
string MyDir = "Your Document Directory";
string sourceFilePath = MyDir + "Nikon_D90_Camera.dgn";
```

> **Pro tip:** `Path.Combine` を使用して、プラットフォームに依存しないパス構築を行いましょう。

## Step 2: Load the DGN File

`Image.Load` でファイルを読み込み、`DgnImage` インスタンスを作成します。このステップで CAD データのラスタライズ準備が整います。

```csharp
using (DgnImage dgnImage = (DgnImage)Image.Load(sourceFilePath))
{
    // Code snippet continues...
}
```

## Step 3: Configure Export Options

`PdfOptions` と `CadRasterizationOptions` を組み合わせて設定します。ここでページサイズ、背景色、エクスポート対象のレイアウト（ビュー）を制御します。

```csharp
var options = new PdfOptions
{
    VectorRasterizationOptions = new CadRasterizationOptions
    {
        PageWidth = 1500,
        PageHeight = 1500,
        CenterDrawing = true,
        AutomaticLayoutsScaling = true,
        BackgroundColor = Color.Black,
        Layouts = new string[] { "1", "2", "3", "9" } // Export specific views
    }
};
```

**DGN を PNG に変換したい**場合は、`PdfOptions` を `PngOptions` に置き換え、同じラスタライズ設定を使用してください。

## Step 4: Save the Result

最後に、レンダリング結果を指定した場所に書き出します。

```csharp
string outFile = "Your Output Directory"; // Specify the output directory
dgnImage.Save(outFile, options);
```

実行後、元の 3‑D DGN 図面を忠実に再現した PDF ファイル（オプションで PNG に変更した場合は PNG ファイル）が生成されます。

## Common Issues & Tips

- **レイアウトが見つからない場合:** `Layouts` に指定したレイアウト名が DGN ファイル内に存在することを確認してください。存在しない場合は無視されます。  
- **大容量ファイル:** メモリ使用量が高くなるのを防ぐため、`PageWidth`/`PageHeight` を段階的に増やしてください。  
- **色の正確性:** 背景が暗く表示される場合は、`BackgroundColor` が期待通り（例: `Color.White`）に設定されているか確認しましょう。

## Conclusion

これで、Aspose.CAD for .NET を使用したフル 3‑D 対応の **DGN から PDF への変換**手順を習得しました。このワークフローは、自動化パイプライン、デスクトップユーティリティ、Web サービスなどに組み込んで、あらゆるユーザーに CAD ビジュアライゼーションを提供できます。

## FAQ's

### Q1: Can I process multiple DGN files simultaneously using this approach?

A1: Yes, you can modify the code to handle multiple files within a loop or as part of a batch processing system.

### Q2: What other export formats are supported by Aspose.CAD for .NET?

A2: Aspose.CAD for .NET supports various export formats, including PDF, PNG, JPG, and more. Refer to the [documentation](https://reference.aspose.com/cad/net/) for details.

### Q3: Is Aspose.CAD for .NET compatible with the latest .NET Core versions?

A3: Yes, Aspose.CAD for .NET is designed to be compatible with the latest .NET Core versions. Ensure you have the appropriate version installed in your environment.

### Q4: Can I customize the export settings further for my specific requirements?

A4: Absolutely! The provided code offers a starting point. You can explore additional options and configurations in the [Aspose.CAD documentation](https://reference.aspose.com/cad/net/).

### Q5: Where can I seek help or share my experiences with Aspose.CAD for .NET?

A5: Join the Aspose.CAD community on the [forum](https://forum.aspose.com/c/cad/19) to interact with other developers and seek assistance.

---

**Last Updated:** 2026-03-24  
**Tested With:** Aspose.CAD 24.11 for .NET  
**Author:** Aspose  

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}