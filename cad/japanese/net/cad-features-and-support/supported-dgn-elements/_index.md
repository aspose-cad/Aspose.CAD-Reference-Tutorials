---
date: 2026-03-29
description: Aspose.CAD for .NET を使用して DGN を PNG に変換する方法を学びましょう。このガイドでは、CAD ファイル形式のサポートと、サポートされている
  DGN 要素の全セットについても説明します。
linktitle: Supported DGN Elements
second_title: Aspose.CAD .NET - CAD and BIM File Format
title: .NET 用 Aspose.CAD で DGN を PNG に変換
url: /ja/net/cad-features-and-support/supported-dgn-elements/
weight: 18
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Aspose.CAD for .NET を使用した DGN から PNG への変換

## はじめに

.NET 開発者で、**DGN から PNG への変換**をシームレスに行いたいですか？ Aspose.CAD for .NET は、DGN ファイルを効率的に処理するための堅牢なソリューションを提供します。このチュートリアルでは、サポートされている DGN 要素を詳しく解説し、Aspose.CAD for .NET の使用方法とそれらの要素を PNG 画像にエクスポートする手順を示します。

## クイック回答
- **Aspose.CAD の機能は？** CAD/BIM ファイル（DGN を含む）を読み取り、変更し、PNG などのラスタ形式に変換します。  
- **2D と 3D の DGN 要素を変換できますか？** はい、2‑D と 3‑D のエンティティの両方がサポートされています。  
- **必要な .NET バージョンは？** .NET Framework 4.5+、.NET Core 3.1+、.NET 5/6+。  
- **テスト用にライセンスは必要ですか？** 無料トライアルが利用可能です。製品版ではライセンスが必要です。  
- **ライブラリはどこで入手できますか？** 公式 Aspose サイトからダウンロードしてください（下記リンク）。

## 「convert DGN to PNG」とは何か

DGN を PNG に変換するとは、ベクトルベースの DGN 図面（2‑D または 3‑D）をラスタ画像形式（PNG）にレンダリングすることを意味します。これにより、Web 上で CAD 図面を表示したり、レポートに埋め込んだり、CAD ビューアを必要とせずにサムネイルを生成したりすることが容易になります。

## CAD ファイル形式サポートに Aspose.CAD for .NET を使用する理由

- **完全な CAD ファイル形式サポート** – DGN、DWG、DXF、DWF など。  
- **外部依存なし** – 純粋な .NET ライブラリで、ネイティブ CAD のインストールは不要です。  
- **高忠実度レンダリング** – 線幅、色、3‑D ジオメトリを正確に保持します。  
- **バッチ処理** – サーバーサイドアプリケーションで多数のファイルを簡単にループ処理できます。

## 前提条件

開始する前に、以下が揃っていることを確認してください。

