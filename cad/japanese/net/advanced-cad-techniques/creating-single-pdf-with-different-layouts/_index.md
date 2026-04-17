---
date: 2026-03-02
description: Aspise.CAD for .NET を使用して、異なるレイアウトを持つ単一の PDF を作成する方法を学びましょう – CAD を PDF
  に変換し、DWG を PDF にエクスポートし、CAD を効率的に PDF として保存します。
linktitle: Creating Single PDF with Different Layouts
second_title: Aspose.CAD .NET - CAD and BIM File Format
title: 異なるレイアウトで単一のPDFを作成する方法 - Aspose.CAD ガイド
url: /ja/net/advanced-cad-techniques/creating-single-pdf-with-different-layouts/
weight: 13
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# 異なるレイアウトを持つ単一 PDF の作成方法 - Aspose.CAD ガイド

## はじめに

**単一 PDF** ファイルに複数の CAD レイアウトを含める必要がある場合、ここが適切な場所です。このチュートリアルでは、CAD 図面を 1 つの PDF ドキュメントに変換し、複数のレイアウトを処理するために必要な正確な手順を順を追って説明します。Aspose.CAD for .NET を使用すれば、**CAD から PDF への変換**、**DWG を PDF にエクスポート**、**CAD を PDF として保存** を数行の C# コードで簡単に実行できます。

## クイック回答
- **このチュートリアルで扱う内容は？** 複数の CAD レイアウトを含む 1 つの PDF を生成する方法。  
- **使用するライブラリは？** Aspose.CAD for .NET。  
- **ライセンスは必要ですか？** 評価用の無料トライアルで動作しますが、本番環境ではライセンスが必要です。  
- **対応 CAD フォーマットは？** DWG、DXF、DGN など多数。  
- **実装にかかる目安の時間は？** 基本的な変換で約 10〜15 分。

## CAD の文脈で「単一 PDF を作成する」とは？

単一 PDF を作成するとは、複数のレイアウト定義（ペーパー スペース）を含む 1 つの CAD ソース ファイルを読み取り、各レイアウトを別々のページとして 1 つの PDF ドキュメントに統合することです。これは、建築図面やエンジニアリング スキーマ、クライアントが統合された PDF パッケージを期待するシナリオで特に有用です。

## なぜ Aspose.CAD を使用するのか？

- **外部依存なし** – 純粋な .NET、AutoCAD のインストールは不要。  
- **ラスター化のフルコントロール** – ページサイズ、DPI、カスタムレイアウト寸法を設定可能。  
- **高忠実度レンダリング** – ベクターデータは可能な限り保持され、鮮明な出力が得られます。  
- **バッチ処理対応** – 同じコードをループ内に配置すれば、多数の図面を自動で処理可能。

## 前提条件

