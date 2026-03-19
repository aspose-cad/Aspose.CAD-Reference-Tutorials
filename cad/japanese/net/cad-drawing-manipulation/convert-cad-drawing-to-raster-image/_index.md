---
date: 2026-03-19
description: .NETでAspose.CADを使用してCADをPNGに変換する方法を学び、CADを効率的にPNGとして保存し、ラスタ画像のワークフローを効率化しましょう。
linktitle: Convert CAD Drawing to Raster Image
second_title: Aspose.CAD .NET - CAD and BIM File Format
title: Aspose.CAD for .NET で CAD を PNG に変換
url: /ja/net/cad-drawing-manipulation/convert-cad-drawing-to-raster-image/
weight: 11
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Aspose.CAD for .NET で CAD を PNG に変換する

## はじめに

現代の CAD 中心のアプリケーションでは、**CAD を PNG に変換する**ことは一般的な要件です。サムネイルの生成、ウェブページへの図面埋め込み、またはデザインをラスタ画像としてアーカイブする場合などに必要です。このチュートリアルでは、Aspose.CAD for .NET ライブラリを使用して CAD 図面（DXF、DWG など）を高品質な PNG ファイルに変換する手順をすべて解説します。最後まで読むと、**CAD を PNG として保存**でき、ラスタライズ設定を完全にコントロールできるため、ワークフローがより高速かつ信頼性の高いものになります。

## クイック回答
- **CAD を PNG に変換するのに最適なライブラリは何ですか？** Aspose.CAD for .NET.  
- **PNG にエクスポートできるファイル形式は何ですか？** DWG, DXF, DGN and other supported CAD formats.  
- **本番環境で使用するにはライセンスが必要ですか？** Yes, a commercial license is required; a free trial is available.  
- **画像サイズや品質をカスタマイズできますか？** Absolutely—rasterization options let you set page width, height, background color, and more.  
- **.NET Core / .NET 6 と互換性がありますか？** Yes, the same API works across .NET Framework, .NET Core, and .NET 5/6.

## 「CAD を PNG に変換する」とは何ですか？

CAD を PNG に変換するとは、ベクターベースの CAD 図面をピクセルベースの画像形式（PNG）にラスタライズすることを意味します。このプロセスは視覚的な忠実度を保ちつつ、ブラウザやモバイルアプリ、CAD 形式をネイティブにサポートしない環境でも簡単に表示できるようにします。

## なぜ Aspose.CAD を使って CAD を PNG に変換するのか？

- **外部依存なし** – 純粋な .NET で、ネイティブ CAD エンジンは不要です。  
- **完全なフォーマットサポート** – DWG、DXF、DGN などを処理します。  
- **細かいラスタライズ制御** – ページサイズ、解像度、背景、線幅など。  
- **高性能** – サーバー側のバッチ処理に最適化されています。

## 前提条件

開始する前に、以下が揃っていることを確認してください：

