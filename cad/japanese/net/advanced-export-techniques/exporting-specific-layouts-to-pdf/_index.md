---
date: 2026-03-13
description: Aspose.CAD for .NET を使用して CAD のラスター化オプションを設定し、特定の DWG レイアウトを PDF にエクスポートする方法を学びましょう
  – CAD ファイルから PDF を作成するための決定的ガイド。
linktitle: Exporting Specific Layouts to PDF
second_title: Aspose.CAD .NET - CAD and BIM File Format
title: CAD ラスタライズオプションの設定 – 特定のレイアウトを PDF にエクスポート - Aspose.CAD ガイド
url: /ja/net/advanced-export-techniques/exporting-specific-layouts-to-pdf/
weight: 13
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# 特定のレイアウトをPDFにエクスポート - Aspose.CAD ガイド

## はじめに

このチュートリアルでは、**CAD ラスタリゼーション オプションの設定方法**を学び、DWG ファイルから単一のレイアウトまたは複数のレイアウトを直接 PDF にエクスポートできるようになります。Aspose.CAD for .NET は *dwg to pdf conversion c#* プロセスをシンプルにし、ページサイズ、解像度、レイアウトの選択を完全にコントロールできます。ガイドの最後までに、数行のコードだけで **CAD ファイルから PDF を作成** できるようになります。

## クイック回答
- **「set cad rasterization options」 は何を行いますか？**  
  Aspose.CAD にベクターデータ（レイアウト、レイヤー、線幅）をラスタライズされた PDF ページにどのように描画するかを指示します。  
- **DWG のレイアウトを PDF にエクスポートするメソッドはどれですか？**  
  `Image.Save` を使用し、`CadRasterizationOptions` を含む設定済みの `PdfOptions` を渡します。  
- **複数のレイアウトを同時にエクスポートできますか？**  
  はい。`Layouts` プロパティにレイアウト名の配列を指定します。  
- **本番環境で使用するにはライセンスが必要ですか？**  
  商用ライセンスが必要です。評価用の無料トライアルも利用可能です。  
- **サポートされている .NET バージョンは何ですか？**  
  .NET Framework 4.5 以上、.NET Core 3.1 以上、.NET 5/6 以降をサポートしています。

## 「set cad rasterization options」とは何ですか？

`CadRasterizationOptions` は、CAD エンティティを PDF などのラスタ形式に変換する際のラスタライズ方法を制御するクラスです。ページサイズ、レイアウト選択、背景色などのプロパティを設定することで、**export dwg layout to pdf** 操作のビジュアル結果を決定できます。

## なぜ CAD ラスタリゼーション オプションを設定するのか？

- **Precision（精度）** – 元の CAD 図面に表示されている線幅やスケールを正確に保持します。  
- **Performance（パフォーマンス）** – 必要なレイアウトだけをレンダリングし、ファイルサイズと処理時間を削減します。  
- **Flexibility（柔軟性）** – ページ幅/高さ、DPI、背景を調整してレポート基準に合わせられます。  

## 前提条件

コードに入る前に、以下が揃っていることを確認してください：

