---
date: 2026-03-21
description: .NET 用 Aspose.CAD を使用して、dxf を png やその他のラスタ形式に変換する方法を学びましょう。シームレスな CAD
  レイヤーエクスポートのためのステップバイステップガイドをご覧ください。
linktitle: Export CAD Layouts to Raster Image Formats
second_title: Aspose.CAD .NET - CAD and BIM File Format
title: .NET 用 Aspose.CAD で DXF を PNG に変換
url: /ja/net/cad-export-formats/export-cad-layouts-to-raster-image-formats/
weight: 10
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Aspose.CAD for .NET で CAD レイアウトをラスタ画像形式にエクスポートする

## はじめに

Aspose.CAD for .NET を使用して **convert dxf to png** やその他のラスタ画像形式を効率的に変換したいですか？このステップバイステップガイドでは、プロセスを順を追って説明し、詳細な手順とコードスニペットを提供して作業をシームレスにします。経験豊富な開発者でも Aspose.CAD の初心者でも、このチュートリアルはすべてのレベルに対応しています。

### クイック回答
- **変換を処理するライブラリは何ですか？** Aspose.CAD for .NET  
- **標準でサポートされている主な形式は？** JPEG、PNG、BMP、TIFF ラスタ画像  
- **特定の CAD レイヤーをエクスポートできますか？** はい – `CadRasterizationOptions.Layers` を使用して個別レイヤーを対象にできます  
- **本番環境でライセンスが必要ですか？** 非トライアル使用には有効な Aspose.CAD ライセンスが必要です  
- **サポートされている .NET バージョンは？** .NET Framework 4.5 以上、.NET Core 3.1 以上、.NET 5/6/7  

## **convert dxf to png** とは何ですか？

DXF（Drawing Exchange Format）ファイルを PNG に変換することは、ベクターベースの CAD データをピクセルベースの画像にラスタライズすることを意味します。これは、CAD 図面をウェブページやレポート、ラスタ画像しかサポートしない環境に埋め込む必要がある場合に便利です。

## なぜ CAD レイヤーを個別にエクスポートするのですか？

CAD レイヤーを個別にエクスポートすると、ビジュアル出力を細かく制御でき、各画像のファイルサイズを削減でき、レイヤー固有のスタイリングや後処理を適用できます。特に、大規模なエンジニアリング図面で、特定のオーディエンスに関連するレイヤーだけが必要な場合に有用です。

## 前提条件

チュートリアルに入る前に、以下を用意してください。