- Aspose.CAD for .NET: Aspose.CAD for .NET がインストールされていることを確認してください。ダウンロードは [here](https://releases.aspose.com/cad/net/) から。  
- 開発環境: .NET 開発環境をセットアップし、C# プログラミングの基本を理解していること。

## 名前空間のインポート

C# プロジェクトで Aspose.CAD for .NET の機能を利用するために、必要な名前空間をインクルードします。

```csharp
using Aspose.CAD.FileFormats.Cad;
using Aspose.CAD.ImageOptions;
using System;
using System.Collections.Generic;
using System.Linq;
using System.Text;
```

## 手順別ガイド

### 手順 1: CAD 画像のロード

まず、ソース CAD ファイル（例: DWG 図面）をロードします。`CadImage` クラスを使用すると、ファイル内のすべてのレイアウトにアクセスできます。

```csharp
// The path to the documents directory.
string MyDir = "Your Document Directory";

using (CadImage cadImage = (CadImage)Image.Load(MyDir + "City skyway map.dwg"))
{
    // Your code for Step 1 goes here
}
```

### 手順 2: ラスター化オプションのカスタマイズ

各レイアウトのラスター化方法を定義します。デフォルトのページサイズを設定し、`LayoutPageSizes` を使用して特定のレイアウトに対して上書きできます。

```csharp
CadRasterizationOptions rasterizationOptions = new CadRasterizationOptions();
rasterizationOptions.PageWidth = 1000;
rasterizationOptions.PageHeight = 1000;

// Custom sizes for several layouts
rasterizationOptions.LayoutPageSizes.Add("ANSI C Plot", new SizeF(500, 1000));
rasterizationOptions.LayoutPageSizes.Add("8.5 x 11 Plot", new SizeF(1000, 100));
```

> **プロのコツ:** 詳細な図面に高解像度出力が必要な場合は、DPI (`rasterizationOptions.Resolution`) を調整してください。

### 手順 3: PDF オプションの定義

ラスター化設定を `PdfOptions` オブジェクトでラップします。これにより、Aspose.CAD が CAD データを直接 PDF ストリームにレンダリングします。

```csharp
PdfOptions pdfOptions = new PdfOptions() { VectorRasterizationOptions = rasterizationOptions };
```

### 手順 4: PDF として保存

最後に、`CadImage` インスタンスの `Save` を呼び出し、対象 PDF ファイル名と作成したオプションを渡します。ライブラリは、設定した各レイアウトに対応するページを持つ単一の PDF を生成します。

```csharp
cadImage.Save(MyDir + "singlePDF_out.pdf", pdfOptions);
```

この呼び出しの後、"ANSI C Plot" と "8.5 x 11 Plot" のレイアウトが 1 つの統合ドキュメントに結合された PDF が得られます。

## よくある落とし穴とトラブルシューティング

| Issue | Reason | Fix |
|-------|--------|-----|
| PDF にレイアウトが欠落 | `LayoutPageSizes` がレイアウト名に対して定義されていない | CAD ファイル内の正確なレイアウト名（大文字小文字を区別）を確認 |
| 出力が低品質 | デフォルト DPI が 96 | 保存前に `rasterizationOptions.Resolution = 300`（またはそれ以上）を設定 |
| ファイルが見つからない | `MyDir` パスが間違っている | `Path.Combine` を使用してプラットフォームに依存しないパスを構築 |

## FAQ（よくある質問）

### Q1: Aspose.CAD for .NET は他の CAD フォーマットでも使用できますか？

A1: はい、Aspose.CAD for .NET は DWG、DXF、DGN などさまざまな CAD フォーマットをサポートしています。

### Q2: 無料トライアルはありますか？

A2: はい、無料トライアルは [here](https://releases.aspose.com/) から利用できます。

### Q3: Aspose.CAD for .NET のサポートはどこで受けられますか？

A3: コミュニティサポートは [Aspose.CAD forum](https://forum.aspose.com/c/cad/19) をご覧ください。

### Q4: 詳細なドキュメントはどこにありますか？

A4: ドキュメントは [here](https://reference.aspose.com/cad/net/) にあります。

### Q5: Aspose.CAD for .NET のライセンスは購入できますか？

A5: はい、ライセンスは [here](https://purchase.aspose.com/buy) から購入可能です。

**追加の Q&A**

**Q:** カスタムページサイズで **DWG を PDF にエクスポート** するには？  
**A:** 手順 2で示したように `CadRasterizationOptions.LayoutPageSizes` を使用して、各 DWG レイアウトを目的の PDF ページ寸法にマッピングします。

**Q:** ベクターデータをラスター化せずに **CAD を PDF として保存** できますか？  
**A:** Aspose.CAD は PDF 作成時に常にラスター化しますが、DPI を上げることで視覚的な忠実度を高めることができます。

## 結論

本ガイドでは、複数レイアウトを含む CAD 図面から **単一 PDF** ファイルを作成する方法を、Aspose.CAD for .NET を使用して実演しました。これで **CAD から PDF への変換**、**DWG を PDF にエクスポート**、**CAD を PDF として保存** を単一の自動化ワークフローで実行するための基礎が整いました。プロジェクトの品質要件に合わせてラスター化設定を調整し、必要に応じてバッチ処理パイプラインに組み込んでください。

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}

---

**最終更新日:** 2026-03-02  
**テスト環境:** Aspose.CAD for .NET 24.11  
**作者:** Aspose  

---