- **Aspose.CAD for .NET** がインストールされていること。以下からダウンロードできます [here](https://releases.aspose.com/cad/net/)。  
- .NET 開発環境（Visual Studio、VS Code、またはお好みの IDE）。  
- 少なくとも 1 つのレイアウトを含む DWG ファイル（ここで使用しているサンプルファイルは `visualization_-_conference_room.dwg`）。

## 名前空間のインポート

.NET プロジェクトで、Aspose.CAD に必要な名前空間をインポートします：

```csharp
using System;
using System.Collections.Generic;
using System.Linq;
using System.Text;
using System.Threading.Tasks;
using Aspose.CAD;
```

## ステップバイステップ ガイド

### ステップ 1: DWG ファイルをロード

まず、変換したい元の DWG ファイルを Aspose.CAD に指定します。

```csharp
// The path to the documents directory.
string MyDir = "Your Document Directory";
string sourceFilePath = MyDir + "visualization_-_conference_room.dwg";

using (Image image = Image.Load(sourceFilePath))
{
    // Your code for further steps goes here.
}
```

### ステップ 2: **CadRasterizationOptions** を設定

ここでは、PDF のページサイズと解像度を決定するラスタリゼーション設定を構成します。

```csharp
// Create an instance of CadRasterizationOptions and set its various properties
CadRasterizationOptions rasterizationOptions = new CadRasterizationOptions();
rasterizationOptions.PageWidth = 1600;
rasterizationOptions.PageHeight = 1600;
```

> **Pro tip:** `PageWidth` と `PageHeight` をターゲット PDF レイアウトのサイズに合わせて調整します。値を大きくすると詳細度は上がりますが、ファイルサイズも増加します。

### ステップ 3: レイアウト名を指定

Aspose.CAD にレンダリングするレイアウトを指示します。`"Layout1"` を DWG ファイル内の正確なレイアウト名に置き換えてください。

```csharp
// Specify desired layout name
rasterizationOptions.Layouts = new string[] { "Layout1" };
```

> **Why this matters:** `Layouts` 配列を限定することで、不要なシートのエクスポートを防ぎ、**dwg to pdf conversion c#** の処理を高速化し、生成される PDF をよりクリーンにします。

### ステップ 4: `PdfOptions` を作成

ラスタリゼーション設定を PDF エクスポートオプションにリンクします。

```csharp
// Create an instance of PdfOptions
PdfOptions pdfOptions = new PdfOptions();
// Set the VectorRasterizationOptions property
pdfOptions.VectorRasterizationOptions = rasterizationOptions;
```

### ステップ 5: PDF にエクスポート

最後に、レンダリングされたレイアウトを PDF ファイルとして保存します。

```csharp
MyDir = MyDir + "ExportSpecificLayoutToPDF_out.pdf";
// Export the DWG to PDF
image.Save(MyDir, pdfOptions);
```

### ステップ 6: 成功メッセージを表示

簡単なコンソール出力で操作が成功したことを確認できます。

```csharp
// Display success message
Console.WriteLine("\nThe DWG file with a specific layout exported successfully to PDF.\nFile saved at " + MyDir);
```

## よくある問題と解決策

| 問題 | 原因 | 対策 |
|------|------|------|
| **PDF が生成されません** | `Layouts` 配列が DWG 内のいずれのレイアウト名とも一致していません。 | CAD ビューアでレイアウト名を確認し、`Layouts` プロパティを更新してください。 |
| **空白ページ** | `PageWidth`/`PageHeight` が 0 または極端に小さい値に設定されています。 | 現実的な寸法（例: 1600 × 1600）を使用するか、これらのプロパティを省略して Aspose に自動計算させてください。 |
| **スケーリングが正しくない** | 高解像度出力が必要な場合に DPI が設定されていません。 | エクスポート前に `rasterizationOptions.Resolution = 300;`（または希望の DPI）を設定してください。 |

## よくある質問

**Q: 複数のレイアウトを同時にエクスポートできますか？**  
A: はい。ステップ 3 の `Layouts` 配列に目的のレイアウト名すべてを含めるだけです。例: `new string[] { "Layout1", "Layout2" }`。

**Q: Aspose.CAD は他の CAD ファイル形式にも対応していますか？**  
A: もちろんです。DWG、DXF、DWF、DGN など多数の形式に対応しています。

**Q: ページサイズ以外の PDF 出力設定はどのように調整できますか？**  
A: `CadRasterizationOptions` の `Resolution`、`BackgroundColor`、`DrawType` などの追加プロパティを調べて、結果を細かく調整してください。

**Q: 追加の Aspose.CAD ドキュメントはどこで見つけられますか？**  
A: 詳細な API リファレンスやサンプルは [documentation](https://reference.aspose.com/cad/net/) をご覧ください。

**Q: 無料トライアルは利用できますか？**  
A: はい、無料トライアルは [here](https://releases.aspose.com/) から入手できます。

## 結論

これで、**CAD ラスタリゼーション オプションの設定方法**と、それを使用して Aspose.CAD for .NET で **特定の DWG レイアウトを PDF にエクスポート**する方法を学びました。この手法により、変換プロセスを正確にコントロールでき、任意の C# アプリケーションに CAD から PDF への機能を迅速かつ確実に統合できます。

---

**Last Updated:** 2026-03-13  
**Tested With:** Aspose.CAD 24.11 for .NET  
**Author:** Aspose  

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}