1. **Aspose.CAD for .NET** – [ダウンロードページ](https://releases.aspose.com/cad/net/)からダウンロードしてください。  
2. .NET 対応の IDE（Visual Studio、Rider、または VS Code）で、.NET Framework 4.6 以上または .NET Core 3.1 以上を対象としたプロジェクトを用意してください。  

## 名前空間のインポート

.NET プロジェクトで、Aspose.CAD の機能にアクセスするために必要な名前空間をインポートします。コードファイルの先頭に以下を追加してください：

```csharp
using System;
using System.Collections.Generic;
using System.Linq;
using System.Text;
using System.Threading.Tasks;
using Aspose.CAD;
```

## ステップバイステップガイド

### ステップ 1: ファイルパスの定義
ソースの CAD ファイルと出力先の PNG パスを設定します。プレースホルダーを実際のディレクトリに置き換えてください。

```csharp
// The path to the documents directory.
string MyDir = "Your Document Directory";
string sourceFilePath = MyDir + "conic_pyramid.dxf";
```

### ステップ 2: CAD 図面の読み込み
`Aspose.CAD.Image.Load` を使用して CAD ファイルを開きます。これにより、図面のメモリ内表現が作成され、ラスタライズできるようになります。

```csharp
using (Aspose.CAD.Image image = Aspose.CAD.Image.Load(sourceFilePath))
{
```

### ステップ 3: ラスタライズオプションの設定  
ベクターデータをピクセルに変換する方法を定義します。ここでは 1200 × 1200 ピクセルのキャンバスを設定していますが、`PageWidth` と `PageHeight` を調整してニーズに合わせることができます（例: 特定の DPI で **convert dwg to png** する場合など）。

```csharp
// Create an instance of CadRasterizationOptions
Aspose.CAD.ImageOptions.CadRasterizationOptions rasterizationOptions = new Aspose.CAD.ImageOptions.CadRasterizationOptions();
// Set page width & height
rasterizationOptions.PageWidth = 1200;
rasterizationOptions.PageHeight = 1200;
```

> **Pro tip:** 大きな図面の描画速度を向上させるには、`rasterizationOptions.BackgroundColor` を単色に設定したり、`rasterizationOptions.DrawType` を有効にしてベクトル変換を高速化することもできます。

### ステップ 4: 結果画像の PNG オプション作成  
ラスタライズ設定を `PngOptions` オブジェクトでラップし、Aspose.CAD に PNG ファイルを出力させます。

```csharp
// Create an instance of PngOptions for the resultant image
ImageOptionsBase options = new Aspose.CAD.ImageOptions.PngOptions();
// Set rasterization options
options.VectorRasterizationOptions = rasterizationOptions;
```

### ステップ 5: 結果の PNG を保存  
ディレクトリパスと希望するファイル名を結合し、ラスタライズされた画像をディスクに書き込みます。このステップで **CAD を PNG として保存** します。

```csharp
MyDir = MyDir + "conic_pyramid_raster_image_out.png";
// Save resultant image
image.Save(MyDir, options);
```

### ステップ 6: 成功メッセージの表示  
変換が成功したことを確認し、ファイルが保存された場所を表示します。

```csharp
//ExEnd:ConvertDrawingToRasterImage            
Console.WriteLine("\nCAD drawing converted successfully to raster image format.\nFile saved at " + MyDir);
```

> **Note:** ステップ 2 の `using` ブロックは `Image` オブジェクトを自動的に破棄し、すべてのリソースが解放されることを保証します。

## 一般的な問題と解決策

| 問題 | 原因 | 対策 |
|-------|-------|-----|
| **空白の PNG 出力** | ラスタライズオプションが設定されていない（例: `PageWidth`/`PageHeight` が未指定）。 | `CadRasterizationOptions` がゼロでないキャンバスサイズを定義していることを確認してください。 |
| **色が正しくない** | 背景色がデフォルトで白になっており、元の図面が透明レイヤーを使用しています。 | `rasterizationOptions.BackgroundColor = Color.Transparent;` を設定してください。 |
| **大きな DWG ファイルでのパフォーマンス低下** | タイル処理なしの高解像度。 | `rasterizationOptions.LayoutOptions` を使用して描画領域を制限するか、DPI を下げてください。 |
| **ライセンス例外** | 本番環境で有効なライセンスなしで実行している。 | 画像をロードする前に `License license = new License(); license.SetLicense("Aspose.CAD.lic");` でライセンスを適用してください。 |

## よくある質問

### Q1: Aspose.CAD はすべての CAD ファイル形式に対応していますか？
**A1:** Aspose.CAD は DWG、DXF、DGN などを含む幅広い CAD ファイル形式をサポートしています。包括的な一覧は [ドキュメント](https://reference.aspose.com/cad/net/) を参照してください。

### Q2: プロジェクトごとにラスタライズオプションをカスタマイズできますか？
**A2:** はい、Aspose.CAD はラスタライズオプションを幅広くカスタマイズでき、開発者はプロジェクト要件に合わせて出力を調整できます。

### Q3: Aspose.CAD の無料トライアルはありますか？
**A3:** はい、無料トライアルで Aspose.CAD の機能を試すことができます。[こちら](https://releases.aspose.com/) から開始してください。

### Q4: Aspose.CAD のサポートはどこで受けられますか？
**A4:** サポートや質問は Aspose.CAD の [サポートフォーラム](https://forum.aspose.com/c/cad/19) へご相談ください。

### Q5: Aspose.CAD の一時ライセンスは利用できますか？
**A5:** はい、開発者は [このリンク](https://purchase.aspose.com/temporary-license/) から Aspose.CAD の一時ライセンスを取得できます。

### Q6: この方法で **DWG を PNG に変換** することもできますか？
**A6:** もちろんです。同じコードは DWG ファイルでも動作します。ソースファイルの拡張子を `.dwg` に変更するだけです。

### Q7: 透明な背景で **DXF を画像にエクスポート**するには？
**A7:** PNG を保存する前に `rasterizationOptions.BackgroundColor = Color.Transparent;` を設定してください。

---

**最終更新日:** 2026-03-19  
**テスト環境:** Aspose.CAD 24.11 for .NET (latest release)  
**作成者:** Aspose  

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}