- **Aspose.CAD for .NET ライブラリ** – [Aspose.CAD ウェブサイト](https://releases.aspose.com/cad/net/) からダウンロード。  
- **CAD 図面ファイル** – ラスタ形式に変換したい DXF ファイル（例: `conic_pyramid.dxf`）。  

## 名前空間のインポート

.NET プロジェクトで Aspose.CAD の機能を活用するために、必要な名前空間をインポートします。コードの先頭に以下の名前空間を追加してください。

```csharp
using System;
using System.Collections.Generic;
using System.Linq;
using System.Text;
using System.Threading.Tasks;
using Aspose.CAD;
```

## **convert dxf to png** の手順 – ステップバイステップガイド

### ステップ 1: CAD 図面の読み込み

まず、DXF ファイルを `Image` オブジェクトにロードします。このオブジェクトはメモリ上で CAD 図面全体を表します。

```csharp
string MyDir = "Your Document Directory";
string sourceFilePath = MyDir + "conic_pyramid.dxf";

// Load a CAD drawing in an instance of Image
using (var image = Image.Load(sourceFilePath))
{
    // Your code for loading the CAD drawing goes here
}
```

### ステップ 2: `CadRasterizationOptions` の作成

出力サイズや解像度など、ラスタライズ設定を構成します。これらのオプションはベクターデータのラスタライズ方法を制御します。

```csharp
// Create an instance of CadRasterizationOptions
var rasterizationOptions = new CadRasterizationOptions();
rasterizationOptions.PageWidth = 500;
rasterizationOptions.PageHeight = 500;
```

### ステップ 3: レイヤーの指定（CAD レイヤーのエクスポート）

特定のレイヤーだけが必要な場合は、ここにレイヤー名を列挙します。これは **export cad layers** を個別に実行する例です。

```csharp
// Add the layer name to the CadRasterizationOptions's layer list
rasterizationOptions.Layers = new string[] { "LayerA" };
```

### ステップ 4: 画像形式の選択 – CAD を PNG（または JPEG）として保存

画像形式固有のオプションオブジェクトを作成します。**save cad as png** を行いたい場合は `JpegOptions` を `PngOptions` に置き換えてください。

```csharp
// Create an instance of JpegOptions (or any ImageOptions for raster formats)
var options = new JpegOptions();
options.VectorRasterizationOptions = rasterizationOptions;
```

> **Pro tip:** PNG ファイルを生成するには、`JpegOptions` の代わりに `new PngOptions()` をインスタンス化するだけです。

### ステップ 5: JPEG（または PNG）形式でエクスポート

最後に、ラスタライズされた画像をディスクに保存します。ファイル拡張子が出力形式を決定します。

```csharp
// Export each layer to Jpeg format
MyDir = MyDir + "CADLayersToRasterImageFormats_out.jpg";
image.Save(MyDir, options);
```

`JpegOptions` を `PngOptions` に置き換えると、同じコードで **convert dxf to png** が実行され、`.png` ファイルが生成されます。

### 追加ステップ: すべてのレイヤーを変換

図面内のすべてのレイヤーに対して **convert cad to raster** が必要な場合は、以下のヘルパーメソッドを呼び出してください。すべてのレイヤーを反復処理し、個別の画像として保存します。

```csharp
ConvertAllLayersToRasterImageFormats();
```

> *Note:* `ConvertAllLayersToRasterImageFormats` の実装は、完全な Aspose.CAD サンプルスイートの一部であり、レイヤーのバッチ処理を示しています。

## 一般的な問題とトラブルシューティング

| 症状 | 考えられる原因 | 対処法 |
|------|----------------|--------|
| 白または空白の画像 | ラスタライズオプションが設定されていない（例: `PageWidth`/`PageHeight` = 0） | `PageWidth` と `PageHeight` が正の値であることを確認してください |
| レイヤーが欠落している | `Layers` 配列のレイヤー名が正しくない | CAD ファイル内の正確なレイヤー名（大文字小文字を区別）を確認してください |
| 低品質の PNG | デフォルトの DPI が低い | 高品質にするには `rasterizationOptions.Resolution = 300;` を設定してください |

## よくある質問（オリジナル）

### Q1: エクスポートに他の画像形式を使用できますか？

A1: はい、可能です。`JpegOptions` を目的の形式のオプション（例: `PngOptions` や `BmpOptions`）に置き換えるだけです。

### Q2: トライアル版は利用可能ですか？

A2: はい、[こちら](https://releases.aspose.com/) からトライアル版をダウンロードして Aspose.CAD の機能を試すことができます。

### Q3: Aspose.CAD のサポートはどう受けられますか？

A3: コミュニティサポートは Aspose.CAD の [フォーラム](https://forum.aspose.com/c/cad/19) で利用できます。専用サポートが必要な場合はライセンス購入をご検討ください。

### Q4: 一時ライセンスは取得できますか？

A4: はい、[こちら](https://purchase.aspose.com/temporary-license/) から一時ライセンスを取得できます。

### Q5: ドキュメントはどこで確認できますか？

A5: 詳細なドキュメントは [こちら](https://reference.aspose.com/cad/net/) をご参照ください。

## 追加 FAQ

**Q: すべてのレイヤーを一括でエクスポートできますか？**  
A: はい、上記の `ConvertAllLayersToRasterImageFormats` メソッドを使用してください。

**Q: Aspose.CAD は SVG のようなベクタ形式をサポートしていますか？**  
A: 主にラスタ形式を対象としていますが、ベクタデータを保持したまま PDF にエクスポートすることは可能です。

**Q: エクスポートした PNG の背景色はどう制御しますか？**  
A: 保存前に `rasterizationOptions.BackgroundColor` に目的の `Color` を設定してください。

**Q: 図面全体ではなく単一のレイアウトだけをエクスポートできますか？**  
A: はい、`rasterizationOptions.Layouts` を設定して、ラスタライズしたいレイアウト名を指定します。

## 結論

これで **convert dxf to png**、**export cad layers**、および **save cad as png** や JPEG を Aspose.CAD for .NET を使用して実行する方法が分かりました。`CadRasterizationOptions` を調整し、画像形式オプションを切り替えることで、ほぼすべてのラスタ出力に対応できます。Aspose.CAD API の他の形式オプションも探索して、CAD‑to‑raster ワークフローをさらに拡張してください。

---

**最終更新日:** 2026-03-21  
**テスト環境:** Aspose.CAD for .NET 24.11（執筆時点での最新）  
**作者:** Aspose  

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}