- .NET プログラミングの基本知識。  
- マシンにインストールされた Visual Studio。  
- Aspose.CAD for .NET ライブラリ（[here](https://releases.aspose.com/cad/net/) からダウンロード可能）。

## 名前空間のインポート

プロジェクトを開始するには、必要な名前空間を .NET アプリケーションにインポートします。この手順により、Aspose.CAD for .NET が提供する機能にアクセスできるようになります。

```csharp
using System;
using System.Collections.Generic;
using System.Linq;
using System.Text;
using System.Threading.Tasks;
using Aspose.CAD;
using Aspose.CAD.FileFormats.Dgn;
using Aspose.CAD.FileFormats.Dgn.DgnElements;
```

## DGN を PNG に変換する方法

以下は、DGN ファイルの読み込み、要素の反復処理、2‑D と 3‑D エンティティの処理、そして最終的に結果を PNG ラスタ画像としてエクスポートするまでの手順を示すステップバイステップガイドです。

### 手順 1: DGN ファイルの読み込み

まず、既存の DGN ファイルを .NET アプリケーション内で `DgnImage` として読み込みます。

```csharp
string MyDir = "Your Document Directory";
string sourceFilePath = MyDir + "Nikon_D90_Camera.dgn";

using (DgnImage dgnImage = (DgnImage)Image.Load(sourceFilePath))
{
    // Your code here
}
```

### 手順 2: DGN 要素の反復処理

`foreach` ループを使用して DGN 要素を反復処理します。Aspose.CAD for .NET は、操作可能なさまざまな DGN 要素タイプを提供しています。

```csharp
foreach (DgnDrawingElementBase element in dgnImage.Elements)
{
    // Your code here
}
```

### 手順 3: 以前サポートされていた 2‑D エンティティの処理

これらのエンティティは、現在 3‑D レンダリングでもサポートされています。`switch` 文を使用して要素タイプに応じたロジック分岐が可能です。

```csharp
switch (element.Metadata.Type)
{
    case DgnElementType.Line:
    case DgnElementType.Ellipse:
    case DgnElementType.Curve:
    // Additional cases
        {
            // Your code here
            break;
        }
}
```

### 手順 4: サポートされている 3‑D エンティティの処理

Aspose.CAD は、複数の 3‑D DGN エンティティを完全にサポートします。必要に応じて `switch` を拡張し、これらを処理してください。

```csharp
switch (element.Metadata.Type)
{
    case DgnElementType.SolidHeader3D:
    case DgnElementType.Cone:
    case DgnElementType.CellHeader:
        {
            // Your code here
            break;
        }
}
```

### 手順 5: PNG としてエクスポートおよび保存

必要な操作が完了したら、DGN 図面を PNG ラスタ画像としてエクスポートし、指定したディレクトリに保存します。

```csharp
Console.WriteLine("\nThe DGN file exported successfully to raster image.\nFile saved at " + MyDir);
```

> **プロのコツ:** `Image.Save` と `new PngOptions()` を使用して、解像度、背景色、その他の PNG 固有の設定を制御できます。

## CAD ファイル形式サポートの概要

Aspose.CAD for .NET は DGN に限定されません。DWG、DXF、DWF など多数の CAD 形式もサポートしており、幅広いエンジニアリング図面を扱える単一の API を提供します。これにより、複数の標準にわたる **CAD ファイル形式サポート** が必要なプロジェクトに最適です。

## よくある問題と解決策

| 問題 | 原因 | 対策 |
|-------|--------|-----|
| **画像が空白になる** | DPI が 0 のままエクスポートされた | `PngOptions` で `ResolutionX` と `ResolutionY` を指定してください。 |
| **3‑D ジオメトリが欠落** | `switch` で要素タイプが処理されていない | 欠落している `DgnElementType` ケースを追加し、適切にレンダリングしてください。 |
| **大きなファイルでメモリ不足** | ファイル全体を一度に読み込んでいる | 要素をバッチ処理するか、可能な場合はストリーミングを使用してください。 |

## よくある質問

### Q1: Aspose.CAD for .NET のドキュメントはどこで見つけられますか？
A1: ドキュメントは[here](https://reference.aspose.com/cad/net/) で確認できます。

### Q2: Aspose.CAD for .NET をダウンロードするには？
A2: ライブラリは[here](https://releases.aspose.com/cad/net/) からダウンロードできます。

### Q3: Aspose.CAD for .NET の無料トライアルはありますか？
A3: はい、無料トライアルは[here](https://releases.aspose.com/) で利用できます。

### Q4: Aspose.CAD for .NET の一時ライセンスはどこで取得できますか？
A4: 一時ライセンスは[here](https://purchase.aspose.com/temporary-license/) で入手可能です。

### Q5: サポートが必要ですか、質問がありますか？
A5: Aspose.CAD for .NET コミュニティの[サポートフォーラム](https://forum.aspose.com/c/cad/19)をご覧ください。

---

**最終更新日:** 2026-03-29  
**テスト環境:** Aspose.CAD for .NET 24.11  
**作者:** Aspose  

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}